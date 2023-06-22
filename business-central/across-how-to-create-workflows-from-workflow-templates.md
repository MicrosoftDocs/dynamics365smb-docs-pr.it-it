---
title: Come creare flussi di lavoro da modelli di flusso di lavoro
description: 'Per risparmiare tempo durante la creazione di nuovi workflow di approvazione, è possibile creare flussi di lavoro non modificabili da modelli di flusso di lavoro con prefisso "MS".'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="create-workflows-from-workflow-templates" />Creare workflow da modelli di workflow

Per risparmiare tempo durante la creazione di nuovi workflow di approvazione, puoi creare i modelli di workflow.  

I modelli di workflow sono flussi di lavoro non modificabili presenti nella versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)]. Il codice dei modelli di flusso di lavoro che vengono creati da Microsoft hanno il prefisso "MS-".  

Un altro modo per creare rapidamente un workflow consiste nell'importare un workflow esistente disponibile in un file all'esterno di [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Importare ed esportare workflow](across-how-to-export-and-import-workflows.md).  

Nella pagina **Workflow** crea un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template" />Per creare un flusso di lavoro da un modello di flusso di lavoro

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo workflow da modello**. Verrà aperta la pagina **Modelli del workflow**.  
3. Seleziona un modello di flusso di lavoro e scegli **OK**.  

   Verrà visualizzata la pagina **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato. Il valore nel campo **Codice** ad esempio con "-01" per indicare che questo è il primo workflow che viene creato dal modello di workflow.  
4. Continuare la creazione del flusso di lavoro modificando i passaggi del flusso di lavoro o aggiungendone di nuovi. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Vedi il relativo [training Microsoft](/training/modules/create-workflows/)

## <a name="see-also" />Vedere anche

[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Importa ed esporta workflow di approvazione](across-how-to-export-and-import-workflows.md)  
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminare i workflow di approvazione](across-how-to-delete-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
