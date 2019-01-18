---
title: Come impostare gli utenti del workflow | Microsoft Docs
description: "Prima di poter creare i flussi di lavoro, è necessario impostare gli utenti che parteciperanno ai flussi di lavoro. Questa operazione è essenziale per specificare, ad esempio, chi riceverà una notifica per agire in una fase del flusso di lavoro."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 8f205520d1028b3de176a720b363ff9c019634df
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-workflow-users"></a>Impostare gli utenti del workflow
Prima di poter creare i workflow, è necessario impostare gli utenti che vi parteciperanno. Questa operazione è essenziale per specificare, ad esempio, chi riceverà una notifica per agire in una fase del flusso di lavoro.  

Nella pagina **Gruppo di utenti del workflow** è possibile impostare gli utenti in gruppi di utenti del workflow e specificare il numero di utenti in una sequenza di processo, ad esempio una catena di responsabili di approvazione.  

Anche gli utenti del workflow che agiscono da utenti dell'approvazione, sia i richiedenti sia i responsabili dell'approvazione, devono essere impostati come utenti del workflow nella pagina **Gruppo di utenti del workflow**. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
>  Per definire che una richiesta di approvazione non venga approvata fino a che non venga approvata da più responsabili di una catena di approvazione, impostare i responsabili di approvazione in una gerarchia. Per il tipo **Responsabile approvazione**, impostare i responsabili approvazione nella pagina **Setup utente approvazione**. Per il tipo **Gruppo di utenti del workflow**, impostare i responsabili di approvazione nella pagina **Gruppi di utenti del workflow** e definire la gerarchia assegnando numeri incrementali a ogni responsabile nel campo **Nr. sequenza**   Per ulteriori informazioni, vedere questo argomento e [Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md).  
>   
>  Per definire che una richiesta di approvazione non venga approvata fino a che non venga approvata da più responsabili uguali, indipendentemente da una gerarchia, impostare un normale gruppo di utenti del flusso di lavoro. Per il tipo **Gruppo di utenti del workflow**, impostare i responsabili di approvazione nella pagina **Gruppi di utenti del workflow** e assegnare lo stesso numero a ogni responsabile nel campo **Nr. sequenza** . Per ulteriori informazioni, vedere questo argomento.  

### <a name="to-set-up-a-workflow-user"></a>Per impostare un utente del flusso di lavoro  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi di utenti del workflow** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Viene visualizzata la pagina **Gruppo di utenti del workflow**.  
3. Nel campo **Codice** immettere un massimo di 20 caratteri che identifichino il workflow.  
4. Nel campo  **Descrizione** descrivere il workflow.  
5. Nella Scheda dettaglio **Membri gruppo utenti del flusso di lavoro** compilare i campi come descritto nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nome utente**|Specificare l'utente che parteciperà ai flussi di lavoro.<br /><br /> L'utente deve essere presente nella pagina **Setup utente**. Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).|  
    |**Nr. sequenza**|Specificare l'ordine in cui l'utente del flusso di lavoro viene impiegato in un flusso di lavoro rispetto ad altri utenti. Questo campo può essere utilizzato, ad esempio, per specificare quando l'utente approva in relazione ad altri responsabili approvazione quando si utilizza l'opzione **Gruppo di utenti del workflow** nel campo **Tipo di responsabile approvazione** nella relativa risposta workflow. **SUGGERIMENTO:** per definire che una richiesta di approvazione non venga approvata fino a che non venga approvata da più responsabili uguali, indipendentemente da una gerarchia, impostare un normale gruppo di utenti del workflow assegnando lo stesso numero di sequenza ai relativi responsabili dell'approvazione.|  
6. Ripetere il passaggio 5 per aggiungere altri utenti del flusso di lavoro nel gruppo di utenti.  
7. Ripetere i passaggi da 2 a 6 per aggiungere altri gruppi di utenti del flusso di lavoro.  

## <a name="see-also"></a>Vedi anche  
[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
[Impostazione dei workflow](across-set-up-workflows.md)   
[Utilizzo dei workflow](across-use-workflows.md)   
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Workflow](across-workflow.md)   

