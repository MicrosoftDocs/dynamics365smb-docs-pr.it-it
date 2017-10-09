---
title: Registrare e rimborsare le spese di lavoro dei dipendenti | Microsoft Docs
description: Registrare le spese di un dipendente con le registrazioni COGE nel conto del dipendente e successivamente registrare un pagamento verso il conto bancario del dipendente per rimborsarlo delle spese sostenute per il lavoro.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8674fcc050e11c9ecb1c423fc5048c1ef630e1ac
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-record-and-reimburse-employees-expenses"></a>Procedura: Registrare e rimborsare le spese dei dipendenti
[!INCLUDE[d365fin](includes/d365fin_md.md)] supporta le transazioni per i dipendenti in modo simile alle transazioni per i fornitori. Di conseguenza, sono disponibili alcune categorie di registrazione dipendenti che consentono di assicurarsi che i movimenti contabili per i dipendenti siano registrati nei conti di pertinenza nella contabilità COGE.

> [!NOTE]  
> Le transazioni relative ai dipendenti possono essere registrate solo nella valuta locale. I rimborsi ai dipendenti non supportano sconti e e tolleranze sui pagamenti.

Se i dipendenti spendono denaro personale durante le attività lavorative, è possibile registrare le spese nei conti dei dipendenti. È quindi possibile rimborsare il dipendente effettuando un pagamento sul conto bancario del dipendente, analogamente a quando si pagano i fornitori.

## <a name="to-record-an-employees-expense"></a>Per registrare le spese di un dipendente
Le spese del dipendente vengono registrate nella finestra **Contabilità generale**.
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.
2. Aprire il batch registrazioni COGE appropriato. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).
3. In una nuova riga di registrazione, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Ripetere il passaggio 3 per le spese che il dipendente ha pagato.

    > [!TIP]  
    > Se si desidera immettere più righe di spesa sopra una riga di contropartita per il conto bancario del dipendente, selezionare la casella di controllo **Suggerisci importo contropartita** nella riga del batch nella finestra **Batch registrazioni COGE**. Il campo **Importo** nella riga di contropartita viene precompilato automaticamente con il valore necessario per pareggiare le spese.
5. Scegliere l'azione **Registra** per registrare spese nel conto del dipendente.

## <a name="to-reimburse-an-employee"></a>Per rimborsare un dipendente
I dipendenti vengono rimborsati registrando i pagamenti nei relativi conti bancari nella finestra **Registrazioni pagamenti**.
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni pagamenti**, quindi scegliere il collegamento correlato.
2. Aprire il batch registrazioni pagamenti appropriato. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).
3. Compilare i campi, se necessario. Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).
4. In alternativa, scegliere l'azione **Suggerisci pagamenti dipendente** per inserire automaticamente righe di registrazione per rimborsi in sospeso al dipendente.
5. Scegliere l'azione **Registra** per registrare il rimborso.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Per riconciliare i rimborsi con movimenti contabili del dipendente
I pagamenti dei dipendenti si applicano ai movimenti contabili aperti correlati come si fa per i pagamenti dei fornitori, ad esempio nella finestra **Registrazione riconciliazione pagamenti**, in base ai movimenti relativi dell'estratto conto. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e Riconciliazione dei conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md). In alternativa, è possibile applicarli manualmente nella finestra **Movimenti contabili dipendente**. Per ulteriori informazioni, vedere [Procedura: Riconciliare manualmente i pagamenti ai fornitori](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Vedi anche
[Procedura: Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Procedura: Stornare le registrazioni](finance-how-reverse-journal-posting.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

