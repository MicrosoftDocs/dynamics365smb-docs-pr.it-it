---
title: Workflow | Microsoft Docs
description: È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 38092f364d1dee1f34d8aa0c0858ac1bc04d829b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378800"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflow in Dynamics 365 Business Central

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.  

 Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

 La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] include una serie di workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per creare workflow. Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-". Per ulteriori informazioni, vedere l'elenco dei modelli di workflow nella pagina Modelli del workflow.  

 Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, è possibile utilizzare Power Automate o lavorare con un partner Microsoft per personalizzare il codice dell'applicazione. Per ulteriori informazioni, vedere [Uso di [!INCLUDE[prod_short](includes/prod_short.md)] in un workflow automatizzato](across-how-use-financials-data-source-flow.md).

Qualsiasi modello di workflow creato con Power Automate viene aggiunto all'elenco dei modelli di workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Uso di Business Central in un workflow automatizzato](across-how-use-financials-data-source-flow.md).  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare gli utenti del flusso di lavoro, specificare la modalità di notifica per gli utenti e creare nuovi flussi di lavoro. Per i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione.|[Impostazione dei workflow](across-set-up-workflows.md)|  
|Abilitare i flussi di lavoro, intervenire sulle relative notifiche, incluse le approvazioni di richieste, e approvare le richieste per eseguire un passaggio del flusso di lavoro. Archiviare ed eliminare i flussi di lavoro.|[Utilizzo dei workflow](across-use-workflows.md)|  

## <a name="see-also"></a>Vedi anche

[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]