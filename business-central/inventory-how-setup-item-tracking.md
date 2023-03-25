---
title: 'Configurare la tracciabilità di articoli con numeri di serie, di lotto e di pacco'
description: 'Configura la tracciabilità di articoli con numeri di serie, di lotto e di pacco'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: edupont
---
# Configurare la tracciabilità di articoli con numeri di serie, di lotto e di pacco

Tieni traccia degli articoli di magazzino anche in configurazioni di magazzino complesse con numeri specifici per ogni articolo, sia come singolo oggetto, come lotto o come pacchetto. Con la tracciabilità degli articoli, è possibile tracciare gli articoli nei movimenti del magazzino interno e nei documenti in uscita e in entrata.

Gli articoli con numeri seriali e di lotto che possono essere analizzati sia in avanti che indietro nella catena di catena di approvvigionamento. Ciò risulta utile per un controllo della qualità generale e per la restituzione dei prodotti. Per ulteriori informazioni, vedere [Analizzare articoli tracciati](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> Nel primo ciclo di rilascio del 2021 e in quelli successivi, attiva l'aggiornamento della funzionalità *Utilizzare la tracciabilità per numero di collo nel sistema di prenotazione e tracciabilità* se desideri lavorare con i numeri di pacchetto, nonché con i numeri di serie e di lotto. Per ulteriori informazioni, vedi [Abilitazione di funzionalità imminenti in anticipo](admin-feature-management.md). Una volta attivata la funzione, puoi assegnare i numeri di pacchetto ai documenti in uscita e in entrata in modo simile a come puoi lavorare con i numeri di lotto.  

## Numeri e tracciabilità degli articoli

Come parte dei processi di magazzino, puoi raggruppare le scorte in pacchi, scatole, contenitori e così via. Ma per tenere traccia degli articoli, assegni numeri univoci come identificazione. Ad esempio, produci e vendi una sedia con il numero articolo *1.900-S*. Ogni singola sedia ha un numero di serie, *1.001*, ma raccogli anche quattro sedie in un lotto, *LOT0001* e spedisci le sedie in un contenitore con il numero del pacco *CONTENITORE010* che include anche altri elementi, come *LOT0100* con tavolini e *LOTTO200* con lampade.  

A seconda della configurazione, utilizzi questi numeri diversi per tenere traccia del magazzino in [!INCLUDE [prod_short](includes/prod_short.md)] nelle varie fasi di acquisto, vendita, operazioni di magazzino e così via.

## Per impostare i codici di tracciabilità articolo

Un codice di tracciabilità articolo riflette i diversi criteri che una società può seguire nell'uso dei numeri seriali e di lotto degli articoli spostati all'interno di un magazzino.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici tracciabilità articolo**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Sul **Numero di serie**, **Numero di lotto** e **Numero pacchetto** Definire i criteri di tracciabilità degli articoli rispettivamente in base al numero seriale, di lotto e di pacchetto.  

> [!NOTE]  
> Per tenere traccia degli articoli specifici o i lotti specifici durante il ciclo di vita, scegliere i campi **Tracciabilità NS specifico** e **Tracciab. lotto specifico** rispettivamente. Di conseguenza nella gestione di un'unità in uscita di un articolo con il codice di tracciabilità articolo, è necessario specificare sempre quale numero seriale esistente o numero di lotto esistente gestire. Ciò significa che, durante la vendita di un'unità dell'articolo, è necessario collegare tale unità a uno specifico gruppo di numeri seriali o numero di lotto in magazzino. In altri termini, è necessario che un numero seriale o numero di lotto assegnato a un articolo durante l'inserimento in magazzino resti sempre collegato a quel tipo di articolo anche al di fuori del magazzino.

Poiché questo specifico campo di setup copre tutte le possibili transazioni eseguibili per l'articolo, anche nei singoli campi In Entrata/In Uscita verrà selezionato. Tuttavia, i campi In Entrata/In Uscita non riguardano gli eventuali collegamenti all'interno del magazzino, bensì consentono unicamente di definire il workflow aziendale relativo all'assegnazione dei numeri di tracciabilità articolo.  

> [!NOTE]  
>  Per assegnare i numeri di tracciabilità articolo nelle attività di warehouse, i campi **Tracciab. NS in warehouse** e **Tracciab. lotto in warehouse** devono essere selezionate nella scheda del codice di tracciabilità articolo.  

## Per impostare le regole di scadenza per i numeri seriali e di lotto

Per alcuni articoli potrebbe essere necessario impostare date e regole di scadenza specifiche nel codice di tracciabilità articolo. Questa funzionalità consente di tenere traccia della scadenza di determinati numeri seriali e di lotto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici tracciabilità articolo**, quindi scegli il collegamento correlato.
2. Selezionare un codice di tracciabilità articolo esistente quindi scegliere l'azione **Modifica**.  
3. Nella Scheda dettaglio **Varie** selezionare i seguenti campi:  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Registrazione scadenza vincolante**|Specifica che una data di scadenza assegnata al numero di tracciabilità articolo al momento dell'inserimento in magazzino deve essere rispettata all'uscita dal magazzino.|  
    |**Richiedi inserimento data di scadenza**|Specifica che è necessario immettere una data di scadenza nella riga di tracciabilità articolo.|  
    |**Usa date di scadenza**|Specifica che si intendono calcolare date di scadenza. |  

## Per impostare le garanzie per i numeri seriali o di lotto

Per alcuni articoli potrebbe essere necessario impostare garanzie specifiche nel codice di tracciabilità articolo. Questa funzionalità consente di tenere traccia della scadenza delle garanzie per determinati numeri seriali o di lotto presenti in magazzino.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici tracciabilità articolo**, quindi scegli il collegamento correlato.  
2. Selezionare un codice di tracciabilità articolo esistente quindi scegliere l'azione **Modifica**.  
3. Nella Scheda dettaglio **Varie** compilare il campo **Formula data garanzia** e selezionare i campi come indicato di seguito:  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Formula data garanzia**|Specifica l'ultimo giorno di garanzia per l'articolo.|  
    |**Richiedi inserimento data garanzia**|Specifica che è necessario immettere manualmente una data di garanzia nella riga di tracciabilità articolo.|  


## Per impostare gli articoli per la tracciabilità con i codici di tracciabilità articolo corretti

Per abilitare la tracciabilità degli articoli devi prima assegnare i codici di tracciabilità articolo a un articolo. Esistono due modi per aggiungere codici di tracciabilità articolo: selezionando il codice in un elenco predefinito o assegnando un nuovo codice univoco. Passa con il mouse sui campi per visualizzare una breve descrizione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articolo**, quindi scegli il collegamento correlato.
2. Seleziona un articolo esistente nell'elenco e apri la pagina **Scheda articolo**.  
3. Nella Scheda dettaglio **Tracciabilità articolo**, assegna i codici di tracciabilità articolo appropriati e specifica dei valori nei campi **Codice tracciabilità articolo**, **Nr. seriali** e **Nr. lotti**.
    1. In alternativa puoi anche creare un nuovo codice di tracciabilità articolo selezionando l'azione **Nuovo**.

## Vedi il relativo [training Microsoft](/training/modules/prepare-item-tracking/)

## Vedere anche

[Utilizzare i numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
