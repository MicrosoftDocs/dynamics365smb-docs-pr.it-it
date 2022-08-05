---
title: Come esportare e importare workflow | Microsoft Docs
description: Per trasferire i workflow ad altri database di Business Central, ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a52d4b4bff0f96023b6206e6cb8cad3d9e59276
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129931"
---
# <a name="export-and-import-workflows"></a>Importa ed esporta workflow

Per trasferire i workflow ad altri database di [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.  

Un altro modo per creare rapidamente i flussi di lavoro prevede la creazione di workflow da modelli di workflow. Per ulteriori informazioni, vedere [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).  

Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Per esportare un flusso di lavoro

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Selezionare un workflow e scegliere l'azione **Esporta in file**.  

## <a name="to-import-a-workflow"></a>Per importare un flusso di lavoro

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Selezionare l'azione **Importa da file**.  
3. Nella pagina **Importa** seleziona il pulsante **Scegli**, scegli il file XML contenente il flusso di lavoro e quindi seleziona il pulsante **Apri**.  

> [!CAUTION]  
> Se il codice del flusso di lavoro è già esistente nel database, i passaggi del flusso di lavoro verranno sovrascritti dai passaggi il flusso di lavoro importato.  

## <a name="see-also"></a>Vedere anche

[Creare i workflow](across-how-to-create-workflows.md)  
[Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md)  
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminare i workflow](across-how-to-delete-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Impostazione dei workflow](across-set-up-workflows.md)  
[Utilizzare i workflow](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]