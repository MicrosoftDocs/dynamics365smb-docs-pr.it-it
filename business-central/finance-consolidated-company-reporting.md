---
title: Consolidare i dati di molteplici società
description: In questo articolo viene spiegato come consolidare i movimenti di contabilità generale di due o più società separate (filiali) in una società consolidata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
---

# Consolidare dati finanziari di molteplici società

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)] nelle filiali che devono riferire nelle organizzazioni madri. [!INCLUDE [prod_short](includes/prod_short.md)] offre ai contabili strumenti che li aiutano a trasferire i movimenti C/G da due o più società (filiali) a una società consolidata.  

Ogni società coinvolta in un consolidamento è detta business unit. La società in cui combini i dati è detta società consolidata.  

Puoi trasferire i dati finanziari dalle filiali alla società consolidata, anche se le filiali utilizzano [!INCLUDE [prod_short](includes/prod_short.md)] in ambienti diversi. Per ulteriori informazioni su come connettersi ad altri ambienti, vedi [Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md#busunit).

Se i rendiconti finanziari di una business unit usano una valuta diversa da quella della società consolidata, devi impostare i tassi di cambio per il consolidamento. Per ulteriori informazioni sui tassi di cambio per i consolidamenti, vedi [Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md#exchrates).  

È possibile eseguire il consolidamento:  

* Per le società che hanno piani dei conti differenti.  
* Per le società che utilizzano anni fiscali e valute differenti.  
* Dell'importo completo o di una percentuale delle informazioni finanziarie di una società.
* Utilizzando differenti tassi di cambio delle valute in singoli conti C/G.
* Società in altri programmi di contabilità e gestione aziendale.
* Società in ambienti [!INCLUDE [prod_short](includes/prod_short.md)] differenti.

Una società consolidata viene impostata come qualsiasi altra società. Il piano dei conti è indipendente dal piano dei conti nelle business unit. Il piano dei conti nelle business unit può differire l'uno dall'altro. Per ulteriori informazioni sull'impostazione di un consolidamento, vedi [Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Il consolidamento dei dati finanziari può essere particolarmente pertinente per processi Intercompany. Per ulteriori informazioni sulle funzionalità interaziendali, vai a [Gestione delle transazioni interaziendali](intercompany-manage.md).

## Consolidare i dati

Prima di eseguire il consolidamento, è una buona idea testare i dati prima di trasferirli alla società consolidata. [!INCLUDE[prod_short](includes/prod_short.md)] cerca le differenze tra le informazioni delle business unit e quelle della società consolidata. Ad esempio, se i numeri di conto o i codici di dimensione sono diversi. Correggi gli eventuali errori rilevati prima di eseguire il report. Puoi verificare il database oppure, se importi dati da un file XML, il file.

### Verificare i dati prima del consolidamento

1. Aprire la società consolidata.  
2. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Business unit**, quindi scegli il collegamento correlato.  
3. Testa il file e il database, come segue:  

    * Per verificare un file, scegliere l'azione **Test file**, immettere il nome del file da verificare, quindi scegliere **Stampa**.  
    * Per verificare il database, scegliere **Test database**.  

### Eseguire il consolidamento

Dopo aver testato i dati, è possibile trasferirli alla società consolidata. Una guida al setup assistito ti aiuterà durante il processo.

> [!NOTE]
> Quando esegui il consolidamento puoi scegliere le società da includere. Se la società consolidata non ha accesso a una o più filiali, la guida ti consentirà di concedere l'accesso alle stesse.

1. Accedere alla società consolidata.  
2. Nella pagina **Business Units** scegli l'azione **Consolida**.  
3. Compilare i campi necessari.  

## Usare il report Bilancio di verifica consolidato

Il report **Bilancio di verifica consolidato** può fornire una panoramica dello stato finanziario generale dell'attività commerciale. Il report combina i movimenti di contabilità generale di ognuna delle società in una nuova società creata per i dati consolidati. La società consolidata è solo un contenitore per i dati unificati e non presenta dati aziendali dinamici. Le società incluse nella società consolidata diventano **business unit** nel report. Se hai al massimo quattro business unit, puoi anche utilizzare il report **Bil. di verif. consolidato (4)**.  

Il report mostra una riga per ogni conto e segue la struttura del piano dei conti. Un conto non viene visualizzato se tutti gli importi nella riga hanno valore 0. Il report visualizza per ogni conto le informazioni seguenti:

* Il nome e il numero del conto.
* I totali per la società consolidata e per ogni business unit. I totali possono essere visualizzati come saldo periodo e come saldo alla data.
* Le eliminazioni eseguite nella società consolidata. Le eliminazioni vengono sempre visualizzate per un periodo corrispondente all'anno fiscale della società consolidata.
* Il totale per la società consolidata in seguito alle eliminazioni, visualizzato sia come saldo periodo che come saldo alla data.

## Eliminare transazioni ripetute

Dopo avere eseguito il consolidamento delle società, è necessario trovare ed eliminare le transazioni registrate più di una volta nelle società. L'elaborazione delle eliminazioni in seguito al consolidamento è un processo manuale.  

Per eliminare transazioni ripetute:

1. Individua le transazioni che potenzialmente devono essere rettificate e immetti le righe delle registrazioni COGE per eliminarle.
2. Eseguire il report **Eliminaz. consolidamenti C/G** per valutare l'effetto delle righe delle registrazioni COGE prima della registrazione.
3. Registrare le transazioni di rettifica.

Il report **Eliminazioni consolidamento C/G** visualizza un bilancio di verifica provvisorio in cui è possibile simulare le conseguenze dell'eliminazione dei movimenti. Il report confronta i movimenti nella società consolidata con le eliminazioni registrate nel giornale di registrazione COGE.

Per poter includere una business unit nel report, devi impostarla nella pagina **Business Unit**. Assicurati di attivare l'interruttore **Consolida**.

Viene creata una riga per ogni conto secondo la struttura del piano dei conti. Un conto non viene visualizzato se tutti gli importi nella riga hanno valore 0. Il report visualizza per ogni conto le informazioni seguenti:

* Numero conto.
* Nome conto.
* Se sono stati selezionati uno o più codici di business unit nel campo **Codice Business Unit** della pagina di richiesta, viene visualizzato un totale per la società consolidata, escluse le business unit e le eliminazioni selezionate. Se il campo **Codice Business Unit** non è stato compilato, viene visualizzato un totale per la società consolidata escluse le eliminazioni.
* Se è stato selezionato un codice di business unit nel campo **Codice Business Unit** nella pagina di richiesta, viene visualizzato un totale per i movimenti importati dalla business unit. Se il campo **Codice Business Unit** non è stato compilato, viene visualizzato un totale per le eliminazioni registrate nella società consolidata.
* Il totale relativo alla società consolidata comprese tutte le business unit e le eliminazioni registrate.
* Le eliminazioni da eseguire nella società consolidata. Ovvero, le voci nel giornale di registrazione generale selezionato nella pagina della richiesta.
* Il testo di registrazione copiato dalle registrazioni generali.
* Il totale della società consolidata in seguito alle eliminazioni, nel caso vengano registrate.

## Esportare e importare dati consolidati tra database

Se i dati di una business unit si trovano in un altro database, puoi eseguire un trasferimento manuale basato su file o automatizzare il processo utilizzando un'API. Per ulteriori informazioni sull'API, vedi [Utilizzare la nostra API per condividere automaticamente i dati tra ambienti](#use-our-api-to-automatically-share-data-across-environments).

Questa sezione descrive il processo manuale basato su file.

I dati vengono esportati in un file prima di essere inclusi nel consolidamento. Esporta ciascuna società separatamente utilizzando il processo batch **Esporta consolidamento**.  

> [!TIP]
> Utilizza lo stesso processo per esportare i dati consolidati che devi inviare a Dynamics 365 Finance. Ad esempio, se la business unit è una filiale e la società madre utilizza Dynamics 365 Finance.

Dopo avere eseguito il processo batch, vengono elaborati tutti i movimenti dei conti di contabilità generale. Per ogni combinazione di dimensioni selezionate e data, i contenuti dei campi **Importo** dei movimenti vengono sommati ed esportati. Viene elaborata la combinazione successiva delle dimensioni e della data selezionate con lo stesso numero di conto. Quindi vengono elaborate le combinazioni del numero di conto successivo e così via.  

I movimenti esportati contengono i seguenti campi: **Nr. conto**, **Data di registrazione** e **Importo**. Se sono state esportate anche informazioni sulle dimensioni, vengono inclusi anche i codici e i valori delle dimensioni.  

1. Per ogni riga esportata, se il totale dei campi **Importo** è in dare, il numero di conto impostato nel campo **Conto consol. dare** viene esportato nella riga. Se l'importo totale è un credito, il numero corrispondente nel campo **Conto consol. avere** viene esportato nella riga.  
2. La data utilizzata per ogni riga esportata è quella di fine del periodo oppure, se il trasferimento avviene giornalmente, la data esatta del calcolo.  
3. Il valore delle dimensioni esportato per il movimento sarà il valore delle dimensioni della società consolidata specificato nel campo **Cod. consolidamento** per tale valore. Se nel campo **Cod. consolidamento** non è stato immesso un valore delle dimensioni della società consolidata per tale valore, nella riga verrà esportato il valore delle dimensioni stesso.  
4. I file XML, inoltre, contengono i tassi di cambio valuta inclusi nel periodo di consolidamento. I tassi sono inclusi in una sezione separata all'inizio del file.  

## Utilizzare la nostra API per condividere automaticamente i dati tra ambienti

[!INCLUDE [prod_short](includes/prod_short.md)] fornisce un'API che ti consente di automatizzare il processo di condivisione dei dati finanziari dalle business unit alla società consolidata. L'API è gratuita e facile da configurare. Ti consente anche di condividere i dati tra ambienti [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, potrebbe essere necessario effettuare la condivisione tra ambienti quando le business unit non si trovano nelle stesse aree geografiche di Azure. Per ulteriori informazioni sull'utilizzo dell'API per automatizzare il processo di consolidamento, vedi [Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md#busunit).

## Vedi anche

[Impostare il consolidamento società](finance-consolidated-company-reporting-setup.md)  
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]