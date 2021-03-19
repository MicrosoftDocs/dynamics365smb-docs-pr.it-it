---
title: Correggere o annullare una fattura vendita registrata
description: Descrive come correggere oppure annullare una fattura di vendita registrata e collegarla a una nota di credito di vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 01/11/2021
ms.author: edupont
ms.openlocfilehash: 7a14155d0b9dc780fa65bbf1f151e82b8a175984
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393401"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Correggere o annullare le fatture di vendita non pagate

È possibile rettificare o annullare una fattura vendita registrata non pagata, purché non sia stata completamente spedita. Ciò risulta utile se si effettua un errore o se il cliente richiede una modifica prima del completamento dell'invio. In tutti gli altri scenari, si consiglia di creare direttamente una nota credito vendita correttiva. Per ulteriori informazioni, vedere [Per creare una nuova nota di credito di vendita da una fattura di vendita registrata](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Dopo che una fattura di vendita registrata è stata parzialmente o interamente pagata, non è possibile correggerla o annullarla dalla fattura di vendita registrata stessa. In alternativa, è necessario creare manualmente una nota di credito di vendita per annullare la vendita e per rimborsare il cliente, facoltativamente gestito con un ordine di reso vendita. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).

La differenza tra l'annullamento o la correzione di una fattura vendita registrata che non è stata pagata o spedita è descritta nella tabella seguente.

| Azione | Descrizione |
| --- | --- |
| **Annulla** |La fattura di vendita registrata viene annullata. Una nota di credito di vendita correttiva viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale. Nella fattura vendita registrata iniziale, le caselle di controllo **Annullato** e **Pagato** sono selezionate. |
| **Correzione** |La fattura vendita registrata viene annullata. Viene creata una nuova fattura vendita con le stesse informazioni, a meno che l'ordine vendita registrato non sia stato registrato da un ordine vendita. In tal caso, si consiglia invece di annullare la fattura vendita registrata e quindi di apportare la correzione e di continuare il processo di vendita dall'ordine vendita originale. <br/><br/>La nuova fattura di vendita ha un numero diverso rispetto alla fattura di vendita iniziale. Una nota di credito di vendita correttiva viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale. Nella fattura vendita registrata iniziale, le caselle di controllo **Annullato** e **Pagato** sono selezionate. |

Quando si rettifica o si annulla una fattura di vendita registrata, la nota di credito di vendita viene applicata a tutti i movimenti contabili generali e di inventario creati quando la fattura di vendita iniziale è stata registrata. Ciò consente di stornare la fattura di vendita nei record finanziari e lascia la nota di credito di vendita registrata correttiva per l'audit trail.  

> [!TIP]
> Se è stata registrata una fattura di pagamento anticipato per una fattura di vendita che si corregge o si annulla, è necessario correggere o annullare anche il pagamento anticipato. Per ulteriori informazioni, vedere [Correggere i pagamenti anticipati](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice"></a>Per annullare una fattura di vendita registrata

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), quindi immettere **Fatture di vendita registrate** e quindi scegliere il collegamento correlato.  
2. Selezionare la fattura di vendita che si desidera annullare.

    > [!NOTE]  
    >   Se viene selezionata la casella di controllo **Annullata**, non è possibile annullare la fattura di vendita registrata poiché è già stata annullata o corretta.
3. Nella pagina **Fattura vendita registrata** scegliere l'azione **Annulla**.

    Una nota di credito di vendita viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale. Il campo **Annullato** nella fattura di vendita registrata iniziale viene modificato in **Sì**.
4. Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di vendita registrata che annulla la fattura di vendita registrata iniziale.

### <a name="partial-invoice-posting-also-supported"></a>Anche la registrazione parziale delle fatture è supportata

Se l'annullamento è correlato a una registrazione parziale della fattura, la riga dell'ordine di vendita di origine viene aggiornata per riflettere la quantità fatturata annullata. I campi **Qtà da fatturare** e **Qtà fatturata** nella riga dell'ordine vendita correlato vengono reimpostati sui valori precedenti alla registrazione parziale.

## <a name="to-correct-a-posted-sales-invoice"></a>Per correggere una fattura di vendita registrata

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), quindi immettere **Fatture di vendita registrate** e scegliere il collegamento correlato.  
2. Selezionare la fattura di vendita che si desidera rettificare.

    > [!NOTE]  
    >   Se viene selezionata la casella di controllo **Annullata**, non è possibile rettificare la fattura di vendita registrata poiché è già stata rettificata o annullata.
3. Nella pagina **Fattura vendita registrata** scegliere l'azione **Rettifica**.  

    > [!NOTE]
    > Se la fattura vendita è stata registrata da un ordine vendita, si consiglia di *annullare* questa fattura vendita e di elaborare la correzione dall'ordine vendita originale. Se l'ordine cliente originale è stato eliminato, ad esempio se è stato spedito completamente, è possibile creare un nuovo ordine vendita utilizzando l'azione **Copia documento**. Per ulteriori informazioni, vedere [Per creare una nota di credito di vendita copiando una fattura di vendita registrata](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Viene creata una nuova fattura di vendita con le stesse informazioni in cui è possibile apportare la rettifica. Il campo **Annullato** nella fattura di vendita registrata iniziale viene modificato in **Sì**.

    Una nota di credito di vendita viene automaticamente creata e registrata per annullare la fattura di vendita registrata iniziale.
5. Scegliere l'azione **Mostra nota credito di rettifica** per visualizzare la nota di credito di vendita registrata che annulla la fattura di vendita registrata iniziale.

## <a name="see-also"></a>Vedi anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]