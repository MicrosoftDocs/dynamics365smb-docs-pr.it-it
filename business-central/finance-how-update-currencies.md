---
title: Aggiornare i tassi di cambio delle valute (video)
description: Se tieni traccia degli importi in differenti valute puoi utilizzare Business Central per rettificare i tassi di cambio.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 09/07/2023
ms.author: bholtorf
---
# <a name="update-currency-exchange-rates"></a>Aggiornare i tassi di cambio valuta

Puoi definire differenti valute in [!INCLUDE [prod_short](includes/prod_short.md)], ad esempio se commerci in valute diverse dalla tua valuta locale. Per tenere traccia delle variazioni dei tassi di cambio valuta, puoi gestire i tassi manualmente oppure impostare un servizio di cambio valuta.

## <a name="currencies"></a>Valute

> [!TIP]  
> In [!INCLUDE[prod_short](includes/prod_short.md)], se stai cercando informazioni in tempo reale sui tassi di cambio delle valute estere o sui tassi di cambio storici, queste informazioni vanno sotto il nome di valuta. Oltre a questo articolo, vedere anche [Impostare una valuta di dichiarazione aggiuntiva](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Specifica i codici valuta nell'elenco **Valute**, comprese le informazioni e le impostazioni aggiuntive necessarie per ciascun codice valuta. Per ulteriori informazioni, vedi [Valute](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Esempio di una transazione in valuta esigibile

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Tassi di cambio

I tassi di cambio sono lo strumento per calcolare il valore in valuta locale (LCY) di ogni transazione in valuta. La pagina **Tassi di cambio** include i seguenti campi:

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Data Inizio**|La data in cui il tasso di valuta è stato effettuato|  
|**Codice valuta**|Il codice valuta relativo a questo tasso di cambio|  
|**Cod. Valuta Relativa**|Se questa valuta fa parte di un calcolo di valuta triangolare, il relativo codice valuta può essere impostato qui|  
|**Importo Tasso di Cambio**|L'importo del tasso di cambio è il tasso da utilizzare per il codice valuta selezionato nella riga. Normalmente 1 o 100|  
|**Importo Tasso di Cambio Relativo**|L'importo del tasso di cambio relazionale è il tasso da utilizzare per il codice valuta relativa|  
|**Rett. Importo Tasso di Cambio**|L'importo del tasso di cambio di rettifica è il tasso da utilizzare per il codice valuta selezionato nella riga per l'utilizzo del processo batch **Regola tassi di cambio**|  
|**Importo Rett. Tasso Cambio Rel.**|L'importo del tasso di cambio di rettifica relazionale è il tasso da utilizzare per il codice valuta selezionato nella riga per l'utilizzo del processo batch **Regola tassi di cambio**|  
|**Fissa importo tasso di cambio**|Specifica se il tasso di cambio della valuta può essere modificato su fatture e righe di registrazione.|  

In generale, i valori dei campi **Importo del tasso di cambio** e **Importo del tasso di cambio relazionale** vengono utilizzati come tasso di cambio predefinito su tutti i nuovi documenti crediti e debiti creati in futuro. Al documento viene assegnato il tasso di cambio in base alla data di lavoro corrente.  

> [!Note]
> Il tasso di cambio effettivo verrà calcolato utilizzando questa formula:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

L'importo del tasso di cambio di rettifica o l'importo del tasso di cambio di rettifica relazionale, aggiorna tutte le transazioni bancarie, attive o passive aperte.  

> [!Note]
> Il tasso di cambio effettivo verrà calcolato utilizzando questa formula:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Rettifica dei tassi di cambio

Poiché i tassi di cambio oscillano costantemente, devi rettificare periodicamente altri equivalenti in valuta. In caso contrario, gli importi che hai convertito da valute estere (o altre valute) e registrato nella contabilità generale in valuta locale possono non essere corretti. Inoltre, devi aggiornare i movimenti giornalieri registrati prima di immettere un tasso di cambio giornaliero.

Usa il processo batch **Rettifica tassi di cambio** per rettificare manualmente i tassi di cambio per movimenti cliente, fornitore e conti correnti bancari registrati. Il processo batch può anche aggiornare importi in altre valute di dichiarazione nei movimenti C/G.  

> [!TIP]
> È possibile utilizzare un servizio per aggiornare automaticamente i tassi di cambio nel sistema. Per ulteriori informazioni, vedere [Per impostare un servizio dei tassi di cambio delle valute](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Tuttavia, ciò non modifica i tassi di cambio sulle transazioni già registrate. Per aggiornare i tassi di cambio sui movimenti registrati, utilizzare il processo batch **Modifica i tassi di cambio**.

Puoi inoltre specificare il modo in cui la rettifica gestirà le dimensioni per utili e perdite non realizzati scegliendo una delle seguenti opzioni nel campo **Registrazione dimensione**:  

* **Dimensioni movimento di origine**: trasferisce valori di dimensione per movimenti C/G per utili e perdite non realizzati dal movimento che stai rettificando.  
* **Nessuna dimensione**: non trasferisce valori di dimensione per utili e perdite non realizzati a movimenti C/G. [!INCLUDE [prod_short](includes/prod_short.md)] utilizzerà comunque le impostazioni predefinite delle dimensioni, ad esempio **Codice obbligatorio**, **Stesso codice** o **Nessun codice**. Se i movimenti della transazione di origine hanno valori di dimensione, la rettifica crea movimenti senza valori di dimensione.  
* **Dimensioni conto C/G**: trasferisce valori di dimensione dal movimento di origine delle impostazioni delle dimensioni del conto C/G per utili e perdite non realizzati a movimenti C/G.

> [!NOTE]
> Per utilizzare la funzionalità di anteprima, devi attivare la funzionalità **Aggiornamento della funzionalità: abilitare l'utilizzo della nuova rettifica tasso di cambio estendibile, inclusa la revisione registrazione** nella pagina **[Gestione funzionalità](https://businesscentral.dynamics.com/?page=2610)**.

> [!IMPORTANT]
> A causa dei requisiti locali in Svizzera, non consigliamo di abilitare **Aggiornamento della funzionalità: abilitare l'utilizzo della nuova rettifica tasso di cambio estendibile, inclusa la revisione registrazione** nella versione per la Svizzera.

## <a name="preview-the-effect-of-an-adjustment"></a>Visualizzare in anteprima l'effetto di una rettifica

Puoi visualizzare in anteprima l'effetto che una rettifica di un tasso di cambio avrà sulla registrazione prima di effettuare la registrazione scegliendo l'azione **Anteprima registrazione** nella pagina di richiesta (report 596) del report **Rettifica tassi di cambio**. Nella pagina di richiesta puoi specificare cosa includere nell'anteprima:

* Una registrazione dettagliata nella contabilità generale per movimento
* Una registrazione riepilogativa per valuta. Seleziona semplicemente il campo **Rettifica per movimento** nel report **Rettifica tassi di cambio**.

### <a name="effect-on-customers-and-vendors"></a>Effetto su clienti e fornitori

Per i conti di clienti e fornitori, il processo batch usa il tasso di cambio che era valido alla data di registrazione specificata per il processo batch per rettificare la valuta. Durante il processo batch vengono calcolate le differenze per singoli saldi in valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili non-realizzati** o nel campo **Conto Perdite Non-Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nel conto crediti/debiti della contabilità generale.

Il processo batch consente di elaborare tutti i movimenti registro clienti e i movimenti fornitori aperti. Se per un movimento vi è una differenza di tasso di cambio, il processo batch crea un nuovo movimento contabile fornitori o clienti dettagliato. Il nuovo movimento riflette l'importo rettificato nel movimento contabile clienti o fornitori.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioni nei movimenti contabili clienti e fornitori

[!INCLUDE [prod_short](includes/prod_short.md)] assegna le dimensioni dai movimenti contabili clienti o fornitori a movimenti di rettifica e registra le rettifiche per ogni combinazione di valori di dimensione.

### <a name="effect-on-bank-accounts"></a>Effetto sui conti correnti bancari

Per i conti correnti bancari, la valuta viene rettificata utilizzando il tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per ogni conto corrente bancario che ha un codice di valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili realizzati** o nel campo **Conto Perdite Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nei conti correnti bancari CoGe specificati nelle categorie di registrazione dei conti correnti bancari. Viene calcolato un solo movimento per valuta per categoria di registrazione.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioni nei movimenti di conto corrente bancario

Ai movimenti di rettifica per il conto CoGe del conto corrente bancario e per il conto profitti/perdite vengono assegnate le dimensioni di default del conto corrente bancario.

### <a name="effect-on-gl-accounts"></a>Effetto su conti C/G

Se registri un'altra valuta di dichiarazione, il processo batch può creare nuovi movimenti di contabilità generale per rettifiche valutarie tra la valuta locale e un'altra valuta di dichiarazione. Verranno calcolate le differenze per ogni movimento C/G e inserite delle rettifiche a seconda del contenuto del campo **Rettifica tasso di cambio** di ogni conto C/G.

#### <a name="dimensions-on-gl-account-entries"></a>Dimensioni in movimenti di conti C/G

Ai movimenti di rettifica vengono assegnate le dimensioni di default dei conti in cui vengono registrati.

> [!Important]
> Prima di eseguire il processo batch, è necessario immettere i tassi di cambio di rettifica necessari alla rettifica dei saldi in valuta estera. Questa operazione viene eseguita nella pagina **Tassi di cambio valuta**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Per impostare un servizio dei tassi di cambio delle valute

È possibile utilizzare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute, ad esempio FloatRates. 

> [!NOTE]
> La maggior parte dei servizi di tasso cambio fornisce dati compatibili con il processo di importazione in [!INCLUDE[prod_short](includes/prod_short.md)]. Tuttavia, a volte i dati vengono formattati in modo diverso e sarà necessario personalizzare il processo di importazione. A tale scopo, è possibile utilizzare il framework di scambio dati la propria codeunit. Per eseguire l'operazione, sarà probabilmente necessario l'aiuto di uno sviluppatore. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Servizi di tassi di cambio valute**, quindi seleziona il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Servizi tasso di cambio valuta** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Attivare il pulsante **Abilitato** per attivare per abilitare il servizio.

> [!NOTE]
> Il seguente video mostra un esempio di come connettersi a un servizio di cambio valuta, utilizzando la Banca centrale europea come esempio. Nel segmento che descrive come impostare le mappature dei campi, l'impostazione nella colonna **Sorgente** per il **Nodo padre per codice valuta** restituirà solo la prima valuta trovata. L'impostazione deve essere `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Per aggiornare i tassi di cambio delle valute mediante un servizio

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Valute**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Aggiorna tassi di cambio**.

Il valore nel campo **Tasso di cambio** della pagina **Valute** viene aggiornato con il tasso di cambio delle valute più recente.

## <a name="correct-mistakes"></a>Correggere errori

Di tanto in tanto è possibile che sia necessario correggere un errore in una transazione di pagamento associata a rettifiche a utili e perdite in valuta estera. Puoi utilizzare l'azione **Storna transazione** nelle pagine **Movimenti contabili bancari**, **Registro cliente Movimenti** e **Movimenti contabili fornitori** per annullare e stornare la transazione di pagamento.

> [!NOTE]
> Quando annulli e storni un pagamento per un movimento a cui erano associate rettifiche del tasso di cambio, lo storno registra i movimenti di storno per le rettifiche. È possibile che tu debba eseguire nuovamente la rettifica del tasso di cambio per ottenere il saldo corrente corretto.

## <a name="see-also"></a>Vedi anche

[Valute in Business Central](finance-currencies.md)  
[Impostare le valute](finance-set-up-currencies.md)  
[Impostare una valuta di dichiarazione addizionale](finance-how-setup-additional-currencies.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
