---
title: Addebito diretto SEPA in Business Central | Microsoft Docs
description: "È possibile riscuotere i pagamenti direttamente dal conto bancario del cliente secondo il formato SEPA."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 557d6411540cc778a8f6810e747d4113fccd8f4c
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Riscuotere pagamenti con addebito diretto SEPA
Con il consenso del cliente, è possibile riscuotere i pagamenti direttamente dal conto bancario del cliente in conformità al formato SEPA.  

 Innanzitutto, impostare il formato di esportazione del file della banca che indica di eseguire un addebito diretto. A questo punto, impostare il metodo di pagamento del cliente. Infine, impostare il mandato di addebito diretto che riflette l'accordo con il cliente per riscuotere i pagamenti in un determinato periodo del contratto.  

 Per indicare alla banca di trasferire l'importo del pagamento dal conto bancario del cliente al conto della propria società, è possibile creare un movimento riscossione di addebiti diretti, contenente informazioni sui conti bancari, sulle fatture di vendita interessate e sul mandato di addebito diretto. È quindi possibile esportare un file XML basato sul movimento riscossione inviato alla banca per l'elaborazione. I pagamenti che non sono stati elaborati verranno comunicati dalla banca, pertanto sarà necessario rifiutare manualmente i movimenti riscossione addebiti diretti in questione.  

 È possibile impostare codici di vendita cliente standard con le informazioni sul mandato e sul metodo di pagamento in addebito diretto. È quindi possibile utilizzare il processo batch **Crea fatture pers. standard** per generare più fatture di vendita con le informazioni di addebito diretto precompilate. Questa operazione può essere eseguita manualmente o automaticamente, in base alla data di scadenza del pagamento.  

 Quando i pagamenti vengono elaborati correttamente, come comunicato dalla banca, è possibile registrare le ricevute dei pagamenti direttamente dalla finestra **Movimenti riscossioni addebiti diretti** o spostando le righe dei pagamenti nel giornale di registrazione in cui si registrano le ricevute di pagamento, ad esempio la finestra **Registrazioni incassi**. In alternativa, a seconda del processo di gestione di cassa, è possibile attendere e collegare i pagamenti solo come parte della riconciliazione bancaria.  

> [!NOTE]  
>  Per raccogliere i pagamenti tramite l'Addebito diretto SEPA, la valuta nella fattura di vendita deve essere EURO.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Preparare i formati dei conti bancari, i metodi di pagamento e gli accordi con i clienti per l'addebito diretto SEPA.|[Impostare gli addebiti diretti SEPA](finance-how-to-set-up-sepa-direct-debit.md)|  
|Indicare alla propria banca di trasferire gli importi dei pagamenti dai conti bancari dei clienti a quello della propria società in base al setup dell'addebito diretto SEPA.|[Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Impostare codici di vendita cliente standard per le fatture ad addebito diretto e generare fatture di vendita con informazioni sull'addebito diretto quando le fatture sono in scadenza.|[Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md)|  
|Registrare i pagamenti effettuati come addebiti diretti SEPA.|[Registrare ricevute di pagamento di addebiti diretti SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Vedi anche  
[Gestione della contabilità clienti](receivables-manage-receivables.md)

