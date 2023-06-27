---
title: Come creare report con XBRL
description: XBRL è un linguaggio basato su XML per l'assegnazione di tag ai dati finanziari che consente alle aziende di elaborare e condividere i dati in maniera efficiente e accurata.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="create-reports-with-xbrl" />Creare report con XBRL

> [!NOTE]
> Stiamo rimuovendo le funzionalità per i report XBRL da [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni vedi [Modifiche nel primo ciclo di rilascio del 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e**X**tensible **B**usiness **R**eporting **L**anguage) è un linguaggio basato su XML (eXtensible Markup Language) per l'assegnazione di tag ai dati finanziari che consente alle aziende di elaborare e condividere i dati in maniera efficiente e accurata. L'iniziativa XBRL abilita il reporting finanziario globale da parte di numerose società che producono software ERP (Enterprise Resource Planning) e organizzazioni contabili internazionali. L'obiettivo dell'iniziativa consiste nel fornire uno standard per il reporting uniforme delle informazioni finanziarie per banche, investitori e autorità governative. Tali funzionalità di reporting possono includere:  

* Rendiconti finanziari  
* Informazioni finanziarie  
* Informazioni non finanziarie  
* Archiviazioni normative, quali i rendiconti finanziari annuali e trimestrali  

> [!NOTE]
> È possibile importare schemi correlati alla contabilità generale e creare documenti di istanza XBRL mappando i dati di contabilità generale (C/G) dal piano dei conti agli elementi di tassonomie progettati per i report finanziari, come conti patrimoniali, conti economici e così via.
>
> Le funzionalità XBRL in Business Central supportano le tassonomie per la specifica 2.1. Tuttavia, le tassonomie possono contenere elementi non supportati come formule linkbase o iXBRL (XBRL inline) o presentare altre differenze strutturali. Ti consigliamo di convalidare la funzionalità XBRL prima di utilizzarla per la creazione di report.
>
> Il supporto completo per le tassonomie potrebbe richiedere strumenti e tag XBRL di terze parti. L'organizzazione XBRL International ha un elenco di strumenti e servizi, a seconda dei requisiti di report XBRL per una determinata tassonomia, potresti voler esplorare queste risorse. Per ulteriori informazioni, vedi [Introduzione per le aziende](https://go.microsoft.com/fwlink/?linkid=2153466) e [Strumenti e servizi](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language" />eXtensible Business Reporting Language

La gestione delle tassonomie XBRL è a cura di www.xbrl.org. Per ulteriori informazioni e se vuoi scaricare le tassonomie, è possibile visitare il sito Web di XBRL.  

Supponiamo che qualcuno vuole le tue informazioni finanziarie. Fornisce una tassonomia, sotto forma di un documento XML, contenente uno o più schemi, ciascuno con una o più righe da compilare. Le righe corrispondono ai singoli dati finanziari richiesti dal mittente. Importi la tassonomia, quindi compili gli schemi, specificando i conti che corrispondono a ciascuna riga e il calcolo desiderato, ad esempio Saldo Periodo o Saldo alla Data. In alcuni casi, invece, è possibile immettere una costante, ad esempio un numero di dipendenti. A questo punto, il documento di istanza (un documento XML) è pronto per essere inviato al richiedente. Poiché questo processo può essere un evento ricorrente, a meno che non vengano apportate modifiche alla tassonomia, sarà sufficiente esportare su richiesta nuovi documenti di istanza per periodi differenti.

## <a name="xbrl-comprises-the-following-components" />Componenti di XBRL

La **Specifica** XBRL definisce il linguaggio XBRL e la modalità di creazione di documenti di istanza XBRL e delle tassonomie. La specifica XBRL illustra il linguaggio in termini tecnici ed è rivolta essenzialmente agli utenti esperti.  

Lo **Schema** XBRL è il componente di base del linguaggio XBRL. Lo schema è costituito da un file XSD (chiamato anche definizione di schema XML) che fornisce le istruzioni di creazione dei documenti di istanza XBRL e delle tassonomie.

Le **Basi di collegamento** XBRL sono i file XML che contengono informazioni sugli elementi definiti nello schema XBRL, ad esempio etichette in una o più lingue, le relazioni tra le informazioni, la modalità di riepilogo degli elementi e così via.  

La **Tassonomia** XBRL è un "vocabolario" o "dizionario", compatibile con la specifica XBRL, che consente lo scambio di informazioni finanziarie.  

Il **Documento di istanza** XBRL è un report finanziario, ad esempio un rendiconto finanziario preparato secondo la specifica XBRL. Il significato dei valori presenti nel documento di istanza è spiegato dalla tassonomia. Infatti, un documento di istanza può avere scarso significato per l'utente, a meno che non conosca la tassonomia in base alla quale è stato preparato.  

## <a name="layered-taxonomies" />Livelli di tassonomie

Una tassonomia può consistere in una tassonomia di base, ad esempio US GAAP (United States Generally Accepted Accounting Principles) o IAS (standard contabili internazionali), e quindi avere una o più estensioni. Analogamente, una tassonomia fa riferimento a uno o più schemi, ognuno dei quali è una tassonomia distinta. Quando le tassonomie aggiuntive vengono caricate nel database, i nuovi elementi vengono semplicemente aggiunti in coda agli elementi esistenti.  

## <a name="linkbases" />Basi collegamento

In base alla specifica XBRL 2, la tassonomia viene descritta utilizzando diversi file XML. Il file XML principale è il file di schema della tassonomia, con estensione xsd, che contiene solo una lista non ordinata di elementi o dati da riportare. Oltre a questo, vi sono in genere file di basi di collegamento, con estensione xml, che contengono dati complementari alla tassonomia primaria (file con estensione xsd). Esistono sei tipi di file di basi di collegamento, quattro dei quali sono rilevanti per [!INCLUDE[prod_short](includes/prod_short.md)]. Si tratta di:

* Base di collegamento delle etichette: questa base di collegamento contiene le etichette o i nomi degli elementi. Il file può contenere etichette in diverse lingue, identificate dalla proprietà XML "lang". L'identificatore di lingua XML in genere contiene un'abbreviazione di due lettere ma, sebbene il significato dell'abbreviazione sia alquanto immediato, non esiste alcuna relazione con il codice lingua di Microsoft Windows o i codici lingua definiti nei dati dimostrativi. Pertanto, quando cerchi le lingue per una tassonomia specifica, vedrai tutte le etichette per il primo elemento della tassonomia. Ciò significa che sarai in grado di visualizzare un esempio per ciascuna lingua. A una tassonomia è possibile collegare diverse basi di collegamento delle etichette, purché le basi di collegamento contengano lingue diverse.  
* Base di collegamento di presentazione: questa base di collegamento contiene informazioni sulla struttura degli elementi o, più precisamente, sul modo in cui la tassonomia ti viene presentata, secondo i suggerimenti del creatore stesso. La base di collegamento fornisce una serie di collegamenti, ognuno dei quali collega due elementi in una relazione di tipo padre-figlio. Quando si applicano tali collegamenti, gli elementi possono essere visualizzati secondo una struttura gerarchica. La base di collegamento di presentazione gestisce esclusivamente la presentazione visiva degli elementi.
* Base di collegamento di calcolo: questa base di collegamento contiene informazioni sul rollup degli elementi. La struttura è abbastanza simile a quella della base collegamento di presentazione, ad eccezione del fatto che a ciascun collegamento o "arco", come viene altrimenti definito, è assegnata una proprietà di peso. Il peso può essere 1 o -1, a indicare se l'elemento deve essere sommato o sottratto dall'elemento padre. Tieni presente che i rollup non si allineano necessariamente alla presentazione visiva.  
* Base di collegamento di riferimento: questa base di collegamento è un file xml contenente informazioni supplementari in merito ai dati richiesti dal creatore della tassonomia.

## <a name="set-up-xbrl-lines" />Impostare righe XBRL

Dopo aver importato o aggiornato la tassonomia, le righe degli schemi devono essere compilate con tutte le informazioni necessarie per soddisfare i particolari requisiti di report finanziari. Queste informazioni includono le informazioni della società di base, i rendiconti finanziari effettivi, le note ai rendiconti finanziari, i prospetti supplementari e così via.  

Imposti le righe XBRL associando i dati della tassonomia ai dati di contabilità generale mediante mappatura.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tassonomie XBRL**, quindi scegli il collegamento correlato.  
2. Nella pagina **Tassonomie XBRL** selezionare una tassonomia dall'elenco.  
3. Scegliere l'azione **Righe**.  
4. Selezionare una riga e compilare i campi.  
5. Per visualizzare informazioni dettagliate sui dati da immettere, scegliere l'azione **Informazioni**.  
6. Per impostare il mapping dei conti C/G nel piano dei conti alle righe XBRL, scegli l'azione **Righe mappa C/G**.  
7. Per aggiungere note al rendiconto finanziario, scegliere l'azione **Note**.  

   > [!TIP]
   > Per escludere righe dai dati esportati, scegli **NON APPLICABILE** come tipo di origine.

   > [!NOTE]  
   > Puoi esportare solo i dati che corrispondono alla selezione nel campo **Tipo di origine**. Ciò include descrizioni e note.  

   > [!NOTE]  
   > Le tassonomie potrebbero contenere elementi che [!INCLUDE[prod_short](includes/prod_short.md)] non supporta. Se un elemento non è supportato, il campo **Tipo di origine** visualizzerà **Non applicabile** e il campo **Descrizione** mostrerà un messaggio di errore, come **Tipo imprevisto: "tipo specifico non riconosciuto"**. Se devi esportare l'elemento, scegli un tipo di origine corrispondente. In genere, questa è una costante o una descrizione. Ciò ti consente di immettere ed esportare dati, tuttavia, tali elementi potrebbero avere regole di convalida che non possono essere verificate prima dell'esportazione.

## <a name="import-an-xbrl-taxonomy" />Importare una tassonomia XBRL

La prima operazione da eseguire per poter utilizzare la funzionalità XBRL è l'importazione della tassonomia nel database aziendale. Una tassonomia è composta da uno o più schemi e da basi di collegamento. Al termine dell'importazione degli schemi e delle basi di collegamento e dopo avere applicato le basi di collegamento agli schemi, è possibile impostare le righe e associare i conti di contabilità generale del Piano dei Conti alle righe di tassonomia appropriate.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tassonomie XBRL**, quindi scegli il collegamento correlato.  
2. Creare una nuova riga e immettere il nome e la descrizione della tassonomia nella pagina **Tassonomie XBRL**.  
3. Scegli l'azione **Schemi** e quindi inserisci la descrizione dello schema.  
4. Per importare lo schema, nella pagina **Schemi XBRL**, scegli l'azione **Importa**, quindi esegui una delle seguenti operazioni per caricare il file:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Per importare la base collegamento, nella pagina **Schemi XBRL**, scegli l'azione **Basi collegamento**, quindi esegui una delle seguenti operazioni per caricare il file:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. A questo punto, è possibile scegliere se applicare o meno la base di collegamento allo schema. Ripetere questa procedura per importare tutte le basi di collegamento.  
7. Scegliere l'azione **Applicare a tassonomia** per applicare la base di collegamento allo schema.  

> [!IMPORTANT]  
> Anziché collegare singolarmente le basi di collegamento dopo l'importazione, è possibile attendere l'importazione di tutte le basi di collegamento e collegarle poi contemporaneamente. A tale scopo, scegli **NO** alla richiesta di collegamento della base di collegamento appena importata allo schema. Selezionare le righe con le basi di collegamento che si desidera collegare.  

## <a name="update-an-xbrl-taxonomy" />Aggiornare una tassonomia XBRL

Quando una tassonomia viene modificata è necessario aggiornare di conseguenza la tassonomia corrente. Il motivo della modifica può essere uno schema modificato, una base di collegamento modificata o una nuova base collegamento. Dopo aver aggiornato la tassonomia, sarà necessario mappare le righe per le nuove righe o per quelle modificate.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tassonomie XBRL**, quindi scegli il collegamento correlato.  
2. Nella pagina **Tassonomie XBRL** scegliere l'azione **Schemi**.  
3. Per aggiornare uno schema, seleziona lo schema da aggiornare e scegli l'azione **Importa**.  
4. Per aggiornare o aggiungere una nuova base di collegamento, scegliere l'azione **Basi collegamento**.  
5. Seleziona la relativa base di collegamento o premi <kbd>CTRL</kbd>+<kbd>N</kbd> per immettere una nuova riga, scegliere il tipo di base di collegamento, quindi inserire una descrizione.  
6. Per importare la base di collegamento, scegliere l'azione **Importa**.  
7. Scegli **Sì** per collegare la base di collegamento allo schema.  

## <a name="see-related-training-at-microsoft-learn" />Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## <a name="see-also" />Vedere anche

[Business Intelligence finanziario](bi.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
