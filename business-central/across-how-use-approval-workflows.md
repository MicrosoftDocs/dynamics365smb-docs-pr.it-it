---
title: Approvare o rifiutare i documenti nei workflow| Documenti Microsoft
description: Richiedere, rifiutare o delegare l'approvazione di, ad esempio, a un documento di vendita o acquisto, come parte di un workflow.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 09/28/2021
ms.author: edupont
ms.openlocfilehash: 46c81fa887af70e7a2f516df38ec003392b1dabd
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079352"
---
# <a name="use-approval-workflows"></a>Utilizzare i workflow di approvazione

Quando un record, ad esempio un documento di acquisto o una scheda cliente, deve essere approvato da una persona della propria organizzazione, inviare una richiesta di approvazione come parte di un flusso di lavoro. In base all'impostazione del flusso di lavoro, al responsabile dell'approvazione appropriato viene inviata una notifica relativa alla richiesta di approvazione del record.

I workflow di approvazione vengono impostati nella pagina **Workflow**. Devi anche impostare gli utenti di approvazione, compresi eventuali limiti di importo, nella pagina di **impostazione dell'utente di approvazione** . Per ulteriori informazioni, vedere [Impostazione dei workflow](across-set-up-workflows.md).  

Oltre ai workflow di approvazione descritti in questo argomento, è possibile eseguire varie altre attività del workflow. Per ulteriori informazioni, vedi [Utilizzare i flussi di lavoro](across-use-workflows.md).

I workflow di approvazione principali dei documenti di acquisto e vendita, le registrazioni dei pagamenti, le schede cliente e le schede articolo sono un punto di inizio per la guida al setup assistito. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).

## <a name="to-request-approval-of-a-record"></a>Per richiedere l'approvazione di un record

La seguente attività viene eseguita da un utente approvazione.

1. Nella pagina che presenta il record, scegli l'azione **Invia richiesta di approvazione** .
2. Per vedere tutte le tue richieste di approvazione, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimenti richieste approvazione**, quindi scegli il collegamento correlato.  

Lo stato del movimento di approvazione viene aggiornato da **Creato** ad **Aperto**. Lo stato del record, ad esempio per una una fattura di acquisto, viene aggiornato da **Aperto** a **Approvazione in sospeso** e rimane bloccato per l'elaborazione finché tutti i responsabili dell'approvazione non hanno approvato il record.

Quando il responsabile dell'approvazione ha approvato il record, lo stato viene impostato su **Rilasciato**. È quindi possibile continuare con i task del record.

## <a name="to-cancel-requests-for-approval"></a>Per annullare le richieste di approvazione

La seguente attività viene eseguita da un utente approvazione con diritti di approvazione.

È possibile che un cliente desideri modificare un ordine dopo che questo è stato inviato per l'approvazione. In questo caso, è possibile annullare il processo di approvazione e apportare le modifiche necessarie all'ordine prima di richiedere nuovamente l'approvazione.

- Nella pagina che visualizza il record, scegli l'azione **Annulla richiesta di approvazione** .

Una volta che la richiesta di approvazione è stata annullata, lo stato della voce di approvazione correlata viene impostato automaticamente su **Annullato**. Lo stato del record viene aggiornato da **Approvazione in sospeso** ad **Aperto**. Il processo di approvazione può quindi essere avviato nuovamente.

## <a name="to-approve-or-reject-requests-for-approval"></a>Per approvare o rifiutare le richieste di approvazione

La seguente attività viene eseguita da un utente approvazione con diritti di approvazione.

È possibile elaborare le richieste di approvazione nella pagina **Richieste da approvare**, ad esempio per approvare più richieste per volta. In alternativa, è possibile elaborare ogni richiesta nel record correlati, ad esempio nella pagina **Fattura acquisto** scegliendo il collegamento nella notifica ricevuta.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Richieste da approvare**, quindi scegli il collegamento correlato.
2. Selezionare una o più righe per il record o i record che si desidera approvare o rifiutare.
3. Selezionare l'azione **Approva**, **Rifiuta** o **Delega**.

Una volta che un record è stato approvato o rifiutato, lo stato di approvazione nel campo **Stato** viene automaticamente impostato su **Approvato** o **Rifiutato**.

Se è impostata una gerarchia di responsabili, lo stato del record sarà impostato su **Approvazione in sospeso** fino a quando tutti i responsabili non avranno approvato il record. A quel punto lo stato del record verrà impostato automaticamente su **Rilasciato**.

Contemporaneamente, lo stato di approvazione cambierà da **Creato** ad **Aperto** non appena verrà creata una richiesta di approvazione per il record. Se la richiesta viene rifiutata, lo stato di approvazione diventa **Rifiutato**. Lo stato rimane **Aperto** o **Rifiutato** fino a quando tutti i responsabili non hanno approvato la richiesta.

## <a name="to-delegate-requests-for-approval"></a>Per delegare le richieste di approvazione

La seguente attività viene eseguita da un utente approvazione con diritti di approvazione.

Per impedire l'accumularsi dei documenti nel sistema o un eventuale altro blocco del flusso di lavoro, il responsabile dell'approvazione e l'amministratore dell'approvazione possono delegare la richiesta di approvazione a un sostituto. Il sostituto può essere un sostituto designato, il responsabile approvazione diretto o l'amministratore approvazioni, in tale ordine di priorità. Questa funzionalità viene in genere utilizzata se il responsabile dell'approvazione si trova fuori sede e non è in grado di approvare le richieste prima della data di scadenza.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Richieste da approvare**, quindi scegli il collegamento correlato.
2. Selezionare una o più righe per le richieste di approvazione che si desidera delegare a un responsabile sostitutivo e quindi scegliere l'azione **Delega**.

Viene inviata una notifica nella quale viene chiesto al responsabile sostitutivo di approvare la richiesta.

## <a name="to-manage-overdue-approval-requests"></a>Per gestire le richieste di approvazione scadute

La seguente attività viene eseguita da un utente approvazione con diritti di approvazione.

A intervalli regolari, è necessario ricordare, agli utenti del flusso di lavoro di approvazione, le richieste di approvazione scadute su cui devono intervenire. A tal fine è possibile utilizzare la funzione **Invia notifiche di approvazione scadute**.

La funzione **Invia notifiche di approvazione scadute** cerca tutte le richieste di approvazione aperte attualmente scadute. Ogni responsabile a cui è associato almeno un movimento di approvazione scaduto riceve una notifica con l'elenco di tutte le relative richieste di approvazione scadute. La notifica viene anche inviata in copia per conoscenza al responsabile dell'approvazione e a tutti i richiedenti delle approvazioni scadute. Questa operazione è utile se il movimento di approvazione scaduto deve essere delegato a un sostituto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Richieste di approvazione scadute**, quindi scegli il collegamento correlato.
2. Nella pagina **Richieste di approvazione scadute**, scegliere l'azione **Invia notifiche di approvazioni scadute**.

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/use-approval-workflows/)

## <a name="see-also"></a>Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Vendite](sales-manage-sales.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]