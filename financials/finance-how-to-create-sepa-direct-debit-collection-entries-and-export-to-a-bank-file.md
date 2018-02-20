---
title: Riscossione addebiti diretti SEPA | Microsoft Docs
description: Creare una riscossione addebiti diretti ed esportarla in un file XML che si invia o si carica nella banca elettronica per l'elaborazione.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct-debit, collection, payment, sepa
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 40e4a90329fc7fc7241b570fd641a0d83b06842e
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca
Per indicare alla banca di trasferire l'importo del pagamento dal conto bancario del cliente al conto della propria società, è possibile creare un movimento riscossione di addebiti diretti, contenente informazioni sul conto bancario del cliente, sulle fatture di vendita interessate e sul mandato di addebito diretto. Dal movimento riscossione addebiti diretti risultante, è possibile esportare un file XML da inviare o caricare sul sito elettronico della banca per l'elaborazione. I pagamenti che non sono stati elaborati dalla banca verranno comunicati dalla banca stessa, pertanto sarà necessario rifiutare manualmente i movimenti riscossione addebiti diretti in questione.  

> [!NOTE]  
>  Per raccogliere i pagamenti tramite l'Addebito diretto SEPA, la valuta nella fattura di vendita deve essere EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Per creare una riscossione di addebiti diretti  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Riscossioni addebiti diretti**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Riscossioni addebiti diretti**, nel gruppo **Nuovo** della scheda **Pagina iniziale**, selezionare **Crea riscossione di addebiti diretti**.  
3. Nella finestra **Crea riscossione di addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Da data scadenza**|Specificare la data di scadenza del pagamento più vicina sulle fatture di vendita per cui si desidera creare una riscossione di addebiti diretti.|  
    |**A data scadenza**|Specificare la data di scadenza del pagamento più lontana sulle fatture di vendita per cui si desidera creare una riscossione di addebiti diretti.|  
    |**Tipo di partner**|Specificare se la riscossione di addebiti diretti viene eseguita per clienti di tipo **Società** o **Persona fisica**.|  
    |**Solo clienti con mandato valido**|Specificare se viene creata una riscossione di addebiti diretti per i clienti che dispongono di un mandato di addebito diretto valido. **Nota:** viene creata una riscossione addebiti diretti anche se il campo **ID mandato per addebito diretto** non viene compilato nella fattura di vendita.|  
    |**Solo fatture con mandato valido**|Specificare se una riscossione addebiti diretti viene creata per le fatture di vendita solo se un mandato di addebito diretto valido è selezionato nel campo **ID mandato per addebito diretto** nella fattura di vendita.|  
    |**Nr. conto bancario**|Specificare in quale conto bancario della società verrà trasferito il pagamento riscosso dal conto bancario del cliente.|  
    |**Nome conto corrente**|Specifica il nome del conto bancario selezionato nel campo **Nr. conto corrente**. Questo campo viene compilato automaticamente.|  

4. Scegliere il pulsante **OK**.  

     Alla finestra **Riscossioni addebiti diretti** viene aggiunta una riscossione addebiti diretti e vengono creati uno o più movimenti di riscossione addebiti diretti.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Per esportare un movimento riscossione di addebiti diretti in un file della banca  
1. Nella finestra **Riscossioni addebiti diretti**, nel gruppo **Processo** della scheda **Pagina iniziale**, selezionare **Movimenti riscossioni addebiti diretti**.  
2. Nella finestra **Movimenti riscossioni addebiti diretti** selezionare il movimento che si desidera esportare, quindi nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Crea file addebiti diretti**.  
3. Salvare il file di esportazione nel percorso da cui verrà inviato o caricato sul sito elettronico della banca.  

     Nella finestra **Movimenti riscossioni addebiti diretti** il campo **Stato riscossione di addebiti diretti** viene impostato su File creato. Nella finestra **Mandati per addebito diretto SEPA** il campo **Contatore debiti** viene aggiornato con un conteggio.  

Se il file esportato non può essere elaborato, ad esempio perché il cliente è insolvente, è possibile rifiutare il movimento riscossione addebiti diretti. Se il file esportato viene elaborato correttamente dalla banca, i pagamenti in scadenza relativi alle fatture di vendita interessate vengono automaticamente riscossi dai clienti interessati. In questo caso è possibile chiudere la riscossione.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Per rifiutare un movimento riscossione di addebiti diretti  
* Nella finestra **Movimenti riscossioni addebiti diretti** selezionare il movimento che non è stato elaborato, quindi nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Rifiuta movimento**.  

     Il valore nel campo **Stato** della finestra **Movimenti riscossioni addebiti diretti** viene modificato in **Rifiutato**.  

### <a name="to-close-a-direct-debit-collection"></a>Per chiudere una riscossione di addebiti diretti  
* Nella finestra **Movimenti riscossioni addebiti diretti** selezionare il movimento che è stato elaborato, quindi nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Chiudi riscossione**.  

     La riscossione di addebiti diretti correlata è chiusa.  

È ora possibile registrare le ricevute dei pagamenti per le fatture di vendita interessate. È possibile eseguire questa operazione come si registrano le ricevute dei pagamenti, ad esempio nella finestra **Registrazione pagamenti**, oppure è possibile registrare le ricevute dei pagamenti correlate direttamente nella finestra **Movimenti riscossioni addebiti diretti**. Per ulteriori informazioni, vedere [Registrare ricevute di pagamento di addebiti diretti SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Vedi anche  
[Impostare gli addebiti diretti SEPA](finance-how-to-set-up-sepa-direct-debit.md)   
[Registrare ricevute di pagamento di addebiti diretti SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md)   
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)   

