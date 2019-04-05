---
title: Impostare i pagamenti anticipati | Microsoft Docs
description: I pagamenti anticipati sono pagamenti che vengono fatturati e registrati in un ordine di pagamento anticipato di vendita o di acquisto prima della fatturazione finale. Potrebbe essere necessario richiedere un deposito prima di iniziare la produzione di articoli su ordine oppure richiedere il pagamento prima della spedizione degli articoli a un cliente. La funzionalità di pagamento anticipato consente di fatturare e riscuotere i depositi richiesti dai clienti o di rimettere i depositi ai fornitori. In questo modo è possibile assicurarsi che tutti i pagamenti siano registrati a fronte di una fattura.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: prepayment
ms.date: 12/04/2018
ms.author: edupont
ms.openlocfilehash: 3038fc256ec45b8eb51abe3f71b7fcc7d273b353
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801605"
---
# <a name="set-up-prepayments"></a>Impostare i pagamenti anticipati
Se è necessario che i clienti inviino il pagamento prima della spedizione di un ordine, oppure se il fornitore richiede l'invio del pagamento prima di spedire l'ordine, è possibile utilizzare la funzionalità Pagamento anticipato. La funzionalità consente di fatturare e riscuotere i depositi dai clienti o di rimettere i depositi ai fornitori e di garantire che tutti i pagamenti parziali siano registrati a fronte di una fattura. Per ulteriori informazioni, vedere [Creare fatture di pagamenti anticipati](finance-how-to-create-prepayment-invoices.md).

Prima di registrare le fatture di pagamento anticipato, è necessario impostare i conti di registrazione nella contabilità generale e la numerazione per i documenti di pagamento anticipato.  

È possibile definire la percentuale dell'importo riga che verrà fatturato per il pagamento anticipato, per un cliente o un fornitore, per tutti gli articoli o per quelli selezionati. Una volta completata l'impostazione, è possibile generare fatture di pagamento anticipato da ordini vendita o da ordini d'acquisto. È possibile utilizzare le percentuali di default per ogni riga di vendita o di acquisto oppure modificare gli importi nella fattura come necessario. È ad esempio possibile specificare un importo totale per l'intero ordine.  

Poiché l'importo pagamento anticipato è di proprietà dell'acquirente fino a quando non riceve le merci o i servizi, è necessario impostare conti di contabilità generale per la gestione degli importi pagamento anticipato fino a quando non viene registrata la fattura finale. I pagamenti anticipati di vendita devono essere registrati in un conto passività fino a quando gli articoli non vengono spediti. I pagamenti anticipati di acquisto devono essere registrati in un conto cespiti fino a quando gli articoli non vengono ricevuti. È inoltre necessario impostare un conto di contabilità generale separato per ogni codice IVA.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Per aggiungere conti pagamento anticipato al setup registrazioni COGE  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup registrazioni COGE** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup registrazioni COGE** compilare i campi seguenti:  

    - **Conto pagam. anticipati vendite**  
    - **Conto pagam. anticipati acquisti**  

Se non sono già stati impostati i conti di contabilità generale per i pagamenti anticipati, è possibile farlo nella pagina **Lista conti C/G**.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Per impostare la numerazione per i documenti pagamento anticipato  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità clienti e vendite** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup contabilità clienti e vendite** compilare i seguenti campi:  

   - **Nr. fatt. pagam. ant. reg.**
   - **Nr. note cr. pagam. ant. reg.**

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità fornitori e acquisti** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup contabilità fornitori e acquisti** compilare i campi seguenti:

    - **Nr. fatt. pagam. ant. reg.**
    - **Nr. note cr. pagam. ant. reg.**

> [!NOTE]  
>  È possibile utilizzare la stessa numerazione per le fatture pagamento anticipato e per quelle normali oppure utilizzare numerazioni diverse. In quest'ultimo caso, le numerazioni non devono sovrapporsi perché non ci devono essere numeri presenti in entrambe.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Per impostare le percentuali pagamento anticipato per articoli, clienti e fornitori  
Per un articolo è possibile impostare una percentuale pagamento anticipato predefinito per tutti i clienti, per un cliente specifico o per un gruppo prezzi cliente.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Selezionare un articolo, quindi scegliere l'azione **Percentuale pagamento anticipato**.  
3. Nella pagina **Percentuali pagamenti anticipati vendite** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Per un cliente o un fornitore, è possibile impostare una percentuale pagamento anticipato predefinita per tutti gli articoli e tutti i tipi di righe di vendita. Immettere la percentuale nella scheda cliente o nella scheda fornitore.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda per un cliente.
3. Compilare il campo **% pagamento anticipato**.
4. Ripetere i passaggi per altri clienti o fornitori.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Per determinare l'ordine di priorità delle percentuali pagamento anticipato  
Per un ordine potrebbero venire indicate una percentuale pagamento anticipato nella testata di vendita e una percentuale diversa per gli articoli nelle righe. Per determinare la percentuale pagamento anticipato applicata a ogni riga di vendita, viene analizzata la presenza della percentuale pagamento anticipato in base all'ordine descritto di seguito e viene utilizzato il primo valore di default individuato:  
1. Percentuale pagamento anticipato per l'articolo nella riga e il cliente a cui si riferisce l'ordine.  
2. Percentuale pagamento anticipato per l'articolo nella riga e il gruppo prezzi cliente a cui appartiene il cliente.  
3. Percentuale pagamento anticipato per l'articolo nella riga per tutti i clienti.  
4. Percentuale pagamento anticipato nella testata di vendita o di acquisto.  

In altri termini, la percentuale pagamento anticipato indicata nella scheda cliente viene utilizzata solo se per l'articolo non sono state impostate altre percentuali pagamento anticipato. Tuttavia, se si modifica il valore del campo **% pagamento anticipato** nella testata di vendita o di acquisto dopo aver creato le righe, viene aggiornata la percentuale di tutte le righe. In questo modo, è possibile creare in modo semplice un ordine con una percentuale pagamento anticipato fissa, indipendentemente dalla percentuale impostata per gli articoli.

## <a name="see-also"></a>Vedi anche  

[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Calcolare imposte Goods and Services Tax su pagamenti anticipati in Australia](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Calcolare imposte Goods and Services Tax su pagamenti anticipati in Nuova Zelanda](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Informazioni sulla contabilità generale e COA](finance-general-ledger.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
