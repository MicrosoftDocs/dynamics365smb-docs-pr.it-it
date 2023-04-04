---
title: Impostare le imposte per la connessione Shopify
description: Modalità di impostazione delle imposte in Shopify e Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Impostare le imposte per la connessione Shopify

In questo articolo, esamineremo il modo in cui le varie impostazioni in Shopify influiscono sui prezzi e sulle imposte in negozio che vengono visualizzati per il cliente. Vedremo anche come configurare [!INCLUDE[prod_short](../includes/prod_short.md)] per supportare le impostazioni in Shopify. Questo articolo non vuole essere una guida fiscale completa. Per ulteriori informazioni, contatta l'autorità fiscale locale o un professionista fiscale.  

L'articolo presuppone che tu sia tenuto a pagare le tasse quando vendi beni a livello locale o internazionale.

## Se vendi sul mercato interno

Una volta configurato il tuo Shopify per riscuotere le tasse nel tuo paese o nella tua regione nazionale, puoi decidere come visualizzare i prezzi sul tuo negozio.
Puoi controllare questa opzione abilitando o disabilitando l'interruttore **Tutti i prezzi includono le imposte** nelle impostazioni [**Imposte e acquisti**](https://www.shopify.com/admin/settings/taxes) in **Amministrazione Shopify**.

È comune che questo interruttore sia abilitato per paesi come Australia, Austria, Belgio, Repubblica Ceca, Danimarca, Finlandia, Francia, Germania, Islanda, Italia, Paesi Bassi, Nuova Zelanda, Norvegia, Spagna, Svezia, Svizzera e Regno Unito. In mercati come questi, il prezzo di *100 euro* definito nella scheda prodotto contiene già l'imposta sul valore aggiunto (IVA) e lo stesso prezzo viene visualizzato al cliente in negozio e al momento del pagamento.  

Negli Stati Uniti e in Canada, i clienti si aspettano di vedere i prezzi dei prodotti senza tasse, aggiunte al momento del pagamento. Quindi il campo **Tutti i prezzi includono le imposte** di solito non è selezionato. In questo caso, il prezzo di *$ 100* definito nella scheda prodotto rappresenta il prezzo senza tasse. In fase di pagamento, le tasse verranno aggiunte al prezzo per calcolare il totale.

Per supportare lo scenario in cui l'opzione **Tutti i prezzi includono le imposte** è selezionato sul lato [!INCLUDE[prod_short](../includes/prod_short.md)], compila il campo **Codice modello cliente** nella pagina **Scheda punto vendita Shopify** per accedere al modello con i seguenti campi definiti:  

1. **Categoria registrazione business generale**, utilizzata per clienti nazionali.  
2. **Categoria di registrazione business IVA**, utilizzata per clienti nazionali.  
3. **Prezzi IVA inclusa** impostata su *Sì*.  

Ora definisci i prezzi degli articoli nel campo **Scheda articolo** o **Listino prezzi di vendita**, con o senza imposte. Quando si esportano i prezzi in Shopify, il sistema calcola il prezzo per includere le tasse nazionali, quindi mostra quel prezzo nella scheda del prodotto in Shopify.

> [!NOTE]
> Se hai configurato il connettore Shopify per creare clienti automaticamente, potresti aver bisogno di più campi nel tuo modello, ad esempio **Categoria registrazione cliente**. Se utilizzi il cliente predefinito per gli ordini importati, assicurati che il cliente abbia gli stessi campi compilati. Devi ancora compilare **Codice modello cliente** come specificato sopra, poiché il campo **Prezzi imposta inclusa**/**Prezzi IVA inclusa** nel documento di vendita creato non dipende dal cliente ma dal **Modello cliente** dal punto vendita Shopify o dal modello cliente per paese.

## Se vendi sul mercato internazionale

In questa sezione, esamineremo le impostazioni per gli scenari in cui è necessario riscuotere le tasse quando vendi in un altro paese, ad esempio altri paesi dell'UE.

Attualmente, l'estensione **connettore Shopify** supporta l'esportazione di un solo prezzo. Shopify applica automaticamente imposte, valute e arrotondamenti locali. L'interruttore **Tutti i prezzi includono le imposte** si traduce nelle azioni descritte nelle seguenti sottosezioni.

### *Tutti i prezzi includono le imposte* è selezionata

|-|Vendite sul mercato interno|Paese estero in cui riscuoti le imposte|Paese estero in cui non riscuoti le imposte|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1200|1200|1200|
|Percentuale aliquota fiscale|20|25|0|
|Prezzo in fase di pagamento|1200|1200|1200|

Il prezzo per il cliente rimane uguale, indipendentemente dalla relativa posizione, ma il margine viene impattato a causa delle aliquote fiscali diverse da paese a paese.

### *Tutti i prezzi includono le imposte* non è selezionata

|-|Vendite sul mercato interno|Paese estero in cui riscuoti le imposte|Paese estero in cui non riscuoti le imposte|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1000|1000|1000|
|Percentuale aliquota fiscale|20|25|0|
|Prezzo in fase di pagamento|1200|1250|1000|

Shopify aggiunge le imposte locali oltre al prezzo definito sulla scheda del prodotto in base a dove vengono spedite le merci.

## Prezzi dinamici tasse incluse

Poiché paesi diversi hanno requisiti diversi a seconda che tu includa o meno le tasse nel prezzo mostrato, puoi attivare [Prezzi dinamici tasse incluse](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) in Shopify. Questa operazione automatizza la funzione di inclusione delle imposte.

Seleziona **Includi o escludi imposte in base al paese del cliente** nella sezione **Altri mercati - Preferenze** delle impostazioni [**Mercati**](https://www.shopify.com/admin/settings/markets) in **Amministrazione di Shopify**.  

> [!NOTE]
> Questa impostazione non influisce sulla rappresentazione dei prezzi nei mercati nazionali, che è controllata dall'interruttore **Tutti i prezzi includono le imposte**.

### *Tutti i prezzi includono le imposte* è selezionata

|-|Vendite sul mercato interno|Paese estero dove l'imposta è inclusa nel prezzo|Paese estero dove l'imposta è esclusa|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1200|1250|1000|
|Percentuale aliquota fiscale|20|25|10|
|Prezzo in fase di pagamento|1200|1250|1100|

Il prezzo per ciascun cliente cambia a seconda della sua posizione.

### *Tutti i prezzi includono le imposte* non è selezionata

|-|Vendite sul mercato interno|Paese estero dove l'imposta è inclusa nel prezzo|Paese estero dove l'imposta è esclusa|
|------------------------|--------|--------|--------|
|Prezzo visualizzato in negozio|1000|1250|1000|
|Percentuale aliquota fiscale|20|25|10|
|Prezzo in fase di pagamento|1200|1250|1100|

> [!NOTE]
> L'interruttore **Tutti i prezzi includono le imposte** non cambia il modo in cui i prezzi vengono visualizzati per i clienti internazionali.

## Se vendi a clienti dell'UE

Diversi paesi dell'UE hanno aliquote fiscali locali diverse. Tuttavia, se risiedi nell'UE e vendi in altri paesi dell'UE, in alcuni casi puoi utilizzare l'aliquota fiscale locale.  

Seleziona la casella **Riscuoti l'IVA** nella sezione **Unione europea** delle impostazioni [**Imposte e acquisti**](https://www.shopify.com/admin/settings/taxes) in **Amministrazione di Shopify**.

|Riscuoti IVA|Aliquota IVA|
|-|-|
|Esenzione per le microimprese|Usa la tua aliquota fiscale nazionale per tutte le vendite all'interno dell'UE|
|Sportello unico o registrazione specifica per paese|Utilizza l'aliquota IVA del paese del tuo cliente|


### Riscuoti l'IVA impostata durante la registrazione allo sportello unico

Nell'esempio seguente, l'interruttore **Tutti i prezzi includono le imposte** è abilitato. Il prezzo sulla scheda prodotto è impostato su *1.200*.
        
|-|Vendite sul mercato interno|Paese estero|
|------------------------|--------|--------|
|Prezzo visualizzato in negozio|1200|1250|
|Percentuale aliquota fiscale|20|25|
|Prezzo in fase di pagamento|1200|1250|       
        
### Riscuoti l'IVA impostata sull'esenzione per le microimprese

Nell'esempio seguente, l'interruttore **Tutti i prezzi includono le imposte** è abilitato. Il prezzo sulla scheda prodotto è impostato su *1.200*.
        
|-|Vendite sul mercato interno|Paese estero con aliquota fiscale locale del 25%.|
|------------------------|--------|--------|
|Prezzo visualizzato in negozio|1200|1200|
|Percentuale aliquota fiscale|20|20|
|Prezzo in fase di pagamento|1200|1200|           
    
Shopify ignora l'aliquota fiscale nel paese estero durante il calcolo dei prezzi finali e utilizza l'aliquota fiscale nazionale.

## Importazione degli ordini Shopify venduti a clienti internazionali

Se riscuoti le tasse da più paesi, molto probabilmente dovrai definire un'impostazione specifica per il paese in [!INCLUDE[prod_short](../includes/prod_short.md)]. Questa operazione è necessaria perché quando viene creato un documento di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)], il sistema calcola le tasse invece di riutilizzare quelle importate da Shopify.

Le impostazioni specifiche per paese/regione vengono scelte nella finestra **Modello cliente Shopify**. Puoi definire **Nr. cliente predefinito** o **N. codice modello cliente**. In entrambi i casi assicurati che il cliente o il modello selezionato abbia i seguenti campi definiti:

1. **Categoria registrazione business generale** (utilizzata per clienti esteri).
2. **Categoria di registrazione business IVA** (utilizzata per clienti esteri).
3. **Prezzi IVA inclusa** (allineato con l'impostazione lato Shopify):
* Scegli *Sì* se **Tutti i prezzi includono le imposte** è abilitata e **Includi o escludi imposte in base al paese del cliente** è disabilitata.
* Scegli *No* se **Tutti i prezzi includono le imposte** è disabilitata e **Includi o escludi imposte in base al paese del cliente** è disabilitata.
* Scegli *Sì* se **Includi o escludi imposte in base al paese del cliente** è abilitata e il paese o la regione sono elencati in [Paesi tasse incluse](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Scegli *No* se **Includi o escludi imposte in base al paese del cliente** è abilitata e il paese o la regione non sono elencati in [Paesi tasse incluse](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> L'impostazione del campo **Prezzi IVA inclusa** proviene dal modello, non dal cliente specifico. Ecco perché è importante che il modello del cliente sia definito.

## Altre note sulle imposte

Mentre l'ordine Shopify importato contiene informazioni sulle imposte, queste vengono ricalcolate quando si crea un documento di vendita. Il ricalcolo rende importante che le impostazioni IVA/imposta siano corrette in [!INCLUDE[prod_short](../includes/prod_short.md)].

- Tasse/aliquote IVA multiple sui prodotti. Ad esempio, alcune categorie di prodotti sono soggette a aliquote fiscali ridotte. Puoi usare la funzione [Forzatura imposta](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) in Shopify. Quando gli elementi vengono importati e creati in [!INCLUDE[prod_short](../includes/prod_short.md)], utilizzano la configurazione fiscale come compilata nel codice del modello dell'articolo nel negozio Shopify. Prima di importare ordini con tali articoli, è necessario aggiornare il gruppo di registrazione dei prodotti con IVA.  

- Aliquote fiscali dipendenti dall'indirizzo. Usa il campo **Priorità area fiscale** insieme alla tabella **Modelli per clienti** per sovrascrivere la logica standard che riempie il **Codice area Fiscale** nel documento di vendita. Il campo **Priorità area fiscale** specifica la priorità da cui la funzione dovrebbe prendere le informazioni su paese/area geografica o stato/provincia. Quindi il record corrispondente nei modelli cliente Shopify viene identificato e **Codice area fiscale**, **Debito fiscale** e **Cat. Reg. Business IVA** vengono utilizzate durante la creazione di un documento di vendita.  

## Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
