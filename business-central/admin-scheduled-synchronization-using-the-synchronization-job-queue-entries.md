---
title: Sincronizzazione di Business Central e Dynamics 365 for Sales | Microsoft Docs
description: Ottenere informazioni sulla sincronizzazione di dati tra Business Central e Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: b3fb3d2680cd85da8b2def7e82fbf62c0046fcc3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "940243"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Pianificazione di una sincronizzazione tra Business Central e Dynamics 365 for Sales
È possibile sincronizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] a intervalli pianificati impostando i processi nella coda processi. I processi di sincronizzazione sincronizzano i dati nei record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e nei record di [!INCLUDE[crm_md](includes/crm_md.md)] che sono stati associati in precedenza. Oppure per i record che non sono ancora associati, a seconda della direzione e delle regole di sincronizzazione, i processi di sincronizzazione possono creare e associare nuovi record nel sistema di destinazione. Esistono vari processi di sincronizzazione predefiniti disponibili. È possibile visualizzarli nella pagina **Movimenti coda processi**. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Processo di sincronizzazione  
Ogni movimento coda processi di sincronizzazione utilizza un mapping di tabella di integrazione che specifica quale tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] e quale entità di [!INCLUDE[crm_md](includes/crm_md.md)] sincronizzare. I mapping di tabella includono anche alcune impostazioni che controllano quali record della tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] e dell'entità di [!INCLUDE[crm_md](includes/crm_md.md)] sincronizzare.  

Per sincronizzare i dati, i record di entità di [!INCLUDE[crm_md](includes/crm_md.md)] devono essere associati a record di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, un cliente di [!INCLUDE[d365fin](includes/d365fin_md.md)] deve essere associato a un conto di [!INCLUDE[crm_md](includes/crm_md.md)]. È possibile impostare le associazioni manualmente, prima di eseguire i processi di sincronizzazione, oppure permettere ai processi di sincronizzazione di impostare le associazioni automaticamente. Nel seguente elenco viene descritto come i dati vengono sincronizzati tra [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)] quando si utilizzano i movimenti coda processi di sincronizzazione. Per ulteriori informazioni, vedere [Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Per impostazione predefinita, solo i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] che sono associati ai record di [!INCLUDE[crm_md](includes/crm_md.md)] vengono sincronizzati. È possibile modificare il mapping di tabella tra un'entità di [!INCLUDE[crm_md](includes/crm_md.md)] e una tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)], in modo che i processi di sincronizzazione di integrazione creeranno nuovi record nel database di destinazione per ogni record del database di origine che non è associato. Anche i nuovi record vengono associati ai record corrispondenti nell'origine. Ad esempio, quando si sincronizzano clienti con conti di [!INCLUDE[crm_md](includes/crm_md.md)], un nuovo record di conto viene creato per ogni cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. I nuovi conti vengono automaticamente associati ai clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Poiché la sincronizzazione in questo caso è bidirezionale, un nuovo cliente viene creato e associato per ogni conto di [!INCLUDE[crm_md](includes/crm_md.md)] che non è già associato.  

    > [!NOTE]  
    >  Esistono regole e filtri che determinano quali dati vengono sincronizzati. Per ulteriori informazioni, vedere [Regole di sincronizzazione](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Quando vengono creati nuovi record in [!INCLUDE[d365fin](includes/d365fin_md.md)], i record utilizzano il modello che viene definito per il mapping di tabella di integrazione o il modello predefinito disponibile per il tipo di record. I campi vengono popolati con i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] o di [!INCLUDE[crm_md](includes/crm_md.md)] in base alla direzione della sincronizzazione. Per ulteriori informazioni, vedere [Procedura: Modificare i mapping di tabella per la sincronizzazione](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Con le sincronizzazioni successive, verranno aggiornati solo i record che sono stati modificati o aggiunti dopo l'ultimo processo di sincronizzazione completato per le entità.  

     I nuovi record in [!INCLUDE[crm_md](includes/crm_md.md)] vengono aggiunti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se i dati nei campi dei record di [!INCLUDE[crm_md](includes/crm_md.md)] vengono modificati, i dati vengono copiati nel campo corrispondente di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Con la sincronizzazione bidirezionale, il processo sincronizza da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] e quindi da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Movimenti coda processi di sincronizzazione predefiniti  
Nella tabella seguente sono descritti i processi di sincronizzazione predefiniti.  

|Movimento coda processi|Descrizione|Direzione|Mapping tabella integrazione|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|Processo di sincronizzazione CONTATTO - Dynamics 365 for Sales|Sincronizza i contatti di [!INCLUDE[crm_md](includes/crm_md.md)] con i contatti di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirezionale|CONTATTO|  
|Processo di sincronizzazione VALUTA - Dynamics 365 for Sales|Sincronizza le valute di transazione di [!INCLUDE[crm_md](includes/crm_md.md)] con le valute di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|  
|Processo di sincronizzazione CLIENTE - Dynamics 365 for Sales|Sincronizza i conti di [!INCLUDE[crm_md](includes/crm_md.md)] e i clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirezionale|CLIENTE|  
|Processo di sincronizzazione GRPPRZCLNT-PREZZO - Dynamics 365 for Sales|Sincronizza i listini prezzi di vendita di [!INCLUDE[crm_md](includes/crm_md.md)] con gruppi di prezzi cliente di [!INCLUDE[d365fin](includes/d365fin_md.md)].| |GRUPPI DI PREZZI CLIENTE-LISTINI PREZZI DI VENDITA|
|Processo di sincronizzazione ARTICOLO - PRODOTTO - Dynamics 365 for Sales|Sincronizza i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con articoli di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|ARTICOLO-PRODOTTO|
|Processo di sincronizzazione FATTVNDTRGSTR-FATT - Dynamics 365 for Sales|Sincronizza le fatture di [!INCLUDE[crm_md](includes/crm_md.md)] con le fatture di vendita registrate di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]|FATTURE-FATTURE DI VENDITA REGISTRATE|
|Processo di sincronizzazione RISORSA-PRODOTTO - Dynamics 365 for Sales|Sincronizza i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con le risorse di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|RISORSA-PRODOTTO|  
|Processo di sincronizzazione AGENTI - Dynamics 365 for Sales|Sincronizza gli agenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] con gli utenti di [!INCLUDE[crm_md](includes/crm_md.md)].|Da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]|AGENTI|
|Processo di sincronizzazione PRZVNDT-PRZPRODOTTI - Dynamics 365 for Sales|Sincronizza i prezzi dei prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con i prezzi di vendita di [!INCLUDE[d365fin](includes/d365fin_md.md)].||PREZZO DEL PRODOTTO - PREZZO DI VENDITA|
|Processo di sincronizzazione UNITÀDIMISURA - Dynamics 365 for Sales|Sincronizza le unità di vendita di [!INCLUDE[crm_md](includes/crm_md.md)] con le unità di misura di [!INCLUDE[d365fin](includes/d365fin_md.md)].|Da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|UNITÀ DI MISURA|  
|Processo di sincronizzazione Statistiche cliente - Dynamics 365 for Sales|Aggiorna i conti di [!INCLUDE[crm_md](includes/crm_md.md)] con i dati cliente di [!INCLUDE[d365fin](includes/d365fin_md.md)] più recenti. In [!INCLUDE[crm_md](includes/crm_md.md)], questa informazione viene visualizzata nel modulo di visualizzazione rapida **Statistiche conto Business Central** dei conti associati ai clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Questi dati possono anche essere aggiornati manualmente da ogni record cliente. Per ulteriori informazioni, vedere [Procedura: Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Nota:** questo movimento coda processi è pertinente solo se la soluzione di integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] è installata in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Informazioni sulla soluzione di integrazione di Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Non applicabile.|Non applicabile.|   

## <a name="to-view-the-synchronization-job-log"></a>Per visualizzare il log processi di sincronizzazione  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Log processi di sincronizzazione** e quindi scegliere il collegamento correlato.
2.  Se si sono verificati uno o più errori per un processo di sincronizzazione, il numero di errori viene visualizzato nella colonna **Operazione non riuscita**. Per visualizzare gli errori per il processo, selezionare il numero.  

    > [!TIP]  
    >  È possibile visualizzare tutti gli errori dei processi di sincronizzazione aprendo direttamente il log errori processi di sincronizzazione.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Per visualizzare il log processi di sincronizzazione dai mapping di tabella  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.
2.  Nella pagina **Mapping tabella integrazione**, selezionare un movimento quindi scegliere **Log processi di sincronizzazione integrazione**.  

## <a name="to-view-the-synchronization-error-log"></a>Per visualizzare il log processi di sincronizzazione  
* Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Errori di sincronizzazione integrazione** e quindi scegliere il collegamento correlato.

## <a name="see-also"></a>Vedere anche  
[Sincronizzazione di dati in Business Central e Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Sincronizzare manualmente i mapping di tabella](admin-manual-synchronization-of-table-mappings.md)  
[Pianificazione di una sincronizzazione tra Business Central e Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Informazioni sull'integrazione di Dynamics 365 Business Central con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



