---
title: Flussi di lavoro in Dynamic 365 Business Central
description: Usa i flussi di lavoro per collegare task di processi aziendali eseguiti da utenti diversi. Le attività di sistema, come la pubblicazione automatica, possono essere incluse come passaggi del flusso di lavoro.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9cfdcc9bbf8e24675c6894b8ca2efbf10129d990
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511183"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflow in Dynamics 365 Business Central

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.  

 Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

 La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] include una serie di workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per creare workflow. Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-". Per ulteriori informazioni, vedere l'elenco dei modelli di workflow nella pagina Modelli del workflow.  

 Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, è possibile utilizzare Power Automate o lavorare con un partner Microsoft per personalizzare il codice dell'applicazione. Per ulteriori informazioni, vedi [Usare [!INCLUDE[prod_short](includes/prod_short.md)] in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md).

Qualsiasi modello di workflow creato con Power Automate viene aggiunto all'elenco dei modelli di workflow in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Usare Business Central in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md).  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare gli utenti del flusso di lavoro, specificare la modalità di notifica per gli utenti e creare nuovi flussi di lavoro. Per i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione.|[Impostazione dei workflow](across-set-up-workflows.md)|  
|Abilitare i flussi di lavoro, intervenire sulle relative notifiche, incluse le approvazioni di richieste, e approvare le richieste per eseguire un passaggio del flusso di lavoro. Archiviare ed eliminare i flussi di lavoro.|[Utilizzare i workflow](across-use-workflows.md)|  

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]