---
title: Come esportare e importare workflow di approvazione
description: 'Per trasferire i workflow ad altri database di Business Central, ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="export-and-import-approval-workflows" />Importa ed esporta workflow di approvazione

Per trasferire i workflow ad altri database di [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.  

Un altro modo per creare rapidamente i flussi di lavoro è da modelli di workflow. Ulteriori informazioni in [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  

Nella pagina **Workflow** crea un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="export-a-workflow" />Esportare un flusso di lavoro

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Selezionare un workflow e scegliere l'azione **Esporta in file**.  

## <a name="import-a-workflow" />Importare un flusso di lavoro

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Selezionare l'azione **Importa da file**.  
3. Nella pagina **Importa**, seleziona **Scegli**, seleziona il file XML contenente il flusso di lavoro, quindi scegli il pulsante **Apri**.  

> [!CAUTION]  
> Se il codice del flusso di lavoro è già esistente nel database, i passaggi del flusso di lavoro verranno sovrascritti dai passaggi il flusso di lavoro importato.  

## <a name="see-also" />Vedere anche

[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md)  
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminare i workflow di approvazione](across-how-to-delete-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
