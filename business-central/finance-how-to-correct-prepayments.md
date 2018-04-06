---
title: Come rettificare i pagamenti anticipati | Microsoft Docs
description: "È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso. È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 12da4eb32b17c115cf089a09f1ad314b55c4d334
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="correct-prepayments"></a>Rettificare i pagamenti anticipati
È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso. È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato.  

## <a name="to-correct-a-prepayment"></a>Per rettificare un pagamento anticipato
La procedura seguente illustra come emettere una nota di credito di pagamento anticipato per annullare tutti i pagamenti anticipati fatturati per un ordine di vendita.  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di vendita**, quindi scegliere il collegamento correlato.  
2. Aprire l'ordine di vendita appropriato.
3. Scegliere l'azione **Pagamento anticipato**, quindi scegliere l'azione **Registra nota credito pagamento anticipato** o l'azione **Registra e stampa nota cr. pagam. ant.**  
4. Nella finestra **Nota credito vendita** rettificare i movimenti desiderati, come per qualsiasi nota di credito vendita. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).     

    > [!NOTE]  
    > Per ridurre l'importo nel campo **Importo riga**, è necessario prima aumentare la percentuale pagamento anticipato nella riga in modo che il valore nel campo **Importo riga pagam. ant.** non scenda sotto il valore del campo **Fattura importo pagam. ant.**.

5. Per creare una fattura pagamento anticipato per le nuove righe nota di credito di vendita,, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato** o l'azione **Registra e stampa fattura pagam. ant.**.  
6. Per emettere una fattura pagamento anticipato aggiuntiva, aumentare l'importo pagamento anticipato in una o più righe e registrare la fattura pagamento anticipato. Verrà creata una nuova fattura per la differenza tra gli importi di pagamenti anticipati fatturati e i nuovi importi di pagamenti anticipati.  

## <a name="see-also"></a>Vedi anche  
[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

