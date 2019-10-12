---
title: Collegare i pagamenti ai documenti correlati e registrali| Microsoft Docs
description: Descrive come registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 5f9301541e73b4137f6c241a18e2f25c4009fc76
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314294"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrare pagamenti e resi nelle Registrazioni pagamenti

Nella pagina **Registrazioni pagamenti** è possibile registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti. Quando si registra una riga di registrazioni dei pagamenti, l'importo pagato viene registrato sul conto bancario di sistema specificato. È quindi necessario intraprendere le azioni necessarie per eseguire il trasferimento effettivo del denaro dal relativo conto bancario.  

Le registrazioni pagamenti sono registrazioni generali ottimizzate per eseguire i pagamenti. È possibile aggiungere rapidamente le righe manualmente, si può consentire a [!INCLUDE[d365fin](includes/d365fin_md.md)] di suggerire i pagamenti dei fornitori ed applicare il pagamento ai documenti registrati. Anche se si sta eseguendo i pagamenti, si immette un importo positivo nel campo **Importo documento**. In base al tipo di documento per la riga delle registrazioni, questo importo viene quindi convertito in un importo negativo nelle transazioni sottostanti. In questo modo, è più veloce aggiungere le righe nelle registrazioni manualmente. Se si preferisce immettere importi negativi, è possibile personalizzare le registrazioni pagamenti per mostrare invece il campo **Importo**.  

- Applicare i pagamenti alle fatture o note di credito

    Se si compila il campo **Collega-a nr. doc.** con la fattura o la nota di credito che deve essere pagata o rimborsata, il documento in questione viene impostato su pagato quando tale registrazione viene contabilizzata. Questa procedura viene definita "collegamento". In alternativa all'applicazione durante la registrazione dei pagamenti, è possibile utilizzare le pagine **Collega movimenti fornitori** e **Collega movimenti clienti** dopo aver effettuato la registrazione dei pagamenti. Per ulteriori informazioni, vedere, ad esempio, [Riconciliare manualmente i pagamenti ai fornitori con la registrazioni pagamenti o dai movimenti contabili fornitori](payables-how-apply-purchase-transactions-manually.md).  

- Ricevere pagamenti suggeriti per fornitori o dipendenti

    Le funzioni **Suggerisci pagamenti fornitore** e **Suggerisci pagamenti dipendente** possono essere utili per compilare automaticamente le righe delle registrazioni pagamenti in base alle priorità e alle data di scadenza. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md). Con questa funzione, il campo **Collega-a nr. doc.** viene sempre compilato.  

- Stampare assegni e inviare elettronicamente i pagamenti alla banca

    Oltre alla registrazione che il pagamento è stato effettuato, è possibile utilizzare la pagina **Registrazioni pagamenti** per emettere il pagamento per l'ulteriore elaborazione da parte della banca. Per ulteriori informazioni, vedere [Effettuare pagamenti tramite assegno](payables-how-work-checks.md) e [Effettuare pagamenti elettronici](payables-how-export-payments-bank-file.md).  

## <a name="to-make-payments-in-the-payment-journal"></a>Per eseguire i pagamenti nelle registrazioni pagamenti

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.
2. Aprire il batch contabile che verrà dedicato ai pagamenti.
3. Se si conoscono i clienti da pagare o rimborsare, compilare i campi manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per collegare anche il pagamento alla relativa fattura o nota di credito, selezionare il campo **Collega-a nr. doc.** nella pagina **Collega movimenti fornitori**, selezionare la relativa fattura o nota di credito, quindi selezionare il pulsante **OK**.

    Molti campi, ad esempio i campi **Importo documento** e **Data scadenza** vengono compilati con le informazioni tratte dal documento selezionato.
5. In alternativa, utilizzare la funzione **Sugg. pagamenti fornitore**. Tutte le informazioni applicabili e gli importi vengono quindi inseriti anche nelle righe del giornale di registrazione. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).

    I messaggi guideranno la compilazione corretta dei campi richiesti.
6.  Una volta completate tutte le righe di registrazione pagamento, scegliere l'azione **Registra**.

## <a name="see-also"></a>Vedi anche
[Effettuare pagamenti tramite assegno](payables-how-work-checks.md)  
[Effettuare pagamenti elettronici](payables-how-export-payments-bank-file.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
