---
title: Sincronizzare ed evadere gli ordini cliente
description: Configura ed esegui l'importazione e l'elaborazione dell'ordine cliente da Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Sincronizzare ed evadere gli ordini cliente

Questo articolo descrive le impostazioni e i passaggi necessari da eseguire per sincronizzare ed evadere gli ordini cliente con Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)].

## Impostare l'importazione di ordini nella scheda del punto vendita Shopify

Immetti un **Codice valuta** se il tuo negozio online utilizza una valuta diversa dalla valuta locale. La valuta specificata deve avere i tassi di cambio configurati. Se il tuo negozio online utilizza la stessa valuta di [!INCLUDE[prod_short](../includes/prod_short.md)], lascia il campo vuoto. 

Puoi riesaminare la valuta del punto vendita nelle impostazioni [Dettagli punto vendita](https://www.shopify.com/admin/settings/general) nel tuo Amministratore Shopify. Shopify può essere configurato per accettare diverse valute, tuttavia gli ordini importati in [!INCLUDE[prod_short](../includes/prod_short.md)] usano la valuta del punto vendita.

Un ordine Shopify regolare può includere importi extra al subtotale, come spese di spedizione o, se abilitate, mance. Questi importi vengono registrati direttamente nel conto C/G che si desidera usare per tipi di transazione specifici:

* **Conto spese spedizione**
* **Conto buono regalo venduto**, per ulteriori informazioni, vedi [Buono regalo](synchronize-orders.md#gift-cards)
* **Conto mance**  

Abilita **Creazione automatica degli ordini** per creare automaticamente documenti di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] una volta importato l'ordine Shopify.

Se desideri rilasciare automaticamente un documento di vendita, attiva l'interruttore **Rilascio automatico ordine cliente**.

Se selezioni il campo **Nr. ordine Shopify nella riga documento**, [!INCLUDE [prod_short](../includes/prod_short.md)] inserisci le righe di vendita di tipo **Commento** con un numero di ordine Shopify.

>[!NOTE]
>Il documento di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] si collega all'ordine Shopify e puoi aggiungere il campo **N. ordine Shopify** all'elenco o alle pagine della scheda per gli ordini di vendita, le fatture e la spedizione. Per ulteriori informazioni sull'aggiunta di un campo, vai a [Per iniziare a personalizzare una pagina tramite il banner **Personalizzazione**](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

Nel campo **Priorità area fiscale**, definisci la priorità su come selezionare un'area di codice fiscale per gli indirizzi dell'ordine. L'ordine Shopify importato contiene informazioni sulle imposte. Le imposte vengono ricalcolate quando si crea i documenti di vendita, quindi è importante che le impostazioni IVA o imposta siano corrette in [!INCLUDE[prod_short](../includes/prod_short.md)]. Per ulteriori informazioni sulle imposte, vai a [Impostare le imposte per la connessione Shopify](setup-taxes.md).

Specifica come elaborerai resi e rimborsi:

* **Vuoto** specifica che non importi ed elabori resi e rimborsi.
* **Importa solo** specifica che importi le informazioni, ma creerai manualmente la nota di credito corrispondente.
* **Crea automaticamente nota di credito** specifica che si importano informazioni e [!INCLUDE[prod_short](../includes/prod_short.md)] crea automaticamente le note di credito. Questa opzione richiede l'attivazione dell'interruttore **Crea automaticamente ordine di vendita**.

Specifica un'ubicazione per i resi e i conti Co.Ge. per i rimborsi per merci e altri rimborsi.

* **Conto rimborso articoli non riforniti**: specifica un nr. conto C/G per articoli per cui non si desidera avere una rettifica di magazzino.
* **Conto rimborso**: specifica un nr. conto C/G per la differenza tra l'importo totale rimborsato e l'importo totale degli articoli.

Scopri di più su [Resi e rimborsi](synchronize-orders.md#returns-and-refunds)

### Mapping metodo spedizione

Il **Codice metodo di spedizione** per documenti di vendita importati da Shopify può essere compilato automaticamente. Devi configurare il **Mapping metodo di spedizione**.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri definire un mapping per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Mapping metodo di spedizione**. Ciò crea automaticamente record per i metodi di spedizione definiti nelle impostazioni [**Spedizione**](https://www.shopify.com/admin/settings/payments) nel tuo **Amministratore Shopify**.
4. Nel campo **Nome**, puoi vedere il nome del metodo di spedizione da Shopify.
5. Immetti il **Codice metodo di spedizione** con il metodo di spedizione corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Se più spese di spedizione sono associate a un ordine cliente; solo uno verrà selezionato come metodo di spedizione e assegnato al documento di vendita.

### Mapping della posizione

Il mapping dell'ubicazione è necessaria per compilare il **Codice ubicazione** per le righe dei documenti di vendita importate da Shopify. Questa opzione è importante se l'interruttore **Posizione obbligatoria** è abilitato nella scheda **Configurazione inventario**, altrimenti non potrai creare documenti di vendita.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri configurare il mapping delle posizioni per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Posizioni** per aprire le **Posizioni punto vendita Shopify**.
4. Scegli l'azione **Recupera posizioni Shopify** per importare tutte le posizioni definite in Shopify. Puoi trovarli nelle impostazioni [**Posizioni**](https://www.shopify.com/admin/settings/locations) nel pannello **Amministratore Shopify**. 
5. Inserisci il **Codice posizione predefinito** con la posizione corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Il mapping dell'ubicazione è usato anche per sincronizzare l'inventario. Per ulteriori informazioni, vedi [Sincronizzare l'inventario con Shopify](synchronize-items.md#sync-inventory-to-shopify)
  
## Eseguire la sincronizzazione degli ordini

Di seguito viene descritto come importare e aggiornare gli ordini di vendita.

> [!NOTE]  
> Gli ordini archiviati in Shopify non possono essere importati. Se hai bisogno di verificare lo stato dell'ordine, apri l'ordine dalla pagina [Ordini](https://www.shopify.com/admin/orders) del riquadro **Amministrazione Shopify** ed esamina dettagli dell'ordine.
> 
> Disattiva l'opzione **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni **Checkout** nel pannello **Amministratore Shopify** per verificare che tutti gli ordini vengano importati in [!INCLUDE[prod_short](../includes/prod_short.md)]. Se devi importare ordini archiviati, usa l'azione **Annulla l'archiviazione degli ordini** nella pagina [Ordini](https://www.shopify.com/admin/orders) del pannello **Amministratore Shopify**. 

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri importare gli ordini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Ordini**.
4. Scegli l'azione **Sincronizza ordini da Shopify**.
5. Definisci i filtri sugli ordini secondo necessità. Ad esempio, puoi importare ordini interamente pagati o quelli con un livello di rischio basso.

> [!NOTE]  
> Quando si filtra per tag, è necessario utilizzare token di filtro `@` e `*`. Ad esempio, se desideri importare ordini contenenti *tag1*, usa `@*tag1*`. `@` assicurerà che il risultato non sia sensibile alla differenza tra maiuscole e minuscole, mentre `*` troverà ordini con più tag.

6. Scegli il pulsante **OK**.

In alternativa, puoi cercare il processo batch **Sincronizza ordini da Shopify**.

È possibile pianificare l'attività da eseguire automaticamente. Ulteriori informazioni su [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

### Informazioni dettagliate

Il connettore Shopify importa gli ordini in due fasi:

1.  Importa le intestazioni degli ordini nella tabella **Ordini Shopify da importare** quando soddisfano determinate condizioni:
    
* Non vengono soddisfatte. Ciò significa che puoi includere o escludere gli ordini dalla sincronizzazione archiviandoli o rimuovendoli dall'archivio in Shopify- Amministra.
* Sono stati creati o modificati dopo l'ultima sincronizzazione. Ciò significa che puoi forzare la reimportazione di un ordine specifico se lo modifichi, ad esempio aggiungendo **Note** o **Tag**.

2.  Importa ordini Shopify e informazioni aggiuntive.
* Il Connettore Shopify elabora tutti i record nella tabella **Ordini Shopify da importare** che corrispondono ai criteri di filtro definiti nella pagina di richiesta **Sincronizza ordini da Shopify**. Ad esempio, tag, canale o stato di evasione ordini. Se non hai specificato alcun filtro, elabora tutti i record.
* Durante l'importazione dell'ordine Shopify, il connettore Shopify richiede informazioni supplementari da Shopify:

    * Intestazione ordine
    * Righe ordine
    * Informazioni sulla spedizione e l'evasione
    * Transazioni
    * Resi e rimborsi, se configurati

La pagina **Ordine Shopify da importare** è utile per la risoluzione dei problemi di importazione degli ordini. Puoi valutare gli ordini disponibili e seguire i passaggi successivi:

* Controlla se un errore ha bloccato l'importazione di un ordine specifico ed esplora i dettagli dell'errore. Controlla il campo **Con errore**.
* Elabora solo ordini specifici. Dovrai compilare il campo **Codice punto vendita**, selezionare uno o più ordini, quindi scegliere l'azione **Importa ordini selezionati**.
* Elimina gli ordini dalla pagina **Ordine Shopify da importare** per escluderli dalla sincronizzazione.

## Esaminare gli ordini importati

Una volta completata l'importazione, puoi esplorare l'ordine Shopify e trovare tutte le informazioni correlate, come transazioni di pagamento, costi di spedizione, livello di rischio, attributi e tag o adempimenti se l'ordine è stato già adempiuto in Shopify. Puoi anche vedere la conferma di ogni ordine inviata al cliente scegliendo l'azione **Pagina di stato Shopify**.

> [!NOTE]  
> Puoi accedere alla finestra **Ordini Shopify** direttamente e vedrai gli ordini con lo stato *aperto* di tutti i punti vendita Per rivedere gli ordini completati, è necessario aprire la pagina **Ordini Shopify** dalla specifica finestra **Scheda del punto vendita Shopify**.

## Creare documenti di vendita in Business Central

Se l'opzione **Creazione automatica ordini** è abilitata nella **Scheda del punto vendita Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tenta di creare un documento di vendita dopo aver importato l'ordine. Se manca un cliente o un prodotto, dovrai risolvere il problema e quindi creare nuovamente l'ordine di vendita.

### Per creare i documenti di vendita

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli ordini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Ordini**.
4. Seleziona l'ordine per il quale desideri creare un documento di vendita e scegli l'azione **Crea documenti di vendita**.
5. Selezionare **Sì**.

Se l'ordine Shopify richiede l'evasione, l'**Ordine di vendita** viene creato. Per gli ordini Shopify evasi, come gli ordini che contengono solo un buono regalo o che sono già gestiti in Shopify, la **Fattura di vendita** viene creata.

Viene ora creato un documento di vendita che può essere gestito utilizzando le funzionalità di [!INCLUDE[prod_short](../includes/prod_short.md)] standard.

### Gestire i clienti mancanti

Se le tue impostazioni impediscono la creazione automatica di un cliente e non è possibile trovare un cliente esistente corretto, dovrai assegnare un cliente a un ordine Shopify manualmente. Questa operazione può essere effettuata in vari modi:

* Puoi assegnare **Nr. cliente di vendita** e **Fatturare a - Nr. cli.** direttamente nella pagina **Ordini Shopify** scegliendo un cliente dall'elenco dei clienti esistenti.
* È possibile selezionare un codice modello cliente, creare e assegnare il cliente tramite l'azione **Crea nuovo cliente** nella pagina **Ordini Shopify**. Si noti che il cliente Shopify deve avere almeno un indirizzo. Gli ordini creati tramite il canale di vendita POS Shopify spesso non contengono i dettagli dell'indirizzo.
* È possibile mappare il cliente esistente al relativo **cliente Shopify** nella finestra **Clienti Shopify** e quindi scegliere l'azione **Trova mapping** nella pagina **Ordini Shopify**.

### In che modo il connettore sceglie quale cliente usare

La funzione *Importa ordine da Shopify* cerca di selezionare i clienti nel seguente ordine:

1. Se **Nr. cliente predefinito** è definito nel **Modello cliente Shopify** per **Spedire a - Codice paese/area geografica**, quindi **Nr. cliente predefinito** viene utilizzato indipendentemente dalle impostazioni nei campi **Importazione cliente da Shopify** e **Tipo di mapping cliente**. Ulteriori informazioni in [Modello cliente per paese](synchronize-customers.md#customer-template-per-countryregion).
2. Se **Importazione cliente da Shopify** è impostato su *Nessuno* e **Nr. cliente predefinito** è definito nella pagina **Scheda punto vendita Shopify**, il **Nr. cliente predefinito** viene utilizzato.

I prossimi passaggi dipendono dal **Tipo di mapping cliente**.

* Se è **Acquisisci sempre il cliente predefinito**, il connettore utilizza il cliente definito nel campo **Nr. cliente predefinito** nella pagina **Scheda punto vendita Shopify**.
* Se è **Per e-mail/telefono**, il connettore tenta di trovare il cliente esistente prima in base all'ID, quindi tramite e-mail e quindi tramite numero di telefono. Se il cliente non viene trovato, il connettore crea un nuovo cliente.
* Se è **Per informazioni Fatturare a**, il connettore tenta di trovare il cliente esistente prima in base all'ID e poi in base alle informazioni sull'indirizzo di fatturazione. Se il cliente non viene trovato, il connettore crea un nuovo cliente.

> [!NOTE]  
> Il connettore utilizza le informazioni dall'indirizzo di fatturazione e crea il cliente di fatturazione in [!INCLUDE[prod_short](../includes/prod_short.md)]. Il cliente a cui vendere è lo stesso del cliente a cui fatturare.

### Diverse regole di elaborazione per gli ordini

Potresti voler elaborare gli ordini in modo diverso in base a una regola. Ad esempio, gli ordini da un canale di vendita specifico, come il POS, dovrebbero utilizzare il cliente predefinito, ma desideri che il tuo negozio online disponga di informazioni reali sul cliente.

Un modo per soddisfare questo requisito è creare una Scheda punto vendita Shopify aggiuntiva e utilizzare i filtri nella pagina di richiesta **Sincronizza ordini da Shopify**.

Esempio: hai un negozio online e un POS Shopify. Per il tuo POS, vuoi utilizzare un cliente fisso, ma per il tuo negozio online vuoi creare clienti in [!INCLUDE[prod_short](../includes/prod_short.md)]. La procedura seguente elenca i passaggi di alto livello. Per saperne di più, vai agli articoli della guida corrispondenti.

1. Crea un punto vendita Shopify chiamato *STORE* e collegalo al tuo account Shopify.
2. Configura la sincronizzazione articolo/prodotto in modo che questo negozio gestisca le informazioni sul prodotto.
3. Specifica che i clienti vengono importati con gli ordini. Il connettore dovrebbe trovare i clienti cercando il loro indirizzo e-mail. Se non trova un indirizzo, utilizza il modello cliente per creare un nuovo cliente.
4. Crea un punto vendita Shopify chiamato *POS* e collegalo allo stesso account Shopify.
6. Assicurati che la sincronizzazione articolo/prodotto sia disabilitata.
7. Seleziona il connettore che utilizza il cliente predefinito.
8. Crea una voce coda processi ricorrente per Report 30104 **Sincronizza ordini da Shopify**. Seleziona **PUNTO VENDITA** nel campo **Codice punto vendita Shopify** e utilizza i filtri per acquisire tutti gli ordini ad eccezione di quelli creati dal canale di vendita POS. Ad esempio, **<>Punto vendita**
9. Crea una voce coda processi ricorrente per il Report 30104 **Sincronizza ordini da Shopify**. Seleziona **POS** nel campo **Codice punto vendita Shopify** e utilizza i filtri per catturare gli ordini generati dal canale di vendita POS. Ad esempio, **Punto vendita**.

Ciascuna coda di lavoro importerà ed elaborerà gli ordini all'interno dei filtri definiti e utilizzerà le regole della scheda del punto vendita Shopify corrispondente. Ad esempio, creeranno ordini del punto vendita per il cliente predefinito.

>[!Important]
> Per evitare conflitti durante l'elaborazione degli ordini, ricorda di utilizzare la stessa categoria della coda lavori per entrambe le voci della coda lavori.

### Impatto delle modifiche degli ordini

In Shopify:

|Modifica|Impatto per l'ordine già importato|Impatto per l'ordine che viene importato per la prima volta|
|------|-----------|-----------|
|Cambia la posizione di evasione | L'ubicazione originale è nelle righe | L'ubicazione di evasione viene sincronizzata con [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Modificare un ordine e aumentare la quantità| L'intestazione dell'ordine e le tabelle supplementari verranno aggiornate in [!INCLUDE[prod_short](../includes/prod_short.md)], non le righe.| L'ordine importato utilizzerà la nuova quantità|
|Modificare un ordine e diminuire la quantità| L'intestazione dell'ordine e le tabelle supplementari verranno aggiornate in [!INCLUDE[prod_short](../includes/prod_short.md)], non le righe.| L'ordine importato utilizzerà la quantità originale, il campo Quantità disponibile per l'evasione conterrà un nuovo valore.|
|Modificare un ordine e rimuovere un articolo esistente | L'intestazione dell'ordine e le tabelle supplementari verranno aggiornate in [!INCLUDE[prod_short](../includes/prod_short.md)], non le righe.| L'articolo rimosso verrà comunque importato, il campo Quantità disponibile per l'evasione conterrà zero. |
|Modifica un ordine e aggiungi nuovo articolo | L'intestazione dell'ordine verrà aggiornata, le righe no. | Gli articoli originali e aggiunti verranno importati. |
|Elaborare l'ordine: evadere, aggiornare le informazioni di pagamento | L'intestazione dell'ordine verrà aggiornata, ma non le righe. |La modifica non ha alcun impatto sulla modalità di importazione dell'ordine.|
|Annullare l'ordine | L'intestazione dell'ordine verrà aggiornata, ma non le righe. |L'ordine annullato non viene importato |

Come puoi vedere, in alcuni casi potrebbe essere ragionevole eliminare l'ordine modificato in [!INCLUDE[prod_short](../includes/prod_short.md)] e importarlo come nuovo.

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Modifica|Impatto|
|------|-----------|
|Cambia la posizione in un'altra posizione, mappata alle posizioni Shopify. Registra spedizione. | L'ordine sarà contrassegnato come evaso. L'ubicazione originale verrà utilizzata. |
|Cambia la posizione in un'altra posizione, non mappata alle posizioni Shopify. Registra spedizione. | L'evasione non verrà sincronizzata con Shopify. |
|Riduci la quantità. Registra spedizione. | L'ordine in Shopify sarà contrassegnato come parzialmente evaso. |
|Aumenta la quantità. Registra spedizione. | L'evasione non verrà sincronizzata con Shopify. |
|Aggiungi un nuovo articolo. Registra spedizione. | L'ordine in Shopify sarà contrassegnato come evaso. Le righe non verranno aggiornate. |

## Sincronizzare le spedizioni con Shopify

Quando un ordine cliente creato da un ordine Shopify viene spedito, è possibile sincronizzare le spedizioni con Shopify.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Sincronizza spedizioni con Shopify**, quindi scegli il collegamento correlato.
2. Definisci i filtri sulle spedizioni secondo necessità. Ad esempio, puoi aggiornare una spedizione registrata in una data specifica.
3. Scegli il pulsante **OK**.

L'ordine in Shopify sarà contrassegnato come evaso. Il cliente riceve automaticamente un messaggio e-mail o SMS di avviso di spedizione. Se sulla spedizione sono specificati un agente di spedizione e un codice di tracciabilità, le informazioni di tracciabilità sono incluse nell'e-mail.

In alternativa, utilizza l'azione **Sincronizza spedizioni** in Ordini di vendita Shopify o nelle pagine del negozio Shopify.

È possibile pianificare l'attività da eseguire in modo automatizzato. Ulteriori informazioni su [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

>[!Important]
>L'ubicazione, inclusa l'ubicazione vuota, definita nella riga di spedizione registrata deve avere un record corrispondente nell'ubicazione Shopify. In caso contrario, questa linea non verrà reinviata a Shopify. Ulteriori informazioni in [Mapping della posizione](synchronize-orders.md#location-mapping).

Ricordati di eseguire **Sincronizza ordini da Shopify** per aggiornare lo stato di evasione di un ordine in [!INCLUDE[prod_short](../includes/prod_short.md)]. La funzionalità del connettore archivia anche gli ordini completamente pagati ed evasi in Shopify e [!INCLUDE[prod_short](../includes/prod_short.md)] purché le condizioni siano soddisfatte. 

### Agenti di spedizione e URL di tracciamento

Se il documento **Spedizione vendita registrate** contiene il **codice Spedizioniere** e/o il **Numero di tracciabilità del pacco**, queste informazioni saranno inviate a Shopify e al cliente nell'e-mail di conferma della spedizione.

La società di tracciamento viene popolata in base allo spedizioniere con le seguenti priorità (dalla più alta alla più bassa):

* **Società tracciabilità Shopify**
* **Nome**
* **Codice**

Se il campo **URL tracciabilità pacchetto** è compilato per il record dello spedizioniere, la conferma della spedizione conterrà anche un URL di tracciamento.

## Resi e rimborsi

In un'integrazione tra Shopify e [!INCLUDE[prod_short](../includes/prod_short.md)], è importante poter sincronizzare quanti più dati aziendali possibile. Ciò semplifica l'aggiornamento dei livelli finanziari e di magazzino in [!INCLUDE[prod_short](../includes/prod_short.md)]. I dati che puoi sincronizzare includono resi e rimborsi che sono stati registrati in Amministra Shopify o POS Shopify.

Resi e rimborsi vengono importati con i relativi ordini se hai abilitato il tipo di lavorazione sulla scheda del punto vendita Shopify.

I resi vengono importati solo a scopo informativo. Non esiste alcuna logica di elaborazione ad essi associata.

Le transazioni finanziarie e, se necessario, di magazzino vengono elaborate tramite rimborsi. I rimborsi possono includere prodotti o solo importi, ad esempio, se un venditore ha deciso di compensare le spese di spedizione o qualche altro importo.
È possibile creare note di credito di vendita per i rimborsi. Le note di credito possono avere le seguenti tipologie di righe:

|Tipo|Nr.|Commento|
|-|-|-|
|Conto C/G|Conto buono regalo venduto| Da utilizzare per i rimborsi relativi ai buoni regalo.|
|Conto C/G|Conto rimborso articoli non in stock | Da utilizzare per i rimborsi relativi a prodotti che non sono stati riassortiti. |
|Articolo |Nr. articolo| Da utilizzare per i rimborsi relativi a prodotti che sono stati riassortiti. Valido per rimborsi diretti o rimborsi collegati a rimborsi. Il codice ubicazione sulla riga di credito in più viene impostato in base al valore selezionato per l'ubicazione di reso.|
|Conto C/G| Conto rimborso | Da utilizzare per altri importi rimborsati non correlati a prodotti o buoni regalo. Ad esempio, mance o se hai specificato manualmente un importo da rimborsare in Shopify. |

>[!Note]
>La posizione di reso, comprese le posizioni vuote, definite in **Scheda punto vendita Shopify** viene utilizzata sulla nota di credito creata. Il sistema ignora le ubicazioni originali dagli ordini o dalle spedizioni.

## Buoni regalo

Nel punto vendita Shopify puoi vendere buoni regalo, che possono essere utilizzati per pagare prodotti reali.

Quando si tratta di buoni regalo, è importante inserire un valore nel campo **Conto buono regalo venduto** nella finestra **Scheda punto vendita Shopify**. Il buono regalo venduto verrà sincronizzato insieme agli ordini in linea. Con l'ordine verrà importato anche un buono regalo applicato, ma ora come transazione. Si noti che il buono regalo non riduce l'importo da fatturare.

Per rivedere i buoni regalo emessi e applicati, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Buoni regalo**, quindi scegli il collegamento correlato.

## Vedere anche

[Iniziare a usare il connettore per Shopify](get-started.md)  
