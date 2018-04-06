---
title: 'Procedura dettagliata: Gestione dei progetti con le commesse | Documenti Microsoft'
description: "In questa procedura dettagliata vengono presentate le funzionalità di gestione dei progetti nelle commesse. Le commesse consentono di pianificare l'impiego delle risorse dell'azienda e di tenere traccia dei vari costi connessi all'impiego delle risorse in un progetto specifico. Le commesse implicano il consumo di ore di lavoro del personale, di ore macchina, degli articoli a magazzino e altri consumi che vanno monitorati man mano che la commessa progredisce."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2df47e6f5bcd7b02282e45757d94bd6fc0f0981d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-managing-projects-with-jobs"></a>Procedura dettagliata: Gestione dei progetti con le commesse
In questa procedura dettagliata vengono presentate le funzionalità di gestione dei progetti nelle commesse. Le commesse consentono di pianificare l'impiego delle risorse dell'azienda e di tenere traccia dei vari costi connessi all'impiego delle risorse in un progetto specifico. Le commesse implicano il consumo di ore di lavoro del personale, di ore macchina, degli articoli a magazzino e altri consumi che vanno monitorati man mano che la commessa progredisce.  

 Nella procedura è illustrata l'impostazione di una nuova commessa oltre ad alcune attività comuni, come la gestione dei prezzi fissi, i pagamenti rateali, la registrazione di fatture relative alle commesse e la copia di commesse.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
 In questa procedura dettagliata sono illustrati i task seguenti:  

### <a name="setting-up-a-job"></a>Impostazione di una commessa  
 Con l'impostazione della struttura del budget per le commesse, creare una commessa è semplice. Questa procedura dettagliata copre le procedure riportate di seguito:  

-   Impostazione di righe di task della commessa e di pianificazione.  
-   Creazione di prezzi specifici della commessa per articoli, risorse e conti di contabilità generale.  
-   Fatturazione da una commessa  

### <a name="handling-fixed-prices"></a>Gestione dei prezzi fissi  
 Nelle commesse è possibile gestire i prezzi fissi e i prezzi per i servizi o i beni concordati in anticipo con i clienti. In questa procedura dettagliata è possibile effettuare quanto segue:  

-   Come si determinano i valori di contratto e della fattura  
-   Come ammettere nella pianificazione lavoro extra non fatturato  

### <a name="copying-a-job"></a>Copia di una commessa  
 Questa parte della procedura dettagliata si incentra sulla copia, parziale o totale, di una commessa al fine di ridurre l'immissione manuale di dati e garantire maggior accuratezza. È incluso quanto segue:  

-   Copia di parte di una commessa a una nuova commessa  
-   Copia di prezzi specifici di una commessa  
-   Copia di righe di pianificazione  

### <a name="making-payment-by-installment"></a>Pagamenti rateali  
 Nel caso di progetti di grande respiro, costosi e che si protraggono per lunghi periodi, il cliente spesso concorda con il fornitore un pagamento rateale. Questo scenario tratta dell'impostazione di questi pagamenti:  

-   Creazione di un pagamento rateale per una commessa  
-   Fatturazione dei pagamenti ai clienti  
-   Contabilizzazione dell'utilizzo in una commessa con pagamento rateale  

## <a name="roles"></a>Ruoli  
 Questa procedura dettagliata include task per i seguenti ruoli:  

-   Manager progetto  
-   Membro del team di progetto  

## <a name="prerequisites"></a>Prerequisiti  
 Prima di svolgere le attività di questa procedura dettagliata, è necessario:  

-   Installare il database demo di CRONUS International Ltd.
-   Creare dati di esempio seguendo la procedura descritta nella sezione seguente.  

## <a name="story"></a>Scenario  
Questa procedura dettagliata è incentrata su CRONUS International Ltd., una società che si occupa di progettazione, consulenza e installazione di nuove infrastrutture, ad esempio aule conferenze e uffici, complete di mobilia e accessori. La maggior parte del lavoro è svolta in base a progetti. Ezio Alboni è un manager di progetto in CRONUS. Utilizza le commesse per avere una panoramica di ciascuna commessa in corso avviata da CRONUS, nonché delle commesse completate. Solitamente è la persona che definisce gli affari con i clienti e inserisce i dettagli di base della commessa, cioè righe di task e di pianificazione e prezzi, in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Trova che creare, gestire e analizzare i dati sia semplice. Alboni inoltre apprezza il modo in cui [!INCLUDE[d365fin](includes/d365fin_md.md)] consente la copia delle commesse e i pagamenti rateali.

 Cinzia Di Marco fa parte del team alle dirette dipendenze di Alboni ed è responsabile del monitoraggio quotidiano della commessa. Immettere il proprio lavoro oltre al lavoro eseguito dai tecnici in ogni task. Registra gli articoli che sono stati utilizzati e altri costi sostenuti.  

## <a name="preparing-sample-data"></a>Preparazione dei dati di esempio  
 Per preparare questa procedura dettagliata, è necessario aggiungere Cinzia come nuova risorsa.  

### <a name="to-prepare-the-sample-data"></a>Per preparare i dati di esempio  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Risorse**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo** per creare una nuova scheda risorsa.  
3.  Nella Scheda dettaglio **Generale** immettere le seguenti informazioni:  

    - **Nr.**: **Di Marco**  
    - **Nome**: **Di Marco**  
    - **Tipo**: **Persona**  

4.  Scegliere il campo **Unità di misura base** e scegliere l'azione **Nuovo** per aprire la finestra **Unità di misura risorse**. Nel campo **Codice** selezionare **Ora**. Scegliere il pulsante **OK**.  
5.  Nella Scheda dettaglio **Fatturazione** inserire i seguenti dati:  

    -   **Costo unitario diretto**: **5**  
    -   **% costi indiretti**: **4**  
    -   **Costo unitario**: **10**  
    -   **Cat. reg. articolo/servizio**: **Servizi**  
    -   **Cat. reg. art./serv. IVA**: **IVA 25**  

6.  Scegliere il pulsante **OK** per salvare le modifiche.  

 Nella procedura descritta di seguito si crea un batch registrazioni commesse perché Cinzia possa registrare il relativo utilizzo.  

### <a name="to-create-a-job-journal-batch"></a>Per creare un batch registrazioni commesse  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Registrazioni commesse** scegliere il campo **Nome batch**. Viene visualizzata la finestra **Batch registrazioni commesse**.  
3.  Scegliere l'azione **Nuovo** per creare una nuova riga con le informazioni seguenti:  

    -   **Nome**: **Di Marco**  
    -   **Descrizione**: **Di Marco**  
    -   **Nr. serie**: **REGCOMM**  

4.  Fare clic sul pulsante **OK** per chiudere tutte le finestre aperte.  

## <a name="setting-up-a-job"></a>Impostazione di una commessa  
 In questo scenario, CRONUS si è aggiudicata un appalto dal cliente Progressive Home Furnishings per la progettazione di un'aula conferenze e di rappresentanza. Il cliente ha sede negli Stati Uniti e il progetto richiede software particolare. Il manager di progetto raggiunge un accordo con il cliente e crea una commessa per il contratto.  

### <a name="to-set-up-a-job"></a>Per impostare una commessa  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo** per creare una nuova scheda.  
3.  Nella Scheda dettaglio **Generale** immettere le seguenti informazioni:  

    -   **Descrizione**: **Consulenza per progettazione aula conferenze**  
    -   **Fatturare a - Nr. cli.**: **01445544**  

4.  Nella Scheda dettaglio **Registrazione** inserire i seguenti dati:  

    -   **Stato**: **Ordine**  
    -   **Cat. reg. commessa**: **Pianifica**  
    -   **Metodo WIP**: **Valore costo**  

5.  Nella Scheda dettaglio **Durata** immettere la data odierna nei campi **Data inizio** e **Data fine**. Queste date agevolano l'applicazione delle conversioni di valuta al momento della fatturazione della commessa.  
6.  Nella Scheda dettaglio **Commercio estero** impostare il codice di valuta su **USD**. Se si seleziona USD nel campo **Codice valuta fattura**, la commessa sarà fatturata in dollari statunitensi e pianificata solo nella valuta locale di CRONUS.  

 È possibile personalizzare il prezzo per i clienti in base alla commessa, in base ai contratti impostati. Nella procedura descritta di seguito, il manager progetto specifica un costo per il tempo di Cinzia, imposta il prezzo per il software necessario e aggiunge i costi di viaggio che il cliente ha accettato di pagare.  

### <a name="to-customize-pricing"></a>Per personalizzare il prezzo  

1.  Nella scheda commessa, scegliere l'azione **Risorsa**.  
2.  Nella finestra **Prezzi risorse commesse**, immettere le seguenti informazioni:  

    -   **Codice**: **Di Marco**  
    -   **Prezzo unitario**: **20**  

3.  Scegliere il pulsante **OK** per chiudere la finestra.  
4.  Scegliere l'azione **Articolo**.  
5.  Nella finestra **Prezzi articoli commesse**, immettere le seguenti informazioni e il prezzo personalizzato:  

    1.  **Nr. articolo**: **80201 (Progr.grafica)**  
    2.  **Prezzo unitario**: **200**  

6.  Scegliere il pulsante **OK** per chiudere la finestra.  
7.  Scegliere l'azione **Conto C/G**.  
8.  Nella finestra **Prezzi conti C/G commesse** , immettere le seguenti informazioni e i costi di viaggio, per i quali il cliente si impegna per pagare il costo più 25%:  

    1.  **Conto C/G**: **8430 (Spese per viaggi e trasferte)**  
    2.  **Fattore costo unitario**: **1,25**  

9. Scegliere il pulsante **OK** per chiudere la finestra.  

 I passaggi finali del setup della commessa sono l'aggiunta dei task commessa e delle righe di pianificazione che fanno parte di ogni task. Le righe di pianificazione determinano ciò che viene fatturato al cliente.  

### <a name="to-add-job-tasks"></a>Per aggiungere task commessa  

1.  Nella scheda **Commessa** per la nuova commessa, scegliere l'azione **Righe task commessa**.  
2.  Nella seguente tabella vengono illustrate le informazioni che è necessario immettere nei campi.  

    |Nr. task commessa|Description|Tipo task commessa|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Consulenza per progettazione aula conferenze|Inizio-Totale|  
    |1010|Incontro di consultazione con cliente|Analitico|  
    |1020|Sviluppo|Analitico|  
    |1090|Totale consulenza|Fine-Totale|  

3.  Per indicare che alcuni task sono sottocategorie di altri task, nella scheda **Azioni** , nel gruppo **Funzioni** , selezionare **Indentazione task commesse**.  

 Una riga di pianificazione può essere di uno dei seguenti tipi:  

-   **Programmazione**: aggiunto alla pianificazione ma non fatturato.  
-   **Contratto**: fatturato ma non aggiunto alla pianificazione.  
-   **Programmazione e contratto**: fatturato e aggiunto alla pianificazione.  

 In questa procedura dettagliata, il manager progetto utilizza **Programmazione e contratto**. Crea tre righe di pianificazione per il task 1010 e due righe di pianificazione per il task 1020.  

### <a name="to-create-planning-lines"></a>Per creare righe di pianificazione  

1.  Selezionare la riga 1010, quindi scegliere l'azione **Righe pianificazione commessa**. Inserire i seguenti dati:  

     **Riga 1**  

    -   **Tipo riga**: **Programmazione e contratto**  
    -   **Data pianificazione**: **(data odierna)**  
    -   **Tipo**: **Risorsa**  
    -   **Nr.**: **Di Marco**  
    -   **Quantità**: **40**  

     **Riga 2**  

    -   **Tipo riga**: **Programmazione e contratto**  
    -   **Data pianificazione**: **(data odierna)**  
    -   **Tipo**: **Risorsa**  
    -   **Nr.**: **Maldonado**  
    -   **Quantità**: **40**  

     **Riga 3**  

    -   **Tipo riga**: **Programmazione e contratto**  
    -   **Data pianificazione**: **(data odierna)**  
    -   **Tipo**: **Conto C/G**  
    -   **Nr.**: **8430 (spese per viaggi e trasferte)**  
    -   **Quantità**: **2**  
    -   **Costo unitario**: **400**  

2.  Scegliere il pulsante **OK** per chiudere la finestra. I totali vengono aggiornati nella finestra **Righe task commessa** .  
3.  Selezionare la riga 1020, quindi scegliere l'azione **Righe pianificazione commessa**. Inserire i seguenti dati:  

     **Riga 1**  

    -   **Tipo riga**: **Programmazione e contratto**  
    -   **Data pianificazione**: **(data odierna)**  
    -   **Tipo**: **Risorsa**  
    -   **Nr.**: **Di Marco**  
    -   **Quantità**: **80**  

     **Riga 2**  

    -   **Tipo riga**: **Programmazione e contratto**  
    -   **Data pianificazione**: **(data odierna)**  
    -   **Tipo**: **Articolo**  
    -   **Nr.**: **80201 (Progr.grafica)**  
    -   **Quantità**: **1**  

4.  Scegliere il pulsante **OK** per chiudere la finestra. I totali vengono aggiornati nella finestra **Righe task commessa** .  

## <a name="calculating-remaining-usage"></a>Calcolo dell'utilizzo residuo  
 Cinzia, il membro del team, lavora alla commessa da qualche tempo e desidera registrare le sue ore e l'utilizzo nella commessa. Non ha lavorato più ore di quanto concordato in origine con il cliente. Utilizza il processo batch **Calc. utilizzo residuo** per calcolare l'utilizzo residuo della commessa in una registrazione di commessa. Per ciascun task viene calcolata la differenza tra l'utilizzo programmato di articoli, risorse e spese di contabilità generale e l'utilizzo effettivo registrato nei movimenti contabili delle commesse. L'utilizzo residuo viene quindi visualizzato nelle registrazioni delle commesse, da cui è possibile eseguirne la registrazione.  

### <a name="to-calculate-remaining-usage"></a>Per calcolare l'utilizzo residuo  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Registrazioni commesse**, nel campo **Nome batch**, aprire la lista **Batch registrazioni commesse**. Selezionare il batch registrazioni commesse di **Cinzia** .  
3.  Scegliere l'azione **Calc. utilizzo residuo**.  
4.  Nella finestra **Commessa - Calc. utilizzo residuo**, nella Scheda dettaglio **Task commessa**, selezionare il campo **Nr. commessa** e selezionare il numero della commessa appropriata, in genere il processo J00010.  
5.  Nella Scheda dettaglio **Opzioni**, digitare **J00001** nel campo **Nr. documento**. Ciò facilita il futuro monitoraggio della registrazione.  
6.  Immettere la data corrente come data di registrazione.  
7.  Scegliere il pulsante **OK**. Verranno generate le righe delle registrazioni delle commesse derivanti dalle righe di pianificazione create dal manager progetto per la commessa.  
8.  Nella finestra di conferma scegliere il pulsante **OK**. Le righe generate vengono aggiunte nelle registrazioni commesse.  
9. Accertarsi che tutti i numeri di documento siano J00001, quindi scegliere l'azione **Registra**. Selezionare **Sì** per confermare la registrazione.  
10. Le righe sono così registrate. Scegliere il pulsante **OK** per chiudere le finestre.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Creazione e registrazione di una fattura di vendita per una commessa  
 Quindi, Cinzia può creare una nuova fattura per l'intera commessa o per parte di una commessa. È anche possibile allegare la fattura a un'altra fattura per lo stesso cliente e per la stessa commessa. In questo caso, può procedere a fatturare l'intera commessa, poiché il progetto è completato.  

### <a name="to-create-a-job-sales-invoice"></a>Per creare una fattura di vendita per una commessa  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2.  Selezionare la commessa creata in precedenza, quindi scegliere l'azione **Crea fattura vendita per commessa**.  
3.  Nella Scheda dettaglio **Task commessa**, cancellare i filtri in **Nr. task commessa** per fatturare la commessa. Nel campo **Nr. commessa** selezionare la commessa appropriata.  
4.  Nella Scheda dettaglio **Opzioni** immettere la data di registrazione e specificare se creare una fattura per task oppure una singola fattura per tutti i task.  
5.  Selezionare il pulsante **OK** per creare la fattura e fare clic sul pulsante **OK** nella finestra di conferma.  

 Dopo che Cinzia ha creato la fattura, può accedervi da **Vendite e marketing** sotto **Gestione ordini** per ulteriori elaborazioni.  

### <a name="to-post-a-new-sales-invoice"></a>Per registrare una nuova fattura di vendita  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Fatture vendite**, quindi scegliere il collegamento correlato.  
2.  Aprire la fattura per il cliente numero 01445544. Sono visibili le informazioni inserite dalle righe di pianificazione.  
3.  Scegliere l'azione **Registra**. Selezionare **Sì** per confermare la registrazione.  

### <a name="to-view-the-posted-invoice"></a>Per visualizzare la fattura registrata  

1.  Aprire la commessa, quindi scegliere l'azione **Righe pianificazione commessa**.  
2.  Selezionare una qualsiasi delle righe di pianificazione fatturate, quindi scegliere l'azione **Ottieni nota credito/fattura vendita**.
3. Nella finestra **Fatture commessa** scegliere l'azione **Apri fattura/nota credito vendita**.  

 Informazioni sulla specifica commessa, come prezzi, costi o margini, sono ora reperibili mediante la finestra **Statistiche**.  

### <a name="to-open-the-statistics-window"></a>Per aprire la finestra Statistiche  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Statistiche**. È possibile esaminare informazioni dettagliate su prezzi, costi e margini delle commesse sia in valuta locale che estera.  
3.  Scegliere il pulsante **Chiudi** per chiudere la finestra **Statistiche commessa**.  

## <a name="handling-fixed-prices"></a>Gestione dei prezzi fissi  
 CRONUS ha ottenuto un contratto per l'allestimento di alcune aule per conferenze. Come manager del progetto, Alboni vuole una panoramica precisa dei task necessari per la commessa con i costi previsti e sostenuti associati per ciascun task. Inoltre, desidera conoscere il prezzo totale a contratto della commessa e l'importo fatturato finora. Ha concluso un contratto con il cliente in cui sono stati concordati prezzi fissi per la commessa.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Per gestire i prezzi fissi nelle commesse  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2.  Selezionare il numero di commessa **Società mercantile internaz.**, quindi scegliere l'azione **Righe task commessa**.  
3.  Selezionare la riga 1120 e nel campo **Programmazione (costo totale)** fare clic con il pulsante destro del mouse sull'importo e scegliere **DrillDown**.  

     Verificando le righe di pianificazione commessa, Alboni stabilisce che avrà anche bisogno di Cinzia per 30 ore per questa fase del progetto. Concorda un prezzo fisso con il cliente.  

4.  Nella finestra **Righe task commessa**, selezionare la riga 1120, quindi scegliere l'azione **Righe pianificazione commessa**.  
5.  Scegliere l'azione **Nuovo** per creare una nuova riga con le informazioni seguenti:  

    -   **Tipo riga**: **Programmazione e contratto**  
    -   **Tipo**: **Risorsa**  
    -   **Nr.**: **Di Marco**  
    -   **Quantità**: **30**  

7.  Scegliere il pulsante **OK** per chiudere la finestra.  
8.  Nel campo **Programmazione (costo totale)** , fare clic con il pulsante destro del mouse sul campo e selezionare **DrillDown** nella finestra **Righe task commessa** . Visualizzare le modifiche alla pianificazione. Le 30 ore sono state aggiunte alla pianificazione.  
9. Scegliere il pulsante **OK** per chiudere le finestre.  

 Dopo che Cinzia è stata aggiunta alla pianificazione per questa riga di task, lavora per 25 ore alla commessa. Immette le ore nelle registrazioni commesse.  

### <a name="to-enter-hours-in-the-job-journal"></a>Per inserire ore nelle Registrazioni commesse  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.  
2.  In una nuova riga inserire i seguenti dati:  

    -   **Tipo riga**: **(vuoto)**  
    -   **Data di registrazione**: **(data odierna)**  
    -   **Nr. documento**: **J00002**  
    -   **Nr. commessa**: **Società mercantile internaz.**  
    -   **Nr. task commessa**: **1120**  
    -   **Tipo**: **Risorsa**  
    -   **Nr.**: **Di Marco**  
    -   **Quantità**: **25**  

3.  Scegliere l'azione **Registra**.  

     Alcuni giorni più tardi, Cinzia lavora per altre 10 ore alla commessa. Ha lavorato 35 ore in tutto. Poiché il contratto è per 30 ore, solo cinque delle ore verranno addebitate al cliente. Cinzia aggiungerà manualmente le cinque ore aggiuntive lavorate alla pianificazione.  

4.  Nella finestra **Registrazioni commesse**, scegliere l'azione **Calc. utilizzo residuo**.  
5.  Nella Scheda dettaglio **Opzioni** della finestra **Commessa - Calc. utilizzo residuo** inserire le seguenti informazioni:  

    -   **Nr. documento**: **J00003**  
    -   **Data di registrazione**: **(data odierna)**  

6.  Nella Scheda dettaglio **Task commessa** inserire le seguenti informazioni:  

    -   **Nr. commessa**: **Società mercantile internaz.**  
    -   **Nr. task commessa**: **1120**  

     Per eseguire il calcolo, fare clic sul pulsante **OK**. Ci sono cinque ore di lavoro residuo per Cinzia. Il campo **Tipo riga** è vuoto, il che indica che solo l'utilizzo deve essere ancora registrato perché il lavoro è già stato pianificato.  

7.  Nella finestra **Registrazioni commesse**, creare una nuova riga con i seguenti dati. Accertarsi che entrambi i numeri di commessa siano consecutivi a quelli già usati:  

    -   **Tipo riga**: **Programmazione**  
    -   **Nr. commessa**: **Società mercantile internaz.**  
    -   **Nr. task commessa**: **1120**  
    -   **Tipo**: **Risorsa**  
    -   **Nr.**: **Di Marco**  
    -   **Quantità**: **5**  

     Utilizzando il tipo di riga **Programmazione**, vengono aggiornati i prezzi e i costi pianificati, mentre non vengono aggiornati i costi e prezzi di contratto che sono fatturati al cliente.  

8.  Scegliere l'azione **Registra**. Scegliere il pulsante **OK** per chiudere la finestra.  
9. Aprire l'elenco **Commesse**.  
10. Selezionare la commessa SOC. MERC, quindi scegliere l'azione **Righe task commessa**.  
11. Selezionare la riga 1120 e fare clic con il pulsante destro del mouse sull'importo del campo **Programmazione (costo totale)**. Selezionare **Drilldown** per visualizzare le informazioni.  

     Le modifiche sono inserite automatiche nella riga per il Nr. task commessa 1120. Nel costo totale del lavoro pianificato, cinque ore in più di lavoro di Cinzia sono state aggiunte alla programmazione.  

12. Scegliere il pulsante **Chiudi** per chiudere la finestra.  
13. Fare clic con il pulsante destro del mouse sull'importo del campo **Contratto (costo totale)** e selezionare **Drilldown** per visualizzare le informazioni.  

     Nel prezzo totale del contratto sono incluse solo le 30 ore pattuite in origine con il cliente.  

## <a name="copying-jobs"></a>Copia di commesse  
 Alboni ha concluso un contratto con un cliente, Grafiche Magiche 2000, per l'allestimento di dieci aule per conferenze. Il contratto è simile a una commessa precedente. Di conseguenza, si risparmierà tempo copiando tale commessa precedente.  

 Nella finestra **Copia commessa** è possibile selezionare la commessa e le righe di task che si desidera copiare. È anche possibile copiare i movimenti contabili o le righe di pianificazione della commessa di origine; nel primo caso vengono create righe di pianificazione basate sull'utilizzo effettivo, nel secondo vengono copiate nella nuova commessa le righe di pianificazione originali. Si potrà quindi scegliere quale tipo di riga di pianificazione o di movimento contabile includere, selezionando solo quelle applicabili alla nuova commessa. Infine, si potrà decidere se copiare anche prezzi e quantità dalla commessa selezionata.  

### <a name="to-copy-a-job"></a>Per copiare una commessa  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo** per creare una nuova commessa. Inserire i seguenti dati:  

    -   **Descrizione**: **Pianificazione di dieci aule per conferenze**  
    -   **Fatturare a - Nr. cli.**: **20000**  

3.  Scegliere l'azione **Copia task commessa da**.  
4.  Nella finestra **Copia task commessa** , immettere le seguenti informazioni:  

    -   **Nr. commessa**: **Società mercantile internaz.**  
    -   **Nr. task commessa - Da**: **1000**  
    -   **Origine**: **Righe pianificazione commessa**  
    -   **Incl. tipo riga pianificazione**: **Programmazione e contratto**  
    -   **Nr. task commessa - A**: **Guildford Pianificazione 10 aule per conferenze**  
    -   Selezionare i campi **Copia dimensioni** e **Copia quantità**.  

5.  Selezionare il pulsante **OK** per copiare la commessa e fare clic sul pulsante **OK** per chiudere la finestra di conferma.  

     Confrontando prezzi, righe task commessa e righe di pianificazione per le due commesse, è possibile verificare che le informazioni sono state copiate correttamente.  

## <a name="making-payments-by-installments"></a>Pagamenti rateali  
 CRONUS si è appena aggiudicata un grande progetto il cui completamento richiederà un anno. Poiché impegna molte risorse, il manager di progetto imposta il contratto per il pagamento anticipato da parte del cliente di parte del prezzo a metà del progetto e il saldo al completamento del progetto.  

### <a name="to-set-up-a-new-account"></a>Per impostare un nuovo conto  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Piano dei conti** scegliere l'azione **Nuovo** per creare una nuova scheda.  
3.  Nella scheda del nuovo **Conto C/G** inserire i seguenti dati:  

    -   **Nr.**: **6630**  
    -   **Nome**: **Pagamento commessa**  

4.  Nel campo **Cat. reg. articolo/servizio** della Scheda dettaglio **Registrazione** selezionare **VARIE**. Scegliere il pulsante **OK** per chiudere la finestra.  
5.  Nella finestra **Piano dei conti**, selezionare **Nr. 6630 Pagamento commessa**, quindi scegliere **Indenta piano dei conti**. Scegliere **Sì** per confermare.  

 Le procedure riportate di seguito mostrano come creare una nuova commessa, impostare il prezzo e il pagamento rateale. Nelle righe di task della commessa è possibile creare righe specifiche dedicate al pagamento rateale. Tutto il lavoro completato per la commessa che viene aggiunto alla pianificazione sarà inserito nelle righe di utilizzo. Per ogni riga di task pagamento nelle righe di pianificazione, il tipo di riga è Contratto, che significa che sarà emessa fattura al cliente. Immettere una nuova riga per il primo acconto. Nella riga di task utilizzo, inserire i dati relativi agli articoli e alle risorse che sono stati utilizzati nel progetto; ciò incrementa la pianificazione in termini di ore dei dipendenti e di articoli impiegati nella commessa.  

### <a name="to-make-a-payment-by-installment"></a>Per effettuare un pagamento rateale  

1.  Creare una nuova commessa.  
2.  Nella nuova scheda **Commessa** inserire i seguenti dati:  

    -   **Descrizione**: **Ridecorazione dell'area reception**  
    -   **Fatturare a - Nr. cli.**: **30000**  
    -   **Cat. reg. commessa**: **Pianifica**  
    -   **Metodo WIP**: **Valore costo**  

3.  Nella scheda commessa, scegliere l'azione **Risorsa**. Inserire i seguenti dati:  

    -   **Codice**: **Di Marco**  
    -   **Prezzo unitario**: **10**  

     Scegliere il pulsante **OK** per chiudere la finestra.  

4.  Nella scheda **Commessa**, scegliere l'azione **Righe task commessa**.  

     Nella seguente tabella vengono illustrate le righe che verranno create.  

    |Riga|Nr. task commessa|Description|Tipo task commessa|  
    |----------|------------------|---------------------------------------|-------------------|  
    |1|1000|Pagamento - primo acconto|Registrazione|  
    |2|2000|Utilizzo|Analitico|  
    |3|3000|Pagamento - secondo acconto|Analitico|  
    |4|4000|Pagamento - saldo|Registrazione|  

5.  Nella finestra **Righe task commessa**, selezionare il task 1000, quindi scegliere l'azione **Righe pianificazione commessa**.  
6.  Creare una riga di pianificazione con i seguenti dati:  

    -   **Tipo riga**: **Contratto**  
    -   **Data pianificazione**: **(data odierna)**  
    -   **Tipo**: **Conto C/G**  
    -   **Nr.**: **6630**  
    -   **Quantità**: **1**  
    -   **Prezzo unitario**: **5000**  

     Scegliere il pulsante **OK** per chiudere la finestra.  

7.  Nella finestra **Righe task commessa** selezionare il **task 2000** e aprirne le **Righe pianificazione commessa**.  

     Nella seguente tabella vengono illustrate le righe di pianificazione che verranno create.  

    |Linee|Tipo riga|Data pianificazione|Tipo|Nr.|Quantità|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Programmazione|(data odierna)|Risorsa|Cinzia|120|  
    |2|Programmazione|(data odierna)|Articolo|70104|10|  

     Scegliere il pulsante **OK** per chiudere la finestra. Nella finestra **Righe task commessa** è possibile visualizzare gli importi di programmazione aggiornati.  

8.  Nella finestra **Righe task commessa** selezionare il **task 3000**.  
9. Creare una riga di pianificazione con i seguenti dati:  

    -   **Tipo riga**: **Contratto**  
    -   **Data pianificazione**: **una data futura**  
    -   **Tipo**: **Conto C/G**  
    -   **Nr.**: **6630**  
    -   **Quantità**: **1**  
    -   **Prezzo unitario**: **5000**  

     Scegliere il pulsante **OK** per chiudere la finestra.  

10. Creare una simile movimento della riga di pianificazione per il task commessa 4000.  

 Ora che le righe di task e di pianificazione sono state registrate, Alboni crea una fattura per il primo pagamento. Procede dalle righe dei task commesse per assicurarsi che la fattura contenga solo le righe del primo pagamento. Aprire l'ordine di vendita dalle righe di pianificazione o dalle righe di task.  

### <a name="to-create-an-invoice"></a>Per creare una fattura  

1.  Nella finestra **Righe task commessa**, selezionare la riga 1000, quindi scegliere l'azione **Crea fattura di vendita**.  
2.  Nella finestra **Crea fattura di vendita** , impostare la data odierna come data di registrazione, specificare **Per task** e fare clic sul pulsante **OK** per creare una fattura con i dati di default. Fare clic sul pulsante **OK** per chiudere la finestra di conferma.  
3.  Scegliere l'azione **Ottieni nota credito/fattura vendita**. Nella fattura di vendita è possibile visualizzare che nella fattura è incluso solo il primo acconto. È ora possibile inviarla al cliente come concordato.  

## <a name="next-steps"></a>Passaggi successivi  
 In questa procedura dettagliata sono state riprodotte alcune delle operazioni di base relative alla gestione delle commesse in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si è appreso come creare una nuova commessa, come copiare una commessa e come gestire i pagamenti. Inoltre, è stato illustrato come tenere traccia delle ore e creare le fatture.  

## <a name="see-also"></a>Vedi anche  
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)   
 [Impostazione della Gestione progetti](projects-setup-projects.md)   
 [Utilizzare le risorse](projects-how-use-resources.md)   
 [Monitoraggio di progressi e performance](projects-how-monitor-progress-performance.md)   
 [Fatturazione di commesse](projects-how-invoice-jobs.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

