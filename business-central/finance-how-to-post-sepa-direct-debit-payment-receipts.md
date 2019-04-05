---
title: Registrare i pagamenti di addebiti diretti SEPA | Microsoft Docs
description: Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6d24df38b980542b1c77d737b8f661fac0df29fa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802043"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a>Registrare ricevute di pagamento di addebiti diretti SEPA
Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate. Per ulteriori informazioni, vedere [Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

È possibile registrare la ricevuta di pagamento direttamente dalla pagina **Riscossioni addebiti diretti** o dalla pagina **Movimenti riscossioni addebiti diretti**. In alternativa, è possibile inoltrare il lavoro a un altro utente preparando le righe registrazioni correlate.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Per registrare una ricevuta di pagamento con addebito diretto dalla pagina Riscossioni di addebiti diretti  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Riscossioni addebiti diretti** e quindi scegliere il collegamento correlato.  
2. Selezionare una riga per una riscossione di addebiti diretti esportata in un file della banca ed elaborata correttamente dalla banca. Per ulteriori informazioni, vedere [Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Scegliere l'azione **Registra ricevute di pagamento**.  
4. Nella pagina **Registra riscossione addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.  

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
