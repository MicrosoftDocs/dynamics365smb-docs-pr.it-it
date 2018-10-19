---
title: Eseguire la migrazione dei dati dei clienti | Documenti Microsoft
description: "È possibile eseguire la migrazione dei dati dei clienti esistenti da un sistema ERP esistente a Business Central utilizzando RapidStart Services. È possibile utilizzare i file Excel in formato xlsx come vettore dati. È inoltre possibile spostare manualmente i dati immettendoli direttamente nella società."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0a1a2a100fbbd0d21c3934802b624e370592bd9e
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="migrate-customer-data"></a>Migrare i dati dei clienti
È possibile eseguire la migrazione dei dati dei clienti esistenti da un sistema ERP esistente a [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando gli strumenti di migrazione dati di RapidStart Services. È possibile utilizzare i file Excel in formato come vettore dati. È inoltre possibile spostare manualmente i dati immettendoli direttamente nella società.

La finestra **Sintesi migrazione dati** e **Foglio di lavoro configurazione** consentono di accedere alle funzioni e alle visualizzazioni per eseguire tutti i task correlati alla migrazione dei dati. È consigliabile eseguire la migrazione di una tabella alla volta, per gestire le dipendenze nei dati. La migrazione interesserà anche le tabelle di dati master, che contengono informazioni su clienti, fornitori, articoli, contatti e la contabilità generale.  

## <a name="to-import-configuration-packages"></a>Per importare pacchetti di configurazione
Quando si crea una nuova società, è possibile importare le impostazioni della nuova società. Importare le impostazioni da un file con estensione rapidstart che offre il contenuto del pacchetto in un formato compresso. Viene importato un set corrispondente di tabelle di migrazione dei dati di default. Il set di dati contiene le tabelle di dati master e le tabelle dati di setup. La prima attività nella migrazione di dati consiste nel valutare se il setup di migrazione di default soddisfa i requisiti della nuova società.

> [!NOTE]  
>  Non è possibile rinominare un file che non sia già un pacchetto di configurazione di RapidStart Services come file del pacchetto di configurazione con estensione .rapidstart e quindi provare a importarlo. Se si prova tale operazione, verrà visualizzato un messaggio di errore.  

Prima di iniziare l'operazione, assicurarsi di essere nella Gestione ruolo utente Implementatore di RapidStart Services.

> [!IMPORTANT]  
>  Durante l'esportazione e l'importazione di pacchetti di configurazione tra due database aziendali, i database devono possedere lo stesso schema al fine di garantire il corretto trasferimento di tutti i dati. Ciò significa che i database devono avere la medesima struttura di tabelle e campi, nella quale le tabelle hanno le stesse chiavi primarie e i campi hanno gli stessi ID e tipi di dati.  
>   
>  È possibile importare un pacchetto di configurazione che è stato esportato da un database con uno schema diverso dal database di destinazione. Tuttavia, i campi o le tabelle nel pacchetto di configurazione mancanti nel database di destinazione non verranno importati.
>   
> Anche le tabelle con chiavi primarie differenti e i campi che contengono tipi di dati differenti non verranno importati con successo. Ad esempio, se il pacchetto di configurazione include la tabella **Cliente 50000** con chiave primaria **Code20** e il database di destinazione del pacchetto include la tabella **Conto bancario cliente 50000** con chiave primaria **Code20 + Code 20**, i dati non verranno importati.  

1. Apre la nuova società.  
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.  
3. Scegliere l'azione **Importa pacchetto**. Passare al file del pacchetto .rapidstart che si desidera importare, quindi scegliere l'azione **Apri**. Durante l'importazione, il contenuto del pacchetto viene decompresso e viene creato il record relativo.  

    Al termine dell'importazione, è possibile visualizzare il numero di tabelle di configurazione che sono state importate nel campo **Nr. tabelle**.  
4. Per esaminare la lista delle tabelle di configurazione, scegliere l'azione **Visualizza**.  
5. Per collegare il pacchetto, scegliere l'azione **Collega pacchetto**.  

    > [!NOTE]  
    >  Le informazioni di migrazione dei dati sono basate sui modelli di configurazione, qualora se ne specifichi uno. Occorre prima aggiornare il modello per modificare la lista dei campi.  

6.  Per esaminare le selezioni del campo, selezionare una tabella e nella scheda **Righe**, scegliere l'azione **Campi**. Confrontare e analizzare il numero di campi disponibili rispetto al numero dei campi di cui sono stati collegati i dati.  

Se la selezione delle tabelle non è adeguata, è possibile creare una o più nuovi file di migrazione dei dati. Se i file sono sufficienti, è possibile passare alla migrazione dei dati utilizzando i file Excel o XML.

## <a name="to-create-a-data-migration-file"></a>Per creare un file di migrazione dati
È possibile creare nuovi file di migrazione dati e personalizzarli per supportare le proprie attività. Notare, tuttavia, che è possibile utilizzare un file solo per migrare un campo con la relativa proprietà **FieldClass** impostata su **Normale**.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetto di configurazione** e quindi scegliere il collegamento correlato.  
2. Selezionare e aprire il pacchetto da utilizzare per la migrazione dei dati, quindi scegliere l'azione **Ottieni tabelle**. Viene visualizzata la finestra **Ottieni tabelle pacchetto**.  
3. Nel campo **TableID** immettere un numero di tabella oppure selezionare una tabella dall'elenco, ad esempio, la tabella 18, **Cliente**. Il campo **Nome tabella** viene compilato automaticamente.  
4. Selezionare la nuova tabella di migrazione, quindi nella scheda **Tabelle**, scegliere l'azione **Campi**. Verrà aperta la finestra **Migration Fields**.  
5. Deselezionare la casella di controllo **Includi campo** per tutti i campi che non si desidera importare, quindi scegliere l'azione **Imposta campo Incluso** o **Cancella campo Incluso**.  

> [!IMPORTANT]  
>  Se la casella di controllo **Includi campo** è selezionata di default, quel campo fa parte della chiave primaria. Non si deve annullare la selezione, altrimenti si introdurranno errori e non sarà possibile importare il record.  
>
>  Se si include un campo con una relazione con un'altra tabella, la casella di controllo **Convalida campo** viene automaticamente selezionata. La convalida può provocare un aggiornamento di altri campi in questa e in altre tabelle e viene eseguita in base all'ordine del numero campo.  

Una nuova tabella di migrazione viene creata.  

## <a name="to-export-data-migration-files"></a>Per esportare i file di migrazione dati
Dopo avere determinato le tabelle in cui si desidera trasferire i dati relativi ai clienti, esportare i file.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.  
2. Selezionare e aprire il pacchetto che si desidera utilizzare per l'esportazione.
3. Selezionare la tabella o le tabelle da esportare, quindi scegliere l'azione **Esporta in Excel**.
4. Salvare il file Excel esportato.  
5. Ripetere questa procedura per tutte le tabelle di migrazione dati importanti. Se si selezionano più tabelle contemporaneamente, l'esportazione dei dati viene effettuata in una cartella di lavoro comune.  

Se la tabella è vuota, il file di migrazione dati risultante contiene celle vuote per i campi selezionati quando si sono scelte o create le tabelle di migrazione per la nuova società. Se nella tabella di migrazione dati selezionata sono contenuti dei dati, questa verrà esportata.  

## <a name="to-map-values-to-be-used-during-import"></a>Per mappare i valori da utilizzare durante l'importazione
Quando si collegano dati importati da Excel o da un pacchetto di RapidStart, [!INCLUDE[d365fin](includes/d365fin_md.md)] considera e gestisce la mappatura in base alle relazioni tra tabelle:  

- Se si definisce un mapping direttamente per un campo in una tabella, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo utilizza.  

- Se il campo è in relazione con un'altra tabella, [!INCLUDE[d365fin](includes/d365fin_md.md)] cerca il mapping definito per il campo della chiave primaria della tabella correlata. La tabella correlata, tuttavia, deve far parte del pacchetto di configurazione.  

- Se le informazioni di mapping sono definite in entrambe le aree, direttamente per il campo e per la chiave primaria nella relativa tabella, [!INCLUDE[d365fin](includes/d365fin_md.md)] cerca il mapping in entrambe le aree.  

- Se gli stessi mapping sono definiti direttamente per un campo e nella tabella correlata, ma hanno nuovi valori diversi, il mapping definito direttamente per il campo ha la priorità rispetto al mapping definito per la tabella a cui fa riferimento il campo.  

Nelle procedure che seguono, è consigliabile verificare in primo luogo i valori che si desidera mantenere durante il processo di migrazione. Per eseguire le procedure riportate di seguito, sono necessari i file di migrazione (.xlsx) esportati da [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere la sezione "Per esportare i file di migrazione dati".

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.
2. Aprire il pacchetto per la società in questione.  
3. Selezionare la tabella per cui si desidera mappare i valori e nella scheda **Tabelle**, scegliere l'azione **Campi**.  
4. Per ogni campo da mappare, scegliere l'azione **Mappatura**.  
5. Nel campo **Vecchio valore**, immettere il valore da modificare. Nel campo **Nuovo valore**, immettere il valore con cui modificare il valore precedente. Scegliere il pulsante **OK**.  
6. Importare i dati dei clienti. Per ulteriori informazioni, vedere la sezione "Per importare i dati dei clienti".
7. Nel campo **Nr. errori del pacchetto**, verificare se sono stati segnalati errori. Se ce ne sono, eseguire il drill-down per visualizzare gli errori. Viene visualizzata la finestra **Record pacchetto di configurazione**.
8. Scegliere l'azione **Mostra errore**. Verrà visualizzato il seguente errore: **<option> non è un'opzione valida. Le opzioni valide sono <valid option list>**. Scegliere il pulsante **OK**.  
9. Per collegare la mappatura impostata, scegliere l'azione **Collega dati**.  

### <a name="mapping-example"></a>Esempio di mappatura  
Il seguente esempio illustra come [!INCLUDE[d365fin](includes/d365fin_md.md)] implementa le definizioni di mapping.  

1. Creare una tabella di configurazione con una tabella **Agenti/Addetti acq.**. Definire un mappatura per il campo **Codice**.  
2. Aggiungere tabelle aggiuntive al pacchetto, ad esempio **Cliente** e **Fornitore**. Queste tabelle fanno entrambe riferimento alla tabella **Agenti/Addetti acq.** rispettivamente tramite i campi **Codice agente** e **Codice addetto acquisti**.  
3. Quando si collegano dati, anche la mappatura fornita per il campo **Codice** nella tabella **Agenti/Addetti acq.** verrà considerata anche durante l'elaborazione dei campi **Codice agente** e **Codice addetto acquisti**.

## <a name="to-add-additional-values-to-included365finincludesd365finmdmd"></a>Per aggiungere altri valori in [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.  
2. Selezionare la tabella per cui si desidera aggiungere ulteriori valori e nella scheda **Tabelle**, scegliere l'azione **Campi**.  
3. Per i campi per i quali si desidera che [!INCLUDE[d365fin](includes/d365fin_md.md)] consenta l'aggiunta di valori durante la migrazione, selezionare la casella di controllo **Crea codici mancanti**.  
4. Importare i dati dei clienti. Per ulteriori informazioni, vedere la sezione "Per importare i dati dei clienti".

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Per pulire ed elaborare i dati prima di collegarli
In alcuni casi, potrebbe essere necessario cancellare i dati dei clienti e elaborarli prima di collegarli al database. A tal fine, è possibile utilizzare il processo batch **Pacchetto di configurazione - Elabora** per correggere i problemi, ad esempio:  

- Convertire le date e i decimali nel formato richiesto dalle impostazioni internazionali sul computer di un utente.  
- Deselezionare spazi iniziali/finali o caratteri speciali.  

Dopo avere eseguito il processo batch, attenersi alla procedura riportata di seguito per elaborare i dati.  

1. Aprire il pacchetto di configurazione della società.  
2. Scegliere l'azione **Elabora dati**.  
3. Per collegare la mappatura impostata, scegliere l'azione **Collega dati**.

## <a name="to-migrate-customer-data"></a>Per migrare i dati dei clienti
Dopo aver esportato una tabella di migrazione, il passo successivo prevede l'immissione dei dati legacy del cliente. Per semplificare i task, è possibile avvantaggiarsi degli strumenti di modifica XML incorporati in Excel. È inoltre possibile utilizzare le funzioni incorporate di Excel per agevolare la formattazione dei dati e inserire i dati nella cella appropriata.

Per assistenza con XML, attivare la scheda **Developer** della barra multifunzione di Excel, quindi scegliere l'azione **Origine** per visualizzare lo schema XML della tabella di migrazione come rappresentato in Excel.

La procedura riportata di seguito è basata su un foglio di lavoro Excel che è stato creato per la migrazione. Per ulteriori informazioni, vedere Procedura: Esportare le tabelle di migrazione.

> [!IMPORTANT]  
> Non modificare le colonne nei fogli di lavoro Excel. Se vengono spostate, modificate o eliminate, il prospetto non può essere importato in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. In Excel aprire il file dei dati esportati. È disponibile un foglio di lavoro con il nome della tabella.
2. Rinominare Sheet1 per indicare che il prospetto verrà utilizzato per trasformare i dati. Copiare la riga di testata senza la relativa formattazione derivante dalla tabella esportata nel nuovo prospetto.
3. In un terzo prospetto copiare tutti i dati del cliente. Rinominare il foglio in "Dati legacy".
4. Creare una formula Excel per mappare i dati nel prospetto di trasformazione tra i campi del prospetto esportato e i dati legacy del cliente.
5. Dopo aver eseguito la mappatura di tutti i dati, copiare l'intervallo dei dati nel foglio di lavoro della tabella.
6. Salvare il file e assicurarsi di non modificare il tipo di file.

È ora possibile importare i file di migrazione dati che contengono i dati legacy del cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Per importare i dati dei clienti
Dopo avere immesso i dati dei clienti nei file di migrazione dati in Excel, importare i file in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Aprire la finestra **Scheda pacchetto di configurazione**.
2. Selezionare la tabella per cui si desidera importare i dati e nella scheda **Tabelle**, scegliere l'azione **Importa da Excel**.
3. Individuare e aprire il file da cui si desidera importare i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)].

I dati del file vengono importati nelle tabelle dei pacchetti di configurazione. È possibile visualizzare il numero di record che sono stati importati nel campo **Nr. record del pacchetto**. Inoltre, è possibile visualizzare il numero di errori di migrazione.

## <a name="to-validate-customer-data"></a>Per convalidare i dati dei clienti
I dati del cliente deve essere convalidati prima di applicare i record al database [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Nella maggior parte dei casi, i dati non validi non vengono creati nel database. Tuttavia, è possibile che l'applicazione talvolta sia bloccata se una tabella di migrazione importata contiene errori.  

1. Nella finestra **Sintesi migrazione**, esaminare il campo **Nr. errori migrazione** per verificare se si sono verificati errori durante l'importazione.  
2. Se esistono errori, selezionare la tabella di migrazione, quindi nella scheda **Tabelle**, selezionare l'azione **Errori**. La casella di controllo **Non valido** è selezionata per ogni record con un errore.  
3. Per esaminare gli errori, selezionare una riga, quindi scegliere l'azione **Mostra errore**.  

    Il campo **Testo errore** contiene il motivo dell'errore. Il campo **Didascalia campo** contiene la didascalia del campo che contiene l'errore.  
4.  Per correggere un errore o eseguire un aggiornamento, nella finestra **Sintesi migrazione dati**, selezionare l'azione **Record migrazione**, quindi nella finestra **Record di migrazione**, correggere il record con l'errore.  

Dopo avere apportato una correzione, il record viene rimosso dall'elenco dei record nella finestra **Errori dati migrazione**.  

È ora possibile applicare i dati del cliente al database.  

## <a name="to-apply-customer-data"></a>Per collegare i dati dei clienti
Una volta importati tutti i record di migrazione dati validi e senza errori, è possibile collegare i record al database di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Aprire la finestra **Pacchetti di configurazione**.  
2. Selezionare la tabella per il file di migrazione dei dati da collegare, quindi scegliere l'azione **Collega dati**.

Nel campo **Nr. record di database**, è possibile visualizzare il numero di record di database creati. È possibile verificare la creazione dei record corretti scegliendo il collegamento nel campo **Nr. record di database**.  

Il database della società del cliente è ora impostato e i dati di base vengono importati. I passaggi successivi del processo di implementazione sono organizzare utenti, definire processi, creare dati aggiuntivi, personalizzare i report e così via.

## <a name="see-also"></a>Vedi anche  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)

