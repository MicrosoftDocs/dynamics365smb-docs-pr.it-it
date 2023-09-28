---
title: Impostare i pagamenti anticipati
description: Scopri come configurare Business Central per usare la funzionalità di pagamento anticipato per fatturare e riscuotere i depositi richiesti dai clienti o di rimettere i depositi ai fornitori.
author: brentholtorf
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: '314, 459, 460, 664'
ms.date: 10/27/2021
ms.author: bholtorf
---
# <a name="set-up-prepayments"></a>Impostare i pagamenti anticipati

Se è necessario che i clienti inviino il pagamento prima della spedizione di un ordine, oppure se il fornitore richiede l'invio del pagamento prima di spedire l'ordine, è possibile utilizzare la funzionalità Pagamento anticipato. La funzionalità di pagamento anticipato consente di fatturare e riscuotere i depositi dai clienti o di rimettere i depositi ai fornitori e di garantire che tutti i pagamenti parziali siano registrati a fronte di una fattura. Per ulteriori informazioni, vedere [Creare fatture di pagamenti anticipati](finance-how-to-create-prepayment-invoices.md).

Prima di registrare le fatture di pagamento anticipato, è necessario impostare i conti di registrazione nella contabilità generale e la numerazione per i documenti di pagamento anticipato. È necessario specificare un account per i pagamenti anticipati relativi alle vendite e un account per i pagamenti anticipati relativi agli acquisti. È possibile specificare gli stessi conti di registrazione da utilizzare per tutti i pagamenti anticipati relativi a tutte le categorie registrazione di attività generali o categorie registrazione di prodotti generici oppure è possibile specificare conti specifici per categorie registrazione specifiche rispettivamente per vendite e acquisti. Ciò dipende dai requisiti dell'azienda per il monitoraggio dei pagamenti anticipati.  

È possibile definire la percentuale dell'importo riga che verrà fatturato per il pagamento anticipato, per un cliente o un fornitore, per tutti gli articoli o per quelli selezionati. Una volta completata l'impostazione, è possibile generare fatture di pagamento anticipato da ordini vendita o da ordini d'acquisto. È possibile utilizzare le percentuali di default per ogni riga di vendita o di acquisto oppure modificare gli importi nella fattura come necessario. È ad esempio possibile specificare un importo totale per l'intero ordine.  

> [!NOTE]
> Si consiglia di non utilizzare una percentuale di pagamento anticipato del 100% nei seguenti casi:
>
> * Se ci si trova in Nord America. A causa del modo in cui vengono calcolate le imposte, una percentuale di pagamento anticipato del 100% può causare problemi con le fatture di pagamento anticipato.
> * In tutte le regioni, se si deduce manualmente uno sconto di pagamento dalla fattura. Una percentuale di pagamento anticipato del 100% non lascerà automaticamente un importo da cui detrarre lo sconto.
>
> Inoltre, quando utilizzi una percentuale di pagamento anticipato del 100%, [!INCLUDE[prod_short](includes/prod_short.md)] potrebbe dover creare movimenti di arrotondamento di compensazione. Quando ciò accade, dovrai scegliere un conto C/G nel campo **Conto arrotondamento fatture** della pagina **Categorie registrazione clienti**. Questo è vero anche se non hai attivato l'interruttore **Arrotondamento fattura** nella pagina **Setup contabilità clienti**. Se non specifichi un conto non potrai registrare le fatture di pagamento anticipato. 

Poiché l'importo pagamento anticipato è di proprietà dell'acquirente fino a quando non riceve le merci o i servizi, è necessario impostare conti di contabilità generale per la gestione degli importi pagamento anticipato fino a quando non viene registrata la fattura finale. I pagamenti anticipati di vendita devono essere registrati in un conto passività fino a quando gli articoli non vengono spediti. I pagamenti anticipati di acquisto devono essere registrati in un conto cespiti fino a quando gli articoli non vengono ricevuti. È inoltre necessario impostare un conto di contabilità generale separato per ogni codice IVA.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Per aggiungere conti pagamento anticipato al setup registrazioni COGE

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup registrazioni COGE**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup registrazioni COGE** compilare i campi seguenti per le righe pertinenti:  

    * **Conto pagam. anticipati vendite**  
    * **Conto pagam. anticipati acquisti**  

> [!TIP]
> Se non è possibile vedere i campi nella pagina **Setup registrazioni COGE**, quindi utilizzare la barra di scorrimento orizzontale nella parte inferiore della pagina per scorrere verso destra.  

Se non sono già stati impostati i conti di contabilità generale per i pagamenti anticipati, è possibile aprire la pagina **Lista conti C/G** dall'elenco di conti pertinente.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Per impostare la numerazione per i documenti pagamento anticipato

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup contabilità clienti**, nella Scheda dettaglio **Numerazioni** compilare i campi seguenti:  

   * **Nr. fatt. pagam. ant. reg.**
   * **Nr. note cr. pagam. ant. reg.**

3. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità fornitori**, quindi scegli il collegamento correlato.
4. Nella pagina **Setup contabilità fornitori**, nella Scheda dettaglio **Numerazioni** compilare i campi seguenti:

    * **Nr. fatt. pagam. ant. reg.**
    * **Nr. note cr. pagam. ant. reg.**

> [!NOTE]  
> È possibile utilizzare la stessa numerazione per le fatture pagamento anticipato e per quelle normali oppure utilizzare numerazioni diverse. In quest'ultimo caso, le numerazioni non devono sovrapporsi perché non ci devono essere numeri presenti in entrambe.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Per impostare le percentuali pagamento anticipato per articoli, clienti e fornitori

Per un articolo è possibile impostare una percentuale pagamento anticipato predefinito per tutti i clienti, per un cliente specifico o per un gruppo prezzi cliente. Se non desideri applicare la stessa percentuale di pagamento anticipato a tutti i clienti, devi specificare a quali clienti o a quali gruppi di prezzi di clienti si applica la percentuale di pagamento anticipato.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Selezionare un articolo, quindi scegliere l'azione **Percentuale pagamento anticipato**.  
3. Nella pagina **Percentuali pagamenti anticipati vendite** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Per un cliente o un fornitore, è possibile impostare una percentuale pagamento anticipato predefinita per tutti gli articoli e tutti i tipi di righe di vendita. Immettere la percentuale nella scheda cliente o nella scheda fornitore. La procedura seguente mostra come specificare una percentuale di pagamento anticipato per un cliente, ma passaggi simili si applicano ai fornitori.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Clienti**, quindi scegli il collegamento correlato.
2. Aprire la scheda per un cliente.
3. Compilare il campo **% pagamento anticipato**.
4. Ripetere i passaggi per altri clienti o fornitori.  

> [!TIP]
> Si può anche accedere alla pagina **Percentuali pagamenti anticipati vendite** dalla scheda cliente o fornitore.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Per determinare l'ordine di priorità delle percentuali pagamento anticipato

Per un ordine potrebbero venire indicate una percentuale pagamento anticipato nella testata di vendita e una percentuale diversa per gli articoli nelle righe. Per determinare la percentuale pagamento anticipato applicata a ogni riga di vendita, viene analizzata la presenza della percentuale pagamento anticipato in base all'ordine descritto di seguito e viene utilizzato il primo valore di default individuato:  

1. Percentuale pagamento anticipato per l'articolo nella riga e il cliente a cui si riferisce l'ordine.  
2. Percentuale pagamento anticipato per l'articolo nella riga e il gruppo prezzi cliente a cui appartiene il cliente.  
3. Percentuale pagamento anticipato per l'articolo nella riga per tutti i clienti.  
4. Percentuale pagamento anticipato nella testata di vendita o di acquisto.  

In altri termini, la percentuale pagamento anticipato indicata nella scheda cliente viene utilizzata solo se per l'articolo non sono state impostate altre percentuali pagamento anticipato. Tuttavia, se si modifica il valore del campo **% pagamento anticipato** nella testata di vendita o di acquisto dopo aver creato le righe, viene aggiornata la percentuale di tutte le righe. In questo modo, è possibile creare in modo semplice un ordine con una percentuale pagamento anticipato fissa, indipendentemente dalla percentuale impostata per gli articoli.

## <a name="to-automatically-release-sales-orders-when-prepayments-are-applied"></a>Per rilasciare automaticamente gli ordini di vendita quando vengono applicati i pagamenti anticipati

È possibile risparmiare tempo impostando un movimento coda processi che rilascerà automaticamente gli ordini di vendita che richiedono il pagamento anticipato dopo l'applicazione dei pagamenti. L'automazione del processo consente di risparmiare la fase di rilascio dell'ordine di vendita.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.
2. Nel campo **Frequenza aggiornamento automatico pagamento anticipato**, specifica la frequenza con cui vuoi eseguire il movimento coda processi.

> [!TIP]
> Mentre sei qui, considera l'aggiunta di una protezione contro la spedizione o la fatturazione di ordini cliente con importi anticipati non pagati. Se attivi l'interruttore **Verifica pagamento anticipato durante la registrazione**, [!INCLUDE[prod_short](includes/prod_short.md)] impedirà alle persone di registrare ordini con importi di pagamento anticipato in sospeso.

3. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti coda processi**, quindi scegli il collegamento correlato.
4. Imposta il movimento coda processi **Aggiornamento pagamento anticipato vendita in sospeso**, ad esempio utilizzando le impostazioni nella scheda dettaglio **Ricorrenza** per pianificare la frequenza con cui vuoi che venga eseguito. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Vedere anche

[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Calcolare imposte Goods and Services Tax su pagamenti anticipati in Australia](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Calcolare imposte Goods and Services Tax su pagamenti anticipati in Nuova Zelanda](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Informazioni sulla contabilità generale e COA](finance-general-ledger.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
