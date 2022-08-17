---
title: Sincronizzare ed evadere gli ordini cliente
description: Configura ed esegui l'importazione e l'elaborazione dell'ordine cliente da Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: bef02c5fcbc2b6174e8a3f746a97f0e11564dcf6
ms.sourcegitcommit: 902da19b0ab7a3fbc051cd69ab2802f30d0f378f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/01/2022
ms.locfileid: "9213691"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Sincronizzare ed evadere gli ordini cliente

Questo articolo descrive le impostazioni e i passaggi necessari da eseguire per sincronizzare ed evadere gli ordini cliente con Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Impostare l'importazione di ordini nella scheda del punto vendita Shopify

Un ordine Shopify regolare può includere importi extra al subtotale, come spese di spedizione o, se abilitate, mance. Questi importi vengono registrati direttamente nel conto C/G che si desidera utilizzare per tipi di transazione specifici:

- **Conto costo spedizione**
- **Conto buono regalo venduto**, per ulteriori informazioni, vedi [Buono regalo](synchronize-orders.md#gift-cards)
- **Conto mance**  

Abilita **Creazione automatica degli ordini** per creare automaticamente documenti di vendita in [!INCLUDE[prod_short](../includes/prod_short.md)] una volta importato l'ordine Shopify.
Il documento di vendita in[!INCLUDE[prod_short](../includes/prod_short.md)] contiene un collegamento all'ordine Shopify. Se selezioni il campo **Nr. ordine Shopify nella riga documento**, queste informazioni verranno ripetute nelle righe di vendita di tipo *Commento*.

Nel campo **Origine area fiscale**, definisci la priorità su come selezionare il codice area fiscale o il gruppo di registrazione attività IVA in base all'indirizzo. Questo passaggio è rilevante per i paesi con imposta sulle vendite e per quelli con IVA. Ulteriori informazioni su [Note sulle imposte](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Mapping metodo spedizione

Il **Codice metodo di spedizione** per documenti di vendita importati da Shopify può essere compilato automaticamente. Devi configurare il **Mapping metodo di spedizione**.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri definire il mapping per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Mapping metodo di spedizione**. Ciò crea automaticamente record per i metodi di spedizione definiti nelle impostazioni [**Spedizione**](https://www.shopify.com/admin/settings/payments) nel tuo **Amministratore Shopify**.
4. Nel campo **Nome**, puoi vedere il nome del metodo di spedizione da Shopify.
5. Immetti il **Codice metodo di spedizione** con il metodo di spedizione corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Se più spese di spedizione sono associate a un ordine cliente; solo uno verrà selezionato come metodo di spedizione e assegnato al documento di vendita.

### <a name="payment-method-mapping"></a>Mapping metodo di pagamento

Per compilare il **Codice metodo di pagamento** per documenti di vendita importati da Shopify automaticamente, è necessario configurare **Mapping metodo di pagamento**.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri definire il mapping per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Mapping metodo di pagamento**.
4. Nei campi **Gateway** e **Società emittente carte di credito**, immetti il nome del metodo di pagamento da Shopify. Il record viene creato automaticamente quando importi gli ordini Shopify.
5. Immetti il **Codice metodo di pagamento** con il metodo di pagamento corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Imposta la **Priorità** per i casi in cui il cliente utilizza più mezzi di pagamento. Il metodo di pagamento con la priorità più alta viene selezionato nel documento di vendita. Se entrambi i metodi di pagamento hanno la stessa priorità, viene utilizzato il metodo di pagamento con l'importo più alto.

> [!NOTE]  
> Se il metodo di pagamento corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)] ha **Tipo contropartita** e **Nr. contropartita** popolato, durante la registrazione il sistema di fatturazione creerà una voce di bilanciamento del *Pagamento* e applicalo al tipo di *Fattura* nel movimento contabile cliente.

### <a name="location-mapping"></a>Mapping della posizione

Per compilare il **Codice posizione** per documenti di vendita importati da Shopify automaticamente, è necessario configurare le **Posizioni punto vendita Shopify**.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri configurare il mapping delle posizioni per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Posizioni** per aprire le **Posizioni punto vendita Shopify**.
4. Scegli l'azione **Recupera posizioni Shopify** per importare tutte le posizioni definite in Shopify. Puoi trovarli nelle impostazioni [**Posizioni**](https://www.shopify.com/admin/settings/locations) nel pannello **Amministratore Shopify**. Nota che la posizione contrassegnata come *Predefinito* verrà utilizzato durante l'importazione degli ordini Shopify inevasi.
5. Inserisci il **Codice posizione predefinito** con la posizione corrispondente in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> È necessario configurare il mapping della posizione se l'interruttore **Posizione obbligatoria** è abilitato nella scheda **Configurazione inventario**, altrimenti non potrai creare documenti di vendita.

## <a name="run-the-order-synchronization"></a>Eseguire la sincronizzazione degli ordini

Di seguito viene descritto come importare e aggiornare gli ordini di vendita.

> [!NOTE]  
> Gli ordini archiviati in Shopify non possono essere importati. Disattiva l'opzione **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni **Checkout** nel pannello **Amministratore Shopify** per verificare che tutti gli ordini vengano importati in [!INCLUDE[prod_short](../includes/prod_short.md)]. Se devi importare ordini archiviati, usa l'azione **Annulla l'archiviazione degli ordini** nella pagina [Ordini](https://www.shopify.com/admin/orders) del pannello **Amministratore Shopify**.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri importare gli ordini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Ordini**.
4. Scegli l'azione **Sincronizza ordini da Shopify**.
5. Definisci i filtri sugli ordini secondo necessità. Ad esempio, puoi importare ordini interamente pagati o quelli con un livello di rischio basso.
6. Scegli il pulsante **OK**.

In alternativa, puoi cercare il processo batch **Sincronizza ordini da Shopify**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Ulteriori informazioni su [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Esaminare gli ordini importati

Una volta completata l'importazione, puoi esplorare l'ordine Shopify e trovare tutte le informazioni correlate, come transazioni di pagamento, costi di spedizione, adempimenti, livello di rischio, se l'ordine è stato già adempiuto in Shopify. Puoi anche vedere la conferma di ogni ordine inviata al cliente scegliendo l'azione **Pagina di stato Shopify**.

> [!NOTE]  
> Puoi accedere alla finestra **Ordini Shopify** direttamente e vedrai gli ordini con lo stato *aperto* di tutti i punti vendita Per rivedere gli ordini completati, è necessario aprire la pagina **Ordini Shopify** dalla specifica finestra **Scheda del punto vendita Shopify**.

## <a name="create-sales-documents-in-business-central"></a>Creare documenti di vendita in Business Central

Se l'opzione **Creazione automatica ordini** è abilitata nella **Scheda del punto vendita Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tenta di creare un documento di vendita una volta importato l'ordine. Se manca un cliente o un prodotto, dovrai risolvere il problema e quindi creare nuovamente l'ordine di vendita.

### <a name="to-create-sales-documents"></a>Per creare i documenti di vendita

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli ordini per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Ordini**.
4. Seleziona l'ordine per il quale desideri creare un documento di vendita e scegli l'azione **Crea documenti di vendita**.
5. Selezionare **Sì**.

Se l'ordine Shopify richiede l'evasione, l'**Ordine di vendita** viene creato. Per gli ordini Shopify evasi, come gli ordini che contengono solo un buono regalo o che sono già gestiti in Shopify, la **Fattura di vendita** viene creata.

Viene ora creato un documento di vendita che può essere gestito utilizzando le funzionalità di [!INCLUDE[prod_short](../includes/prod_short.md)] standard.

### <a name="manage-missing-customers"></a>Gestire i clienti mancanti

Se le tue impostazioni impediscono la creazione automatica di un cliente e non è possibile trovare un cliente esistente corretto, dovrai assegnare un cliente a un ordine Shopify manualmente. Questa operazione può essere effettuata in vari modi:

- Puoi assegnare **Nr. cliente di vendita** direttamente nella pagina **Ordini Shopify** scegliendo un cliente dall'elenco dei clienti esistenti.
- È possibile selezionare un codice modello cliente, creare e assegnare il cliente tramite l'azione **Crea nuovo cliente** nella pagina **Ordini Shopify**.
- È possibile mappare il cliente esistente al relativo **cliente Shopify** nella finestra **Clienti Shopify** e quindi scegliere l'azione **Trova mapping** nella pagina **Ordini Shopify**.

### <a name="tax-remarks"></a>Note sulle imposte

L'ordine Shopify importato contiene informazioni sulle tasse, ma le tasse vengono ricalcolate quando crei il documento di vendita, quindi è importante che le impostazioni tasse/aliquote siano corrette in [!INCLUDE[prod_short](../includes/prod_short.md)].

- Tasse/aliquote IVA multiple sui prodotti. Ad esempio, alcune categorie di prodotti sono soggette a aliquote fiscali ridotte. Tali elementi devono esistere in [!INCLUDE[prod_short](../includes/prod_short.md)] ed essere mappati ai prodotto Shopify. In caso contrario, con la creazione automatica degli articoli mancanti, viene utilizzato il gruppo di registrazione dei prodotti IVA.

- Aliquote fiscali dipendenti dall'indirizzo. Usa il campo **Priorità area fiscale** insieme alla tabella **Modelli per clienti** per sovrascrivere la logica standard che riempie il **Codice area Fiscale** nel documento di vendita. Il campo **Priorità area fiscale** specifica la priorità utilizzata per determinare le informazioni su paese/area geografica e stato/provincia. Quindi il record corrispondente nei modelli cliente Shopify viene trovato e **Codice area fiscale**, **debito fiscale** e **Cat. Reg. Business IVA** viene utilizzata quando viene creato un documento di vendita.

- Prezzi imposta inclusa Il campo **Prezzi imposta inclusa**/**Prezzi IVA inclusa** nel documento di vendita creato non dipende dal cliente, ma dal **Modello cliente** della pagina **punto vendita Shopify** o dal modello cliente per paese.

### <a name="impact-of-order-editing"></a>Impatto delle modifiche degli ordini

In Shopify:

|Modifica|Impatto|
|------|-----------|
|Cambia la posizione di evasione | La posizione originale verrà sincronizzata con [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Modifica un ordine e modifica la quantità| L'intestazione dell'ordine e le tabelle supplementari verranno aggiornate in [!INCLUDE[prod_short](../includes/prod_short.md)], non le righe. |
|Modifica un ordine e aggiungi nuovo articolo | L'intestazione dell'ordine verrà aggiornata, le righe no. |

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Modifica|Impatto|
|------|-----------|
|Cambia la posizione in un'altra posizione, mappata alle posizioni Shopify. Registra spedizione. | Dopo aver sincronizzato l'evasione, la posizione verrà aggiornata in Shopify. |
|Cambia la posizione in un'altra posizione, non mappata alle posizioni Shopify. Registra spedizione. | L'evasione non verrà sincronizzata con Shopify. |
|Cambia la riduzione quantità. Registra spedizione. | L'ordine in Shopify sarà contrassegnato come parzialmente evaso. |
|Aggiungi un nuovo articolo. Registra spedizione. | L'ordine in Shopify sarà contrassegnato come evaso. Le righe non verranno aggiornate. |

## <a name="synchronize-shipments-to-shopify"></a>Sincronizzare le spedizioni con Shopify

Quando un ordine cliente creato da un ordine Shopify viene spedito, è possibile sincronizzare le spedizioni con Shopify.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Sincronizza spedizioni con Shopify**, quindi scegli il collegamento correlato.
2. Definisci i filtri sulle spedizioni secondo necessità. Ad esempio, puoi aggiornare una spedizione registrata in una data specifica.
3. Scegli il pulsante **OK**.

L'ordine in Shopify sarà contrassegnato come evaso. Il cliente riceve automaticamente un messaggio e-mail o SMS di avviso di spedizione. Se sulla spedizione sono specificati un agente di spedizione e un codice di tracciabilità, le informazioni di tracciabilità sono incluse nell'e-mail.

> [!NOTE]  
> Ricordati di eseguire **Sincronizza ordini da Shopify** per aggiornare lo stato di evasione di un ordine in [!INCLUDE[prod_short](../includes/prod_short.md)]. La funzionalità del connettore archivia anche gli ordini completamente pagati ed evasi in entrambi Shopify e in [!INCLUDE[prod_short](../includes/prod_short.md)] purché le condizioni siano soddisfatte.

### <a name="shipping-agents-and-tracking-url"></a>Agenti di spedizione e URL di tracciamento

Se il documento **Spedizione vendita registrate** contiene il **codice Spedizioniere** e/o il **Numero di tracciabilità del pacco**, queste informazioni saranno inviate a Shopify e al cliente nell'e-mail di conferma della spedizione.

La società di tracciamento viene popolata in base allo spedizioniere con le seguenti priorità (dalla più alta alla più bassa):

- **Società tracciabilità Shopify**
- **Nome**
- **Codice**

Se il campo **URL tracciabilità pacchetto** è compilato per il record dello spedizioniere, la conferma della spedizione conterrà anche un URL di tracciamento.

## <a name="gift-cards"></a>Buoni regalo

Nel punto vendita Shopify puoi vendere buoni regalo, che possono essere utilizzati per pagare prodotti reali.

Quando si tratta di buoni regalo, è importante inserire un valore nel campo **Conto buono regalo venduto** nella finestra **Scheda punto vendita Shopify**. Il buono regalo venduto verrà sincronizzato insieme agli ordini in linea. Con l'ordine verrà importato anche un buono regalo applicato, ma ora come transazione. Si noti che il buono regalo non riduce l'importo da fatturare.

Per rivedere i buoni regalo emessi e applicati, scegli l'icona a forma di ![lampadina che che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Buoni regalo**, quindi scegli il collegamento correlato.

## <a name="transactions-and-payouts"></a>Transazioni e pagamenti

Quando un cliente completa il pagamento nel negozio online, le informazioni sui pagamenti vengono salvate come **Transazione**. Potrebbero esserci più transazioni collegate all'ordine, ad esempio quando un cliente utilizza una carta regalo per pagare parte del costo e quindi utilizza una carta di credito o PayPal per l'importo rimanente. 

Se usi Shopify Payment come fornitore di servizi di pagamento, quindi oltre alle informazioni sul denaro ricevuto dal cliente dal fornitore di servizi di pagamento, puoi anche visualizzare i pagamenti da Shopify sul tuo conto bancario. 

### <a name="transactions"></a>Transazioni

Le operazioni di pagamento avvenute in Shopify sono sincronizzate insieme agli ordini e possono essere visualizzate dalla pagina *Ordini Shopify*.

Per rivedere tutte le transazioni, scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Transazioni** e scegli il collegamento correlato.

Se hai configurato la mappatura del metodo di pagamento il documento di vendita creato verrà assegnato un codice metodo di pagamento. Ulteriori informazioni su [Mappatura del metodo di pagamento](#payment-method-mapping).

### <a name="payouts"></a>Pagamenti

Se nel tuo negozio usi Shopify Payment, riceverai i pagamenti tramite *Pagamenti Shopify* quando un cliente paga utilizzando Shopify Payments e i checkout accelerati.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare i pagamenti per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Sincronizza pagamenti**.

Per rivedere tutti i pagamenti, scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Pagamenti** e scegli il collegamento correlato.

I **Pagamenti** sono solo a scopo informativo e non influiscono sulla contabilità generale o sui movimenti contabili bancari, sebbene possano essere utili durante l'elaborazione dell'estratto conto bancario.

## <a name="see-also"></a>Vedere anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
