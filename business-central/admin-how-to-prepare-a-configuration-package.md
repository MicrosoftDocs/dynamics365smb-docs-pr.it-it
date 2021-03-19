---
title: Preparazione di un pacchetto di configurazione | Documenti di Microsoft
description: Informazioni su come configurare un pacchetto di configurazione RapidStart che può aiutare a creare nuove società in base ai dati esistenti.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6b8e0a46375bce9ffd22b160766925bf803025f0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378200"
---
# <a name="prepare-a-configuration-package"></a>Preparazione di un pacchetto di configurazione

Quando si configura una nuova società con un pacchetto di configurazione, le relazioni tra tabelle vengono riconosciute ed elaborate. I dati vengono importati e collegati in ordine corretto. Anche le tabelle dimensioni vengono importate se sono incluse nel pacchetti di configurazione. Per ulteriori informazioni, vedere [Per importare i dati dei clienti](admin-migrate-customer-data.md#to-import-customer-data).  

Per agevolare il cliente nell'utilizzo del pacchetto di configurazione, è possibile aggiungere un questionario o un insieme di questionari al pacchetto di configurazione. Il questionario può agevolare il cliente nella comprensione delle diverse opzioni di setup. In genere, i questionari vengono creati per le tabelle di setup principali dove un cliente può richiedere ulteriori indicazioni su come selezionare un'impostazione appropriata. Per ulteriori informazioni, vedere [Raggruppare i valori di setup del cliente](admin-gather-customer-setup-values.md).

## <a name="before-you-create-a-configuration-package"></a>Prima di creare un pacchetto di configurazione

Ci sono alcune cose da considerare prima di creare un pacchetto di configurazione perché avranno un impatto su di te o sulla capacità del tuo cliente di importarlo.  

### <a name="tables-that-contain-posted-entries"></a>Tabelle che contengono voci registrate

Non è possibile importare dati in tabelle che contengono voci registrate, come le tabelle per movimenti cliente, fornitore e contabili articoli, pertanto non è necessario includere questi dati nel pacchetto di configurazione. È possibile aggiungere voci a queste tabelle dopo aver importato il pacchetto di configurazione utilizzando le registrazioni per pubblicare le voci. Per ulteriori informazioni, vedere [Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md).

### <a name="table-names-that-contain-special-characters"></a>Nomi di tabella che contengono caratteri speciali

Prestare attenzione se si dispone di tabelle o campi con lo stesso nome temporale ma differenziati da caratteri speciali, ad esempio %, &, <, >, ( e ). Ad esempio, la tabella "XYZ" potrebbe contenere i campi "Campo 1" e "Campo 1%".

Il processore XML accetta solo alcuni caratteri speciali e rimuove quelli che non accetta. Se la rimozione di un carattere speciale, come il segno % in "Campo 1%", genera due o più tabelle o campi con lo stesso nome, si verificherà un errore durante l'esportazione o l'importazione di un pacchetto di configurazione. 

### <a name="licensing"></a>Licenze

La licenza deve includere le tabelle che si stanno aggiornando. Se non si è sicuri, consultare la pagina **Foglio di lavoro configurazione**. Se la licenza include la tabella, la la casella di controllo **Tabella con licenza** è selezionata.  

### <a name="permissions"></a>Autorizzazioni

Il processo di creazione e importazione di un pacchetto di configurazione comporta le seguenti autorizzazioni valide per tutte le tabelle nel pacchetto:  

- L'utente che esporta i dati per il pacchetto di configurazione deve avere autorizzazioni valide in **Lettura**.
- L'utente che importa il pacchetto di configurazione deve avere autorizzazioni valide in **Inserimento** e **Modifica**.

### <a name="database-schema"></a>Schema del database

Durante l'esportazione e l'importazione di pacchetti di configurazione tra due database aziendali, i database devono possedere lo stesso schema al fine di garantire il corretto trasferimento di tutti i dati. Ciò significa che i database devono avere la medesima struttura di tabelle e campi, nella quale le tabelle hanno le stesse chiavi primarie e i campi hanno gli stessi ID e tipi di dati.  

È possibile importare un pacchetto di configurazione che è stato esportato da un database con uno schema diverso dal database di destinazione. Tuttavia, i campi o le tabelle nel pacchetto di configurazione mancanti nel database di destinazione non verranno importati. Anche le tabelle con chiavi primarie differenti e i campi che contengono tipi di dati differenti non verranno importati con successo. Ad esempio, se il pacchetto di configurazione include la tabella **Cliente 50000** con chiave primaria **Code20** e il database di destinazione del pacchetto include la tabella **Conto bancario cliente 50000** con chiave primaria **Code20 + Code 20**, i dati non verranno importati.  

## <a name="to-create-a-configuration-package"></a>Per creare un pacchetto di configurazione

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi come appropriato nella Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Per escludere i questionari di configurazione, i modelli di configurazione e le tabelle del foglio di lavoro di configurazione dal pacchetto, selezionare la casella di controllo **Escludi tabelle di configurazione**. In caso contrario, tali tabelle verranno aggiunte automaticamente alla lista di tabelle del pacchetto al momento dell'esportazione del pacchetto.  
5. Scegliere l'azione **Ottieni tabelle**. Viene visualizzata la pagina con il processo batch **Ottieni tabelle pacchetto**.  
6. Selezionare il campo **Seleziona tabelle**. Verrà visualizzata la pagina **Selezione configurazione**.  
7. Scegliere l'azione **Seleziona tutto** per aggiungere tutte le tabelle al pacchetto oppure selezionare la casella di controllo **Selezionato** per ogni tabella della lista che si desidera aggiungere.
8. Scegliere il pulsante **OK**. Il conteggio delle tabelle selezionate verrà visualizzato nel campo **Seleziona tabelle**. Specificare le opzioni aggiuntive, quindi scegliere il pulsante **OK**. Le tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] vengono aggiunte alle righe della pagina **Pacchetto di configurazione**.  

    > [!NOTE]  
    >  È possibile eseguire questa operazione anche nel foglio di lavoro della configurazione. Selezionare le tabelle che si desidera includere nel pacchetto, quindi selezionare l'azione **Assegna pacchetto**.

9. Per selezionare i campi che si desidera includere da una tabella, selezionare la tabella e sulla barra degli strumenti **Righe**, scegliere l'azione **Campi**.
Specificare i campi da includere nel pacchetto. Per default, vengono inclusi tutti i campi.

    - Per selezionare solo i campi da includere, scegliere l'azione **Cancella campo Incluso**. Per aggiungere tutti i campi, scegliere l'azione **Imposta campo incluso**.  
    - Per specificare che i dati di un campo non devono essere convalidati, deselezionare la casella di controllo **Convalida campo** del campo.  

10. Determinare se sono stati introdotti errori potenziali scegliendo l'azione **Convalida pacchetto**. Questo può verificarsi nel caso in cui non vengono incluse le tabelle su cui si basa la configurazione.  
11. Scegliere il pulsante **OK**.  

Dopo aver rifinito la lista dei campi da includere in una tabella, è possibile controllare i risultati in Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Per filtrare e verificare il set di dati

1. Per filtrare un determinato set di record da includere nel pacchetto, nella scheda **Righe**, selezionare **Filtri** e specificare i valori di filtro appropriati.  
2. Nella scheda del pacchetto, nella scheda **Righe**, selezionare l'azione **Esporta in Excel**.  
3. Confermare i messaggi che consentono l'esportazione dei dati in Excel. Verrà visualizzato il file XLSX denominato. Verificare i record che sono stati esportati.  
4. Chiudere Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Per includere un modello per il collegamento a una tabella

In alcune tabelle, come quella che conterrà dati master, è possibile specificare un modello da applicare ai dati. Il modello può includere i campi richiesti che si desidera collegare a tutti i dati master e che non si desidera mai modificare. È, ad esempio, possibile creare un modello che può essere utilizzato con i dati dei clienti. Il modello può contenere tutti i campi richiesti, consentendo quindi l'importazione coerente di informazioni standardizzate. Le informazioni che non possono essere standardizzate, come la ragione sociale del cliente, vengono quindi considerate quando si effettua l'importazione dei dati dei clienti. Per ulteriori informazioni, vedere [Preparare la migrazione dei dati dei clienti con modelli](admin-use-templates-to-prepare-customer-data-for-migration.md).  

1. Nella pagina **Scheda pacchetto di configurazione**, selezionare una tabella, quindi scegliere il campo **Modello dati**. Viene visualizzata una lista dei modelli in base alla tabella.
2. Selezionare un modello e scegliere il pulsante **OK**.  

Al completamento del pacchetto, seguire la procedura seguente per salvare il pacchetto in un file. Sarà quindi possibile assegnare il pacchetto a un cliente o a un partner per essere utilizzato.

### <a name="to-save-and-export-a-configuration-package"></a>Per salvare ed esportare un pacchetto di configurazione

- Nella pagina **Scheda pacchetto di configurazione**, scegliere l'azione **Esporta pacchetto**.  

Il pacchetto viene creato in un file con estensione rapidstart, che offre il contenuto del pacchetto in un formato compresso. I questionari, i modelli di configurazione così come il foglio di lavoro configurazione vengono aggiunti al pacchetto automaticamente a meno che non si decida specificatamente di escluderli.  

È possibile salvare il file con un nome significativo, ma non è possibile modificare l'estensione del file. L'estensione del file deve essere rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Per copiare un pacchetto di configurazione

Dopo avere creato un pacchetto che soddisfa le proprie esigenze, questo può essere utilizzato come base per la creazione di pacchetti simili. Tale approccio può velocizzare l'implementazione e migliorare la ripetibilità di RapidStart Services.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.  
2. Selezionare un pacchetto dalla lista, quindi scegliere l'azione **Copia pacchetto**.  
3. Nel campo **Nuovo codice pacchetto** inserire un codice per il nuovo pacchetto.  
4. Se si desidera copiare anche i dati del database dal pacchetto esistente, selezionare la casella di controllo **Copia dati**.  
5. Scegliere il pulsante **OK**.

## <a name="to-customize-a-configuration-package"></a>Per personalizzare un pacchetto di configurazione

Utilizzare il foglio di lavoro configurazione per raccogliere e classificare le informazioni che si desidera utilizzare per configurare una nuova società e disporre le tabelle in modo logico. La formattazione del prospetto è basata su una gerarchia semplice: le aree contengono gruppi che, a loro volta, contengono tabelle. Le aree e i gruppi sono facoltativi, ma diventano necessari per attivare una panoramica del processo di configurazione nella Gestione ruolo utente di RapidStart Services.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi scegliere il collegamento correlato.  
2. Nel campo **Tipo riga**, scegliere **Area**. Nel campo **Nome** immettere un nome descrittivo.  
3. Nel campo **Tipo riga**, scegliere **Gruppo**. Nel campo **Nome** immettere un nome descrittivo.  
4. Nel campo **Tipo riga**, scegliere **Tabella**. Nel campo **ID tabella**, selezionare la tabella che si desidera includere nel prospetto.  

A questo punto è possibile assegnare le tabelle a pacchetti di configurazione specifici che sono stati creati o che si intende creare. Per ulteriori informazioni, vedere [Per assegnare una tabella a un pacchetto di configurazione](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Per utilizzare le tabelle essenziali

1. Selezionare la casella di controllo **Tabella essenziale** per indicare una tabella utilizzata di frequente durante il processo di setup di un cliente standard, ad esempio, la tabella **Conto C/G**. Quando una tabella presenta questa designazione, un cliente potrà filtrare il proprio prospetto in modo semplice per visualizzare solo la lista delle tabelle essenziali che richiedono attenzione.  
2. Scegliere l'azione **Solo elementi essenziali** per ottenere la visualizzazione filtrata. La lista delle tabelle contiene solo le tabelle per cui è stata selezionata la casella di controllo.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Per assegnare una tabella a un pacchetto di configurazione

Dopo aver definito le tabelle che si desidera gestire come parte della configurazione, è possibile assegnare le tabelle ai pacchetti di configurazione. A ciascuna tabella è possibile assegnare un solo pacchetto. Nella procedura riportata di seguito viene assegnato il pacchetto dall'interno a partire dal foglio di lavoro configurazione.  

> [!NOTE]  
> È inoltre possibile creare direttamente un pacchetto e aggiungervi tabelle. Per ulteriori informazioni, vedere [Per creare un pacchetto di configurazione](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi scegliere il collegamento correlato.
2. Nel foglio di lavoro configurazione, selezionare una riga o un gruppo di righe che si desidera assegnare a un pacchetto di configurazione, quindi scegliere l'azione **Assegna pacchetto**.  
3. Selezionare un pacchetto dalla lista o scegliere l'azione **Nuovo** per creare un nuovo pacchetto, quindi scegliere il pulsante **OK**.  

    La tabella verrà aggiunta al pacchetto, a meno che non sia già contenuta nello stesso. Il campo relativo al codice pacchetto della riga del prospetto verrà compilato con il codice del pacchetto a cui è assegnata la tabella.  
4. Se si sceglie un pacchetto esistente, è possibile visualizzare quante tabelle sono già contenute nel pacchetto verificando le informazioni nel campo **Nr. tabelle**.

## <a name="to-review-or-customize-existing-database-data"></a>Per analizzare o personalizzare dati in database esistenti

Quando si crea un pacchetto di configurazione per una soluzione, è possibile visualizzare e personalizzare i dati del database disponibili per adattarli alle esigenze del cliente. Alla tabella del database deve essere associata una pagina.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi scegliere il collegamento correlato.
2. Nel foglio di lavoro configurazione, individuare le tabelle di cui si desidera visualizzare o modificare i dati.  

    > [!NOTE]  
    >  Assicurarsi che a ogni tabella sia stato assegnato un ID pagina. Per le tabelle [!INCLUDE[prod_short](includes/prod_short.md)], il valore viene compilato automaticamente. Per le tabelle personalizzate, occorre immettere l'ID.

3. Scegliere l'azione **Dati database**. Viene visualizzata la pagina per la pagina relativa.
4. Esaminare le informazioni disponibili. Modificare in base alle esigenze eliminando i record non pertinenti o aggiungendone di nuovi.  

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Per copiare dati da un ambiente di test in uno di produzione

Dopo aver esaminato e testato tutte le informazioni di setup, è possibile copiare i dati all'interno del proprio ambiente di produzione. Creare una nuova società nello stesso database.

1. Aprire e inizializzare la nuova società.  
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi scegliere il collegamento correlato.  
3. Scegliere l'azione **Copia dati da società**.  
4. Nella pagina **Copia dati società**, selezionare **Copia da**. Verrà aperta la pagina **Società**.  
5. Selezionare la società da cui copiare i dati e selezionare il pulsante **OK**. Viene visualizzata una lista di tabelle selezionate nel foglio di lavoro configurazione. Solo le tabelle contenenti i record sono incluse nella lista.
6. Selezionare le tabelle da cui copiare i dati, quindi scegliere l'azione **Copia dati**. Nella pagina **Copia dati società**, selezionare il pulsante **OK**.  

## <a name="see-also"></a>Vedere anche

[Preparare la migrazione dei dati dei clienti con modelli](admin-use-templates-to-prepare-customer-data-for-migration.md)  
[Raggruppare i valori di setup del cliente](admin-gather-customer-setup-values.md)  
[Impostare la configurazione della società](admin-set-up-company-configuration.md)  
[Impostazione di una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Analizzare la telemetria della traccia del pacchetto di configurazione](/dynamics365smb-devitpro/dev-itpro/administration/telemetry-configuration-package-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]