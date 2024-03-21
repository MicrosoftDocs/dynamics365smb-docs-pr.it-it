---
title: Come impostare gli utenti del workflow
description: 'Prima di poter creare i workflow, devi impostare gli utenti che parteciperanno agli stessi nella pagina Setup utente approvazione.'
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-a-sequence-of-workflow-users"></a>Impostare una sequenza di utenti del workflow

Prima di poter creare i workflow di approvazione, devi impostare gli utenti che invieranno le richieste e i relativi responsabili dell'approvazione. Ad esempio, puoi specificare chi riceverà una notifica per agire in una fase workflow. I partecipanti del workflow di approvazione vengono impostati nella pagina **Setup utente approvazione**. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).

Nella pagina **Gruppi utenti del workflow**, puoi specificare dove un partecipante si impegna in un workflow di approvazione immettendo un numero nel campo **Nr. sequenza** . Ad esempio, puoi specificare che gli utenti si impegnino in un ordine sequenziale, come una catena di responsabili dell'approvazione. Puoi anche specificare un elenco semplice di responsabili dell'approvazione immettendo lo stesso numero. In quest'ultimo caso, solo uno dei responsabili dell'approvazione deve approvare una richiesta.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group"></a>Per impostare un gruppo del workflow

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di utenti del workflow**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**. Viene visualizzata la pagina **Gruppo di utenti del workflow**.  
3. Nel campo **Codice** immettere un massimo di 20 caratteri che identifichino il workflow.  
4. Nel campo  **Descrizione** descrivere il workflow.  
5. Nella Scheda dettaglio **Membri gruppo utenti del workflow** compilare i campi come descritto nella tabella seguente.  

   |Campo|Descrizione|
   |-----|-----------|
   |**Nome utente**|Specifica l'utente che parteciperà a un workflow.<br /><br /> L'utente deve essere presente nella pagina **Setup utente**. Ulteriori informazioni in [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).|
   |**Nr. sequenza**|Specificare l'ordine in cui l'utente del workflow viene impiegato in un workflow rispetto ad altri utenti. Questo campo può essere utilizzato, ad esempio, per specificare quando l'utente approva in relazione ad altri responsabili approvazione quando si utilizza l'opzione **Gruppo di utenti del workflow** nel campo **Tipo di responsabile approvazione** nella relativa risposta workflow.| 

6. Ripetere il passaggio 5 per aggiungere altri utenti del workflow nel gruppo utenti.  

## <a name="see-also"></a>Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Configurare i workflow di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
