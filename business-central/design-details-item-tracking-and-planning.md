---
title: Dettagli di progettazione - Tracciabilità e pianificazione degli articoli | Microsoft Docs
description: 'Poiché sono memorizzati nel sistema di prenotazione, i numeri di tracciabilità degli articoli sono completamente coordinati con i record di tracciabilità degli ordini.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Dettagli di progettazione: Tracciabilità articolo e pianificazione
Poiché sono memorizzati nel sistema di prenotazione, i numeri di tracciabilità degli articoli sono completamente coordinati con i record di tracciabilità degli ordini. Ciò significa che agli articoli con record di tracciabilità ordini possono essere assegnati numeri di tracciabilità articoli. Al contrario, gli articoli con numeri di tracciabilità articolo possono diventare record di tracciabilità ordini. Per altre informazioni, vedere [Dettagli di progettazione - Progettazione tracciabilità articolo](design-details-item-tracking-design.md).

Per ulteriori informazioni sui sistemi integrati, vedere [Dettagli di progettazione - Prenotazioni, monitoraggio degli ordini e messaggi di azione](design-details-reservation-order-tracking-and-action-messaging.md).

Poiché la tracciabilità degli ordini riguarda solo l'applicazione di articoli specifici, il coordinamento con i numeri di tracciabilità degli articoli si applica solo agli articoli impostati per utilizzare la tracciabilità di articoli specifici. Questo comportamento è impostato dai campi **Tracciabilità NS specifico** e **Tracciabilità lotto specifico** sulla scheda oggetto, che specificano quanto segue:

- L'articolo deve contenere un numero di serie o un numero di lotto quando viene registrato.
- L'articolo deve essere applicato allo stesso numero di serie o numero di lotto quando viene registrato in uscita.

In linea con i principi di bilanciamento domanda/offerta standard, il sistema di pianificazione e la relativa funzionalità di tracciabilità degli ordini corrispondono ai numeri di tracciabilità articolo che forniscono articoli e domanda solo se l'articolo in questione utilizza una tracciabilità articolo specifico. In tutti gli altri casi, i sistemi di pianificazione e tracciabilità degli ordini ignorano i numeri di tracciabilità degli articoli quando applicano l'offerta per soddisfare la domanda o applicano la domanda all'offerta. Per ulteriori informazioni, vedere [Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md).

Ad esempio, quando esiste la tracciabilità dell'ordine per un determinato articolo, ciò implica che i record per l'articolo sono già nella tabella **Movimenti impegni** che è il nucleo del sistema di prenotazione, prima che vengano definiti i numeri di tracciabilità dell'articolo. Pertanto, le seguenti restrizioni di accoppiamento si applicano ai numeri di tracciabilità articolo da tracciare ordine:

- La domanda con un numero di serie o numero di lotto può coprire solo l'offerta con lo stesso numero di serie o numero di lotto.
- La domanda senza un numero di serie o di lotto può coprire qualsiasi offerta, con o senza un numero di serie o di lotto.

Oltre alle loro conseguenze sulla tracciabilità dinamica degli ordini, le restrizioni sull'associazione della tracciabilità degli articoli non influiscono in modo significativo sul sistema di pianificazione.

Dal lato dell'offerta, in genere un numero di serie o di lotto non viene inserito fino a subito prima della registrazione dell'ordine, ad esempio una ricevuta di acquisto nel magazzino. Quando si inserisce un numero di serie o di lotto sul lato della domanda, ad esempio in un ordine cliente, quel numero di serie o di lotto è già in inventario. Di conseguenza, i numeri di tracciabilità degli articoli in genere non rappresentano un problema nella pianificazione dell'offerta.

Per gli articoli che utilizzano la tracciabilità specifica degli articoli, tutta la domanda che trasporta numeri seriali o di lotto deve corrispondere all'offerta corrispondente. Nella maggior parte dei casi, non ha senso riordinare un numero di serie o di lotto specifico, quindi la pianificazione dell'acquisto o della produzione non è probabilmente influenzata. Tuttavia, quando si trasferiscono articoli da una posizione a un'altra, è probabile che il trasferimento avvenga per un lotto specifico, quindi la pianificazione degli approvvigionamenti potrebbe essere influenzata dalla specifica restrizione di accoppiamento.

Per ulteriori informazioni, vedere [Dettagli di progettazione - Trasferimenti nella pianificazione](design-details-transfers-in-planning.md).

## Bilanciamento della domanda e dell'offerta
Se un articolo richiede la tracciabilità di un articolo specifico, viene creato un collegamento di tracciabilità dell'ordine da tutta la domanda di tracciabilità dell'articolo a qualsiasi offerta di tracciabilità articolo corrispondente, con l'unica limitazione che l'offerta deve essere preceduta dalla domanda. Se, in tali circostanze, non viene trovata alcuna offerta di tracciabilità articolo che corrisponde alla domanda specifica di tracciabilità articolo, viene immediatamente creata una nuova offerta di tracciabilità articolo senza considerare il dimensionamento dell'ordine, i parametri di pianificazione o la riprogrammazione dell'offerta esistente dello stesso numero di serie o di lotto.

Se i numeri di tracciabilità degli articoli vengono assegnati sul lato della domanda o sul lato dell'offerta senza richiedere la tracciabilità specifica degli articoli, viene creato un collegamento di tracciabilità dell'ordine dalla domanda a quell'offerta, in base alla tempistica e alla quantità più adatte, come nella normale procedura di bilanciamento. Il numero di tracciabilità articolo specificato viene inserito nel record di tracciabilità ordine nello stesso modo in cui qualsiasi quantità di tracciabilità articolo specificata definisce un'estremità del collegamento di tracciabilità ordine. Ciò significa che il numero di tracciabilità dell'articolo inserito viene conservato mentre fa anche parte del record di tracciabilità dell'ordine.

Se i numeri di tracciabilità degli articoli vengono assegnati sul lato dell'offerta senza richiedere la tracciabilità specifica degli articoli, tale offerta viene considerata fissa dal sistema di pianificazione. Nessun ridimensionamento o riprogrammazione è suggerito per questa offerta, ma l'offerta viene presa in considerazione quando il sistema di pianificazione tenta di soddisfare i requisiti lordi.

Per altre informazioni, vedere [Dettagli di progettazione - Bilanciamento della domanda e dell'offerta](design-details-balancing-demand-and-supply.md).  

## Vedere anche  
[Dettagli di progettazione: Progettazione tracciabilità articolo](design-details-item-tracking-design.md)  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)  
[Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]