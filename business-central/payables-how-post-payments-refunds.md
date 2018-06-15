---
title: Collegare i pagamenti ai documenti correlati e registrali| Microsoft Docs
description: Descrive come registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: it-it
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Registrare pagamenti e rimborsi
Nella finestra **Registrazioni pagamenti** è possibile registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti. Quando si registra una riga di registrazioni dei pagamenti, l'importo pagato viene registrato sul conto bancario di sistema specificato. È quindi necessario intraprendere le azioni necessarie per eseguire il trasferimento effettivo del denaro dal relativo conto bancario.

Se si compila il campo **Collega-a nr. doc.** con la fattura o la nota di credito che deve essere pagata o rimborsata, il documento in questione viene impostato su pagato quando tale registrazione viene contabilizzata. Questa procedura viene definita "collegamento". In alternativa all'applicazione durante la registrazione dei pagamenti, è possibile utilizzare le finestre **Collega movimenti fornitori** e **Collega movimenti clienti** dopo aver effettuato la registrazione dei pagamenti. Per ulteriori informazioni, vedere, per esempio, [Riconciliare manualmente i pagamenti ai fornitori](payables-how-apply-purchase-transactions-manually.md).

La funzione **Suggerisci pagamenti fornitore** può essere utile per compilare automaticamente le righe delle registrazioni pagamenti in base alle priorità e alle data di scadenza. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md). Con questa funzione, il campo **Collega-a nr. doc.** viene sempre compilato.

Oltre alla registrazione che il pagamento è stato effettuato, è possibile utilizzare la finestra **Registrazioni pagamenti** per emettere il pagamento per l'ulteriore elaborazione da parte della banca. Per ulteriori informazioni, vedere [Effettuare pagamenti tramite assegno](payables-how-work-checks.md) e [Effettuare pagamenti elettronici](payables-how-export-payments-bank-file.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni pagamenti**, quindi scegliere il collegamento correlato.
2. Aprire il batch contabile che verrà dedicato ai pagamenti.
3. Se si conoscono i clienti da pagare o rimborsare, compilare i campi manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per collegare anche il pagamento alla relativa fattura o nota di credito, selezionare il campo **Collega-a nr. doc.** nella finestra **Collega movimenti fornitori**, selezionare la relativa fattura o nota di credito, quindi selezionare il pulsante **OK**.

    Molti campi, ad esempio i campi **Importo** e **Data scadenza** vengono compilati con le informazioni tratte dal documento selezionato.
5. In alternativa, utilizzare la funzione **Sugg. pagamenti fornitore**. Tutte le informazioni applicabili e gli importi vengono quindi inseriti anche nelle righe del giornale di registrazione. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).

    I messaggi guideranno la compilazione corretta dei campi richiesti.
6.  Una volta completate tutte le righe di registrazione pagamento, scegliere l'azione **Registra**.

## <a name="see-also"></a>Vedi anche
[Effettuare pagamenti tramite assegno](payables-how-work-checks.md)  
[Effettuare pagamenti elettronici](payables-how-export-payments-bank-file.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

