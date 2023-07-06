---
title: 'Dettagli di progettazione: Progettazione tracciabilità articolo'
description: In questo argomento viene descritta la progettazione alla base della tracciabilità articolo in Business Central man mano che matura attraverso le versioni del prodotto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a>Dettagli di progettazione: Progettazione tracciabilità articolo

Tracciabilità articolo in [!INCLUDE[prod_short](includes/prod_short.md)] avviata con [!INCLUDE [navnow_md](includes/navnow_md.md)]. La funzionalità di tracciabilità articolo si trova in una struttura di oggetti separata con collegamenti complessi a documenti registrati e movimenti contabili articoli ed è integrata con il sistema di prenotazione, che gestisce la prenotazione, la tracciabilità degli ordini e la messaggistica di azione. Per ulteriori informazioni, vedi [Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md) in Dettagli progettazione: Pianificazione degli approvvigionamenti.  

Questa progettazione incorpora i movimenti di tracciabilità articolo nei calcoli della disponibilità totale in tutto il sistema, inclusa la pianificazione, la produzione e il warehouse. I numeri seriali e di lotto sono applicati nei movimenti contabili articoli per garantire il semplice accesso ai dati storici a scopo di tracciabilità. Con il primo ciclo di rilascio del 2021, il monitoraggio degli articoli in [!INCLUDE [prod_short](includes/prod_short.md)] include i numeri di pacchetto.  

Con l'aggiunta dei numeri seriali, di lotto e di pacchetto gli attributi permanenti dell'articolo vengono gestiti dal sistema di impegno contemporaneamente alla gestione dei collegamenti intermittenti tra approvvigionamento e domanda sotto forma di movimenti di tracciabilità ordini e di movimenti impegni. Un'altra caratteristica diversa dei numeri seriali o di lotto confrontati ai dati di impegno convenzionali è il fatto che possono essere registrati, parzialmente o completamente. Di conseguenza, la tabella **Movimenti impegni** (T337) utilizza ora una tabella correlata denominata **Specifica tracciabilità** (T336) che gestisce e visualizza le somme delle quantità di tracciabilità articolo registrate e attive. Per ulteriori informazioni, vedere [Dettagli di progettazione: Movimenti di tracciabilità articolo storici e attivi](design-details-active-versus-historic-item-tracking-entries.md).  

Nel diagramma seguente viene descritta la progettazione della funzionalità di tracciabilità articolo in [!INCLUDE[prod_short](includes/prod_short.md)].  

![Esempio di flusso di tracciabilità articolo.](media/design_details_item_tracking_design.png "Esempio di flusso di tracciabilità articolo")  

L'oggetto di registrazione centrale è riprogettato per gestire la sottoclassificazione univoca di una riga di documento sotto forma di numero seriale o di numeri di lotto. Speciali tabelle di relazione vengono aggiunte per creare relazioni uno a molti tra i documenti registrati e i relativi movimenti contabili articoli e movimenti contabili di valorizzazione.  

Codeunit 22, **Reg. magazzino - registra righe**, ora suddivide la registrazione in base ai numeri di tracciabilità articolo specificati nella riga del documento. Ciascun numero di tracciabilità articolo sulla riga crea il proprio movimento contabile articolo per l'articolo. Ciò significa che il collegamento dalla riga del documento registrato ai movimenti contabili articoli associati è una relazione uno a molti. Tale relazione viene gestita dalle seguenti tabelle di relazione di tracciabilità articolo.  

|Campo|Descrizione|  
|---------------|---------------------------------------|  
|**Relazione movimento articolo** (T6507)|Correla la righe spedite o ricevute ai movimenti contabili articoli|  
|**Relazione movimento valorizz.** (T6508)|Correla le righe fatturate ai movimenti di valorizzazione|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Struttura di registrazione di tracciabilità articolo](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
