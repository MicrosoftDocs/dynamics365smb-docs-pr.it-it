---
title: 'Procedura: Riconciliare i pagamenti dei clienti manualmente dall&quot;elenco dei documenti di vendita non pagati | Documenti Microsoft'
description: 'Procedura: Riconciliare i pagamenti dei clienti manualmente dall&quot;elenco dei documenti di vendita non pagati'
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c60b4fd5ef58740e4ac518a2538873353554fd87
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-customer-payments-manually-from-a-list-of-unpaid-sales-documents"></a>Procedura: Riconciliare i pagamenti dei clienti manualmente dall'elenco dei documenti di vendita non pagati
Quando i clienti hanno effettuato i pagamenti sul conto corrente elettronico, è necessario collegare ogni importo pagato al documento di vendita corrispondente e registrare il pagamento per aggiornare i movimenti cliente, bancari e di contabilità generale.

**Nota**: è possibile effettuare le stesse attività, inclusi i pagamenti fornitori, nella finestra **Registrazioni riconciliazione pagamenti** utilizzando le funzioni per l'importazione del rendiconto bancario, il collegamento automatico e la riconciliazione bancaria. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

La finestra **Registrazione pagamenti** è progettata per assistere l'utente nell'esecuzione di attività in contropartite interne utilizzando le cifre effettive di cassa per garantire una riscossione efficiente dei pagamenti dai clienti. Questo strumento di elaborazione dei pagamenti consente di verificare rapidamente e registrare i pagamenti singoli o forfettari, elaborare i pagamenti scontati e individuare documenti non pagati specifici per i quali viene eseguito il pagamento.

I pagamenti per clienti diversi, con date di pagamento diverse, devono essere registrati come pagamenti singoli. I pagamenti per lo stesso cliente, con uguale data di pagamento, possono essere registrati come pagamento forfettario. Ciò risulta utile, ad esempio, quando un cliente ha effettuato un pagamento singolo che copre più fatture di vendita.

## <a name="to-set-up-the-payment-registration-journal"></a>Per impostare le registrazioni pagamenti
Poiché è possibile registrare tipi diversi di pagamento in conti di contropartita diversi, è necessario selezionare un conto di contropartita nella finestra **Setup registrazione pagamenti** prima di iniziare l'elaborazione dei pagamenti clienti. Se si esegue la registrazione sempre alla stessa contropartita, è possibile impostare tale conto come predefinito ed evitare ogni volta di aprire la finestra **Registrazione pagamenti**.  

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Setup registrazione pagamenti**, quindi scegliere il collegamento correlato.

    In alternativa, nella finestra **Registrazione pagamenti** scegliere l'azione **Setup**.    
2. Compilare i campi della finestra **Setup registrazione pagamenti**. Selezionare il campo per visualizzare una breve descrizione del campo o il collegamento alle informazioni correlate.  

## <a name="to-reconcile-payments-individually"></a>Per riconciliare i pagamenti individualmente
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.  
2. Selezionare la casella di controllo **Pagamento effettuato** nella riga che rappresenta il documento registrato per cui è stato eseguito un pagamento.

    Se la casella di controllo **Compila automaticamente data di ricezione** nella finestra **Setup registrazione pagamenti** è selezionata, la data di lavorazione viene immessa nel campo **Data ricezione**.  
3. Nel campo **Data ricezione** immettere la data di esecuzione del pagamento. La data può essere diversa dalla data di lavoro.  
4. Nel campo **Importo ricevuto** immettere l'importo pagato.

    Per i pagamenti completi, questo importo è uguale a quello nel campo **Importo residuo** della riga. Per i pagamenti parziali, questo importo è minore di quello nel campo **Importo residuo** della riga.    
5. Ripetere i passaggi da 2 a 4 per le altre righe che rappresentano i documenti registrati per i quali vengono eseguiti i pagamenti.  
6. Scegliere l'azione **Registra pagamenti**.  

Le informazioni sui pagamenti vengono registrate per i documenti rappresentati dalle righe in cui è selezionata la casella di controllo **Pagamento effettuato**.  

I movimenti dei pagamenti vengono registrati nei conti di contabilità generale, nei conti bancari e nei conti clienti. Ogni pagamento viene collegato al documento di vendita registrato correlato.  

## <a name="to-reconcile-lump-payments"></a>Per riconciliare i pagamenti forfettari
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.
2. Selezionare la casella di controllo **Pagamento effettuato** nelle righe che rappresentano i documenti registrati per lo stesso cliente o fornitore per cui è stato eseguito un pagamento forfettario.  

    **Nota**: il cliente indicato nel campo **Nome** deve essere lo stesso in tutte le righe che verranno registrate come pagamento forfettario.  

    Se la casella di controllo **Compila automaticamente data di ricezione** nella finestra **Setup registrazione pagamenti** è selezionata, la data di lavorazione viene inserita nel campo **Data ricezione**.  
3. Nel campo **Data ricezione** immettere la data di esecuzione del pagamento. La data può essere diversa dalla data di lavoro.  

    **Nota**: questa data deve essere uguale in tutte le righe che verranno registrate come pagamento forfettario.  
4. Nel campo **Importo ricevuto** immettere gli importi su più righe che riassumono l'importo del pagamento forfettario.  

    **Suggerimento**: provare a registrare quanti più pagamenti completi è possibile con l'importo forfettario. Immettere gli importi che sono gli stessi presenti nel campo **Importo residuo** nel maggior numero di righe possibili.  
5. Ripetere i passaggi da 2 a 4 per altre righe che rappresentano i documenti registrati per lo stesso cliente per cui è stato eseguito un pagamento forfettario.  
6. Scegliere l'azione **Registra come pagamento forfettario**. Le informazioni sui pagamenti immesse vengono registrate per i documenti rappresentati dalle righe in cui è selezionata la casella di controllo **Pagamento effettuato**.  

I movimenti dei pagamenti vengono registrati nei conti di contabilità generale, nei conti bancari e nei conti clienti. Ogni pagamento viene collegato al documento di vendita registrato correlato.  

Se un pagamento della banca non è rappresentato dalla riga della finestra **Registrazione pagamenti**, è possibile che il documento correlato non sia ancora stato registrato. In questo caso, è possibile utilizzare una funzione di ricerca per trovare rapidamente il documento e registrarlo per elaborare il pagamento. Per ulteriori informazioni, vedere la sezione Procedura: Individuare documenti non pagati durante la riconciliazione manuale dei pagamenti clienti.  

Se un pagamento della banca non è rappresentato da alcun documento in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile aprire una riga di registrazione COGE precompilata nella finestra **Registrazione pagamenti** per registrare il pagamento direttamente nella contropartita senza collegarlo a un documento. In alternativa, è consigliabile inserire il pagamento nelle registrazioni fino a chiarire l'origine del pagamento. Per ulteriori informazioni, vedere la sezione "Per registrare un pagamento senza un documento correlato".  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Per elaborare manualmente i pagamenti clienti con sconti
Se è stato pattuito uno sconto nei pagamenti con il cliente, gli importi del pagamento possono essere inferiori rispetto agli importi della fattura se il pagamento viene eseguito prima della data dello sconto stabilita.  

Nella seguenti procedure vengono illustrati quattro modi diversi di registrare i pagamenti scontati nella finestra **Registrazione pagamenti**.  

* L'importo di pagamento è uguale all'importo residuo scontato e la data di pagamento è antecedente alla data di sconto. Il pagamento viene registrato così come è.  
* L'importo di pagamento è uguale all'importo residuo scontato ma la data di pagamento è successiva alla data di sconto. Il pagamento viene registrato come parziale. Il documento rimane aperto per raccogliere/pagare l'importo residuo. In alternativa, impostare una data di sconto successiva per consentire il pagamento completo.  
* L'importo di pagamento è inferiore all'importo scontato residuo. Il pagamento viene registrato come parziale. Il documento rimane aperto per raccogliere/pagare l'importo residuo.  
* L'importo di pagamento è superiore all'importo scontato residuo. I pagamenti vengono registrati così come sono. Solo l'importo residuo viene registrato. L'importo addizionale viene accreditato al cliente.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Per elaborare un importo di pagamento uguale all'importo scontato e dove si trova la data di pagamento prima della data di sconto
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è uguale a quello riportato nel campo **Importo residuo dopo sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.    
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga zero (0).  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento completo nei conti di contabilità generale, bancario e cliente.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Per elaborare un importo di pagamento uguale all'importo scontato ma dove si trova la data di pagamento dopo la data di sconto
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è uguale a quello riportato nel campo **Importo residuo dopo sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.
3. Nel campo **Data ricezione** immettere la data di pagamento che è posteriore alla data indicata nel campo **Data sconto pagamento**. Il carattere dei campi dati diventano rossi e un messaggio di errore viene visualizzato nella parte inferiore della finestra.

    **Suggerimento**: per fare un'eccezione e concedere lo sconto anche se il pagamento è in ritardo, è necessario attenersi alla seguente procedura:
4. Scegliere l'azione **Dettagli**.  
5. Nella finestra **Dettagli registrazione pagamenti**, nel campo **Data sconto pagamento** della Scheda dettaglio **Sconto pagamento**, immettere una data che sia posteriore alla data indicata nel campo **Data ricezione** della finestra **Registrazione pagamenti**.  

    Il messaggio di errore e il carattere rosso scompaiono ed è possibile procedere a elaborare il pagamento scontato.    
6. Verificare che il campo **Importo residuo** contenga l'importo residuo per pagare l'importo fattura completo.  
7. Scegliere l'azione **Registra pagamenti** per registrare il pagamento parziale nei conti di contabilità generale, bancario e cliente.  

Il documento correlato rimane aperto.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Per elaborare un pagamento inferiore all'importo scontato residuo
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è inferiore a quello riportato nel campo **Importo residuo dopo sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.  
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga l'importo residuo per pagare l'importo scontato.  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento parziale nei conti di contabilità generale, bancario e cliente.  

Il documento correlato rimane aperto.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Per elaborare un pagamento superiore all'importo scontato residuo
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è maggiore a quello riportato nel campo **Importo residuo dopo sconto**.  

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.    
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga zero (0).  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento completo nei conti di contabilità generale, bancario e cliente.  

Il documento correlato è chiuso e al cliente viene accreditato l'importo di pagamento in eccesso.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Per trovare un documento di vendita specifico non completamente fatturato
La finestra **Registrazione pagamenti** fornisce supporto in attività necessarie per le contropartite interne con le cifre effettive di cassa per garantire la raccolta dai clienti e il pagamento dovuto ai fornitori. Mostra i pagamenti in entrata inevasi come righe che rappresentano i documenti di vendita in cui è dovuto il pagamento di un importo.  

In genere, quando è stato eseguito un pagamento ed è stato registrato nella banca o altrove, il documento di vendita o di acquisto correlato è rappresentato come riga nella finestra **Registrazione pagamenti** poiché il documento in questione attende la registrazione del pagamento dell'importo inevaso. Talvolta un pagamento effettuato non è tuttavia rappresentato da una riga nella finestra **Registrazione pagamenti**, in genere perché la fattura del documento in questione non è stata completamente registrata.

Nella finestra **Ricerca documenti**, è possibile cercare tra i documenti che non sono completamente fatturati. È possibile eseguire la ricerca in base a uno dei seguenti criteri:  

* Numero documento  
* Importo o intervallo di importi  

Nella procedura seguente viene illustrato come trovare un documento specifico utilizzando entrambi i criteri di ricerca.  

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.
2. Con il puntatore su una riga qualsiasi, scegliere l'azione **Cerca documenti**.
3. Nella finestra **Ricerca documenti** immettere un valore di ricerca nel campo **Nr. documento**. .  

    **Nota**: il valore immesso in questo campo è racchiuso tra caratteri jolly nascosti. Ciò significa che la funzione ricerca tutti i numeri dei documenti contenenti il valore immesso.    
4. Nel campo **Importo** immettere l'importo specifico presente nel documento che si desidera cercare.  
5. Nel campo **% tolleranza importo** immettere una percentuale per definire l'intervallo degli importi che si desidera cercare per trovare il documento aperto.  

    Se si immette 10, la funzione cercherà gli importi in un intervallo tra il dieci percento in meno e il dieci percento in più rispetto al valore del campo **Importo**.    
6. Scegliere l'azione **Cerca**.  

La funzione di ricerca cerca tra i documenti che non sono completamente fatturati in base ai criteri specificati.  

Se uno o più documenti corrispondono ai criteri di ricerca, verrà aperta la finestra **Risultato ricerca documenti** nella quale saranno visualizzate le righe che rappresentano tali documenti. Ogni riga contiene un numero di documento, una descrizione e un importo in modo che sia possibile trovare un documento specifico, ad esempio in base alle informazioni sul rendiconto bancario.  

Se un pagamento della banca non è rappresentato da alcun documento in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile aprire una riga di registrazione COGE precompilata nella finestra **Registrazione pagamenti** per registrare il pagamento direttamente nella contropartita senza collegarlo a un documento. In alternativa, è consigliabile inserire il pagamento nelle registrazioni fino a chiarire l'origine del pagamento.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Per registrare un pagamento senza un documento correlato
Se un pagamento della banca non è rappresentato da alcun documento in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile aprire una riga di registrazione COGE precompilata nella finestra **Registrazione pagamenti** per registrare il pagamento direttamente nella contropartita senza collegarlo a un documento. In alternativa, è consigliabile registrare il pagamento nelle registrazioni fino a chiarire l'origine del pagamento.  

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione pagamenti**, quindi scegliere il collegamento correlato.  

Registrare un pagamento non documentato.  

1. Scegliere l'azione **Contabilità generale**.  

    Verrà visualizzata la finestra **Contabilità generale** con una riga precompilata con il conto di contropartita del batch registrazioni impostato nella finestra **Setup registrazione pagamenti**.  
2. Compilare i campi rimanenti nella riga delle registrazioni generali, ad esempio l'importo e il numero cliente o altre informazioni dal rendiconto bancario. Per ulteriori informazioni, vedere [Procedura: Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  

È possibile registrare la riga di registrazione per aggiornare nella contropartita. In alternativa, è possibile lasciare invariata la riga di registrazione non inserita e aggiungere una nota che indica che per il pagamento è necessaria un'analisi più accurata.  

Se la riga di registrazione non viene registrata, verrà aggiunta al valore del campo **Saldo non registrato** nella parte inferiore della finestra **Registrazione pagamenti**.  

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

