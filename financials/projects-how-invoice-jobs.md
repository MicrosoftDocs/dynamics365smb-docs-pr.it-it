---
title: Creare una fattura di vendita per fatturare una commessa| Documenti Microsoft
description: Viene descritto come fatturare ai clienti le spese commessa durante lo svolgimento di un progetto.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2fdc8f99fa81a0eecd55438bba33b1a93335a416
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-invoice-jobs"></a>Procedura: Fatturare commesse
Durante il progetto, è possibile che si accumulino i costi di commessa derivanti dall'utilizzo delle risorse, dai materiali e dagli acquisti correlati alla commessa. A seconda dello stato di avanzamento della commessa, tali transazioni vengono inserite nelle registrazioni commesse. È importante registrare tutti i costi prima di fatturare al cliente.

È possibile fatturare l'intera commessa dalla finestra **Righe task commessa** oppure fatturare solo le righe fatturabili selezionate dalla finestra **Righe pianificazione**. La fatturazione può essere effettuata dopo la chiusura della commessa oppure durante lo svolgimento delle operazioni correlate alla commessa, a determinati intervalli basati su un'apposita programmazione.

> [!NOTE]  
>   Se si seleziona **Fatturabile** nel campo **Tipo riga commessa** dei documenti di acquisto per gli acquisti correlati alla commessa, vengono create le righe di pianificazione commessa che sono pronte per la fatturazione al cliente. Per ulteriori informazioni, vedere [Procedura: Gestire gli approvvigionamenti per un progetto](projects-how-manage-project-supplies.md).

## <a name="to-create-and-post-a-job-sales-invoice"></a>Per creare e registrare una fattura di vendita per una commessa
È possibile creare una fattura per una commessa o per uno o più task commessa per un cliente al completamento del lavoro da fatturare o al raggiungimento della data per la fatturazione in base a una programmazione di fatturazione.

Dalla finestra **Commesse** è possibile fatturare a un cliente selezionando la commessa, quindi scegliendo l'azione **Crea fattura vendita per commessa**. Nella procedura che segue viene mostrato come utilizzare un processo batch per fatturare più commesse.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commessa - Crea fattura vendita**, quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Impostare i filtri se si desidera limitare le commesse che devono essere elaborate nel processo batch.
4. Scegliere il pulsante **OK** per creare le fatture di assistenza.  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a>Per creare più fatture di vendita commesse dalle righe di pianificazione commessa
È possibile creare una fattura da righe di pianificazione commessa e indicare in quella occasione la quantità dell'articolo, la risorsa o il conto di contabilità generale che si desidera fatturare.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.
2. Aprire una commessa appropriata.
3. Selezionare un task commessa per il quale il campo **Tipo task commessa** contiene **Registrazione**, quindi scegliere l'azione **Righe pianificazione commessa**.  
4. In una riga di pianificazione commessa, nel campo **Qtà da trasferire in fattura** , immettere la quantità dell'articolo, la risorsa, il tipo del conto di contabilità generale che si desidera fatturare.  
5. Scegliere l'azione **Crea fattura di vendita**.
6. Nella finestra **Commessa - Crea fattura vendita**, immettere la data di registrazione e se si desidera creare una nuova fattura o aggiungere questa fattura a una esistente.
7. Scegliere il pulsante **OK**.  

    Nella riga di pianificazione commessa, nel campo **Qtà trasferita in fattura**, è possibile visualizzare la quantità.
8. Nella finestra **Righe pianificazione commessa** scegliere l'azione **Fatture/Note credito vendite**.

    Verrà visualizzata la finestra **Fatture di vendita** nella quale sarà mostrata la quantità che è stata trasferita in fattura.  
9. Apportare tutte le modifiche aggiuntive, quindi scegliere l'azione **Registra**.

> [!NOTE]  
>   La procedura sopra riportata è simile per la creazione, la revisione e la registrazione di una nota di credito di vendita correlata a una commessa.

## <a name="to-calculate-and-post-job-completion-entries"></a>Per calcolare e registrare i movimenti di completamento della commessa
Al termine di tutte le operazioni di registrazione e fatturazione dell'utilizzo per una commessa, è necessario aggiornare la commessa in modo che il campo **Stato** sia impostato su **Completato**. Successivamente, è necessario stornare eventuali WIP registrati nella contabilità generale.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare una commessa aperta, quindi scegliere l'azione **Modifica**.
3. Nel campo **Stato** selezionare **Completato**.
4. Seguire i passaggi di assistenza per calcolare e registrare il WIP. In alternativa, seguire i passaggi 5 e 6 per effettuare questa operazione manualmente.  
5. Scegliere l'azione **Calcola WIP**.
6. Nella finestra **Commessa - Calcola WIP** compilare i campi in base alle esigenze.  

     Per i movimenti WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.  
7. Scegliere l'azione **Commessa - Registra WIP in C/G**.
8. Nella finestra **Commessa - Registra WIP in C/G** compilare i campi in base alle esigenze.  

     Per i movimenti C/G WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.

## <a name="see-also"></a>Vedi anche
[Gestire progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

