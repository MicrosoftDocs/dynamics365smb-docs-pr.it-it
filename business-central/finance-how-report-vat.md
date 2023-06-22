---
title: Inviare la dichiarazione IVA alle autorità fiscali
description: 'Informazioni su come preparare un report che elenca l''IVA di vendita durante un periodo, o di vendite e acquisti, e inviarlo a un''autorità fiscale.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 01/31/2022
ms.author: bholtorf
---

# <a name="report-vat-to-tax-authorities" />Dichiarare l'IVA all'autorità fiscale

Questo argomento descrive i report [!INCLUDE[prod_short](includes/prod_short.md)] che si possono utilizzare per inviare informazioni sugli importi IVA di vendite e di acquisti all'autorità fiscale del proprio paese. A seconda del paese specifico, i report possono includere informazioni specifiche o possono essere presenti report aggiuntivi da inviare. Controlla gli articoli per il tuo paese nella sezione [Funzionalità locale](about-localization.md).  

È possibile utilizzare i seguenti report predefiniti:

* Il report **Lista vendite UE**  

    Il report Lista vendite UE elenca gli importi IVA che l'azienda ha raccolto con la vendita a clienti con partita IVA nei paesi dell'Unione Europea.  
* Il report **Dichiarazione IVA**  

    Il report Dichiarazione IVA include gli importi IVA per vendite e acquisti a clienti e da fornitori in tutti i paesi che utilizzano l'IVA.  

In entrambi i casi (come in altri report relativi all'IVA), l'IVA viene calcolata in base al setup registrazioni IVA e alle categorie di registrazione IVA impostate. [!INCLUDE[prod_short](includes/prod_short.md)] mostra i movimenti IVA sempre in base alla loro **data IVA** come data di dichiarazione principale.  

> [!NOTE]
> Tutti i report relativi all'IVA ora vengono eseguiti utilizzando la **Data IVA** per filtrare i record pertinenti. Anche se imposti **Utilizzo data IVA** come **Non utilizzare la funzionalità Data IVA** [!INCLUDE[prod_short](includes/prod_short.md)] nasconderà tutte le istanze di **Data IVA** in tutta l'applicazione. Tuttavia, la **Data IVA** è ancora utilizzata in tutti i report e viene compilata automaticamente con la **Data di registrazione**.

Se si desidera visualizzare uno storico completo delle voci di IVA, ogni registrazione che implica l'iVA crea una voce nella pagina **Movimenti IVA**. Questi movimenti vengono utilizzati per calcolare l'importo della liquidazione dell'IVA, ovvero un versamento o un rimborso, per un periodo specifico. Per vedere i movimenti IVA, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimenti IVA**, quindi scegli il collegamento correlato.

> [!NOTE]
> Ogni ambiente [!INCLUDE[prod_short](includes/prod_short.md)] è destinato a gestire le dichiarazioni in base alle normative in un singolo paese. Ad esempio, la versione olandese di [!INCLUDE[prod_short](includes/prod_short.md)] gestisce le dichiarazioni IVA nei Paesi Bassi ma non in altri paesi. Allo stesso modo, la versione americana di [!INCLUDE[prod_short](includes/prod_short.md)] gestisce la dichiarazione 1099 negli Stati Uniti e non supporta la richiesta di dichiarazione IVA in altri paesi, a meno che non sia portata da un'estensione fornita dall'ecosistema partner o da una modifica del codice specifica del cliente.

## <a name="a-nameecsaleslistaabout-the-ec-sales-list-report" /><a name="ecsaleslist"></a>Informazioni sul report Lista vendite UE

Nell'Unione Europea (UE) e nel Regno Unito, tutte le società che vendono beni e servizi a clienti con partita IVA, inclusi i clienti in altri paesi dell'Unione Europea (UE), è necessario inviare una versione elettronica del report Lista vendite UE ai clienti e alle autorità fiscali. Il report **Lista vendite UE** è valido solo per i paesi dell'Unione Europea.

Il report include una riga per ogni tipo di transazione con il cliente e visualizza l'importo totale per ogni tipo di transazione. Esistono tre tipi di transazioni che il report può includere:  

* Prodotti B2B  
* Servizi B2B  
* Prodotti di triangolazione B2B  

I prodotti e i servizi *B2B* specificano se sono stati venduti prodotti o servizi e vengono controllati dall'impostazione **Assistenza UE** nel setup registrazioni IVA. I *prodotti di triangolazione B2B* indicano se è stato attivato un commercio con terze parti e vengono controllati dall'impostazione **Triangolazione intracomunitaria** nei documenti di vendita, ad esempio ordini di vendita, fatture, note di credito e così via.  

Dopo che l'autorità fiscale ha esaminato il report, invia un messaggio e-mail alla persona per la società. In [!INCLUDE[prod_short](includes/prod_short.md)], il nome del contatto è specificato nella pagina **Informazioni società**. Prima di inviare il report, assicurarsi che il contatto sia stato selezionato.  

### <a name="submit-an-ec-sales-list-report" />Inviare un report Lista vendite UE

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="a-namevatreturnaabout-the-vat-return-report" /><a name="vatreturn"></a>Informazioni sul report Dichiarazione IVA

Utilizzare questo report per inviare l'IVA per i documenti di vendita e di acquisto, ad esempio gli ordini vendita e gli ordini acquisto, le fatture e le note di credito. Le informazioni nel report vengono mostrate nello stesso formato di quello utilizzato nel modulo di dichiarazione delle autorità fiscali e doganali.  

Per la dichiarazione IVA è possibile specificare i movimenti per includere:

* Inviare solo le transazioni aperte, o aperte e chiuse. Questo approccio è utile, ad esempio, quando si prepara la dichiarazione IVA di fine anno.
* Inviare solo movimenti da periodi specificati, o includere anche i movimenti di periodi precedenti. Ciò risulta utile quando si deve aggiornare la dichiarazione IVA già inviata, ad esempio, se un fornitore invia una fattura in ritardo.    

## <a name="to-connect-to-your-tax-authoritys-web-service" />Per connettersi al servizio Web dell'autorità fiscale
[!INCLUDE[prod_short](includes/prod_short.md)] include le connessioni di servizio ai siti Web delle autorità fiscali. Nel Regno Unito, ad esempio, è possibile abilitare la connessione di servizio **GovTalk** per inviare elettronicamente i report Lista vendite UE e Dichiarazione IVA. Se si desidera inviare il report manualmente, ad esempio inserendo i dati sul sito Web dell'autorità fiscale, questa connessione non è necessaria.   

Per dichiarare l'IVA a un'autorità fiscale elettronicamente, è necessario connettere [!INCLUDE[prod_short](includes/prod_short.md)] al servizio Web dell'autorità fiscale. Tale soluzione richiede l'impostazione di un account con l'autorità fiscale. Dopo avere impostato un account, è possibile abilitare la connessione di servizio fornita in [!INCLUDE[prod_short](includes/prod_short.md)].

1. Scegli la ![lampadina che apre la funzione Dimmi 2](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Connessioni servizio**, quindi scegli il collegamento appropriato.
2. Compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > È consigliabile testare la connessione. A tal fine, seleziona la casella di controllo **Modalità di test**, quindi prepara e invia la dichiarazione IVA come descritto nella sezione [Per preparare e inviare una dichiarazione IVA](#to-prepare-and-submit-a-vat-report). Mentre è attiva la modalità di test, il servizio verifica se l'autorità fiscale può ricevere la dichiarazione e lo stato del report indicherà se l'invio ha avuto esito positivo. È importante ricordare che non si tratta di un invio effettivo. Per inviare realmente il report, è necessario deselezionare la casella di controllo **Modalità di test** e quindi ripetere la procedura di invio.

## <a name="to-set-up-vat-reports-in-includeprodshortincludesprodshortmd" />Per impostare i report IVA in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods" />Per impostare i periodi di dichiarazione IVA

Facoltativamente, se la tua attività non si trova nel Regno Unito, utilizza la pagina **Periodi di dichiarazione IVA** per impostare le dichiarazioni IVA programmate. Se la tua attività si trova nel Regno Unito, vedi [Rendere le imposte digitali nel Regno Unito](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Periodi di dichiarazione IVA**, quindi scegli il collegamento correlato.  
2. Nella pagina **Periodi di dichiarazione IVA** compila i campi per impostare il primo periodo. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Ripeti il passaggio 2 per tutti i periodi aggiuntivi che vuoi aggiungere.  

Ora, quando è giunto il momento di presentare una dichiarazione IVA per un periodo di dichiarazione IVA, scegli il periodo nella pagina **Periodi di dichiarazione IVA** quindi scegli l'azione **Crea dichiarazione IVA**. Poi, nella scheda **Dichiarazione IVA** scegli l'azione **Suggerisci righe** come descritto nel passaggio 3 della procedura seguente.  

## <a name="to-prepare-and-submit-a-vat-report" />Per salvare e inviare un report IVA

1. Scegli la ![lampadina che apre la funzione Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Lista vendite UE** o **Dichiarazione IVA**, quindi seleziona il collegamento correlato.  
2. Scegliere **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per generare il contenuto del report, scegliere l'azione **Suggerisci righe**.  

    > [!NOTE]  
    >  Nel report Lista vendite UE, è possibile rivedere le transazioni incluse nelle righe del report prima di inviarlo. A tale scopo, selezionare la riga e scegliere l'azione **Mostra movimenti IVA**.  

4. Per convalidare e preparare il report per l'invio, scegliere l'azione **Rilascio**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] verifica che il report sia impostato correttamente. Se la convalida ha esito negativo, gli errori vengono visualizzati in **Errori e avvisi** per consentirne la correzione. In genere, se il messaggio è relativo a un'impostazione mancante in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile fare clic sul messaggio per aprire la pagina che contiene le informazioni da correggere.  
5. Per inviare il report, scegliere l'azione **Invia**.  

Dopo avere inviato il report, [!INCLUDE[prod_short](includes/prod_short.md)] controlla il servizio e memorizza un record delle comunicazioni. Il campo **Stato** indica se il report è in esecuzione. Ad esempio, quando le autorità elaborano il report, lo stato del report diventa **Operazione completata**. Se l'autorità fiscale trova errori nel report inviato, lo stato del report diventa **Operazione non riuscita**. È possibile visualizzare gli errori in **Errori e avvisi**, correggerli e quindi inviare il report nuovamente. Per visualizzare un elenco di tutti i report Lista vendite UE, andare alla pagina **Report lista vendite UE**.  

### <a name="vat-return-statuses" />Stato dichiarazione IVA

Le dichiarazioni IVA possono avere stati diversi, come descritto nella tabella seguente.

| Stato | Descrizione |
|------------|-------------------------|
| Apri | Quando crei una nuova dichiarazione IVA. Puoi eseguire l'azione **Suggerisci righe**. Se devi correggere i valori, puoi eseguire nuovamente l'azione **Suggerisci righe**. Non puoi inviare una dichiarazione IVA con questo stato. |
| Rilasciato | Lo stato verrà modificato quando utilizzi l'azione **Rilascia**. [!INCLUDE[prod_short](includes/prod_short.md)] mostrerà la Scheda dettaglio **Errori e avvisi**. Non puoi apportare modifiche o utilizzare l'azione **Suggerisci righe**. Per apportare modifiche è necessario riaprire la dichiarazione IVA. |
| Rifiutato | Se l'invio non è andato a buon fine (ad esempio, se l'autenticazione non è riuscita), lo stato cambierà in **Rifiutato**. Non puoi riaprire una dichiarazione IVA con questo stato. |
| Inviato | La dichiarazione IVA viene inviata utilizzando l'azione **Invia** oppure viene contrassegnata come inviata utilizzando l'azione **Segna come inviata**. |
| Accettato | La dichiarazione IVA ha questo stato se il report è contrassegnato come accettato utilizzando l'azione **Segna come accettato**. Se il report **Dichiarazione IVA** è contrassegnato come **Accettato** puoi eseguire l'azione **Calcola e registra liquidazione IVA**. |

## <a name="viewing-communications-with-your-tax-authority" />Visualizzare le comunicazioni con l'autorità fiscale

In alcuni paesi, quando si invia il report si scambiano messaggi con l'autorità fiscale. È possibile visualizzare il primo e l'ultimo messaggio inviato o ricevuto scegliendo l'azione **Scarica messaggio di invio** e **Scarica messaggio di risposta**.  

## <a name="submitting-vat-reports-manually" />Inviare i report IVA manualmente
Se si utilizza un altro metodo per presentare il report, ad esempio esportando l'XML e caricandolo in un sito Web dell'autorità fiscale, in seguito sarà possibile scegliere **Contrassegna come Inviato** per chiudere il periodo contabile. Quando il report viene contrassegnato come rilasciato, non può più essere modificato. Se si deve modificare il report dopo averlo contrassegnato come rilasciato, è necessario riaprirlo.

## <a name="vat-settlement" />Liquidazione IVA
Periodicamente, è necessario rimettere l'IVA netta alle autorità fiscali. Se occorre liquidare l'IVA frequentemente, è possibile eseguire il processo batch **Calcolo e registrazione liquidazione IVA** per chiudere i movimenti IVA aperti e trasferire gli importi IVA di vendita e di acquisto nel conto di liquidazione IVA.

Quando si trasferiscono gli importi IVA nel conto di liquidazione, il conto relativo all'IVA acquisti viene accreditato mentre il conto relativo all'IVA vendite viene addebitato in base all'importo calcolato per il periodo specificato. L'importo netto viene accreditato sul conto di liquidazione dell'IVA. Nel caso in cui l'importo dell'IVA acquisti sia maggiore, l'importo netto verrà addebitato. È possibile registrare la liquidazione immediatamente o stampare prima un report di test.  

> [!Note]
> Quando si utilizza il processo batch **Calcolo e registrazione liquidazione IVA**, non si specifica una **Cat. reg. business IVA** e una **Cat. reg. art./serv. IVA**, vengono inclusi i movimenti con tutte le categorie di registrazione e i codici categoria di registrazione articoli/servizi IVA.

## <a name="configuring-your-own-vat-reports" />Configurazione dei report IVA personalizzati

Puoi usare il report **Lista vendite UE** predefinito. Tuttavia, puoi anche creare i tuoi report, se disponi di una licenza di sviluppo, in modo da poter creare codeunit. Per assistenza, contatta un partner Microsoft.  

Nella tabella seguente sono descritte le codeunit da creare per il report.  

| Codeunit | Operazione che deve eseguire |
|----|-----|
|Suggerisci righe| Recupera le informazioni contenute nella tabella **Movimenti IVA** e visualizzale nelle righe del report IVA.|
|Contenuto | Controllare il formato del report. Ad esempio, se è JSON o XML. Il formato da utilizzare varia a seconda dei requisiti del service Web dell'autorità fiscale |
|Invio | Controllare come e quando il report viene inviato in base ai requisiti dell'autorità fiscale. |
|Gestore risposte | Gestire le risposte dell'autorità fiscale. Ad esempio, potrebbe inviare un messaggio e-mail al contatto della società. |
|Annulla | Inviare un annullamento di un report IVA inviato in precedenza all'autorità fiscale. |  

> [!Note]
> Quando crei le codeunit per il report, presta attenzione al valore nel campo **Versione report IVA**. Questo campo deve riflettere la versione del report che è o era richiesto dall'autorità fiscale. Ad esempio, si potrebbe immettere **2021** nel campo per indicare che il report è conforme ai requisiti in essere in quell'anno. Per individuare la versione corrente, contattare l'autorità fiscale.  

## <a name="see-related-microsoft-trainingtrainingpathsprocess-vat-dynamics--business-central" />Vedi il relativo [training Microsoft](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Setup dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Impostare le vendite](sales-setup-sales.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
