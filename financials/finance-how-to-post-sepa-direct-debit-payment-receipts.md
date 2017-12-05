---
title: Registrare i pagamenti di addebiti diretti SEPA | Microsoft Docs
description: "Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 021c48efc6bf6b1fdb7b17bf742cb6f084d3964b
ms.contentlocale: it-it
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a>Procedura: Registrare ricevute di pagamento di addebiti diretti SEPA
Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate. Per ulteriori informazioni, vedere [Procedura: Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

È possibile registrare la ricevuta di pagamento direttamente dalla finestra **Riscossioni addebiti diretti** o dalla finestra **Movimenti riscossioni addebiti diretti**. In alternativa, è possibile inoltrare il lavoro a un altro utente preparando le righe registrazioni correlate.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Per registrare una ricevuta di pagamento con addebito diretto dalla finestra Riscossioni di addebiti diretti  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Riscossioni addebiti diretti**, quindi scegliere il collegamento correlato.  
2. Selezionare una riga per una riscossione di addebiti diretti esportata in un file della banca ed elaborata correttamente dalla banca. Per ulteriori informazioni, vedere [Procedura: Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Scegliere l'azione **Registra ricevute di pagamento**.  
4. Nella finestra **Registra riscossione addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nr. riscossione di addebiti diretti**|Specificare la riscossione di addebiti diretti per cui si desidera registrare la ricevuta di pagamento.|  
    |**Definizione registrazioni COGE**|Specificare quale definizione di registrazione COGE utilizzare per registrare la ricevuta di pagamento, ad esempio le ricevute delle entrate di cassa.|  
    |**Nome batch registrazioni COGE**|Specificare quale il batch di registrazioni COGE utilizzare per la registrazione della ricevuta di pagamento.|  
    |**Crea solo registrazioni**|Selezionare questa casella di controllo se non si desidera registrare la ricevuta di pagamento quando si sceglie il pulsante **OK**. La ricevuta di pagamento verrà preparata nella registrazione specificata e non verrà registrata finché non vengono contabilizzate le righe registrazioni in questione.|  

5. Scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedi anche  
 [Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Vendite](sales-manage-sales.md)

