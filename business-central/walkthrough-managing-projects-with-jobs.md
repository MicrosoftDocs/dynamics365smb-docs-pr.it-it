---
title: 'Procedura dettagliata: gestione di progetti con progetti'
description: Questa procedura dettagliata ti introduce alle funzionalità di gestione dei progetti che ti consentono di pianificare l'utilizzo delle risorse della tua azienda.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-managing-projects"></a>Procedura dettagliata: gestione dei progetti

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In questa procedura dettagliata vengono presentate le funzionalità di gestione dei progetti. I progetti consentono di pianificare l'impiego delle risorse dell'azienda e di tenere traccia dei vari costi connessi all'impiego delle risorse in un progetto specifico. I progetti implicano il consumo di ore di lavoro del personale, di ore macchina, degli articoli a magazzino e altri consumi che vanno monitorati man mano che il progetto progredisce.  

Questa procedura dettagliata copre la configurazione di un nuovo progetto e le attività correlate:

- Gestire i prezzi fissi
- Effettuare pagamenti rateali
- Registrare fatture da progetti
- Copiare progetti

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata

 In questa procedura dettagliata sono illustrati le seguenti attività:  

### <a name="setting-up-a-project"></a>Impostazione di un progetto

Con l'impostazione della struttura del budget per i progetti, creare un progetto è semplice. Questa procedura dettagliata copre le procedure riportate di seguito:  

- Impostare righe di attività di progetto e righe di pianificazione.  
- Creazione di prezzi specifici del progetto per articoli, risorse e conti di contabilità generale.  
- Fatturare ai clienti per un progetto  

### <a name="handling-fixed-prices"></a>Gestione dei prezzi fissi

 È possibile gestire i prezzi fissi e i prezzi per servizi o beni concordati in anticipo con i clienti. In questa procedura dettagliata, vengono fornite informazioni per:  

- Determinare i valori di contratto e fattura.  
- Includere lavoro extra non fatturato nella pianificazione.  

### <a name="copying-a-project"></a>Copia di un progetto

 Questa parte della procedura dettagliata si incentra sulla copia, parziale o totale, di un progetto al fine di ridurre l'immissione manuale di dati e garantire maggior accuratezza.

- Copiare parte di un progetto in un nuovo progetto.  
- Copiare prezzi specifici di un progetto.  
- Copiare righe di pianificazione.  

### <a name="making-payment-by-installment"></a>Pagamenti rateali

 Nel caso di progetti di grande respiro, costosi e che si protraggono per lunghi periodi, il cliente spesso concorda con il fornitore un pagamento rateale. Questo scenario tratta dell'impostazione di questi pagamenti:  

- Creare un pagamento rateale per un progetto.  
- Fatturare pagamenti ai clienti.  
- Contabilizzare l'utilizzo nell'impostazione di un progetto per pagamenti rateali.  

## <a name="roles"></a>Ruoli

 Questa procedura dettagliata include attività per i seguenti ruoli:  

- Project manager  
- Membro del team di progetto  

## <a name="prerequisites"></a>Prerequisiti

 Prima di svolgere le attività di questa procedura dettagliata, è necessario:  

- Installare il database dimostrativo CRONUS.
- Creare dati di esempio seguendo la procedura descritta nella sezione seguente.  

## <a name="story"></a>Scenario

Per questa procedura dettagliata viene utilizzata una società di progettazione e consulenza immaginaria denominata CRONUS che progetta e installa nuove infrastrutture. Ad esempio, sale conferenza e uffici arredati, accessori e unità di immagazzinaggio. La maggior parte del lavoro è svolta in base a progetti. Ezio Alboni è un project manager in CRONUS e utilizza il progetto per avere una panoramica di ciascuna attività in corso avviata e completata da CRONUS. Solitamente è la persona che definisce gli affari con i clienti e inserisce i dettagli di base del progetto, cioè righe di attività e di pianificazione e prezzi, in [!INCLUDE[prod_short](includes/prod_short.md)]. Alboni trova che creare, gestire e analizzare i dati sia semplice. Alboni inoltre apprezza il modo in cui [!INCLUDE[prod_short](includes/prod_short.md)] consente la copia di progetti e pagamenti rateali.

 Cinzia Di Marco fa parte del team alle dirette dipendenze di Alboni ed è responsabile del monitoraggio quotidiano del progetto. Cinzia registra il lavoro svolto dai tecnici in ogni attività nonché i materiali utilizzati e i costi incorsi.  

## <a name="preparing-sample-data"></a>Preparazione dei dati di esempio

Per preparare questa procedura dettagliata, è necessario aggiungere Cinzia come risorsa.  

### <a name="to-prepare-the-sample-data"></a>Per preparare i dati di esempio

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Risorse**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** per creare una nuova scheda risorsa.  
3. Nella Scheda dettaglio **Generale** immettere le seguenti informazioni:  

    - **Nr.**: **Di Marco**  
    - **Nome**: **Di Marco**  
    - **Tipo**: **Persona**  

4. Scegliere il campo **Unità di misura base** e scegliere l'azione **Nuovo** per aprire la pagina **Unità di misura risorse**. Nel campo **Codice** selezionare **Ora**.  
5. Nella Scheda dettaglio **Fatturazione** inserire i seguenti dati:  

    - **Costo unitario diretto**: **5**  
    - **% costi indiretti**: **4**  
    - **Costo unitario**: **10**  
    - **Cat. reg. articolo/servizio**: **Servizi**  
    - **Cat. reg. art./serv. IVA**: **IVA 25**  

6. Chiudere la pagina.

Nella procedura descritta di seguito si crea un batch registrazioni progetti affinché Cinzia possa registrare il relativo utilizzo.  

### <a name="to-create-a-project-journal-batch"></a>Per creare un batch registrazioni progetti

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Registrazione progetti** scegliere il campo **Nome batch**. Viene visualizzata la pagina **Batch registrazioni progetti**.  
3. Scegliere l'azione **Nuovo** per creare una nuova riga con le informazioni seguenti:  

    - **Nome**: **Di Marco**  
    - **Descrizione**: **Di Marco**  
    - **Nr. serie**: **REGCOMM**  

4. Scegliere il pulsante **OK** per salvare le modifiche.

## <a name="setting-up-a-project-1"></a>Impostazione di un progetto

In questo scenario, CRONUS si è aggiudicata un appalto dal cliente Progressive Home Furnishings per la progettazione di una sala conferenze e di rappresentanza. Il cliente ha sede negli Stati Uniti e il progetto richiede software particolare. Il project manager raggiunge un accordo con il cliente e crea un progetto per il contratto.  

### <a name="to-set-up-a-project"></a>Per impostare un progetto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** per creare una nuova scheda.  
3. Nella Scheda dettaglio **Generale** immettere le seguenti informazioni:  

    - **Descrizione**: **Consulenza per progettazione aula conferenze**  
    - **Fatturare a - Nr. cli.**: **01445544**  

4. Nella Scheda dettaglio **Registrazione** inserire i seguenti dati:  

    - **Stato**: **Pianificazione**  
    - **Categoria registrazione progetto**: **Impostazione**  
    - **Metodo WIP**: **Valore costo**  

5. Nella Scheda dettaglio **Durata** immettere la data odierna nei campi **Data inizio** e **Data fine**. Queste date agevolano l'applicazione delle conversioni di valuta al momento della fatturazione del progetto.  
6. Nella Scheda dettaglio **Commercio estero** impostare il codice di valuta su **USD**. Se si seleziona USD nel campo **Codice valuta fattura**, il progetto viene fatturato in dollari statunitensi e pianificato solo nella valuta locale di CRONUS.  

 È possibile personalizzare il prezzo per i clienti per progetto, in base ai contratti. Nella procedura successiva, il project manager specifica un costo per il tempo di Cinzia, imposta il prezzo per il software necessario e aggiunge i costi di viaggio che il cliente ha accettato di pagare.  

### <a name="to-customize-pricing"></a>Per personalizzare il prezzo

1. Nella **Scheda progetto**, scegliere l'azione **Risorsa**.  
2. Nella pagina **Prezzi risorse progetto**, immettere le seguenti informazioni:  

    - **Codice**: **Di Marco**  
    - **Prezzo unitario**: **20**  

3. Chiudere la pagina.  
4. Scegliere l'azione **Articolo**.  
5. Nella pagina **Prezzi articoli progetto**, immettere le seguenti informazioni e il prezzo personalizzato:  

    1. **Nr. articolo**: **80201 (Progr.grafica)**  
    2. **Prezzo unitario**: **200**  

6. Chiudere la pagina.  
7. Scegliere l'azione **Conto C/G**.  
8. Nella pagina **Prezzi conti C/G progetti**, immettere le seguenti informazioni e i costi di viaggio, per i quali il cliente si impegna a pagare il costo più il 25%:  

    1. **Conto C/G**: **8430 (Spese per viaggi e trasferte)**  
    2. **Fattore costo unitario**: **1,25**  

9. Chiudere la pagina.  

 I passaggi finali dell'impostazione del progetto sono l'aggiunta delle attività di progetto e delle righe di pianificazione progetto che fanno parte di ogni attività. Le righe di pianificazione determinano ciò che viene fatturato al cliente.  

### <a name="to-add-project-tasks"></a>Per aggiungere attività di progetto

1. Nella scheda **Progetto** per il nuovo progetto, scegliere l'azione **Righe attività di progetto**.  
2. Nella seguente tabella vengono illustrate le informazioni che è necessario immettere nei campi.  

    |Nr. attività di progetto|Descrizione|Tipo di attività di progetto|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Consulenza per progettazione aula conferenze|Inizio-Totale|  
    |1010|Incontro di consultazione con cliente|Analitico|  
    |1020|Sviluppo|Analitico|  
    |1090|Totale consulenza|Fine-Totale|  

3. Per mostrare che alcune attività sono sottocategorie di altre attività, scegliere l'azione **Indenta attività di progetto**.  

Una riga di pianificazione può essere di uno dei seguenti tipi:  

- **Budget**: aggiunto alla pianificazione ma non fatturato.  
- **Fatturabile**: fatturato ma non aggiunto alla pianificazione.  
- **Sia Budget sia fatturabile**: fatturato e aggiunto alla pianificazione.  

In questa procedura dettagliata, il project manager utilizza **Budget e fatturabile**. Crea tre righe di pianificazione per il task 1010 e due righe di pianificazione per l'attività 1020.  

### <a name="to-create-planning-lines"></a>Per creare righe di pianificazione

1. Selezionare la riga 1010, quindi scegliere l'azione **Righe di pianificazione progetto**.  
2. Creare righe di pianificazione con i seguenti dati:  

    | Riga | Tipo riga | Data pianificazione  | Tipo        | No.   | Quantità | Prezzo unitario |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Sia budget sia fatturabile | (data odierna) | Risorsa | Cinzia | 40        |     |
    | 2    | Sia budget sia fatturabile | (data odierna) | Risorsa | Maldonado | 40        |     |
    | 3    | Sia budget sia fatturabile | (data odierna) | Conti C/G | 8430 (spese per viaggi e trasferte) | 2 | 400    |

     Chiudere la pagina. I totali vengono aggiornati nella pagina **Righe attività di progetto**.  
3. Selezionare la riga 1020, quindi scegliere l'azione **Righe di pianificazione progetto**. Inserire i seguenti dati:  

    | A linee | Tipo riga | Data pianificazione  | Tipo        | No.   | Quantità | Prezzo unitario |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Sia budget sia fatturabile | (data odierna) | Risorsa | Cinzia | 80        |     |
    | 2    | Sia budget sia fatturabile | (data odierna) | Articolo | 80201 (Progr. grafica) | 1 |     |

4. Chiudere la pagina. I totali vengono aggiornati nella pagina **Righe attività di progetto**.  

## <a name="calculating-remaining-usage"></a>Calcolo dell'utilizzo residuo

Cinzia, il membro del team, lavora al progetto da qualche tempo e desidera registrare le sue ore e l'utilizzo nella commessa. Non ha lavorato più ore di quanto concordato in origine con il cliente. Cinzia utilizza il processo batch **Calc. utilizzo residuo** per calcolare l'utilizzo residuo in una registrazione progetti. Per ciascuna attività il processo batch calcola la differenza tra l'utilizzo programmato di articoli, risorse e spese di contabilità generale e l'utilizzo effettivo registrato nei movimenti contabili progetto. L'utilizzo residuo viene quindi visualizzato nella registrazione progetti e Cinzia può eseguirne la registrazione.  

### <a name="to-calculate-remaining-usage"></a>Per calcolare l'utilizzo residuo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Registrazione progetti**, nel campo **Nome batch**, aprire l'elenco **Batch registrazioni progetti**. Selezionare il batch registrazioni progetti **Cinzia**.  
3. Scegliere l'azione **Calc. utilizzo residuo**.  
4. Nella Scheda dettaglio **Attività di progetto** della pagina **Progetto - Calcolo utilizzo residuo** scegli il campo **Nr. progetto** e seleziona il numero di progetto pertinente, in genere J00010.  
5. Nella Scheda dettaglio **Opzioni**, digitare **J00001** nel campo **Nr. documento**. Queste informazioni agevolano il futuro monitoraggio della registrazione.  
6. Immetti la data corrente come data di registrazione.  
7. Scegli il pulsante **OK**. Questa azione genera le righe di registrazione progetto nelle righe di pianificazione create dal project manager.  
8. Nella pagina di conferma scegliere il pulsante **OK**. Le righe generate vengono aggiunte alla registrazione progetti.  
9. Accertarsi che tutti i numeri di documento siano J00001, quindi scegliere l'azione **Registra**. Selezionare **Sì** per confermare la registrazione.  

Le righe sono così registrate.  

## <a name="creating-and-posting-a-project-sales-invoice"></a>Creazione e registrazione di una fattura di vendita per un progetto

Cinzia può ora creare una nuova fattura per l'intero progetto o per parte di un progetto. Può anche allegare la fattura a un'altra fattura per lo stesso cliente e per lo stesso progetto. In questo caso, Cinzia fattura l'intero progetto poiché è completato.  

### <a name="to-create-a-project-sales-invoice"></a>Per creare una fattura di vendita per un progetto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Selezionare il progetto creato in precedenza, quindi scegliere l'azione **Crea fattura vendita per progetto**.  
3. Nella Scheda dettaglio **Attività di progetto**, cancellare i filtri in **Nr. attività di progetto** per fatturare il progetto. Nel campo **Nr. progetto** selezionare il progetto pertinente.  
4. Nella Scheda dettaglio **Opzioni** immettere la data di registrazione e specificare se creare una fattura per attività oppure una singola fattura per tutte le attività.  
5. Selezionare il pulsante **OK** per creare la fattura e fare clic sul pulsante **OK** nella pagina di conferma.  

Dopo che Tricia ha creato la fattura, è disponibile nella Gestione ruolo utente **Gestione ordini vendite**.

### <a name="to-post-a-new-sales-invoice"></a>Per registrare una nuova fattura di vendita

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.  
2. Aprire la fattura per il cliente numero 01445544. Sono visibili le informazioni inserite dalle righe di pianificazione.  
3. Scegliere l'azione **Registra**. Selezionare **Sì** per confermare la registrazione.  

### <a name="to-view-the-posted-invoice"></a>Per visualizzare la fattura registrata

1. Aprire il progetto, quindi scegliere l'azione **Righe pianificazione progetto**.  
2. Selezionare una qualsiasi delle righe di pianificazione fatturate, quindi scegliere l'azione **Ottieni nota credito/fattura vendita**.
3. Nella pagina **Fatture progetto** scegliere l'azione **Apri fattura/nota credito vendita**.  

Cinzia ha una domanda su prezzi, costi o margini pertinenti a questo specifico progetto, quindi accede alle informazioni nella pagina **Statistiche**.  

### <a name="to-open-the-statistics-page"></a>Per aprire la pagina Statistiche

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Statistiche**. È possibile esaminare informazioni dettagliate su prezzi, costi e margini dei progetti sia in valuta locale che estera.  
3. Scegliere il pulsante **Chiudi** per chiudere la pagina **Statistiche progetto**.  

## <a name="handling-fixed-prices-1"></a>Gestione dei prezzi fissi

CRONUS ha ottenuto un contratto per l'allestimento di alcune sale per conferenze. Come project manager, Alboni vuole una panoramica precisa dei task necessari per il progetto con i costi previsti e sostenuti associati per ciascuna attività. Inoltre, Alboni desidera conoscere il prezzo totale a contratto del progetto e l'importo fatturato finora. Ha concluso un contratto con il cliente in cui sono stati concordati prezzi fissi per il progetto.  

### <a name="to-manage-fixed-pricing-in-projects"></a>Per gestire i prezzi fissi nei progetti

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Selezionare il numero di progetto **Società mercantile internaz.**, quindi scegliere l'azione **Righe attività di progetto**.  
3. Seleziona la riga 1,120 e nel campo **Budget (costo totale)** fai clic con il pulsante destro del mouse sull'importo e scegli **DrillDown**.  

     Esaminando le righe di pianificazione progetto, Alboni stabilisce che ha bisogno di Cinzia per 30 ore per questa fase del progetto. E concorda un prezzo fisso con il cliente.  

4. Nella pagina **Righe attività di progetto**, selezionare la riga 1120, quindi scegliere l'azione **Righe di pianificazione progetto**. Creare una riga di pianificazione con i seguenti dati:  

    | Riga | Tipo riga | Tipo        | No.   | Quantità |
    |------|-----------|-------------|-------|----------|
    | 1    | Sia budget sia fatturabile  | Risorsa | Cinzia | 30 |

     Chiudere la pagina.  
5. Nel campo **Budget (costo totale)**, fai clic con il pulsante destro del mouse sul campo e scegli di nuovo **Drilldown** nella pagina **Righe attività di progetto**. Visualizzare le modifiche alla pianificazione. Le 30 ore vengono aggiunte alla pianificazione.  
6. Chiudere le pagine.  

Dopo che Cinzia è stata aggiunta alla pianificazione per questa riga di attività, lavora per 25 ore al progetto e immette queste ore nella registrazione progetto.  

### <a name="to-enter-hours-in-a-project-journal"></a>Per inserire ore in una registrazione progetti

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
2. In una nuova riga inserire i seguenti dati:  

    - **Tipo riga**: **(vuoto)**  
    - **Data di registrazione**: **(data odierna)**  
    - **Nr. documento**: **J00002**  
    - **Nr. progetto**: **Società mercantile internaz.**  
    - **Nr. attività di progetto**: **1120**  
    - **Tipo**: **Risorsa**  
    - **Nr.**: **Di Marco**  
    - **Quantità**: **25**  

3. Scegli l'azione **Registra**.  

     Pochi giorni dopo, Cinzia lavora per altre 10 ore sul progetto e ora ha lavorato 35 ore in tutto. Poiché il contratto è per 30 ore, solo cinque delle ore vengono addebitate al cliente. Cinzia aggiunge manualmente le altre cinque ore alla pianificazione.  

4. Nella pagina **Registrazione progetti**, scegliere l'azione **Calc. utilizzo residuo**.  
5. Nella Scheda dettaglio **Opzioni** della pagina **Progetto - Calcolo utilizzo residuo** inserire le seguenti informazioni:  

    - **Nr. documento**: **J00003**  
    - **Data di registrazione**: **(data odierna)**  

6. Nella Scheda dettaglio **Attività di progetto** inserire le seguenti informazioni:  

    - **Nr. progetto**: **Società mercantile internaz.**  
    - **Nr. attività di progetto**: **1120**  

7. Per eseguire il calcolo, fare clic sul pulsante **OK**.

    Ci sono cinque ore di lavoro residuo per Cinzia. Il campo **Tipo riga** è vuoto, il che indica che solo l'utilizzo deve essere ancora registrato perché il lavoro è già stato pianificato.  

8. Nella finestra **Registrazione progetti**, creare una nuova riga con i seguenti dati. Accertarsi che entrambi i numeri di progetto siano consecutivi a quelli già usati:  

    - **Tipo riga**: **Budget**  
    - **Nr. progetto**: **Società mercantile internaz.**  
    - **Nr. attività di progetto**: **1120**  
    - **Tipo**: **Risorsa**  
    - **Nr.**: **Di Marco**  
    - **Quantità**: **5**  

     Se si utilizza il tipo di riga **Budget**, vengono aggiornati i prezzi e i costi pianificati, mentre non vengono aggiornati i costi e prezzi di contratto che sono fatturati al cliente.  

9. Scegli l'azione **Registra**. Scegliere il pulsante **OK** per chiudere la pagina.  
10. Aprire l'elenco **Progetti**.  
11. Seleziona il progetto SOCIETÀ MERCANTILE INTERNAZ. e poi, nella sezione **Righe attività di progetto** seleziona la riga 1120 e nel campo **Budget (costo totale)** fai clic con il pulsante destro del mouse sull'importo. Selezionare **Drilldown** per visualizzare le informazioni.  

     Le modifiche sono inserite automaticamente nella riga per il Nr. attività di progetto 1120. Nel costo totale del lavoro pianificato, cinque ore in più di lavoro di Cinzia sono state aggiunte alla programmazione.  

12. Scegliere il pulsante **Chiudi** per chiudere la pagina.  
13. Fare clic con il pulsante destro del mouse sull'importo del campo **Contratto (costo totale)** e selezionare **Drilldown** per visualizzare le informazioni.  

Nel prezzo totale del contratto sono incluse solo le 30 ore pattuite in origine con il cliente.  

## <a name="copying-projects"></a>Copia di progetti

Alboni ha concluso un contratto con un cliente, Selagorian Ltd, per l'allestimento di dieci sale per conferenze. Il contratto è simile a un progetto precedente. Di conseguenza, si risparmierà tempo copiando tale progetto precedente.  

Nella pagina **Copia progetto** è possibile selezionare il progetto e le righe di attività che si desidera copiare.

- Copiare i movimenti contabili del progetto di origine per creare righe di pianificazione basate sull'utilizzo effettivo.
- Copiare le righe di pianificazione progetto di origine per copiare le righe di pianificazione originali nel nuovo progetto.

Si può quindi scegliere quale tipo di riga di pianificazione o di movimento contabile includere, selezionando solo quello applicabile al nuovo progetto. Infine, si può decidere se copiare anche prezzi e quantità dal progetto selezionato.  

### <a name="to-copy-a-project"></a>Per copiare un progetto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** per creare un nuovo progetto. Inserire i seguenti dati:  

    - **Descrizione**: **Pianificazione di dieci aule per conferenze**  
    - **Fatturare a - Nr. cli.**: **20000**  

3. Scegliere l'azione **Copia attività di progetto da**.  
4. Nella pagina **Copia attività di progetto**, immettere le seguenti informazioni:  

    - **Nr. progetto**: **Società mercantile internaz.**  
    - **Nr. attività di progetto da**: **1000**  
    - **Origine**: **Righe di pianificazione progetto**  
    - **Incl. tipo riga pianificazione**: **Budget e fatturabile**  
    - **Nr. attività di progetto - A**: **Società Mercantile Internaz. Pianificazione 10 sale per conferenze**  
    - Selezionare i campi **Copia dimensioni** e **Copia quantità**.  

5. Selezionare il pulsante **OK** per copiare il progetto e fare clic sul pulsante **OK** per chiudere la pagina di conferma.  

Confrontando prezzi, righe di attività di progetto e righe di pianificazione progetto per i due progetti, è possibile verificare che le informazioni sono state copiate correttamente.  

## <a name="making-payments-by-installments"></a>Effettuare pagamenti rateali

CRONUS si è appena aggiudicata un grande progetto il cui completamento richiederà un anno. Poiché impegna molte risorse, il project manager imposta il contratto per il pagamento anticipato da parte del cliente di parte del prezzo a metà del progetto e il saldo al completamento del progetto.  

### <a name="to-set-up-a-new-account"></a>Per impostare un nuovo conto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Piano dei conti** scegliere l'azione **Nuovo** per creare una nuova scheda.  
3. Nella scheda del nuovo **Conto C/G** inserire i seguenti dati:  

    - **Nr.**: **40255**  
    - **Nome**: **Pagamento progetto**  

4. Nel campo **Cat. reg. articolo/servizio** della Scheda dettaglio **Registrazione**, seleziona **Servizi**. Chiudere la pagina.  
5. Nella pagina **Piano dei conti**, selezionare **Nr. 40255 Pagamento commessa**, quindi scegliere **Indenta piano dei conti**. Scegliere **Sì** per confermare.  

Le procedure riportate di seguito mostrano come creare uno nuovo progetto, impostare il prezzo e il pagamento rateale. Nelle righe di attività di progetto è possibile creare righe specifiche dedicate al pagamento rateale. Tutto il lavoro completato per il progetto che viene aggiunto alla pianificazione sarà inserito nelle righe di utilizzo. Per ogni riga di attività pagamento nelle righe di pianificazione, il tipo di riga è **Fatturabile**, che significa che sarà emessa fattura al cliente. Immettere una nuova riga per il primo acconto. Nella riga di attività utilizzo, inserire i dati relativi agli articoli e alle risorse che sono stati utilizzati nel progetto; ciò incrementa la pianificazione in termini di ore dei dipendenti e di articoli impiegati nel progetto.  

### <a name="to-make-a-payment-by-installment"></a>Per effettuare un pagamento rateale

1. Creare un nuovo progetto.  
2. Nella nuova scheda **Progetto** inserire i seguenti dati:  

    - **Descrizione**: **Ridecorazione dell'area reception**  
    - **Fatturare a - Nr. cli.**: **30000**  
    - **Categoria registrazione progetto**: **Impostazione**  
    - **Metodo WIP**: **Valore costo**  

3. Nella Scheda progetto, scegli l'azione **Prezzi**, quindi scegli l'azione **Risorsa**. Inserire i seguenti dati:  

    - **Codice**: **Di Marco**  
    - **Prezzo unitario**: **10**  

     Chiudere la pagina.  

4. Nella scheda **Progetto**, della sezione **Attività**, aggiungi le righe di attività di progetto come descritto nella tabella seguente:  

    | A linee | Nr. attività di progetto | Descrizione          | Tipo di attività di progetto |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Pagamento - primo acconto | Registrazione       |
    | 2    | 2000         | Utilizzo                | Registrazione       |
    | 3    | 3000         | Pagamento - secondo acconto     | Registrazione       |
    | 4    | 4000         | Pagamento - saldo | Registrazione       |

5. Scegli l'attività 1000, quindi l'azione **Righe di pianificazione progetto**.  

6. Creare una riga di pianificazione con le seguenti informazioni:  

    | Riga | Tipo riga | Data pianificazione  | Tipo        | No.   | Quantità | Prezzo unitario |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Fatturabile  | (data odierna) | Conti C/G | 40255 | 1        | 5000       |

     Chiudere la pagina.  

7. Scegli l'attività 2000, quindi l'azione **Righe di pianificazione progetto**.  

8. Creare una riga di pianificazione con le seguenti informazioni:

    | Riga | Tipo riga | Data pianificazione  | Tipo     | No.    | Quantità |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budget    | (data odierna) | Risorsa | Cinzia | 120      |
    | 2    | Budget    | (data odierna) | Articolo     | 70104  | 10       |

     Chiudere la pagina. Nella pagina **Righe attività di progetto** è possibile visualizzare gli importi di programmazione aggiornati.  

9. Scegli l'attività 32000, quindi l'azione **Righe di pianificazione progetto**.  

10. Creare una riga di pianificazione con le seguenti informazioni:

    | Riga | Tipo riga | Data pianificazione   | Tipo        | No.   | Quantità | Prezzo unitario |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Fatturabile  | (una data futura) | Conti C/G | 40255 | 1        | 5000       |

     Chiudere la pagina.  

11. Creare un movimento della riga di pianificazione simile per l'attività di progetto 4000.  

 Ora che le righe di attività e di pianificazione sono state registrate, Alboni crea una fattura per il primo pagamento. Alboni procede dalle righe di attività di progetto per assicurarsi che la fattura contenga solo le righe del primo pagamento. Aprire l'ordine di vendita dalle righe di pianificazione o dalle righe di attività.  

### <a name="to-create-an-invoice"></a>Per creare una fattura

1. Nella pagina **Righe attività di progetto**, selezionare la riga 1000, quindi scegliere l'azione **Crea fattura di vendita**.  
2. Nella pagina **Crea fattura di vendita**, impostare la data odierna come data di registrazione, specificare **Per attività** e fare clic sul pulsante **OK** per creare una fattura con i dati di default. Fare clic sul pulsante **OK** per chiudere la pagina di conferma.  
3. Scegliere l'azione **Ottieni nota credito/fattura vendita**. Nella fattura di vendita è possibile visualizzare che nella fattura è incluso solo il primo acconto. È ora possibile inviarla al cliente come concordato.  

## <a name="summary"></a>Riepilogo

In questa procedura dettagliata sono state riprodotte alcune delle operazioni di base relative alla gestione dei progetti in [!INCLUDE[prod_short](includes/prod_short.md)]. Si è appreso come creare uno nuovo progetto, come copiare un progetto e come gestire i pagamenti. Inoltre, è stato illustrato come tenere traccia delle ore e creare le fatture.  

## <a name="see-also"></a>Vedere anche

 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Impostazione della Gestione progetti](projects-setup-projects.md)  
 [Utilizzare le risorse](projects-how-use-resources.md)  
 [Monitoraggio di progressi e performance](projects-how-monitor-progress-performance.md)  
 [Fatturare i progetti](projects-how-invoice-jobs.md)  
 [Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
