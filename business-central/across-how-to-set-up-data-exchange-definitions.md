---
title: "Definire la modalità di scambio elettronico dei dati | Microsoft Docs"
description: "È possibile utilizzare un provider esterno di servizi OCR per convertire file PDF o di immagine in documenti elettronici."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4828da068f1e17d031300948e930c9685a2f274d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-data-exchange-definitions"></a>Impostare le definizioni di scambio dati
[!INCLUDE[d365fin](includes/d365fin_md.md)] può essere impostato in modo da scambiare i dati di tabelle specifiche con quelli di file esterni, ad esempio per inviare e ricevere documenti elettronici, importare ed esportare dati bancari o di altro tipo, come la retribuzione, i tassi di cambio delle valute e i cataloghi di articoli. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).  

Come preparazione alla creazione di una definizione di scambio di dati per un file o flusso di dati, è possibile utilizzare lo schema XML correlato per definire gli elementi dati da includere nella Scheda dettaglio **Definizioni colonne**. Vedere il passaggio 6 nella sezione "Per descrivere la formattazione di righe e colonne nel file". Per altre informazioni, vedere [Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Generalmente le definizioni di scambio di dati vengono impostate nella finestra **Definizione scambio di dati**. Tuttavia, quando si imposta una definizione di scambio dati per l'aggiornamento dei tassi di cambio delle valute, il processo viene avviato nella finestra **Scheda Setup aggiornamento tasso di cambio in valuta** semplificata.  

> [!NOTE]  
>  Se il file in fase di conversione è in formato XML, il termine *"colonna"* in questo argomento deve essere interpretato come un *"elemento XML contenente dati"*.  

In questo argomento sono incluse le seguenti procedure:  

* Per creare la definizione di scambio di dati  
* Per esportare una definizione di scambio di dati come file XML per l'utilizzo da parte di altri utenti  
* Per importare un file XML per una definizione di scambio di dati esistente  

## <a name="to-create-a-data-exchange-definition"></a>Per creare la definizione di scambio di dati  
La creazione di una definizione di scambio di dati include due task:  

1. Nella finestra **Definizione di scambio dati** descrivere la formattazione delle righe e delle colonne del file.  
2. Nella finestra **Mapping scambio dati** eseguire il mapping delle colonne nel file di dati ai campi in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

     Questa funzionalità è descritta nelle procedure seguenti.  

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Per descrivere la formattazione di righe e colonne nel file  
1. Nella casella **Cerca** immettere **Definizioni scambio dati**, quindi selezionare il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nella Scheda dettaglio **Generale** descrivere la definizione di scambio di dati e il tipo di file di dati compilando i campi come descritto nella tabella seguente.  

    |Campo|Definizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice**|Immettere un codice per identificare la definizione di scambio di dati.|  
    |**Nome**|Immettere un nome per la definizione di scambio di dati.|  
    |**Tipo di file**|Specificare il tipo di file per il quale viene utilizzata la definizione di scambio di dati. È possibile scegliere tra tre tipi di file:<br /><br /> -   **XML**: stringhe sovrapposte di contenuto e di markup circondate da tag che indicano funzione.<br />-   **Variable Text**: i record hanno lunghezza variabile e sono separati da un carattere come la virgola o il punto e virgola. Noto anche come *file delimitato*.<br />-   **Fixed Text**: i record hanno la stessa lunghezza, si utilizzano i caratteri riempimento e ogni record è in una riga separata. Noto anche come *file a larghezza fissa*.|  
    |**Tipo**|Specificare il tipo di attività commerciale per cui viene utilizzata la definizione di scambio di dati, ad esempio **Esportazione pagamento**.|  
    |**Codeunit per la gestione dati**|Specificare la codeunit che trasferisce i dati dentro e fuori dalle tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit per convalida**|Specificare la codeunit che viene utilizzata per convalidare i dati rispetto alle regole commerciali predefinite.|  
    |**Codeunit per lettura/scrittura**|Specificare la codeunit che elabora i dati importati prima di eseguire il mapping e i dati esportati dopo avere eseguito il mapping.|  
    |**Lettura/Scrittura XMLport**|Specificare l'oggetto XMLport tramite cui un file di dati importato o un servizio entra prima del mapping e tramite cui i dati esportati escono quando l'oggetto viene scritto in un file di dati o un servizio dopo il mapping.|  
    |**Codeunit per la gestione dati est.**|Specificare la codeunit che trasferisce i dati esterni dentro e fuori dal framework di scambio dati.|  
    |**Codeunit per feedback utente**|Specificare la codeunit che esegue varie pulizie dopo il mapping, ad esempio contrassegna le righe come esportate ed elimina i record temporanei.|  
    |**Codifica file**|Specificare la codifica del file. **Nota:** il campo è valido solo per l'importazione.|  
    |**Separatore colonna**|Specificare in che modo sono separate le colonne nel file di dati, se il file è di tipo **Variable Text**.|  
    |**Righe intestazione**|Specificare il numero di righe di intestazione esistenti nel file.<br /><br /> In questo modo si garantisce la non importazione dei dati dell'intestazione. **Nota:** il campo è valido solo per l'importazione.|  
    |**Tag intestazione**|Se la riga dell'intestazione è presente in diverse posizioni nel file, immettere il testo della prima colonna nella riga dell'intestazione.<br /><br /> In questo modo si garantisce la non importazione dei dati dell'intestazione. **Nota:** il campo è valido solo per l'importazione.|  
    |**Tag piè di pagina**|Se la riga del piè di pagina è presente in diverse posizioni nel file, immettere il testo della prima colonna nella riga del piè di pagina.<br /><br /> In questo modo si garantisce la non importazione dei dati del piè di pagina. **Nota:** il campo è valido solo per l'importazione.|  

4. Nella Scheda dettaglio **Definizioni righe** descrivere la formattazione delle righe nel file di dati compilando i campi come indicato nella tabella seguente.  

    > [!NOTE]  
    >  Per l'importazione degli estratti conto bancari, è possibile creare una sola riga per il singolo formato di file di estratto conto bancario che si desidera importare.  
    >   
    >  Per l'esportazione di pagamenti, è possibile creare una riga per ogni tipo di pagamento che si desidera esportare. In questo caso, nella Scheda dettaglio **Definizioni colonne** vengono visualizzate colonne differenti per ogni tipo di pagamento.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice**|Immettere un codice per identificare la riga nel file.|  
    |**Nome**|Immettere un nome che descrive la riga nel file.|  
    |**Conteggio colonne**|Specificare di quante colonne è composta la riga nel file di dati. **Nota:** il campo è valido solo per l'importazione.|  
    |**Tag riga dati**|Specificare la posizione nello Schema XML correlato dell'elemento che rappresenta il movimento principale del file di dati. **Nota:** il campo è valido solo per l'importazione.|  
    |**Spazio dei nomi**|Specificare lo spazio dei nomi che è previsto nel file, per consentire la convalida dello spazio dei nomi. È possibile lasciare questo campo vuoto se non si desidera abilitare la convalida dello spazio dei nomi.|  

5. Ripetere il passaggio 4 per creare una riga per ogni tipo di dati del file che si desidera esportare.  

     Continuare a descrivere la formattazione delle colonne nel file di dati compilando i campi nella Scheda dettaglio **Definizioni colonne** come indicato nella tabella seguente. È possibile utilizzare il file della struttura, ad esempio un file XSD, affinché, tramite il file, la Scheda dettaglio venga precompilata con gli articoli corrispondenti. Per altre informazioni, vedere [Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. Nella Scheda dettaglio **Definizioni colonne** scegliere **Ottieni struttura file**.  
7. Nella finestra **Ottieni struttura file** selezionare il file della struttura correlato, quindi scegliere il pulsante **OK**. Le righe nella Scheda dettaglio **Definizioni colonne** vengono compilate in base alla struttura del file di dati.  
8. Nella scheda dettaglio **Definizioni colonne** modificare o compilare i campi come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nr. colonna**|Specificare il numero che corrisponde alla posizione della colonna nella riga del file.<br /><br /> Per i file XML, specificare il numero che riflette il tipo di elemento nel file contenente i dati.|  
    |**Nome**|Specificare il nome della colonna.<br /><br /> Per i file XML, specificare il markup che contrassegna i dati da scambiare.|  
    |**Tipo di dati**|Specificare se i dati da scambiare sono di tipo **Testo**, **Data** o **Decimale**.|  
    |**Formato dati**|Specificare il formato dei dati, se disponibile. Ad esempio, **gg-MM-aaaa** se il tipo di dati è **Data**. **Nota:** per l'esportazione specificare il formato dati in base a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per l'importazione specificare il formato dati in base a .NET Framework. Per altre informazioni, vedere [Stringhe di formato standard della data e dell'ora](http://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Impostazioni cultura formattazione dati**|Specificare le impostazioni cultura del formato dati, se disponibile. Ad esempio, **en-US** se il tipo di dati è **Decimale** per garantire che la virgola viene utilizzata come il separatore .000, in base al formato degli Stati Uniti. Per altre informazioni, vedere [Stringhe di formato standard della data e dell'ora](http://go.microsoft.com/fwlink/?LinkID=323466). **Nota:** il campo è valido solo per l'importazione.|  
    |**Lunghezza**|Specificare la lunghezza della riga a larghezza fissa che include la colonna se il file di dati è di tipo **Fixed Text**.|  
    |**Description**|Immettere una descrizione della colonna, a scopo informativo.|  
    |**Percorso**|Specificare la posizione dell'elemento nello Schema XML correlato.|  
    |**Identificatore segno negativo**|Immettere il valore utilizzato nel file di dati per identificare gli importi negativi nei file di dati che non possono contenere segni negativi. Questo identificatore viene utilizzato per stornare gli importi identificati in segni negativi durante l'importazione. **Nota:** il campo è valido solo per l'importazione.|  
    |**Costante**|Specificare tutti i dati che si desidera esportare in questa colonna, ad esempio le informazioni aggiuntive sul tipo di pagamento. **Nota:** il campo è valido solo per l'esportazione.|  

9. Ripetere il passaggio 8 per ogni colonna o elemento XML del file di dati che dispone di dati che si desidera scambiare con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Il passaggio successivo nella creazione di una definizione di scambio dati consiste nel decidere tra quali colonne o elementi XML nel file di dati e quali campi in [!INCLUDE[d365fin](includes/d365fin_md.md)] si desidera eseguire il mapping.  

> [!NOTE]  
>  Il mapping specifico dipende dallo scopo aziendale del file di dati da sostituire e dalle variazioni locali. Anche lo standard bancario SEPA include variazioni locali. [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta l'importazione dei file di rendiconto bancario SEPA CAMT come funzionalità predefinita. Questa è rappresentata dal codice del record della definizione di scambio dati **SEPA CAMT** nella finestra **Definizioni scambio di dati**. Per informazioni sul mapping dei file specifico del supporto SEPA CAMT, vedere [Mapping dei campi durante l'importazione dei file SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Per eseguire il mapping delle colonne del file di dati nei campi in [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Nella Scheda dettaglio **Definizioni righe** selezionare le righe per le quali di desidera eseguire il mapping tra colonne e campi, quindi scegliere **Mapping campi**. Verrà aperta la finestra **Mapping scambio dati**.  
2. Nella Scheda dettaglio **Generale** specificare l'impostazione del mapping compilando i campi come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**ID tabella**|Specificare la tabella che utilizza i campi verso i quali o dai quali vengono scambiati i dati in base al mapping.|  
    |**Utilizza come tabella intermedia**|Specifica se la tabella che si seleziona nel campo **ID tabella** è una tabella intermedia nella quale vengono memorizzati i dati importati prima che ne venga eseguita la mappatura alla tabella di destinazione.<br /><br /> Generalmente, si utilizza una tabella intermedia quando la definizione di scambio di dati viene utilizzata per importare e convertire documenti elettronici, ad esempio fatture del fornitore in fatture di acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).|  
    |**Nome**|Immettere un nome per l'impostazione del mapping.|  
    |**Codeunit pre-mappatura**|Specificare la codeunit che prepara il mapping tra i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)] e i dati esterni.|  
    |**Codeunit mapping**|Specificare la codeunit che viene utilizzata per eseguire il mapping tra le colonne o gli elementi dati XML specificati e i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit post-mappatura**|Specificare la codeunit che completa il mapping tra i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)] e i dati esterni. **Nota:** se si utilizza la funzionalità del servizio di conversione di dati bancari, la codeunit converte i dati esportati da [!INCLUDE[d365fin](includes/d365fin_md.md)] in formato generico pronto per l'esportazione. Per l'importazione, la codeunit converte i dati esterni in un formato pronto per l'importazione in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  Nella Scheda dettaglio **Mapping campi** specificare il mapping tra le colonne e i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)] compilando i campi come indicato nella tabella che segue.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nr. colonna**|Specificare la colonna nel file di dati per la quale si desidera definire una mappa.<br /><br /> È possibile selezionare solo le colonne rappresentate da righe nella Scheda dettaglio **Definizioni colonne** nella finestra **Definizione scambio di dati**.|  
    |**ID campo**|Specificare il campo al quale viene mappata la colonna nel campo **Nr. colonna** .<br /><br /> È possibile effettuare le selezioni solo da campi che sono presenti nella tabella specificata nel campo **Tabella** della Scheda dettaglio **Generale**.|  
    |**Opzionale**|Specificare che la mappa verrà ignorata se il campo è vuoto. **Nota:** se non si seleziona questa casella di controllo, si verifica un errore di esportazione se il campo è vuoto. **Nota:** il campo è valido solo per l'esportazione.|  
    |**ID tabella di destinazione**|Visibile solo quando la casella di controllo **Utilizza come tabella intermedia** è selezionata.<br /><br /> Specifica la tabella alla quale viene eseguita la mappatura del valore del campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|  
    |**Didascalia tabella di destinazione**|Visibile solo quando la casella di controllo **Utilizza come tabella intermedia** è selezionata.<br /><br /> Specifica il nome della tabella nel campo **ID tabella di destinazione**, che è la tabella alla quale viene eseguita la mappatura del valore nel campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|  
    |**ID campo di destinazione**|Visibile solo quando la casella di controllo **Utilizza come tabella intermedia** è selezionata.<br /><br /> Specifica il campo nella tabella di destinazione al quale viene eseguita la mappatura del valore nel campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|  
    |**Didascalia campo di destinazione**|Visibile solo quando la casella di controllo **Utilizza come tabella intermedia** è selezionata.<br /><br /> Specifica il nome del campo nella tabella di destinazione al quale viene eseguita la mappatura del valore nel campo **Didascalia colonna**, quando si utilizza una tabella intermedia per l'importazione dei dati.|  
    |**Opzionale**|Visibile solo quando la casella di controllo **Utilizza come tabella intermedia** è selezionata.<br /><br /> Specificare se la mappa deve essere ignorata se il campo è vuoto. Se non si seleziona questa casella di controllo, si verificherà un errore di esportazione se il campo è vuoto.|  

La definizione di scambio di dati è ora pronta per essere abilitata per gli utenti. Per altre informazioni, vedere [Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Impostare il bonifico SEPA](finance-how-to-set-up-sepa-credit-transfer.md), [Impostare gli addebiti diretti SEPA](finance-how-to-set-up-sepa-direct-debit.md) ed [Eseguire i pagamenti con servizio di conversione di dati bancari o bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

Dopo aver creato la definizione di scambio di dati per un file di dati specifico, è possibile esportarla come file XML che può essere utilizzato per abilitare rapidamente l'importazione del file di dati in questione. Questa funzionalità è descritta nella procedura seguente.  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Per esportare una definizione di scambio di dati come file XML per l'utilizzo da parte di altri utenti  
1. Nella casella **Cerca** immettere **Definizioni scambio dati**, quindi selezionare il collegamento correlato.  
2. Selezionare la definizione di scambi di dati che si desidera esportare.  
3. Scegliere l'azione **Esporta definizione scambio dati**.  
4. Salvare il file XML che rappresenta la definizione di scambio di dati in un'ubicazione appropriata.  

    Se è già stata creata una definizione di scambio di dati, occorre solo importare il file XML nel framework di scambio di dati. Questa funzionalità è descritta nella procedura seguente.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Per importare una definizione di scambio di dati esistente  
1. Salvare il file XML che rappresenta la definizione di scambio di dati in un'ubicazione appropriata.  
2. Nella casella **Cerca**, immettere **Definizioni scambio di dati**, quindi selezionare il collegamento correlato.  
3. Scegliere l'azione **Nuovo**. Verrà aperta la finestra **Definizione scambio di dati**.  
4. Scegliere l'azione **Importa definizione scambio dati**.  
5. Scegliere il file salvato nel passaggio 1.  

## <a name="see-also"></a>Vedi anche  
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Impostare un bonifico SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Impostare gli addebiti diretti SEPA](finance-how-to-set-up-sepa-direct-debit.md)  
[Eseguire i pagamenti con servizio di conversione di dati bancari o bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

