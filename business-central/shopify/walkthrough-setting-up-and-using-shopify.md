---
title: Configurare e usare il connettore Shopify
description: Vari scenari di integrazione per dimostrare il flusso di lavoro tra Shopify e Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Procedura dettagliata: configurare e usare il connettore Shopify

Questa sezione illustra alcuni scenari tipici e illustra i passaggi per testare o addestrare gli utenti sul flusso di lavoro di [!INCLUDE[prod_short](../includes/prod_short.md)] e del punto vendita Shopify integrato.

## <a name="prerequisites"></a>Prerequisiti

### <a name="shopify"></a>Shopify

Devi avere:

- Un account Shopify
- Un negozio online con Shopify

Scopri di più su come creare valutazioni di prova e impostazioni consigliate Shopify in [Creare e configurare un account Shopify](shopify-account.md).

### <a name="business-central"></a>Business Central

È necessario avere un account [!INCLUDE[prod_short](../includes/prod_short.md)]. 

Ad esempio, puoi creare un account demo o avviare una valutazione. Per ulteriori informazioni, vedi [Preparare ambienti dimostrativi di Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) e [Iscriversi per la versione di valutazione](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Collegamento di Business Central al punto vendita Shopify

In [!INCLUDE[prod_short](../includes/prod_short.md)] esegui le operazioni seguenti:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), e immetti **Punti vendita Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona l'azione **Nuovo**.
3. Nel campo **Codice**, immetti `DEMO1`.
4. Nel campo **URL Shopify**, immetti l'URL per il punto vendita online a cui desideri connetterti.
5. Attiva l'interruttore **Abilitato** quindi rivedi e accetta i termini e le condizioni.

Per configurare il punto vendita Shopify, esegui i passaggi seguenti:

1. Disattiva l'interruttore **Consenti sincronizzazioni in background**.
2. Seleziona *A Shopify* nel campo **Sincronizza articolo**.
3. Seleziona *A Shopify* nel campo **Sincronizza immagini articolo**.
4. Abilita l'interruttore **Sincronizza attributi articolo**.
5. Abilita l'interruttore **Inventario tracciato**.
6. Seleziona *Nega* nel campo **Criterio di inventario predefinito**.
7. Abilita l'interruttore **Crea automaticamente clienti sconosciuti**.
8. Compila il campo **Codice modello cliente/società** con il modello appropriato.
9. Compila il campo **Conto costo spedizione**, **Conto mance** con il conto ricavi. Ad esempio, negli Stati Uniti, utilizza `40210`.
10. Abilita l'interruttore **Creazione automatica degli ordini**.
11. Disattiva l'interruttore **Rilascia automaticamente ordini vendita**.

Configurare il mapping della posizione:

1. Seleziona l'azione **Posizioni** per aprire **Posizioni punto vendita Shopify**.
2. Seleziona l'azione **Ottieni ubicazioni Shopify** per importare tutte le posizioni definite in Shopify. Seleziona la voce con l'interuttore **Primario** selezionato.
3. In **Filtro ubicazione**, immetti `''|EAST|MAIN`.
4. Seleziona *Disponibilità calcolata a oggi* nel campo **Calcolo scorte** per abilitare una sincronizzazione dell'inventario per un'ubicazione Shopify.

## <a name="walkthrough-start-selling-products-online"></a>Procedura dettagliata: iniziare a vendere prodotti online

### <a name="scenario"></a>Scenario

Supponiamo che tu voglia provare Shopify come punto vendita online senza dedicare molto tempo alla configurazione, soprattutto perché mantieni già i tuoi articoli in [!INCLUDE[prod_short](../includes/prod_short.md)] correttamente. Dopo aver lanciato il tuo punto vendita online Shopify, ottieni immediatamente nuovi clienti che sono soddisfatti del tuo punto vendita e della loro esperienza di acquisto. Quindi, decidono di lasciare mance alla cassa.

### <a name="steps"></a>Passaggi

In [!INCLUDE[prod_short](../includes/prod_short.md)], attieniti alla seguente procedura:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Prodotti Shopify** e scegli il collegamento correlato.
2. Seleziona **Aggiungi articoli**.
3. Nel campo **Codice punto vendita** immetti `DEMO1`.
4. Imposta il filtro `CHAIR` nel campo **Codice categoria articolo**.
5. Attiva l'interruttore **Sincronizza immagini prodotto**.
6. Attiva l'interruttore **Sincronizza inventario**.
7. Seleziona **OK** e attendi il completamento della sincronizzazione iniziale di articoli, prezzi, immagini e scorte.

Nel **punto vendita online Shopify**:
> [!Tip]  
> Apri **Amministrazione Shopify**, accedendo all'URL specificato nel campo **URL** della pagina **Scheda punto vendita Shopify**. Seleziona l'icona a forma di occhio accanto al canale di vendita **Punto vendita online**, situato nella barra laterale di **Amministrazione Shopify**. 

Apri il catalogo dei prodotti. Avviso:

* Titoli, immagini e prezzi dei prodotti.
* Indicatore di disponibilità (esaurito in caso di esaurimento scorte).

Scegli qualsiasi prodotto che può essere venduto, ad esempio, `BERLIN Swivel Chair, yellow`. Nota che la descrizione contiene gli attributi dell'articolo.

Seleziona **Compralo subito** e procedi alla fase di pagamento.

1. Nel campo **E-mail o numero di cellulare** inserisci `cl@contoso.com` (o l'e-mail su cui desideri ricevere le conferme dell'ordine e della spedizione).
2. Nei campi **Nome** e **Cognome**, inserisci `Claudia Lawson`.
3. Inserisci l'indirizzo locale.
4. Seleziona la casella di controllo **Salva queste informazioni per la prossima volta**.
6. Mantieni *Standard* come metodo di spedizione.
8. Nel campo **Numero carta di credito**, immetti `1` se utilizzi *(per il test) Bogus Gateway* o `5555 5555 5555 4444` se utilizzi *Shopify payments* in modalità test.
9. Compila il campo **Nome sulla scheda**.
10. Nel campo **Data di scadenza** , inserisci il mese e l'anno corrente.
11. In **Codice di sicurezza**, immetti `111`.
7. Facoltativo: seleziona il suggerimento `10%`.
8. 12. Seleziona **Paga adesso**.

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Ordini Shopify**, quindi scegli il collegamento correlato.
2. Seleziona l'azione **Sincronizza ordini da Shopify**.
3. Seleziona **OK**.

L'ordine importato è pronto per l'elaborazione.

1. Seleziona l'ordine importato per aprire la finestra **Ordine Shopify**.
2. Nota che vengono creati il nuovo cliente e nuovi ordini cliente.
3. Esplora le azioni **Rischio** e **Costo di spedizione**.
4. Seleziona **Ordine vendita** per aprire la finestra **Ordine vendita** L'ordine cliente è una domanda che, se necessario, può essere soddisfatta con l'assemblaggio, la produzione o l'acquisto con l'ausilio del motore di pianificazione. Supporta inoltre vari processi di gestione del magazzino con completa separazione dei compiti.
6. Nel campo **Agente**, immetti `DHL`. Riapri l'ordine, se necessario, scegliendo l'azione **Riapri**.
7. In **Nr. identificazione collo**, immetti `123456789`.
8. Seleziona **Registra**, l'opzione **Spedisci e fattura**, quindi il pulsante **OK**.

Ora i dati fisici e finanziari sono registrati in [!INCLUDE[prod_short](../includes/prod_short.md)]. È ora di inviare una notifica a Shopify relativa alle modifiche.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), icona, immetti **Sincronizza spedizioni con Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona **OK**.

In **Amministrazione Shopify** nota che l'ordine è ora contrassegnato come *Completato*. Puoi anche rivedere i dettagli della spedizione e vedere l'URL di tracciamento lì. Se esegui **Sincronizza ordini da Shopify** di nuovo, l'ordine verrà archiviato in entrambi i sistemi.

## <a name="walkthrough-add-your-customers-to-your-new-online-store"></a>Procedura dettagliata: aggiungere i clienti al nuovo punto vendita online

### <a name="scenario-1"></a>Scenario

Dopo un avvio rapido di successo del tuo nuovo punto vendita online, desideri che i tuoi attuali clienti lo visitino e inizino a effettuare ordini. A seconda del piano e del processo Shopify, puoi provare i flussi B2B e D2C.

### <a name="d2c-steps"></a>Passaggi per D2C

In [!INCLUDE[prod_short](../includes/prod_short.md)] esegui le operazioni seguenti:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Clienti Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona **Aggiungi clienti**.
3. Nel campo **Codice punto vendita** immetti `DEMO1`.
4. Imposta il filtro `20000` nel campo **Nr.** .
5. Seleziona **OK** e attendi il completamento della sincronizzazione iniziale dei clienti.

In **Amministrazione Shopify** nota che il cliente è stato importato. Apri i clienti e nota che il nome e il cognome del cliente provengono dal campo **Nome contatto** di **Scheda cliente**. Il nome della società si trova nell'indirizzo predefinito, collegato al cliente. Se utilizzi *Conti cliente classici*, puoi selezionare **Invia invito al conto** per invitare il cliente. Con *Nuovi conti cliente* non è richiesta una password per l'accesso dei clienti, ma Shopify consente ai tuoi clienti di accedere utilizzando un codice di verifica a 6 cifre inviato via e-mail. 

### <a name="b2b-steps"></a>Passaggi per B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

In [!INCLUDE[prod_short](../includes/prod_short.md)] procedi come segue:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Società Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona **Aggiungi società**.
3. Nel campo **Codice punto vendita** immetti `DEMO1`.
4. Imposta il filtro `30000` nel campo **Nr.** .
5. Seleziona **OK** e attendi il completamento della sincronizzazione iniziale dei clienti.

In  **Shopify - Amministra**, nota che la società e il cliente sono stati importati. Apri i clienti e nota il riquadro dettagli informazioni Società con il collegamento a società, ubicazione e autorizzazioni assegnate. Seleziona **[...]** nel riquadro dettagli informazioni **Società** quindi seleziona **Invia e-mail di accesso B2B** per invitare il cliente.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Procedura dettagliata: messa a punto della gestione degli elementi

### <a name="scenario-2"></a>Scenario

Ti piacerà aggiungere maggiore flessibilità e controllo ai tuoi processi relativi alla gestione degli articoli. Desideri migliorare le descrizioni dei prodotti e aggiungere ulteriori passaggi di revisione prima che i prodotti diventino disponibili per tutti i clienti.

### <a name="steps-1"></a>Passaggi

In [!INCLUDE[prod_short](../includes/prod_short.md)] procedi come segue:

Preparare i dati.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), , immetti **Gruppo di prezzi per clienti** e seleziona il relativo collegamento.
2. Aggiungi nuovo gruppo di prezzo. Nel campo **Codice**, immetti `SHOPIFY`.
3. Chiudi la finestra **Gruppo prezzi cliente**.
4. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Articoli** e seleziona il collegamento correlato.
5. Seleziona la voce *1896-S, Athens Desk* quindi segui questi passaggi:

6. Seleziona l'azione **Varianti**, quindi aggiungi due varianti: `PREMIUM, Athens Desk, Premium edition` e `ESSENTIAL, Athens Desk, Essential edition`.
7. Seleziona l'azione **Testo di marketing** e utilizza  **Bozza con Copilot** per ottenere un testo creativo e accattivante. Se il suggerimento del testo di marketing non è abilitato, inserisci semplicemente: "**Il design semplice ed elegante** si fonde con qualsiasi completo. *Disponibile in due edizioni.*". 
8. Seleziona l'azione **Prezzi vendita** e aggiungi nuovi prezzi come mostrato nella seguente tabella:

   |A linee|Tipo vendita|Codice vendita|Tipo|Codice|Codice variante<br>(aggiungi il campo tramite personalizzazione)|Prezzo unitario|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Gruppo di prezzi cliente|SHOPIFY|Articolo|1896-S|ESSENTIAL|700|
   |2|Gruppo di prezzi cliente|SHOPIFY|Articolo|1896-S|PREMIUM|1000|

9. Seleziona l'azione **Sconti sulle vendite** e aggiungi un nuovo sconto:

   * **Tipo vendita** *Gruppo sconti cliente*
   * **Codice vendita** *DETTAGLIO*
   * **Tipo** *Articolo*
   * **Codice** *1896-S*
   * **Cod. Unità di Misura** *PCS*
   * **Sconto riga %** *10*

10. Seleziona l'azione **Riferimenti articolo** e aggiungi le seguenti righe:

   |A linee|Tipo riferimento|Nr. riferimento|Codice variante|
   |------|------------|------------|------------|
   |1|Codice a barre|77777777|ESSENTIAL|
   |2|Codice a barre|11111111|PREMIUM|

11. Seleziona la voce *1920-S, ANTWERP Conference Table* ed esegui i seguenti passaggi.
12. Seleziona **Regolazione dell'inventario** e nel campo **Nuovo inventario**, inserisci `100` per le posizioni *EST* e *OVEST*. 
13. Seleziona **OK**.

Regolare le impostazioni di sincronizzazione.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), e immetti **Punti vendita Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona il punto vendita `DEMO1` per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Abilita il campo **Sincronizza testo marketing**.
4. Seleziona **Numero articolo + codice variante** nel campo *Mapping SKU*.
5. Seleziona *Continua* nel campo **Criterio di inventario predefinito**.
6. Seleziona **Bozza** nel campo *Stato dei prodotti creati*.
7. Seleziona **Stato su archiviato** nel campo *Azione per prodotto rimosso*.
8. Seleziona *SHOPIFY* nel campo **Gruppo prezzi cliente**.
9. Seleziona *DETTAGLIO* nel campo **Gruppo sconto cliente**.
 
Esegui la sincronizzazione.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), e immetti **Punti vendita Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona il punto vendita `DEMO1` per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Seleziona l'azione **Prodotti** per aprire la finestra **Prodotti Shopify**.
4. Seleziona l'azione **Aggiungi articoli**.
5. Imposta il filtro **TABLE|DESK** sul campo *Codice categoria articolo*.
6. Attiva l'interruttore **Sincronizza immagini prodotto**.
7. Attiva l'interruttore **Sincronizza inventario**.
8. Seleziona **OK** e attendi il completamento della sincronizzazione iniziale di articoli, prezzi, immagini e scorte.

I prodotti vengono aggiunti. Tieni presente che lo stato è impostato su *Bozza*, pertanto gli articoli non sono visibili nel punto vendita online Shopify.

1. Seleziona la riga con l'articolo *Tavolo conferenza 1920-S, ANTWERP*. In **Titolo SEO**, immetti `Rectangular meeting table Antwerp, 10 seats, black`.
2. Seleziona *Attivo* nel campo **Stato**.
3. Seleziona la riga con l'articolo *1906-S, ATENE, Piedistallo* quindi seleziona l'azione **Elimina**.

In **Amministrazione Shopify** nota che tutti i prodotti hanno stati diversi.

* *Tavolo conferenza ANTWERP* è *Attivo* perché abbiamo cambiato lo stato nella finestra **Prodotto Shopify**.
* *Scrivania ATENE* è *Bozza* perché abbiamo configurato lo stato predefinito per tutti i prodotti aggiunti come *Bozza*.
* *Piedistallo ATENE* è *Archiviato* perché abbiamo configurato il punto vendita per assegnare automaticamente lo stato su *Archiviato* per i prodotti eliminati.

Nota che l'inventario per il tavolo da conferenza di ANTWERP è 100, perché abbiamo configurato il sistema per usare l'inventario solo da due posizioni PRINCIPALE ed EST. L'inventario in un'altra località (OVEST) viene ignorato.

* Apri *Tavolo conferenza ANTWERP*, annota i campi **Tipo personalizzato**, **Fornitore**, **Peso**, **Costo per articolo** e la sezione **Anteprima elenco motore di ricerca**.
* Apri *Scrivania Atene*, scorri verso il basso fino alla sezione **Varianti** e nota come è popolato **SKU**.
* Seleziona **Modifica** per rivedere il codice a barre e i prezzi.
* Modifica lo stato di *Scrivania Atene* su *Attivo* e seleziona l'azione **Anteprima**.

Nel **punto vendita Shopify online** apri il catalogo prodotti, trova il prodotto *Scrivania ATENE*. Nota che sono disponibili diverse opzioni. Per diverse opzioni, i prezzi sono diversi. Presta attenzione alle informazioni sugli sconti.

### <a name="additional-steps-for-b2b"></a>Ulteriori passaggi per B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Puoi configurare il connettore per creare e assegnare automaticamente il catalogo per le società esportate. I passaggi seguenti sono utili se desideri un controllo più preciso di ciò che è disponibile per i clienti B2B.

In **Shopify - Amministra** crea un catalogo e assegnalo.

1. Seleziona **Prodotti** e quindi **Cataloghi** nella barra laterale di **Shopify - Amministra**.
2. Crea un catalogo per prodotti specifici. Chiamalo "B2B". 
3. Scegli **Gestisci** e quindi **Gestisci prodotti e prezzi**.
4. Seleziona il filtro *Escluso*, trova *ATHERN Desk* e scegli **Includi in catalogo**.
5. Seleziona **Clienti** e quindi **Società** nella barra laterale di **Shopify - Amministra**.
6. Seleziona *School of Fine Art*, scegli **[...]** e quindi **Aggiungi cataloghi** e aggiungi il catalogo *B2B* creato in precedenza.

In [!INCLUDE[prod_short](../includes/prod_short.md)] procedi come segue:

Preparare i dati.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Articoli** e seleziona il collegamento correlato.

2. Seleziona la voce **1896-S, Athens Desk** quindi segui questi passaggi:

3. Seleziona l'azione **Sconti sulle vendite** e aggiungi un nuovo sconto:

   * **Tipo vendita** *Gruppo sconti cliente*
   * **Codice vendita** *INGROSSO*
   * **Tipo** *Articolo*
   * **Codice** *1896-S*
   * **Cod. Unità di Misura** *PCS*
   * **Sconto riga %** *25*

4. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Cataloghi Shopify** e seleziona il collegamento correlato.
5. Seleziona **Ottieni cataloghi**.
6. Nel campo **Codice punto vendita** immetti `DEMO1`.
7. Seleziona la voce del catalogo *B2B* per la quale desideri sincronizzare i prezzi.
8. Abilita l'interruttore **Sincronizza prezzi**.
9. Seleziona *SHOPIFY* nel campo **Gruppo di prezzi cliente**.
10. Seleziona *INGROSSO* nel campo **Gruppo sconto cliente**.
11. Scegli **Sincronizza prezzi** e attendi il completamento della sincronizzazione dei prezzi.

In **Shopify - Amministra**, esplora i prezzi per il catalogo *B2B*.

Nel **punto vendita Shopify online** apri il catalogo prodotti, trova il prodotto *Scrivania ATENE*. I prezzi sono informazioni sugli sconti.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Procedura dettagliata: sincronizzare il completamento della transazione e l'ordine per l'acquirente individuale e il rappresentante della società
Questa è una continuazione di [Procedura dettagliata: iniziare a vendere prodotti online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Puoi anche provare con i tuoi dati, ad esempio la tua sandbox o il tuo punto vendita Shopify.

Acquirente individuale

1. In **Punto vendita online Shopify**: Scegli l'icona **Conto**. Immetti l'indirizzo e-mail a cui hai accesso.
2. Accedi utilizzando un codice di verifica monouso a 6 cifre inviato tramite l'indirizzo e-mail che hai inserito.
3. Esplora il catalogo prodotti. Dovresti essere in grado di vedere tutti i prodotti con i prezzi al dettaglio.
4. Seleziona la variante Essential e quindi **Acquista ora** e completa la transazione.
5. Compila i campi **Nome** e **Cognome**.
6. Inserisci l'indirizzo locale.
7. Mantieni *Standard* come metodo di spedizione.
8. Nel campo **Numero carta di credito**, immetti `1` se utilizzi *(per il test) Bogus Gateway* o `5555 5555 5555 4444` se utilizzi *Shopify payments* in modalità test.
9. Nel campo **Data di scadenza**, immetti il mese e l'anno corrente.
10. In **Codice di sicurezza**, immetti `111`.
11. Compila il campo **Nome sulla scheda**.
12. Seleziona **Paga adesso**.
 
Rappresentante della società

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. In **Shopify - Amministra**.
2. Seleziona **Clienti** e quindi **Società** nella barra laterale di **Shopify - Amministra**.
3. Apri la voce *School of Fine Art*.
4. Scegli **[...]** nella casella **School of Fine Art**, quindi scegli **Modifica condizioni di pagamento** e seleziona *All'evasione*.
5. Scegli **[...]** nella casella **Clienti**, quindi scegli **Aggiungi cliente** e aggiungi un cliente con l'indirizzo e-mail che hai utilizzato per accedere al punto vendita in precedenza.
6. In **Punto vendita online Shopify**: Scegli l'icona **Conto**. Immetti l'indirizzo e-mail a cui hai accesso.
7. Accedi utilizzando un codice di verifica monouso a 6 cifre inviato tramite l'indirizzo e-mail che hai inserito.
8. Esplora il catalogo dei prodotti. Dovrebbe essere visualizzato solo il prodotto aggiunto al catalogo *B2B* con prezzi al dettaglio speciali.
9. Seleziona la variante Essential e quindi **Acquista ora** e completa la transazione.
10. Nota che i campi Conto, Spedire a e Metodo di pagamento sono compilati.
11. Immetti `PO-12345` nel campo **Numero ordine d'acquisto**.
12. Seleziona **Invia ordine**.
 
In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Ordini Shopify**, quindi scegli il collegamento correlato.
2. Seleziona l'azione **Sincronizza ordini da Shopify**.
3. Seleziona **OK**.

L'ordine importato è pronto per l'elaborazione.

1. Seleziona l'ordine importato per aprire la finestra **Ordine Shopify**.
2. Tieni presente che sebbene entrambi gli ordini siano stati inviati dalla stessa persona, sono collegati a due clienti diversi. 
3. Nell'ordine inviato per conto della società puoi vedere il valore nel campo **Numero ordine di acquisto**, che viene anche trasferito al campo **Nr. documento esterno** del documento di vendita creato.
4. Perché abbiamo configurato la società B2B per gestire i pagamenti al di fuori di Shopify, il campo **Stato finanziario** è impostato su *In sospeso*. Una volta ricevuto il pagamento, seleziona l'azione **Contrassegna come pagato**. Lo stato finanziario verrà aggiornato in Shopify. 

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Procedura dettagliata: importare articoli, clienti, società da Shopify

### <a name="scenario-3"></a>Scenario

Hai già un punto vendita online di successo e vorresti iniziare a usare [!INCLUDE[prod_short](../includes/prod_short.md)] come software gestionale aziendale. Desideri importare quanti più dati possibile da Shopify. 

### <a name="steps-2"></a>Passaggi

Questa è la continuazione di [Procedura dettagliata: iniziare a vendere prodotti online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) e [ Procedura dettagliata: aggiungere i clienti al nuovo punto vendita online](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Puoi anche provare con i tuoi dati, ad esempio la tua sandbox o il tuo punto vendita Shopify.

In [!INCLUDE[prod_short](../includes/prod_short.md)], segui i passaggi elencati di seguito.

#### <a name="prepare-data"></a>Preparare i dati

1. Passa a una prova gratuita di 30 giorni senza dati di esempio. Per ulteriori informazioni, vedi [Aggiungere i propri dati a una prova vuota](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), e immetti **Punti vendita Shopify**, quindi seleziona il collegamento correlato.
3. Seleziona **Nuovo**.
4. Nel campo **Codice**, immetti `DEMO2`.
5. Nel campo **URL Shopify**, immetti l'URL al punto vendita online a cui desideri connetterti.
6. Attiva l'interruttore **Abilitato** quindi rivedi e accetta i termini e le condizioni.

Configura il punto vendita Shopify come descritto qui:

1. Disabilita l'opzione **Consenti sincronizzazioni in background**.
2. Seleziona *Da Shopify* nel campo **Sincronizza articolo**.
3. Abilita l'interruttore **Crea automaticamente articoli sconosciuti**.
4. Compila il campo **Codice modello articolo** con il modello appropriato.
5. Seleziona *Da Shopify* nel campo **Sincronizza immagini articolo**.
6. Seleziona **Numero articolo e codice variante** nel campo *Mapping unità di stockkeeping*.
7. Seleziona *Tutti i clienti* in **Importazione clienti da Shopify**.
8. Abilita l'interruttore **Crea automaticamente clienti sconosciuti**.
9. Compila il campo **Codice modello cliente/società** con il modello appropriato.
10. Seleziona *Tutti i clienti* in **Importazione società da Shopify**.
11. Abilita l'interruttore **Crea automaticamente società sconosciute**.

#### <a name="run-the-synchronization"></a>Esegui la sincronizzazione

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), e immetti **Punti vendita Shopify**, quindi seleziona il collegamento correlato.
2. Seleziona il punto vendita *DEMO2* per il quale desideri sincronizzare i dati per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Seleziona **Sincronizza prodotti**.
4. Seleziona **Sincronizza immagini prodotto**.
5. Seleziona **Sincronizza clienti**.
6. Seleziona **Sincronizza società**.

### <a name="results"></a>Risultati

* I prodotti Shopify vengono importati. Per verificare, seleziona l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prodotti Shopify** e scegli il collegamento correlato.
* Vengono creati elementi con immagini. Per verificare, seleziona l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articolo** e seleziona il collegamento correlato.
* I clienti Shopify vengono importati. Per verificare, seleziona l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti Shopify**, quindi seleziona il collegamento correlato.
* Le società Shopify vengono importate. Per verificare, seleziona l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Società Shopify**, quindi seleziona il collegamento correlato.
* I clienti vengono creati. Per verificare, seleziona l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi seleziona il collegamento correlato.


## <a name="see-also"></a>Vedere anche

[Iniziare a usare il connettore Shopify](get-started.md)  
