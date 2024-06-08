---
title: Impostare e fatturare pagamenti anticipati di vendite
description: I pagamenti anticipati sono pagamenti che vengono fatturati e registrati in un ordine di pagamento anticipato di vendita o di acquisto prima della fatturazione finale.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 01/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-set-up-and-invoicing-sales-prepayments"></a>Procedura dettagliata: impostare e fatturare pagamenti anticipati di vendite

Questa procedura dettagliata illustra il processo di configurazione e di utilizzo dei pagamenti anticipati in [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Ad esempio, è possibile inviare altre fatture di pagamento anticipato se vengono aggiunti più articoli all'ordine.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata

In questa procedura dettagliata verranno descritti gli scenari seguenti:  

- Impostazione dei pagamenti anticipati  
- Creazione di un ordine che richiede un pagamento anticipato  
- Creazione di una fattura di pagamento anticipato  
- Correzione dei requisiti di pagamento anticipato di un ordine  
- Collegamento di pagamenti anticipati a un ordine  
- Fatturazione dell'importo finale di un ordine con pagamento anticipato  

### <a name="roles"></a>Ruoli

Questa procedura dettagliata include task per i seguenti ruoli:  

- Manager contabilità (Barbara Zighetti)  
- Gestore ordini (Elisabetta Scotti)  
- Amministratore contabilità clienti (Armando Pinto)  

## <a name="story"></a>Scenario

 Barbara un manager di contabilità e spetta a lei decidere quali clienti devono versare un deposito prima che gli articoli siano lavorati o spediti. Barbara imposta [!INCLUDE[prod_short](includes/prod_short.md)] per calcolare i pagamenti anticipati automaticamente.  

 Elisabetta Scotti è un gestore ordini di vendita. Quando un cliente chiama per effettuare un ordine, Elisabetta inserisce l'ordine nel sistema mentre il cliente è al telefono. In questo modo, Elisabetta può verificare subito i prezzi e le condizioni di pagamento con il cliente e può procedere alle modifiche all'ordine mentre negozia con il cliente.  

 Armando lavora nel reparto Contabilità clienti e registra fattura e pagamenti.  

 In questo scenario, Barbara definisce i requisiti di pagamento anticipato per il cliente Selangorian in base al suo storico di credito. Barbara dà istruzioni a Elisabetta su come gestire gli ordini.  

 Quando il cliente chiama, Elisabetta negozia con il cliente fino a raggiungere un accordo, quindi sceglie di calcolare il pagamento anticipato in diversi modi.  

 Dopo che Elisabetta ha emesso la fattura per il pagamento anticipato, il cliente ordina un articolo aggiuntivo. Elisabetta aggiorna l'ordine e crea una seconda fattura per il pagamento anticipato.  

 Armando registra il pagamento del cliente, lo collega alle fatture e invia la fattura finale.  

## <a name="set-up-prepayments"></a>Impostare i pagamenti anticipati

Barbara imposta il sistema per la gestione dei pagamenti anticipati da parte dei clienti.  

- Decide di adottare per i pagamenti anticipati la stessa numerazione utilizzata per le fatture di vendita.  
- Imposta l'applicazione in modo che controlli automaticamente se sono previsti pagamenti anticipati prima della fatturazione finale di un ordine.  
- Imposta i valori predefiniti per le percentuali di pagamento anticipato da richiedere per specifici articoli e clienti.  

Le seguenti procedure illustrano come svolgere i task di Barbara:  

### <a name="to-set-up-number-series-for-prepayments"></a>Per impostare la numerazione per i pagamenti anticipati

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup contabilità clienti** espandere la Scheda dettaglio **Numerazioni**.  
3. Verificare che la numerazione per le fatture di pagamento anticipato registrate nel campo **Nr. fatt. pagam. ant. reg.** sia la stessa delle fatture di vendita registrate (**Nr. fatture registrate**) e che la numerazione per le note di credito registrate per i pagamenti anticipati (**Nr. note cr. pagam. ant. reg.**) sia la stessa delle note di credito registrate (**Nr. note credito registrate**).  

### <a name="to-block-shipments-for-unpaid-prepayment"></a>Per bloccare le spedizioni in caso di mancato versamento del pagamento anticipato

1. Nella Scheda dettaglio **Generale** della pagina **Setup contabilità clienti** selezionare la casella di controllo **Verifica pagamento anticipato durante la registrazione**.

Non è possibile spedire o fatturare un ordine con un importo pagamento anticipato non pagato.  

Barbara stabilisce che, come regola di default, al cliente 20000 venga fatturato il 30% di anticipo su tutti gli ordini. Pertanto, Barbara inserisce una percentuale predefinita di pagamento anticipato nella scheda cliente.  

Stabilisce altresì che a tutti i clienti sia richiesto un deposito del 20% per l'articolo 1896-S. Il cliente 20000 ha uno storico dei pagamenti insoddisfacente e quindi il suo pagamento anticipato per l'articolo 1896-S sarà del 40%. La procedura seguente spiega come impostare le percentuali di pagamento anticipate di default.  

### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Per assegnare percentuali predefinite di pagamento anticipato a clienti e articoli

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Clienti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda per il cliente 20000 (Trey Research).
3. Nella Scheda dettaglio **Pagamenti**, nel campo **% pagamento anticipato** immettere **30**.  
4. Scegliere l'azione **Correlata**, selezionare la voce di menu **Vendite**, quindi scegliere la voce di menu **Percentuali pagamenti anticipati**.  
5. Compilare nel modo seguente due righe della pagina **Percentuali pagamenti anticipati vendite**:  

    |**Tipo vendita**|**Codice vendita**|**Nr. Articolo**|**% pagamento anticipato**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Cliente**|**20000**|**1896-S**|**40**|
    |**Cliente**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > In base al proprio paese/area geografica, è inoltre necessario specificare un codice gruppo imposta nella Scheda dettaglio **Costi e registrazione** per l'articolo 1896-S. Quando si utilizza la società demo, questo campo è già impostato.

6. Chiudere tutte le pagine.  

### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Per specificare un conto per i pagamenti anticipati di vendita nel setup registrazioni COGE

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni COGE**, quindi scegli il collegamento correlato.  
2. Selezionare la riga in cui il campo **Cat. reg. business gen.** è impostato su **DOMESTICO** e il campo **Cat. reg. articolo/servizio** è impostato su **DETTAGLIO**.  
3. Nel campo **Conto pagam. anticipati vendite**, specificare l'account pertinente. La tua selezione viene salvata automaticamente.  

> [!TIP]
> Se non è possibile vedere il campo nella pagina **Setup registrazioni COGE**, utilizzare la barra di scorrimento orizzontale nella parte inferiore della pagina per scorrere verso destra.  

## <a name="create-an-order-that-requires-a-prepayment"></a>Creare un ordine che richiede un pagamento anticipato

 Nello scenario seguente, Elisabetta, il gestore ordini, crea un ordine mentre parla con un cliente. Gli articoli che il cliente sta ordinando richiedono un pagamento anticipato. Inoltre, il cliente ha effettuato alcuni pagamenti in ritardo in passato. Elisabetta ha ricevuto istruzione di richiedergli l'importo fisso di **800** euro come pagamento anticipato per l'ordine.  

Il cliente chiede di pagare il 35%, ed Elisabetta, essendo autorizzata ad accogliere la richiesta, modifica l'ordine.  

Crea quindi la fattura di pagamento anticipato e la invia al cliente  

### <a name="to-create-a-sales-order-with-a-prepayment"></a>Per creare un ordine di vendita con un pagamento anticipato

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Nome cliente** scegliere **Trey Research**.  
4. Chiudere l'avviso di oltre fido visualizzato.  
5. Compilare due righe di vendita nel modo seguente.  

    |**Tipo**|**Nr.**|**Quantità**|  
    |--------------|-------------|------------------|  
    |**Articolo**|**1896-S**|**1**|  
    |**Articolo**|**1900-S**|**1**|

    I campi del pagamento anticipato nella riga di vendita sono nascosti per default. Per visualizzare i campi, è necessario personalizzare la pagina. Per ulteriori informazioni, vedere [Per avviare la personalizzazione di una pagina tramite il banner Personalizzazione](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

6. Verificare che il campo **% pagamento anticipato** sulla riga dell'articolo **1900-S** contenga **30**. Il valore di default è stato copiato dalla testata di vendita, popolata dalla scheda cliente.  

    Il campo **% pagamento anticipato** sulla riga dell'articolo **1896-S** contiene **40**. 40 è la percentuale immessa nella pagina **Percentuali pagamenti anticipati vendite** per l'articolo **1896-S** e il cliente **20000**.  

    Per ulteriori informazioni, vedere [Impostare i pagamenti anticipati](finance-set-up-prepayments.md).  
7. Nell'azione **Ordine**, scegli **Statistiche**.  
8. Nella Scheda dettaglio **Pagamento anticipato**, il campo **Importo pagam. ant. IVA escl.** contiene il valore **458.16**. Se crei ora una fattura di pagamento anticipato per l'ordine, 458,16 è l'importo sulla fattura.  

    In questo scenario, Elisabetta deve chiedere al cliente un pagamento anticipato totale di **800**.  

    > [!IMPORTANT]  
    >  In base al proprio paese/area geografica, il seguente passaggio potrebbe non essere applicabile.  
9. Modificare in **800** l'importo nel campo **Importo pagam. ant. IVA escl.** e chiudere la pagina.  
10. Controlla il campo **% pagamento anticipato** nelle righe di vendita: puoi constatare che è stato ricalcolato in **67,02438** e **67,02282**.  

     Il calcolo include tutte le righe che hanno una percentuale di pagamento anticipato superiore a zero.  

     Ora il cliente chiede se la percentuale di pagamento anticipato può essere impostata su 35%. Il supervisore di Elisabetta accetta la modifica.
11. Nella pagina **Ordine vendita**, nella Scheda dettaglio **Pagamento anticipato** del campo **% pagamento anticipato**, immettere **35**.  
12. Nel messaggio di avviso visualizzato, selezionare il pulsante **Sì** . Un tasso del 35% verrà applicato come percentuale di pagamento per l'intero ordine.  
13. Verifica che le righe siano state aggiornate correttamente.  

## <a name="create-a-prepayment-invoice"></a>Creare una fattura di pagamento anticipato

Dopo aver inserito nell'ordine i valori di pagamento anticipato corretti, Elisabetta crea la fattura di pagamento anticipato e la invia al cliente.  

### <a name="to-create-a-prepayment-invoice"></a>Per creare una fattura di pagamento anticipato

1. Nella pagina **Ordine vendita**, selezionare **Azioni**, quindi **Registrazione**, **Pagamento anticipato** e quindi selezionare **Registra e stampa fattura pagam. ant.**
2. Scegli **Sì** per registrare la fattura.  

> [!NOTE]  
> Susan invierebbe ora la fattura al cliente.  

## <a name="create-an-additional-prepayment-invoice"></a>Creare una fattura di pagamento anticipato aggiuntiva

Il giorno seguente, il cliente chiama Elisabetta e apporta modifiche all'ordine. Il cliente desidera due articoli 1896-S. Elisabetta riapre e aggiorna l'ordine, crea una seconda fattura per il pagamento anticipato dell'ordine e la invia al cliente.  

### <a name="to-create-an-additional-prepayment-invoice"></a>Per creare una fattura di pagamento anticipato aggiuntiva

1. Nella pagina **Ordine vendita**, scegliere l'azione **Rilascia**, quindi **Riapri**.  
2. Immettere **2** nel campo **Quantità** della riga dell'articolo **1896-S**.  

    Nell'azione **Ordine**, scegli **Statistiche**. Il campo **Importo pagam. ant. IVA esclusa** ora contiene **768,04** e il campo **Fattura importo pagam. ant. IVA esclusa** contiene **417,76**. Questi valori indicano l'esistenza di un importo di pagamento anticipato aggiuntivo che non è stato ancora fatturato.  
3. Per registrare una fattura per l'importo aggiuntivo, seleziona **Azioni**, quindi **Registrazione**, **Pagamento anticipato** e infine seleziona **Registra e stampa fattura pagam. ant.**
4. Scegli **Sì** per registrare la fattura.  

## <a name="apply-the-prepayments"></a>Applicare i pagamenti anticipati

Il cliente paga l'importo del pagamento anticipato. Armando, dell'ufficio contabilità, registra il pagamento e lo applica alle fatture di pagamento anticipato.  

### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Per collegare un pagamento a una fattura di pagamento anticipato

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni incassi**, quindi scegli il collegamento correlato.  
2. Compilare una riga di registrazione con le informazioni indicate di seguito.  

    |Nome campo|Immettere|  
    |----------------|-----------|  
    |**Tipo di documento**|**Pagamento**|  
    |**Tipo conto**|**Cliente**|  
    |**Nr. conto**|**20000**|  
3. Scegli l'azione **Processi** e poi **Collega movimenti**.  
4. Nella pagina **Collega mov. cliente** selezionare la prima fattura di pagamento anticipato, quindi scegliere l'azione **Processo** e infine l'azione **Imposta Collega a ID**.  
5. Ripetere il passaggio precedente per il secondo pagamento anticipato.  
6. Scegli il pulsante **OK**.  

    Nei campi **Importo** è ora riportata la somma delle due fatture di pagamento anticipato.  

7. Per pubblicare il diario, scegliere l'azione **Registra/Stampa**, quindi selezionare **Invia**.
8. Scegliere il pulsante **Sì**.

## <a name="invoice-the-remaining-amount"></a>Fatturare l'importo residuo

Ora l'amministratore della contabilità clienti, Armando, è stato informato che gli articoli dell'ordine sono stati spediti e che l'ordine è pronto per essere fatturato. Armando crea quindi la fattura per l'ordine.  

### <a name="to-invoice-the-remaining-amount"></a>Per fatturare l'importo residuo

1. Aprire l'ordine di vendita.
2. Scegliere l'azione **Pubblicazione**, quindi **Invia**.
3. Selezionare **Spedizione e Fattura** e quindi fare clic sul pulsante **OK**.
4. Se si desidera vedere in anteprima la fatture, fare clic sul pulsante **Sì**.

    > [!NOTE]  
    > A questo punto il reparto spedizioni ha di norma già registrato la spedizione.  

    Armando può visualizzare lo storico per verificare che la fattura di vendita sia stata creata come concepita.

5. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Fatture di vendita registrate**, quindi scegli il collegamento correlato.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Aggiornare automaticamente lo stato di ordini e fatture con pagamento anticipato

È possibile velocizzare l'elaborazione di ordini e fatture impostando movimenti nella coda processi che aggiornano automaticamente lo stato di tali documenti. Quando viene pagata una fattura con pagamento anticipato, le voci della coda processi possono modificare automaticamente lo stato del documento da **In attesa di pagamento anticipato** a **Rilasciato**. Quando imposti le voci della coda processi, le codeunit che dovrai utilizzare sono **383 Aggiornamento pagamento anticipato vendita in sospeso** e **383 Aggiornamento pagamento anticipato acquisto in sospeso**. Ti consigliamo di pianificare l'esecuzione frequente delle voci, ad esempio ogni minuto. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="next-steps"></a>Passaggi successivi

In questa procedura dettagliata sono stati esaminati i passaggi per impostare la funzione di gestione dei pagamenti anticipati in [!INCLUDE[prod_short](includes/prod_short.md)]. 

- Imposta le percentuali predefinite di pagamento anticipato per clienti e articoli.
- Utilizza metodi diversi per calcolare i pagamenti anticipati su un ordine.  
- Calcola l'importo del pagamento anticipato come percentuale del totale dell'ordine.
- Assegna un importo totale di pagamento anticipato all'ordine.  

Inoltre, è stata registrata una fattura di pagamento anticipato, creata una fattura per un secondo pagamento anticipato in seguito alla modifica dell'ordine e registrata la fattura finale per l'importo residuo.  

Le funzionalità di pagamento anticipato semplificano l'impostazione e l'applicazione delle regole di pagamento anticipato per clienti e articoli. Ti consentono anche di registrare ogni pagamento per una fattura.  

## <a name="see-also"></a>Vedere anche

[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Dati finanziari](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
