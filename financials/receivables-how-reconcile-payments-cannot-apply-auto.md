---
title: 'Procedura: Riconciliare i pagamenti che non possono essere collegati automaticamente | Documenti Microsoft'
description: 'Procedura: Riconciliare i pagamenti che non possono essere collegati automaticamente'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7b4c109ebda260ee86e2b955a17389b54493de65
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>Procedura: Riconciliare i pagamenti che non possono essere collegati automaticamente
Talvolta può essere necessario gestire i pagamenti al conto corrente bancario che non possono essere collegati a un movimento aperto di contabilità generale, cliente o fornitore correlato. I motivi possono essere che in [!INCLUDE[d365fin](includes/d365fin_md.md)] non sono presenti documenti cui possa essere collegato il pagamento o che il documento correlato in [!INCLUDE[d365fin](includes/d365fin_md.md)] ha un importo diverso da quello della transazione, ad esempio, a causa del cambio della valuta. Nella finestra **Registrazione riconciliazione pagamenti** tutti gli importi delle transazioni per i pagamenti che non sono ancora collegati vengono visualizzati nel campo **Differenza**, inclusi gli importi che non possono essere collegati per i motivi citati prima.

I pagamenti che non possono essere collegati possono essere visualizzati nelle righe di registrazione riconciliazione pagamenti nei seguenti modi:

* Il valore nel campo **Differenza** è uguale al valore del campo **Importo transazioni**, pertanto nessuna parte del pagamento può essere collegata a un movimento contabile del conto corrente bancario, fornitore o cliente aperto.
* Il valore nel campo **Differenza** è inferiore al valore del campo **Importo transazioni**, pertanto una parte del pagamento può essere collegata a un movimento contabile del conto corrente bancario, fornitore o cliente aperto. La parte residua del pagamento non può essere collegata e deve essere riconciliata manualmente o registrandola direttamente in un conto.

Per riconciliare questi pagamenti, scegliere il pulsante Trasferisci differenza a conto quindi specificare su quale conto registrare l'importo del campo Differenza quando si effettua la registrazione riconciliazione pagamenti.

**Nota**: tale funzionalità consente di impostare la riconciliazione automatica dei pagamenti ricorrenti che non possono essere collegati ai relativi movimenti contabili del conto corrente bancario, fornitore o cliente aperti. Per ulteriori informazioni, vedere [Procedura: Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Per riconciliare i pagamenti che non possono essere collegati
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazioni riconciliazione pagamenti**, quindi scegliere il collegamento correlato.
2. Aprire una registrazione della riconciliazione di pagamento. Per ulteriori informazioni, vedere [Procedura: Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).
3. Scegliere **Trasferisci differenza a conto**. Si apre la finestra **Trasferisci differenza a conto**.
4. Nel campo **Tipo conto** specificare il tipo di conto in cui sarà registrato l'importo di pagamento.
5. Nel campo **Nr. conto** specificare il conto in cui sarà registrato l'importo di pagamento.
6. Nel campo **Descrizione** specificare il testo che descrive questa registrazione di pagamento diretto. Per impostazione predefinita, viene inserito il testo nel campo **Testo transazione** nella riga di registrazione riconciliazione pagamenti.
7. Scegliere il pulsante **OK**.

Se il valore nel campo **Differenza** è uguale al valore del campo **Importo transazioni** quando si registra la riconciliazione pagamenti, l'intero pagamento nella riga di registrazione sarà registrato direttamente nel conto di contropartita specificato.

Se il valore nel campo **Differenza** è inferiore al valore del campo **Importo transazioni**, verrà creata una nuova riga di registrazione aggiuntiva con lo stesso testo e la stessa data e con la differenza inserita nel campo **Importo transazioni**. Nella riga di registrazione originale, la differenza verrà dedotta dal valore nel campo **Importo transazioni** e il pagamento rimarrà collegato al relativo movimento contabile del conto corrente bancario, fornitore o cliente. Quando si contabilizza la registrazione riconciliazione pagamenti, una parte del pagamento verrà registrata come pagamento collegato. L'altra parte del pagamento verrà registrata direttamente nel conto specificato.

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

