---
title: Come creare report con XBRL
description: XBRL è un linguaggio basato su XML per l'assegnazione di tag ai dati finanziari che consente alle aziende di elaborare e condividere i dati in maniera efficiente e accurata.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: b282ea2aeec8e28b36bdadfdb57065e8c9e0c727
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075058"
---
# <a name="create-reports-with-xbrl"></a>Creare report con XBRL

> [!NOTE]
> Stiamo rimuovendo le funzionalità per i report XBRL da [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Modifiche nel primo ciclo di rilascio del 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL è l'acronimo di eXtensible Business Reporting Language, un linguaggio basato su XML per l'assegnazione di tag ai dati finanziari che consente alle aziende di elaborare e condividere i dati in maniera efficiente e accurata. L'iniziativa XBRL abilita il reporting finanziario globale da parte di numerose società che producono software ERP e organizzazioni contabili internazionali. L'obiettivo dell'iniziativa consiste nel fornire uno standard per il reporting uniforme delle informazioni finanziarie per banche, investitori e autorità governative. Tali funzionalità di reporting possono includere:  

 • Rendiconti finanziari  
 • Informazioni finanziarie  
 • Informazioni non finanziarie  
 • Archiviazioni normative, quali i rendiconti finanziari annuali e trimestrali  

> [!NOTE]
> È possibile importare schemi correlati alla contabilità generale e creare documenti di istanza XBRL mappando i dati C/G dal piano dei conti agli elementi di tassonomie progettati per i report finanziari, come conti patrimoniali, conti economici e così via.
> 
> Le funzionalità XBRL in Business Central supportano le tassonomie per la Specifica 2.1. Le tassonomie potrebbero tuttavia contenere elementi non supportati, come basi di collegamento delle formule, iXBRL, o avere altre differenze strutturali. Si consiglia di convalidare la funzionalità XBRL prima di utilizzarla per la creazione di report.
> 
> Il supporto completo per le tassonomie potrebbe richiedere strumenti e tag XBRL di terze parti. L'organizzazione XBRL International dispone di un elenco di strumenti e servizi che è possibile utilizzare per la creazione di report XBRL. A seconda dei requisiti di creazione di report XBRL per una determinata tassonomia, potrebbe essere necessario esplorare tali risorse. Per ulteriori informazioni, vedi la pagina di [introduzione per le aziende](https://go.microsoft.com/fwlink/?linkid=2153466) e [Strumenti e servizi](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language
XBRL (e **X** tensible **B** usiness **R** eporting **L** anguage) è un linguaggio XML utilizzato per la creazione di rendiconti finanziari. Esso fornisce uno standard uniforme per la stesura di report utilizzato da tutti gli utenti che forniscono informazioni finanziarie, ad esempio società private e pubbliche, commercialisti, autorità di regolamentazione, analisti finanziari, investitori, operatori finanziari e finanziatori, nonché terze parti che svolgono un ruolo chiave, quali sviluppatori di software e analisti di dati.  

La gestione delle tassonomie è a cura di www.xbrl.org. Per ulteriori informazioni o se si desidera scaricare le tassonomie, è possibile visitare il sito Web di XBRL.  

Chi richiede informazioni finanziarie fornisce una tassonomia, sotto forma di un documento XML, contenente uno o più schemi, ciascuno con una o più righe da compilare. Le righe corrispondono ai singoli dati finanziari richiesti dal mittente. È innanzitutto necessario importare la tassonomia, quindi procedere alla compilazione degli schemi, specificando il conto o i conti che corrispondono a ciascuna riga e il tipo di intervallo temporale da utilizzare, ad esempio Saldo Periodo o Saldo alla Data. In alcuni casi, invece, è possibile immettere una costante, ad esempio un numero di dipendenti. A questo punto, il documento di istanza (un documento XML) è pronto per essere inviato al richiedente. Poiché questo processo può essere un evento ricorrente, a meno che non vengano apportate modifiche alla tassonomia, sarà sufficiente esportare su richiesta nuovi documenti di istanza per periodi differenti.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>Componenti di XBRL  
La **Specifica** XBRL definisce il linguaggio XBRL e la modalità di creazione di documenti di istanza XBRL e delle tassonomie XBRL. La specifica XBRL illustra il linguaggio in termini tecnici ed è rivolta essenzialmente agli utenti esperti.  

Lo **Schema** XBRL è il componente di base del linguaggio XBRL. Lo schema è costituito da un file XSD che fornisce le istruzioni di creazione dei documenti di istanza e delle tassonomie.  

Le **Basi di collegamento** XBRL sono i file XML che contengono varie informazioni sugli elementi definiti nello schema XBRL, ad esempio etichette in una o più lingue, le relazioni tra le informazioni, la modalità di riepilogo degli elementi e così via.  

La **Tassonomia** XBRL è un "vocabolario" o "dizionario", compatibile con la specifica XBRL, creato da un gruppo per lo scambio di informazioni finanziarie.  

Il **Documento di istanza** XBRL è un report finanziario, ad esempio un rendiconto finanziario preparato secondo la specifica XBRL. Il significato dei valori presenti nel documento di istanza è spiegato dalla tassonomia. Un documento di istanza può avere scarso significato per l'utente, a meno che non conosca la tassonomia in base alla quale è stato preparato.  

## <a name="layered-taxonomies"></a>Livelli di tassonomie  
Una tassonomia può essere composta da una tassonomia di base, ad esempio, us-gaap o IAS, e disporre di una o più estensioni. Analogamente, una tassonomia fa riferimento a uno o più schemi, ognuno dei quali è una tassonomia distinta. Quando le tassonomie aggiuntive vengono caricate nel database, i nuovi elementi vengono semplicemente aggiunti in coda agli elementi esistenti.  

## <a name="linkbases"></a>Basi di collegamento  
 In base alla specifica XBRL 2, la tassonomia viene descritta utilizzando diversi file XML. Il file XML principale è il file di schema della tassonomia, con estensione xsd, che contiene solo una lista non ordinata di elementi o dati da riportare. Oltre a questo, vi sono in genere file di basi di collegamento associati, con estensione xml, che contengono dati complementari alla tassonomia primaria (file con estensione xsd). Esistono sei tipi di file di basi di collegamento, quattro dei quali sono rilevanti per lo schema XBRL di Nome prodotto. Si tratta di:  

-   Base di collegamento delle etichette: questa base di collegamento contiene le etichette o i nomi degli elementi. Il file può contenere etichette in diverse lingue, identificate dalla proprietà XML "lang". L'identificatore di lingua XML in genere contiene un'abbreviazione di due lettere ma, sebbene il significato dell'abbreviazione sia alquanto immediato, non esiste alcuna relazione con il codice lingua di Windows o i codici lingua definiti nei dati dimostrativi. Pertanto, quando un utente cerca le lingue per una tassonomia specifica, vedrà tutte le etichette per il primo elemento della tassonomia. Ciò significa che sarà in grado di visualizzare un esempio per ciascuna lingua. A una tassonomia è possibile collegare diverse basi di collegamento delle etichette, purché le basi di collegamento contengano lingue diverse.  

-   Base di collegamento di presentazione: questa base di collegamento contiene informazioni sulla struttura degli elementi o, più precisamente, sul modo in cui la tassonomia viene presentata all'utente, secondo i suggerimenti del creatore stesso. La base di collegamento fornisce una serie di collegamenti, ognuno dei quali collega due elementi ponendoli in una relazione di tipo padre-figlio. Quando si applicano tali collegamenti, gli elementi possono essere visualizzati secondo una struttura gerarchica. Si noti che la base di collegamento di presentazione gestisce esclusivamente la presentazione visiva degli elementi all'utente.  

-   Base di collegamento di calcolo: questa base di collegamento contiene informazioni sul rollup degli elementi. La struttura è abbastanza simile a quella della base collegamento di presentazione, ad eccezione del fatto che a ciascun collegamento o "arco", come viene altrimenti definito, è assegnata una proprietà di peso. Il peso può essere 1 o -1, a indicare se l'elemento deve essere sommato o sottratto dall'elemento padre. Si noti che i rollup non si accordano necessariamente alla presentazione visiva.  

-   Base di collegamento di riferimento: questa base di collegamento è un file xml contenente informazioni supplementari in merito ai dati richiesti dal creatore della tassonomia.

## <a name="to-set-up-xbrl-lines"></a>Per impostare le righe XBRL  
Dopo aver importato o aggiornato la tassonomia, è necessario fornire alle righe degli schemi tutte le informazioni necessarie. Tali dati includono informazioni di base sulla società, rendiconti finanziari effettivi, note sui rendiconti finanziari, situazioni contabili aggiuntive e altre informazioni necessarie a soddisfare i requisiti del resoconto finanziario specifico.  

È possibile impostare le righe XBRL associando i dati della tassonomia ai dati di contabilità generale mediante mappatura.  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tassonomie XBRL**, quindi scegli il collegamento correlato.  
2.  Nella pagina **Tassonomie XBRL** selezionare una tassonomia dall'elenco.  
3.  Scegliere l'azione **Righe**.  
4.  Selezionare una riga e compilare i campi.   
5.  Per visualizzare informazioni dettagliate sui dati da immettere, scegliere l'azione **Informazioni**.  
6.  Per impostare il mapping dei conti C/G nel piano dei conti alle righe XBRL, scegliere l'azione **Righe mappa C/G**.  
7.  Per aggiungere note al rendiconto finanziario, scegliere l'azione **Note**.  

   > [!TIP]
   > Per escludere righe dall'esportazione, scegli **NON APPLICABILE** come tipo di origine.

   > [!NOTE]  
   > Puoi esportare solo i dati che corrispondono alla selezione nel campo **Tipo di origine**. Ciò include descrizioni e note.  

   > [!NOTE]  
   > Le tassonomie potrebbero contenere elementi che [!INCLUDE[prod_short](includes/prod_short.md)] non supporta. Se un elemento non è supportato, il campo **Tipo di origine** visualizzerà **Non applicabile** e il campo **Descrizione** mostrerà un messaggio di errore, come **Tipo imprevisto: "tipo specifico non riconosciuto"**. Se devi esportare l'elemento, scegli un tipo di origine corrispondente. In genere, questa è una costante o una descrizione. Ciò consentirà di immettere ed esportare dati, tuttavia, tali elementi potrebbero avere regole di convalida che non possono essere verificate prima dell'esportazione.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Per importare una tassonomia XBRL  
La prima operazione da eseguire per poter utilizzare la funzionalità XBRL è l'importazione della tassonomia nel database aziendale. Una tassonomia è composta da uno o più schemi e da basi di collegamento. Al termine dell'importazione degli schemi e delle basi di collegamento e dopo avere applicato le basi di collegamento agli schemi, è possibile impostare le righe e associare i conti di contabilità generale del Piano dei Conti alle righe di tassonomia appropriate.  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tassonomie XBRL**, quindi scegli il collegamento correlato.  
2.  Creare una nuova riga e immettere il nome e la descrizione della tassonomia nella pagina **Tassonomie XBRL**.  
3.  Scegliere l'azione **Schemi** e quindi inserire la descrizione dello schema.  
4.  Per importare lo schema, nella pagina **Schemi XBRL** scegliere l'azione **Importa** e quindi selezionare una cartella e un file XSD. Scegliere il pulsante **Apri**.  
5.  Per importare la base di collegamento, nella pagina **Schemi XBRL** scegliere l'azione **Basi collegamento** e quindi selezionare una cartella e un file XML. Scegliere il pulsante **Apri**.  
6.  A questo punto, è possibile scegliere se applicare o meno la base di collegamento allo schema. Ripetere questa procedura per importare tutte le basi di collegamento.  
7. Scegliere l'azione **Applicare a tassonomia** per applicare la base di collegamento allo schema.  

> [!IMPORTANT]  
>  Anziché collegare singolarmente le basi di collegamento dopo l'importazione, è possibile attendere l'importazione di tutte le basi di collegamento e collegarle poi contemporaneamente. A tale scopo, fare clic sul pulsante **NO** alla richiesta di collegamento della base di collegamento appena importata allo schema. Selezionare le righe con le basi di collegamento che si desidera collegare.  

## <a name="to-update-an-xbrl-taxonomy"></a>Per aggiornare una tassonomia XBRL  
Quando una tassonomia viene modificata è necessario aggiornare di conseguenza la tassonomia corrente. Il motivo della modifica può essere uno schema modificato, una base di collegamento modificata o una nuova base collegamento. Dopo aver aggiornato la tassonomia, sarà necessario mappare le righe per le nuove righe o per quelle modificate.  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tassonomie XBRL**, quindi scegli il collegamento correlato.  
2.  Nella pagina **Tassonomie XBRL** scegliere l'azione **Schemi**.  
3.  Per aggiornare uno schema, selezionare lo schema da aggiornare e scegliere l'azione **Importa**.  
4.  Per aggiornare o aggiungere una nuova base di collegamento, scegliere l'azione **Basi collegamento**.  
5.  Selezionare la relativa base di collegamento o premere CTRL+N per immettere una nuova riga, scegliere il tipo di base di collegamento, quindi inserire una descrizione.  
6.  Per importare la base di collegamento, scegliere l'azione **Importa**.  
7.  Scegliere il pulsante **Sì** per collegare la base di collegamento allo schema.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Finanze](finance.md)    
[Business Intelligence](bi.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]