---
title: 'Procedura: Impostare le ore di lavoro e le ore di assistenza | Documenti Microsoft'
description: "È possibile specificare le ore lavorative solitamente dedicate all'assistenza nell'azienda. Le ore di assistenza vengono utilizzate per calcolare la data e l'ora di risposta per gli ordini e le offerte di assistenza e per inviare degli avvisi relativi all'ora di risposta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-hours-and-service-hours"></a>Impostare le ore di lavoro e le ore di assistenza
Solitamente, un sistema di gestione dell'assistenza tiene traccia delle ore delle risorse e dello stato dell'ordine di assistenza al fine di poter prevedere i carichi di lavoro e le esigenze di assistenza. [!INCLUDE[d365fin](includes/d365fin_md.md)] dispone di una serie di strumenti integrati che è possibile personalizzare per poter registrare questo tipo di informazioni.  
  
Una volta definite le ore di assistenza predefinite dell'azienda, è possibile calcolare i tempi di risposta per gli ordini di assistenza o inviare avvisi ogni volta che arrivano delle chiamate di assistenza. La funzionalità di avviso è implementata congiuntamente al job scheduler.   
  
Quando si lavora su un ordine di assistenza, si vorrà aggiornarne lo stato in modo da monitorare lo stato di avanzamento. Lo stato dell'ordine di assistenza corrisponde allo stato di riparazione degli articoli in assistenza nell'ordine di assistenza. Per ulteriori informazioni, vedere [Informazioni su stato assistenza e stato riparazione](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Per impostare le ore di assistenza di default  
La finestra **Ore di assistenza di default** consente di impostare le ore lavorative dedicate in genere all'assistenza nell'azienda. Le ore di assistenza vengono utilizzate per calcolare la data e l'ora di risposta per gli ordini e le offerte di assistenza e per inviare degli avvisi relativi all'ora di risposta. Le ore di assistenza di default vengono utilizzate per contratti di assistenza per cui non vengono impostate ore specifiche.  
  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ore di assistenza di default**, quindi scegliere il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Se le righe della finestra **Ore di assistenza di default** vengono lasciate vuote, il valore di default sarà pari a 24 ore, valido esclusivamente per i giorni lavorativi.  
  
## <a name="to-set-up-work-hour-templates"></a>Per impostare i modelli delle ore di lavoro
La finestra **Modelli Ore di Lavoro** consente di impostare modelli che contengano le ore medie di lavoro nell'azienda. Ad esempio è possibile creare modelli per tecnici full-time e part-time. È possibile utilizzare modelli ore di lavoro quando si aggiungono capacità alle risorse.  
  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modelli ore di lavoro**, quindi scegliere il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Dopo aver immesso le ore di lavoro per ogni giorno, il valore nel campo **Totale per settimana** viene calcolato automaticamente.  

## <a name="to-set-up-contract-specific-service-hours"></a>Per impostare le ore di assistenza specifiche del contratto  
La finestra **Ore Assistenza** consente di impostare ore di assistenza specifiche per il cliente titolare del contratto di assistenza. Le ore di assistenza vengono utilizzate per il calcolo della data e dell'ora di risposta per ordini e offerte di assistenza appartenenti al contratto di assistenza.  
  
Se non si impostano ore di assistenza specifiche per il contratto di assistenza, verranno utilizzate quelle di default per i contratti di assistenza.  
  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Contratti assistenza**, quindi scegliere il collegamento correlato.  
2. Aprire il contratto di assistenza per cui si desidera impostare delle ore di assistenza specifiche, quindi scegliere **Ore assistenza**.  
4. Per impostare le ore di assistenza in base alle ore di assistenza di default, scegliere l'azione **Copia ore assist. di default**.  
5. Modificare i campi nei movimenti ore di assistenza. Inserire o eliminare i movimenti per impostare le ore di assistenza per il contratto. Si noti che i campi **Giorno**, **Ora inizio** e **Ora fine** sono obbligatori per ogni riga.  
6. Se si desidera che le ore di assistenza siano valide a partire da una data specifica, compilare il campo **Data inizio**.  
7. Se si desidera che le ore di assistenza siano valide anche durante i giorni festivi, immettere un segno di spunta nel campo **Valido nei Giorni Festivi**.  

## <a name="see-also"></a>Vedi anche  
[Informazioni su stato assegnazione e stato riparazione](service-allocation-status-and-repair-status.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  
[Informazioni su stato assistenza e stato riparazione](service-order-repair-status.md)  

