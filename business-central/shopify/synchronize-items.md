---
title: Sincronizzare articoli e inventario
description: Configurare ed eseguire sincronizzazioni di articoli tra Shopify e Business Central
ms.date: 04/28/2024
ms.topic: article
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# <a name="synchronize-items-and-inventory"></a>Sincronizzare articoli e inventario

Gli **Articoli** in [!INCLUDE[prod_short](../includes/prod_short.md)] sono equivalenti ai *prodotti* in Shopify e includono beni fisici, download digitali, servizi e buoni regalo che vendi. Ci sono due ragioni principali per sincronizzare gli elementi:

1. La gestione dei dati viene eseguita principalmente in [!INCLUDE[prod_short](../includes/prod_short.md)]. Devi esportare tutti o alcuni dati da lì in Shopify e renderli visibili. Puoi esportare il nome dell'articolo, la descrizione, l'immagine, i prezzi, la disponibilità, le varianti, i dettagli del fornitore e il codice a barre. Una volta esportati, puoi rivedere gli articoli o renderli immediatamente visibili.
2. Quando un ordine di Shopify viene importato, le informazioni sugli articoli sono essenziali per l'ulteriore elaborazione del documento in [!INCLUDE[prod_short](../includes/prod_short.md)].

I due scenari precedenti sono sempre abilitati.

Un terzo scenario è gestire i dati in Shopify e importare gli articoli in blocco in [!INCLUDE[prod_short](../includes/prod_short.md)]. Questo scenario può essere utile per gli eventi di migrazione dei dati, quando un punto vendita online esistente deve essere collegato a uno nuovo ambiente [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="define-item-synchronizations"></a>Definire le sincronizzazioni degli articoli

1. Scegli l'icona di ricerca a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punto vendita Shopify**. Apri il punto vendita per il quale desideri configurare la sincronizzazione degli articoli.
2. Dal campo **Sincronizza articolo**, seleziona l'opzione richiesta.

   Nella seguente tabella vengono descritte le opzioni.

   |Opzione|Descrizione|
   |------|-----------|
   |**Vuoto**| I prodotti vengono importati insieme all'importazione degli ordini. I prodotti vengono esportati in Shopify se un utente esegue l'azione **Aggiungi articolo** dalla pagina **Prodotti Shopify**. Questa opzione è il processo predefinito.|
   |**A Shopify**| Seleziona questa opzione se, dopo la sincronizzazione iniziale attivata dall'azione **Aggiungi articolo**, prevedi di aggiornare i prodotti manualmente utilizzando l'azione **Sincronizza prodotto** o la coda processi per gli aggiornamenti ricorrenti. Ricordati di abilitare il campo **Può aggiornare il prodotto Shopify**. Se non è abilitato, è uguale all'opzione **Vuoto** (processo predefinito). Per ulteriori informazioni, vedi la sezione [Esportare articoli su Shopify](synchronize-items.md#export-items-to-shopify)|
   |**Da Shopify**| Scegli questa opzione se prevedi di importare prodotti da Shopify in blocco, manualmente con l'azione **Sincronizza prodotto** o la coda processi per gli aggiornamenti ricorrenti. Per ulteriori informazioni, vedi la sezione [Importare articoli da Shopify](synchronize-items.md#import-items-from-shopify)|

   > [!NOTE]
   > Modifica **Sincronizza articolo** da **Da Shopify** a **A Shopify** non ha effetto se non abiliti **Può aggiornare Prodotti Shopify**.

## <a name="import-items-from-shopify"></a>Importare articoli da Shopify

Importa gli articoli da Shopify in blocco o insieme agli ordini per aggiungerli alle tabelle **Prodotto Shopify** e **Variante Shopify**. Quindi mappa i prodotti e le varianti importati ad Articoli e varianti in [!INCLUDE[prod_short](../includes/prod_short.md)]. Gestisci il processo utilizzando le seguenti impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Crea automaticamente articoli sconosciuti**|Quando prodotti e varianti Shopify vengono importati in [!INCLUDE[prod_short](../includes/prod_short.md)], la funzione [!INCLUDE[prod_short](../includes/prod_short.md)] cerca sempre di trovare prima il record corrispondente nell'elenco degli elementi. **Mapping SKU** influisce sul modo in cui viene eseguita la corrispondenza e crea un nuovo articolo e/o una variante articolo. Abilita questa opzione se desideri creare un nuovo articolo o quando non esiste un record corrispondente. Il nuovo articolo viene creato utilizzando i dati importati e il **Codice modello articolo**. Se questa opzione non è abilitata, dovrai creare un articolo manualmente e usare l'azione **Esegui mapping prodotto** nella pagina **Prodotti Shopify**.|
|**Codice modello articolo**|Utilizzalo insieme all'interruttore **Crea automaticamente articoli sconosciuti**.<br>Scegli il modello che vuoi usare per gli articoli creati automaticamente.|
|**Mapping SKU**|Scegli come vuoi usare il valore **SKU** importato da Shopify durante il mapping la creazione dell'articolo/variante. Per ulteriori informazioni vedi la sezione [Effetto delle SKU e dei codici a barre dei prodotti Shopify sulla mappatura e sulla creazione di articoli e varianti in Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Separatore campo SKU**|Usalo insieme a **Mapping SKU** impostato sull'opzione **[Nr. articolo e codice variante](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Definisci un separatore da usare per dividere la SKU.<br>Se in Shopify crei la variante con SKU "1000/001", digita "/" nel campo **Separatore di campo SKU** per ottenere il numero dell'articolo [!INCLUDE[prod_short](../includes/prod_short.md)] come "1000" e il codice della variante articolo come "001". Tieni presente che se crei la variante con lo SKU '1000/001/111' in Shopify, il numero dell'articolo in [!INCLUDE[prod_short](../includes/prod_short.md)] sarà "1000" e il codice della variante articolo "001". La parte "111" viene ignorata. |
|**Prefisso variante**|Usato insieme a **Mapping SKU** impostato sull'opzione **Codice variante** o **Nr. articolo + Codice variante** come strategia di fallback quando lo SKU proveniente da Shopify è vuoto.<br>Se vuoi creare la variante articolo in [!INCLUDE[prod_short](../includes/prod_short.md)] automaticamente, dovrai inserire un valore in **Codice**. Per impostazione predefinita, viene utilizzato il valore definito nel campo SKU importato da Shopify. Tuttavia, se lo SKU è vuoto, genererà codice che inizia con il prefisso della variante definito e "001".|
|**Shopify può aggiornare l'articolo**|Scegli questa opzione se desideri aggiornare automaticamente gli articoli e/o le varianti.|
|**UdM come variante**| Scegli questa opzione se desideri che tutte le unità di misura degli articoli vengano esportate come varianti separate. Personalizza la pagina per aggiungere il campo. Per ulteriori informazioni, vedi la sezione [Unità di misura come variante](synchronize-items.md#unit-of-measure-as-variant).|
|**Nome opzione variante per UdM**| Utilizza questo campo con **UdM come variante** per specificare sotto quale opzione aggiungere varianti che rappresentano unità di misura. Il valore predefinito è *Unità di misura*. Utilizza la personalizzazione per aggiungere il campo alla pagina.|

## <a name="export-items-to-shopify"></a>Esportare articoli in Shopify

Esistono diversi modi per esportare articoli in Shopify:

* Utilizza l'azione **Aggiungi articolo a Shopify** direttamente dalla pagina **Scheda articolo**.
* Utilizza l'azione  **Aggiungi articolo**  nella pagina  **Prodotti Shopify** .
* Esegui la sincronizzazione degli articoli una o più volte con l'automazione.

Indipendentemente dal modo in cui esporti gli articoli, le informazioni specifiche sugli articoli vengono trasferite all'elenco dei prodotti Shopify a seconda delle impostazioni scelte per la sincronizzazione degli articoli.

> [!IMPORTANT]
> Il prodotto viene aggiunto solo al canale di vendita **Negozio online**. Devi pubblicare prodotti su altri canali di vendita, come Shopify POS, da Shopify.

Puoi gestire il processo di esportazione degli articoli utilizzando queste impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Sincronizza testo esteso articolo**|Seleziona questo campo per sincronizzare il testo esteso dell'articolo. Dal momento che verrà aggiunto al campo **Descrizione**, può contenere codice HTML. |
|**Sincronizza attributi articolo**|Seleziona questo campo per sincronizzare gli attributi dell'articolo. Gli attributi sono formattati come una tabella e inclusi nel campo **Descrizione** di Shopify.|
|**Sincronizza testo marketing articolo**|Seleziona questo campo per sincronizzare il testo di marketing dell'articolo. Sebbene il testo di marketing sia una sorta di descrizione, è diverso da quello del campo **Descrizione** dell'articolo. Il campo **Descrizione** viene in genere utilizzato come nome visualizzato conciso per identificare rapidamente il prodotto. Il testo di marketing, invece, è un testo più ricco e descrittivo. Il suo scopo è aggiungere contenuti di marketing e promozionali. Questo testo può quindi essere pubblicato con l'articolo in Shopify. Il testo di marketing può essere creato in due modi: Utilizza Copilot, che suggerisce il testo generato dall'intelligenza artificiale o inizia da zero.|
|**Codice lingua**|Seleziona questo campo se desideri usare le versioni tradotte per titolo, attributi e testo esteso.|
|**Mapping SKU**|Scegli come vuoi compilare il campo SKU in Shopify. Le opzioni supportate sono:<br> - **Nr. articolo** per usare il numero di articolo per prodotti e varianti.<br> - **Nr. articolo + Codice variante** per creare uno SKU concatenando i valori di due campi. Per gli articoli senza varianti, viene utilizzato solo il numero di articolo.<br>- **Nr. articolo fornitore** per usare il numero del fornitore dell'articolo definito nella **Scheda articolo** sia per i prodotti che per le varianti.<br> - **Codice a barre** per usare il tipo di codice a barre **Riferimento articolo**. Questa opzione rispetta le varianti.<br>Se **Aggiornamento prodotti Shopify consentito** è abilitato, le modifiche nel campo **Mapping SKU** saranno propagate a Shopify dopo la successiva sincronizzazione di tutti i prodotti e le varianti elencati nella pagina **Prodotti Shopify** per il punto vendita selezionato.|
|**Separatore campo SKU**|Definisci un separatore per l'opzione **Nr. articolo + Codice variante**.|
|**Inventario tracciato**| Scegli come il sistema dovrebbe popolare il campo **Tieni traccia dell'inventario** per i prodotti esportati su Shopify. È possibile aggiornare le informazioni sulla disponibilità da [!INCLUDE[prod_short](../includes/prod_short.md)] per i prodotti in Shopify il cui inventario di traccia è abilitato. Ulteriori informazioni nella sezione [Inventario](synchronize-items.md#sync-inventory-to-shopify).|
|**Criterio di inventario predefinito**|Scegli *Nega* per evitare stock negativo del lato Shopify. <br>Se **Aggiornamento prodotti Shopify consentito** è abilitato, le modifiche nel campo **Criterio di inventario predefinito** saranno propagate a Shopify dopo la successiva sincronizzazione di tutti i prodotti e le varianti elencati nella pagina **Prodotti Shopify** per il punto vendita selezionato.|
|**Può aggiornare prodotti Shopify**|Definisci in questo campo se [!INCLUDE[prod_short](../includes/prod_short.md)] può solo creare articoli o anche aggiornarli. Seleziona questa opzione se, dopo la sincronizzazione iniziale attivata dall'azione **Aggiungi articolo**, prevedi di aggiornare i prodotti manualmente utilizzando l'azione **Sincronizza prodotto** o la coda processi per gli aggiornamenti ricorrenti. Ricordati di selezionare **A Shopify** nel campo **Sincronizzazione articoli**.<br>**Può aggiornare Prodotti Shopify** non ha impatto sulla sincronizzazione di prezzi, immagini o livelli di inventario, che sono configurati da controlli indipendenti.<br>Se **Può aggiornare Prodotti Shopify** è abilitato, i seguenti campi Shopify verranno aggiornati sul prodotto e se necessario a livello di variante: **SKU**, **Codice a barre**, **Peso**. **Titolo**, **Tipo di prodotto**, **Fornitore** e **Descrizione** sul prodotto verrà aggiornata se i valori esportati non sono vuoti. Per la descrizione, ciò significa che è necessario abilitare uno qualsiasi degli interruttori **Sincronizza testo esteso articolo**, **Sincronizza testo marketing articolo** e **Sincronizza attributi articolo** e gli attributi, il testo esteso o di marketing devono avere valori. Se il prodotto utilizza varianti, la variante viene aggiunta o rimossa se necessario. <br>Se il prodotto su Shopify è configurato per utilizzare una matrice di varianti che combina due o più opzioni, il connettore Shopify non può creare varianti per quel prodotto. In [!INCLUDE[prod_short](../includes/prod_short.md)] non c'è modo di definire la matrice delle opzioni, ecco perché il connettore utilizza il **Codice variante** come unica opzione. Tuttavia Shopify si aspetta diverse opzioni e si rifiuta di creare una variante se mancano informazioni sulla seconda e altre opzioni. |
|**UdM come variante**| Scegli questa opzione se desideri che alcune opzioni siano esportate e importate come unità di misura anziché come varianti. Personalizza la pagina per aggiungere il campo. Per ulteriori informazioni, vedi la sezione [Unità di misura come variante](synchronize-items.md#unit-of-measure-as-variant).|
|**Nome opzione variante per UdM**| Utilizza questo campo con **UdM come variante** per specificare quale opzione contiene varianti che rappresentano unità di misura. Il valore predefinito è *Unità di misura*. Personalizza la pagina per aggiungere il campo.|

> [!NOTE]
> Quando desideri esportare molti articoli e varianti, alcuni potrebbero essere bloccati. Non puoi includere articoli e varianti bloccati nei calcoli dei prezzi, quindi non verranno esportati. Il connettore ignora questi articoli e varianti, quindi non è necessario filtrarli nella pagina di richiesta **Aggiungi articolo a Shopify**.

## <a name="advanced-details"></a>Dettagli avanzati

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Effetto delle SKU e dei codici a barre dei prodotti Shopify sulla mappatura e sulla creazione di articoli e varianti in Business Central

Quando i prodotti vengono importati da Shopify alle tabelle **Prodotti Shopify** e **Varianti Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] cerca di trovare i record esistenti.

Nella seguente tabella vengono illustrate le differenze tra le opzioni del campo **Mapping SKU**.

|Opzione|Effetto sul mapping|Effetto sulla creazione|
|------|-----------------|------------------|
|**Vuoto**|Il campo SKU non viene utilizzato nella routine di mapping degli articoli.|Nessun effetto sulla creazione dell'articolo.<br>Questa opzione impedisce la creazione di varianti. Nell'ordine cliente viene utilizzato solo l'articolo principale. Una variante può ancora essere mappata manualmente dalla pagina **Prodotto Shopify**.|
|**Nr. Articolo**|Scegli se il campo SKU contiene il numero dell'articolo.|Nessun effetto sulla creazione dell'articolo senza varianti. Per un articolo con varianti, ogni variante viene creata come articolo separato.<br>Se Shopify ha un prodotto con due varianti e i loro SKU sono "1000" e "2000", in [!INCLUDE[prod_short](../includes/prod_short.md)] il sistema creerà due elementi con i numeri "1000" e "2000".|
|**Codice variante**|Il campo SKU non viene utilizzato nella routine di mapping degli articoli.|Nessun effetto sulla creazione dell'articolo. Quando viene creata una variante articolo, il valore del campo SKU viene utilizzato come codice. Se lo SKU è vuoto, viene generato un codice utilizzando il campo **Prefisso variante**.|
|**Nr. articolo e codice variante**|Seleziona questa opzione se il campo SKU contiene un numero articolo e il codice della variante articolo separato dal valore definito nel campo **Separatore di campo SKU**.|Quando viene creato un articolo, la prima parte del valore del campo SKU viene utilizzata come **Nr.**. Se il campo SKU è vuoto, un numero di articolo viene generato utilizzando le serie di numeri definite nel campo **Codice modello articolo** o **Nr. articolo** della pagina **Setup magazzino**.<br>Quando viene creato un articolo, la funzione della variante utilizza la seconda parte del valore del campo SKU come **Codice**. Se il campo SKU è vuoto, viene generato un codice utilizzando il campo **Prefisso variante**.|
|**Nr. fornitore articolo**|Scegli se il campo SKU contiene il numero dell'articolo fornitore. In questo caso, il campo **Nr. articolo fornitore** non viene utilizzato nella pagina **Scheda articolo** e viene usato il **Nr. articolo fornitore** del **Catalogo fornitore articoli**. Se il record *Catalogo fornitori articolo* trovato contiene un codice variante, questo codice viene utilizzato per mappare la variante Shopify.|Se esiste un fornitore corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)], il valore SKU verrà utilizzato come **Nr. articolo fornitore** nella pagina **Scheda articolo** e come **Riferimento articolo** di tipo di *fornitore*. <br>Impedisce la creazione di varianti. È utile quando si desidera usare solo l'articolo principale nell'ordine cliente. Sarai ancora in grado di mappare una variante manualmente dalla pagina **Prodotto Shopify**.|
|**Codice a barre**|Scegli se il campo SKU contiene un codice a barre. Viene eseguita una ricerca tra **Riferimenti di articoli** di tipo *codice a barre*. Se il record Riferimento articolo trovato contiene un codice variante, questo verrà utilizzato per mappare la variante Shopify.|Nessun effetto sulla creazione dell'articolo. <br>Impedisce la creazione di varianti. È utile quando si desidera usare solo l'articolo principale nell'ordine cliente. Sarai ancora in grado di mappare una variante manualmente dalla pagina **Prodotto Shopify**.|

Nella seguente tabella viene illustrato l'effetto del campo **Codice a barre**.

|Effetto sul mapping|Effetto sulla creazione|
|-----------------|------------------|
|Viene eseguita una ricerca nei **Riferimenti di articoli** con un tipo di codice a barre per il valore nel campo **Codice a barre** in Shopify. Se il record Riferimento articolo trovato contiene un codice variante, questo verrà utilizzato per mappare la variante Shopify.|Il codice a barre viene salvato come **Riferimento articolo** per l'articolo e la variante articolo.|

> [!NOTE]  
> È possibile attivare il mapping per prodotti/varianti selezionati scegliendo **Prova Trova mapping prodotti** o per tutti i prodotti importati non mappati selezionando **Prova mapping ricerca**.

### <a name="fields-mapping-overview"></a>Panoramica mapping dei campi

|Shopify|Origine quando esportato da [!INCLUDE[prod_short](../includes/prod_short.md)]|Destinazione quando importato in [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Stato|In base al campo **Stato per i prodotti creati** nella **Scheda punto vendita Shopify**. Per ulteriori informazioni, vedi la sezione [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Non utilizzato.|
|Titolo | **Descrizione**. Se il codice della lingua è definito ed esiste la traduzione dell'articolo corrispondente, verrà utilizzata la traduzione dell'articolo al posto della descrizione.|**Descrizione**|
|Titolo variante | **Codice variante**.|**Descrizione** di variante|
|Descrizione|Combina testi estesi, testi di marketing e attributi se abiliti le opzioni corrispondenti nella scheda punto vendita Shopify. Rispetta il codice lingua.|Non utilizzato.|
|Titolo pagina SEO|Valore fisso: vuoto. Per ulteriori informazioni, vedi la sezione [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Non utilizzato.|
|Meta descrizione SEO|Valore fisso: vuoto. Per ulteriori informazioni, vedi la sezione [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Non utilizzato.|
|Elemento multimediale|**Immagine**. Scopri di più nella sezione [Sincronizzare le immagini degli articoli](synchronize-items.md#sync-item-images)|**Immagine**|
|Prezzo|Il calcolo del prezzo per il cliente finale include il prezzo unitario dell'articolo, il gruppo prezzi cliente, il gruppo sconto cliente e il codice valuta. Scopri di più nella sezione [Sincronizzare i prezzi](synchronize-items.md#sync-prices-with-shopify)|**Prezzo unitario**. Il prezzo viene importato solo negli elementi appena creati, ma non verrà aggiornato nelle sincronizzazioni successive.|
|Confronta prezzo|Il calcolo del prezzo senza sconto. Se il valore è inferiore o uguale a **Prezzo**, il connettore invia 0 (null) invece del valore effettivo.|Non utilizzato.|
|Costo per articolo|**Costo unitario**|**Costo unitario**. Il costo unitario viene importato solo negli elementi appena creati e non verrà aggiornato nelle sincronizzazioni successive.|
|SKU|Ulteriori informazioni in **Mapping SKU** nella sezione [Esportare articoli in Shopify](synchronize-items.md#export-items-to-shopify).|Per ulteriori informazioni vedi la sezione [Effetto delle SKU e dei codici a barre dei prodotti Shopify sulla mappatura e sulla creazione di articoli e varianti in Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Codice a barre|**Riferimenti di articoli** del tipo codice a barre.|**Riferimenti di articoli** del tipo codice a barre.|
|L'inventario sarà immagazzinato in| Dipende dalle ubicazioni dei punti vendita Shopify. Se il campo **Ubicazione prodotto predefinita** di **Servizi di evasione ordini di Business Central** è abilitato, le scorte vengono immagazzinate e spedite da **Servizi di evasione ordini di Business Central**. Altrimenti, vengono utilizzate l'ubicazione primaria o molteplici ubicazioni di Shopify. Per ulteriori informazioni, vedi [Due approcci per gestire le evasioni](synchronize-items.md#two-approaches-to-manage-fulfillments)| Non utilizzato.|
|Traccia quantità|In base al campo **Inventario tracciato** nella pagina **Scheda punto vendita di Shopify**. Ulteriori informazioni nella sezione [Inventario](synchronize-items.md#sync-inventory-to-shopify). Utilizzato solo quando esporti un prodotto per la prima volta.|Non utilizzato.|
|Continuare a vendere quando le scorte sono esaurite|In base al **Criterio di inventario predefinito** nella **Scheda del punto vendita Shopify**.|Non utilizzato.|
|Tipo|**Descrizione** di **Codice categoria articolo**. Se il tipo non è specificato in Shopify, viene aggiunto come tipo personalizzato.|**Codice categoria articolo**. Mapping per descrizione.|
|Fornitore|**Nome** del fornitore da **Nr. fornitore**|Mapping **Nr. fornitore** per nome.|
|Peso|**Peso lordo**.|Non utilizzato.|
|Imponibile|Valore fisso: abilitato.|Non utilizzato.|
|Codici imposta|**Codice gruppo imposte**. Rilevante solo per le imposte di vendita. Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|Non utilizzato.|

### <a name="tags"></a>Tag

Esamina i tag importati nella scheda Dettagli **Tag** nella pagina **Prodotto Shopify**. Nella stessa pagina per modificare i tag, scegli l'azione **Tag**.

Se l'opzione **A Shopify** è selezionata nel campo **Sincronizza articolo**, i tag assegnati vengono esportati in Shopify alla successiva sincronizzazione.

### <a name="unit-of-measure-as-variant"></a>Unità di misura come variante

Shopify non supporta più unità di misura. Se desideri vendere lo stesso prodotto come ad esempio pezzo e set e utilizzare prezzi o sconti diversi, devi creare unità di misura come varianti di prodotto.
Il connettore Shopify può essere configurato per esportare unità di misura come varianti o importare varianti come unità di misura.

Per abilitare questa funzionalità, utilizza i campi **UdM come variante** e **Nome opzione variante** in **Scheda punto vendita Shopify**. I campi sono nascosti per impostazione predefinita; utilizza la personalizzazione per aggiungerli alla pagina.

**Unità di misura come note sulla variante**

* Quando il prodotto viene importato in [!INCLUDE[prod_short](../includes/prod_short.md)], il connettore creerà unità di misura. Dovrai aggiornare **Quantità per unità di misura**.
* Quando si ha a che fare con la matrice delle varianti, ad esempio Colore e UdM e si desidera importare prodotti, è necessario impostare *N. articolo + Codice variante* nel campo **Mapping unità di stockkeeping** e assicurarsi che il campo **SKU** in Shopify abbia lo stesso valore per tutte le unità di misura e includa il numero di articolo e il codice variante.
* In [!INCLUDE[prod_short](../includes/prod_short.md)] la disponibilità viene calcolata per articolo/variante articolo e non per unità di misura. Ciò significa che la stessa disponibilità verrà assegnata a ciascuna variante che rappresenta l'unità di misura (rispetto a **Quantità per unità di misura**), il che può portare a casi in cui la quantità disponibile in Shopify non è accurata. Esempio: articolo venduto in pezzi (PZ) e scatola da 6. L'inventario in [!INCLUDE[prod_short](../includes/prod_short.md)] è di 6 pezzi. Articolo esportato in Shopify come prodotto con due varianti. Una volta eseguita la sincronizzazione dell'inventario, il livello dell'inventario in Shopify sarà 6 per la variante PZ e 1 per la variante SCATOLA. L'acquirente può esplorare solo il punto vendita e vedere che il prodotto è disponibile in entrambe le opzioni ed effettuare un ordine per 1 SCATOLA. L'acquirente successivo vedrà che la SCATOLA non è disponibile, ma ci sono ancora 6 PZ. Questo problema verrà risolto con la successiva sincronizzazione dell'inventario.

### <a name="url-and-preview-url"></a>URL e URL di anteprima

Un elemento aggiunto a Shopify o importato da Shopify potrebbe avere l'**URL** o **URL di anteprima** popolato. Il campo **URL** sarà vuoto se il prodotto non è pubblicato nel punto vendita online, ad esempio perché il suo stato è bozza. L'**URL** sarà vuoto se il punto vendita è protetto da password, ad esempio perché si tratta di un punto vendita di sviluppo. Nella maggior parte dei casi puoi utilizzare l'**URL di anteprima** per verificare come verrà visualizzato il prodotto una volta pubblicato.

## <a name="run-item-synchronization"></a>Esegui sincronizzazione articoli

La sincronizzazione completa o parziale degli articoli può essere eseguita in molti modi diversi.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Sincronizzazione iniziale degli articoli da Business Central a Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Aggiungi articoli**.
3. Nel campo **Codice punto vendita** immetti il primo codice. Se apri la finestra **Prodotto Shopify** dalla pagina **Scheda punto vendita**, il codice punto vendita verrà compilato automaticamente.
4. Se hai configurato la sincronizzazione dell'immagine e dell'inventario, puoi includerli nello stesso processo. Includerli nello stesso processo è utile per scenari demo o quando si ha a che fare con importi minori di dati.
5. Definisci i filtri sugli articoli come richiesto. Ad esempio, puoi filtrare per il numero articolo o il codice categoria articolo.
6. Selezionare **OK**.

Gli articoli risultanti vengono creati automaticamente in Shopify con i prezzi. A seconda delle scelte effettuate, potrebbero essere incluse immagini e livelli di inventario. L'operazione potrebbe richiedere del tempo se viene aggiunto un numero elevato di articoli.

In alternativa, puoi sincronizzare un articolo scegliendo l'azione **Aggiungi a Shopify** nella pagina **Scheda articolo**.  

> [!NOTE]  
> La sincronizzazione iniziale degli articoli da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify non considera le impostazioni **Sincronizza articolo** e **Aggiornamento prodotti Shopify consentito**. 

### <a name="sync-products-from-shopify-to-business-central"></a>Sincronizza i prodotti da Shopify a Business Central

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza prodotti**.

In alternativa, utilizza l'azione **Sincronizza prodotti** sulla pagina **Prodotti Shopify** o cerca il processo batch **Sincronizzare prodotti**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Ulteriori informazioni su [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products"></a>Aggiornamenti ad hoc di prodotti Shopify

Quando i record vengono aggiornati nella tabella **Prodotto Shopify**, le seguenti modifiche vengono sincronizzate con Shopify.

Aggiorna:

* **Stato** - puoi scegliere tra attivo, archiviato o bozza.
* **Titolo SEO**
* **Descrizione SEO**

Eliminazione:

In base al valore in **Azione per prodotti rimossi** nella pagina **Scheda punto vendita Shopify**, il prodotto viene aggiornato in Shopify quando il record viene eliminato dalla pagina **Prodotti Shopify**.

* **Vuoto**: non succederà nulla. Se necessario, esegui l'azione richiesta da **Amministratore Shopify**.
* **Stato in bozza**: lo stato del prodotto in Shopify è impostato per *Bozza*.
* **Stato su Archiviato**: il prodotto è archiviato in Shopify.

## <a name="sync-item-images"></a>Sincronizza immagini articolo

La sincronizzazione delle immagini può essere configurata per gli articoli sincronizzati. Scegliere una delle seguenti opzioni:

* **Disattivata**: la sincronizzazione delle immagini è disattivata.
* **A Shopify**: le immagini degli articoli vengono esportate in Shopify.
* **Da Shopify**: le immagini da Shopify vengono importate in [!INCLUDE[prod_short](../includes/prod_short.md)].

La sincronizzazione delle immagini può essere inizializzata nei due modi descritti di seguito.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Sincronizzare le immagini dei prodotti dalla pagina del punto vendita Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare le immagini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza immagini prodotto**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Sincronizzare le immagini dei prodotti dalla pagina dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza immagini prodotto**.

### <a name="image-synchronization-remarks"></a>Osservazioni sulla sincronizzazione delle immagini

* Quando esporti immagini da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, le immagini sostituiscono quelle esportate in precedenza. Le immagini precedenti non sono più disponibili.
* Se elimini un'immagine in [!INCLUDE[prod_short](../includes/prod_short.md)], l'immagine in Shopify non viene eliminata. Dovrai eliminare manualmente le vecchie immagini in **Amministrazione Shopify**.
* Le immagini esportate in Shopify devono essere conformi ai requisiti Shopify. Altrimenti, non puoi importarle. Per ulteriori informazioni sui requisiti multimediali, vai a [Tipi di supporto del prodotto su help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Sincronizzare i prezzi con Shopify

Puoi gestire il processo di esportazione dei prezzi utilizzando queste impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Gruppo prezzi cliente**|Determina il prezzo di un articolo in Shopify. Viene preso il prezzo di vendita di questo gruppo di prezzi cliente. Se non viene specificato alcun gruppo, viene utilizzato il prezzo della scheda articolo.|
|**Categoria sconto clienti**|Determina lo sconto da usare per calcolare il prezzo di un articolo in Shopify. I prezzi scontati sono archiviati nel campo **Prezzo** e il prezzo intero è archiviato nel campo **Confronta prezzo**.|
|**Consenti sconto riga**|Specifica se consentire lo sconto riga nel calcolo dei prezzi per Shopify. Questa impostazione si applica solo ai prezzi dell'articolo. I prezzi per il gruppo di prezzi cliente hanno propri interruttori sulle righe.|
|**Prezzi IVA inclusa**|Specifica se i calcoli del prezzo per Shopify includono l'IVA. Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|
|**Cat. reg. business IVA**|Specifica la categoria registrazione business IVA che viene utilizzata per calcolare i prezzi in Shopify. Questo deve essere il gruppo che utilizzi per i clienti nazionali. Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|
|**Codice valuta**|Immetti un Codice valuta solo se il tuo negozio online utilizza una valuta diversa dalla valuta locale. La valuta specificata deve avere i tassi di cambio configurati. Se il tuo negozio online utilizza la stessa valuta di [!INCLUDE[prod_short](../includes/prod_short.md)], lascia il campo vuoto.|

Puoi esportare i prezzi per gli articoli sincronizzati nei due modi descritti di seguito.

### <a name="sync-prices-from-the-shopify-products-page"></a>Sincronizzare i prezzi dalla pagina dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza i prezzi con Shopify**.

### <a name="price-calculation-remarks"></a>Nore sul calcolo del prezzo

* Quando si determina un prezzo, [!INCLUDE[prod_short](../includes/prod_short.md)] utilizza la logica del "prezzo più basso". Tuttavia, la logica del prezzo più basso ignora il prezzo unitario definito nella scheda articolo se un prezzo è definito nel gruppo di prezzi. Questo è vero anche se il prezzo unitario del prezzo della scheda articolo è inferiore.
* Per calcolare i prezzi, il connettore crea un'offerta di vendita temporanea per l'articolo con una quantità pari a 1 e utilizza la logica di calcolo dei prezzi standard. Vengono utilizzati solo i prezzi e gli sconti applicabili per la quantità 1. Non puoi esportare prezzi o sconti diversi in base alla quantità.
* Il connettore invia una richiesta per aggiornare i prezzi Shopify se il prezzo in [!INCLUDE[prod_short](../includes/prod_short.md)] è cambiato. Ad esempio, se hai sincronizzato prodotti e prezzi e poi modificato il prezzo in Shopify, scegliendo l'azione **Sincronizza prezzi in Shopify** non avrà alcun impatto sul prezzo in Shopify poiché il nuovo prezzo calcolato dal connettore è lo stesso del prezzo memorizzato nella variante Shopify della sincronizzazione precedente. Il campo **Confronta prezzo** viene aggiornato solo se il prezzo principale è cambiato.

## <a name="sync-inventory-to-shopify"></a>Sincronizzare l'inventario con Shopify

La sincronizzazione dell'inventario può essere configurata per gli articoli già sincronizzati. Ci sono due condizioni che devono essere soddisfatte:

1. Il monitoraggio dell'inventario deve essere abilitato per un prodotto in Shopify. Se gli elementi vengono esportati in Shopify, considera l'abilitazione dell'opzione **Inventario tracciato** nella pagina **Punto vendita Shopify**. Per ulteriori informazioni, vedi la sezione [Esportare articoli su Shopify](synchronize-items.md#export-items-to-shopify)
2. La sincronizzazione dell'inventario deve essere abilitata per **Posizioni Shopify**.

### <a name="to-enable-inventory-sync"></a>Per abilitare la sincronizzazione dell'inventario

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare l'inventario per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Posizioni** per aprire **Posizioni punto vendita Shopify**.
4. Scegli l'azione **Recupera posizioni Shopify** per importare tutte le posizioni definite in Shopify. Puoi trovarli nelle impostazioni [**Posizioni**](https://www.shopify.com/admin/settings/locations) in **Amministratore Shopify**.
5. Nel campo **Filtro posizione**, aggiungi posizioni, se desideri includere l'inventario solo da posizioni specifiche. Puoi quindi immettere *EST|OVEST*, in modo che l'inventario solo da queste due posizioni sia disponibile per la vendita tramite il negozio online.
6. Seleziona il metodo di calcolo delle scorte da utilizzare per le ubicazioni Shopify selezionate.
7. Abilita **Ubicazione prodotto predefinita** se desideri che l'ubicazione venga utilizzata per la creazione di record di inventario e partecipi alla sincronizzazione dell'inventario.

Puoi inizializzare le sincronizzazione dell'inventario in due modi descritti di seguito.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Sincronizzare l'inventario dalla pagina del punto vendita Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare l'inventario per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza inventario**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Sincronizzare l'inventario dalla pagina dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza inventario**.

### <a name="inventory-remarks"></a>Note sull'inventario

* Esistono due metodi standard di calcolo delle scorte: **Saldo disponibile previsto alla data** e **Inventario gratuito (non impegnato)**. Con l'estensibilità, puoi aggiungere più opzioni. Per saperne di più sull'estensibilità, vai a [Esempi](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Puoi esaminare le informazioni sulle scorte ricevute da Shopify nella pagina **Scheda dettaglio Inventario Shopify**. In questa Scheda dettaglio, ottieni una panoramica delle scorte Shopify e l'ultimo inventario calcolato in [!INCLUDE[prod_short](../includes/prod_short.md)]. C'è un record per posizione.
* Se le informazioni sulle scorte in Shopify sono diverse dal **Saldo disponibile previsto** in[!INCLUDE[prod_short](../includes/prod_short.md)], le scorte verranno aggiornate in Shopify.
* Quando aggiungi una nuova ubicazione in Shopify, devi anche aggiungere i relativi record di inventario. Shopify non lo fa automaticamente per i prodotti e le varianti esistenti e il connettore non sincronizza i livelli di inventario per tali articoli nella nuova ubicazione. Per ulteriori informazioni, vai a [Assegnazione delle scorte alle ubicazioni](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* **Servizi di evasione di Business Central** e le ubicazioni normali sono entrambi supportati e utilizzabili per la spedizione e l'inventario.

#### <a name="example-of-calculation-of-projected-available-balance"></a>Esempio di calcolo del saldo disponibile previsto

Sono disponibili 10 pezzi dell'articolo A e due ordini di vendita in sospeso. Uno per lunedì con quantità *Uno* e uno per giovedì con quantità *Due*. A seconda di quando sincronizzi l'inventario, il sistema aggiornerà il livello delle scorte in Shopify con quantità diverse:

|Quando viene eseguita la sincronizzazione dell'inventario|Valore utilizzato per aggiornare il livello delle scorte|Commento|
|------|-----------------|-----------------|
|Martedì|9|Inventario 10 meno l'ordine di vendita impostato per la spedizione lunedì|
|Venerdì|7|Inventario 10 meno entrambi gli ordini di vendita|

### <a name="two-approaches-to-manage-fulfillments"></a>Due approcci per gestire le evasioni

Esistono due modi per gestire l'evasione in Shopify:

* Evasione Shopify "integrata" e monitoraggio dell'inventario
* Evasione di terze parti e monitoraggio dell'inventario

L'inventario per ciascun prodotto in Shopify può essere immagazzinato tramite Shopify o 3PL.

Se utilizzi l'evasione Shopify, puoi anche definire più ubicazioni in Shopify. Una volta creato l'ordine, Shopify seleziona l'ubicazione in base alla disponibilità e alla priorità. Puoi anche specificare in quali ubicazioni intendi monitorare un prodotto specifico, ad esempio non vendere mai dall'ubicazione *ShowRoom*.

Se utilizzi 3PL, la gestione fisica viene gestita dal fornitore 3PL, quindi le ubicazioni non sono necessarie. Per 3PL il campo SKU diventa obbligatorio.

Quando decidi in quale ubicazione tenere traccia dell'articolo, Shopify crea record nella tabella **Livelli di inventario** , che può essere aggiornata manualmente con la disponibilità di inventario.

Il connettore supporta entrambe le modalità. Può inviare l'inventario a più ubicazioni Shopify o funzionare come servizio di evasione.

Dalla prospettiva di [!INCLUDE[prod_short](../includes/prod_short.md)] quando crei un articolo e desideri inviarlo a Shopify devi anche:

* Utilizza l'interruttore **Ubicazione prodotto predefinita** per specificare se questo articolo sarà evaso tramite l'evasione Shopify o tramite 3PL. È sempre disponibile il **servizio di evasione Business Central**, ma possono essere presenti più servizi di evasione se vengono installate più app. Puoi abilitare **Ubicazione prodotto predefinita** solo in un record se desideri utilizzare il servizio di evasione. 
* Utilizzare l'interruttore **Ubicazione prodotto predefinita** per specificare quali ubicazioni desideri utilizzare per tenere traccia dell'inventario. Puoi attivare **Ubicazione prodotto predefinita** per più ubicazioni in cui **Servizio di evasione** è disabilitato. Tieni presente che l'inventario verrà sempre monitorato per l'ubicazione principale.

#### <a name="whats-the-difference"></a>Qual è la differenza?

L'evasione Shopify è utile durante l'utilizzo di Shopify POS e sono presenti più punti vendita fisici. Desideri che i dipendenti del punto vendita fisico siano a conoscenza del relativo inventario corrente. In questo caso crei più ubicazioni in Shopify, più ubicazioni in [!INCLUDE[prod_short](../includes/prod_short.md)] e attivi **Ubicazione prodotto predefinita** per tutte queste ubicazioni.  

Se la logistica viene gestita in [!INCLUDE[prod_short](../includes/prod_short.md)] dove è possibile avere tutte le ubicazioni necessarie che rappresentano i centri di distribuzione, non si creano ubicazioni in Shopify, il connettore  crea automaticamente i servizi di evasione di Business Central ed è possibile collegare l'inventario tramite filtri di ubicazione da diverse ubicazioni a un record di servizi di evasione. Di conseguenza, in  Shopify non ci sono informazioni sulla provenienza della merce, ma solo informazioni di tracciabilità, mentre in [!INCLUDE[prod_short](../includes/prod_short.md)] puoi selezionare in base alla disponibilità e alla vicinanza alla destinazione.

#### <a name="example-of-using-default-product-location-toggle"></a>Esempio di utilizzo dell'interruttore Ubicazione prodotto predefinita

Dopo aver scelto l'azione **Ottieni ubicazioni Shopify** nella pagina **Ubicazioni Shopify** vengono visualizzate le seguenti ubicazioni:

|Nome|Servizio di evasione|Primario|
|------|-----------------|-----------------|
|Principale| |**Sì**|
|Secondo| | |
|Servizio di evasione di Business Central|**Sì**| |

Esaminiamo l'impatto dell'attivazione dell'interruttore Ubicazione prodotto predefinita:

|Il nome delle ubicazioni in cui l'interruttore Ubicazione prodotto predefinita è attivato|Impatto sul modo in cui viene creato il prodotto in Shopify|
|------|-----------------|
|Principale| L'inventario sarà immagazzinato in: Più ubicazioni; Ubicazioni selezionate: Principale (primario) |
|Principale e Secondo| L'inventario sarà immagazzinato in: Più ubicazioni; Ubicazioni selezionate: Principale e Secondo |
|Servizio di evasione di Business Central|L'inventario sarà immagazzinato in Servizio di evasione di Business Central; Ubicazioni selezionate: (App) Servizio di evasione di Business Central|
|Servizio di evasione di Business Central e Principale| Errore: non è possibile utilizzare le ubicazioni Shopify standard con le ubicazioni del servizio di evasione|

## <a name="see-also"></a>Vedere anche

[Iniziare a usare il connettore per Shopify](get-started.md)  
