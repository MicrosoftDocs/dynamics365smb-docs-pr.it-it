---
title: Sincronizzazione di Business Central e Common Data Service | Microsoft Docs
description: Ottenere informazioni sulla sincronizzazione di dati tra Business Central e Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cce95930cde316c5e233382effb0bb241b3b79fd
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196593"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Pianificazione di una sincronizzazione tra Business Central e Common Data Service
È possibile sincronizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[d365fin](includes/cds_long_md.md)] a intervalli pianificati impostando i processi nella coda processi. I processi di sincronizzazione sincronizzano i dati nei record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e nei record di [!INCLUDE[d365fin](includes/cds_long_md.md)] che sono stati associati in precedenza. Oppure per i record che non sono ancora associati, a seconda della direzione e delle regole di sincronizzazione, i processi di sincronizzazione possono creare e associare nuovi record nel sistema di destinazione. 

Esistono vari processi di sincronizzazione predefiniti disponibili. I processi sono eseguiti nel seguente ordine per evitare di associare dipendenze tra entità. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. Processo di sincronizzazione VALUTA - [!INCLUDE[d365fin](includes/cds_long_md.md)].
2. Processo di sincronizzazione FORNITORE - [!INCLUDE[d365fin](includes/cds_long_md.md)]. 
3. Processo di sincronizzazione CONTATTO - [!INCLUDE[d365fin](includes/cds_long_md.md)].
4. Processo di sincronizzazione CLIENTE - [!INCLUDE[d365fin](includes/cds_long_md.md)].
5. Processo di sincronizzazione AGENTI - [!INCLUDE[d365fin](includes/cds_long_md.md)].

È possibile visualizzare i processi nella pagina **Movimenti coda processi**. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

### <a name="default-synchronization-job-queue-entries"></a>Movimenti coda processi di sincronizzazione predefiniti  
Nella tabella seguente sono descritti i processi di sincronizzazione predefiniti per [!INCLUDE[d365fin](includes/cds_long_md.md)].  

|Movimento coda processi|Descrizione|Direzione|Mapping tabella integrazione|Frequenza di sincronizzazione predefinita (minuti)|Tempo di inattività predefinito (minuti)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Processo di sincronizzazione CONTATTO - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincronizza i contatti di [!INCLUDE[d365fin](includes/cds_long_md.md)] con i contatti di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirezionale|CONTATTO|30|720 <br>(12 ore)| 
|Processo di sincronizzazione VALUTA - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincronizza le valute di transazione di [!INCLUDE[d365fin](includes/cds_long_md.md)] con le valute di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)]|VALUTA|30|720 <br> (12 ore)| 
|Processo di sincronizzazione CLIENTE - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincronizza i conti di [!INCLUDE[d365fin](includes/cds_long_md.md)] e i clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirezionale|CLIENTE|30|720<br> (12 ore)|
|Processo di sincronizzazione FORNITORE - [!INCLUDE[d365fin](includes/cds_long_md.md)].|Sincronizza i conti di [!INCLUDE[d365fin](includes/cds_long_md.md)] e i clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirezionale|FORNITORE|30|720<br> (12 ore)|
|Processo di sincronizzazione AGENTI - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincronizza gli agenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] con gli utenti di [!INCLUDE[d365fin](includes/cds_long_md.md)].|Da [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]|AGENTI|30|1440<br> (24 ore)|

## <a name="synchronization-process"></a>Processo di sincronizzazione  
Ogni movimento coda processi di sincronizzazione utilizza un mapping di tabella di integrazione che specifica quale tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] e quale entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] sincronizzare. I mapping di tabella includono anche alcune impostazioni che controllano quali record della tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] e dell'entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] sincronizzare.  

Per sincronizzare i dati, i record di entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] devono essere associati a record di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, un cliente di [!INCLUDE[d365fin](includes/d365fin_md.md)] deve essere associato a un conto di [!INCLUDE[d365fin](includes/cds_long_md.md)]. È possibile impostare le associazioni manualmente, prima di eseguire i processi di sincronizzazione, oppure permettere ai processi di sincronizzazione di impostare le associazioni automaticamente. Nel seguente elenco viene descritto come i dati vengono sincronizzati tra Common Data Service e [!INCLUDE[d365fin](includes/d365fin_md.md)] quando si utilizzano i movimenti coda processi di sincronizzazione. Per ulteriori informazioni, vedere [Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md).

-   La casella di controllo **Sinc. solo record associati** controlla se vengono creati nuovi record durante la sincronizzazione. Per impostazione predefinita, la casella di controllo è selezionata, il che significa che verranno sincronizzati solo i record associati. Nel mapping di tabella di integrazione, è possibile modificare il mapping di tabella tra un'entità di [!INCLUDE[d365fin](includes/cds_long_md.md)] e una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)], in modo che i processi di sincronizzazione di integrazione creeranno nuovi record nel database di destinazione per ogni record del database di origine che non è associato. Per altre informazioni, vedere [Creazione di nuovi record](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Esempio** Se si deseleziona la casella di controllo **Snc. solo record associati**, quando si sincronizzano i clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)] con account in [!INCLUDE[d365fin](includes/cds_long_md.md)], un nuovo account viene creato e automaticamente associato per ciascun cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Inoltre, poiché in questo caso la sincronizzazione è bidirezionale, un nuovo cliente viene creato e associato per ogni account di [!INCLUDE[d365fin](includes/cds_long_md.md)] che non è già associato.  

    > [!NOTE]  
    > Esistono regole e filtri che determinano quali dati vengono sincronizzati. Per ulteriori informazioni, vedere [Regole di sincronizzazione](admin-synchronizing-business-central-and-sales.md).

-   Quando vengono creati nuovi record in [!INCLUDE[d365fin](includes/d365fin_md.md)], i record utilizzano il modello che viene definito per il mapping di tabella di integrazione o il modello predefinito disponibile per il tipo di record. I campi vengono popolati con i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] o di [!INCLUDE[d365fin](includes/cds_long_md.md)] in base alla direzione della sincronizzazione. Per ulteriori informazioni, vedere [Modificare i mapping di tabella per la sincronizzazione](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Con le sincronizzazioni successive, verranno aggiornati solo i record che sono stati modificati o aggiunti dopo l'ultimo processo di sincronizzazione completato per le entità.  

     I nuovi record in [!INCLUDE[d365fin](includes/cds_long_md.md)] vengono aggiunti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se i dati nei campi dei record di [!INCLUDE[d365fin](includes/cds_long_md.md)] vengono modificati, i dati vengono copiati nel campo corrispondente di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Con la sincronizzazione bidirezionale, il processo sincronizza da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)] e quindi da [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="about-inactivity-timeouts"></a>Informazioni sui timeout di inattività
Alcuni movimenti coda processi, come quelli che pianificano la sincronizzazione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)], utilizzano il campo **Timeout inattività** nella scheda Movimento coda processi per impedire l'esecuzione inutile del movimento coda processi.  
<br><br>

> ![Diagramma di flusso per quando i movimenti coda processi vengono sospesi a causa di inattività.](media/on-hold-with-inactivity-timeout.png)

Quando il valore in questo campo non è zero e la coda processi non ha trovato alcuna modifica durante l'ultima esecuzione, [!INCLUDE[d365fin](includes/d365fin_md.md)] sospende il movimento coda processi. Quando ciò accade, il campo **Stato della coda processi** visualizzerà **In sospeso a causa di inattività** e [!INCLUDE[d365fin](includes/d365fin_md.md)] attenderà il periodo di tempo specificato nel campo **Timeout inattività** prima di eseguire nuovamente il movimento coda processi. 

Ad esempio, per impostazione predefinita, il movimento coda processi CURRENCY, che sincronizza le valute in [!INCLUDE[d365fin](includes/cds_long_md.md)] con tassi di cambio in [!INCLUDE[d365fin](includes/d365fin_md.md)], cercherà le modifiche ai tassi di cambio ogni 30 minuti. Se non vengono rilevate modifiche, [!INCLUDE[d365fin](includes/d365fin_md.md)] sospende il movimento coda processi CURRENCY per 720 minuti (sei ore). Se un tasso di cambio viene modificato in [!INCLUDE[d365fin](includes/d365fin_md.md)] quando il movimento coda processi viene sospeso, [!INCLUDE[d365fin](includes/d365fin_md.md)] riattiverà automaticamente tale movimento e riavvierà la coda processi. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] attiverà automaticamente i movimenti coda processi sospesi solo quando si verificano delle modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le modifiche in [!INCLUDE[d365fin](includes/cds_long_md.md)] non attiveranno i movimenti coda processi.

## <a name="to-view-the-synchronization-job-log"></a>Per visualizzare il log processi di sincronizzazione  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Log processi di sincronizzazione** e quindi scegliere il collegamento correlato.
2.  Se si sono verificati uno o più errori per un processo di sincronizzazione, il numero di errori viene visualizzato nella colonna **Operazione non riuscita**. Per visualizzare gli errori per il processo, selezionare il numero.  

    > [!TIP]  
    > È possibile visualizzare tutti gli errori dei processi di sincronizzazione aprendo direttamente il log errori processi di sincronizzazione.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Per visualizzare il log processi di sincronizzazione dai mapping di tabella  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.
2.  Nella pagina **Mapping tabella integrazione**, selezionare un movimento quindi scegliere **Log processi di sincronizzazione integrazione**.  

## <a name="to-view-the-synchronization-error-log"></a>Per visualizzare il log processi di sincronizzazione  
* Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Errori di sincronizzazione integrazione** e quindi scegliere il collegamento correlato.

## <a name="see-also"></a>Vedere anche  
[Sincronizzazione di dati in Business Central e [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Sincronizzare manualmente i mapping di tabella](admin-manual-synchronization-of-table-mappings.md)  
[Pianificazione di una sincronizzazione tra Business Central e [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Informazioni sull'integrazione di Dynamics 365 Business Central con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
