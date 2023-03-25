---
title: Come impostare gli utenti del flusso di lavoro
description: 'Prima di poter creare i flussi di lavoro, è necessario impostare gli utenti che parteciperanno nella pagina Gruppo di utenti del flusso di lavoro.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
---
# Impostare gli utenti del workflow

Prima di poter creare i workflow di approvazione, è necessario impostare gli utenti che parteciperanno ai workflow. Questa operazione è essenziale per specificare, ad esempio, chi riceverà una notifica per agire in una fase del flusso di lavoro.  

Nella pagina **Gruppi di utenti del workflow** è possibile impostare gli utenti in gruppi di utenti del workflow e specificare il numero di utenti in una sequenza di processo, ad esempio una catena di responsabili di approvazione. 

Anche gli utenti del workflow che agiscono da utenti dell'approvazione, sia i richiedenti sia i responsabili dell'approvazione, devono essere impostati come utenti del workflow nella pagina **Gruppo di utenti del workflow**. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Per definire che una richiesta di approvazione non venga approvata finché più utenti non la approvano, impostare i responsabili di approvazione in una gerarchia. Per il tipo **Responsabile approvazione**, impostare i responsabili approvazione nella pagina **Setup utente approvazione**. Per il tipo **Gruppo di utenti del workflow**, impostare i responsabili di approvazione nella pagina **Gruppi di utenti del workflow** e definire la gerarchia assegnando numeri incrementali a ogni responsabile nel campo **Nr. sequenza** . Ulteriori informazioni di seguito e in [Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md). 

## Per impostare un utente del flusso di lavoro

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di utenti del flusso di lavoro**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**. Viene visualizzata la pagina **Gruppo di utenti del workflow**.  
3. Nel campo **Codice** immettere un massimo di 20 caratteri che identifichino il workflow.  
4. Nel campo  **Descrizione** descrivere il workflow.  
5. Nella Scheda dettaglio **Membri gruppo utenti del flusso di lavoro** compilare i campi come descritto nella tabella seguente.  

   |Campo|Descrizione|
   |-----|-----------|
   |**Nome utente**|Specificare l'utente che parteciperà ai flussi di lavoro.<br /><br /> L'utente deve essere presente nella pagina **Setup utente**. Ulteriori informazioni in [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).|
   |**Nr. sequenza**|Specificare l'ordine in cui l'utente del flusso di lavoro viene impiegato in un flusso di lavoro rispetto ad altri utenti. Questo campo può essere utilizzato, ad esempio, per specificare quando l'utente approva in relazione ad altri responsabili approvazione quando si utilizza l'opzione **Gruppo di utenti del workflow** nel campo **Tipo di responsabile approvazione** nella relativa risposta workflow.| 

   > [!TIP]
   > Per definire che una richiesta di approvazione richieda che più utenti uguali l'abbiano approvata, indipendentemente da una gerarchia, imposta un normale gruppo di utenti del workflow assegnando lo stesso numero di sequenza ai tutti i relativi responsabili dell'approvazione.

6. Ripetere il passaggio 5 per aggiungere altri utenti del workflow nel gruppo di utenti.  
7. Ripetere i passaggi da 2 a 6 per aggiungere altri gruppi di utenti del flusso di lavoro.  

## Vedi il relativo [training Microsoft](/training/modules/create-workflows/)

## Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
