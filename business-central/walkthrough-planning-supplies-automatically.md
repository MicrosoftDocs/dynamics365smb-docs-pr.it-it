---
title: Procedura dettagliata - Pianificazione automatica degli approvvigionamenti
description: In questa procedura dettagliata viene illustrato come utilizzare il sistema di pianificazione degli approvvigionamenti per pianificare automaticamente tutti gli ordini di produzione e acquisto in diversi ordini di vendita.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# <a name="walkthrough-planning-supplies-automatically"></a>Procedura dettagliata: Pianificazione automatica degli approvvigionamenti

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Espressioni come "esecuzione della pianificazione" ed "esecuzione MRP" fanno riferimento al calcolo della programmazione produzione master (MPS, Master Production Schedule) e al piano di richiesta dei materiali (MPR, Material Requirements Plan) in base alla domanda prevista ed effettiva.  

-   Per MPS si intende il calcolo di una programmazione produzione master in base alla domanda effettiva e alla previsione della domanda. Il calcolo MPS viene utilizzato per articoli finali associati a una riga ordine di vendita o previsione. Tali articoli sono denominati "articoli MPS" e sono identificati dinamicamente all'inizio del calcolo.  
-   Per MRP si intende il calcolo delle richieste di materiale in base alla domanda effettiva di componenti e alla previsione della domanda a livello di componente. La programmazione MRP viene calcolata solo per articoli diversi dagli articoli MPS. Lo scopo generale della pianificazione MRP consiste nel fornire piani formali rapportati alla scala cronologica, in base all'articolo, per fornire l'articolo corretto al momento giusto, nel luogo adatto e nella quantità appropriata.  

 Gli algoritmi di pianificazione utilizzati per MPS e MRP sono identici. Gli algoritmi di pianificazione usano il confronto. il riutilizzo di ordini di approvvigionamento esistenti e messaggi di azione. Il processo del sistema di pianificazione analizza cosa è necessario o sarà necessario (domanda) e cosa è disponibile o previsto (approvvigionamento). Quando tali quantità vengono confrontate, messaggi di azione vengono visualizzati nel prospetto di pianificazione. I messaggi di azione sono suggerimenti per creare un nuovo ordine di approvvigionamento, modificare un ordine di approvvigionamento (quantità o data) o annullarne uno esistente. Questi possono essere ordini di produzione, ordini di acquisto e ordini di trasferimento. Per ulteriori informazioni, vedere [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md).  

 Il risultato della pianificazione viene in parte calcolato sulla base della domanda e degli approvvigionamenti nel database e in parte sulla base delle schede Unità di stockkeeping o articolo, delle DB di produzione e dei cicli.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata
 In questa procedura dettagliata viene illustrato come utilizzare il sistema di pianificazione degli approvvigionamenti per pianificare automaticamente tutti gli ordini di produzione e acquisto necessari per produrre 15 biciclette da turismo richieste tramite diversi ordini di vendita. Per fornire una procedura dettagliata chiara e realistica, il numero delle righe di pianificazione viene limitato filtrando tutti gli altri set di domanda e approvvigionamento nella società demo CRONUS, ad eccezione della domanda di vendita presso l'ubicazione EST.  

 In questa procedura dettagliata sono illustrati i task seguenti:  

-   Creazione dell'ordine di vendita e calcolo di un piano di approvvigionamento completo  
-   Visualizzazione dei parametri di pianificazione e movimenti di tracciabilità ordini dietro le righe di pianificazione  
-   Creazione automatica degli ordini di approvvigionamento suggeriti  
-   Creazione di una nuova domanda di vendita e ripianificazione  

## <a name="roles"></a>Ruoli

-   Responsabile pianificazione produzione  
-   Rivenditore  

## <a name="prerequisites"></a>Prerequisiti
 Per completare questa procedura dettagliata, sarà necessario:  

-   La società demo CRONUS Italia S.p.A.  
-   Modificare vari valori di setup articolo eseguendo i passaggi nella sezione "Preparazione dei dati di esempio", più avanti in questa procedura dettagliata.  

## <a name="story"></a>Scenario
 Il cliente, Cannon Group PLC, ordina cinque biciclette da turismo con consegna il 05-02-2021 (5 febbraio).  

 Eduardo, il responsabile della pianificazione produzione, pianifica gli approvvigionamenti per la prima settimana di febbraio 2021. Prima di calcolare un piano di approvvigionamento iniziale, Eduardo filtra in base alla propria ubicazione, EST, e immette un intervallo di pianificazione compreso tra le date di lavoro 01-23-2021 e 07-02-2021.  

 L'unica domanda per quella settimana riguarda l'ordine di vendita di Cannon Group. Eduardo vede che nessuna delle righe di pianificazione contiene avvisi, quindi procede alla creazione di ordini di approvvigionamento senza modifiche per le righe di pianificazione suggerite.  

 Il giorno successivo, prima che qualsiasi ordine di approvvigionamento iniziale venga avviato o registrato, Eduardo viene avvisato che un altro cliente ha ordinato dieci biciclette da turismo da spedire il 12-02-2021. Eduardo procede alla rettifica del piano di approvvigionamento in base alla nuova domanda. Il ricalcolo restituisce un piano solo cambiamenti che suggerisce modifiche sia ai tempi sia alla quantità di alcuni degli ordini di approvvigionamento creati inizialmente.  

 Durante i vari passaggi di pianificazione, Eduardo cerca gli ordini interessati e utilizza la funzionalità Tracciabilità ordine per visualizzare le diverse domande associate ai diversi approvvigionamenti.  

## <a name="preparing-sample-data"></a>Preparazione dei dati di esempio
 Creare unità di stockkeeping (USK) per la bicicletta da turismo e una selezione dei suoi componenti, numeri di articolo compresi tra 1001 e 1300. Alcuni componenti sono esclusi per semplificare le procedure. Rettificare i parametri di pianificazione dei componenti selezionati per fornire un risultato di pianificazione più trasparente.  

### <a name="to-create-stockkeeping-units"></a>Per creare unità di stockkeeping

1.  Aprire la scheda articolo per l'articolo 1001, bicicletta da turismo.  
2.  Scegliere l'azione **Crea unità di stockkeeping**.  
3.  Nella pagina **Crea unità di stockkeeping** lasciare invariate tutte le opzioni e i filtri, quindi fare clic sul pulsante **OK**.  
4.  Ripetere i passaggi da 1 a 3 per tutti gli articoli nella numerazione compresa tra 1100 e 1300.  

### <a name="to-change-selected-planning-parameters"></a>Per variare i parametri di pianificazione selezionati

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Unità di stockkeeping**, quindi scegli il collegamento correlato.  
2.  Aprire la scheda unità di stockkeeping EST per l'articolo 1100, Ruota anteriore.  
3.  Nella Scheda dettaglio **Pianificazione** compilare i campi come indicato nella tabella seguente.  

    |Metodo di riordino|Scorta di sicurezza|Periodo di accumulo lotti|Periodo di riprogrammazione|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Lotto-per-Lotto|Vuoto|2W|2W|  

4.  Ripetere i passaggi 2 e 3 per tutte le unità di stockkeeping nella numerazione compresa tra 1100 e 1300.  

 I dati di esempio per la procedura dettagliata sono pronti.  

## <a name="creating-a-regenerative-supply-plan"></a>Creazione di un piano di approvvigionamento rigenerativo
 In seguito a un nuovo ordine di vendita per cinque biciclette da turismo, Ricardo avvia il processo di pianificazione impostando le opzioni, i filtri e pianificando l'intervallo per escludere tutte le altre domande ad eccezione della prima settimana di febbraio presso l'ubicazione EST. Ricardo inizia calcolando una programmazione produzione master (MPS), quindi elaborerà un piano di approvvigionamento completo per tutte le domande di ultimo livello (MRP).  

### <a name="to-create-the-sales-order"></a>Per creare l'ordine di vendita

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Nella pagina **Ordine vendita** compilare i campi come indicato nella tabella riportata di seguito.  

    |Vendere a - Nome cliente|Data spedizione|Nr. Articolo|Ubicazione|Quantità|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Cannon Group|02-05-2014|1001|EST|5|  

4.  Accettare l'avviso di disponibilità e scegliere **Sì** per registrare la nuova quantità di domanda.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a>Per creare un piano rigenerativo per soddisfare la domanda presso l'ubicazione EST

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto pianificazione**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Calcola piano - Rigenerativo**.  
3.  Nella pagina **Calcola piano - Pianif. magaz.** compilare i campi come indicato nella tabella seguente.  

    |Calcola piano|Data Inizio|Data fine|Mostra risultati:|Limita totali a|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Sì<br /><br /> **MRP** = No|01-23-2021<br /><br /> (data di lavoro)|02-07-2021|1001..1300|Filtro ubicazione = EST|  

4.  Scegliere **OK** per avviare l'esecuzione della pianificazione.  

     Viene creata una riga di pianificazione che suggerisce l'emissione di un ordine di produzione pianificata per produrre dieci biciclette da turismo, articolo 1001, entro il 05-02-2021, ovvero la data di spedizione dell'ordine di vendita.  

     Verificare che questa riga di pianificazione sia correlata all'ordine di vendita di Cannon Group utilizzando la funzione **Tracciabilità ordine** che collega in modo dinamico la domanda all'approvvigionamento pianificato.  

5.  Selezionare la nuova riga di pianificazione, quindi scegliere l'azione **Tracciabilità ordine**.  
6.  Nella pagina **Tracciabilità ordine** scegliere l'azione **Mostra**.  

     Viene visualizzato l'ordine di vendita per la spedizione di cinque biciclette da turismo al cliente numero 10000 il 05-02-2021.  

7.  Chiudere le pagine **Ordine vendita** e **Tracciabilità ordine**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Per calcolare MRP per includere i componenti necessari sottostanti

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto pianificazione**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Calcola piano - Rigenerativo**.  
3.  Nella pagina **Calcola piano - Pianif. magaz.** compilare i campi come indicato nella tabella seguente.  

    |Calcola|Data Inizio|Data fine|Mostra risultati:|Limita totali a:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Sì<br /><br /> **MRP** = Sì|01-23-2021|02-07-2021|1001..1300|Filtro ubicazione = EST|  

4.  Scegliere **OK** per avviare l'esecuzione della pianificazione.  

     Viene creato un totale di 14 righe di pianificazione per suggerire gli ordini di approvvigionamento per l'intera domanda rappresentata dall'ordine di vendita delle biciclette da turismo presso l'ubicazione EST.  

## <a name="analyze-the-planning-result"></a>Analisi del risultato della pianificazione
 Per analizzare le quantità suggerite, Eduardo esegue il drill-down sulle righe di pianificazione selezionate per visualizzare i parametri di pianificazione e i movimenti di tracciabilità ordine.  

 Nella pagina **Prospetto pianificazione** si noti che nella colonna **Data scadenza** gli ordini di approvvigionamento suggeriti vengono programmati dalla data di scadenza dell'ordine di vendita, 05-02-2021. La sequenza temporale inizia nella riga di pianificazione superiore con l'ordine di produzione per produrre le biciclette da turismo completate. La sequenza temporale termina nella riga di pianificazione inferiore con l'ordine di acquisto per uno degli articoli di ultimo livello, 1255, cavità posteriore, con scadenza il 30-01-2021. Come nella riga di pianificazione per l'articolo 1251, Assale posteriore, questa riga rappresenta un ordine di acquisto per i componenti in scadenza alla data di inizio dell'articolo principale prodotto, articolo di subassemblaggio 1250, che a sua volta ha come data di scadenza il 03-02-2014. Nel foglio di lavoro è possibile verificare che la data di scadenza di tutti gli articoli sottostanti è la data di inizio degli articoli padre.  

 La riga di pianificazione per l'articolo 1300, asse catena, suggerisce dieci pezzi. Questo valore si discosta dai cinque pezzi suggeriti per la maggior parte degli altri articoli nel piano. Visualizzare i movimenti di tracciabilità ordine.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Per visualizzare movimenti di tracciabilità ordine per l'articolo 1300

1.  Selezionare la riga di pianificazione per l'articolo 1300, quindi scegliere l'azione **Tracciabilità ordine**.  

     Le due righe nella pagina **Tracciabilità ordine** mostrano che cinque pezzi vengono tracciati dalla riga di pianificazione (prima riga di tracciabilità ordine) all'ordine di vendita 1001 (seconda riga di tracciabilità ordine). Gli ultimi cinque pezzi suggeriti sulla riga di pianificazione non sono correlati ad alcuna riga di documento, ma a un parametro di pianificazione, movimento previsione o movimento ordine programmato. Queste quantità non tracciate vengono sommate nel campo **Quantità non tracciata** nella testata della pagina **Tracciabilità ordine**.  

2.  Scegliere il campo **Quantità non tracciata**.  

     Nella pagina **Elementi di pianificazione non tracciati** è indicato che l'articolo 1300 utilizza un parametro di pianificazione, Quantità minima ordine, con valore 10.00. Di conseguenza, la riga di pianificazione è per dieci pezzi in totale, ma solo cinque possono essere correlati a una domanda. Gli ultimi cinque pezzi rappresentano una quantità non tracciata per soddisfare il parametro di pianificazione. Continuare per esaminare il parametro di pianificazione.  

### <a name="to-check-the-planning-parameter"></a>Per controllare il parametro di pianificazione

1.  Nella pagina **Elementi di pianificazione non tracciati** selezionare la riga di tracciabilità ordine per l'articolo 1300.  
2.  Scegliere il campo **Nr. articolo**, quindi scegliere l'azione **Avanzate**.  
3.  Nella pagina **Lista articoli** scegliere l'azione **Unità di stockkeeping**.  
4.  Nella pagina **Lista unità di stockkeeping** aprire la scheda unità di stockkeeping EST.  
5.  Nella Scheda dettaglio **Pianificazione** notare che nel campo **Quantità minima ordine** è visualizzato il valore 10.  
6.  Chiudere tutte le pagine ad eccezione della pagina **Prospetto pianificazione**.  

### <a name="to-view-more-order-tracking-entries"></a>Per visualizzare ulteriori movimenti di tracciabilità ordine

1.  Selezionare la riga di pianificazione per l'articolo 1110, Cerchione, quindi scegliere l'azione **Tracciabilità ordine**.  

     Nella pagina **Tracciabilità ordine** è indicato che sono necessari cinque cerchioni per ogni ordine di produzione per le ruote anteriori e posteriori rispettivamente.  

     La stessa tracciabilità ordine è collegata alle righe di pianificazione per gli articoli 1120, 1160 e 1170. Per l'articolo 1120, il campo **Quantità per** nella DB di produzione di ogni articolo della ruota è 50 PZ, ciò dà come risultato una quantità totale di 100.  

     La riga di pianificazione per l'articolo 1150 per sei pezzi è irregolare. Procedere con l'analisi.  

2.  Selezionare la riga di pianificazione per l'articolo 1150, quindi scegliere l'azione **Tracciabilità ordine**.  

     Nella pagina **Tracciabilità ordine** è indicato che cinque unità vengono tracciate per la ruota anteriore e un'unità non è tracciata. Visualizzare la quantità non tracciata.  

3.  Scegliere il campo **Quantità non tracciata**.  

     Nella pagina **Elementi di pianificazione non tracciati** è indicato che l'articolo 1150 utilizza un parametro di pianificazione, Molteplicità ordine, di 2,00 che specifica che l'articolo ordinato, deve essere di una quantità divisibile per 2. Il numero più vicino a 5 divisibile per 2 è 6.  

     La stessa tracciabilità ordine si applica alle righe di pianificazione per i componenti Mozzo anteriore, articoli 1151 e 1155, ad eccezione del fatto che ogni necessità viene moltiplicata per la percentuale di scarto definita per l'articolo 1150 nel campo **Percentuale scarti** nella scheda articolo.  

 L'analisi del piano di approvvigionamento iniziale è completata. Notare che la casella di controllo **Accetta messaggio azione** è selezionata in tutte le righe di pianificazione indicando che sono pronte a essere convertite in ordini di approvvigionamento.  

## <a name="carrying-out-action-messages"></a>Esecuzione di messaggi di azione
 Successivamente, Eduardo converte le righe di pianificazione suggerite in ordini di approvvigionamento mediante la funzione **Esegui messaggi di azione**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Per creare automaticamente gli ordini di approvvigionamento suggeriti

1.  Selezionare la casella di controllo **Accetta messaggio azione** in tutte le righe di pianificazione con un avviso di tipo Eccezione.  
2.  Scegliere l'azione **Esegui messaggi di azione**.  
3.  Nella pagina **Pianificaz. - Esegui mess. azione** compilare i campi come indicato nella tabella seguente.  

    |Ordine di produzione|Ordine acquisto|Ordine di trasferimento|  
    |----------------------|--------------------|--------------------|  
    |Confermato|Crea ordini acquisto|Crea ordini di trasferimento|  

4.  Scegliere **OK** per creare automaticamente tutti gli ordini di approvvigionamento suggeriti.  
5.  Chiudere la pagina **Prospetto pianificazione** vuota.  

 Il calcolo, l'analisi e la creazione iniziali di un piano di approvvigionamento per la domanda presso l'ubicazione EST nella prima settimana di febbraio sono stati completati. Nella sezione seguente un altro cliente ordina dieci biciclette da turismo ed Eduardo deve ripianificare.  

## <a name="creating-a-net-change-plan"></a>Creazione di un piano solo cambiamenti
 Il giorno successivo, prima che qualsiasi ordine di approvvigionamento venga avviato o registrato, viene ricevuto un nuovo ordine di vendita da Libros S.A. per dieci biciclette da turismo con consegna il 12-02-2021. Dopo essere stato avvisato della nuova domanda, Eduardo procede alla ripianificazione per rettificare il piano di approvvigionamento corrente. Eduardo utilizza la funzione Solo cambiamenti per calcolare solo le modifiche apportate alla domanda o all'approvvigionamento dopo l'esecuzione dell'ultima pianificazione. Inoltre, Eduardo estende il periodo di pianificazione al 14-02-2021 per includere la nuova domanda di vendita il 12-02-2014.  

 Il sistema di pianificazione calcola il modo migliore per coprire la domanda per questi due prodotti identici, ad esempio per consolidare alcuni ordini di acquisto e produzione, riprogrammare altri ordini e creare nuovi ordini in base alle esigenze.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Per creare le nuove domande di vendita e ripianificare di conseguenza

1.  Scegliere l'azione **Nuovo**.  
2.  Nella pagina **Ordine vendita** compilare i campi come indicato nella tabella riportata di seguito.  

    |Vendere a - Nome cliente|Data spedizione|Nr. Articolo|Ubicazione|Quantità|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A.|02-12-2021|1001|EST|10|  

3.  Accettare l'avviso di disponibilità e scegliere **Sì** per registrare la quantità di domanda.  
4.  Continuare la pianificazione per rettificare il piano di approvvigionamento corrente.  
5.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto pianificazione**, quindi scegli il collegamento correlato.  
6.  Scegliere l'azione **Calcola piano - Solo cambiamenti**.  
7.  Nella pagina **Calcola piano - Pianif. magaz.** compilare i campi come indicato nella tabella seguente.  

    |Calcola piano|Data Inizio|Data fine|Mostra risultati:|Limita totali a|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Sì<br /><br /> **MRP** = Sì|01-23-2021|02-14-2021|1001..1300|Filtro ubicazione = EST|  

8.  Scegliere **OK** per avviare l'esecuzione della pianificazione.  

 Viene creato un totale di 14 righe di pianificazione. Nel campo **Messaggio azione** della prima riga di pianificazione è visualizzato **Nuovo**, nel campo **Quantità** è visualizzato 10 e nel campo **Data scadenza** è visualizzato 12-02-21. Questa nuova riga per l'articolo padre principale, 1001, Bicicletta da turismo, viene creata perché l'elemento utilizza il metodo di riordino **Ordine**, il che significa che deve essere fornito in una relazione uno-a-uno con la relativa domanda, l'ordine di vendita di dieci pezzi.  

 Le due righe di pianificazione successive sono gli ordini di produzione per le ruote delle biciclette. Ogni ordine esistente di cinque, nel campo **Quantità in origine**, viene aumentato a 15, nel campo **Quantità**. Entrambi gli ordini di produzione presentano date di scadenza invariate, come indicato nel campo **Messaggio azione** contenente **Modifica qtà**. Ciò accade anche per la riga di pianificazione per l'articolo 1300, ad eccezione del fatto che la relativa molteplicità ordine pari a 10,00 arrotonda a 20 pezzi la domanda tracciata per 15.  

 Tutte le altre righe di pianificazione presentano il messaggio di azione **Riprogr. e mod. qtà**. Ciò significa che oltre all'aumento della quantità, le date di scadenza vengono spostate in relazione al primo piano di approvvigionamento per includere la quantità supplementare nel periodo di produzione disponibile (capacità). I componenti acquistati vengono nuovamente pianificati e aumentati per fornire gli ordini di produzione. Continuare per analizzare il nuovo piano.  

## <a name="analyze-the-changed-planning-result"></a>Analisi del risultato della pianificazione modificata
 Poiché tutti gli articoli lotto-per-lotto pianificati nel filtro, da 1100 a 1300, hanno un periodo di riprogrammazione di due settimane, i relativi ordini di approvvigionamento esistenti sono stati tutti modificati per soddisfare la nuova domanda, che viene eseguita entro le due settimane specificate.  

 Più righe di pianificazione vengono semplicemente moltiplicate per tre per fornire 15 biciclette da turismo anziché 5 e le date di scadenza vengono spostate a una data precedente per fornire le quantità modificate entro la data di spedizione dell'ordine di vendita a Cannon Group. Per queste righe di pianificazione, è possibile tenere traccia di tutte le quantità. Le righe di pianificazione restanti sono aumentate di dieci pezzi e vengono spostate le date di scadenza. Per le righe di pianificazione, una parte della quantità non è tracciata a causa dei parametri di pianificazione. Visualizzare alcuni dei movimenti di tracciabilità ordine.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Per visualizzare movimenti di tracciabilità ordine per l'articolo 1250

1.  Selezionare la riga di pianificazione per l'articolo 1250, quindi scegliere l'azione **Tracciabilità ordine**.  

     Nelle sette righe della pagina **Tracciabilità ordine** viene indicato che cinque e dieci pezzi vengono tracciati dalla ruota posteriore alle biciclette da turismo sui due ordini di vendita rispettivamente.  

     Gli ultimi cinque pezzi non vengono tracciati. Procedere con l'analisi.  

2.  Scegliere il campo **Quantità non tracciata**.  

     Nella pagina **Elementi di pianificazione non tracciati** è indicato che l'articolo 1250 utilizza un parametro di pianificazione, Molteplicità ordine, di 10,00. Di conseguenza, la riga di pianificazione è per 20 pezzi in totale per arrotondare l'effettiva necessità al numero più vicino divisibile per 10. Gli ultimi cinque pezzi rappresentano una quantità non tracciata per soddisfare il parametro di pianificazione.  

3.  Chiudere tutte le pagine ad eccezione della pagina **Prospetto pianificazione**.  

### <a name="to-view-an-existing-order"></a>Per visualizzare un ordine esistente

1.  Nella riga di pianificazione per l'articolo 1250, fare clic sul campo **Nr. ordine rif.**.    
2.  Nella pagina **Ord. produzione confermato** per il mozzo posteriore. Verrà visualizzato l'ordine esistente per dieci pezzi creati nella prima esecuzione della pianificazione.  
3.  Chiudere l'ordine di produzione pianificato confermato.  

 Viene completata la procedura dettagliata relativa all'utilizzo del sistema di pianificazione per il rilevamento automatico della domanda, il calcolo degli ordini di approvvigionamento appropriati alla domanda, ai parametri di pianificazione e alla creazione automatica dei diversi tipi di ordini di approvvigionamento con le quantità e le date appropriate.  

## <a name="see-also"></a>Vedere anche
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)    -->
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
