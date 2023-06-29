---
title: Definire la modalità di scambio elettronico dei dati
description: 'Definisci come Business Central scambia i dati con file esterni come documenti elettronici, dati bancari, cataloghi di articoli e altro ancora.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="set-up-data-exchange-definitions"></a><a name="set-up-data-exchange-definitions"></a>Impostare le definizioni di scambio dati

Puoi impostare [!INCLUDE[prod_short](includes/prod_short.md)] per scambiare i dati di tabelle specifiche con i dati di file esterni. Ad esempio per inviare e ricevere documenti elettronici, importare ed esportare dati bancari o altri dati, come buste paga e cataloghi di articoli. Per ulteriori informazioni, vedi [Scambio di dati in modalità elettronica](across-data-exchange.md).  

Per creare una definizione di scambio di dati per un file o flusso di dati, è possibile utilizzare lo schema XML correlato per definire gli elementi dati da includere nella Scheda dettaglio **Definizioni colonne**. Vedere il passaggio 6 nella sezione [Per descrivere la formattazione di righe e colonne nel file](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Per ulteriori informazioni, vedi [Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Generalmente le definizioni di scambio di dati vengono impostate nella pagina **Definizione scambio di dati**. Tuttavia, per aggiornare i tassi di cambio valuta, è più veloce utilizzare un servizio di cambio valuta. Per ulteriori informazioni, vedi [Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Se il file in fase di conversione è in formato XML, il termine *"colonna"* in questo argomento deve essere interpretato come un *"elemento XML contenente dati"*.  

In questo articolo sono incluse le seguenti procedure:  

* Creare la definizione di scambio di dati.
* Esportare una definizione di scambio di dati come file XML per l'utilizzo da parte di altri utenti.
* Importare un file XML per una definizione di scambio di dati esistente.

## <a name="create-a-data-exchange-definition"></a><a name="create-a-data-exchange-definition"></a>Creare la definizione di scambio di dati

La creazione di una definizione di scambio di dati include due task:  

1. Nella pagina **Definizione di scambio dati** descrivere la formattazione delle righe e delle colonne del file. Ulteriori informazioni nella sezione [Per descrivere la formattazione di righe e colonne nel file](#formatlinescolumns).  
2. Nella pagina **Mapping scambio dati** eseguire il mapping delle colonne nel file di dati ai campi in [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni nella sezione [Per eseguire il mapping delle colonne del file di dati nei campi in [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name=formatlinescolumns></a>Per descrivere la formattazione di righe e colonne nel file

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti le **definizioni di scambio dati**, e scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Nella Scheda dettaglio **Generale** descrivere la definizione di scambio di dati e il tipo di file di dati compilando i campi come descritto nella tabella seguente.  

    |Campo|Definizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice**|Immettere un codice per identificare la definizione di scambio di dati.|  
    |**Nome**|Immettere un nome per la definizione di scambio di dati.|  
    |**Tipo di file**|Specifica il tipo di file per il quale viene utilizzata la definizione di scambio di dati. È possibile scegliere tra quattro tipi di file:<br /><br /> -   **XML**: stringhe sovrapposte di contenuto e di markup circondate da tag che indicano funzione.<br />-   **Testo variabile**: I record hanno una lunghezza variabile e sono separati da un carattere, ad esempio una virgola o un punto e virgola, noto anche come *file delimitato*.<br />-   **Testo fisso**: i record hanno la stessa lunghezza, si utilizzano i caratteri riempimento e ogni record è in una riga separata, noto anche come *file a larghezza fissa*.<br />- **Json**: stringhe sovrapposte di contenuto in JavaScript.|  
    |**Tipo**|Specificare il tipo di attività commerciale per cui viene utilizzata la definizione di scambio di dati, ad esempio **Esportazione pagamento**.|  
    |**Codeunit per la gestione dati**|Specificare la codeunit che trasferisce i dati dentro e fuori dalle tabelle in [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit per convalida**|Specificare la codeunit che viene utilizzata per convalidare i dati rispetto alle regole commerciali predefinite.|  
    |**Codeunit per lettura/scrittura**|Specificare la codeunit che elabora i dati importati prima di eseguire il mapping e i dati esportati dopo avere eseguito il mapping.|  
    |**Lettura/Scrittura XMLport**|Specifica l'oggetto XMLport attraverso cui un servizio o un file di dati importato entra nel sistema prima della mappatura e tramite il quale i dati esportati escono dal sistema quando vengono scritti in un servizio o un file di dati dopo la mappatura.|  
    |**Codeunit per la gestione dati est.**|Specificare la codeunit che trasferisce i dati esterni dentro e fuori dal framework di scambio dati.|  
    |**Codeunit per feedback utente**|Specificare la codeunit che esegue varie pulizie dopo il mapping, ad esempio contrassegna le righe come esportate ed elimina i record temporanei.|  
    |**Codifica file**|Specificare la codifica del file. **Nota:** il campo è valido solo per l'importazione.|  
    |**Separatore colonna**|Specificare in che modo sono separate le colonne nel file di dati, se il file è di tipo **Variable Text**.|  
    |**Righe intestazione**|Specificare il numero di righe di intestazione esistenti nel file.<br /><br /> Con questa impostazione si garantisce che i dati dell'intestazione non vengano importati. **Nota:** il campo è valido solo per l'importazione.|  
    |**Tag intestazione**|Se la riga dell'intestazione è presente in diverse posizioni nel file, immettere il testo della prima colonna nella riga dell'intestazione.<br /><br /> Con questa opzione si garantisce che i dati dell'intestazione non vengano importati. **Nota:** il campo è valido solo per l'importazione.|  
    |**Tag piè di pagina**|Se la riga del piè di pagina è presente in diverse posizioni nel file, immettere il testo della prima colonna nella riga del piè di pagina.<br /><br /> Con questa opzione si garantisce che i dati del piè di pagina non vengano importati. **Nota:** il campo è valido solo per l'importazione.|  

   > [!TIP]
   > Per visualizzare quali codeunit Microsoft utilizza nelle definizioni esistenti nel prodotto standard, esamina i tre campi **Codeunit** della pagina **Mapping campi** sotto la scheda dettaglio **Generale** per ogni definizione.  

4. Nella Scheda dettaglio **Definizioni righe** descrivere la formattazione delle righe nel file di dati compilando i campi come indicato nella tabella seguente.  

    > [!NOTE]  
    > Per l'importazione degli estratti conto bancari, è possibile creare una sola riga per il singolo formato di file di estratto conto bancario che si desidera importare.  
    >
    > Per l'esportazione di pagamenti, è possibile creare una riga per ogni tipo di pagamento che si desidera esportare. In questo caso, nella Scheda dettaglio **Definizioni colonne** vengono visualizzate colonne differenti per ogni tipo di pagamento.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Tipo riga**|Specifica il tipo della riga nel file.|  
    |**Codice**|Immettere un codice per identificare la riga nel file.|  
    |**Nome**|Immettere un nome che descrive la riga nel file.|  
    |**Conteggio colonne**|Specifica di quante colonne è composta la riga nel file di dati. **Nota:** il campo è valido solo per l'importazione.|  
    |**Tag riga dati**|Specificare la posizione nello Schema XML correlato dell'elemento che rappresenta il movimento principale del file di dati. **Nota:** il campo è valido solo per l'importazione.|  
    |**Spazio dei nomi**|Specificare lo spazio dei nomi che è previsto nel file, per consentire la convalida dello spazio dei nomi. È possibile lasciare questo campo vuoto se non si desidera abilitare la convalida dello spazio dei nomi.|  
    |**Codice padre**|Specifica l'elemento padre della riga indicato nel campo **Codice**, nei casi in cui il setup dello scambio dati riguardi file con elementi padre e figlio, come la testata e le righe di un documento.

5. Ripetere il passaggio 4 per creare una riga per ogni tipo di dati del file che si desidera esportare.  

     Continuare a descrivere la formattazione delle colonne nel file di dati compilando i campi nella Scheda dettaglio **Definizioni colonne** come indicato nella tabella seguente. È possibile utilizzare il file della struttura, ad esempio un file .xsd, affinché, tramite il file, la Scheda dettaglio venga precompilata con gli articoli corrispondenti. Per ulteriori informazioni, vedi [Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Nella Scheda dettaglio **Definizioni colonne** scegli l'azione **Ottieni struttura file**.  
7. Nella pagina **Ottieni struttura file** seleziona il file della struttura correlato, quindi scegli **OK**. Le righe nella Scheda dettaglio **Definizioni colonne** vengono compilate in base alla struttura del file di dati.  
8. Nella scheda dettaglio **Definizioni colonne** modificare o compilare i campi come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nr. colonna**|Specifica il numero che corrisponde alla posizione della colonna nella riga del file.<br /><br /> Per i file XML, specificare il numero che riflette il tipo di elemento nel file contenente i dati.|  
    |**Nome**|Specificare il nome della colonna.<br /><br /> Per i file XML, specificare il markup che contrassegna i dati da scambiare.|  
    |**Tipo di dati**|Specificare se i dati da scambiare sono di tipo **Testo**, **Data** o **Decimale**.|  
    |**Formato dati**|Specificare il formato dei dati, se disponibile. Ad esempio, **gg-MM-aaaa** se il tipo di dati è **Data**. **Nota:** per l'esportazione specifica il formato dati in base a [!INCLUDE[prod_short](includes/prod_short.md)]. Per l'importazione specificare il formato dati in base a .NET Framework. Per altre informazioni, vedi [Stringhe di formato standard della data e dell'ora](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Impostazioni cultura formattazione dati**|Specifica il formato dei dati regionale, se disponibile. Ad esempio, **en-US** se il tipo di dati è **Decimale** per garantire che la virgola viene utilizzata come il separatore .000, in base al formato degli Stati Uniti. Per altre informazioni, vedi [Stringhe di formato standard della data e dell'ora](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Nota:** il campo è valido solo per l'importazione.|  
    |**Lunghezza**|Specificare la lunghezza della riga a larghezza fissa che include la colonna se il file di dati è di tipo **Fixed Text**.|  
    |**descrizione**|Specifica una descrizione della colonna a scopo informativo.|  
    |**Percorso**|Specificare la posizione dell'elemento nello Schema XML correlato.|  
    |**Identificatore segno negativo**|Immettere il valore utilizzato nel file di dati per identificare gli importi negativi nei file di dati che non possono contenere segni negativi. Questo identificatore viene utilizzato per stornare gli importi identificati in segni negativi durante l'importazione. **Nota:** il campo è valido solo per l'importazione.|  
    |**Costante**|Specificare tutti i dati che si desidera esportare in questa colonna, ad esempio le informazioni aggiuntive sul tipo di pagamento. **Nota:** il campo è valido solo per l'esportazione.|  
    |**Riempimento testo richiesto**|Specifica che i dati devono includere la spaziatura del testo.|  
    |**Carattere riempimento**|Specifica il carattere di riempimento del testo.|  
    |**Giustificazione**|Specifica se la giustificazione della colonna è a destra o a sinistra.|  

9. Ripetere il passaggio 8 per ogni colonna o elemento XML del file di dati che dispone di dati che si desidera scambiare con [!INCLUDE[prod_short](includes/prod_short.md)].  

Il passaggio successivo nella creazione di una definizione di scambio dati consiste nel decidere tra quali colonne o elementi XML nel file di dati e quali campi in [!INCLUDE[prod_short](includes/prod_short.md)] si desidera eseguire il mapping.  

> [!NOTE]  
> Il mapping specifico dipende dallo scopo aziendale del file di dati da sostituire e dalle variazioni locali. Anche lo standard bancario SEPA include variazioni locali. [!INCLUDE[prod_short](includes/prod_short.md)] supporta l'importazione dei file di rendiconto bancario SEPA CAMT come funzionalità predefinita. Questa è rappresentata dal codice del record della definizione di scambio dati **SEPA CAMT** nella pagina **Definizioni scambio di dati**. Per informazioni sul mapping dei file specifico del supporto SEPA CAMT, vedere [Mapping dei campi durante l'importazione dei file SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name=mapfields></a>Per eseguire il mapping delle colonne del file di dati nei campi in [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> A volte i valori nei campi che si desidera mappare sono diversi. Ad esempio, in un'app aziendale il codice della lingua per gli Stati Uniti è "U.S.", ma in un'altra è "US". Ciò significa che è necessario trasformare il valore quando si scambiano i dati. Ciò accade attraverso le regole di trasformazione definite per i campi. Per ulteriori informazioni, vedi [Regole di trasformazione](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

A partire dal secondo ciclo di rilascio del 2022, puoi anche raggruppare in base a qualsiasi campo, utilizzare l'indice chiave per ordinare i risultati e i nuovi tipi di trasformazione **Arrotondamento** e **Ricerca campo**.

1. Nella Scheda dettaglio **Definizioni righe** seleziona le righe per le quali vuoi eseguire il mapping tra colonne e campi, quindi scegli **Mapping campi**. Verrà aperta la pagina **Mapping scambio dati**.  
2. Nella Scheda dettaglio **Generale** specificare l'impostazione del mapping compilando i campi come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**ID tabella**|Specificare la tabella che utilizza i campi verso i quali o dai quali vengono scambiati i dati in base al mapping.|  
    |**Utilizza come tabella intermedia**|Specifica se la tabella che si seleziona nel campo **ID tabella** è una tabella intermedia nella quale vengono memorizzati i dati importati prima che ne venga eseguita la mappatura alla tabella di destinazione.<br /><br /> Generalmente, si utilizza una tabella intermedia quando la definizione di scambio di dati viene utilizzata per importare e convertire documenti elettronici, ad esempio fatture del fornitore in fatture di acquisto in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Scambio di dati in modalità elettronica](across-data-exchange.md).|  
    |**Nome**|Immettere un nome per l'impostazione del mapping.|  
    |**Indice chiave**|Specificare l'indice della chiave per ordinare i record di origine prima dell'esportazione.|
    |**Codeunit pre-mappatura**|Specificare la codeunit che prepara il mapping tra i campi in [!INCLUDE[prod_short](includes/prod_short.md)] e i dati esterni.|  
    |**Codeunit mapping**|Specificare la codeunit che viene utilizzata per eseguire il mapping tra le colonne o gli elementi dati XML specificati e i campi in [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit post-mappatura**|Specificare la codeunit che completa il mapping tra i campi in [!INCLUDE[prod_short](includes/prod_short.md)] e i dati esterni. **Nota:** se si utilizza la funzionalità dell'estensione AMC Banking 365 Fundamentals, la codeunit converte i dati esportati da [!INCLUDE[prod_short](includes/prod_short.md)] in formato generico pronto per l'esportazione. Per l'importazione, la codeunit converte i dati esterni in un formato pronto per l'importazione in [!INCLUDE[prod_short](includes/prod_short.md)].|
3. Nella scheda dettaglio **Mapping campi** specifica quali colonne vengono mappate a quali campi in [!INCLUDE[prod_short](includes/prod_short.md)] compilando i campi come descritto nelle tabelle seguenti, a seconda se il campo **Utilizza come tabella intermedia** sia stato abilitato o meno.  
   * Con l'interruttore **Utilizza come tabella intermedia** disattivato:

     |Campo|Descrizione|  
     |--------------------------------- |---------------------------------------|  
     |**Nr. colonna**|Specificare la colonna nel file di dati per la quale si desidera definire una mappa.<br /><br /> È possibile selezionare solo le colonne rappresentate da righe nella Scheda dettaglio **Definizioni colonne** nella pagina **Definizione scambio di dati**.|
     |**Didascalia colonna**|Specifica la didascalia della colonna nel file esterno della quale viene eseguita la mappatura al campo nel campo **ID tabella di destinazione** quando utilizzi una tabella intermedia per l'importazione dei dati.|
     |**ID campo**|Specificare il campo al quale viene mappata la colonna nel campo **Nr. colonna** .<br /><br /> È possibile effettuare le selezioni solo da campi che sono presenti nella tabella specificata nel campo **ID tabella** della Scheda dettaglio **Generale**.|
     |**Didascalia campo**|Specifica la didascalia del campo nel file esterno di cui viene eseguita la mappatura al campo nel campo **ID tabella di destinazione** quando utilizzi una tabella intermedia per l'importazione dei dati.|
     |**Opzionale**|Specificare se la mappa deve essere ignorata se il campo è vuoto. Se non selezioni questa opzione, si verificherà un errore di esportazione se il campo è vuoto.|  
     |**Regola di trasformazione**|Specifica la regola che trasforma il testo importato in un valore supportato prima di poterne eseguire il mapping a un campo specificato. Quando scegli un valore in questo campo, lo stesso valore viene inserito nel campo **Regola di trasformazione** nella tabella **Buf. mapping campo scambio dati** e viceversa. Vedi la sezione successiva per ulteriori informazioni sulle regole di trasformazione disponibili che possono essere applicate.|
     |**Sovrascrivi valore**|Specifica che il valore corrente verrà sovrascritto da un nuovo valore.|
     |**Priorità**|Specifica l'ordine in cui devono essere elaborate le mappature dei campi. La mappatura del campo con il numero di priorità più alto verrà elaborata per prima.|
     |**Moltiplicatore**|Specifica un moltiplicatore da applicare ai dati numerici, inclusi i valori negativi.|

   * Con l'interruttore **Utilizza come tabella intermedia** abilitato:

     |Campo|Descrizione|  
     |---------------------------------|---------------------------------------|  
     |**Nr. colonna**|Specifica la colonna nel file di dati per la quale vuoi definire una mappa.<br /><br /> È possibile selezionare solo le colonne rappresentate da righe nella Scheda dettaglio **Definizioni colonne** nella pagina **Definizione scambio di dati**.|
     |**Didascalia colonna**|Specifica la didascalia della colonna nel file esterno della quale viene eseguita la mappatura al campo nel campo **ID tabella di destinazione** quando utilizzi una tabella intermedia per l'importazione dei dati.|
     |**ID tabella di destinazione**|Specifica la tabella alla quale viene eseguita la mappatura del valore del campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|
     |**Didascalia tabella**|Specifica il nome della tabella nel campo **ID tabella di destinazione**, che è la tabella alla quale viene eseguita la mappatura del valore nel campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|
     |**ID campo di destinazione**|Specifica il campo nella tabella di destinazione al quale viene eseguita la mappatura del valore nel campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|
     |**Didascalia campo**|Specifica il nome del campo nella tabella di destinazione al quale viene eseguita la mappatura del valore nel campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|
     |**Solo convalida**|Specifica che la mappa elemento-campo non viene utilizzata per convertire i dati, ma solo per convalidare i dati.|
     |**Regola di trasformazione**|Specifica la regola che trasforma il testo importato in un valore supportato prima di poterne eseguire il mapping a un campo specificato. Quando scegli un valore in questo campo, lo stesso valore viene inserito nel campo **Regola di trasformazione** nella tabella **Buf. mapping campo scambio dati** e viceversa. Vedi la sezione successiva per ulteriori informazioni sulle regole di trasformazione disponibili che possono essere applicate.|
     |**Priorità**|Specifica l'ordine in cui devono essere elaborate le mappature dei campi. La mappatura del campo con il numero di priorità più alto verrà elaborata per prima.|

4. Nella Scheda dettaglio **Raggruppamento campi**, specifica le regole che desideri utilizzare per raggruppare i tuoi campi quando crei il file compilando i campi come descritto nella tabella seguente.  

     |Campo|Descrizione|  
     |--------------------------------- |---------------------------------------|  
     |**ID campo**|Specifica il numero del campo nel file esterno che viene utilizzato per il raggruppamento e questo campo deve essere specificato dall'utente.|
     |**Didascalia campo**|Specifica la didascalia del campo nel file esterno che viene utilizzato per il raggruppamento.|

## <a name="transformation-rules"></a><a name="transformation-rules"></a>Regole di trasformazione

Se i valori nei campi che si stanno mappando differiscono tra loro, è necessario utilizzare le regole di trasformazione per le definizioni di scambio dei dati per renderle uguali. Si definiscono le regole di trasformazione per le definizioni di scambio dei dati aprendo una definizione esistente o creando una nuova definizione e quindi nella scheda dettaglio **Definizioni righe** scegliendo **Gestisci** e poi **Mapping dei campi**. Vengono fornite le regole predefinite, ma è possibile anche crearne di proprie. La tabella seguente descrive i tipi di trasformazione che è possibile eseguire.

|Opzione|Descrizione|
|---------|---------|
|**Maiuscole**|In maiuscolo tutte le lettere.|
|**Minuscole**|Tutte le lettere minuscole.|
|**Ortografia titolo**|In maiuscolo la prima lettera di ogni parola.|
|**Taglia**|Rimuovere gli spazi vuoti prima e dopo il valore.|
|**Sottostringa**|Trasforma una parte specifica di un valore. Per specificare da dove iniziare la trasformazione, scegliere **Posizione iniziale** o **Testo iniziale**. La posizione iniziale è un numero che rappresenta il primo carattere da trasformare. Il testo iniziale è la lettera immediatamente prima della lettera da sostituire. Se si desidera iniziare con la prima lettera del valore, utilizzare una posizione iniziale. Per specificare dove interrompere la trasformazione, scegli **Lunghezza**, che è il numero di caratteri da sostituire, oppure **Testo finale**, che è il carattere immediatamente successivo all'ultimo carattere da trasformare.|
|**Sostituisci**|Trovare un valore e sostituirlo con un altro. La trasformazione è utile per sostituire valori semplici, come una determinata parola.|
|**Espressione regolare - Sostituisci**|Utilizzare un'espressione regolare come parte di un'operazione Trova e sostituisci. La trasformazione è utile per sostituire molteplici valori o più complessi.|
|**Rimuovi caratteri non alfanumerici**|Eliminare i caratteri che non sono lettere o numeri, come simboli o caratteri speciali.|
|**Formattazione della data**|Specificare come visualizzare le date. Ad esempio, è possibile trasformare GG-MM-AAAA in AAAA-MM-GG.|
|**Formattazione decimale**|Definire le regole per il posizionamento decimale e la precisione di arrotondamento.|
|**Espressione regolare - Corrispondenza**|Utilizzare un'espressione regolare per trovare uno o più valori. Questa regola è simile alle opzioni **Sottostringa** e **Espressione regolare - Sostituisci**.|
|**Personalizzato**|Questa regola di trasformazione è un'opzione avanzata che richiede l'assistenza di uno sviluppatore. Abilita un evento di integrazione a cui è possibile iscriversi se vuoi utilizzare il tuo codice di trasformazione. Se sei uno sviluppatore e desideri utilizzare questa opzione, consulta la sezione seguente.|
|**Formattazione di data e ora**|Definisci come visualizzare la data corrente e l'ora del giorno.|
|**Ricerca campo**|Usa campi di tabelle diverse. Per utilizzarlo, è necessario seguire alcune regole. Per prima cosa, usa **ID tabella** per specificare l'ID della tabella che contiene il record per la ricerca del campo. Nel campo **ID campo di origine**, specifica l'ID del campo che contiene il record per la ricerca del campo. Infine, nel campo **ID campo di destinazione**, specifica l'ID del campo per trovare il record per la ricerca del campo. Facoltativamente, utilizza il campo **Regola ricerca campo** per specificare il tipo di ricerca del campo. Per il campo **Destinazione**, viene utilizzato il valore **ID campo di destinazione**, anche se è vuoto. Per il campo **Originale se la destinazione è vuota**, il valore originale viene utilizzato se la destinazione è vuota.|
|**Arrotonda**|Arrotonda il valore in questo campo utilizzando alcune regole aggiuntive. Innanzitutto, nel campo **Precisione**, specifica una precisione di arrotondamento. Successivamente, nel campo **Direzione**, specifica la direzione di arrotondamento.|

> [!NOTE]  
> Per ulteriori informazioni sulla formattazione di data e ora, vedi [Stringhe di formato di data e ora standard](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### <a name="tip-for-developers-example-of-the-custom-option"></a><a name="tip-for-developers-example-of-the-custom-option"></a>Suggerimento per gli sviluppatori: esempio dell'opzione Personalizzato

L'esempio seguente mostra come implementare il proprio codice di trasformazione.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Dopo aver definito le regole, è possibile verificarle. Nella scheda dettaglio **Test**, immetti un valore di esempio da trasformare, quindi controlla i risultati scegliendo **Aggiorna**.

## <a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a><a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Esportare una definizione di scambio di dati come file XML per l'utilizzo da parte di altri utenti

Dopo aver creato la definizione di scambio di dati per un file di dati specifico, è possibile esportarla come file XML che può essere importato. Questa attività è descritta nella procedura seguente.  

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti le **definizioni di scambio dati**, e scegli il collegamento correlato.  
2. Selezionare la definizione di scambi di dati che si desidera esportare.  
3. Scegliere l'azione **Esporta definizione scambio dati**.  
4. Salvare il file XML che rappresenta la definizione di scambio di dati in un'ubicazione appropriata.  

    Se è già stata creata una definizione di scambio di dati, occorre solo importare il file XML nel framework di scambio di dati. Questa attività è descritta nella procedura seguente.  

## <a name="import-an-existing-data-exchange-definition"></a><a name="import-an-existing-data-exchange-definition"></a>Importare una definizione di scambio di dati esistente

1. Salvare il file XML che rappresenta la definizione di scambio di dati in un'ubicazione appropriata.  
2. Scegli la ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti le **definizioni di scambio dati**, e scegli il collegamento correlato.  
3. Scegliere l'azione **Importa definizione scambio dati**.  
4. Scegliere il file salvato nel passaggio 1.  

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Impostare lo scambio di dati](across-set-up-data-exchange.md)  
[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
