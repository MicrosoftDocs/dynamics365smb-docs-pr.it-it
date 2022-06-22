---
title: Sincronizzare clienti
description: Importare cliente da o esportarli in Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 75c4de7736572ff923c74464dc33b218d0665e3f
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808864"
---
# <a name="synchronize-customers"></a>Sincronizzare clienti

Quando un ordine viene importato da Shopify, le informazioni sul cliente sono essenziali per l'ulteriore elaborazione del documento in [!INCLUDE[prod_short](../includes/prod_short.md)]. Esistono due opzioni principali e le loro combinazioni:

* Usa il cliente speciale per tutti gli ordini.
* Importa le informazioni sui clienti effettivi da Shopify. Questa opzione è disponibile anche quando esporti prima un cliente in Shopify da [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="how-connector-chooses-which-customer-to-use"></a>In che modo il connettore sceglie quale cliente utilizzare

La funzione *Importa ordine da Shopify* cerca di selezionare il cliente nel seguente ordine:

1. Se **Nr. cliente predefinito** è definito nel **Modello cliente Shopify** per il paese corrispondente, **Nr. cliente predefinito** viene utilizzato indipendentemente dalle impostazioni in **Importazione cliente da Shopify** e **Tipo di mapping cliente**. Per ulteriori informazioni, vedi [Modello cliente per paese](synchronize-customers.md#customer-template-per-country).
2. Se **Importazione cliente da Shopify** è impostato su *Nessuno* e **Nr. cliente predefinito** è definito nella **Scheda punto vendita Shopify**, il **Nr. cliente predefinito** viene utilizzato.

I prossimi passaggi dipendono da **Tipo di mapping cliente**.

* **Acquisisci sempre il cliente predefinito**, quindi utilizza il cliente definito nel campo **Nr. cliente predefinito** nella finestra **Scheda punto vendita Shopify**.
* **Per e-mail/telefono**, il connettore tenta di trovare il cliente esistente prima in base all'ID, quindi tramite e-mail e quindi tramite telefono. Se il cliente non viene trovato, il connettore crea un nuovo cliente.
* **Per informazioni Fatturare a**, il connettore tenta di trovare il cliente esistente prima in base all'ID e poi in base alle informazioni sull'indirizzo di fatturazione. Se non viene trovato, il connettore crea un nuovo cliente.

> [!NOTE]  
> Il connettore utilizza le informazioni dall'indirizzo di fatturazione e crea il cliente di fatturazione in [!INCLUDE[prod_short](../includes/prod_short.md)]. Il cliente a cui vendere è uguale a cliente a cui fatturare.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Impostazioni importanti durante l'importazione di clienti da Shopify

Importa i clienti da Shopify in blocco o insieme all'importazione degli ordini, le seguenti impostazioni consentono di gestire il processo:

|Campo|Descrizione|
|------|-----------|
|**Importazione cliente da Shopify**|Seleziona **Tutti i clienti** se prevedi di importare clienti da Shopify in blocco; sia manualmente con l'azione **Sincronizza clienti** o tramite la coda dei processi per gli aggiornamenti ricorrenti. Indipendentemente dalla selezione, le informazioni sul cliente verranno sempre importate insieme all'ordine. Tuttavia, l'uso di queste informazioni dipendedai **Modelli cliente Shopify** e le impostazioni nel campo **Tipo di mapping cliente**.|
|**Tipo di mapping cliente**|Definisci come desideri che il connettore esegua il mapping.<br>- **Per e-mail/telefono** se desideri che il connettore mappi il cliente Shopify importato al cliente esistente in[!INCLUDE[prod_short](../includes/prod_short.md)] utilizzando e-mail e telefono.</br>- **Per informazioni Fatturare a** se desideri che il connettore mappi il cliente Shopify importato al cliente esistente in [!INCLUDE[prod_short](../includes/prod_short.md)] utilizzando le informazioni sull'indirizzo della parte che riceve la fattura.</br>Seleziona **Acquisisci sempre il cliente predefinito** se desidera che il sistema utilizzi un cliente da **Nr. cliente predefinito** . |
|**Shopify può aggiornare i clienti**| Seleziona se desideri che il connettore aggiorni i clienti trovati, quando le opzioni  **Per e-mail/telefono** o **Per informazioni Fatturare a** sono selezionate nl campo **Tipo di mapping cliente**.|
|**Crea automaticamente clienti sconosciuti**| Selezionare se si desidera che il connettore crei clienti mancanti, quando le opzioni **Per e-mail/telefono** o **Per informazioni Fatturare a** sono selezionate nel campo **Tipo di mapping cliente**. Verrà creato un nuovo cliente utilizzando i dati importati e **Codice modello cliente** definito nelle pagine **Scheda punto vedita Shopify** o **Modello cliente Shopify**. Si noti che il cliente Shopify deve avere almeno un indirizzo. Se questa opzione non è abilitata, dovrai creare il Cliente canualmente e collegarlo al cliente Shopify. Puoi sempre avviare la creazione di un cliente manualmente dalla pagina **Ordine Shopify**.|
|**Codice modello cliente**|Usato insieme a **Crea automaticamente clienti sconosciuti**.<br> Scegli il modello predefinito da utilizzare per i clienti creati automaticamente. È possibile definire modelli per paese/regione nella finestra **Modelli cliente Shopify**, utile per un corretto calcolo delle tasse. Per ulteriori informazioni, vedere [Note sulle imposte](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Modello cliente per paese

Alcune impostazioni possono essere definite a livello nazionale/regionale o statale/provinciale. Le impostazioni possono essere configurate in [Spedizione e consegna](https://www.shopify.com/admin/settings/shipping) su Shopify.

**Modello cliente Shopify** consente di fare quanto segue per ogni paese:

1. Specificare **Nr. cliente predefinito**, che ha la priorità sulla selezione nei campi **Importazione cliente da Shopify** e **Tipo di mapping cliente**. Viene utilizzato nell'ordine cliente importato.
2. Definisci il **Codice modello cliente**, che viene utilizzato per creare clienti mancanti, se **Crea automaticamente clienti sconosciuti** è abilitato. Se **Codice modello cliente** è vuoto, la funzione utilizza **Codice modello cliente** definito nella **Scheda punto vendita Shopify**.
3. In alcuni casi, **Codice modello cliente** per paese non è sufficiente per garantire il corretto calcolo delle tasse. Ad esempio, per i paesi con imposta sulle vendite.

> [!NOTE]  
> I codici paese sono codici paese ISO 3166-1 alpha-2. Per altre informazioni, vedi [Codice paese](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Esportare clienti su Shopify

I clienti esistenti possono essere esportati in Shopify in blocco. Di conseguenza, vengono creati un cliente e un indirizzo predefinito. Puoi gestire il processo con l'aiuto delle seguenti impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Esportare clienti su Shopify**|Seleziona se prevedi di esportare tutti i clienti con un indirizzo e-mail valido da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify in blocco; manualmente, usando l'azione **Sincronizza clienti** o tramite la coda processi per gli aggiornamenti ricorrenti.|
|**Shopify può aggiornare i clienti**|Usato insieme a **Esporta cliente in Shopify**. Abilitalo, se desideri generare aggiornamenti in un secondo momento da [!INCLUDE[prod_short](../includes/prod_short.md)] per i clienti che già esistono in Shopify.|

> [!NOTE]  
> Dopo aver creato clienti in Shopify, è consigliabile inviare inviti diretti ai clienti. Li incoraggerà ad attivare il proprio account.

### <a name="populate-customer-information-in-shopify"></a>Inserisci le informazioni sui clienti in Shopify

Un cliente in Shopify ha nome, cognome, email e/o numero di telefono. Puoi compilare il nome e il cognome dalla scheda cliente in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorità|Campo in scheda cliente|Descrizione|
|------|------|-----------|
|1|**Nome contatto**|Priorità massima, se il campo **Nome contatto** è compilato e il campo **Origine contatto** in **Scheda punto vendita Shopify** contiene le opzioni *Nome e cognome* o *Cognome e Nome*, definendo come dividere i valori.|
|2|**Nome 2**|Se il campo **Nome 2** è compilato e il campo **Origine nome 2** nella **Scheda punto vendita Shopify** contiene le opzioni *Nome e cognome* o *Cognome e Nome* definendo come dividere i valori.|
|3|**Nome**|Priorità minima, se il campo **Nome contatto** è compilato e il campo **Origine nome** in **Scheda punto vendita Shopify** contiene le opzioni *Nome e cognome* o *Cognome e Nome*, definendo come dividere i valori.|

Un cliente in Shopify ha anche un indirizzo predefinito, che oltre a nome, cognome, email e/o telefono può contenere azienda e indirizzo. Puoi popolare il campo **Azienda** in base ai dati della scheda cliente in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorità|Campo in scheda cliente|Descrizione|
|------|------|-----------|
|1|**Nome**|Priorità massima, se il campo **Origine nome** nella **Scheda punto vednita Shopify** contiene *Nome azienda*.|
|2|**Nome 2**|Priorità più bassa, se il campo **Origine nome 2** nella **Scheda cliente Shopify** contiene *Nome azienda*.|

Per gli indirizzi in cui viene utilizzato il paese/provincia, seleziona *Codice* o *Nome* nel vampo **Origine Paese** nella **Scheda punto vendita Shopify** per specificare quale tipo di dati sono archiviati in[!INCLUDE[prod_short](../includes/prod_short.md)] nel campo **Paese**.

## <a name="sync-customers"></a>Sincronizzare clienti

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri sincronizzare i clienti per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Sincronizza clienti**.

In alternativa, puoi utilizzare l'azione **Avvia sincronizzazione clienti** sulla finestra **Clienti Shopify** o cerca il processo batch **Sincronizzare clienti**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Per ulteriori informazioni, vedi [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
