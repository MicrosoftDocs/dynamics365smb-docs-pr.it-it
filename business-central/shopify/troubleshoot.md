---
title: Risoluzione dei problemi di sincronizzazione tra Shopify Business Central
description: Scopri cosa fare in caso di errore durante la sincronizzazione dei dati tra Shopify e Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Risoluzione dei problemi di sincronizzazione tra Shopify Business Central

È possibile imbattersi in situazioni in cui è necessario risolvere i problemi quando si sincronizzano i dati tra Shopify e [!INCLUDE[prod_short](../includes/prod_short.md)]. Questa pagina definisce i passaggi per la risoluzione dei problemi di alcuni scenari tipici che potrebbero verificarsi.

## <a name="run-tasks-in-the-foreground"></a>Eseguire attività in primo piano

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri risolvere i problemi per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Disattiva l'opzione **Consenti sincronizzazioni in background**.

Ora, quando viene attivata l'azione di sincronizzazione, l'attività verrà eseguita in primo piano. Se si verifica un errore, viene visualizzata una finestra di dialogo di errore con un collegamento **Copia dettagli**. Utilizza il collegamento per copiare informazioni in un editor di testo per ulteriori analisi.

## <a name="logs"></a>Log

Se un'attività di sincronizzazione non riesce, puoi attivare l'interruttore **Registro abilitato** nella pagina **Scheda punto vendita Shopify** per attivare la registrazione. Quindi attiva manualmente l'attività di sincronizzazione e rivedi i log.

### <a name="to-enable-logging"></a>Per abilitare la registrazione

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri risolvere i problemi per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Abilita l'interruttore **Log abilitato**.

### <a name="to-review-logs"></a>Per esaminare i registri

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Movimenti di registri Shopify**, quindi scegli il collegamento correlato.
2. Seleziona la voce di registro correlata e apri la pagina **Voce di registro Shopify**.
3. Esamina la richiesta, il codice di stato e la descrizione e i valori di risposta. È possibile scaricare i valori di richiesta e risposta come file in un formato di testo.

Quindi ricordati di disattivare la registrazione per evitare un effetto negativo sulle prestazioni e aumentare le dimensioni del database.

Dalla pagina **Voci di registro Shopify**, è possibile attivare l'eliminazione di tutte le voci di registro o di quelle più vecchie di sette giorni.

## <a name="data-capture"></a>Acquisizione dati

Indipendentemente dal fatto che **Registro attivato** sia attivato, alcune risposte Shopify vengono sempre registrate. Puoi ispezionare o scaricare i registri dalla pagina **Lista acquisizione dati**.

Scegli l'azione **Dati Shopify recuperati** in una delle seguenti pagine:

- **Ordine Shopify**
- **Evasioni ordini Shopify**
- **Costi di spedizione ordine Shopify**
- **Transazioni ordine Shopify**
- **Pagamenti Shopify**
- **Transazioni di pagamento Shopify**
- **Transazioni Shopify**

## <a name="reset-sync"></a>Reimposta sincronizzazione

Per prestazioni ottimali, il connettore importa solo clienti, prodotti e ordini creati o modificati dopo l'ultima sincronizzazione. Nella pagina **Scheda punto vendita Shopify**, sono disponibili funzioni per modificare la data/ora dell'ultima sincronizzazione o ripristinarla completamente. Questa funzione garantisce che tutti i dati vengano sincronizzati e non solo le modifiche dall'ultima sincronizzazione.

Questa funzione si applica solo alle sincronizzazioni da Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)]. Può essere utile se è necessario ripristinare i dati eliminati come prodotti, clienti o ordini eliminati.

## <a name="request-the-access-token"></a>Richiedere il token di accesso

Se [!INCLUDE[prod_short](../includes/prod_short.md)] non si connette al tuo account Shopify, prova a richiedere il token di accesso da Shopify. Potrebbe essere necessario richiedere un nuovo token se sono state apportate modifiche alle chiavi di sicurezza o alle autorizzazioni richieste (ambiti di applicazione).

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri recuperare il token di accesso per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Richiedi accesso**.
4. Se richiesto, accedi al tuo account Shopify.

L'interruttore **Con chiave di accesso** verrà attivato.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment"></a>Verifica e abilita le autorizzazioni per effettuare richieste HTTP in un ambiente non di produzione

Per funzionare correttamente, l'estensione connettore Shopify richiede l'autorizzazione per effettuare richieste HTTP. Durante il test nel sandbox, le richieste HTTP sono vietate per tutte le estensioni.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Gestione estensioni**, quindi scegli il collegamento correlato.
2. Seleziona l'estensione **Connettore Shopify**.
3. Scegli l'azione **Configura** per aprire la pagina **Impostazione estensione**.
4. Assicurati che l'interruttore **Consenti richieste HTTPClient** sia abilitato.

## <a name="rotate-the-shopify-access-token"></a>Ruotare il token di accesso Shopify

Le procedure seguenti descrivono come ruotare il token di accesso utilizzato dal connettore Shopify per accedere al tuo punto vendita Shopify online.

### <a name="in-shopify"></a>In Shopify

1. Da **Amministratore Shopify**, vai ad [App](https://www.shopify.com/admin/apps).
2. Seleziona **Elimina** nella riga con l'app **Dynamics 365 Business Central**.
3. Nel messaggio che viene visualizzato, seleziona **Elimina**.

### <a name="in-"></a>In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri ruotare il token di accesso per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Richiedi accesso**.
4. Se richiesto, accedi al tuo account Shopify, rivedi privacy e autorizzazioni, quindi scegli il pulsante **Installa app**.

## <a name="known-issues"></a>Problemi noti

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store"></a>Errore: l'intestazione vendite non esiste. Campi e valori di identificazione: Tipo documento="Offerta", N.="PUNTO VENDITA SHOPIFY"

Per calcolare i prezzi il connettore Shopify crea un documento di vendita temporaneo (offerta) per un cliente temporaneo (codice negozio) e usa la logica di calcolo del prezzo standard. Se un'estensione di terze parti sottoscrive eventi su un documento di vendita temporaneo, l'intestazione potrebbe non essere disponibile. Ti consigliamo di contattare il fornitore dell'estensione. Chiedigli di modificare il codice per verificare la presenza di record temporanei. In alcuni casi basta aggiungere il metodo `IsTemporary` al posto giusto. Per ulteriori informazioni su `IsTemporary`, vai a [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Per verificare che il problema sia causato da un'estensione di terze parti, utilizza il collegamento **Copia informazioni negli appunti** nel messaggio di errore e copia il contenuto a un editor di testo. Le informazioni contengono uno **stack di chiamate AL**, dove la prima riga è la riga in cui si è verificato l'errore. Di seguito è riportato un esempio di stack di chiamate AL.

AL stack di chiamate:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Ricordarti di condividere le informazioni sullo stack di chiamate AL con il fornitore dell'estensione.

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty"></a>Errore: Categoria registrazione business deve avere un valore in Cliente: "PUNTO VENDITA SHOPIFY". Non può essere zero o vuoto

Nella pagina **Scheda punto vendita Shopify** compila il campo **Codice modello cliente**, scegli il modello che include il campo **Categoria registrazione business** popolato. Il modello cliente viene utilizzato per creare clienti e calcolare i prezzi di vendita sui documenti di vendita.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Errore: L'importazione dei dati nel negozio Shopify non è abilitata. Vai alla scheda del punto vendita per abilitarla

Nella pagina **Scheda punto vendita Shopify**, abilita l'interruttore **Consenti sincronizzazione dati in Shopify**. Questa impostazione ha lo scopo di proteggere il punto vendita online dall'ottenere dati dimostrativi da [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Errore Oauth invalid_request: impossibile trovare l'API per l'applicazione Shopify con api_key

Sembra che usi l'[app Embed](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), dove l'URL del client ha il formato: `https://[application name].bc.dynamics.com`. Il connettore Shopify non funziona per le app Embed. Per ulteriori informazioni, vai a [Per quali prodotti Microsoft è disponibile il connettore Shopify?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx"></a>Errore: errore interno. A quanto pare si è verificato un errore. ID richiesta: XXXXXXXXX-XXXX-XXXX-XXXX-XXXX

Contatta l'assistenza di Shopify entro 7 giorni dal verificarsi di questo errore e fornisci l'ID richiesta. Per saperne di più, vai a [Opzioni di supporto per Shopify](shopify-faq.md#shopify).

## <a name="see-also"></a>Vedere anche

[Iniziare a usare il connettore per Shopify](get-started.md)
