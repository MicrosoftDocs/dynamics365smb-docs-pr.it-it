---
title: Flussi di lavoro in Dynamic 365 Business Central
description: Usa le funzionalità di flusso di lavoro integrate per impostare flussi di lavoro di approvazione per integrare i flussi di lavoro automatizzati basati su Power Automate. È possibile impostare passaggi per assegnare attività a persone diverse nell'ambito delle diverse attività dei processi aziendali.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 0bd4c54bc089906877052efdbf471fc3dbe1fc30
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533431"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflow in Dynamics 365 Business Central

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.  

La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] supporta tre tipi di flussi di lavoro:

* Flussi di lavoro di approvazione automatizzati basati su modelli di flusso di lavoro integrati  

  Nella pagina **Modelli di flusso di lavoro**, puoi vedere tutti i flussi di lavoro disponibili. La versione di valutazione di [!INCLUDE[prod_short](includes/prod_short.md)] include molti workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per creare workflow. Quando apri un modello di flusso di lavoro dalla pagina **Modelli di flusso di lavoro** e il nome del flusso di lavoro inizia con *MS-*, il modello di flusso di lavoro viene aggiunto da Microsoft.  
* Flussi automatizzati che hai impostato tu stesso  

  Qualsiasi modello di workflow creato con Power Automate viene aggiunto all'elenco dei modelli di workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Per altre informazioni, vedi [Utilizzare Business Central nei flussi Power Automate](across-how-use-financials-data-source-flow.md).  
* Flussi attivati manualmente dall'azione **Automatizza** (solo [!INCLUDE [prod_short](includes/prod_short.md)] online). Per ulteriori informazioni, vedere [Flussi istantanei manuali](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Flussi di Power Automate

Con [!INCLUDE [prod_short](includes/prod_short.md)] online, puoi iscriverti a Power Automate e quindi creare flussi automatizzati avanzati che puoi eseguire dall'interno di [!INCLUDE [prod_short](includes/prod_short.md)]. For altre informazioni, vedi [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] nei flussi di Power Automate](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Flussi di lavoro di approvazione automatici

Puoi creare un flusso di lavoro di approvazione elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

[!INCLUDE[workflow](includes/workflow.md)]

Per impostare e utilizzare flussi di lavoro non definiti in Power Automate, controlla i seguenti articoli:  

|**Per**|**Vedere**|  
|------------|-------------|  
|Impostare gli utenti del flusso di lavoro, specificare la modalità di notifica per gli utenti e creare nuovi flussi di lavoro. Per i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione.|[Impostare i flussi di lavoro](across-set-up-workflows.md)|  
|Abilitare i flussi di lavoro, intervenire sulle relative notifiche, incluse le approvazioni di richieste, e approvare le richieste per eseguire un passaggio del flusso di lavoro. Archiviare ed eliminare i flussi di lavoro.|[Utilizzare i workflow](across-use-workflows.md)|  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/create-workflows/)

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] nei flussi Power Automate](across-how-use-financials-data-source-flow.md)  
[Risolvere i problemi dei flussi di lavoro automatizzati di [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
