---
title: Sincronizzare articoli e inventario
description: Configurare ed eseguire sincronizzazioni di articoli tra Shopify e Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: fac1a3df12070a2030d6d2d8dfd5e740d8cca4f9
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768142"
---
# <a name="synchronize-items-and-inventory"></a>Sincronizzare articoli e inventario

Gli **Articoli** in [!INCLUDE[prod_short](../includes/prod_short.md)] sono equivalenti ai *prodotti* in Shopify, che includono beni fisici, download digitali, servizi e buoni regalo che vendi. Ci sono due ragioni principali per sincronizzare gli elementi:

1. In primo luogo, la gestione dei dati viene eseguita in [!INCLUDE[prod_short](../includes/prod_short.md)] ed è necessario esportare tutti o alcuni dati in Shopify e renderli visibile. Puoi esportare il nome dell'articolo, la descrizione, l'immagine, i prezzi, la disponibilità, le varianti, i dettagli del fornitore e il codice a barre. Una volta importati, gli articoli possono diventare immediatamente visibili oppure possono essere esaminati e migliorati prima da una persona responsabile.
2. Quando un ordine di Shopify viene importato, le informazioni sugli articoli sono essenziali per l'ulteriore elaborazione del documento in [!INCLUDE[prod_short](../includes/prod_short.md)].

Questi due scenari sono sempre abilitati.

Un altro scenario è quando i dati vengono gestiti in Shopify e vuoi importare quegli articoli in blocco [!INCLUDE[prod_short](../includes/prod_short.md)]. Questo scenario può essere utile per gli eventi di migrazione dei dati, quando un punto vendita online esistente deve essere collegato a uno nuovo [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="to-define-item-synchronizations"></a>Per definire le sincronizzazioni degli articoli

1. Scegli l'icona di ricerca a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Punto vendita Shopify**. Apri un punto vendita per il quale desideri configurare la sincronizzazione degli articoli.
2. Dal campo **Sincronizza articolo**, seleziona l'opzione richiesta. <br>Nella seguente tabella vengono illustrate le diverse opzioni.

|Opzione|Descrizione|
|------|-----------|
|**Vuoto**| I prodotti vengono importati insieme all'importazione degli ordini. I prodotti vengono esportati in Shopify se l'utente esegue l'azione **Aggiungi articolo** dalla finestra **Prodotti Shopify**. Si tratta del comportamento predefinito. |
|**A Shopify**| Seleziona questa opzione se, dopo la sincronizzazione iniziale attivata dall'azione **Aggiungi articolo**, prevedi di aggiornare i prodotti manualmente utilizzando l'azione **Sincronizza prodotto** o tramite la coda processi per gli aggiornamenti ricorrenti. Ricordati di abilitare il campo **Può aggiornare il prodotto Shopify**. Se non abilitato, è uguale all'opzione **Vuoto**. |
|**Da Shopify**| Scegli questa opzione se prevedi di importare prodotti da Shopify in blocco, manualmente con l'azione **Sincronizza prodotto** o tramite la coda processi per gli aggiornamenti ricorrenti. Se nessuna opzione è selezionata, è uguale all'opzione **Vuoto**.|

## <a name="import-items-from-shopify"></a>Importare articoli da Shopify

Sia se importano articoli da Shopify in blocco o insieme all'importazione di ordini, questi articoli vengono aggiunti prima al **prodotto Shopify** e alle tabelle **Variante Shopify**. Le seguenti impostazioni consentono di gestire il processo:

|Campo|Descrizione|
|------|-----------|
|**Crea automaticamente articoli sconosciuti**|Quando prodotti e varianti shopify vengono importati in [!INCLUDE[prod_short](../includes/prod_short.md)], la funzione [!INCLUDE[prod_short](../includes/prod_short.md)] cerca sempre di trovare prima il record corrispondente nell'elenco degli elementi. **Mapping SKU** influisce sul modo in cui viene eseguita la corrispondenza e crea un nuovo articolo e/o una variante di articolo. Per ulteriori informazioni, vedere [Mapping prodotto](synchronize-items.md#). Abilita questa opzione se desideri creare un nuovo articolo o quando non esiste un record corrispondente. Il nuovo articolo verrà creato utilizzando i dati importati e **Codice modello articolo**. Se questa opzione non è abilitata, dovrai creare un articolo manualmente e utilizzare l'azione **Esegui mapping prodotto** dalla pagina **Prodotti Shopify**.|
|**Codice modello articolo**|Utilizzato insieme a **Crea automaticamente articoli sconosciuti**. <br> Scegli il modello da utilizzare per gli articoli creati automaticamente.|
|**Mapping SKU**|Scegli come vuoi usare il valore **SKU** importato da Shopify durante il mapping la creazione dell'articolo/variante. Per ulteriori informazioni, vedere [Come lo SKU e il codice a barre definiti nel prodotto Shopify hanno impatto sul mapping e la creazione di articoli e varianti](synchronize-items.md#how-sku-and-barcode-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**Separatore campo SKU**|Usato insieme a **Mapping SKU** impostato sull'opzione **Nr. articolo + Codice Variante**.<br> Definisci un separatore da utilizzare per dividere lo SKU. <br>Ad esempio, se in Shopify crei la variante con SKU "1000/001", digita "/" nel campo **Separatore di campo SKU** per ottenere il numero dell'articolo [!INCLUDE[prod_short](../includes/prod_short.md)] come "1000" e il codice della variante articolo come "001".
|**Prefisso variante**|Usato insieme a **Mapping SKU** impostato sulle opzioni **Codice variante** o **Nr. articolo + Codice variante** come strategia di fallback quando lo SKU proveniente da Shopify è vuoto.<br>Se vuoi creare la variante articolo in [!INCLUDE[prod_short](../includes/prod_short.md)] automaticamente, dovrai inserire un valore in **Codice**. Per impostazione predefinita, viene utilizzato il valore definito nel campo SKU importato da Shopify. Tuttavia, se lo SKU è vuoto, genererà codice che inizia con il prefisso della variante definito e "001".|
|**Shopify può aggiornare l'articolo**| Scegli questa opzione se desideri aggiornare automaticamente gli articoli e/o le varianti.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Come SKU e codici a barre definiti nel prodotto Shopify influenza il mapping e la creazione di articoli e varianti in Business Central

Quando i prodotti vengono importati da Shopify alle tabelle **Prodotti Shopify** e **Varianti Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] cerca di trovare i record esistenti. Nella seguente tabella vengono illustrate le diverse opzioni nel campo **Mapping SKU**.

|Opzione|Effetto sul mapping|Effetto sulla creazione|
|------|-----------------|------------------|
|**Vuoto**|Il campo SKU non viene utilizzato nella routine di mapping degli articoli.|Nessun effetto sulla creazione dell'articolo. <br>Impedisce la creazione di varianti. È utile quando nell'ordine cliente viene utilizzato solo l'articolo principale. Una variante può ancora essere mappata manualmente dalla finestra **Prodotto Shopify**.|
|**Nr. Articolo**|cegli se il campo SKU contiene il numero dell'articolo.|Nessun effetto sulla creazione dell'articolo senza varianti. Per un articolo con varianti, ogni variante viene creata come articolo separato.<br> Ad esempio, se Shopify ha un prodotto con due varianti e i loro SKU sono "1000" e "2000", in [!INCLUDE[prod_short](../includes/prod_short.md)] il sistema creerà due elementi con i numeri "1000" e "2000".|
|**Cod. variante**|Il campo SKU non viene utilizzato nella routine di mapping degli articoli.|Nessun effetto sulla creazione dell'articolo. Quando viene creata una variante di articolo, il valore del campo SKU viene utilizzato come codice. Se lo SKU è vuoto, viene generato un codice utilizzando il campo **Prefisso variante**.|
|**Nr. articolo e codice variante**| Seleziona se il campo SKU contiene un numero articolo e il codice della variante dell'articolo separato dal valore definito nel campo **Separatore di campo SKU**.|Quando viene creato un articolo, la prima parte del valore del campo SKU viene utilizzata come **Nr.**. Se lo SKU è vuoto, un numero di articolo viene generato utilizzando le serie di numeri definite in **Codice modello articolo** o **Nr. articolo** dalla finestra **Setup magazzino**.<br>Quando viene creato un articolo, la funzione della variante utilizza la seconda parte del valore del campo SKU come **Codice**. Se lo SKU è vuoto, viene generato un codice utilizzando il campo **Prefisso variante**.|
|**Nr. fornitore articolo**| Scegli se il campo SKU contiene il numero di articolo del fornitore. In questo caso, il **Nr. articolo venditore** non è utilizzato nella finestra **Scheda articolo**, ma **Nr. articolo fornitore** dal **Catalogo fornitori articolo**. Se il record *Catalogo fornitori articolo* trovato contiene un codice variante, questo codice variante viene utilizzato per mappare la variante Shopify.|Se esiste un fornitore corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)], il valore SKU verrà utilizzato come **Nr. articolo fornitore** nella **Scheda oggetto** e come **Riferimento articolo** di tipo Fornitore. <br>Impedisce la creazione di varianti. È utile quando si desidera utilizzare solo l'articolo principale nell'ordine cliente. Sarai ancora in grado di mappare una variante manualmente dalla finestra **Prodotto Shopify**.|
|**Codice a barre**| Scegli se il campo SKU contiene un codice a barre. Viene eseguita una ricerca tra **Riferimenti di articoli** di tipo fornitore. Se il record Riferimento articolo trovato contiene un codice variante, questo verrà utilizzato per mappare la variante Shopify.|Nessun effetto sulla creazione dell'articolo. <br>Impedisce la creazione di varianti. Può essere utile quando nell'ordine cliente viene utilizzato solo l'articolo principale. Una variante può ancora essere mappata manualmente dalla finestra **Prodotto Shopify**.|

Nella seguente tabella viene illustrato l'effetto del campo **Codice a barre**.

|Effetto sul mapping|Effetto sulla creazione|
|-----------------|------------------|
|Viene eseguita una ricerca tra i **Riferimenti di articoli** del tipo codice a barre per il valore definito nel campo Codice a barre in Shopify. Se il record di riferimento articolo trovato contiene un codice variante, questo verrà utilizzato per mappare la variante Shopify.|Il codice a barre viene salvato come **Riferimento articolo** per articolo e variante di articolo.|

> [!NOTE]  
> È possibile ttivare il mapping per il prodotto/varianti selezionati o per tutti i prodotti importati non mappati scegliendo **Prova Trova mapping prodotti** (per selezionato) o **Prova mapping ricerca** (per tutti).

## <a name="export-items-to-shopify"></a>Esportare articoli in Shopify

Scegli gli elementi dal tuo elenco di articoli che verranno esportati su Shopify. Usa l'azione **Aggiungi articolo** dalla finestra **Prodotti Shopify** per aggiungere articoli all'elenco prodotti Shopify.

Le seguenti impostazioni consentono di gestire il processo di esportazione degli articoli:

|Campo|Descrizione|
|------|-----------|
|**Gruppo prezzi cliente**|Determina il prezzo di un articolo in Shopify. Viene preso il prezzo di vendita di questo gruppo di prezzi cliente. Se non viene inserito alcun gruppo, viene utilizzato il prezzo della scheda articolo.|
|**Categoria sconto clienti**|Determina lo sconto da utilizzare per calcolare il prezzo di un articolo in Shopify. I prezzi scontati sono archiviati nel campo **Prezzo** e il prezzo intero è archiviato nel campo **Confronta prezzo**.|
|**Sincronizza testo esteso articolo**|Seleziona per sincronizzare il testo esteso dell'articolo. Dal momento che verrà aggiunto a *Descrizione*, può contenere codice HTML. |
|**Sincronizza attributi articolo**|Seleziona per sincronizzare gli attributi dell'articolo. Gli attributi sono formattati come una tabella e inclusi nel campo *Descrizione* su Shopify.|
|**Codice lingua**|Se selezionata, le versioni tradotte vengono utilizzate per titolo, attributi e testo esteso.|
|**Mapping SKU**|Scegli come vuoi compilare il campo SKU in Shopify. Le opzioni supportate sono:<br> - **Nr. articolo** per utilizzare il numero di articolo per prodotti e varianti.<br> - **Nr. articolo + Codice variante** per creare uno SKU concatenando i valori di due campi. Per gli articoli senza varianti, viene utilizzato solo il numero di articolo.<br>- **Nr. articolo fornitore** per utilizzare il numero del fornitore dell'articolo definito nella *Scheda articolo* sia per i prodotti che per le varianti.<br> - **Codice a barre** - usa **Riferimento articolo** di tipo codice a barre. Questa opzione rispetta le varianti. |
|**Separatore campo SKU**|Definisci un separatore per l'opzione **Nr. articolo + Codice variante**.|
|**Inventario tracciato**|Scegli come il sistema dovrebbe popolare il campo **Tieni traccia dell'inventario** per i prodotti esportati su Shopify. È possibile aggiornare le informazioni sulla disponibilità da [!INCLUDE[prod_short](../includes/prod_short.md)] per i prodotti in Shopify il cui inventario di traccia è abilitato. Per ulteriori informazioni, vedere [Magazzino](synchronize-items.md#sync-inventory-to-shopify).|
|**Criterio di inventario predefinito**|Scegli *Nega* per evitare stock negativo del lato Shopify. |
|**Può aggiornare prodotti Shopify**|Definisci se [!INCLUDE[prod_short](../includes/prod_short.md)] può solo creare articoli o anche aggiornarli. Seleziona questa opzione se, dopo la sincronizzazione iniziale attivata dall'azione **Aggiungi articolo**, prevedi di aggiornare i prodotti manualmente utilizzando l'azione **Sincronizza prodotto** o tramite la coda processi per gli aggiornamenti ricorrenti. Ricordati di selezionare **A Shopify** nel campo **Sincronizzazione articoli**.|

### <a name="fields-mapping-overview"></a>Panoramica mapping dei campi

|Shopify|Origine quando esportato da [!INCLUDE[prod_short](../includes/prod_short.md)]|Destinazione quando importato in [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Stato|In base allo **Stato per i prodotti creati** nella **Scheda punto vendita Shopify**. Per ulteriori informazioni, vedere [Aggiornamenti ad hoc di prodotti Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products).|Non utilizzato.|
|Titolo|**Descrizione**. Se il codice della lingua è definito ed esiste la traduzione dell'articolo corrispondente, verrà utilizzata la traduzione dell'articolo al posto della descrizione.|**descrizione**|
|Descrizione|Combina testi e attributi estesi se le opzioni corrispondenti nella scheda punto vendita Shopify sono abilitate. Rispetta codice lingua.|Non utilizzato.|
|Titolo pagina SEO|Valore fisso: vuoto, vedi [Aggiornamenti ad hoc di prodotti Shopify ](synchronize-items.md#ad-hock-updates-of-shopify-products). |Non utilizzato.|
|Meta descrizione SEO|Valore fisso: vuoto, vedi [Aggiornamenti ad hoc di prodotti Shopify ](synchronize-items.md#ad-hock-updates-of-shopify-products). |Non utilizzato.|
|Elemento multimediale|**Immagine**, per ulteriori informazioni, vedere [Sincronizzare le immagini degli articoli](synchronize-items.md#sync-item-images)|**Immagine**|
|Prezzo|Il prezzo per il cliente finale viene calcolato in base al gruppo prezzi articolo, al gruppo sconto articolo, al codice valuta e al codice modello cliente. |Non utilizzato.|
|Confronta prezzo|Il prezzo senza sconto viene calcolato in base al gruppo prezzi articolo, al gruppo sconto articolo, al codice valuta e al codice modello cliente. |Non utilizzato.|
|Costo per articolo|**Costo unitario**|**Costo unitario**|
|SKU|Vedere **Mapping SKU** in [Esportare articoli in Shopify](synchronize-items.md#export-items-to-shopify)| Vedi [Come lo SKU e il codice a barre definiti nel prodotto Shopify hanno impatto sul mapping e la creazione di articoli e varianti](synchronize-items.md#how-sku-and-barcode-defined-in-shopify-product-impact-mapping-and-creation-of-items-and-variants-in-business-central)|
|Codice a barre|**Riferimenti di articoli** di tipo codice a barre|**Riferimenti di articoli** di tipo codice a barre|
|Traccia quantità|In base a **Inventario tracciato** nella **Scheda punto vendita di Shopify**. Per ulteriori informazioni, vedere [Magazzino](synchronize-items.md#sync-inventory-to-shopify).|Non utilizzato.|
|Continuare a vendere quando le scorte sono esaurite|In base al **Criterio di inventario predefinito** nella **Scheda del punto vendita Shopify**. Non importato.|Non utilizzato.|
|Tipo|**Descrizione** di **Codice categoria articolo**. Se il tipo non è specificato su Shopify, verrà aggiunto come tipo personalizzato.|**Codice categoria articolo**. Mapping per descrizione.|
|Fornitore|**Nome** del fornitore da **Nr. fornitore** |Mapping **Nr. fornitore** per nome.|
|Peso|**Peso lordo**.|Non utilizzato.|
|Imponibile|Valore fisso: Abilitato.|Non utilizzato.|
|Codici imposta|**Codice gruppo imposte**. Rilevante solo per le imposte di vendita. Per ulteriori informazioni, vedi [Imposte](synchronize-orders.md#tax-remarks) |Non utilizzato.|

### <a name="tags"></a>Tag

I tag importati possono essere esaminati nel riquadro Dettagli **Tag** nel **Prodotto Shopify**. Per modificare i tag, scegli l'azione **Tag** nella pagina **Prodotto Shopify**.
Se l'opzione **A Shopify** è selezionata nel campo **Sincronizza articolo**, i tag assegnati vengono esportati in Shopify alla successiva sincronizzazione.

## <a name="run-item-synchronization"></a>Esegui sincronizzazione articoli

La sincronizzazione completa o parziale degli articoli può essere eseguita in molti modi diversi.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Sincronizzazione iniziale degli articoli da Business Central a Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Aggiungi articoli**.
3. Nel campo **Codice punto vendita** immetti il primo codice. Se apri la finestra **Prodotto Shopify** dalla finestra **Scheda punto vendita**, il codice punto vendita verrà compilato automaticamente.
4. Definisci i filtri sugli articoli come richiesto. Ad esempio, puoi filtrare per numero articolo o codice categoria articolo.
5. Selezionare **OK**.

Gli articoli ottenuti vengono creati automaticamente in Shopify con prezzi ma immagini e livelli di inventario non sono inclusi. L'operazione potrebbe richiedere del tempo se viene aggiunto un numero elevato di articoli.

### <a name="sync-products-from-shopify-to-business-central"></a>Sincronizza i prodotti da Shopify a Business Central

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Negozio Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza prodotti**.

In alternativa, utilizza l'azione **Sincronizza prodotti** sulla finestra **Prodotti Shopify** o cerca il processo batch **Sincronizzare prodotti**.

### <a name="ad-hock-updates-of-shopify-products"></a>Aggiornamenti ad hoc di prodotti Shopify

Quando i record vengono aggiornati nella tabella **Prodotto Shopify**, le seguenti modifiche vengono sincronizzate con Shopify.

Aggiorna:

* **Stato** - puoi scegliere tra attivo, archiviato o bozza.
* **Titolo SEO**
* **Descrizione SEO**

Eliminazione:

In base al valore in **Azione per prodotti rimossi** in **Scheda punto vendita Shopify**, il prodotto viene aggiornato in Shopify quando il record viene eliminato dalla pagina **Prodotti Shopify**.

* **Vuoto** - non succederà nulla. Se necessario, l'utente deve eseguire l'azione richiesta da Amministratire Shopify.
* **Stato in bozza** - lo stato del prodotto in Shopify è impostato per *Bozza*.
* **Stato su Archiviato** - il prodotto è archiviato in Shopify.

## <a name="sync-item-images"></a>Sincronizza immagini articolo

La sincronizzazione delle immagini può essere configurata per gli articoli sincronizzati. È possibile scegliere tra le seguenti opzioni:

* **Vuoto** - la sincronizzazione delle immagini è disattivata.
* **A Shopify** - le immagini degli articoli vengono esportate in Shopify
* **Da Shopify** - le immagini da Shopify vengono importate in [!INCLUDE[prod_short](../includes/prod_short.md)]

La sincronizzazione delle immagini può essere inizializzata in due modi.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Sincronizzare le immagini dei prodotti dalla finestra del punto vendita Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare le immagini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza immagini prodotto**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Sincronizzare le immagini dei prodotti dalla finestra dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza immagini prodotto**.

### <a name="image-synchronization-remarks"></a>Osservazioni sulla sincronizzazione delle immagini

* Quando si esportano immagini da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, vengono aggiunte le nuove immagini a Shopify, mantenendo intatte le vecchie immagini. Se un'immagine viene aggiornata in [!INCLUDE[prod_short](../includes/prod_short.md)], dovrai eliminare le vecchie immagini in Amministratore Shopify.
* Le immagini che vengono esportate in Shopify e non rispettano i requisiti definiti da Shopify non verranno importate. Per ulteriori informazioni, vedere [Tipi di supporto del prodotto su help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Sincronizzare i prezzi con Shopify

I prezzi possono essere esportati per gli articoli sincronizzati nei modi descritti di seguito.

### <a name="sync-prices-from-the-shopify-products-window"></a>Sincronizzare i prezzi dalla finestra dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza i prezzi con Shopify**.

### <a name="price-calculation-remarks"></a>Nore sul calcolo del prezzo

* Per il calcolo del prezzo, è importante avere un valore nel campo **Modello cliente predefinito**.
* Ricordarsi di inserire un **Codice valuta** se il tuo negozio online utilizza una valuta diversa da LCY.
* Quando si determina un prezzo, [!INCLUDE[prod_short](../includes/prod_short.md)] utilizza la logica del "prezzo più basso". Significa che se il prezzo unitario definito nella scheda articolo è inferiore a quello definito nel gruppo di prezzi, viene utilizzato il prezzo unitario della scheda articolo.

## <a name="sync-inventory-to-shopify"></a>Sincronizzare l'inventario con Shopify

La sincronizzazione dell'inventario può essere configurata per gli articoli già sincronizzati. Ci sono due condizioni che devono essere soddisfatte:

1. Il monitoraggio dell'inventario deve essere abilitato per un prodotto in Shopify. Se gli elementi vengono esportati in Shopify, considera l'abilitazione dell'opzione **Inventario tracciato** nella scheda **Punto vendita Shopify**. Per ulteriori informazioni, vedere [Esportare articoli su Shopify](synchronize-items.md#export-items-to-shopify).
2. La sincronizzazione dell'inventario deve essere abilitata per **Posizioni Shopify**.

### <a name="to-enable-inventory-sync"></a>Per abilitare la sincronizzazione dell'inventario

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Negozio Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare l'inventario per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Posizioni** per aprire **Posizioni punto vendita Shopify**.
4. Scegli l'azione **Recupera posizioni Shopify** per importare tutte le posizioni definite in Shopify. Puoi trovarli nelle impostazioni [**Posizioni**](https://www.shopify.com/admin/settings/locations) in **Amministratore Shopify**.
5. Nel campo **Filtro posizione**, aggiungi posizioni, se desideri includere l'inventario solo da posizioni specifiche. Ad esempio, puoi immettere *EST|OVEST*, in modo che l'inventario solo da queste due posizioni sia disponibile per la vendita tramite il negozio online.
6. Deseleziona l'opzione **Disabilitato** per abilitare la sincronizzazione dell'inventario per le posizioni Shopify selezionate.

Puoi inizializzare le sincronizzazione dell'inventario in due modi.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Sincronizzare l'inventario dalla finestra del punto vendita Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare l'inventario per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza inventario**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Sincronizzare l'inventario dalla finestra dei prodotti Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. icona, immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Sincronizza inventario**.

### <a name="inventory-remarks"></a>Note sull'inventario

* Il connettore calcola il **Saldo disponibile previsto** e lo esporta in Shopify.
* Puoi esaminare le informazioni sulle scorte ricevute daShopify nella pagina **Scheda dettaglio Inventario Shopify**. In questa Scheda dettaglio, ottieni una panoramica delle scorte Shopify e l'ultimo inventario calcolato in [!INCLUDE[prod_short](../includes/prod_short.md)]. C'è un record per posizione.
* Se le informazioni sulle scorte in Shopify sono diverse dal **Saldo disponibile previsto** in[!INCLUDE[prod_short](../includes/prod_short.md)], le scorte verranno aggiornate in Shopify.

## <a name="see-also"></a>Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
