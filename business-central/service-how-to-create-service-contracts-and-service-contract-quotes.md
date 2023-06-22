---
title: Come utilizzare contratti di assistenza e offerte di contratto di assistenza | Documenti Microsoft
description: È possibile creare un contratto di assistenza manualmente o partendo da un'offerta di contratto assistenza. È possibile creare un contratto basato su un'offerta di contratto di assistenza.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="work-with-service-contracts-and-service-contract-quotes" />Utilizzare contratti e offerte di contratto di assistenza
È possibile creare un contratto di assistenza manualmente o partendo da un'offerta di contratto assistenza. Se l'offerta di contratto di assistenza viene utilizzata come base per un contratto di assistenza, la società propone un'offerta al cliente, il quale la approva prima che possa essere convertita in un contratto di assistenza. Le procedure per la creazione di un contratto di assistenza o di un'offerta di contratto di assistenza sono analoghe.  

## <a name="to-create-a-service-contract-or-service-contract-quote" />Per creare un contratto o un'offerta di contratto di assistenza
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza** o **Offerte contratto assistenza**, quindi seleziona il collegamento correlato.  
2. Creare un nuovo contratto o un'offerta di contratto di assistenza.  
3. Compilare il campo **Nr.** . Verrà visualizzata una finestra di dialogo in cui viene chiesto se si desidera compilare il contratto o l'offerta utilizzando i dati di un modello di contratto. Se si desidera creare un contratto di assistenza o un'offerta di questo tipo, fare clic sul pulsante **Sì**. Verrà visualizzata la pagina **Lista modelli contr. assist**.  
4. Selezionare il modello appropriato, quindi scegliere **OK** per creare il contratto o l'offerta di contratto di assistenza.  
5. Nel campo **Nr. cliente** scegliere il cliente.  
6. Se non si desidera che una differenza di importo annuo venga distribuita automaticamente, selezionare la casella di controllo **Permetti differenza importo**. I valori dei campi **Importo annuo** e **Importo annuo calcolato** non vengono automaticamente equiparati. Se si desidera che una differenza di importo annuo, che potrebbe derivare da una modifica nel contratto di servizio, venga distribuita automaticamente, lasciare deselezionata la casella di controllo **Permetti differenza importo**.  
7. Inserire le righe di contratto nel contratto o nell'offerta di contratto di assistenza.  
8. Compilare debitamente il resto dei campi.  

## <a name="to-convert-a-service-contract-quote-to-service-contract" />Per convertire un'offerta di contratto di assistenza in contratto di assistenza
Quando un cliente ha accettato un'offerta di contratto di assistenza, quest'ultima viene trasformata in un contratto di assistenza. Contemporaneamente è possibile creare una fattura di assistenza per il periodo iniziale del contratto, se la data di inizio del contratto risulta precedente al successivo periodo di fatturazione.

Dopo il completamento dei passaggi seguenti, viene creato un contratto di assistenza con lo stato **Firmato**. Se viene creata una fattura di assistenza per il periodo d'inizio del contratto, l'importo fatturato verrà calcolato come riportato di seguito, in base al livello di dettaglio del contratto.  

Per i contratti dettagliati l'importo fatturato verrà calcolato come segue:  

* importo fatturato = totale dell'importo fatturato per ogni riga di contratto.  
* Importo fatturato per ogni riga di contratto = ((valore offerta ÷ 12) × numero di mesi nel periodo iniziale) + ((valore offerta ÷ numero di giorni nell'anno) × numero di giorni residui nel periodo iniziale).  
* Se la riga di contratto scade prima della fine del periodo d'inizio, la data di termine diventerà la data finale del periodo d'inizio della riga.  

Per i contratti non dettagliati l'importo fatturato verrà calcolato come segue:  

* importo fatturato = (importo annuale ÷ numero di giorni nell'anno) × il numero di giorni nel periodo d'inizio.  
* Se il contratto scade prima della fine del periodo d'inizio, la data di scadenza diventerà la data di fine periodo d'inizio.    

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Offerte contratto assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l' offerta contratto di assistenza che si desidera convertire in un contratto di assistenza.  
3. Scegliere l'azione **Crea contratto**.  
4. Se la data di inizio del contratto risulta precedente al successivo periodo di fatturazione, viene richiesto se si desidera creare una fattura per il periodo iniziale del contratto. Selezionare **Sì**.  

 La fattura di assistenza viene registrata nel conto relativo all'assistenza del contratto, anche se il contratto è prepagato.

## <a name="to-create-contract-service-credit-memos" />Per creare note di credito di assistenza per un contratto
È possibile utilizzare una nota di credito di assistenza per un contratto quando un cliente annulla un contratto di assistenza prepagato oppure elimina un articolo in assistenza da un contratto prepagato. La nota di credito di vendita consente inoltre di correggere una fattura di assistenza errata.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note credito assistenza**, quindi scegli il collegamento correlato.  
2. Creare una nuova nota di credito di assistenza.  
3. Compilare il campo **Nr.** .  
4. Nel campo **Nr. cliente** immettere il numero del cliente relativo al contratto di assistenza.  

     Nella Scheda dettaglio **Fatturazione** vengono visualizzate le informazioni copiate dalla scheda **Cliente**. Se si desidera registrare la nota di credito per un cliente diverso da quello specificato nella Scheda dettaglio **Generale**, immettere il relativo numero nel campo **Fatturare a - Nr. cli.**    

    > [!NOTE]  
    >  È possibile confrontare la nota di credito con il documento originale registrato nella pagina **Fatture assistenza registrate**. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture assistenza registrate**, quindi scegli il collegamento correlato.  

5. Compilare i campi relativi a **data di registrazione** e **data del documento**.  
6. Nelle righe della nota di credito immettere le informazioni relative agli articoli resi o rimossi o agli abbuoni che verranno inviati. È inoltre possibile utilizzare il processo batch **Prendi mov. contr. prepagati**.  

 Per creare automaticamente una nota di credito durante l'eliminazione delle righe di contratto da un contratto di assistenza, nella Scheda dettaglio **Dettagli fattura** della pagina **Contratto di assistenza** selezionare la casella di controllo **Note credito automatiche**.  

 Per creare manualmente una nota di credito durante l'eliminazione delle righe di contratto da un contratto di assistenza, nella pagina **Contratto di assistenza** scegliere l'azione **Nota credito**.  

## <a name="updating-and-evaluating-contracts" />Aggiornamento e valutazione dei contratti
Talvolta può essere necessario modificare le condizioni di un contratto dopo che è stato creato. Nella maggior parte dei casi è sufficiente aprire il contratto in questione nella pagina **Contratto di assistenza** e apportare le modifiche necessarie.  

È possibile cambiare lo stato del contratto, inizialmente impostato su **Bloccato**, aggiungere e rimuovere righe del contratto e annullare un contratto. Se si desidera vedere come procede l'attività in termini di guadagni e perdite, è possibile eseguire una rapida analisi utilizzando la funzionalità Trendscape contratto.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote" />Per aggiungere una riga di contratto a un contratto di assistenza o a un'offerta di contratto
Quando un cliente acquista un nuovo articolo e desidera includerlo in un contratto di assistenza esistente o un'offerta di contratto, è possibile registrare l'articolo come articolo in assistenza e inserirlo nel contratto o nell'offerta di contratto come nuova riga di contratto.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza**, quindi scegli il collegamento correlato.  
2. Aprire il contratto di assistenza o l'offerta di contratto di assistenza per cui si desidera aggiungere una nuova riga.  
3. Scegliere l'azione **Apri contratto** per aprire il contratto o l'offerta di contratto di assistenza per la modifica.  
4. Nella Scheda dettaglio **Dettagli fattura** selezionare il campo **Permetti differenza importo** se si desidera modificare l'importo annuo e ripartire manualmente la differenza dell'importo annuo nelle righe di contratto. In alternativa, deselezionare la casella di controllo nel campo **Permetti differenza importo**. La differenza dell'importo annuo verrà ripartita automaticamente nelle righe di contratto dopo la modifica dell'importo annuo.  
5. Nella Scheda dettaglio **Righe** aggiungere l'articolo o gli articoli in assistenza oppure una descrizione in ciascuna riga. In alternativa, è possibile aggiungere righe di offerta di contratto. È possibile creare contratti multipli per un articolo in assistenza in modo che risulti incluso contemporaneamente in differenti contratti di assistenza o offerte di contratto.  
6. Verificare e correggere i numeri nei campi **% sconto riga**, **Importo sconto riga**, **Ora di risposta**, **Periodo assistenza** e in altri campi, se necessario.

## <a name="to-remove-contract-lines" />Per eliminare le righe di contratto
A seguito della rimozione di articoli in assistenza da un contratto di assistenza, potrebbe essere necessario dover rimuovere le righe corrispondenti dal contratto di assistenza. Solitamente si rimuove una riga di contratto scaduta o corrispondente all'articolo in assistenza che si è guastato.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza**, quindi scegli il collegamento correlato.  
2. Aprire il contratto di assistenza da cui si desidera rimuovere delle righe.  
3. Scegliere l'azione **Apri contratto** per aprire il contratto di assistenza per la modifica.  
4. Scegliere la riga del contratto che si desidera rimuovere. Compilare il campo **Data scadenza contratto** con la data a partire da cui si desidera rimuovere la riga. Ad esempio, è possibile immettere la data in cui l'articolo in assistenza si è guastato.  
5. Scegliere l'azione **Rimuovi righe contratto**. Verrà visualizzata la pagina **Eliminaz. righe da contratti**.  
6. Compilare i filtri di default: **Nr. contratto**, **Nr. articolo in assistenza** e **Tipo contratto**. Se necessario, è possibile applicare più filtri o modificare quelli esistenti.  
7. Compilare i campi della Scheda dettaglio **Opzioni**, quindi scegliere l'azione **Elimina righe** .  

> [!NOTE]  
>  Se il contratto non è dettagliato, occorre aggiornare il valore del campo **Importo annuo** nella Scheda dettaglio **Dettagli fattura** della pagina **Contratto di assistenza** in modo da riflettere l'eliminazione dell'articolo in assistenza dal contratto.  
>   
>  Se il contratto è dettagliato e prepagato e sono state registrate fatture per il contratto, è possibile creare una nota di credito per il contratto. Scegliere l'azione **Crea nota credito**. Questa operazione non è necessaria se è selezionata la casella di controllo nel campo **Note credito automatiche** nella Scheda dettaglio **Dettagli fattura**. In tal caso, una nota di credito viene automaticamente creata quando si rimuove una riga di contratto.

## <a name="service-line-cost-and-value" />Costo e valore riga assistenza
Nelle righe di un contratto di assistenza, gli importi in **Costo riga** e **Valore riga** viene calcolato come descritto nelle seguenti tabelle.

| Opzioni costo riga | Description|
|----------------------------------|---------------------------------------|  
|**Articolo in assistenza** | Il costo viene automaticamente recuperato dal campo **Costo di default del contratto** della tabella **Articolo in assistenza** e copiato nel campo **Costo riga**. Per il calcolo del costo della riga viene utilizzata la seguente formula:<br /><br /> Costo unitario di vendita × % valore contratto ÷ 100|  
|**Articolo** | Il costo viene automaticamente recuperato dal campo **Costo unitario** della tabella **Articolo** e dal valore del campo **% valore contratto** della tabella **Setup gest. assist.** Per il calcolo del costo della riga viene utilizzata la seguente formula:<br /><br /> Costo unitario × % valore contratto% ÷ 100|  
|**Descrizione testo** | Il valore del campo **Costo riga** viene impostato su zero.|  

| Opzioni valore riga | Description|
|----------------------------------|---------------------------------------|  
|**Articolo in assistenza** | Il prezzo viene automaticamente recuperato dal campo **Valore contratto di default** della tabella **Articolo in assistenza** e copiato nel campo **Valore riga**.|  
|**Articolo** | In base al valore del campo **Metodo calc. valore contratto** della tabella **Setup gest. assist.** l'importo viene recuperato dal campo **Prezzo unitario** o **Costo unitario** della tabella **Articolo**. Successivamente, tale valore viene moltiplicato per il contenuto del campo **% Valore contratto** della tabella **Setup gest. assist.** e diviso per 100. L'importo risultante viene quindi copiato nel campo **Valore riga**.<br /><br /> **NOTA:** Se il valore del campo **Metodo calc. valore contratto** è impostato su **Nessuno**, il contenuto del campo **Valore riga** non verrà calcolato.|  
|**Descrizione testo** | Il contenuto del campo **Valore riga** è impostato su zero.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes" />Per aggiungere uno sconto contrattuale alle offerte di contratto di assistenza
È possibile aggiungere sconti contrattuali relativi all'assistenza in offerte di contratto e in contratti di assistenza. Tali sconti possono essere applicati ai pezzi di ricambio in gruppi specifici di articoli in assistenza, alle ore delle risorse per le risorse che si trovano in particolari gruppi di risorse e a particolari costi di assistenza.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Offerte contratto assistenza**, quindi scegli il collegamento correlato.  
2. Scegliere l'offerta per cui aggiungere sconti.  
3. Scegliere l'azione **Sconti assistenza**. Verrà visualizzata la pagina **Sconti contratto/assistenza**.  
4. Fare clic sull'azione **Nuovo** per creare un nuovo sconto contrattuale.  
5. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Per aggiungere sconti contrattuali direttamente a un contratto di assistenza, eseguire operazioni analoghe nella pagina **Contratto assistenza**.  

## <a name="to-change-the-owner-of-a-service-contract" />Per modificare l'intestatario di un contratto di assistenza
Può essere necessario modificare l'intestatario di un contratto di assistenza. Se un articolo in assistenza di un contratto di assistenza è registrato in contratti multipli non annullati intestati allo stesso cliente, verrà automaticamente aggiornato l'intestatario di tutti i contratti di assistenza che includono questo articolo, così come di tutti gli altri articoli in assistenza inclusi in tali contratti.  

> [!NOTE]  
>  In questo caso, vengono presi in considerazione solo i contratti non annullati. Lo stato delle offerte di contratto non viene tenuto in considerazione.  

> [!IMPORTANT]  
>  Articoli in assistenza e contratti possono essere correlati. La modifica dell'intestatario di un contratto di assistenza può avere effetto su queste correlazioni.  
>   
>  Ad esempio, si supponga che l'articolo in assistenza Nr. 8 sia incluso nei contratti CA00003 e CA00015. Il contratto CA00015 contiene anche l'articolo in assistenza Nr. 15, che rientra altresì nel contratto CA00080. In questo caso, verrà cambiato l'intestatario di tutti e tre i contratti e gli articoli in assistenza.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza**, quindi scegli il collegamento correlato. Aprire il contratto di assistenza rilevante di cui si desidera modificare l'intestatario.  
2. Scegliere l'azione **Apri contratto** per aprire il contratto per la modifica.  
3. Scegliere l'azione **Cambia cliente**. Verrà visualizzata la pagina **Cambia cliente nel contratto**.  
4. Nei campi **Nr. contratto** e **Nr. articolo in assistenza** sono indicati i numeri del contratto e dell'articolo in assistenza intestati al cliente selezionato. Se al cliente sono intestati più contratti in cui sono inclusi più articoli in assistenza, il valore di questi campi sarà **Multiplo**. Per visualizzare la lista dei contratti o degli articoli in assistenza correlati, selezionare i valori di questi campi.  
5. Nel campo **Nuovo nr. cliente** scegliere il nuovo cliente.  
6. Nel campo **Nuovo spedire a - Codice** selezionare l'indirizzo.  
7. Scegliere il pulsante **OK** per modificare il cliente e il codice di spedizione dei contratti di assistenza.  
8. Scegliere l'azione **Blocca contratto** per bloccare il contratto e garantire che le modifiche vengano applicate ai contratti.  

## <a name="to-update-a-service-contract-price" />Per aggiornare un prezzo del contratto di assistenza
È possibile aggiornare i prezzi nei contratti di assistenza indicando una percentuale di aggiornamento del prezzo.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Aggiorna prezzi contratti assistenza**, quindi seleziona il collegamento correlato.
2. Scegliere il contratto di assistenza.  
3. Immettere una data nel campo **Aggiorna alla data**. Il processo batch aggiornerà i prezzi dei contratti con le date di aggiornamento dei prezzi successive in questa data o precedentemente ad essa.  
4. Nel campo **Aggiornamento prezzo %** immettere la percentuale con cui si intendono aggiornare i prezzi.  
5. Nel campo **Azione** selezionare **Varia prezzi contratti**.  

## <a name="to-post-prepaid-contract-entries" />Per registrare movimenti di contratto prepagati
Se si utilizzano contratti di assistenza prepagati, occorre registrare regolarmente i movimenti dei contratti prepagati, trasferendo quindi i pagamenti prepagati dai conti contrattuali prepagati a conti contrattuali normali.  

Prima di registrare movimenti di contratti prepagati, occorre specificare una numerazione nel campo **Nr. Reg. Giroconto Prepagato** della pagina **Setup Gest. Assist**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra mov. contratti prepagati**, quindi seleziona il collegamento correlato.  
2. Immettere una data nel campo **Registra fino alla data**. Il processo batch registrerà i movimenti contabili di assistenza prepagati con date di registrazione fino a tale data.  
4. Nel campo **Data di Registrazione** immettere la data che si intende utilizzare come data di registrazione nella riga di registrazioni COGE.  
5. Nel campo **Azione** scegliere **Giroconto Trans. Contr. Prepagati**.  
6. Scegliere **OK** per registrare i movimenti.

## <a name="changing-the-service-contract-status" />Modifica dello stato del contratto di assistenza
Dopo la firma del contratto di assistenza, il valore del campo **Modifica stato** viene automaticamente impostato su **Bloccato**. Se si desidera modificare le informazioni nel contratto o nell'offerta di contratto di assistenza, è innanzitutto necessario modificare lo stato del contratto o dell'offerta da **Bloccato** ad **Aperto**. Si noti che non è possibile creare fatture di assistenza per il contratto di assistenza se lo stato è **Aperto**. Dopo la modifica del contratto o dell'offerta di contratto, sarà necessario ripristinare lo stato **Bloccato** per consentire la creazione di fatture di assistenza e di movimenti contabili per il contratto di assistenza, includendo le modifiche apportate.  

> [!NOTE]  
>  Il campo **Modifica stato** non è correlato al campo **Stato rilascio** nella testata dell'ordine di assistenza, che determina la gestione della warehouse degli articoli in assistenza.  

## <a name="to-cancel-a-service-contract" />Per annullare un contratto di assistenza
Può essere necessario annullare un contratto di assistenza alla scadenza di quest'ultimo o per volontà della società o del cliente.  

> [!NOTE]  
>  Non è possibile riaprire un contratto dopo che è stato annullato.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza**, quindi scegli il collegamento correlato.  
2. Aprire il contratto di assistenza da annullare.  
3. Scegliere l'azione **Apri contratto** per aprire il contratto di assistenza per la modifica.  
4. Nel campo **Codice causa annullamento** scegli il codice causa specifico. Per aggiungere ulteriori codici causale, scegliere l'azione **Avanzato**.  

     Se la casella di controllo **Usa causale cancellaz. contrat.** della pagina **Setup gest. assist.** è selezionata, per annullare un contratto sarà necessario specificare un codice causale.  

5. Nel campo **Stato** selezionare **Annullato**.  
6. Se al contratto sono associate fatture non registrate, note di credito o movimenti prepagati aperti, verrà visualizzato un messaggio di conferma. Nella finestra del messaggio scegliere **No** per tornare al contratto e registrare i documenti oppure scegliere **Sì** per procedere all'annullamento.  

## <a name="filing-a-service-contract-or-contract-quote" />Archiviazione di un contratto di assistenza o un'offerta di contratto di assistenza
È possibile archiviare contratti di assistenza e offerte di contratto in qualsiasi momento per registrare e memorizzare una copia del contratto o dell'offerta di contratto nel programma. In [!INCLUDE[prod_short](includes/prod_short.md)] i contratti di assistenza vengono archiviati automaticamente quando le offerte di contratto vengono convertite in contratti di assistenza oppure quando i contratti di assistenza vengono eliminati. È possibile archiviare un contratto o un'offerta scegliendo l'azione **Archivia contratto** nelle pagine **Contratti assistenza** o **Offerte contratto assistenza**. Se si desidera visualizzare i contratti archiviati delle offerte cercando **Contratti archiviati**.

## <a name="see-also" />Vedi anche
[Impostare i contratti di assistenza](service-how-setup-service-contracts.md)  
[Gestione assistenza](service-service.md)  
[Convertire i contratti di assistenza che includono importi IVA](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
