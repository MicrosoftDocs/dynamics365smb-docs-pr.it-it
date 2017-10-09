---
title: Correggere o annullare una fattura di vendita registrata | Documenti Microsoft
description: Descrive come correggere oppure annullare una fattura di vendita registrata e collegarla a una nota di credito di vendita.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6de89bc0865fbe8617e33288b9c0c8fe7da802ef
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a>Procedura: Correggere o annullare le fatture di vendita non pagate
È possibile correggere o annullare una fattura di vendita registrata. Ciò risulta utile se si effettua un errore o se il cliente richiede una modifica.

> [!NOTE]  
>   Dopo che una fattura di vendita registrata è stata parzialmente o interamente pagata, non è possibile correggerla o annullarla dalla fattura di vendita registrata stessa. In alternativa, è necessario creare manualmente una nota di credito di vendita per annullare la vendita e per rimborsare il cliente, facoltativamente gestito con un ordine di reso vendita. Per ulteriori informazioni vedere [Procedura: Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).

Nella finestra **Fatture vendita registrate** è possibile scegliere l'azione **Rettifica** o **Annulla** per eseguire le operazioni descritte nella seguente tabella.

| Azione | Descrizione |
| --- | --- |
| **Correzione** |La fattura di vendita registrata viene annullata. Una nuova fattura di vendita con le stesse informazioni viene creata. È possibile apportare la correzione e successivamente continuare il processo di vendita. La nuova fattura di vendita ha un numero diverso rispetto alla fattura di vendita iniziale. Una nota di credito di vendita correttiva viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale. Nella fattura di vendita registrata iniziale, le caselle di controllo Annullato e Pagato sono selezionate. |
| **Annulla** |La fattura di vendita registrata viene annullata. Una nota di credito di vendita correttiva viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale. Nella fattura di vendita registrata iniziale, le caselle di controllo Annullato e Pagato sono selezionate. |

Quando si rettifica o si annulla una fattura di vendita registrata, la nota di credito di vendita viene applicata a tutti i movimenti contabili generali e di inventario creati quando la fattura di vendita iniziale è stata registrata. Ciò consente di stornare la fattura di vendita nei record finanziari e lascia la nota di credito di vendita registrata correttiva per l'audit trail.

## <a name="to-correct-a-posted-sales-invoice"></a>Per correggere una fattura di vendita registrata
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di vendita registrate** e quindi scegliere il collegamento correlato.  
2. Selezionare la fattura di vendita che si desidera rettificare.

    > [!NOTE]  
>   Se viene selezionata la casella di controllo **Annullata**, non è possibile rettificare la fattura di vendita registrata poiché è già stata rettificata o annullata.
3. Nella finestra **Fattura vendita registrata** scegliere l'azione **Rettifica**.  
4. Viene creata una nuova fattura di vendita con le stesse informazioni in cui è possibile apportare la rettifica. Il campo **Annullato** nella fattura di vendita registrata iniziale viene modificato in **Sì**.

    Una nota di credito di vendita viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale.
5. Scegliere l'azione **Mostra nota credito di rettifica** per visualizzare la nota di credito di vendita registrata che annulla la fattura di vendita registrata iniziale.

## <a name="to-cancel-a-posted-sales-invoice"></a>Per annullare una fattura di vendita registrata
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di vendita registrate** e quindi scegliere il collegamento correlato.  
2. Selezionare la fattura di vendita che si desidera annullare.

    > [!NOTE]  
>   Se viene selezionata la casella di controllo **Annullata**, non è possibile annullare la fattura di vendita registrata poiché è già stata annullata o corretta.
3. Nella finestra **Fattura vendita registrata** scegliere l'azione **Annulla**.

    Una nota di credito di vendita viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale. Il campo **Annullato** nella fattura di vendita registrata iniziale viene modificato in **Sì**.
4. Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di vendita registrata che annulla la fattura di vendita registrata iniziale.

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

