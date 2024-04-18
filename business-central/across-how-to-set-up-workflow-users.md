---
title: Come impostare gli utenti del workflow
description: 'Prima di poter creare i workflow, devi impostare gli utenti che parteciperanno agli stessi nella pagina Setup utente approvazione.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 04/04/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-a-sequence-of-workflow-users"></a>Impostare una sequenza di utenti del workflow

Prima di poter creare i workflow di approvazione, devi impostare gli utenti che possono inviare le richieste e i relativi responsabili dell'approvazione. Ad esempio, puoi specificare chi riceve una notifica per agire in una fase workflow. I partecipanti del workflow di approvazione vengono impostati nella pagina **Setup utente approvazione**. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).

Nella pagina **Gruppi utenti del workflow**, puoi specificare dove un partecipante si impegna in un workflow di approvazione immettendo un numero nel campo **Nr. sequenza** . Ad esempio, puoi specificare che gli utenti si impegnino in un ordine sequenziale, come una catena di responsabili dell'approvazione. Puoi anche specificare un elenco semplice di responsabili dell'approvazione immettendo lo stesso numero. In quest'ultimo caso, solo uno dei responsabili dell'approvazione deve approvare una richiesta.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group"></a>Per impostare un gruppo del workflow

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di utenti del workflow**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**. Viene visualizzata la pagina **Gruppo di utenti del workflow**.  
3. Nel campo **Codice** immettere un massimo di 20 caratteri che identifichino il workflow.  
4. Nel campo  **Descrizione** descrivere il workflow.  
5. Nella Scheda dettaglio **Membri gruppo utenti del workflow** compila i campi nella prima riga come descritto nella tabella seguente.  

   |Campo|Descrizione|
   |-----|-----------|
   |**Nome utente**|Specifica l'utente che partecipa a un workflow.<br /><br /> L'utente deve essere presente nella pagina **Setup utente**. Ulteriori informazioni in [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).|
   |**Nr. sequenza**|Specificare l'ordine in cui l'utente del workflow viene impiegato in un workflow rispetto ad altri utenti. Questo campo può essere utilizzato, ad esempio, per specificare quando l'utente approva in relazione ad altri responsabili approvazione quando si utilizza l'opzione **Gruppo di utenti del workflow** nel campo **Tipo di responsabile approvazione** nella relativa risposta workflow.|

   > [!NOTE]
   > In genere, i numeri di sequenza sono sequenziali per gli utenti in un gruppo di utenti del workflow. Tuttavia, più utenti possono avere lo stesso numero di sequenza. In tal caso, solo uno degli utenti deve approvare una richiesta prima che il workflow passi alla fase successivo. Ad esempio, se l'utente A e l'utente B sono entrambi il numero due nella sequenza, il workflow passa alla fase tre quando l'utente A o l'utente B approva la richiesta.
6. Ripetere il passaggio 5 per aggiungere altri utenti del workflow nel gruppo utenti.  

## <a name="see-also"></a>Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Configurare i workflow di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
