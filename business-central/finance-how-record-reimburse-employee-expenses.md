---
title: Registrare e rimborsare le spese di lavoro dei dipendenti | Microsoft Docs
description: Registrare le spese di un dipendente con le registrazioni COGE nel conto del dipendente e successivamente registrare un pagamento verso il conto bancario del dipendente per rimborsarlo delle spese sostenute per il lavoro.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 660cb4d9f2238bffeb1c7eaf49d5d70dbb654f45
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244793"
---
# <a name="record-and-reimburse-employees-expenses"></a>Registrare e rimborsare le spese dei dipendenti
[!INCLUDE[d365fin](includes/d365fin_md.md)] supporta le transazioni per i dipendenti in modo simile alle transazioni per i fornitori. Di conseguenza, sono disponibili alcune categorie di registrazione dipendenti che consentono di assicurarsi che i movimenti contabili per i dipendenti siano registrati nei conti di pertinenza nella contabilità COGE.

> [!NOTE]  
> Le transazioni relative ai dipendenti possono essere registrate solo nella valuta locale. I rimborsi ai dipendenti non supportano sconti e e tolleranze sui pagamenti.

Se i dipendenti spendono denaro personale durante le attività lavorative, è possibile registrare le spese nei conti dei dipendenti. È quindi possibile rimborsare il dipendente effettuando un pagamento sul conto bancario del dipendente, analogamente a quando si pagano i fornitori.

## <a name="to-record-an-employees-expense"></a>Per registrare le spese di un dipendente
Le spese del dipendente vengono registrate nella pagina **Contabilità generale**.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.
2. Aprire il batch registrazioni COGE appropriato. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).
3. In una nuova riga di registrazione, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Ripetere il passaggio 3 per le spese che il dipendente ha pagato.

    > [!TIP]  
    > Se si desidera immettere più righe di spesa sopra una riga di contropartita per il conto bancario del dipendente, selezionare la casella di controllo **Suggerisci importo contropartita** nella riga del batch nella pagina **Batch registrazioni COGE**. Il campo **Importo** nella riga di contropartita viene precompilato automaticamente con il valore necessario per pareggiare le spese.
5. Scegliere l'azione **Registra** per registrare spese nel conto del dipendente.

## <a name="to-reimburse-an-employee"></a>Per rimborsare un dipendente
I dipendenti vengono rimborsati registrando i pagamenti nei relativi conti bancari nella pagina **Registrazioni pagamenti**.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.
2. Aprire il batch registrazioni pagamenti appropriato. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).
3. Compilare i campi, se necessario. Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).
4. In alternativa, scegliere l'azione **Suggerisci pagamenti dipendente** per inserire automaticamente righe di registrazione per rimborsi in sospeso al dipendente.
5. Scegliere l'azione **Registra** per registrare il rimborso.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Per riconciliare i rimborsi con movimenti contabili del dipendente
I pagamenti dei dipendenti si applicano ai movimenti contabili aperti correlati come si fa per i pagamenti dei fornitori, ad esempio nella pagina **Registrazione riconciliazione pagamenti**, in base ai movimenti relativi dell'estratto conto. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md). In alternativa, è possibile applicarli manualmente nella pagina **Movimenti contabili dipendente**. Per ulteriori informazioni, vedere [Riconciliare manualmente i pagamenti ai fornitori con la registrazioni pagamenti o dai movimenti contabili fornitori](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Vedi anche
[Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Stornare le registrazioni](finance-how-reverse-journal-posting.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
