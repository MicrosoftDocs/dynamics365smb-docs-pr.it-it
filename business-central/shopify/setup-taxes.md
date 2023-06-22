---
title: Impostare le imposte per la connessione Shopify
description: Modalità di impostazione delle imposte in Shopify e Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="set-up-taxes-for-the-shopify-connection" />Impostare le imposte per la connessione Shopify

In questo articolo, esamineremo il modo in cui le varie impostazioni in Shopify influiscono sui prezzi e sulle imposte in negozio visualizzati per i clienti. Vedremo anche come configurare [!INCLUDE[prod_short](../includes/prod_short.md)] per supportare le impostazioni in Shopify. Questo articolo non vuole essere una guida fiscale completa. Per ulteriori informazioni, contatta l'autorità fiscale locale o un professionista fiscale.  

L'articolo presuppone che tu sia tenuto a pagare le tasse quando vendi beni a livello locale o internazionale.

## <a name="if-you-sell-domestically" />Se vendi sul mercato interno

Una volta configurato il tuo Shopify per riscuotere le tasse nel tuo paese o nella tua regione nazionale, puoi decidere come visualizzare i prezzi sul tuo negozio.

Puoi specificare se includere le imposte nei prezzi attivando o disattivando l'interruttore **Tutti i prezzi includono le imposte** nell'impostazione [**Imposte e acquisti**](https://www.shopify.com/admin/settings/taxes) in **Amministrazione Shopify**.

L'interruttore è in genere abilitato per i seguenti paesi:

* Australia
* Austria
* Belgio
* Repubblica Ceca
* Danimarca
* Finlandia
* Francia
* Germania
* Islanda
* Italia
* Paesi Bassi
* Nuova Zelanda
* Norvegia
* Spagna
* Svezia
* Svizzera
* Regno Unito. 

In mercati come questi, un prezzo di 100 EUR definito sulla scheda prodotto contiene già l'IVA. Il prezzo, comprensivo di IVA, viene visualizzato al cliente nella vetrina e alla cassa.  

Negli Stati Uniti e in Canada, i clienti non si aspettano che i prezzi siano comprensivi di imposte. L'imposta viene aggiunta al momento del pagamento, quindi l'interruttore **Tutti i prezzi includono le imposte** di solito è disattivato. In questo caso, il prezzo di $100 definito nella scheda prodotto è il prezzo senza tasse. Al momento del pagamento, le tasse vengono aggiunte al prezzo.

Per supportare lo scenario in cui **Tutti i prezzi includono le imposte** è selezionato, in [!INCLUDE[prod_short](../includes/prod_short.md)], compila i seguenti campi nella pagina **Scheda punto vendita Shopify**:  

1. Attiva l'interruttore **Prezzi IVA inclusa**.  
2. Nel campo **Gruppo di registrazione business IVA** specifica il gruppo di registrazione utilizzato per i clienti nazionali.  

Ora definisci i prezzi degli articoli nel campo **Scheda articolo** o **Listino prezzi di vendita** con o senza imposte. Quando si esportano i prezzi in Shopify, [!INCLUDE [prod_short](../includes/prod_short.md)] include le tasse nazionali nel prezzo calcolato e mostra il prezzo per il prodotto in Shopify.

[!Note]
> Queste impostazioni influiscono sull'esportazione dei prezzi. Quando importi ordini da Shopify, l'impostazione per il campo **Prezzi IVA inclusa** viene dal **Modello cliente** sulla scheda punto vendita Shopify o sul modello cliente per paese. Anche se utilizzi il cliente predefinito per gli ordini importati, devi inserire il **Codice modello cliente**.

## <a name="if-you-sell-internationally" />Se vendi sul mercato internazionale

Questa sezione illustra le impostazioni per gli scenari in cui è necessario riscuotere le tasse quando vendi in un altro paese, ad esempio altri paesi dell'UE.

Attualmente, il connettore Shopify supporta l'esportazione di un solo prezzo. Shopify applica automaticamente imposte, valute e arrotondamenti locali. L'interruttore **Tutti i prezzi includono le imposte** si traduce nelle azioni descritte nelle seguenti sottosezioni.

### <a name="all-prices-include-tax-is-selected" />Tutti i prezzi includono le imposte è selezionata

|-|Vendite sul mercato interno|Paese estero in cui riscuoti le imposte|Paese estero in cui non riscuoti le imposte|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1200|1200|1200|
|Percentuale aliquota fiscale|20|25|0|
|Prezzo in fase di pagamento|1200|1200|1200|

Il prezzo per il cliente rimane uguale, indipendentemente dalla relativa posizione, ma il margine viene impattato a causa delle aliquote fiscali diverse da paese a paese.

### <a name="all-prices-include-tax-is-not-selected" />Tutti i prezzi includono le imposte non è selezionata

|-|Vendite sul mercato interno|Paese estero in cui riscuoti le imposte|Paese estero in cui non riscuoti le imposte|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1000|1000|1000|
|Percentuale aliquota fiscale|20|25|0|
|Prezzo in fase di pagamento|1200|1250|1000|

Shopify aggiunge le imposte locali al prezzo definito sulla scheda del prodotto in base a dove vengono spedite le merci.

## <a name="dynamic-tax-inclusive-pricing" />Prezzi dinamici tasse incluse

I paesi hanno requisiti diversi per l'inclusione delle tasse nei prezzi. Se desideri che i prezzi includano automaticamente le tasse, puoi attivare [Prezzi dinamici tasse incluse](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) in Shopify.

In **Amministrazione Shopify**, seleziona **Includi o escludi imposte in base al paese del cliente** nella sezione **Altri mercati - Preferenze** delle impostazioni [**Mercati**](https://www.shopify.com/admin/settings/markets).  

> [!NOTE]
> Questa impostazione non influisce sui prezzi nei mercati nazionali, che è controllata dall'interruttore **Tutti i prezzi includono le imposte**.

### <a name="all-prices-include-tax-is-selected" />Tutti i prezzi includono le imposte è selezionata

|-|Vendite sul mercato interno|Paese estero dove l'imposta è inclusa nel prezzo|Paese estero dove l'imposta è esclusa|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1200|1250|1000|
|Percentuale aliquota fiscale|20|25|10|
|Prezzo in fase di pagamento|1200|1250|1100|

Il prezzo per ciascun cliente cambia a seconda della sua posizione.

### <a name="all-prices-include-tax-is-not-selected" />Tutti i prezzi includono le imposte non è selezionata

|-|Vendite sul mercato interno|Paese estero dove l'imposta è inclusa nel prezzo|Paese estero dove l'imposta è esclusa|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1000|1250|1000|
|Percentuale aliquota fiscale|20|25|10|
|Prezzo in fase di pagamento|1200|1250|1100|

> [!NOTE]
> L'interruttore **Tutti i prezzi includono le imposte** non cambia il modo in cui i prezzi vengono visualizzati per i clienti internazionali.

## <a name="if-you-sell-to-eu-customers" />Se vendi a clienti dell'UE

Diversi paesi dell'UE hanno aliquote fiscali locali diverse. Tuttavia, se risiedi nell'UE e vendi in altri paesi dell'UE, in alcuni casi puoi utilizzare l'aliquota fiscale locale.  

In **Amministrazione Shopify**, seleziona la casella di controllo **Riscuoti l'IVA** nella sezione **Unione europea** delle impostazioni [**Imposte e acquisti**](https://www.shopify.com/admin/settings/taxes).

|Riscuoti IVA|Aliquota IVA|
|-|-|
|Esenzione per le microimprese|Usa la tua aliquota fiscale nazionale per tutte le vendite all'interno dell'UE|
|Sportello unico o registrazione specifica per paese|Utilizza l'aliquota IVA del paese del tuo cliente|

### <a name="collect-vat-set-to-one-stop-shop-registration" />Riscuoti l'IVA impostata durante la registrazione allo sportello unico

Nell'esempio seguente, l'interruttore **Tutti i prezzi includono le imposte** è attivato. Il prezzo sulla scheda prodotto è impostato su *1.200*.

|-|Vendite sul mercato interno|Paese estero|
|------------------------|--------|--------|
|Prezzo visualizzato in negozio|1200|1250|
|Percentuale aliquota fiscale|20|25|
|Prezzo in fase di pagamento|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption" />Riscuoti l'IVA impostata sull'esenzione per le microimprese

Nell'esempio seguente, l'interruttore **Tutti i prezzi includono le imposte** è attivato. Il prezzo sulla scheda prodotto è impostato su *1.200*.

|-|Vendite sul mercato interno|Paese estero con aliquota fiscale locale del 25%.|
|------------------------|--------|--------|
|Prezzo visualizzato in negozio|1200|1200|
|Percentuale aliquota fiscale|20|20|
|Prezzo in fase di pagamento|1200|1200|

Shopify usa l'aliquota fiscale nazionale e ignora l'aliquota fiscale nel paese estero durante il calcolo dei prezzi finali.

## <a name="importing-shopify-orders-sold-to-international-customers" />Importazione degli ordini Shopify venduti a clienti internazionali

Se riscuoti le tasse da più paesi, molto probabilmente dovrai definire un'impostazione specifica per il paese in [!INCLUDE[prod_short](../includes/prod_short.md)]. C'è un motivo per cui questa impostazione è obbligatoria. Quando viene creato un documento di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)], [!INCLUDE [prod_short](../includes/prod_short.md)] calcola le tasse invece di riutilizzare quelle importate da Shopify.

Le impostazioni specifiche per paese/regione vengono scelte nella pagina **Modello cliente Shopify**. Puoi definire **Nr. cliente predefinito** o **N. codice modello cliente**. In entrambi i casi, assicurati che il cliente o il modello abbia i seguenti campi compilati:

1. **Categoria registrazione business generale** (utilizzata per clienti esteri).
2. **Categoria di registrazione business IVA** (utilizzata per clienti esteri).
3. **Prezzi IVA inclusa** (allineato con l'impostazione lato Shopify):

* Scegli **Sì** se **Tutti i prezzi includono le imposte** è abilitata e **Includi o escludi imposte in base al paese del cliente** è disabilitata.
* Scegli **No** se **Tutti i prezzi includono le imposte** è disabilitata e **Includi o escludi imposte in base al paese del cliente** è disabilitata.
* Scegli **Sì** se **Includi o escludi imposte in base al paese del cliente** è abilitata e il paese o la regione sono elencati in [Paesi tasse incluse](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Scegli **No** se **Includi o escludi imposte in base al paese del cliente** è abilitata e il paese o la regione non sono elencati in [Paesi tasse incluse](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> L'impostazione del campo **Prezzi IVA inclusa** proviene dal modello, non dal cliente specifico. Ecco perché è importante definire il modello del cliente.

## <a name="other-tax-remarks" />Altre note sulle imposte

Mentre l'ordine Shopify importato contiene informazioni sulle imposte, queste vengono ricalcolate quando si crea un documento di vendita. Il ricalcolo rende importante che le impostazioni IVA/imposta siano corrette in [!INCLUDE[prod_short](../includes/prod_short.md)].

* Tasse/aliquote IVA multiple sui prodotti. Ad esempio, alcune categorie di prodotti sono soggette a aliquote fiscali ridotte. Puoi usare la funzione [Forzatura imposta](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) in Shopify. Quando gli articoli vengono importati e creati in [!INCLUDE[prod_short](../includes/prod_short.md)], utilizzano la configurazione fiscale come specificata nel codice del modello dell'articolo nel negozio Shopify. Prima di importare gli ordini con tali articoli, aggiorna il gruppo di registrazione dei prodotti con IVA.  
* Aliquote fiscali dipendenti dall'indirizzo. Usa il campo **Priorità area fiscale** insieme alla tabella **Modelli per clienti** per sovrascrivere la logica standard che riempie il **Codice area Fiscale** nel documento di vendita. Il campo **Priorità area fiscale** specifica la priorità da cui la funzione dovrebbe prendere le informazioni su paese/area geografica o stato/provincia. Quindi il record corrispondente nei modelli cliente Shopify viene identificato e **Codice area fiscale**, **Debito fiscale** e **Cat. Reg. Business IVA** vengono utilizzate durante la creazione di un documento di vendita.  

## <a name="see-also" />Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
