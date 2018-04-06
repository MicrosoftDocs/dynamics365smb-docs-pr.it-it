---
title: 'Procedura: Ristrutturare le warehouse | Documenti Microsoft'
description: "È possibile che si desideri ristrutturare la warehouse e definire nuovi codici collocazione e nuove caratteristiche per le collocazioni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d2820513ec95c43464979effd85d5113359886ef
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="restructure-warehouses"></a>Ristrutturare warehouse
È possibile che si desideri ristrutturare la warehouse e definire nuovi codici collocazione e nuove caratteristiche per le collocazioni. Questo tipo di attività, in genere, non viene eseguita di frequente. È tuttavia possibile che si verifichino situazioni in cui si renda necessario eseguire una riclassificazione per raggiungere o mantenere una maggiore efficienza. Ad esempio:  

- potrebbe essere necessario utilizzare nuovi codici collocazione che consentano l'utilizzo di un sistema di acquisizione automatica dei dati, ad esempio, mediante PC palmari;  
- è possibile che la warehouse abbia acquistato un nuovo sistema di scaffalatura che offre nuove possibilità di immagazzinamento degli articoli;  
- è possibile che una società abbia modificato l'assortimento di articoli e abbia spostato la warehouse in una nuova ubicazione in conseguenza di questi cambiamenti.  

Se la warehouse prevede l'utilizzo delle collocazioni ma non di stoccaggi e prelievi guidati, ristrutturarla creando le nuove collocazioni che si desidera utilizzare in futuro.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a>Per ristrutturare una warehouse di base in cui vengono utilizzate solo collocazioni  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.  
2.  Nella Scheda dettaglio **Warehouse** impostare il campo **Selezione collocazioni di default** su **Ultima coll. usata**.  
3.  Spostare tutto il contenuto delle collocazioni correnti nelle collocazioni appena create.  

    1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni riclassificazione articolo**, quindi scegliere il collegamento correlato.  
    2.  Selezionare una riga delle registrazioni, quindi scegliere l'azione **Ottieni contenuto collocazione**.  
    3.  Nella Scheda Dettaglio **Contenuto collocazione** impostare, i filtri nei campi **Cod. ubicazione**, **Cod. collocazione** e **Nr. articolo** per specificare il contenuto che si desidera spostare.  
    4.  Scegliere il pulsante **OK** per completare una riga di registrazione.  
    5.  Nel campo **Nuovo cod. collocazione** selezionare la collocazione in cui si desidera spostare gli articoli.  
    6.  Ripetere i passaggi da b a e per tutto il contenuto collocazione che si desidera spostare.  
    7.  Scegliere l'azione **Registra**.  

In questo modo sono state svuotate le collocazioni in cui gli articoli erano contenuti. Le collocazioni di default per gli articoli risultano pertanto sostituite con le nuove collocazioni.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a>Per ristrutturare una warehouse avanzata in cui vengono utilizzati stoccaggi e prelievi guidati  

1.  Creare le nuove collocazioni che si desidera utilizzare in futuro. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md).  
2.  Spostare tutto il contenuto delle collocazioni correnti nelle collocazioni appena create.  

    1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni riclassificazione warehouse**, quindi scegliere il collegamento correlato.  
    2.  Per le collocazioni che non comportano veri e propri spostamenti di articoli, creare una riga per ciascuna delle collocazioni correnti in **Registrazioni riclass.whse.**, specificando il codice di collocazione precedente nel campo **Dal codice collocazione** e il nuovo codice di collocazione nel campo **A codice collocazione**.  
    3.  Se alcuni movimenti implicano spostamenti fisici che verranno effettuati dagli addetti al magazzino, utilizzare la funzione **Prospetti movimenti** per preparare le istruzioni di movimento anziché utilizzare le registrazioni di riclassificazione warehouse. Per ulteriori informazioni, vedere [Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Quando le collocazioni precedenti vengono svuotate, riclassificarle come collocazioni di tipo **QC** per assicurare che non siano incluse nei flussi dell'articolo.  

    1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.  
    2.  Selezionare la riga con l'ubicazione, quindi scegliere l'azione **Collocazioni**.  
    3.  Nella finestra **Collocazioni** immettere **QC** nel campo **Codice tipo collocazione** per ciascuna delle collocazioni precedenti svuotate nel passaggio 3 della procedura precedente.  

Sono state rimosse le collocazioni dal flusso warehouse e sono state riclassificate come collocazioni QC. Queste non dispongono dei campi di attività nella finestra **Tipi collocazione** selezionata e pertanto non vengono considerate dal flusso di articoli. Per ulteriori informazioni, vedere [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin"></a>Per eliminare una collocazione  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.  
2.  Selezionare l'ubicazione in cui si desidera eliminare collocazioni. Scegliere l'azione **Collocazioni**.  
3.  Selezionare le righe per le collocazioni che si desidera eliminare.  
4.  Scegliere l'azione **Elimina**.  

Se si sceglie il pulsante **Sì**, la collocazione viene eliminata in modo permanente, mentre il codice collocazione rimane invariato in tutti i movimenti warehouse.  

Se si desidera rinominare una collocazione in modo che vengano rinominati anche tutti i record ad essa associati, eseguire questa operazione nella finestra **Collocazioni**. I record includono il contenuto delle collocazioni, le righe attività warehouse, le righe attività warehouse registrate, le righe dei prospetti warehouse, le righe dei carichi warehouse, le righe dei carichi di warehouse registrati, le righe delle spedizioni warehouse, le righe delle spedizioni warehouse registrate e i movimenti warehouse.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a>Per rinominare una collocazione e modificare il codice collocazione in tutti i record  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.  
2.  Selezionare l'ubicazione in cui si desidera rinominare una collocazione o cambiare il codice collocazione e scegliere l'azione **Collocazioni**.  
3.  Selezionare la collocazione che si desidera modificare e immettere un nuovo codice collocazione nel campo **Codice**.  
4.  Scegliere il pulsante **Sì**.  

> [!NOTE]  
>  Se si sceglie **Sì** ed esistono numerosi movimenti relativi alla collocazione, ad esempio nel caso in cui non si sia provveduto ad eliminare periodicamente i vecchi documenti di warehouse, l'operazione di ridenominazione dei record potrebbe richiedere diverso tempo. Pertanto, se si utilizza questo metodo, si consiglia di eseguire il processo batch **Elimina doc. whse. registrati** prima di avviare il processo di ridenominazione. Si tenga inoltre presente che questo processo batch consente di eliminare solo stoccaggi, prelievi e movimentazioni.  
>   
>  Se si rinomina una collocazione di carico o una collocazione di spedizione, verranno rinominati tutti i carichi registrati o le spedizioni registrate riferiti alla collocazione in questione.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

