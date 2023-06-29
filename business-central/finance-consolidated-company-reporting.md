---
title: Consolidare i dati di molteplici società
description: In questo articolo viene spiegato come consolidare i movimenti di contabilità generale di due o più società separate (filiali) in una società consolidata.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# <a name="consolidating-financial-data-from-multiple-companies"></a><a name="consolidating-financial-data-from-multiple-companies"></a>Consolidare dati finanziari di molteplici società

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)] nelle filiali che devono riferire nelle organizzazioni madri. In entrambi i casi, i contabili utilizzano strumenti integrati per consolidare i dati finanziari.  

È possibile consolidare i movimenti di contabilità generale di due o più società separate (filiali) in una società consolidata. Ogni società coinvolta in un consolidamento è detta business unit. La società generata da questa unione è detta società consolidata.  

È possibile importare dati nella società consolidata da altre società nello stesso tenant [!INCLUDE [prod_short](includes/prod_short.md)], da tenant o da file.  

Se i rendiconti finanziari di una business unit sono in una valuta diversa da quella usata nella società consolidata, è necessario impostare i tassi di cambio per il consolidamento.  

È possibile eseguire il consolidamento:  

* Per le società che hanno piani dei conti differenti.  
* Per le società che utilizzano anni fiscali e valute differenti.  
* Dell'importo completo o di una percentuale delle informazioni finanziarie di una società
* Utilizzando differenti tassi di cambio delle valute in singoli conti C/G
* Società in altri programmi di contabilità e gestione aziendale

Una società consolidata viene impostata come qualsiasi altra società. Il piano dei conti è indipendente dal piano dei conti nelle business unit. Il piano dei conti nelle business unit può differire l'uno dall'altro. Impostare un elenco di società da consolidare, verificare i dati contabili prima di eseguire il consolidamento, importare da file o database e generare report relativi al consolidamento. Per ulteriori informazioni, vedere [Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Il consolidamento dei dati finanziari può risultare utile in particolare con i processi Intercompany. Per ulteriori informazioni, vedere [Gestione delle transazioni Intercompany](intercompany-manage.md).

## <a name="use-the-consolidated-trial-balance-report"></a><a name="use-the-consolidated-trial-balance-report"></a>Usare il report Bilancio di verifica consolidato

Il report **Bilancio di verifica consolidato** può fornire una panoramica dello stato finanziario generale dell'attività commerciale. Il report combina i movimenti di contabilità generale di ognuna delle società in una nuova società creata per i dati consolidati. Questa società è in genere detta *società consolidata*. La società consolidata è solo un contenitore per i dati unificati e non presenta dati aziendali dinamici. Le società incluse nella società consolidata diventano **business unit** nel report. Per ulteriori informazioni, vedere [Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md). Se hai al massimo quattro business unit, puoi anche utilizzare il report **Bil. di verif. consolidato (4)**.  

Il report mostra una riga per ogni conto e segue la struttura del piano dei conti. Un conto non viene visualizzato se tutti gli importi nella riga hanno valore 0. Il report visualizza per ogni conto le informazioni seguenti:

* Il nome e il numero del conto.
* I totali per la società consolidata e per ogni business unit. I totali possono essere visualizzati come saldo periodo e come saldo alla data.
* Le eliminazioni eseguite nella società consolidata. Le eliminazioni vengono sempre visualizzate per un periodo corrispondente all'anno fiscale della società consolidata.
* Il totale per la società consolidata in seguito alle eliminazioni, visualizzato sia come saldo periodo che come saldo alla data.

## <a name="consolidate-data"></a><a name="consolidate-data"></a>Consolidare i dati

Il trasferimento dei dati dalle business unit alla società consolidata è l'effettivo *consolidamento*. Prima del consolidamento è consigliabile controllare se vi sono differenze tra le informazioni di base nelle business unit e nella società consolidata. Sono disponibili due report utilizzabili per verificare il database e il file.

### <a name="to-test-the-data-before-you-consolidate"></a><a name="to-test-the-data-before-you-consolidate"></a>Per verificare i dati prima del consolidamento

Verifica i dati prima di trasferirli alla società consolidata. [!INCLUDE[prod_short](includes/prod_short.md)] cerca le differenze tra le informazioni delle business unit e quelle della società consolidata. Ad esempio, se i numeri di conto o i codici di dimensione sono diversi. È necessario correggere gli eventuali errori prima di eseguire il report. È possibile verificare il database oppure, se si importano dati da un file XML, il file in questione.  

1. Aprire la società consolidata.  
2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Business unit**, quindi scegli il collegamento correlato.  
3. Testa il file e il database, come segue:  

    * Per verificare un file, scegliere l'azione **Test file**, immettere il nome del file da verificare, quindi scegliere **Stampa**.  
    * Per verificare il database, scegliere **Test database**.  

### <a name="run-the-consolidation"></a><a name="run-the-consolidation"></a>Eseguire il consolidamento

Dopo aver testato i dati, è possibile trasferirli alla società consolidata.  

1. Accedere alla società consolidata.  
2. In **Gestione ruolo utente Contabile**, scegliere l'azione **Esegui consolidamento**.  
3. Compilare i campi necessari.  
4. Nella sezione Filtro, impostare un filtro per il nome della business unit o della società pertinente.  
5. Facoltativamente, programmare l'esecuzione di un report in un orario comodo.  

## <a name="eliminate-repeated-transactions"></a><a name="eliminate-repeated-transactions"></a>Eliminare transazioni ripetute

Dopo avere eseguito il consolidamento delle società, è necessario trovare ed eliminare le transazioni registrate più di una volta nelle società. L'elaborazione delle eliminazioni in seguito al consolidamento è un processo manuale.  

Per eliminare transazioni ripetute:

1. Individua le transazioni che potenzialmente devono essere rettificate e immetti le righe delle registrazioni COGE per eliminarle.
2. Eseguire il report **Eliminaz. consolidamenti C/G** per valutare l'effetto delle righe delle registrazioni COGE prima della registrazione.
3. Registrare le transazioni di rettifica.

Il report **Eliminazioni consolidamento C/G** visualizza un bilancio di verifica provvisorio in cui è possibile simulare le conseguenze dell'eliminazione dei movimenti. Il report confronta i movimenti nella società consolidata con le eliminazioni registrate nel giornale di registrazione COGE.

Prima di poter includere una business unit nel report è necessario impostarla nella pagina **Business Unit**. Il campo **Consolida** deve essere selezionato.

Viene creata una riga per ogni conto secondo la struttura del piano dei conti. Un conto non viene visualizzato se tutti gli importi nella riga hanno valore 0. Per ogni conto vengono visualizzate le informazioni seguenti:

* Numero conto.
* Nome conto.
* Se sono stati selezionati uno o più codici di business unit nel campo **Codice Business Unit** della pagina di richiesta, viene visualizzato un totale per la società consolidata, escluse le business unit e le eliminazioni selezionate. Se il campo **Codice Business Unit** non è stato compilato, viene visualizzato un totale per la società consolidata escluse le eliminazioni.
* Se è stato selezionato un codice di business unit nel campo **Codice Business Unit** nella pagina di richiesta, viene visualizzato un totale per i movimenti importati dalla business unit. Se il campo **Codice Business Unit** non è stato compilato, viene visualizzato un totale per le eliminazioni registrate nella società consolidata.
* Il totale relativo alla società consolidata comprese tutte le business unit e le eliminazioni registrate.
* Le eliminazioni da eseguire nella società consolidata. Ovvero, le voci nel giornale di registrazione generale selezionato nella pagina della richiesta.
* Il testo di registrazione copiato dalle registrazioni generali.
* Il totale della società consolidata in seguito alle eliminazioni, nel caso vengano registrate.

## <a name="export-and-import-consolidated-data-between-databases"></a><a name="export-and-import-consolidated-data-between-databases"></a>Esportare e importare dati consolidati tra database

Se i dati di una business unit si trovano in un database diverso, è necessario esportarli in un file prima di includerli nel consolidamento. Ogni società deve essere esportata separatamente. A questo scopo, viene utilizzato il processo batch **Esporta consolidamento**.  

> [!TIP]
> Utilizzare lo stesso processo per esportare i dati consolidati che devono essere inviati a Dynamics 365 Finance, ad esempio se l'attuale business unit è una filiale e la società madre utilizza Dynamics 365 Finance.

Dopo avere eseguito il processo batch, vengono elaborati tutti i movimenti dei conti di contabilità generale. Per ogni combinazione di dimensioni selezionate e data, i contenuti dei campi **Importo** dei movimenti vengono sommati ed esportati. Viene elaborata la combinazione successiva delle dimensioni e della data selezionate con lo stesso numero di conto. Quindi vengono elaborate le combinazioni del numero di conto successivo e così via.  

I movimenti esportati contengono i seguenti campi: **Nr. conto**, **Data di registrazione** e **Importo**. Se sono state esportate anche informazioni sulle dimensioni, vengono inclusi anche i codici e i valori delle dimensioni.  

1. Per ogni riga esportata, se il totale dei campi **Importo** è in dare, il numero di conto impostato nel campo **Conto consol. dare** viene esportato nella riga. Se l'importo totale è un credito, il numero corrispondente nel campo **Conto consol. avere** viene esportato nella riga.  
2. La data utilizzata per ogni riga esportata è quella di fine del periodo oppure, se il trasferimento avviene giornalmente, la data esatta del calcolo.  
3. Il valore delle dimensioni esportato per il movimento sarà il valore delle dimensioni della società consolidata specificato nel campo **Cod. consolidamento** per tale valore. Se nel campo **Cod. consolidamento** non è stato immesso un valore delle dimensioni della società consolidata per tale valore, nella riga verrà esportato il valore delle dimensioni stesso.  
4. I file XML, inoltre, contengono i tassi di cambio valuta inclusi nel periodo di consolidamento. I tassi sono inclusi in una sezione separata all'inizio del file.  

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Impostare il consolidamento di una società](finance-consolidated-company-reporting-setup.md)  
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
