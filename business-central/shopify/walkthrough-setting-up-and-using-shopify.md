---
title: Configurare e usare il connettore Shopify
description: Vari scenari di integrazione per dimostrare il flusso di lavoro tra Shopify e Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector" />Procedura dettagliata: configurare e usare il connettore Shopify

Questa sezione illustra alcuni scenari tipici e illustra i passaggi per testare o addestrare gli utenti sul flusso di lavoro di [!INCLUDE[prod_short](../includes/prod_short.md)] e del punto vendita Shopify integrato.

## <a name="prerequisites" />Prerequisiti

### <a name="shopify" />Shopify

Devi avere:

- Un account Shopify
- Un negozio online con Shopify

Scopri di più su come creare valutazioni di prova e impostazioni consigliate Shopify in [Creare e configurare l'account Shopify](shopify-account.md).

### <a name="business-central" />Business Central

È necessario avere un account [!INCLUDE[prod_short](../includes/prod_short.md)]. 

Ad esempio, puoi creare un account CRONUS o avviare la valutazione. Per ulteriori informazioni, vedi [Preparare ambienti dimostrativi di Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) e [Iscriversi per la versione di valutazione](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop" />Collegamento di Business Central al punto vendita Shopify

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.
3. Nel campo **Codice**, immetti `DEMO1`.
4. Nel campo **URL Shopify**, immetti l'URL al punto vendita online a cui desideri connetterti.
5. Attiva l'interruttore **Abilitato**, rivedi e accetta i termini e le condizioni.

Configura il punto vendita Shopify come descritto nei seguenti passaggi:

1. Abilita l'interruttore **Log abilitato**.
2. Disattiva l'opzione **Consenti sincronizzazioni in background**.
3. Seleziona **A Shopify** nel campo **Sincronizza articolo**.
4. Seleziona **A Shopify** nel campo **Sincronizza immagini articolo**.
5. Abilita l'interruttore **Sincronizza attributi articolo**.
6. Abilita l'interruttore **Inventario tracciato**.
7. Seleziona **Nega** nel campo **Criterio di inventario predefinito**.
8. Abilita l'interruttore **Crea automaticamente clienti sconosciuti**.
9. Compila il campo **Codice modello cliente** con il modello appropriato.
10. Compila il campo **Conto costo spedizione**, **Conto mance** con il conto ricavi. Ad esempio, negli Stati Uniti, utilizza `40100`.
11. Abilita l'interruttore **Creazione automatica degli ordini**.

Configurare il mapping della posizione:

1. Scegli l'azione **Posizioni** per aprire **Posizioni punto vendita Shopify**.
2. Scegli l'azione **Ottieni ubicazioni Shopify** per importare tutte le posizioni definite in Shopify.
3. In **Filtro ubicazione**, immetti `''|EAST|MAIN`.
4. Disattiva l'interruttore **Disabilitato** per abilitare la sincronizzazione dell'inventario per la posizione Shopify selezionata.

## <a name="walkthrough-start-selling-products-online" />Procedura dettagliata: iniziare a vendere prodotti online

### <a name="scenario" />Scenario

Supponiamo che tu voglia provare Shopify come punto vendita online senza dedicare molto tempo alla configurazione, soprattutto perché mantieni già i tuoi articoli in [!INCLUDE[prod_short](../includes/prod_short.md)] correttamente. Dopo aver lanciato il tuo punto vendita online Shopify, ottieni immediatamente nuovi clienti che sono soddisfatti del tuo punto vendita e della loro esperienza di acquisto. Quindi, decidono di lasciare mance alla cassa.

### <a name="steps" />Passaggi

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

1. Scegli la ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Aggiungi articoli**.
3. Nel campo **Codice punto vendita** immettere *DEMO1*.
4. Imposta il filtro `CHAIR` sul campo **Codice categoria articolo** (aggiungi campo filtro se necessario).
5. Seleziona **OK** e attendi il completamento della sincronizzazione iniziale di articoli e prezzi.
6. Scegli l'azione **Sincronizza immagini prodotto**.
7. Scegli l'azione **Sincronizza inventario**.

Un **punto vendita online Shopify**
> [!Tip]  
> Apri **Amministrazione Shopify**, accedendo all'URL specificato nel campo **URL** della pagina **Scheda punto vendita Shopify**. Quindi scegli l'icona a forma di occhio accanto al canale di vendita **Negozio online**, situato nella barra laterale di **Amministrazione Shopify**. 

Apri il catalogo dei prodotti. Avviso:

* Titoli, immagini e prezzi dei prodotti.
* Indicatore di disponibilità (esaurito in caso di esaurimento scorte).

Scegli qualsiasi prodotto che può essere venduto, ad esempio, `BERLIN Swivel Chair, yellow`. Nota che la descrizione contiene gli attributi dell'articolo.

Scegli il pulsante **Compralo subito** e procedi alla fase di pagamento.

1. Nel campo **E-mail o numero di cellulare** inserisci `cl@contoso.com` (o l'e-mail su cui desideri ricevere le conferme dell'ordine e della spedizione).
2. In  **Nome** e **Cognome**, inserisci `Claudia Lawson`.
3. Inserisci l'indirizzo locale.
4. Seleziona la casella di controllo **Salva queste informazioni per la prossima volta** .
5. Fai clic sul pulsante **Continua con la spedizione**.
6. Mantieni `Standard` come metodo di spedizione e quindi scegli il pulsante **Continua al pagamento**.
7. Seleziona il suggerimento `10%`.
8. Nel campo **Carta di credito**, inserisci `1` se utilizzi *(per il test) Bogus Gateway*, se utilizzi *Shopify payments* in modalità test, inserisci `5555 5555 5555 4444`.
9. Compila il campo **Nome sulla scheda**.
10. Nel campo **Data di scadenza** , inserisci il mese e l'anno corrente.
11. In **Codice di sicurezza**, immetti `111`.
12. Fai clic sul pulsante **Paga ora**.

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

1. Scegli la ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini Shopify**, quindi seleziona il collegamento correlato.
2. Scegli l'azione **Sincronizza ordini da Shopify**.
3. Selezionare **OK**.

L'ordine importato è pronto per l'elaborazione.

1. Seleziona l'ordine importato per aprire la finestra **Ordine Shopify**.
2. Nota che vengono creati il nuovo cliente e il nuovo ordine cliente.
3. Esplora le azioni **Rischio** e **Costo di spedizione**.
4. Scegli l'azione **Ordine di vendita** per aprire la finestra **Ordine vendita**. L'ordine cliente è una domanda che, se necessario, può essere soddisfatta con l'assemblaggio, la produzione o l'acquisto con l'ausilio del motore di pianificazione. Supporta inoltre vari processi di gestione del magazzino con completa separazione dei compiti.
5. Scegliere l'azione **Riapri**.
6. Nel campo **Agente**, immetti `DHL`.
7. In **Nr. identificazione collo**, immetti `123456789`.
8. Scegli l'azione **Registra**, seleziona l'opzione **Spedisci e fattura**, quindi il pulsante **OK**.

Ora i dati fisici e finanziari sono registrati in [!INCLUDE[prod_short](../includes/prod_short.md)]. È ora di inviare una notifica a Shopify relativa alle modifiche.

1. Scegli la ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") icona, immetti **Sincronizza spedizioni con Shopify**, quindi scegli il collegamento correlato.
2. Selezionare **OK**.

In **Amministrazione Shopify** nota che l'ordine è ora contrassegnato come *Completato*. Puoi anche rivedere i dettagli della spedizione e vedere l'URL di tracciamento lì. Se esegui **Sincronizza ordini da Shopify** di nuovo, l'ordine verrà archiviato in entrambi i sistemi.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store" />Procedura dettagliata: invita i tuoi clienti nel tuo nuovo punto vendita online

### <a name="scenario" />Scenario

Dopo un avvio rapido di successo del tuo nuovo punto vendita online, desideri che i tuoi attuali clienti lo visitino e inizino a effettuare ordini.

### <a name="steps" />Passaggi

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita **DEMO1** per il quale desideri sincronizzare i clienti per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegliere l'azione **Sincronizza clienti**.

In **Amministrazione Shopify** nota che i clienti sono stati importati. Apri uno dei clienti e nota che il nome e il cognome del cliente provengono dal campo **Nome contatto** di **Scheda cliente**. Il nome dell'azienda si trova nell'indirizzo predefinito, collegato al cliente. Scegli **Invia invito account** per invitare il cliente.

## <a name="walkthrough-fine-tuning-of-item-management" />Procedura dettagliata: messa a punto della gestione degli elementi

### <a name="scenario" />Scenario

Ti piacerà aggiungere maggiore flessibilità e controllo ai tuoi processi relativi alla gestione degli articoli. Desideri migliorare la descrizione del prodotto e desideri aggiungere ulteriori passaggi di revisione prima che i prodotti diventino disponibili per il cliente finale.

### <a name="steps" />Passaggi

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

Preparare i dati.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Gruppo di prezzi per clienti** e scegli il relativo collegamento.
2. Aggiungi nuovo gruppo di prezzo. Nel campo **Codice**, immetti `SHOPIFY`.
3. Chiudi la finestra **Gruppo prezzi cliente**.
4. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli** e scegli il collegamento correlato.

Seleziona la voce **1896-S, Athens Desk** ed esegui i seguenti passaggi.

1. Scegli l'azione **Varianti**, quindi aggiungi due varianti `PREMIUM, Athens Desk, Premium edition` e `ESSENTIAL, Athens Desk, Essential edition`.
2. Scegli l'azione **Testo esteso**, crea un nuovo testo esteso valido per tutti i codici lingua. Nel campo **Descrizione**, immetti `Shopify`. 
3. Aggiungi il seguente testo con i tag HTML: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Scegli l'azione **Prezzi vendita** e aggiungi nuovi prezzi come mostrato nella seguente tabella:

  |A linee|**Tipo vendita**|**Codice vendita**|Tipo|Codice|Codice variante<br>(aggiungi il campo tramite personalizzazione)|Prezzo unitario|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Gruppo di prezzi cliente|SHOPIFY|Articolo|1896-S|ESSENTIAL|700|
  |2|Gruppo di prezzi cliente|SHOPIFY|Articolo|1896-S|PREMIUM|1000|

5. Scegli l'azione **Sconti sulle vendite** e aggiungi un nuovo sconto:

* **Tipo vendita** *Gruppo sconti cliente*
* **Codice vendita** *DETTAGLIO*
* **Tipo** *Articolo*
* **Codice** *1896-S*
* **Cod. Unità di Misura** *PCS*
* **Sconto riga %** *10*

6. Scegli l'azione **Riferimenti articolo** e aggiungi le seguenti righe:

  |A linee|**Tipo riferimento**|**Nr. riferimento**|Codice variante|
  |------|------------|------------|------------|
  |1|Codice a barre|77777777|ESSENTIAL|
  |2|Codice a barre|11111111|PREMIUM|


Seleziona la voce **1920-S, ANTWERP Conference Table** ed esegui i seguenti passaggi.

1. Scegli **Regolazione dell'inventario** e nel campo **Nuovo inventario**, inserisci `100` per le posizioni *EST* e *OVEST*. 
2. Selezionare **OK**.

Regolare le impostazioni di sincronizzazione.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita *DEMO1* per il quale desideri sincronizzare gli articoli per l'apertura della pagina Scheda del punto vendita Shopify.
3. Seleziona *SHOPIFY* nel campo **Gruppo prezzi cliente**.
4. Seleziona *DETTAGLIO* nel campo **Gruppo sconto cliente**.
5. Abilita il campo **Sincronizza testo esteso elemento**.
6. Seleziona **Numero articolo + codice variante** nel campo *Mapping SKU*.
7. Seleziona **Bozza** nel campo *Stato dei prodotti creati*.
8. Seleziona **Stato su archiviato** nel campo *Azione per prodotto rimosso*.

Esegui la sincronizzazione.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita *DEMO1* per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Prodotti** per aprire la finestra **Prodotti Shopify**.
4. Scegli l'azione **Aggiungi articoli**.
5. Imposta il filtro **TABELLA** sul campo *Codice categoria articolo*.
6. Scegli l'azione **Sincronizza immagini prodotto**.
7. Scegli l'azione **Sincronizza inventario**.

I prodotti vengono aggiunti. Tieni presente che lo stato è impostato su *Bozza*, pertanto gli articoli non sono visibili nel punto vendita online Shopify.

1. Seleziona la riga con l'articolo *Tavolo conferenza 1920-S, ANTWERP*. In **Titolo SEO**, immetti `Rectangular meeting table Antwerp, 10 seats, black`.
2. Seleziona *Attivo* nel campo **Stato**.
3. Seleziona la riga con l'articolo *1906-S, ATENE, Piedistallo* quindi scegli l'azione **Elimina**.

In **Amministrazione Shopify** nota che tutti i prodotti hanno stati diversi.

* *Tavolo conferenza ANTWERP* è *Attivo* perché abbiamo cambiato lo stato nella finestra **Prodotto Shopify**.
* *Scrivania ATENE* è *Bozza* perché abbiamo configurato lo stato predefinito per tutti i prodotti aggiunti come *Bozza*.
* *Piedistallo ATENE* è *Archiviato* perché abbiamo configurato il punto vendita per assegnare automaticamente lo stato su *Archiviato* per i prodotti eliminati.

Nota che l'inventario per il tavolo da conferenza di ANTWERP è 100, perché abbiamo configurato il sistema per usare l'inventario solo da due posizioni PRINCIPALE ed EST. L'inventario in altre località (OVEST) viene ignorato.

* Apri *Tavolo conferenza ANTWERP*, annota i campi **Tipo personalizzato**, **Fornitore**, **Peso**, **Costo per articolo** e la sezione **Anteprima elenco motore di ricerca**.
* Apri *Scrivania Atene*, scorri verso il basso fino alla sezione **Varianti** e nota come è popolato **SKU**.
* Scegli **Modifica** per rivedere il codice a barre e i prezzi.
* Modifica lo stato di *Scrivania Atene* su *Attivo* e scegli l'azione **Anteprima**.

Nel **punto vendita Shopify online** apri il catalogo prodotti, trova il prodotto *Scrivania ATENE*. Nota che sono disponibili diverse opzioni. Per diverse opzioni, i prezzi sono diversi. Presta attenzione alle informazioni sugli sconti.

## <a name="walkthrough-import-items-from-shopify" />Procedura dettagliata: importare articoli da Shopify

### <a name="scenario" />Scenario

Hai già un punto vendita online di successo e vorresti iniziare a usare [!INCLUDE[prod_short](../includes/prod_short.md)] come software gestionale aziendale. Desideri importare quanti più dati possibile da Shopify. 

### <a name="steps" />Passaggi

Questa è una continuazione di [Procedura dettagliata: iniziare a vendere prodotti online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Puoi anche provare con i tuoi dati, ad esempio la tua sandbox o il tuo punto vendita Shopify.

In [!INCLUDE[prod_short](../includes/prod_short.md)], effettua i seguenti passaggi:

#### <a name="prepare-data" />Preparare i dati

1. Passa a una prova gratuita di 30 giorni senza dati di esempio. Per ulteriori informazioni, vedi [Aggiungere i propri dati a una prova vuota](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
3. Scegli l'azione **Nuovo**.
4. Nel campo **Codice**, immetti `DEMO2`.
5. Nel campo **URL Shopify**, immetti l'URL al punto vendita online a cui desideri connetterti.
6. Attiva l'interruttore **Abilitato**, rivedi e accetta i termini e le condizioni.

Configura il punto vendita Shopify come descritto di seguito nei prossimi passaggi:

7. Abilita l'interruttore **Log abilitato**.
8. Disabilita l'opzione **Consenti sincronizzazioni in background**.
9. Seleziona **Da Shopify** nel campo **Sincronizza articolo**.
5. Abilita l'interruttore **Crea automaticamente articoli sconosciuti**.
11. Compila il campo **Codice modello articolo** con il modello appropriato.
12. Seleziona **Da Shopify** nel campo **Sincronizza immagini articolo**.
13. Seleziona **Tutti i clienti** in **Importazione clienti da Shopify**.
14. Abilita l'interruttore **Crea automaticamente clienti sconosciuti**.
15. Compila il campo **Codice modello cliente** con il modello appropriato.
16. Compila il campo **Conto spese spedizione**, **Conto mance** con il conto ricavi. Ad esempio, negli Stati Uniti, utilizza `40100`.
17. Abilita l'interruttore **Creazione automatica degli ordini**.

#### <a name="run-the-synchronization" />Esegui la sincronizzazione

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita *DEMO2* per il quale desideri sincronizzare i dati per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Sincronizza prodotti**.
4. Scegli l'azione **Sincronizza immagini prodotto**.
5. Scegli l'azione **Sincronizza clienti**.

### <a name="results" />Risultati

* I prodotti Shopify vengono importati. Per verificare, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Prodotti Shopify**, quindi scegli il collegamento correlato.
* Vengono creati elementi con immagini. Per verificare, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articolo** e scegli il collegamento correlato.
* I clienti Shopify vengono importati. Per verificare, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti Shopify**, quindi scegli il collegamento correlato.
* I clienti vengono creati. Per verificare, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.


## <a name="see-also" />Vedi anche

[Iniziare a usare il connettore Shopify](get-started.md)  
