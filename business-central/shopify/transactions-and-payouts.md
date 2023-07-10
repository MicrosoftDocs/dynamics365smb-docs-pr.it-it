---
title: Sincronizzare transazioni e pagamenti
description: Configura ed esegui l'importazione di transazioni e pagamenti da Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# <a name="transactions-and-payouts"></a>Transazioni e pagamenti

Quando un cliente completa il pagamento nel negozio online, le informazioni sui pagamenti vengono salvate come **Transazione**. Potrebbero esserci più transazioni collegate all'ordine, ad esempio quando un cliente utilizza una carta regalo per pagare parte del costo e quindi utilizza una carta di credito o PayPal per l'importo rimanente.

Se usi Shopify Payment come fornitore di servizi di pagamento, quindi oltre alle informazioni sul denaro ricevuto dal cliente dal fornitore di servizi di pagamento, puoi anche visualizzare i pagamenti da Shopify sul tuo conto bancario.

## <a name="transactions"></a>Transazioni

Le operazioni di pagamento avvenute in Shopify sono sincronizzate agli ordini e possono essere visualizzate dalla pagina **Ordini Shopify**.

Per rivedere tutte le transazioni, scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Transazioni** e scegli il collegamento correlato.

Il campo **Nr. fatture registrate** può essere utile nel processo di riconciliazione.

Se hai configurato la mappatura del metodo di pagamento il documento di vendita creato verrà assegnato un codice metodo di pagamento. Ulteriori informazioni su [Mappatura del metodo di pagamento](#payment-method-mapping).

## <a name="payouts"></a>Pagamenti

Se nel tuo negozio usi il metodo di pagamento Shopify, riceverai i pagamenti tramite **Pagamenti Shopify** quando un cliente paga utilizzando Shopify Payments e checkout accelerati.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare i pagamenti per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Sincronizza pagamenti**.

Per rivedere tutti i pagamenti, scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Pagamenti** e scegli il collegamento correlato.

I **Pagamenti** sono solo a scopo informativo e non influiscono sulla contabilità generale o sui movimenti contabili bancari, sebbene possano essere utili durante l'elaborazione dell'estratto conto bancario.

## <a name="payment-method-mapping"></a>Mapping metodo di pagamento

Per compilare il **Codice metodo di pagamento** per documenti di vendita importati da Shopify automaticamente, è necessario configurare **Mapping metodo di pagamento**.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri definire un mapping per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Mapping metodo di pagamento**.
4. Nei campi **Gateway** e **Società emittente carte di credito**, immetti il nome del metodo di pagamento da Shopify. Il record viene creato automaticamente quando importi gli ordini Shopify.
5. Immetti il **Codice metodo di pagamento** con il metodo di pagamento corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Imposta la **Priorità** per i casi in cui il cliente utilizza più mezzi di pagamento. Il metodo di pagamento con la priorità più alta viene selezionato nel documento di vendita. Se entrambi i metodi di pagamento hanno la stessa priorità, viene utilizzato il metodo di pagamento con l'importo più alto.

> [!NOTE]  
> Se il metodo di pagamento corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)] ha **Tipo contropartita** e **Nr. contropartita** popolato, durante la registrazione il sistema di fatturazione creerà una voce di bilanciamento del *Pagamento* e applicalo al tipo di *Fattura* nel movimento contabile cliente.

## <a name="use-cases"></a>Utilizzare casi
  
Parti:

* Acquirente: persona che acquista la merce dal negozio online Shopify.
* Venditore: la tua società.
* Provider di servizi di pagamento: società che facilita l'elaborazione dei pagamenti. Può essere Shopify Payments o una terza parte.

### <a name="how-money-flows"></a>Modalità dei flussi di denaro

L'acquirente acquista la merce nel negozio online. L'ultima fase è l'elaborazione del pagamento.

>[!NOTE]
> Questo esempio non copre i casi in cui il pagamento viene completato fuori dal pagamento Shopify, valido per scenari B2B.
  
L'acquirente paga con carta di credito, PayPal o un metodo di pagamento locale come MobilePay in Danimarca. Il provider di servizi di pagamento preleva l'intero importo dall'acquirente. In questo momento il denaro dell'acquirente viene trasferito al provider di servizi di pagamento.

A seconda del provider di servizi di pagamento, il venditore potrebbe vedere questo denaro nel proprio conto presso il provider di servizi di pagamento, sia gli importi ricevuti, sia le commissioni detratte. I provider di servizi di pagamento spesso riscuotono una commissione da ogni transazione e in alcuni casi possono anche avere una commissione fissa.
  
A seconda del provider di servizi di pagamento, il commerciante attiva un trasferimento di denaro sul proprio conto bancario (pagamento) manualmente o automaticamente entro un periodo definito: una volta al giorno, una volta al mese e così via.
  
A seconda della banca, il venditore può vedere questa transazione in entrata sul proprio conto bancario tramite l'online banking o nell'estratto conto.

Ci sono diverse opzioni su come gestire le transazioni di pagamento in [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Opzione 1: riconcilia i trasferimenti in entrata sul conto bancario con le fatture originali
  
Il venditore importa l'ordine di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] e registra la spedizione e la fattura.

Risultato: il sistema crea un **Movimento contabile cliente** di tipo *Fattura* con l'intero importo, l'opzione **Apri** è impostata su Sì. **Importo residuo** è uguale all'importo fatturato.

Il venditore importa l'estratto conto utilizzando la registrazione riconciliazione pagamenti.

Problemi:

1. Può essere difficile se ci sono più fatture (e note di credito), ma un solo pagamento dal provider di servizi di pagamento in un'unica soluzione.
2. L'importo di solito non corrisponde a causa della commissione. Puoi utilizzare la tolleranza di pagamento o/e gli sconti sui pagamenti per gestire le commissioni.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Opzione 2: riconciliare i bonifici in entrata sul conto bancario con il conto provvisorio che rappresenta denaro presso il provider di servizi di pagamento
  
Il venditore importa l'ordine di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] e registra la spedizione e la fattura.
  
Risultato: il sistema crea un movimento contabile cliente di tipo **Fattura** con l'intero importo e l'opzione **Apri** è impostata su Sì. **Importo residuo** è uguale all'importo fatturato.

Tuttavia, poiché l'ordine cliente ha un codice per il metodo di pagamento in cui i campi **Tipo contropartita** e **Nr. contropartita** vengono compilati, il sistema crea automaticamente un altro movimento contabile cliente del tipo **Pagamento** e lo applica al movimento contabile cliente creato in precedenza.

>[!NOTE]
> Il sistema compila il campo Codice metodo di pagamento in base alla mappatura del metodo di pagamento. Ulteriori informazioni su [Mappatura del metodo di pagamento](#payment-method-mapping).
  
È possibile definire i conti di contropartita per i metodi di pagamento in due modi:

* **Tipo contropartita** impostato su *Banca* e **Nr. contropartita** compilare il conto bancario speciale che rappresenta il tuo conto presso il provider di servizi di pagamento.
* **Tipo contropartita** impostato su **Conti C/G** e **Nr. contropartita** compilare il conto C/G che rappresenta il tuo conto presso il provider di servizi di pagamento.

È opportuno utilizzare un conto bancario se il provider di servizi di pagamento esporta una sorta di estratto conto, che è possibile importare nel giornale di registrazione di riconciliazione pagamenti.

Il venditore importa l'estratto conto utilizzando la registrazione riconciliazione pagamenti. Il pagamento in entrata può essere elaborato:

* come bonifico da altra banca. Se il trasferimento richiede alcuni giorni o prevede il cambio di valuta, potresti voler utilizzare un conto C/G provvisorio.
* come differenza sul conto C/G che rappresenta il tuo conto presso il provider di servizi di pagamento.
  
Il saldo residuo sul conto C/G o sul conto bancario che rappresenta il tuo conto presso il provider di servizi di pagamento può essere cancellato come "Oneri/Commissioni"

Problemi:

1. Puoi creare più conti C/G o conti bancari se hai a che fare con più provider di servizi di pagamento. Tuttavia, gli ordini di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] supportano un solo codice del metodo di pagamento, il che rende difficile la gestione dei casi in cui un acquirente utilizza più metodi di pagamento per un ordine.

## <a name="see-also"></a>Vedere anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
