---
title: Sincronizzare clienti e società
description: Importa clienti da o esportali in Shopify.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Sincronizzare clienti e società

Quando importi un ordine da Shopify, le informazioni sul cliente sono essenziali per l'ulteriore elaborazione del documento in [!INCLUDE[prod_short](../includes/prod_short.md)]. Esistono due opzioni principali per eseguire questa azione e varie combinazioni:

* Usa un cliente speciale per tutti gli ordini.
* Importa le informazioni sui clienti da Shopify. Questa opzione è disponibile anche quando esporti clienti in Shopify da [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify ti consente di eseguire la tua attività B2B e DTC da un'unica posizione con la potenza e la facilità della piattaforma tutto in uno di Shopify. Il connettore Shopify funziona anche con diverse versioni di e-commerce.

Shopify ha due entità, cliente e società, ma [!INCLUDE[prod_short](../includes/prod_short.md)] ha solo l'entità cliente, che influisce sul funzionamento della sincronizzazione.

Quando esegui DTC, l'acquirente viene creato in Shopify come cliente. Il cliente viene quindi importato [!INCLUDE[prod_short](../includes/prod_short.md)] come cliente Shopify e collegato o convertito in cliente.

Se esegui B2B, l'acquirente viene creato in Shopify come cliente collegato ad una società. Il cliente viene importato in [!INCLUDE[prod_short](../includes/prod_short.md)] come cliente Shopify e la società viene importata in [!INCLUDE[prod_short](../includes/prod_short.md)] come società Shopify e collegata o convertita in cliente.

Per esportare un cliente da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, i passaggi sono diversi a seconda di ciò che desideri fare:

* Esportare un cliente come cliente Shopify per DTC.
* Esportare un cliente come società e cliente per il flusso B2B.

## Impostazioni importanti durante l'importazione di clienti DTC da Shopify

Importando i clienti da Shopify in blocco o insieme all'importazione degli ordini, le seguenti impostazioni consentono di gestire il processo:

|Campo|Descrizione|
|------|-----------|
|**Importazione cliente da Shopify**|Seleziona **Tutti i clienti** se prevedi di importare clienti da Shopify in blocco; sia manualmente con l'azione **Sincronizza clienti** o tramite la coda dei processi per gli aggiornamenti ricorrenti. Indipendentemente dalla selezione, le informazioni sul cliente verranno sempre importate insieme all'ordine. Tuttavia, l'uso di queste informazioni dipende dai **Modelli cliente Shopify** e le impostazioni nel campo **Tipo di mapping cliente**.|
|**Tipo di mapping cliente**|Definisci come desideri che il connettore esegua il mapping.</br></br>- **Per e-mail/telefono** se desideri che il connettore utilizzi informazioni sull'account e-mail e sul numero di telefono per mappare il cliente Shopify importato a un cliente in Business Central.</br></br>- **Per informazioni Fatturare a** se desideri che il connettore utilizzi l'indirizzo del destinatario della fattura per mappare il cliente Shopify importato a un cliente esistente in Business Central.</br></br>- **Acquisisci sempre il cliente predefinito** consente al sistema di utilizzare un cliente da **Nr. cliente predefinito** . |
|**Shopify può aggiornare i clienti**| Seleziona questo campo se desideri che il connettore aggiorni i clienti trovati, quando le opzioni  **Per e-mail/telefono** o **Per informazioni Fatturare a** sono selezionate nl campo **Tipo di mapping cliente**.|
|**Crea automaticamente clienti sconosciuti**| Seleziona questo campo se desideri che il connettore crei clienti mancanti, quando le opzioni **Per e-mail/telefono** o**Per informazioni Fatturare a** sono selezionate nel campo **Tipo di mapping cliente**. Viene creato un nuovo cliente utilizzando i dati importati e il **Codice modello cliente** definito nelle pagine **Scheda punto vedita Shopify** o **Modello cliente Shopify**. Si noti che il cliente Shopify deve avere almeno un indirizzo. Gli ordini creati tramite il canale di vendita POS Shopify spesso non contengono i dettagli dell'indirizzo. Se questa opzione non è abilitata, devi creare il cliente manualmente e collegarlo al cliente Shopify.|
|**Codice modello cliente/società**|Usa questo campo insieme a **Crea automaticamente clienti sconosciuti**.</br></br>Scegli il modello predefinito da utilizzare per i clienti creati automaticamente. Assicurati che il modello selezionato contenga i campi obbligatori, come i campi **Cat. reg. business**, **Cat. reg. cliente**, IVA o campi relativi alle imposte.</br></br>È possibile definire modelli per paese/area geografica nella pagina **Modelli cliente Shopify**, utile per un calcolo corretto delle tasse.</br></br>Ulteriori informazioni sulla [Configurazione delle imposte](setup-taxes.md).|

### Modello cliente per paese/area geografica

Alcune impostazioni possono essere definite a livello nazionale/regionale o statale/provinciale. Le impostazioni possono essere configurate in [Spedizione e consegna](https://www.shopify.com/admin/settings/shipping) su Shopify.

Puoi eseguire le seguenti operazioni per ogni cliente con il **Modello cliente Shopify**:

1. Specificare **Nr. cliente predefinito**, che ha la priorità sulla selezione nei campi **Importazione cliente da Shopify** e **Tipo di mapping cliente**. Viene utilizzato nell'ordine cliente importato.
2. Definisci il **Codice modello cliente**, che viene utilizzato per creare clienti mancanti, se **Crea automaticamente clienti sconosciuti** è abilitato. Se **Codice modello cliente** è vuoto, la funzione utilizza **Codice modello cliente** definito nella **Scheda punto vendita Shopify**. Il sistema tenta innanzitutto di trovare un modello **Codice paese/area geografica** per l'indirizzo predefinito. Se non trova un modello, usa il primo indirizzo.
3. In alcuni casi, il **Codice modello cliente** definito per un paese/area geografica non è sufficiente per garantire il corretto calcolo delle imposte (ad esempio, per i paesi/aree geografiche con imposta sulle vendite). In questo caso, l'inclusione delle **Area fiscale** potrebbe essere un'utile aggiunta.
4. Il campo **Area imposte** contiene anche un abbinamento **Codice paese** e **Nome regione**. Questa coppia è utile quando il connettore deve convertire un codice in un nome o viceversa.

> [!NOTE]  
> I codici paese sono codici paese ISO 3166-1 alpha-2. Ulteriori informazioni sul [Codice paese](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Impostazioni importanti durante l'esportazione di clienti DTC in Shopify

Puoi esportare i clienti esistenti in Shopify in blocco. In ogni caso, vengono creati un cliente e un indirizzo predefinito. Puoi gestire il processo utilizzando le seguenti impostazioni:

|Campo|Descrizione|
|------|-----------|
|**Shopify può aggiornare i clienti**| Abilitala, se desideri generare aggiornamenti in un secondo momento da Business Central per i clienti che già esistono in Shopify.|

I seguenti sono i requisiti per esportare un cliente:

* Il cliente deve disporre di un indirizzo e-mail valido.
* Quando esporti clienti con indirizzi che includono province/stati, assicurati che **Codice ISO** sia compilato per paesi/aree geografiche.|
* Quando un paese/area geografica è selezionaato nella scheda cliente, assicurati che **Codice ISO** sia specificato. Per i clienti locali, con il paese/area geografica vuoto, il connettore Shopify utilizza il paese/area geografica specificato nella pagina **Informazioni società**.
* Se il cliente ha un numero di telefono, il numero deve essere univoco perché Shopify non accetterà un secondo cliente con lo stesso numero di telefono.
* Se il cliente ha un numero di telefono, deve essere nel formato E.164. Sono supportati diversi formati se rappresentano un numero che può essere composto da qualsiasi luogo del mondo. I seguenti formati sono validi:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Dopo aver creato i clienti in Shopify, puoi inviare loro inviti diretti incoraggiandoli ad attivare i loro account.

### Inserisci le informazioni sui clienti in Shopify

Un cliente in Shopify ha nome, cognome, e-mail e/o numero di telefono. Puoi immettere il nome e il cognome dalla scheda cliente in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorità|Campo in scheda cliente|Descrizione|
|------|------|-----------|
|1|**Nome contatto**|Priorità massima, se il campo **Nome contatto** è compilato e il campo **Origine contatto** in **Scheda punto vendita Shopify** contiene l'opzione *Nome e cognome* o *Cognome e Nome* per definire come dividere i valori.|
|2|**Nome 2**|Se il campo **Nome 2** è compilato e il campo **Origine nome 2** nella **Scheda punto vendita Shopify** contiene l'opzione *Nome e cognome* o *Cognome e Nome* per definire come dividere i valori.|
|3|**Nome**|Priorità minima, se il campo **Nome contatto** è compilato e il campo **Origine nome** in **Scheda punto vendita Shopify** contiene le opzioni *Nome e cognome* o *Cognome e Nome* per definire come dividere i valori.|

Anche un cliente in Shopify ha un indirizzo predefinito. L'indirizzo può contenere un'azienda e un indirizzo oltre al nome, cognome, e-mail e/o telefono. Puoi popolare il campo **Azienda** in base ai dati della scheda cliente in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorità|Campo in scheda cliente|Descrizione|
|------|------|-----------|
|1|**Nome**|Priorità massima, se il campo **Origine nome** nella**Scheda punto vednita Shopify** contiene *Nome azienda*.|
|2|**Nome 2**|Priorità più bassa, se il campo **Origine nome 2** nella **Scheda cliente Shopify** contiene *Nome azienda*.|

Per gli indirizzi in cui viene utilizzato il paese/regione, seleziona **Codice** o **Nome** nel campo **Origine regione** nella pagina **Scheda punto vendita Shopify**. Specifica il tipo di dati archiviati in [!INCLUDE[prod_short](../includes/prod_short.md)] nel campo **Regione**. Ricordati di inizializzare i modelli dei clienti per paese/area geografica in modo che la mappatura del codice/nome della regione sia pronta. 

## Esportare clienti DTC in Shopify

### Sincronizzazione iniziale dei clienti da Business Central a Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") della ricerca. immetti **Clienti Shopify**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Aggiungi cliente**.
3. Nel campo **Codice punto vendita** immetti il primo codice. Se apri la finestra **Clienti Shopify** dalla pagina **Scheda punto vendita**, il codice punto vendita viene compilato automaticamente.
4. Definisci i filtri sui clienti come richiesto. Ad esempio, puoi filtrare in base al codice Paese/area geografica.
5. Selezionare **OK**.

I clienti risultanti vengono creati automaticamente in Shopify con l'indirizzo.

> [!NOTE]  
> La sincronizzazione iniziale dei clienti da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify non considera le impostazioni **Aggiornamento clienti Shopify consentito**.

### Sincronizzare clienti

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita specifico per il quale desideri sincronizzare i clienti.
3. Scegliere l'azione **Sincronizza clienti**.

In alternativa, utilizza l'azione **Avvia sincronizzazione clienti** sulla finestra **Clienti Shopify** o cerca il processo batch **Sincronizzare clienti**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Per ulteriori informazioni, vedi [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

## Società B2B

Se usi B2B in Shopify, oltre ai clienti puoi creare anche società. È possibile collegare uno o più clienti individuali a una società. Puoi anche definire condizioni di pagamento, ubicazioni e cataloghi.

## Impostazioni importanti durante l'importazione di società B2B da Shopify

Importando le società da Shopify in blocco o durante l'importazione di ordini, utilizza le impostazioni nella tabella seguente per gestire il processo.

|Campo|Descrizione|
|------|-----------|
|**Importazione società da Shopify**|Seleziona **Tutte le società** se prevedi di importare clienti da Shopify in blocco, sia manualmente con l'azione **Sincronizza società** o tramite la coda dei processi per gli aggiornamenti ricorrenti. Indipendentemente dalla selezione, le informazioni sul cliente vengono sempre importate insieme all'ordine. Tuttavia, l'uso di queste informazioni dipende dai **Modelli società Shopify** e le impostazioni nel campo **Tipo di mapping società**.|
|**Tipo di mapping società**|Definisci come desideri che il connettore esegua il mapping.</br></br>- **Per e-mail/telefono** se desideri che il connettore mappi le società Shopify importate a un cliente esistente in Business Central utilizzando indirizzo e-mail e numero di telefono del contatto.</br></br>- Seleziona **Acquisisci sempre la società predefinita** se vuoi che il sistema utilizzi la società nel campo **Nr. società predefinita** . |
|**Shopify può aggiornare la società**| Seleziona questo campo se desideri che il connettore aggiorni i clienti trovati, quando l'opzione **Per e-mail/telefono** è selezionata nel campo **Tipo di mapping società**.|
|**Crea automaticamente società sconosciute**| Seleziona questo campo se desideri che il connettore crei nuovi clienti, quando l'opzione **Per e-mail/telefono** è selezionata nel campo **Tipo di mapping società**. Viene creato un nuovo cliente utilizzando i dati importati e il **Codice modello cliente/società** definito nelle pagine **Scheda punto vendita Shopify** o **Modello cliente Shopify**.|
|**Codice modello cliente/società**|Usa questo campo insieme a **Crea automaticamente società sconosciute**.</br></br>- Scegli il modello predefinito da utilizzare per i clienti creati automaticamente. Assicurati che i campi obbligatori siano compilati nel modello, come i campi **Cat. reg. business**, **Cat. reg. cliente**, **IVA** o altri campi relativi alle imposte.</br></br>- È possibile definire modelli per paese/regione nella pagina **Modelli cliente Shopify**, utile per un corretto calcolo delle tasse.</br></br>Per ulteriori informazioni, vedi [Configurazione delle imposte](setup-taxes.md).|

> [!NOTE]  
> La società deve avere un contatto principale. In caso contrario, il connettore ignora la società.
> Viene importata solo l'ubicazione meno recente.
> Viene importato solo il contatto principale.

## Impostazioni importanti durante l'esportazione di società B2B in Shopify

Puoi esportare i clienti esistenti in Shopify in blocco come società. In ogni caso vengono creati una società, un'ubicazione predefinita e un contatto principale. È anche possibile creare un catalogo.

|Campo|Descrizione|
|------|-----------|
|**Aggiornamento società Shopify consentito**| Abilita questa opzione se desideri generare aggiornamenti in un secondo momento da Business Central per le società che già esistono in Shopify.|
|**Autorizzazioni contatto predefinite**| Specifica quali autorizzazioni devono essere assegnate al contatto principale; puoi scegliere tra **Nessuno**, **Solo ordine** e **Amministratore ubicazione**.|
|**Creazione automatica catalogo**| Abilita questa opzione se desideri creare un catalogo che includa tutti i prodotti. Per ogni società esportata viene creato un catalogo.|

## Esportare una società B2B in Shopify

### Sincronizzazione iniziale di società B2B da Business Central a Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. e immetti **Società Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Aggiungi società**.
3. Nel campo **Codice punto vendita** immetti il codice. Se apri la finestra **Società Shopify** dalla pagina **Scheda punto vendita**, il codice punto vendita viene compilato automaticamente.
4. Definisci i filtri sui clienti come richiesto. Ad esempio, puoi filtrare in base al codice Paese/area geografica.
5. Selezionare **OK**.

La società e i clienti risultanti vengono creati automaticamente in Shopify.

> [!NOTE]  
> La sincronizzazione iniziale delle società da [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify non prende in considerazione le impostazioni **Aggiornamento società di Shopify consentito**.

### Sincronizzare una società B2B

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita specifico per il quale desideri sincronizzare i clienti.
3. Scegli l'azione **Sincronizza società**.

In alternativa, utilizza l'azione **Avvia sincronizza società** nella pagina **Società Shopify** o cerca il processo batch **Sincronizza società**.

È possibile pianificare l'attività da eseguire in modo automatizzato. Per ulteriori informazioni, vedi [Programmare le attività ricorrenti](background.md#to-schedule-recurring-tasks).

## Vedere anche

[Iniziare a usare il connettore per Shopify](get-started.md)  
