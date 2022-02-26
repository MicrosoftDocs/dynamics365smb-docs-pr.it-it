---
title: 'Procedura: Stoccare articoli con gli stoccaggi warehouse | Documenti Microsoft'
description: Scopri i diversi modi per stoccare gli articoli in Business Central con le seguenti attività Stoccaggi warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 0f4dbac3c3131cf31690710cba9457e7508acad5
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438084"
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Eseguire lo stoccaggio con Stoccaggi warehouse:
Quando l'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi e dei carichi warehouse, è possibile utilizzare la funzionalità relativa ai documenti di stoccaggio warehouse per controllare lo stoccaggio degli articoli.  

Quando si registra un carico warehouse, i documenti di origine, ad esempio ordini di acquisto, ordini di trasferimento in entrata oppure ordini di reso vendita, vengono aggiornati, la quantità ricevuta viene registrata nei movimenti contabili articoli e le righe relative agli articoli ricevuti vengono inviate alla funzione di stoccaggio nella warehouse. Se si utilizzano stoccaggi e prelievi guidati, le righe per lo stoccaggio possono essere create anche tramite stoccaggio guidato.  

A seconda del setup della warehouse, le righe vengono rese disponibili nel prospetto stoccaggi oppure utilizzate per creare immediatamente delle istruzioni di stoccaggio. Per ulteriori informazioni, vedere [Pianificare stoccaggi nei prospetti](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Oltre ai metodi standard per creare stoccaggi warehouse descritti in questo argomento, è possibile creare uno stoccaggio a partire dal carico warehouse registrato correlato. Questo è utile se sono state eliminate le righe di stoccaggio oppure si utilizzano stoccaggi e prelievi guidati e si è stabilito di non utilizzare il prospetto stoccaggi, poiché è possibile creare o ricreare istruzioni di stoccaggio dalle righe di carico registrate.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Per eseguire lo stoccaggio di articoli senza utilizzare stoccaggi e prelievi guidati  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi**, quindi scegli il collegamento correlato.  
2.  Aprire lo stoccaggio warehouse pronto per la gestione.  

    È possibile ordinare le righe stoccaggio in base a diversi criteri, ad esempio per articolo, numero di scaffale o data di scadenza, e ottimizzare di conseguenza il processo di stoccaggio.  
3.  In ciascuna riga nel campo **Qtà da gestire** immettere la quantità che si desidera stoccare.  
4.  Dopo aver completato lo stoccaggio degli articoli, scegliere l'azione **Registra stoccaggio** per registrare il completamento dell'attività e rendere gli articoli disponibili per il prelievo.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Per eseguire lo stoccaggio di articoli utilizzando stoccaggi e prelievi guidati  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi**, quindi scegli il collegamento correlato.
    Se sono state create istruzioni di stoccaggio, verrà visualizzato uno stoccaggio nella warehouse.  
2.  Aprire lo stoccaggio warehouse che si desidera utilizzare.  
3.  Quando si inizia a lavorare su un stoccaggio specifico, immettere il proprio ID utente nella Scheda dettaglio **Generale**, se richiesto.  
4.  Eseguire le azioni Prendere e Mettere indicate nelle righe del campo **Tipo azione**.  

    Si tenga presente che a ciascuna riga di carico corrispondono almeno due righe di stoccaggio nella warehouse:  

    -   La prima riga, in cui il campo **Tipo azione** è impostato su **Prendere**, indica l'ubicazione degli articoli nell'area di carico. Non è possibile modificare il campo relativo alla zona e alla collocazione in questa riga.  
    -   Nelle righe successive, in cui il campo **Tipo azione** è impostato su **Mettere**, viene indicata la posizione in cui inserire gli articoli nell'area di immagazzinamento. Se la warehouse ha ricevuto un numero elevato di articoli in una riga di carico, è possibile che tali articoli debbano essere stoccati in diverse collocazioni, a ciascuna delle quali corrisponde una riga Mettere.  

        Se si desidera che le righe Prendere e Mettere per ciascuna riga di carico non siano consecutive, è possibile ordinarle selezionando **Articolo** nel campo **Metodo ordinamento** della Scheda dettaglio **Generale**.  

        Se la disposizione fisica della warehouse riflette le valutazioni delle collocazioni, è possibile utilizzare il metodo di ordinamento **Valutazione collocazione** per preparare un percorso di stoccaggio che consentirà di ridurre le operazioni da eseguire all'interno della warehouse.  

5.  Una volta posizionati tutti gli articoli nelle collocazioni, come indicato nelle istruzioni, scegliere l'azione **Registra stoccaggio**.  

Nelle ubicazioni impostate per l'utilizzo di stoccaggi e prelievi guidati, le impostazioni che seguono sono prerequisiti per la procedura precedente:  

- Viene impostato un modello di stoccaggio. Per ulteriori informazioni, vedere [Impostare i modelli di stoccaggio](warehouse-how-to-set-up-put-away-templates.md).  
- Vengono definiti il peso, la cubatura e i requisiti di immagazzinamento speciali relativi all'articolo o all'unità di stockkeeping. Per ulteriori informazioni, vedere Peso lordo.  
- La capacità, il tipo di collocazione e la valutazione delle collocazioni. Per ulteriori informazioni, vedere Valutazione collocazione.  

La valutazione della collocazione viene presa in considerazione quando più collocazioni soddisfano i criteri del modello di stoccaggio. Se i criteri del modello di stoccaggio e la valutazione della collocazione sono gli stessi per più di una collocazione, viene scelta la collocazione con il numero più alto.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Per creare uno stoccaggio a partire dal carico registrato  
 Se l'ubicazione è impostata per l'elaborazione degli stoccaggi e dei carichi e sono state eliminate le righe di stoccaggio oppure si utilizzano stoccaggi e prelievi guidati e si è stabilito di non utilizzare il prospetto stoccaggi, è possibile creare o ricreare istruzioni di stoccaggio per le righe di carico registrate.

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi whse. registrati**, quindi seleziona il collegamento correlato.  
2.  Selezionare un carico registrato che deve essere stoccato.  
3.  Scegliere l'azione **Scheda**.  

    Se il campo **Stato del documento** è vuoto, ciò indica che il carico non è stato assolutamente stoccato. In caso contrario, il campo indica che il carico è parzialmente o completamente stoccato.  

4.  Se il carico non è stato stoccato o è stato stoccato solo parzialmente, scegliere l'azione **Crea stoccaggio**.  
5.  Immettere le informazioni appropriate nella pagina di richiesta del processo batch per creare lo stoccaggio, quindi scegliere **OK**.   

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]