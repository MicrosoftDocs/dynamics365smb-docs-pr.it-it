---
title: Collegare i pagamenti ai documenti di vendita non pagati
description: Si collegano gli importi pagati dai clienti ai relativi documenti di vendita e si registra il pagamento per aggiornare i movimenti contabili cliente, contabilità generale e i movimenti contabili bancari.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.search.form: 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6fa22b84284d05d77bd04919403435d99050cded
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517793"
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Riconciliare i pagamenti dei clienti dall'elenco dei documenti di vendita non pagati
Quando i clienti hanno effettuato i pagamenti sul conto corrente elettronico, è necessario collegare ogni importo pagato al documento di vendita corrispondente e registrare il pagamento per aggiornare i movimenti cliente, bancari e di contabilità generale. In base alle esigenze aziendali, è possibile ottenere pagato e registrare il pagamento in diversi modi: manualmente, in modo automatico e tramite i servizi di pagamento.  

> [!NOTE]  
>   È possibile effettuare le stesse attività, inclusi i pagamenti fornitori, nella pagina **Registrazioni riconciliazione pagamenti** utilizzando le funzioni per l'importazione del rendiconto bancario, il collegamento automatico e la riconciliazione bancaria. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

La pagina **Registra pagamenti clienti** è progettata per assistere l'utente nell'esecuzione di attività in contropartite interne utilizzando le cifre effettive di cassa per garantire una riscossione efficiente dei pagamenti dai clienti. Questo strumento di elaborazione dei pagamenti consente di verificare rapidamente e registrare i pagamenti singoli o forfettari, elaborare i pagamenti scontati e individuare documenti non pagati specifici per i quali viene eseguito il pagamento.

I pagamenti per clienti diversi, con date di pagamento diverse, devono essere registrati come pagamenti singoli. I pagamenti per lo stesso cliente, con uguale data di pagamento, possono essere registrati come pagamento forfettario. Ciò risulta utile, ad esempio, quando un cliente ha effettuato un pagamento singolo che copre più fatture di vendita.

## <a name="to-set-up-the-payment-registration-journal"></a>Per impostare le registrazioni pagamenti
Poiché è possibile registrare tipi diversi di pagamento in conti di contropartita diversi, è necessario selezionare un conto di contropartita nella pagina **Setup registrazione pagamenti** prima di iniziare l'elaborazione dei pagamenti clienti. Se si esegue la registrazione sempre alla stessa contropartita, è possibile impostare tale conto come predefinito ed evitare ogni volta di aprire la pagina **Registra pagamenti clienti**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup registrazione pagamenti**, quindi scegli il collegamento correlato.

    In alternativa, nella pagina **Registra pagamenti clienti** scegliere l'azione **Setup**.    
2. Compilare i campi della pagina **Setup registrazione pagamenti**. Selezionare il campo per visualizzare una breve descrizione del campo o il collegamento alle informazioni correlate.  

## <a name="to-register-customer-payments-individually"></a>Per registrare i pagamenti del cliente singolarmente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registra pagamenti clienti**, quindi scegli il collegamento correlato.  

    Nella pagina **Registra pagamenti clienti** vengono visualizzati tutti i documenti registrati per cui un pagamento può essere registrato. La pagina può anche essere aperta dalle pagine **Clienti** e **Scheda cliente** dove viene automaticamente filtrata per il cliente specificato.  
2. Selezionare la casella di controllo **Pagamento effettuato** nella riga che rappresenta il documento registrato per cui è stato eseguito un pagamento.

    Se la casella di controllo **Compila automaticamente data di ricezione** nella pagina **Setup registrazione pagamenti** è selezionata, la data di lavorazione viene immessa nel campo **Data ricezione**.  
3. Nel campo **Data ricezione** immettere la data di esecuzione del pagamento. La data può essere diversa dalla data di lavoro.  
4. Nel campo **Importo ricevuto** immettere l'importo pagato.

    Per i pagamenti completi, questo importo è uguale a quello nel campo **Importo residuo** della riga. Per i pagamenti parziali, questo importo è minore di quello nel campo **Importo residuo** della riga.    
5. Ripetere i passaggi da 2 a 4 per le altre righe che rappresentano i documenti registrati per i quali vengono eseguiti i pagamenti.  
6. Scegliere l'azione **Registra pagamenti**.  

Le informazioni sui pagamenti vengono registrate per i documenti rappresentati dalle righe in cui è selezionata la casella di controllo **Pagamento effettuato**.  

I movimenti dei pagamenti vengono registrati nei conti di contabilità generale, nei conti bancari e nei conti clienti. Ogni pagamento viene collegato al documento di vendita registrato correlato.  

## <a name="to-reconcile-lump-sum-payments"></a>Per riconciliare i pagamenti forfettari
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.
2. Selezionare la casella di controllo **Pagamento effettuato** nelle righe che rappresentano i documenti registrati per lo stesso cliente o fornitore per cui è stato eseguito un pagamento forfettario.  

    > [!NOTE]  
    >   Il cliente nel campo **Nome** deve essere lo stesso in tutte le righe che verranno registrate come pagamento forfettario.  

    Se la casella di controllo **Compila automaticamente data di ricezione** nella pagina **Setup registrazione pagamenti** è selezionata, la data di lavorazione viene inserita nel campo **Data ricezione**.  
3. Nel campo **Data ricezione** immettere la data di esecuzione del pagamento. La data può essere diversa dalla data di lavoro.  

    > [!NOTE]  
    >   Questa data deve essere uguale in tutte le righe che verranno registrate come pagamento forfettario.  
4. Nel campo **Importo ricevuto** immettere gli importi su più righe che riassumono l'importo del pagamento forfettario.  

    > [!TIP]  
    > Provare a registrare quanti più pagamenti completi è possibile con l'importo forfettario. Immettere gli importi che sono gli stessi presenti nel campo **Importo residuo** nel maggior numero di righe possibili.  
5. Ripetere i passaggi da 2 a 4 per altre righe che rappresentano i documenti registrati per lo stesso cliente per cui è stato eseguito un pagamento forfettario.  
6. Scegliere l'azione **Registra come pagamento forfettario**. Le informazioni sui pagamenti immesse vengono registrate per i documenti rappresentati dalle righe in cui è selezionata la casella di controllo **Pagamento effettuato**.  

I movimenti dei pagamenti vengono registrati nei conti di contabilità generale, nei conti bancari e nei conti clienti. Ogni pagamento viene collegato al documento di vendita registrato correlato.  

Se un pagamento della banca non è rappresentato dalla riga della pagina **Registrazione pagamenti**, è possibile che il documento correlato non sia ancora stato registrato. In questo caso, è possibile utilizzare una funzione di ricerca per trovare rapidamente il documento e registrarlo per elaborare il pagamento. Per ulteriori informazioni, vedere [Per trovare un documento di vendita specifico non completamente fatturato](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-find-a-specific-sales-document-that-is-not-fully-invoiced).  

Se un pagamento della banca non è rappresentato da alcun documento in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile aprire una riga di registrazione COGE precompilata nella pagina **Registrazione pagamenti** per registrare il pagamento direttamente nella contropartita senza collegarlo a un documento. In alternativa, è consigliabile inserire il pagamento nelle registrazioni fino a chiarire l'origine del pagamento. Per ulteriori informazioni, vedere [Per registrare un pagamento senza un documento correlato](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Per elaborare manualmente i pagamenti clienti con sconti
Se è stato pattuito uno sconto nei pagamenti con il cliente, gli importi del pagamento possono essere inferiori rispetto agli importi della fattura se il pagamento viene eseguito prima della data dello sconto stabilita.  

Nella seguenti procedure vengono illustrati quattro modi diversi di registrare i pagamenti scontati nella pagina **Registrazione pagamenti**.  

* L'importo di pagamento è uguale all'importo residuo scontato e la data di pagamento è antecedente alla data di sconto. Il pagamento viene registrato così come è.  
* L'importo di pagamento è uguale all'importo residuo scontato ma la data di pagamento è successiva alla data di sconto. Il pagamento viene registrato come parziale. Il documento rimane aperto per raccogliere/pagare l'importo residuo. In alternativa, impostare una data di sconto successiva per consentire il pagamento completo.  
* L'importo di pagamento è inferiore all'importo scontato residuo. Il pagamento viene registrato come parziale. Il documento rimane aperto per raccogliere/pagare l'importo residuo.  
* L'importo di pagamento è superiore all'importo scontato residuo. I pagamenti vengono registrati così come sono. Solo l'importo residuo viene registrato. L'importo addizionale viene accreditato al cliente.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Per elaborare un importo di pagamento uguale all'importo scontato e dove si trova la data di pagamento prima della data di sconto
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è uguale a quello riportato nel campo **Importo residuo dopo sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.    
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga zero (0).  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento completo nei conti di contabilità generale, bancario e cliente.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Per elaborare un importo di pagamento uguale all'importo scontato ma dove si trova la data di pagamento dopo la data di sconto
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è uguale a quello riportato nel campo **Importo residuo dopo sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.
3. Nel campo **Data ricezione** immettere la data di pagamento che è posteriore alla data indicata nel campo **Data sconto pagamento**. Il carattere dei campi dati diventano rossi e un messaggio di errore viene visualizzato nella parte inferiore della pagina.

    > [!TIP]  
    >   Per fare un'eccezione e concedere lo sconto anche se il pagamento è in ritardo, è necessario attenersi alla seguente procedura:
4. Scegliere l'azione **Dettagli**.  
5. Nella pagina **Dettagli registrazione pagamenti**, nel campo **Data sconto pagamento** della Scheda dettaglio **Sconto pagamento**, immettere una data che sia posteriore alla data indicata nel campo **Data ricezione** della pagina **Registrazione pagamenti**.  

    Il messaggio di errore e il carattere rosso scompaiono ed è possibile procedere a elaborare il pagamento scontato.    
6. Verificare che il campo **Importo residuo** contenga l'importo residuo per pagare l'importo fattura completo.  
7. Scegliere l'azione **Registra pagamenti** per registrare il pagamento parziale nei conti di contabilità generale, bancario e cliente.  

Il documento correlato rimane aperto.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Per elaborare un pagamento inferiore all'importo scontato residuo
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è inferiore a quello riportato nel campo **Importo residuo dopo sconto**.

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.  
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga l'importo residuo per pagare l'importo scontato.  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento parziale nei conti di contabilità generale, bancario e cliente.  

Il documento correlato rimane aperto.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Per elaborare un pagamento superiore all'importo scontato residuo
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.  
2. Immettere l'importo del pagamento nel campo **Importo ricevuto**. L'importo è maggiore a quello riportato nel campo **Importo residuo dopo sconto**.  

    La casella di controllo **Pagamento effettuato** viene selezionata automaticamente e nel campo **Data ricezione** viene inserita la data di lavoro.    
3. Nel campo **Data ricezione** immettere la data di pagamento. La data è anteriore alla data nel campo **Data sconto pagamento**.
4. Verificare che il campo **Importo residuo** contenga zero (0).  
5. Scegliere l'azione **Registra pagamenti** per registrare il pagamento completo nei conti di contabilità generale, bancario e cliente.  

Il documento correlato è chiuso e al cliente viene accreditato l'importo di pagamento in eccesso.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Per trovare un documento di vendita specifico non completamente fatturato
La pagina **Registrazione pagamenti** fornisce supporto in attività necessarie per le contropartite interne con le cifre effettive di cassa per garantire la raccolta dai clienti. Mostra i pagamenti in entrata inevasi come righe che rappresentano i documenti di vendita in cui è dovuto il pagamento di un importo.  

In genere, quando è stato eseguito un pagamento ed è stato registrato nella banca o altrove, il documento di vendita o di acquisto correlato è rappresentato come riga nella pagina **Registrazione pagamenti** poiché il documento in questione attende la registrazione del pagamento dell'importo inevaso. Talvolta un pagamento effettuato non è tuttavia rappresentato da una riga nella pagina **Registrazione pagamenti**, in genere perché la fattura del documento in questione non è stata completamente registrata.

Nella pagina **Ricerca documenti**, è possibile cercare tra i documenti che non sono completamente fatturati. È possibile eseguire la ricerca in base a uno dei seguenti criteri:  

* Numero documento  
* Importo o intervallo di importi  

Nella procedura seguente viene illustrato come trovare un documento specifico utilizzando entrambi i criteri di ricerca.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.
2. Con il puntatore su una riga qualsiasi, scegliere l'azione **Cerca documenti**.
3. Nella pagina **Ricerca documenti** immettere un valore di ricerca nel campo **Nr. documento**.  

    > [!NOTE]  
    >   Il valore immesso in questo campo è contenuta in caratteri jolly nascosti. Ciò significa che la funzione ricerca tutti i numeri dei documenti contenenti il valore immesso.    
4. Nel campo **Importo** immettere l'importo specifico presente nel documento che si desidera cercare.  
5. Nel campo **% tolleranza importo** immettere una percentuale per definire l'intervallo degli importi che si desidera cercare per trovare il documento aperto.  

    Se si immette 10, la funzione cercherà gli importi in un intervallo tra il dieci percento in meno e il dieci percento in più rispetto al valore del campo **Importo**.    
6. Scegliere l'azione **Cerca**.  

La funzione di ricerca cerca tra i documenti che non sono completamente fatturati in base ai criteri specificati.  

Se uno o più documenti corrispondono ai criteri di ricerca, verrà aperta la pagina **Risultato ricerca documenti** nella quale saranno visualizzate le righe che rappresentano tali documenti. Ogni riga contiene un numero di documento, una descrizione e un importo in modo che sia possibile trovare un documento specifico, ad esempio in base alle informazioni sul rendiconto bancario.  

Se un pagamento della banca non è rappresentato da alcun documento in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile aprire una riga di registrazione COGE precompilata nella pagina **Registrazione pagamenti** per registrare il pagamento direttamente nella contropartita senza collegarlo a un documento. In alternativa, è consigliabile inserire il pagamento nelle registrazioni fino a chiarire l'origine del pagamento.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Per registrare un pagamento senza un documento correlato
Se un pagamento della banca non è rappresentato da alcun documento in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile aprire una riga di registrazione COGE precompilata nella pagina **Registrazione pagamenti** per registrare il pagamento direttamente nella contropartita senza collegarlo a un documento. In alternativa, è consigliabile registrare il pagamento nelle registrazioni fino a chiarire l'origine del pagamento.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione pagamenti**, quindi scegli il collegamento correlato.  

    Registrare un pagamento non documentato.  
2. Scegliere l'azione **Contabilità generale**.  

    Verrà visualizzata la pagina **Contabilità generale** con una riga precompilata con il conto di contropartita del batch registrazioni impostato nella pagina **Setup registrazione pagamenti**.  
3. Compilare i campi rimanenti nella riga delle registrazioni generali, ad esempio l'importo e il numero cliente o altre informazioni dal rendiconto bancario. Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).  

È possibile registrare la riga di registrazione per aggiornare nella contropartita. In alternativa, è possibile lasciare invariata la riga di registrazione non inserita e aggiungere una nota che indica che per il pagamento è necessaria un'analisi più accurata.  

Se la riga di registrazione non viene registrata, verrà aggiunta al valore del campo **Saldo non registrato** nella parte inferiore della pagina **Registrazione pagamenti**.  

## <a name="see-also"></a>Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]