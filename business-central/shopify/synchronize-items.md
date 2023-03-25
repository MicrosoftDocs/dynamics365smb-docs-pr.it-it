---
title: Sincronizzare articoli e inventario
description: Configurare ed eseguire sincronizzazioni di articoli tra Shopify e Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
---

# Sincronizzare articoli e inventario

Gli **Articoli** in [!INCLUDE[prod_short](../includes/prod_short.md)] sono equivalenti ai *prodotti* in Shopify e includono beni fisici, download digitali, servizi e buoni regalo che puoi vendere. Ci sono due ragioni principali per sincronizzare gli elementi:

1. La gestione dei dati viene eseguita principalmente in [!INCLUDE[prod_short](../includes/prod_short.md)]. Devi esportare tutti o alcuni dati da lì in Shopify e renderli visibili. Puoi esportare il nome dell'articolo, la descrizione, l'immagine, i prezzi, la disponibilità, le varianti, i dettagli del fornitore e il codice a barre. Una volta esportati, puoi rivedere gli articoli o renderli immediatamente visibili.
2. Quando un ordine di Shopify viene importato, le informazioni sugli articoli sono essenziali per l'ulteriore elaborazione del documento in [!INCLUDE[prod_short](../includes/prod_short.md)].

I due scenari precedenti sono sempre abilitati.

Un terzo scenario è gestire i dati in Shopify e importare gli articoli in blocco in [!INCLUDE[prod_short](../includes/prod_short.md)]. Questo scenario può essere utile per gli eventi di migrazione dei dati, quando un punto vendita online esistente deve essere collegato a uno nuovo ambiente [!INCLUDE[prod_short](../includes/prod_short.md)].

## Definire le sincronizzazioni degli articoli

1. Scegli l'icona di ricerca a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punto vendita Shopify**. Apri il punto vendita per il quale desideri configurare la sincronizzazione degli articoli.
2. Dal campo **Sincronizza articolo**, seleziona l'opzione richiesta.

   Nella seguente tabella vengono descritte le opzioni.

|Opzione|Descrizione|
|------|-----------|
|**Vuoto**| I prodotti vengono importati insieme all'importazione degli ordini. I prodotti vengono esportati in Shopify se un utente esegue l'azione **Aggiungi articolo** dalla pagina **Prodotti Shopify**. Questa opzione è il processo predefinito.|
|**A Shopify**| Seleziona questa opzione se, dopo la sincronizzazione iniziale attivata dall'azione **Aggiungi articolo**, prevedi di aggiornare i prodotti manualmente utilizzando l'azione **Sincronizza prodotto** o la coda processi per gli aggiornamenti ricorrenti. Ricordati di abilitare il campo **Può aggiornare il prodotto Shopify**. Se non è abilitato, è uguale all'opzione **Vuoto** (processo predefinito). Per ulteriori informazioni, vedi la sezione [Esportare articoli su Shopify](synchronize-items.md#export-items-to-shopify)|
|**Da Shopify**| Scegli questa opzione se prevedi di importare prodotti da Shopify in blocco, manualmente con l'azione **Sincronizza prodotto** o la coda processi per gli aggiornamenti ricorrenti. Per ulteriori informazioni, vedi la sezione [Importare articoli da Shopify](synchronize-items.md#import-items-from-shopify)|

## Importare articoli da Shopify

Importa gli articoli da Shopify in blocco o insieme agli ordini per aggiungerli alle tabelle **Prodotto Shopify** e **Variante Shopify**. Quindi mappa i prodotti e le varianti importati ad Articoli e varianti in [!INCLUDE[prod_short](../includes/prod_short.md)]. Gestisci il processo utilizzando le seguenti impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Crea automaticamente articoli sconosciuti**|Quando prodotti e varianti Shopify vengono importati in [!INCLUDE[prod_short](../includes/prod_short.md)], la funzione [!INCLUDE[prod_short](../includes/prod_short.md)] cerca sempre di trovare prima il record corrispondente nell'elenco degli elementi. **Mapping SKU** influisce sul modo in cui viene eseguita la corrispondenza e crea un nuovo articolo e/o una variante di articolo. Abilita questa opzione se desideri creare un nuovo articolo o quando non esiste un record corrispondente. Il nuovo articolo viene creato utilizzando i dati importati e il **Codice modello articolo**. Se questa opzione non è abilitata, dovrai creare un articolo manualmente e usare l'azione **Esegui mapping prodotto** nella pagina **Prodotti Shopify**.|
|**Codice modello articolo**|Utilizzalo insieme all'interruttore **Crea automaticamente articoli sconosciuti**.<br>Scegli il modello che vuoi usare per gli articoli creati automaticamente.|
|**Mapping SKU**|Scegli come vuoi usare il valore **SKU** importato da Shopify durante il mapping la creazione dell'articolo/variante. Per ulteriori informazioni vedi la sezione [Effetto delle SKU e dei codici a barre dei prodotti Shopify sulla mappatura e sulla creazione di articoli e varianti in Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Separatore campo SKU**|Usalo insieme a **Mapping SKU** impostato sull'opzione **[Nr. articolo e codice variante](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Definisci un separatore da usare per dividere la SKU.<br>Se in Shopify crei la variante con SKU "1000/001", digita "/" nel campo **Separatore di campo SKU** per ottenere il numero dell'articolo [!INCLUDE[prod_short](../includes/prod_short.md)] come "1000" e il codice della variante articolo come "001".|
|**Prefisso variante**|Usato insieme a **Mapping SKU** impostato sull'opzione **Codice variante** o **Nr. articolo + Codice variante** come strategia di fallback quando lo SKU proveniente da Shopify è vuoto.<br>Se vuoi creare la variante articolo in [!INCLUDE[prod_short](../includes/prod_short.md)] automaticamente, dovrai inserire un valore in **Codice**. Per impostazione predefinita, viene utilizzato il valore definito nel campo SKU importato da Shopify. Tuttavia, se lo SKU è vuoto, genererà codice che inizia con il prefisso della variante definito e "001".|
|**Shopify può aggiornare l'articolo**|Scegli questa opzione se desideri aggiornare automaticamente gli articoli e/o le varianti.|

### Effetto delle SKU e dei codici a barre dei prodotti Shopify sulla mappatura e sulla creazione di articoli e varianti in Business Central

Quando i prodotti vengono importati da Shopify alle tabelle **Prodotti Shopify** e **Varianti Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] cerca di trovare i record esistenti.

Nella seguente tabella vengono illustrate le differenze tra le opzioni del campo **Mapping SKU**.

|Opzione|Effetto sul mapping|Effetto sulla creazione|
|------|-----------------|------------------|
|**Vuoto**|Il campo SKU non viene utilizzato nella routine di mapping degli articoli.|Nessun effetto sulla creazione dell'articolo.<br>Questa opzione impedisce la creazione di varianti. Nell'ordine cliente viene utilizzato solo l'articolo principale. Una variante può ancora essere mappata manualmente dalla pagina **Prodotto Shopify**.|
|**Nr. Articolo**|Scegli se il campo SKU contiene il numero dell'articolo|Nessun effetto sulla creazione dell'articolo senza varianti. Per un articolo con varianti, ogni variante viene creata come articolo separato.<br>Se Shopify ha un prodotto con due varianti e i loro SKU sono "1000" e "2000", in [!INCLUDE[prod_short](../includes/prod_short.md)] il sistema creerà due elementi con i numeri "1000" e "2000".|
|**Codice variante**|Il campo SKU non viene utilizzato nella routine di mapping degli articoli.|Nessun effetto sulla creazione dell'articolo. Quando viene creata una variante di articolo, il valore del campo SKU viene utilizzato come codice. Se lo SKU è vuoto, viene generato un codice utilizzando il campo **Prefisso variante**.|
|**Nr. articolo e codice variante**|Seleziona questa opzione se il campo SKU contiene un numero articolo e il codice della variante dell'articolo separato dal valore definito nel campo **Separatore di campo SKU**.|Quando viene creato un articolo, la prima parte del valore del campo SKU viene utilizzata come **Nr.**. Se il campo SKU è vuoto, un numero di articolo viene generato utilizzando le serie di numeri definite nel campo **Codice modello articolo** o **Nr. articolo** della pagina **Setup magazzino**.<br>Quando viene creato un articolo, la funzione della variante utilizza la seconda parte del valore del campo SKU come **Codice**. Se il campo SKU è vuoto, viene generato un codice utilizzando il campo **Prefisso variante**.|
|**Nr. fornitore articolo**|Scegli se il campo SKU contiene il numero dell'articolo fornitore. In questo caso, il campo **Nr. articolo fornitore** non viene utilizzato nella pagina **Scheda articolo** e viene usato il **Nr. articolo fornitore** del **Catalogo fornitore articoli**. Se il record *Catalogo fornitori articolo* trovato contiene un codice variante, questo codice viene utilizzato per mappare la variante Shopify.|Se esiste un fornitore corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)], il valore SKU verrà utilizzato come **Nr. articolo fornitore** nella pagina **Scheda articolo** e come **Riferimento articolo** di tipo di *fornitore*. <br>Impedisce la creazione di varianti. È utile quando si desidera usare solo l'articolo principale nell'ordine cliente. Sarai ancora in grado di mappare una variante manualmente dalla pagina **Prodotto Shopify**.|
|**Codice a barre**|Scegli se il campo SKU contiene un codice a barre. Viene eseguita una ricerca tra **Riferimenti di articoli** di tipo *codice a barre*. Se il record Riferimento articolo trovato contiene un codice variante, questo verrà utilizzato per mappare la variante Shopify.|Nessun effetto sulla creazione dell'articolo. <br>Impedisce la creazione di varianti. È utile quando si desidera usare solo l'articolo principale nell'ordine cliente. Sarai ancora in grado di mappare una variante manualmente dalla pagina **Prodotto Shopify**.|

Nella seguente tabella viene illustrato l'effetto del campo **Codice a barre**.

|Effetto sul mapping|Effetto sulla creazione|
|-----------------|------------------|
|Viene eseguita una ricerca nei **Riferimenti di articoli** con un tipo di codice a barre per il valore nel campo **Codice a barre** in Shopify. Se il record Riferimento articolo trovato contiene un codice variante, questo verrà utilizzato per mappare la variante Shopify.|Il codice a barre viene salvato come **Riferimento articolo** per l'articolo e la variante di articolo.|

> [!NOTE]  
> È possibile attivare il mapping per prodotti/varianti selezionati scegliendo **Prova Trova mapping prodotti** o per tutti i prodotti importati non mappati selezionando **Prova mapping ricerca**.

## Esportare articoli in Shopify

Scegli gli elementi dal tuo elenco di articoli da esportare su Shopify. Usa l'azione **Aggiungi articolo** nella pagina **Prodotti Shopify** per aggiungere articoli all'elenco prodotti Shopify. 

>[!IMPORTANT]
>Il prodotto verrà aggiunto solo al canale di vendita **Negozio online**. Devi pubblicare prodotti su altri canali di vendita, come Shopify POS, da Shopify.

Puoi gestire il processo di esportazione degli articoli utilizzando queste impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Gruppo prezzi cliente**|Determina il prezzo di un articolo in Shopify. Viene preso il prezzo di vendita di questo gruppo di prezzi cliente. Se non viene inserito alcun gruppo, viene utilizzato il prezzo della scheda articolo.|
|**Categoria sconto clienti**|Determina lo sconto da usare per calcolare il prezzo di un articolo in Shopify. I prezzi scontati sono archiviati nel campo **Prezzo** e il prezzo intero è archiviato nel campo **Confronta prezzo**.|
|**Sincronizza testo esteso articolo**|Seleziona questo campo per sincronizzare il testo esteso dell'articolo. Dal momento che verrà aggiunto al campo *Descrizione*, può contenere codice HTML. |
|**Sincronizza attributi articolo**|Seleziona questo campo per sincronizzare gli attributi dell'articolo. Gli attributi sono formattati come una tabella e inclusi nel campo *Descrizione* di Shopify.|
|**Codice lingua**|Seleziona questo campo se desideri usare le versioni tradotte per titolo, attributi e testo esteso.|
|**Mapping SKU**|Scegli come vuoi compilare il campo SKU in Shopify. Le opzioni supportate sono:<br> - **Nr. articolo** per usare il numero di articolo per prodotti e varianti.<br> - **Nr. articolo + Codice variante** per creare uno SKU concatenando i valori di due campi. Per gli articoli senza varianti, viene utilizzato solo il numero di articolo.<br>- **Nr. articolo fornitore** per usare il numero del fornitore dell'articolo definito nella *Scheda articolo* sia per i prodotti che per le varianti.<br> - **Codice a barre** per usare il tipo di codice a barre **Riferimento articolo**. Questa opzione rispetta le varianti.|
|**Separatore campo SKU**|Definisci un separatore per l'opzione **Nr. articolo + Codice variante**.|
|**Inventario tracciato**| Scegli come il sistema dovrebbe popolare il campo **Tieni traccia dell'inventario** per i prodotti esportati su Shopify. È possibile aggiornare le informazioni sulla disponibilità da [!INCLUDE[prod_short](../includes/prod_short.md)] per i prodotti in Shopify il cui inventario di traccia è abilitato. Ulteriori informazioni nella sezione [Inventario](synchronize-items.md#sync-inventory-to-shopify).|
|**Criterio di inventario predefinito**|Scegli *Nega* per evitare stock negativo del lato Shopify.|
|**Può aggiornare prodotti Shopify**|Definisci in questo campo se [!INCLUDE[prod_short](../includes/prod_short.md)] può solo creare articoli o anche aggiornarli. Seleziona questa opzione se, dopo la sincronizzazione iniziale attivata dall'azione **Aggiungi articolo**, prevedi di aggiornare i prodotti manualmente utilizzando l'azione **Sincronizza prodotto** o la coda processi per gli aggiornamenti ricorrenti. Ricordati di selezionare **A Shopify** nel campo **Sincronizzazione articoli**.|
|**Codice modello cliente**|Scegli il modello predefinito da usare durante il calcolo del prezzo. Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|

### Panoramica mapping dei campi

|Shopify|Origine quando esportato da [!INCLUDE[prod_short](../includes/prod_short.md)]|Destinazione quando importato in [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Stato|In base al campo **Stato per i prodotti creati** nella **Scheda punto vendita Shopify**. Per ulteriori informazioni, vedi la sezione [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Non utilizzato.|
|Titolo | **Descrizione**. Se il codice della lingua è definito ed esiste la traduzione dell'articolo corrispondente, verrà utilizzata la traduzione dell'articolo al posto della descrizione.|**descrizione**|
|Descrizione|Combina testi e attributi estesi se le opzioni corrispondenti nella scheda punto vendita Shopify sono abilitate. Rispetta il codice lingua.|Non utilizzato.|
|Titolo pagina SEO|Valore fisso: vuoto. Per ulteriori informazioni, vedi la sezione [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Non utilizzato.|
|Meta descrizione SEO|Valore fisso: vuoto. Per ulteriori informazioni, vedi la sezione [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Non utilizzato.|
|Elemento multimediale|**Immagine**. Scopri di più nella sezione [Sincronizzare le immagini degli articoli](synchronize-items.md#sync-item-images)|**Immagine**|
|Prezzo|Il calcolo del prezzo per il cliente finale include il gruppo prezzi articolo, il gruppo sconto articolo, il codice valuta e il codice modello cliente.|**Prezzo Unitario**|
|Confronta prezzo|Il calcolo del prezzo senza sconto include il gruppo prezzi articolo, il gruppo sconto articolo, il codice valuta e il codice modello cliente.|Non utilizzato.|
|Costo per articolo|**Costo unitario**|**Costo unitario**|
|SKU|Ulteriori informazioni in **Mapping SKU** nella sezione [Esportare articoli in Shopify](synchronize-items.md#export-items-to-shopify).|Per ulteriori informazioni vedi la sezione [Effetto delle SKU e dei codici a barre dei prodotti Shopify sulla mappatura e sulla creazione di articoli e varianti in Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Codice a barre|**Riferimenti di articoli** del tipo codice a barre.|**Riferimenti di articoli** del tipo codice a barre.|
|Traccia quantità|In base al campo **Inventario tracciato** nella pagina **Scheda punto vendita di Shopify**. Ulteriori informazioni nella sezione [Inventario](synchronize-items.md#sync-inventory-to-shopify).|Non utilizzato.|
|Continuare a vendere quando le scorte sono esaurite|In base al **Criterio di inventario predefinito** nella **Scheda del punto vendita Shopify**. Non importato.|Non utilizzato.|
|Tipo|**Descrizione** di **Codice categoria articolo**. Se il tipo non è specificato in Shopify, viene aggiunto come tipo personalizzato.|**Codice categoria articolo**. Mapping per descrizione.|
|Fornitore|**Nome** del fornitore da **Nr. fornitore**|Mapping **Nr. fornitore** per nome.|
|Peso|**Peso lordo**.|Non utilizzato.|
|Imponibile|Valore fisso: abilitato.|Non utilizzato.|
|Codici imposta|**Codice gruppo imposte**. Rilevante solo per le imposte di vendita. Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|Non utilizzato.|

### Tag

Esamina i tag importati nella scheda Dettagli **Tag** nella pagina **Prodotto Shopify**. Nella stessa pagina per modificare i tag, scegli l'azione **Tag**.
Se l'opzione **A Shopify** è selezionata nel campo **Sincronizza articolo**, i tag assegnati vengono esportati in Shopify alla successiva sincronizzazione.

## Esegui sincronizzazione articoli

La sincronizzazione completa o parziale degli articoli può essere eseguita in molti modi diversi.

### Sincronizzazione iniziale degli articoli da Business Central a Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Aggiungi articoli**.
3. Nel campo **Codice punto vendita** immetti il primo codice. Se apri la finestra **Prodotto Shopify** dalla pagina **Scheda punto vendita**, il codice punto vendita verrà compilato automaticamente.
4. Se hai configurato la sincronizzazione dell'immagine e dell'inventario, puoi includerli nello stesso processo. Includerli nello stesso processo è utile per scenari demo o quando si ha a che fare con quantità minori di dati. 
5. Definisci i filtri sugli articoli come richiesto. Ad esempio, puoi filtrare per il numero articolo o il codice categoria articolo.
6. Selezionare **OK**.

Gli articoli risultanti vengono creati automaticamente in Shopify con i prezzi. A seconda delle scelte effettuate, potrebbero essere incluse immagini e livelli di inventario. L'operazione potrebbe richiedere del tempo se viene aggiunto un numero elevato di articoli.

### Sincronizza i prodotti da Shopify a Business Central

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza prodotti**.

In alternativa, utilizza l'azione **Sincronizza prodotti** sulla pagina **Prodotti Shopify** o cerca il processo batch **Sincronizzare prodotti**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Ulteriori informazioni su [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

### Aggiornamenti ad hoc di prodotti Shopify

Quando i record vengono aggiornati nella tabella **Prodotto Shopify**, le seguenti modifiche vengono sincronizzate con Shopify.

Aggiorna:

* **Stato** - puoi scegliere tra attivo, archiviato o bozza.
* **Titolo SEO**
* **Descrizione SEO**

Eliminazione:

In base al valore in **Azione per prodotti rimossi** nella pagina **Scheda punto vendita Shopify**, il prodotto viene aggiornato in Shopify quando il record viene eliminato dalla pagina **Prodotti Shopify**.

* **Vuoto** - non succederà nulla. Se necessario, esegui l'azione richiesta da **Amministratore Shopify**.
* **Stato in bozza** - lo stato del prodotto in Shopify è impostato per *Bozza*.
* **Stato su Archiviato** - il prodotto è archiviato in Shopify.

## Sincronizza immagini articolo

La sincronizzazione delle immagini può essere configurata per gli articoli sincronizzati. Scegliere una delle seguenti opzioni:

* **Disattivata**: la sincronizzazione delle immagini è disattivata.
* **A Shopify** - le immagini degli articoli vengono esportate in Shopify.
* **Da Shopify** - le immagini da Shopify vengono importate in [!INCLUDE[prod_short](../includes/prod_short.md)].

La sincronizzazione delle immagini può essere inizializzata nei due modi descritti di seguito.

### Sincronizzare le immagini dei prodotti dalla pagina del punto vendita Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare le immagini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza immagini prodotto**.

### Sincronizzare le immagini dei prodotti dalla pagina dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza immagini prodotto**.

### Osservazioni sulla sincronizzazione delle immagini

* Quando si esportano immagini da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, vengono aggiunte le nuove immagini a Shopify, mantenendo intatte le vecchie immagini. Se un'immagine viene aggiornata in [!INCLUDE[prod_short](../includes/prod_short.md)], dovrai eliminare le vecchie immagini in **Amministratore Shopify**.
* Le immagini esportate in Shopify che non rispettano i requisiti definiti da Shopify non verranno importate. Per ulteriori informazioni, vedi [Tipi di supporto del prodotto su help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## Sincronizzare i prezzi con Shopify

I prezzi per gli articoli sincronizzati possono essere esportati nei due modi descritti di seguito.

### Sincronizzare i prezzi dalla pagina dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza i prezzi con Shopify**.

### Nore sul calcolo del prezzo

* Per il calcolo del prezzo, è importante avere un valore nel campo **Modello cliente predefinito**. Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).
* Immetti un **Codice valuta** solo se il tuo negozio online utilizza una valuta diversa dalla valuta locale. La valuta specificata deve avere i tassi di cambio configurati. Se il tuo negozio online utilizza la stessa valuta di [!INCLUDE[prod_short](../includes/prod_short.md)], lascia il campo vuoto.
* Quando si determina un prezzo, [!INCLUDE[prod_short](../includes/prod_short.md)] utilizza la logica del "prezzo più basso". La logica del prezzo minore indica che se il prezzo unitario definito nella scheda articolo è inferiore a quello definito nel gruppo di prezzi, viene utilizzato il prezzo unitario della scheda articolo.

## Sincronizzare l'inventario con Shopify

La sincronizzazione dell'inventario può essere configurata per gli articoli già sincronizzati. Ci sono due condizioni che devono essere soddisfatte:

1. Il monitoraggio dell'inventario deve essere abilitato per un prodotto in Shopify. Se gli elementi vengono esportati in Shopify, considera l'abilitazione dell'opzione **Inventario tracciato** nella pagina **Punto vendita Shopify**. Per ulteriori informazioni, vedi la sezione [Esportare articoli su Shopify](synchronize-items.md#export-items-to-shopify)
2. La sincronizzazione dell'inventario deve essere abilitata per **Posizioni Shopify**.

### Per abilitare la sincronizzazione dell'inventario

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare l'inventario per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Posizioni** per aprire **Posizioni punto vendita Shopify**.
4. Scegli l'azione **Recupera posizioni Shopify** per importare tutte le posizioni definite in Shopify. Puoi trovarli nelle impostazioni [**Posizioni**](https://www.shopify.com/admin/settings/locations) in **Amministratore Shopify**.
5. Nel campo **Filtro posizione**, aggiungi posizioni, se desideri includere l'inventario solo da posizioni specifiche. Puoi quindi immettere *EST|OVEST*, in modo che l'inventario solo da queste due posizioni sia disponibile per la vendita tramite il negozio online.
6. Deseleziona l'opzione **Disabilitato** per abilitare la sincronizzazione dell'inventario per le posizioni Shopify selezionate.

Puoi inizializzare le sincronizzazione dell'inventario in due modi descritti di seguito.

### Sincronizzare l'inventario dalla pagina del punto vendita Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare l'inventario per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza inventario**.

### Sincronizzare l'inventario dalla pagina dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza inventario**.

### Note sull'inventario

* Il connettore calcola il **Saldo disponibile previsto** alla data corrente e lo esporta in Shopify.
* Puoi esaminare le informazioni sulle scorte ricevute da Shopify nella pagina **Scheda dettaglio Inventario Shopify**. In questa Scheda dettaglio, ottieni una panoramica delle scorte Shopify e l'ultimo inventario calcolato in [!INCLUDE[prod_short](../includes/prod_short.md)]. C'è un record per posizione.
* Se le informazioni sulle scorte in Shopify sono diverse dal **Saldo disponibile previsto** in[!INCLUDE[prod_short](../includes/prod_short.md)], le scorte verranno aggiornate in Shopify.

#### Esempio di calcolo del saldo disponibile previsto

Sono disponibili 10 pezzi dell'articolo A e due ordini di vendita in sospeso. Uno per lunedì con quantità *Uno* e uno per giovedì con quantità *Due*. A seconda di quando sincronizzi l'inventario, il sistema aggiornerà il livello delle scorte in Shopify con quantità diverse:

|Quando viene eseguita la sincronizzazione dell'inventario|Valore utilizzato per aggiornare il livello delle scorte|Commento|
|------|-----------------|-----------------|
|Martedì|9|Inventario 10 meno l'ordine di vendita impostato per la spedizione lunedì|
|Venerdì|7|Inventario 10 meno entrambi gli ordini di vendita|

## Vedere anche

[Iniziare a usare il connettore per Shopify](get-started.md)  
