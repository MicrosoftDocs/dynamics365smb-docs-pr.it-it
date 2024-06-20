---
title: Come creare flussi di lavoro da modelli di flusso di lavoro
description: 'Per risparmiare tempo durante la creazione di nuovi workflow di approvazione, puoi creare i workflow da modelli di workflow.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-workflows-from-workflow-templates"></a>Creare workflow da modelli di workflow

Nella pagina **Workflow** crei un workflow creando una serie di fasi workflow nelle righe. Ogni fase consiste di un evento workflow (Evento), moderato dalle condizioni di evento (Condizione) e in una risposta workflow (Risposta), moderata dalle opzioni di risposta. I campi nel righe del workflow forniscono elenchi fissi di valori di eventi e risposte che rappresentano gli scenari che [!INCLUDE [prod_short](includes/prod_short.md)] supporta. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).

Per risparmiare tempo durante la creazione di workflow di approvazione, [!INCLUDE [prod_short](includes/prod_short.md)] fornisce modelli di workflow. I modelli sono disponibili nella pagina **Modelli del workflow**. Puoi utilizzare i modelli così come sono o personalizzarli per soddisfare le tue esigenze. Il codice dei modelli di workflow di Microsoft hanno il prefisso **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Se modifichi un modello di workflow, ma in seguito ti penti della modifica, utilizza l'azione **Reimposta i modelli Microsoft** per ripristinare l'impostazione originale del workflow.

> [!CAUTION]
> L'azione **Reimposta i modelli Microsoft** reimposta tutti i modelli di workflow di Microsoft. Non puoi reimpostare un singolo modello.  

Un altro modo per creare rapidamente un workflow è importarlo, ad esempio, se lo hai esportato da un'altra istanza di [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Importare ed esportare workflow](across-how-to-export-and-import-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Per creare un flusso di lavoro da un modello di flusso di lavoro

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo workflow da modello**. Verrà aperta la pagina **Modelli del workflow**.  
3. Seleziona un modello di flusso di lavoro e scegli **OK**.  

   Verrà visualizzata la pagina **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato. Il valore nel campo **Codice** ad esempio con "-01" per indicare che questo è il primo workflow che viene creato dal modello di workflow.  
4. Per personalizzare il workflow, modifica le fasi workflow o aggiungine di nuove. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Vedere anche

[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Importare ed esportare workflow di approvazione](across-how-to-export-and-import-workflows.md)  
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminare i workflow di approvazione](across-how-to-delete-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurare workflow di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
