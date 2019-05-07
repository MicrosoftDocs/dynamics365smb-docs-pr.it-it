---
title: Impostare gli addebiti diretti SEPA | Microsoft Docs
description: Informazioni su come impostare gli addebiti diretti SEPA in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 2ca52a5c1e6f009f0a430e5b35b725c832132c6f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "927034"
---
# <a name="set-up-sepa-direct-debit"></a>Impostare gli addebiti diretti SEPA
Nella pagina **Riscossioni addebiti diretti** è possibile esportare le istruzioni nella banca elettronica per eseguire una riscossione di addebiti diretti dal conto corrente del cliente al conto corrente della banca. [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta il formato di addebito diretto SEPA, ma nel proprio paese potrebbero essere disponibili anche altri formati di pagamento elettronico.  

Per abilitare l'esportazione di formati di file della banca che non sono supportati come predefiniti in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile impostare una definizione di scambio dati utilizzando il framework di scambio dati. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).  

Prima di poter elaborare elettronicamente i pagamenti del cliente esportando le istruzioni di addebito diretto nel formato di addebito diretto SEPA, è necessario effettuare i seguenti passaggi di impostazione:  

* Impostare il formato di esportazione del file della banca che indica di eseguire la riscossione di un addebito diretto dal conto bancario del cliente al proprio.  
* Impostare il metodo di pagamento del cliente.  
* Impostare il mandato di addebito diretto che riflette l'accordo con il cliente per riscuotere i pagamenti in un determinato periodo del contratto.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Per impostare il conto bancario per l'addebito diretto SEPA  
1. Nella casella **Cerca** immettere **C/C bancari**, quindi selezionare il collegamento correlato.  
2. Aprire il conto bancario che si desidera utilizzare per l'addebito diretto.  
3. Nella Scheda dettaglio **Trasferimento**, nel campo **Formato esport. addebito dir. SEPA**, scegliere l'opzione per addebito diretto SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Per impostare il metodo di pagamento del cliente per l'addebito diretto SEPA  
1. Nella casella **Cerca** immettere **Metodi di pagamento**, quindi selezionare il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Impostare un metodo di pagamento. Compilare i campi specifici dell'addebito diretto come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Addebito diretto**|Specificare se il metodo di pagamento riguarda la riscossione di addebiti diretti SEPA.|  
    |**Cod. condizioni pag. addebiti dir.**|Specificare le condizioni di pagamento, ad esempio NON PAGARE, che vengono visualizzate sulle fatture di vendita pagate con addebito diretto SEPA per indicare al cliente che il pagamento verrà riscosso automaticamente. In alternativa, lasciare vuoto il campo.|  

    > [!NOTE]  
    >  Non immettere un valore nel campo **Nr. contropartita**.  

4. Fare clic sul pulsante **OK** per chiudere la pagina **Metodi di pagamento**.  
5. Nella casella **Cerca** immettere **Clienti**, quindi selezionare il collegamento correlato.  
6. Aprire la scheda del cliente che si desidera impostare per la riscossione di addebiti diretti SEPA.  
7. Scegliere il campo **Codice metodo di pagamento**, quindi selezionare il codice del metodo di pagamento specificato nel passaggio 3.  
8. Ripetere i passaggi da 6 a 7 per tutti i clienti che si desidera impostare per la riscossione degli addebiti diretti SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Per impostare il mandato di addebito diretto che rappresenta l'accordo con il cliente  
1. Nella casella **Cerca** immettere **Clienti**, quindi selezionare il collegamento correlato.  
2. Aprire la scheda del cliente che si desidera impostare per l'addebito diretto SEPA.  
3. Scegliere l'azione **C/C bancari**.  
4. Nella pagina **Lista C/C bancari clienti** selezionare il conto bancario cliente che utilizzerà gli addebiti diretti, quindi nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Mandati di addebito diretto**.  
5. Nella pagina **Mandati per addebito diretto SEPA** compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice C/C bancario clienti**|Specifica il conto bancario da cui vengono riscossi i pagamenti in addebito diretto. Questo campo viene compilato automaticamente.|  
    |**Data di inizio validità**|Specificare la data in cui ha inizio il mandato di addebito diretto.|  
    |**Data di fine validità**|Specificare la data in cui termina il mandato di addebito diretto.|  
    |**Data di firma**|Specificare la data in cui il cliente ha firmato il mandato di addebito diretto.|  
    |**Tipo di pagamento**|Specificare se l'accordo riguarda una (**Singola**) o più (**Ricorrente**) riscossioni di addebiti diretti.|  
    |**Numero previsto di debiti**|Specificare il numero di riscossioni di addebiti diretti che si prevede di eseguire. Questo campo è pertinente solo se nel campo **Tipo di pagamento** è stato selezionato **Ricorrente**.|  
    |**Contatore debiti**|Specifica quante riscossioni di addebiti diretti sono state effettuate mediante il mandato di addebito diretto. Questo campo viene aggiornato automaticamente.|  
    |**Bloccato**|Specificare che le riscossioni di addebiti diretti non possono essere eseguite mediante questo mandato di addebito diretto.|  

6.  Ripetere i passaggi da 1 a 5 per tutti i clienti che si desidera impostare per l'addebito diretto SEPA.  

 Il mandato di addebito diretto viene inserito automaticamente nel campo **ID mandato per addebito diretto** quando si crea una fattura di vendita per il cliente selezionato nel passaggio 2. Per altre informazioni, vedere [Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Vedi anche  
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md)
[Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md)
[Scambio di dati in modalità elettronica](across-data-exchange.md)
