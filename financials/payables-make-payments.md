---
title: Panoramica dei task di gestione dei pagamenti ai fornitori| Documenti Microsoft
description: Descrive i task per gestire i pagamenti ai fornitori o ai creditori, inclusa la registrazione delle righe di pagamento e la visualizzazione di una panoramica del saldo dovuto.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00792adb8b4c7deccee262982cd532423884c8f5
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="making-payments"></a>Effettuare i pagamenti
Quando si eseguono i pagamenti ai fornitori o i rimborsi ai dipendenti, si registrano le relative righe di pagamento nella finestra **Registrazioni pagamenti**. Per individuare i pagamenti fornitore in scadenza, è possibile utilizzare la funzione **Sugg. pagamenti fornitore**. È inoltre possibile utilizzare il report **Fornitori - Scadenziario riepilogativo** per avere una panoramica dei pagamenti fornitore in scadenza.

Dalle registrazioni pagamenti è possibile stampare assegni automatici o registrare l'emissione degli assegni. Se si seleziona **Assegno automatico** nel campo **Tipo pagamento banca**, tutte le righe che rappresentano assegni devono essere stampate prima che le registrazioni pagamenti possano essere contabilizzate.

Quando si registrano i pagamenti, è possibile esportarli in un file della banca da caricare nella banca per l'elaborazione.

Una volta effettuati i pagamenti presso la banca, è necessario collegarli ai relativi movimenti contabili fornitori o dipendenti aperti. Questa operazione può essere eseguita manualmente o importando un file del rendiconto bancario e collegando i pagamenti automaticamente. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e Riconciliazione dei conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| A | Vedere |
| --- | --- |
|Utilizzare la finestra **Registrazioni pagamenti**, su cui si basano le registrazioni COGE, per registrare i pagamenti ai fornitori o ai dipendenti.|[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)|
| Utilizzare una funzione per suggerire i pagamenti fornitore in base ai criteri selezionati, ad esempio la data di scadenza, l'idoneità allo sconto e la liquidità. |[Procedura: Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md) |
|Rimborsare ai dipendenti le spese personali durante le attività aziendali effettuando i pagamenti sul conto corrente bancario.|[Procedura: Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md)|
| Emettere assegni per i pagamenti fornitore, come stampati o come assegni automatici. Annullare gli assegni prima o dopo la registrazione. |[Procedura: Utilizzo degli assegni](payables-how-work-checks.md) |
| Pagare il fornitore in contanti o con assegno e registrare il pagamento mentre si registra la fattura. |[Procedura: Saldare immediatamente le fatture di acquisto](finance-how-to-settle-purchase-invoices-promptly.md) |
| Assicurarsi che la banca compensi solo gli assegni e gli importi convalidati inviandole un file che contenga informazioni sul fornitore, l'assegno e il pagamento. |[Procedura: Esportare un file Positive Pay](finance-how-positive-pay.md) |
|Esportare i pagamenti dalla finestra **Registrazioni pagamenti** a un file della banca che viene caricato nella banca per l'elaborazione, incluso l'EFT (trasferimento elettronico di fondi) nell'America del Nord. |[Procedura: Esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

