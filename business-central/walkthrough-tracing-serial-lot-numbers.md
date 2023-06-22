---
title: Procedura dettagliata - Tracciabilità dei numeri seriali/lotto
description: Questo argomento descrive le azioni necessarie per evitare la vendita di un articolo difettoso e anche come rintracciare e richiamare gli articoli quando necessario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# <a name="walkthrough-tracing-seriallot-numbers" />Procedura dettagliata: Tracciabilità dei numeri seriali/lotto

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In caso di prodotti difettosi, è necessario identificare gli errori e impedire la distribuzione degli articoli interessati. Qualora vengano spediti prodotti difettosi, è necessario risalire al destinatario e, se necessario, richiederne la restituzione.  

Il primo task della gestione dei difetti consiste nell'identificare la provenienza degli articoli difettosi e le ubicazioni in cui sono stati utilizzati. Questa analisi è basata su dati storici e può essere semplificata svolgendo ricerche tra i movimenti di tracciabilità articoli nella pagina **Tracciabilità articolo**.  

Il secondo task consiste nel determinare se gli articoli tracciati sono pianificati in documenti aperti, ad esempio ordini di vendita non registrati o registrazioni consumi. Questa operazione viene eseguita nella pagina **Trova movimenti**. È possibile utilizzare la funzione Trova movimenti per individuare tutti i tipi di record di database.  

## <a name="about-this-walkthrough" />Informazioni sulla procedura dettagliata

In questa procedura dettagliata viene illustrato come identificare gli articoli difettosi, il loro fornitore e in quali ubicazioni sono stati utilizzati in modo da poter fare un richiamo sugli ordini o bloccarli.  

In questa procedura dettagliata sono illustrati i task seguenti:  

- Tracciabilità dall'utilizzo all'origine.  
- Tracciabilità dall'origine all'utilizzo.  
- Ricerca di tutti i record correnti che contengono il numero seriale/di lotto tracciato  

## <a name="roles" />Ruoli

Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

- Manager qualità  
- Manager warehouse  
- Gestore ordini  
- Rivenditore  

## <a name="prerequisites" />Prerequisiti

Per completare questa procedura dettagliata, sarà necessario:  

- La società [!INCLUDE[prod_short](includes/prod_short.md)].  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## <a name="story" />Scenario

Luca, il manager qualità, deve occuparsi di un reso vendita dell'articolo 1002, una bicicletta da corsa. Il cliente, Selangorian Ltd., sostiene che alcune delle saldature presenti sul telaio hanno ceduto. I tecnici del controllo qualità confermano che il telaio della bicicletta restituita è effettivamente difettoso. Il manager qualità deve a questo punto determinare:  

- Il lotto dei telai difettosi.  
- L'ordine di acquisto con cui è stato ricevuto il lotto difettoso.  

Il reparto vendite comunica al manager qualità che il numero seriale della bicicletta restituita, l'articolo 1002, è NS1. Con questa informazione di base Luca dovrà determinare il luogo in cui la bicicletta da corsa finita è stata utilizzata l'ultima volta e quindi tracciare all'indietro l'origine per stabilire il lotto di provenienza del componente difettoso.  

I risultati di questo primo task di tracciabilità articolo consentono di identificare i telai difettosi e il loro fornitore. In seguito, ma nello stesso processo di tracciabilità, il manager qualità dovrà trovare tutte le biciclette vendute prodotte con il telaio proveniente dal lotto difettoso in modo da poter fare un richiamo o bloccare tutti gli ordini interessati. Infine, il manager qualità dovrà trovare tutti i documenti aperti in cui viene utilizzato il lotto difettoso, affinché non vengano effettuate ulteriori transazioni.  

I primi due task di gestione dei difetti vengono eseguiti nella pagina **Tracciabilità articolo**. L'ultimo task viene invece eseguito nella pagina **Trova movimenti** in combinazione con la pagina **Tracciabilità articolo**.  

## <a name="prepare-sample-data" />Preparazione dei dati di esempio

È necessario creare i nuovi articoli seguenti:  

- 2000, Telaio da corsa: tracciabilità basata sul lotto, componente di 1002  
- 1002, Bicicletta da corsa: tracciabilità basata sul numero seriale  

Sarà quindi necessario creare diverse transazioni di acquisto, produzione e vendita con i due articoli.  

### <a name="to-create-the-items" />Per creare gli articoli

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Nr.** immettere **2000**, quindi procedere al completamento dei campi seguenti.  

    |Descrizione|Unità di misura base|Righe Cat. reg. art./serv.|Cat. reg. art./serv. IVA|Cat. reg. magazzino|Codice tracciabilità articolo|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Telaio da corsa|PZ|MAT. PRIME|IVA25|MAT. PRIME|LOTTI|  

    > [!NOTE]  
    >  Per immettere l'unità di misura base, fare clic sul pulsante **Nuovo**, quindi selezionare **PSC** nella pagina **Unità di misura articoli**.  

4. Tutti gli altri campi contengono dati di default accettabili o non devono essere compilati.  
5. Scegliere **OK** per creare la prima nuova scheda articolo, 2000.  
6. Selezionare **Nuovo**.  
7. Nel campo **Nr.** immettere **1002**, quindi procedere al completamento dei campi seguenti.  

    |Descrizione|Unità di misura base|Righe Cat. reg. art./serv.|Cat. reg. art./serv. IVA|Cat. reg. magazzino|Sistema di rifornimento|Codice tracciabilità articolo|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Bicicletta da corsa|PZ|DETTAGLIO|IVA25|PR. FINITI|Ord. prod.|NSTUTTI|  

    > [!NOTE]  
    >  Per immettere l'unità di misura base, fare clic sul pulsante **Nuovo**, quindi selezionare **PSC** nella pagina **Unità di misura articoli**.  

    A questo punto, definire il setup manufacturing dell'articolo.

8. Nella Scheda dettaglio **Rifornimento** immettere **1000** nel campo **Nr. ciclo**.  
9. Scegliere il campo **Nr. DB di produzione**, quindi **Avanzate**.  
10. Nella pagina **Lista DB produzione** scegliere la prima riga, **1000**, quindi selezionare l'azione **Modifica**.  
11. Nella pagina **DB produzione** modificare il valore nel campo **Stato** in **In sviluppo**.  
12. Spostarsi su una riga vuota, immettere **2000** nel campo **Nr.** quindi immettere **1** nel campo **Quantità per**.  
13. Modificare il valore nel campo **Stato** in **Certificata**.  
14. Selezionare il pulsante **OK** per registrare la distinta base di produzione nella scheda articolo e chiudere la pagina **DB produzione**.  

    A questo punto, acquistare telai da corsa da Custom Metals Incorporated.  

### <a name="to-purchase-components" />Per acquistare i componenti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Creare un ordine di acquisto per il fornitore, Custom Metals Incorporated, compilando i seguenti campi della riga.  

    |Articolo|Quantità|Nr. lotto|  
    |----|--------|-------|  
    |2000|10|LOTTO1|  

4. Per immettere il numero di lotto, scegliere l'azione **Righe tracciabilità articolo**.  
5. Nella pagina **Righe tracciabilità articolo** compilare i campi **Nr. lotto** e **Quantità (base)**, quindi chiudere la pagina.  
6. Immettere un valore nel campo **Nr. fatt. fornitore**.  
7. Scegliere l'azione **Registra**, selezionare l'opzione **Carico e fattura**, quindi il pulsante **OK**.  

    A questo punto, acquistare i telai da corsa da Coolwood Technologies.  
8. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
9. Scegliere l'azione **Nuovo**.
10. Creare un ordine di acquisto per il fornitore, Coolwood Technologies, compilando i seguenti campi della riga.  

    |Articolo|Quantità|Nr. lotto|  
    |----------|--------------|-------------|  
    |2000|11|LOTTO2|  

11. Per immettere il numero di lotto, selezionare nel gruppo **Riga** della Scheda dettaglio **Righe** l'azione **Righe tracciabilità articolo**.  
12. Nella pagina **Righe tracciabilità articolo** compilare i campi **Nr. lotto** e **Quantità (base)**, quindi chiudere la pagina.  
13. Immettere un valore nel campo **Nr. fatt. fornitore**.  
14. Scegliere l'azione **Registra**, selezionare l'opzione **Carico e fattura**, quindi il pulsante **OK**.  

    Quindi, produrre due biciclette da corsa, NS1 e NS2.  

### <a name="to-produce-end-items" />Per produrre gli articoli finali

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di produzione rilasciati**, quindi scegli il collegamento correlato.  
2. Scegliere il gruppo **Nuovo**.  
3. Creare un nuovo ordine di produzione rilasciato compilando i campi seguenti.  

    |Nr. origine|Quantità|Nr. seriale|  
    |----------|--------|----------|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4. Scegliere l'azione **Aggiorna ordine produzione**, quindi scegliere il pulsante **OK** per compilare la riga.  
5. Per immettere i numeri seriali, scegliere l'azione **Righe tracciabilità articolo**.  
6. Nella pagina **Righe tracciabilità articolo** compilare i campi **Nr. seriale** e **Quantità (base)**, quindi chiudere la pagina.  

    Successivamente, registrare i consumi dei telai da corsa dal LOTTO1.  
7. Nella pagina **Ordine produzione rilasciato** selezionare l'azione **Registrazioni di produzione**.  
8. Nella pagina **Registrazioni di produzione** selezionare la riga consumi per l'articolo 2000 e scegliere l'azione **Righe tracciabilità articolo**.
9. Nella pagina **Righe tracciabilità articolo** scegliere il campo **Nr. lotto**, selezionare **LOTTO1**, quindi scegliere **OK**.  
10. Lasciare invariati tutti gli altri valori di default nella pagina **Registrazioni di produzione** e scegliere l'azione **Registra**.  

    Quindi, produrre altre due biciclette da corsa, NS3 e NS4.  

11. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di produzione rilasciati**, quindi scegli il collegamento correlato.  
12. Scegliere l'azione **Nuovo**.  
13. Creare un nuovo ordine di produzione rilasciato compilando i campi seguenti nella testata.  

    |Nr. origine|Quantità|Nr. seriale|  
    |----------------|--------------|----------------|  
    |1002|2|NS3|  
    |1002|2|NS4|  

14. Scegliere l'azione **Aggiorna ordine produzione** per compilare la riga.  
15. Per immettere i numeri seriali, selezionare l'azione **Righe tracciabilità articolo** e i numeri su due righe nel campo **Nr. seriale** nella pagina **Righe tracciabilità articolo**.  

    Successivamente, registrare più consumi dei telai da corsa dal LOTTO1.  
16. Nella pagina **Ordine produzione rilasciato** selezionare l'azione **Registrazioni di produzione**.  
17. Nella pagina **Registrazioni di produzione** selezionare la riga consumi per l'articolo 2000 e scegliere l'azione **Righe tracciabilità articolo**.
18. Nella pagina **Righe tracciabilità articolo** scegliere il campo **Nr. lotto**, selezionare **LOTTO1**, quindi scegliere **OK**.  
19. Lasciare invariati tutti gli altri valori di default nella pagina **Registrazioni di produzione** e scegliere l'azione **Registra**.  

    Sono state prodotte quattro biciclette da corsa, da NS1 a NS4, e consumati quattro dei dieci telai da corsa del LOTTO1, due telai in ogni ordine di produzione.  

20. Chiudere le registrazioni e gli ordini di produzione.  

    A questo punto, vendere le biciclette. In primo luogo vendere la bicicletta da corsa con NS1 a Selangorian Ltd.  

### <a name="to-sell-the-end-items" />Per vendere gli articoli finali

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**, quindi creare un ordine di vendita compilando i campi seguenti.  

    |Cliente|Articolo|Qtà|Nr. seriale|  
    |--------------|----------|----------|----------------|  
    |Grafiche magiche 2000|1002|1|SN1|  

3.  Per immettere il numero seriale, selezionare l'azione **Righe tracciabilità articolo** e il numero nel campo **Nr. seriale** della pagina **Righe tracciabilità articolo**.  
4.  Scegliere l'azione **Registra**, selezionare l'opzione **Spedisci e fattura**, quindi il pulsante **OK**.  

    Infine, vendere la bicicletta da corsa con NS2 a The Cannon Group PLC.  

5.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
6.  Scegliere l'azione **Nuovo**, quindi creare un ordine di vendita compilando i campi seguenti.  

    |Cliente|Articolo|Qtà|Nr. seriale|  
    |--------------|----------|----------|----------------|  
    |Cannon Group SpA.|1002|1|SN2|  

7.  Per immettere il numero seriale, selezionare l'azione **Righe tracciabilità articolo** e il numero nel campo **Nr. seriale** della pagina **Righe tracciabilità articolo**.  
8.  Scegliere l'azione **Registra**, selezionare l'opzione **Spedisci e fattura**, quindi il pulsante **OK**.  

    Infine, vendere alcuni telai da corsa separatamente. Cannon Group SpA ordina quattro telai da corsa separati per la sua linea di montaggio.  

9. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
10. Scegliere l'azione **Nuovo**, quindi creare un ordine di vendita compilando i campi seguenti.  

    |Cliente|Articolo|Qtà|Nr. seriale|  
    |--------------|----------|----------|----------------|  
    |Cannon Group SpA.|2000|5|LOTTO1|  

11. Per immettere il numero seriale, nella Scheda dettaglio **Righe**, nel gruppo **Riga**, selezionare l'azione **Righe tracciabilità articolo** e il numero nel campo **Nr. seriale** nella pagina **Righe tracciabilità articolo**.  

    > [!NOTE]  
    >  Non registrare l'ultimo ordine di vendita per cinque telai da corsa.  

    I dati necessari per illustrare le funzionalità Tracciabilità articolo e Trova movimenti sono pronti.  

## <a name="tracing-from-usage-to-origin" />Tracciabilità dall'utilizzo all'origine

 Il reparto vendite comunica al manager qualità che il numero seriale della bicicletta restituita, l'articolo 1002, è NS1. Con questa informazione di base può determinare dove la bicicletta da corsa finita è stata utilizzata l'ultima volta, in questo caso nella spedizione a Selangorian Ltd. Il manager qualità deve quindi tracciare all'indietro l'origine per stabilire il lotto di provenienza del telaio difettoso e il relativo fornitore.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it" />Per risalire al lotto che includeva il telaio difettoso e al relativo fornitore

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Tracciabilità articolo**, quindi scegli il collegamento correlato.  
2.  Nella pagina **Tracciabilità articolo** immettere **NS1** nel campo **Filtro nr. seriale**, quindi immettere **1002** nel campo **Filtro articolo**.  
3.  Mantenere l'impostazione di default **Solo articoli tracciati** nel campo **Mostra componenti** e il metodo di analisi **Utilizzo - Origine** nel campo **Metodo analisi**.  
4.  Scegliere l'azione **Analizza**.  

    Si noti che una testata spedizione vendita corrisponde ai criteri di ricerca. Prima di continuare, verificare che la spedizione sia quella della bicicletta da corsa difettosa effettuata a Selangorian Ltd.  

5.  Selezionare la riga di analisi quindi scegliere l'azione **Mostra documento**.  

    Continuare a tracciare l'origine della spedizione di vendita della bicicletta da corsa con il numero NS1.  
6.  Fare clic sull'icona + sulle righe di tracciabilità per espandere gradualmente e percorrere all'indietro la catena di transazioni da cui ha avuto origine la spedizione.  

    È possibile analizzare il seguente storico delle transazioni:  

    - Il primo documento registrato immediatamente precedente nella catena di transazioni è la registrazione di output SN1 dal primo ordine di produzione rilasciato.  
    - Questo documento è a sua volta preceduto dalla registrazione consumi dal primo ordine di produzione rilasciato. Il manager qualità nota che è stato utilizzato un telaio da corsa appartenente al LOTTO1.  
    - L'ultimo documento registrato di questa catena è la ricezione acquisti registrata con cui i telai da corsa del LOTTO1 sono entrati in magazzino.  

    Il manager qualità ha così individuato il lotto dei telai difettosi e può quindi cercare l'ultima riga di tracciabilità per vedere il fornitore, ovvero Custom Metals Incorporated.  

    > [!NOTE]  
    >  Non apportare ulteriori modifiche al risultato di tracciabilità, perché verrà utilizzato nella sezione successiva.  

     Il primo task di gestione dei difetti tramite la pagina **Tracciabilità articolo** è stato completato. Il manager qualità deve ora determinare se altri documenti registrati hanno gestito telai da corsa del LOTTO1.  

## <a name="tracing-from-origin-to-usage" />Tracciabilità dall'origine all'utilizzo

 Il manager qualità ha stabilito che i telai da corsa difettosi appartenevano al LOTTO1. Deve ora trovare eventuali altre biciclette prodotte con i telai difettosi in modo da fare un richiamo sull'ordine o bloccarlo.  

 Un modo per preparare questo task di analisi nella pagina **Tracciabilità articolo** consiste nell'immettere manualmente LOTTO1 nel campo **Filtro nr. lotto** e 2000 nel campo **Filtro articolo**. Tuttavia, questa procedura dettagliata utilizza la funzione **Analizza opposto - da Riga** .  

### <a name="to-find-all-usage-of-the-faulty-lot" />Per trovare tutti gli utilizzi del lotto difettoso

1.  Nella pagina **Tracciabilità articolo** selezionare la riga della ricezione acquisti, l'ultima riga di analisi e scegliere **Analizza opposto - da Riga**.  

    Il risultato è basato sui filtri della riga di tracciabilità per la ricezione acquisti, LOTTO1 e articolo 2000, e sul metodo di analisi **Origine - Utilizzo**.  

    Per una sintesi di tutti gli utilizzi dell'articolo 2000 con LOTTO1, continuare a espandere tutte le righe di tracciabilità.  

2.  Scegliere l'azione **Espandi tutto**.  

    Le prime quattro righe di tracciabilità fanno riferimento alla spedizione a Selangorian Ltd., che è già stata risolta. L'ultima riga indica che è stata prodotta un'altra bicicletta, NS2, nello stesso ordine di produzione rilasciato e che è stata venduta e spedita con un'altra spedizione.  

    Il manager qualità informa immediatamente il reparto vendite affinché possano avviare un richiamo della bicicletta difettosa presso il cliente, Cannon Group PLC.  

    Allo stesso tempo, nota dalle ultime tre righe di tracciabilità che altri due articoli, NS3 e NS4, sono stati prodotti con telai del LOTTO1. Decide di agire per bloccare questi articoli in magazzino.  

    Il secondo task di gestione dei difetti tramite la pagina **Tracciabilità articolo** è stato completato. Poiché la pagina **Tracciabilità articolo** è basata unicamente sui movimenti registrati, il manager qualità deve passare alla pagina **Trova movimenti** per assicurarsi che il LOTTO1 non venga utilizzato nei documenti non registrati.  

## <a name="finding-all-records-of-a-seriallot-number" />Ricerca di tutti i record di un numero seriale/di lotto

 Tramite la pagina **Tracciabilità articolo** il manager qualità ha stabilito che i telai da corsa difettosi appartenevano al LOTTO1, ha individuato il loro fornitore e le transazioni registrate in cui sono state utilizzate. Deve ora determinare se il LOTTO1 esiste in documenti aperti passando alla pagina **Trova movimenti** in cui può eseguire una ricerca in tutti i record di database.  

### <a name="to-find-all-occurrences-of-lot-in-non-posted-records-such-as-open-orders" />Per trovare tutte le occorrenze del LOTTO1 nei record non registrati, ad esempio ordini aperti

1.  Nella pagina **Tracciabilità articolo** selezionare la prima riga di tracciabilità, la ricezione acquisti del LOTTO1.  
2.  Scegliere l'azione **Trova movimenti**.  

    La pagina **Trova movimenti** viene preimpostata con filtri di ricerca in base al risultato di analisi per il LOTTO1. Il manager qualità riconosce la maggior parte dei record che riguarda documenti già identificati nella pagina **Tracciabilità articolo**. Ad esempio, l'ultima riga Trova movimenti di tipo Ordine di produzione fa riferimento ai due ordini di produzione rilasciati che hanno utilizzato i telai del LOTTO1.  

    Tuttavia, la seconda riga Trova movimenti di tipo **Righe vendite** è una riga documento non registrata, pertanto il manager qualità procede con l'analisi.  

3.  Per aprire il record Righe vendite, selezionare la seconda riga Trova movimenti e scegliere l'azione **Mostra**. In alternativa, selezionare il valore nel campo **Nr. di record**.  

    Il manager qualità nota una riga vendite aperta per i telai da corsa difettosi. Suggerisce immediatamente al reparto vendite che questo ordine deve essere annullato e che è necessario avviare un nuovo ordine di produzione basato su telai non difettosi.  

 La procedura dettagliata relativa all'utilizzo della pagina **Trova movimenti** per la gestione dei difetti in combinazione con la pagina **Tracciabilità articolo** è stata completata.  

## <a name="see-related-microsoft-trainingtrainingpathsuse-serial-lot-numbers" />Vedi il relativo [training Microsoft](/training/paths/use-serial-lot-numbers/)

## <a name="see-also" />Vedere anche

[Utilizzare i numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)  
[Trova movimenti](ui-find-entries.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
