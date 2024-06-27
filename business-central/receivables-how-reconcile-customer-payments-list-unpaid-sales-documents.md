---
title: Collegare i pagamenti a documenti di vendita non pagati
description: 'Si collegano gli importi pagati dai clienti ai relativi documenti di vendita e si registra il pagamento per aggiornare i movimenti contabili cliente, contabilità generale e i movimenti contabili bancari.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Riconciliare i pagamenti dei clienti dall'elenco dei documenti di vendita non pagati

Dopo che i clienti hanno effettuato pagamenti elettronici sul tuo conto bancario, devi intraprendere le seguenti azioni:

* Collegare ogni importo pagato al documento di vendita correlato.
* Registrare il pagamento per aggiornare i movimenti del cliente, della contabilità generale e della contabilità bancaria.

In base alle esigenze aziendali, è possibile registrare i pagamenti manualmente, in modo automatico e tramite i servizi di pagamento.  

> [!NOTE]  
> È possibile eseguire le stesse attività, inclusi i pagamenti dei fornitori, nella pagina **Registrazione riconciliazione pagamenti**. Ad esempio, è possibile importare estratti conto, utilizzare l'applicazione automatica e riconciliare i conti correnti bancari. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

Utilizza la pagina **Registra pagamenti clienti** per bilanciare i conti interni utilizzando le cifre di cassa effettive per garantire che i pagamenti vengano raccolti. Puoi verificare e registrare rapidamente pagamenti singoli o forfettari, elaborare pagamenti scontati e trovare i documenti non pagati.

I pagamenti per differenti clienti, con date di pagamento diverse, devono essere registrati come pagamenti singoli. I pagamenti per lo stesso cliente, con uguale data di pagamento, possono essere registrati come pagamento forfettario. I pagamenti forfettari sono utili, ad esempio, quando un cliente ha effettuato un pagamento singolo che copre più fatture di vendita.

## Per impostare le registrazioni pagamenti

Poiché è possibile registrare tipi diversi di pagamento in conti di contropartita diversi, è necessario selezionare un conto di contropartita nella pagina **Setup registrazione pagamenti** prima di iniziare l'elaborazione dei pagamenti clienti. Se si esegue la registrazione sempre alla stessa contropartita, è possibile impostare tale conto come predefinito ed evitare ogni volta di aprire la pagina **Registra pagamenti clienti**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazione pagamenti**, quindi scegli il collegamento correlato. Puoi anche andare nella pagina **Registra pagamenti clienti** e scegliere l'azione **Setup**.
2. Compilare i campi della pagina **Setup registrazione pagamenti**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> Per semplificare l'identificazione successiva dei movimenti che sono stati registrati tramite il giornale di registrazione, è possibile assegnare una numerazione specifica alla registrazione pagamenti. La serie numerica è utile se si utilizzano registrazioni riconciliazione pagamenti per registrare e collegare i pagamenti.

## Per registrare i pagamenti del cliente singolarmente

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.  

    Nella pagina **Registra pagamenti clienti** vengono visualizzati tutti i documenti registrati per cui un pagamento può essere registrato. La pagina può anche essere aperta dalle pagine **Clienti** e **Scheda cliente** dove viene automaticamente filtrata per il cliente specificato.  
2. Selezionare la casella di controllo **Pagamento effettuato** nella riga che rappresenta il documento registrato per cui è stato eseguito un pagamento.
3. Nel campo **Data ricezione** immettere la data di esecuzione del pagamento. Questa data potrebbe essere diversa dalla data del lavoro.  

   Se la casella di controllo **Compila automaticamente data di ricezione** nella pagina **Setup registrazione pagamenti** è selezionata, il campo **Data ricezione** include la data del lavoro.  
4. Nel campo **Importo ricevuto** immettere l'importo pagato.

    Per i pagamenti completi, questo importo è uguale a quello nel campo **Importo residuo** della riga. Per i pagamenti parziali, questo importo è minore di quello nel campo **Importo residuo** della riga.
5. Ripetere i passaggi da 2 a 4 per le altre righe per i documenti registrati per i quali vengono eseguiti i pagamenti.  
6. Scegliere l'azione **Registra pagamenti**.  

Le informazioni sui pagamenti vengono registrate per i documenti nelle righe in cui è selezionata la casella di controllo **Pagamento effettuato**. I movimenti dei pagamenti vengono registrati nei conti di contabilità generale, nei conti bancari e nei conti clienti.

## Per riconciliare i pagamenti forfettari

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.
2. Selezionare la casella di controllo **Pagamento effettuato** nelle righe per i documenti registrati per lo stesso cliente o fornitore per cui è stato eseguito un pagamento forfettario.  

    > [!NOTE]  
    > Il cliente nel campo **Nome** deve essere lo stesso in tutte le righe da includere nel pagamento forfettario.  

    Se la casella di controllo **Compila automaticamente data di ricezione** nella pagina **Setup registrazione pagamenti** è selezionata, il campo **Data ricezione** include la data del lavoro.  
3. Nel campo **Data ricezione** immettere la data di esecuzione del pagamento. Questa data potrebbe essere diversa dalla data del lavoro.  

    > [!NOTE]  
    > Questa data deve essere uguale in tutte le righe che verranno registrate come pagamento forfettario.  
4. Nel campo **Importo ricevuto** immettere gli importi su più righe che riassumono l'importo del pagamento forfettario.  

    > [!TIP]  
    > Provare a registrare quanti più pagamenti completi è possibile con l'importo forfettario. Immettere gli importi che sono gli stessi presenti nel campo **Importo residuo** nel maggior numero di righe possibili.  
5. Ripetere i passaggi da 2 a 4 per altre righe che rappresentano i documenti registrati per lo stesso cliente per cui è stato eseguito un pagamento forfettario.  
6. Scegliere l'azione **Registra come pagamento forfettario**.

   Le informazioni sui pagamenti vengono registrate per i documenti nelle righe in cui è selezionata la casella di controllo **Pagamento effettuato**. I movimenti dei pagamenti vengono registrati nei conti di contabilità generale, nei conti bancari e nei conti clienti. Ogni pagamento viene collegato al documento di vendita registrato correlato.  

Se un pagamento della banca non è rappresentato da una riga nella pagina **Registra pagamenti cliente**, è possibile che il documento correlato non sia stato registrato. In questo caso, è possibile utilizzare una funzione di ricerca per trovare rapidamente il documento e registrarlo per elaborare il pagamento. Per ulteriori informazioni, vedi [Per trovare un documento di vendita specifico non completamente fatturato](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Se un pagamento della banca non è rappresentato da alcun documento, puoi aprire una registrazione COGE precompilata nella pagina **Registra pagamenti cliente** per registrare il pagamento direttamente nel conto di contropartita senza collegarlo a un documento. In alternativa, potresti registrare il pagamento nella registrazione fino a quando non viene chiarita l'origine del pagamento. Per ulteriori informazioni, vedere [Per registrare un pagamento senza un documento correlato](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## Per elaborare manualmente i pagamenti clienti con sconti

Se è stato pattuito uno sconto nei pagamenti con il cliente, gli importi del pagamento possono essere inferiori rispetto agli importi della fattura se il pagamento viene eseguito prima della data dello sconto stabilita.  

Nella seguenti procedure vengono illustrati i modi in cui registrare i pagamenti scontati nella pagina **Registrazione pagamenti**.  

* L'importo di pagamento è uguale all'importo residuo scontato e la data di pagamento è antecedente alla data di sconto. Il pagamento viene registrato così come è.  
* L'importo di pagamento è uguale all'importo residuo scontato ma la data di pagamento è successiva alla data di sconto. Il pagamento viene registrato come parziale. Il documento rimane aperto per raccogliere/pagare l'importo residuo. Puoi anche impostare una data di sconto successiva per consentire il pagamento completo.  
* L'importo di pagamento è inferiore all'importo scontato residuo. Il pagamento viene registrato come parziale. Il documento rimane aperto per raccogliere/pagare l'importo residuo.  
* L'importo di pagamento è superiore all'importo scontato residuo. I pagamenti vengono registrati così come sono. Solo l'importo residuo viene registrato. L'importo extra viene accreditato al cliente.  

### Per elaborare un importo di pagamento uguale all'importo scontato e dove si trova la data di pagamento prima della data di sconto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è uguale a quello riportato nel campo **Importo residuo incluso sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga zero (0).  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento completo nei conti di contabilità generale, bancario e cliente.

### Per elaborare un importo di pagamento uguale all'importo scontato ma dove si trova la data di pagamento dopo la data di sconto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è uguale a quello riportato nel campo **Importo residuo incluso sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.
3. Nel campo **Data ricezione** immettere la data di pagamento che è posteriore alla data indicata nel campo **Data sconto pagamento**.

   Il carattere dei campi dati diventano rossi e un messaggio di errore viene visualizzato nella parte inferiore della pagina. I prossimi due passaggi risolvono il problema.
4. Scegliere l'azione **Dettagli**.  
5. Nella pagina **Dettagli registrazione pagamenti**, nel campo **Data sconto pagamento** della Scheda dettaglio **Sconto pagamento**, immettere una data che sia posteriore alla data indicata nel campo **Data ricezione** della pagina **Registrazione pagamenti**.  

    Il messaggio di errore e il carattere rosso scompaiono ed è possibile continuare a elaborare il pagamento scontato.
6. Verificare che il campo **Importo residuo** contenga l'importo residuo per pagare l'importo fattura completo.  
7. Scegliere l'azione **Registra pagamenti** per registrare il pagamento parziale nei conti di contabilità generale, bancario e cliente.  

Il documento correlato rimane aperto.

### Per elaborare un pagamento inferiore all'importo scontato residuo

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è inferiore a quello riportato nel campo **Importo residuo incluso sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.  
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga l'importo residuo per pagare l'importo scontato.  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento parziale nei conti di contabilità generale, bancario e cliente.  

Il documento correlato rimane aperto.

### Per elaborare un pagamento superiore all'importo scontato residuo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è superiore a quello riportato nel campo **Importo residuo incluso sconto**.  

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga zero (0).  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento completo nei conti di contabilità generale, bancario e cliente.  

Il documento correlato è chiuso e al cliente viene accreditato l'importo di pagamento in eccesso.  

## Per trovare un documento di vendita specifico non completamente fatturato

La pagina **Registra pagamenti cliente** fornisce supporto in attività necessarie per le contropartite interne con le cifre effettive di cassa per garantire la raccolta dai clienti. Mostra i pagamenti in entrata inevasi come righe che rappresentano i documenti di vendita in cui è dovuto il pagamento di un importo.  

In genere, quando viene effettuato un pagamento, registrato in banca o in altro modo, il documento di vendita o di acquisto viene rappresentato come una riga nella pagina **Registra pagamenti cliente**. Il documento è in attesa della registrazione del pagamento per l'importo dovuto. Talvolta un pagamento effettuato non è tuttavia rappresentato da una riga nella pagina **Registra pagamenti cliente**, in genere perché il documento non è stato fatturato completamente.

Usa l'azione **Ricerca documenti** per cercare i documenti che non sono fatturati completamente. È possibile eseguire la ricerca in base a uno dei seguenti criteri:  

* Numero documento  
* Importo o intervallo di importi  

Nella procedura seguente viene illustrato come trovare un documento specifico utilizzando entrambi i criteri di ricerca.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.
2. Con il puntatore su una riga qualsiasi, scegliere l'azione **Cerca documenti**.
3. Nella pagina **Ricerca documenti** immettere un valore di ricerca nel campo **Nr. documento**.  

    > [!NOTE]  
    > Il valore immesso in questo campo è contenuta in caratteri jolly nascosti. Ciò significa che l'azione ricerca tutti i numeri dei documenti contenenti il valore immesso.
4. Nel campo **Importo** immettere l'importo specifico nel documento che si desidera trovare.  
5. Nel campo **% tolleranza importo** immettere una percentuale per definire l'intervallo degli importi che si desidera cercare per trovare il documento aperto.  

    Se inserisci 10, l'azione cerca gli importi in un intervallo compreso tra più o meno il 10% del valore nel campo **Importo**.
6. Scegliere l'azione **Cerca**.  

Se uno o più documenti corrispondono ai criteri di ricerca, viene aperta la pagina **Risultato ricerca documenti** nella quale sono visualizzate le righe che rappresentano tali documenti. Ogni riga contiene un numero di documento, una descrizione e un importo.

Se un pagamento della banca non è rappresentato da alcun documento, puoi aprire una registrazione COGE precompilata nella pagina **Registra pagamenti cliente** per registrare il pagamento direttamente nel conto di contropartita senza collegarlo a un documento. In alternativa, potresti registrare il pagamento nella registrazione fino a quando non viene chiarita l'origine del pagamento.  

## Per registrare un pagamento senza un documento correlato

Se un pagamento in banca non è rappresentato da un documento, è possibile utilizzare l'azione **Registrazione COGE** per aprire una riga di registrazione COGE precompilata dalla pagina **Registra pagamenti cliente**. Utilizza la registrazione per registrare il pagamento direttamente nel conto di contropartita senza collegare il pagamento a un documento. In alternativa, potresti registrare il pagamento nella registrazione fino a quando non viene chiarita l'origine del pagamento.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Contabilità generale**.  

    Verrà visualizzata la pagina **Contabilità generale** con una riga contenente il conto di contropartita del batch registrazioni impostato nella pagina **Setup registrazione pagamenti**.  
3. Compila i restanti campi della riga di registrazione. Ad esempio, fornisci l'importo, il numero del cliente o le informazioni dall'estratto conto. Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).  

Puoi registrare la riga di registrazione per aggiornare il totale nel conto di contropartita. Puoi anche non registrare la riga di registrazione e magari aggiungere una nota indicante che per il pagamento è necessaria un'analisi più accurata.  

Se non si registra la riga di registrazione, il relativo valore viene aggiunto al valore nel campo **Importo residuo incluso sconto** nella pagina **Registrazione pagamenti**.  

## Vedere anche

[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]