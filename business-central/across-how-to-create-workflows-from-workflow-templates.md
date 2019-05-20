---
title: Come creare workflow da modelli di workflow | Microsoft Docs
description: Per risparmiare tempo durante la creazione di nuovi workflow, è possibile creare i workflow da modelli di workflow.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 82d288ab59f80c6e5d2e46f8168f10552b5b900d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241222"
---
# <a name="create-workflows-from-workflow-templates"></a>Creare flussi di lavoro da modelli di flusso di lavoro
Per risparmiare tempo durante la creazione di nuovi workflow, è possibile creare i workflow da modelli di workflow.  

 I modelli di workflow sono flussi di lavoro non modificabili presenti nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-".  

 Un altro modo per creare rapidamente un workflow consiste nell'importare un workflow esistente disponibile in un file all'esterno di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Esportare e importare workflow](across-how-to-export-and-import-workflows.md).  

Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Per creare un flusso di lavoro da un modello di flusso di lavoro  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Crea flusso di lavoro da modello**. Verrà aperta la pagina **Modelli del workflow**.  
3.  Selezionare un modello di flusso di lavoro e scegliere il pulsante **OK**.  

     Verrà visualizzata la pagina **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato. Il valore nel campo **Codice** ad esempio con "-01" per indicare che questo è il primo workflow che viene creato dal modello di workflow.  
4.  Continuare la creazione del flusso di lavoro modificando i passaggi del flusso di lavoro o aggiungendone di nuovi. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Vedi anche  
 [Creare i workflow](across-how-to-create-workflows.md)   
 [Importare ed esportare workflow](across-how-to-export-and-import-workflows.md)   
 [Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)   
 [Eliminare i workflow](across-how-to-delete-workflows.md)   
 [Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Impostazione dei workflow](across-set-up-workflows.md)   
 [Utilizzo dei workflow](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
