---
title: Impostazione dei workflow | Microsoft Docs
description: È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96c39641c9665542c8c27b004bb27f92768d57dc
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910906"
---
# <a name="setting-up-workflows"></a>Impostazione dei workflow
È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow. Per ulteriori informazioni, vedere [Utilizzo dei workflow](across-use-workflows.md).  

 Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del flusso di lavoro e gli utenti dell'approvazione, specificare la modalità di ricezione delle notifiche sui passaggi del flusso di lavoro e successivamente creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice.  

 Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

 Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, il partner Microsoft deve implementarli tramite la personalizzazione del codice dell'applicazione. Per ulteriori informazioni, vedere [Procedura dettagliata: Implementazione di nuovi eventi e risposte workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) nella Guida per sviluppatori e professionisti IT.

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare gli utenti e i gruppi di utenti del flusso di lavoro.|[Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)|  
|Impostare gli utenti del flusso di lavoro che partecipano ai flussi di approvazione.|[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)|  
|Specificare in che modo gli utenti ricevono le notifiche dei passaggi del flusso di lavoro, incluse le richieste di approvazione.|[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)|  
|Specificare se gli utenti sono avvertiti mediante e-mail o nota e la frequenza alla quale le notifiche vengono inviate.|[Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Personalizzare il contenuto delle notifiche e-mail modificando Report 1320, E-mail di notifica.|[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)|  
|Impostare un server SMTP per consentire la comunicazione e-mail in entrata e in uscita di [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Impostare la posta elettronica](admin-how-setup-email.md)|
|Specificare i diversi passaggi di un flusso di lavoro in base al collegamento tra gli eventi del flusso di lavoro e le risposte del flusso di lavoro.|[Creare i workflow](across-how-to-create-workflows.md)|  
|Usare i modelli di flussi di lavoro per creare nuovi flussi di lavoro.|[Creare flussi di lavoro da modelli di flusso di lavoro](across-how-to-create-workflows-from-workflow-templates.md)|  
|Condividere workflow con altri database [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Importare ed esportare workflow](across-how-to-export-and-import-workflows.md)|  
|Come impostare un flusso di lavoro per approvare documenti di vendita seguendo una procedura end-to-end.|[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Aggiungere supporto per uno scenario aziendale che richiede nuovi eventi o risposte del flusso di lavoro personalizzando il codice dell'applicazione.|[Procedura dettagliata: Implementazione di nuovi eventi e risposte workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="example-of-an-approval-workflow"></a>Esempio di flusso di lavoro di approvazione
Questo video mostra come impostare un flusso di lavoro che chiede a qualcuno di richiedere l'approvazione di qualcun altro prima di poter modificare le informazioni su un cliente esistente o creare un nuovo cliente.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI]

## <a name="see-also"></a>Vedere anche  
 [Utilizzo dei workflow](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Utilizzo di Business Central](ui-work-product.md)
