---
title: Workflow | Microsoft Docs
description: "È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/16/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d8bf7311a6d180f789d6a7d9532478c25cf3c2c1
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="workflow"></a>Workflow
È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.  

 Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

 La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] include una serie di workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per creare workflow. Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-". Per ulteriori informazioni, vedere l'elenco dei modelli di workflow nella pagina Modelli del workflow.  

 Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, il partner Microsoft deve implementarli tramite la personalizzazione del codice dell'applicazione. Per ulteriori informazioni, vedere [Procedura dettagliata: Implementazione di nuovi eventi e risposte workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) nella Guida per sviluppatori e professionisti IT.

 > [!NOTE]
 > Oltre alla funzionalità Workflow in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile eseguire l'integrazione a Microsoft Flow per definire workflow per gli eventi in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si noti che sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso creato con Microsoft Flow viene aggiunta all'elenco dei modelli di flusso in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Uso di Business Central in un workflow automatizzato](across-how-use-financials-data-source-flow.md).  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare gli utenti del flusso di lavoro, specificare la modalità di notifica per gli utenti e creare nuovi flussi di lavoro. Per i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione.|[Impostazione dei workflow](across-set-up-workflows.md)|  
|Abilitare i flussi di lavoro, intervenire sulle relative notifiche, incluse le approvazioni di richieste, e approvare le richieste per eseguire un passaggio del flusso di lavoro. Archiviare ed eliminare i flussi di lavoro.|[Utilizzo dei workflow](across-use-workflows.md)|  

## <a name="see-also"></a>Vedi anche  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

