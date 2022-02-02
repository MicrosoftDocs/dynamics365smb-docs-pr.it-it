---
title: Dettagli di progettazione - Panoramica warehouse
description: Per supportare la gestione fisica degli articoli a livello di collocazione e di zona, è necessario tenere traccia di tutte le informazioni per ogni transazione o spostamento nella warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 49c25082d8f43210011cc7f482c4f4af330c1a19
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011600"
---
# <a name="design-details-warehouse-overview"></a>Dettagli di progettazione: Panoramica warehouse
Per supportare la gestione fisica degli articoli a livello di collocazione e di zona, è necessario tenere traccia di tutte le informazioni per ogni transazione o spostamento nella warehouse. Le informazioni sono gestite nella tabella **Movimento warehouse**. Ogni transazione viene memorizzata in un registro warehouse.  

I documenti warehouse e le registrazioni di warehouse vengono utilizzati per registrare i movimenti degli articoli nella warehouse. Ogni volta che viene spostato, ricevuto, stoccato, selezionare, spedito o rettificato un articolo nel magazzino, i movimenti di magazzino vengono registrati per archiviare le informazioni fisiche sull'area, la collocazione e la quantità.

La tabella **Contenuto collocazione** viene utilizzata per gestire tutte le dimensioni diverse del contenuto di una collocazione per articolo, ad esempio l'unità di misura, la quantità massima e quella minima. La tabella **Contenuto collocazione** contiene anche campi di flusso ai movimenti della warehouse, istruzioni di warehouse e righe delle registrazioni di warehouse, grazie ai quali è possibile calcolare rapidamente la disponibilità di un articolo per collocazione e la collocazione per un articolo. Per ulteriori informazioni, vedere [Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md).  

Quando le registrazioni degli articoli avvengono in una posizione diversa dal modulo warehouse, viene utilizzata una collocazione di rettifica predefinita per ubicazione per sincronizzare i movimenti warehouse con i movimenti di magazzino. Durante l'inventario fisico del magazzino, tutte le differenze tra le quantità calcolate e quelle conteggiate vengono registrate nella collocazione di rettifica e quindi registrate come movimenti contabili articoli di rettifica. Per ulteriori informazioni, vedere [Dettagli di progettazione: Integrazione con il magazzino](design-details-integration-with-inventory.md).  

Nell'illustrazione seguente sono descritti i tipici flussi di warehouse.  

![Panoramica dei processi della warehouse.](media/design_details_warehouse_management_overview.png "Panoramica dei processi della warehouse")  

## <a name="basic-or-advanced-warehousing"></a>Gestione avanzata o di base della warehouse  
La funzionalità di warehouse in [!INCLUDE[prod_short](includes/prod_short.md)] può essere implementata in diversi livelli di complessità, a seconda dei processi e del volume degli ordini di una società. La principale differenza consiste nel fatto che le attività sono eseguite ordine per ordine nella gestione di base della warehouse, mentre vengono eseguite al momento del consolidamento per più ordini nella gestione avanzata della warehouse.  

 Per differenziare tra i diversi livelli di complessità, questa documentazione fa riferimento a due termini generali, gestione di base della warehouse e gestione avanzata della warehouse. Questa semplice differenziazione copre numerosi livelli di complessità come definito dal setup dell'ubicazione e i sottoprodotti, ciascuno supportato da documenti di interfaccia utente differenti. Per ulteriori informazioni, vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md).  

> [!NOTE]  
>  Il livello più avanzato della gestione della warehouse è denominato "Installazioni WMS" in questa documentazione, poiché questo livello richiede la funzionalità più avanzata, vale a dire Sistema di gestione warehouse.  

 I seguenti documenti dell'interfaccia utente vengono utilizzati nelle gestioni di base e avanzata della warehouse.  

## <a name="basic-ui-documents"></a>Documenti di base dell'interfaccia utente  

-   **Stoccaggio in magazzino**  
-   **Prelievi magazzino**  
-   **Movimento di magazzino**  
-   **Reg. Magazzino**  
-   **Registrazioni riclassificazione articolo**  
-   (Vari report)  

## <a name="advanced-ui-documents"></a>Documenti dell'interfaccia utente avanzati  

-   **Carico warehouse**  
-   **Prospetto stoccaggi**  
-   **Stoccaggio warehouse**  
-   **Prospetto prelievi**  
-   **Prelievo warehouse**  
-   **Movimento worksheet**  
-   **Movimentazione warehouse**  
-   **Prelievo interno whse.**  
-   **Stocc. int. whse.**  
-   **Prospetto creaz. collocazione**  
-   **Prospetto creaz. cont. colloc.**  
-   **Registrazioni articoli whse.**  
-   **Reg. ricl. articoli whse**  
-   (Vari report)  

Per ulteriori informazioni su ogni documento, vedere i rispettivi argomenti della pagina.  

### <a name="terminology"></a>Terminologia  
Per allinearsi ai concetti finanziari di acquisti e vendite, la documentazione della warehouse di [!INCLUDE[prod_short](includes/prod_short.md)] si riferisce ai seguenti termini per il flusso degli articoli nella warehouse.  

|Termine|Description|  
|----------|---------------------------------------|  
|Flusso in entrata|Spostamento articoli nell'ubicazione della warehouse, ad esempio gli acquisti e i trasferimenti in entrata.|  
|Flusso interno|Spostamento articoli nell'ubicazione della warehouse, ad esempio i componenti di produzione e l'output.|  
|Flusso in uscita|Spostamento articoli all'esterno dell'ubicazione della warehouse, ad esempio le vendite e i trasferimenti in uscita.|  

## <a name="see-also"></a>Vedere anche  
 [Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]