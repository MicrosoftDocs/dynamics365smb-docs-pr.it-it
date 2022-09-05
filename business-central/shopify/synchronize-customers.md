---
title: Sincronizzare clienti
description: Importare cliente da o esportarli in Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: d4ff86179fa5b82bcc398ee58cf92fc121c486d8
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361423"
---
# <a name="synchronize-customers"></a>Sincronizzare clienti

Quando un ordine viene importato da Shopify, le informazioni sul cliente sono essenziali per l'ulteriore elaborazione del documento in [!INCLUDE[prod_short](../includes/prod_short.md)]. Esistono due opzioni principali per eseguire questa azione e le loro combinazioni:

* Usa un cliente speciale per tutti gli ordini.
* Importa le informazioni sui clienti effettivi da Shopify. Questa opzione è disponibile anche quando esporti prima i clienti in Shopify da [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="how-the-connector-chooses-which-customer-to-use"></a>In che modo il connettore sceglie quale cliente utilizzare

La funzione *Importa ordine da Shopify* cerca di selezionare i clienti nel seguente ordine:

1. Se **Nr. cliente predefinito** è definito nel **Modello cliente Shopify** per il paese corrispondente, **Nr. cliente predefinito** viene utilizzato indipendentemente dalle impostazioni nei campi **Importazione cliente da Shopify** e **Tipo di mapping cliente**. Ulteriori informazioni in [Modello cliente per paese](synchronize-customers.md#customer-template-per-country).
2. Se **Importazione cliente da Shopify** è impostato su *Nessuno* e **Nr. cliente predefinito** è definito nella pagina **Scheda punto vendita Shopify**, il **Nr. cliente predefinito** viene utilizzato.

I prossimi passaggi dipendono dal **Tipo di mapping cliente**.

* Se è **Acquisisci sempre il cliente predefinito**, il connettore utilizza il cliente definito nel campo **Nr. cliente predefinito** nella pagina **Scheda punto vendita Shopify**.
* Se è **Per e-mail/telefono**, il connettore tenta di trovare il cliente esistente prima in base all'ID, quindi tramite e-mail e quindi tramite numero di telefono. Se il cliente non viene trovato, il connettore crea un nuovo cliente.
* Se è **Per informazioni Fatturare a**, il connettore tenta di trovare il cliente esistente prima in base all'ID e poi in base alle informazioni sull'indirizzo di fatturazione. Se il cliente non viene trovato, il connettore crea un nuovo cliente.

> [!NOTE]  
> Il connettore utilizza le informazioni dall'indirizzo di fatturazione e crea il cliente di fatturazione in [!INCLUDE[prod_short](../includes/prod_short.md)]. Il cliente a cui vendere è lo stesso del cliente a cui fatturare.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Impostazioni importanti durante l'importazione di clienti da Shopify

Se importi i clienti da Shopify in blocco o insieme all'importazione degli ordini, le seguenti impostazioni consentono di gestire il processo:

|Campo|Descrizione|
|------|-----------|
|**Importazione cliente da Shopify**|Seleziona **Tutti i clienti** se prevedi di importare clienti da Shopify in blocco; sia manualmente con l'azione **Sincronizza clienti** o tramite la coda dei processi per gli aggiornamenti ricorrenti. Indipendentemente dalla selezione, le informazioni sul cliente verranno sempre importate insieme all'ordine. Tuttavia, l'uso di queste informazioni dipende dai **Modelli cliente Shopify** e le impostazioni nel campo **Tipo di mapping cliente**.|
|**Tipo di mapping cliente**|Definisci come desideri che il connettore esegua il mapping.<br>- **Per e-mail/telefono** se desideri che il connettore mappi il cliente Shopify importato al cliente esistente in [!INCLUDE[prod_short](../includes/prod_short.md)] utilizzando e-mail e telefono.</br>- **Per informazioni Fatturare a** se desideri che il connettore utilizzi l'indirizzo del destinatario fattura per mappare il cliente Shopify importato al cliente esistente in [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Seleziona **Acquisisci sempre il cliente predefinito** se desidera che il sistema utilizzi un cliente da **Nr. cliente predefinito** . |
|**Shopify può aggiornare i clienti**| Seleziona questo campo se desideri che il connettore aggiorni i clienti trovati, quando le opzioni  **Per e-mail/telefono** o **Per informazioni Fatturare a** sono selezionate nl campo **Tipo di mapping cliente**.|
|**Crea automaticamente clienti sconosciuti**| Seleziona questo campo se desideri che il connettore crei clienti mancanti, quando le opzioni **Per e-mail/telefono** o **Per informazioni Fatturare a** sono selezionate nel campo **Tipo di mapping cliente**. Verrà creato un nuovo cliente utilizzando i dati importati e il **Codice modello cliente** definito nelle pagine **Scheda punto vedita Shopify** o **Modello cliente Shopify**. Si noti che il cliente Shopify deve avere almeno un indirizzo. Se questa opzione non è abilitata, dovrai creare il cliente manualmente e collegarlo al cliente Shopify. Puoi sempre avviare la creazione di un cliente manualmente dalla pagina **Ordine Shopify**.|
|**Codice modello cliente**|Questo campo viene usato insieme a **Crea automaticamente clienti sconosciuti**.<br>- Scegli il modello predefinito da utilizzare per i clienti creati automaticamente. Assicurati che il modello selezionato contenga i campi obbligatori, come i campi **Cat. reg. business**, **Cat. reg. cliente**, IVA o campi relativi alle imposte.<br>- È possibile definire modelli per paese/regione nella pagina **Modelli cliente Shopify**, utile per un corretto calcolo delle tasse. <br>- Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Modello cliente per paese

Alcune impostazioni possono essere definite a livello nazionale/regionale o statale/provinciale. Le impostazioni possono essere configurate in [Spedizione e consegna](https://www.shopify.com/admin/settings/shipping) su Shopify.

Puoi eseguire le seguenti operazioni per ogni cliente con il **Modello cliente Shopify**:

1. Specificare **Nr. cliente predefinito**, che ha la priorità sulla selezione nei campi **Importazione cliente da Shopify** e **Tipo di mapping cliente**. Viene utilizzato nell'ordine cliente importato.
2. Definisci il **Codice modello cliente**, che viene utilizzato per creare clienti mancanti, se **Crea automaticamente clienti sconosciuti** è abilitato. Se **Codice modello cliente** è vuoto, la funzione utilizza **Codice modello cliente** definito nella **Scheda punto vendita Shopify**.
3. Definisci se i prezzi includono imposte/IVA per gli ordini importati.
4. In alcuni casi, il **Codice modello cliente** definito per un paese non è sufficiente per garantire il corretto calcolo delle imposte (ad esempio, per i paesi con imposta sulle vendite). In questo caso, l'inclusione delle **Aree fiscali** potrebbe essere un'utile aggiunta.

> [!NOTE]  
> I codici paese sono codici paese ISO 3166-1 alpha-2. Ulteriori informazioni sul [Codice paese](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Esportare clienti su Shopify

I clienti esistenti possono essere esportati in Shopify in blocco. In ogni caso, vengono creati un cliente e un indirizzo predefinito. Puoi gestire il processo utilizzando le seguenti impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Esportare clienti su Shopify**|Seleziona se vuoi esportare tutti i clienti con un indirizzo e-mail valido da [!INCLUDE[prod_short](../includes/prod_short.md)] in Shopify. Puoi farlo manualmente, usando l'azione **Sincronizza i clienti** o automaticamente, utilizzando una coda processi per gli aggiornamenti ricorrenti.<br> Quando esporti clienti con indirizzi che includono province/stati, assicurati che **Codice ISO** sia compilato per paesi/regioni.|
|**Shopify può aggiornare i clienti**|Viene usato insieme all'impostazione **Esporta cliente in Shopify**. Abilitalo, se desideri generare aggiornamenti in un secondo momento da [!INCLUDE[prod_short](../includes/prod_short.md)] per i clienti che già esistono in Shopify.|

> [!NOTE]  
> Dopo aver creato i clienti in Shopify, puoi inviare loro inviti diretti incoraggiandoli ad attivare i loro account.

### <a name="populate-customer-information-in-shopify"></a>Inserisci le informazioni sui clienti in Shopify

Un cliente in Shopify ha nome, cognome, email e/o numero di telefono. Puoi compilare il nome e il cognome dalla scheda cliente in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorità|Campo in scheda cliente|Descrizione|
|------|------|-----------|
|1|**Nome contatto**|Priorità massima, se il campo **Nome contatto** è compilato e il campo **Origine contatto** in **Scheda punto vendita Shopify** contiene l'opzione *Nome e cognome* o *Cognome e Nome* per definire come dividere i valori.|
|2|**Nome 2**|Se il campo **Nome 2** è compilato e il campo **Origine nome 2** nella **Scheda punto vendita Shopify** contiene l'opzione *Nome e cognome* o *Cognome e Nome* per definire come dividere i valori.|
|3|**Nome**|Priorità minima, se il campo **Nome contatto** è compilato e il campo **Origine nome** in **Scheda punto vendita Shopify** contiene le opzioni *Nome e cognome* o *Cognome e Nome* per definire come dividere i valori.|

Un cliente in Shopify ha anche un indirizzo predefinito, che può contenere un'azienda e un indirizzo oltre al nome, cognome, e-mail e/o telefono. Puoi popolare il campo **Azienda** in base ai dati della scheda cliente in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorità|Campo in scheda cliente|Descrizione|
|------|------|-----------|
|1|**Nome**|Priorità massima, se il campo **Origine nome** nella **Scheda punto vednita Shopify** contiene *Nome azienda*.|
|2|**Nome 2**|Priorità più bassa, se il campo **Origine nome 2** nella **Scheda cliente Shopify** contiene *Nome azienda*.|

Per gli indirizzi in cui viene utilizzato il paese/provincia, seleziona *Codice* o *Nome* nel campo **Origine Paese** nella **Scheda punto vendita Shopify**. Specifica il tipo di dati archiviati in [!INCLUDE[prod_short](../includes/prod_short.md)] nel campo **Paese**.

## <a name="sync-customers"></a>Sincronizzare clienti

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita specifico per il quale desideri sincronizzare i clienti.
3. Scegliere l'azione **Sincronizza clienti**.

In alternativa, utilizza l'azione **Avvia sincronizzazione clienti** sulla finestra **Clienti Shopify** o cerca il processo batch **Sincronizzare clienti**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Ulteriori informazioni su [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Vedere anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
