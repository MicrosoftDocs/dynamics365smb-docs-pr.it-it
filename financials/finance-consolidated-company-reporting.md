---
title: "Consolidare i dati di molteplici società | Microsoft Docs"
description: "Ottenere una visualizzazione di riepilogo dello stato finanziario delle proprie società."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 07/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c4b5a37bb7544d747e9411599ad590f4757942df
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Consolidare dati finanziari di molteplici società
Se si hanno più società in [!INCLUDE[d365fin](includes/d365fin_md.md)], il report Bilancio di verifica consolidato nella Gestione ruolo utente Contabile può fornire una panoramica dello stato finanziario dell'attività commerciale globale.  

Il report combina i movimenti di contabilità generale di ognuna delle società in una nuova società creata per contenere i dati consolidati. Questa società è in genere detta "società consolidata". La società consolidata è solo un contenitore per i dati unificati e non presenta dati aziendali dinamici. Le società incluse nella società consolidata diventano **business unit** nel report.

Il consolidamento dei dati finanziari può risultare utile in particolare con i processi Intercompany. Per ulteriori informazioni, vedere [Gestione delle transazioni Intercompany](intercompany-manage.md).

È possibile eseguire il consolidamento:  

* Per le società che hanno piani dei conti differenti.  
* Per le società che utilizzano anni fiscali e valute differenti.  
* Dell'importo completo o di una percentuale delle informazioni finanziarie di una società
* Utilizzando differenti tassi di cambio delle valute in singoli conti C/G

In base alla complessità delle proprie società, esistono due modi per impostare il report:

* Se non sono necessarie impostazioni avanzate, come includere una società di cui si possiede solo una parte, è possibile utilizzare la guida al setup assistito **Consolidamento società** per impostare rapidamente un consolidamento. La guida consente di eseguire le operazioni di base.
* Se sono necessarie impostazioni più avanzate, è possibile eseguire un setup personalizzato della società consolidata e delle business unit.

## <a name="to-do-a-simple-consolidation-setup"></a>Per eseguire un setup semplice del consolidamento
Se il consolidamento è semplice, ad esempio perché si è il solo proprietario delle business unit da consolidare, la guida al setup assistito **Consolidamento società** consente l'esecuzione delle seguenti operazioni:

* Scegliere se creare una nuova società consolidata, oppure se consolidare i dati in una società già creata per il consolidamento. La società non deve contenere transazioni.
* Visualizzare un'anteprima dei risultati. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica la possibilità di trasferire correttamente transazioni e dati master alla società consolidata.

Per utilizzare la guida al setup assistito, attenersi a questa procedura:

1. Nella Gestione ruolo utente **Contabile**, scegliere l'azione **Setup assistito**.
2. Scegliere **Imposta creazione di report di consolidamento**, quindi completare ogni passaggio nella guida al setup assistito.

## <a name="to-do-an-advanced-consolidation-setup"></a>Per eseguire un setup avanzato del consolidamento
Se sono necessarie impostazioni più avanzate per il consolidamento, è possibile impostare il consolidamento manualmente. Ad esempio, se si possiedono solo parzialmente alcune società o se non si intende includere alcune società nel consolidamento. Una società consolidata può essere impostata come qualsiasi altra società. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] consente di impostare un elenco di società da consolidare, verificare i dati contabili prima di eseguire il consolidamento, importare file e generare report relativi al consolidamento.  

1. Accedere alla società consolidata.
2. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Business Unit**, quindi scegliere il collegamento correlato.  
3. Scegliere **Nuovo** e compilare i campi necessari.  

Se una business unit utilizza una valuta straniera, è necessario specificare il tasso di cambio da utilizzare nel consolidamento. È inoltre necessario immettere le informazioni di consolidamento nei conti C/G della business unit. Tali processi sono descritti nelle sezioni riportate di seguito.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Per preparare conti di contabilità generale per il consolidamento
Se il piano dei conti nella business unit differisce dalla società consolidata, è necessario preparare conti di contabilità generale per il consolidamento. È possibile specificare i conti in cui registrare debiti e crediti nonché il metodo da utilizzare per convertire le valute nella società consolidata. Ciò è utile se, ad esempio, si esegue spesso il report.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.  
2. Aprire la scheda del conto e compilare i campi della Scheda dettaglio **Consolidamento**.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Per specificare i tassi di cambio per i consolidamenti
Se una business unit utilizza una valuta diversa rispetto alla società consolidata, è necessario specificare i metodi dei tassi di cambio per ogni conto prima di eseguire il consolidamento. Per ogni conto, il contenuto del campo **Metodo conversione consol.** determina il tasso di cambio. Nel campo **Tabella tasso di cambio valuta** di ogni scheda business unit specificare se per il consolidamento saranno utilizzati i tassi di cambio della business unit o della società consolidata. Se si utilizzano i tassi di cambio della società consolidata, è possibile modificare i tassi di cambio per una business unit. Per le business unit, se nel campo **Tabella tasso di cambio valuta** della scheda business unit è indicato **Locale**, è possibile modificare il tasso di cambio nella scheda stessa. I tassi di cambio vengono copiati dalla tabella **Tassi di cambio valute**, ma è possibile modificarli prima del consolidamento.

Nella tabella seguente sono descritti i metodi dei tassi di cambio che è possibile utilizzare per i conti.

|Tasso di cambio | Uso tipico |
|---|---|
|Tasso medio (manuale) | il tasso medio per il periodo da consolidare viene calcolato manualmente. La media viene calcolata come media matematica o come valore approssimativo e viene specificata per ogni business unit. È utilizzato per i conti economici.|
|Tasso di chiusura | Utilizzato per i conti di bilancio patrimoniale.|
|Ultimo tasso di chiusura | Il tasso valido nel mercato del cambio estero alla data per cui lo stato patrimoniale o il conto economico viene preparato. Questo tasso viene specificato per ogni business unit. Utilizzato per i conti di bilancio patrimoniale.|
|Tasso storico | Il tasso di cambio valido al momento della transazione.|
|Tasso composito | Gli importi del periodo corrente vengono convertiti sulla base del tasso medio e aggiunti al saldo precedentemente registrato nella società consolidata. Questo metodo viene solitamente utilizzato per conti utili non distribuiti, poiché includono importi relativi a periodi diversi e sono quindi costituiti da importi convertiti con diversi tassi di cambio.|
|Tasso equo | È analogo al tasso **composito**. Le differenze sono registrate in conti di contabilità generale separati.|   

Per specificare i tassi di cambio per le business unit, attenersi alla seguente procedura:

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Business Unit**, quindi scegliere il collegamento correlato.  
2. Nella pagina **Lista business unit**, scegliere la business unit, quindi l'azione **Tasso medio (manuale)**.   
3. Nella pagina **Modifica tasso di cambio**, il campo **Importo tasso cambio relativo** contiene valori copiati dalla tabella **Tassi di cambio valute**, ma è possibile modificarli. Chiudere la pagina.  
4. Scegliere l'azione **Tasso di chiusura**.  
5. Nel campo **Importo tasso cambio relativo**, immettere il tasso di cambio.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Per escludere una società dal consolidamento
Se non si desidera includere una business unit nel consolidamento, è possibile escluderla. A questo proposito, passare alla scheda business unit e deselezionare la casella di controllo **Consolidare**.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Per includere una società di cui si possiede soltanto una parte
Se si possiede solo una parte di una società, è possibile includere una percentuale di ogni transazione che corrisponde alla percentuale della società di cui si è possessore. Ad esempio, se si possiede il 70% della società, il consolidamento includerà € 70 di una fattura di € 100. Per specificare la percentuale della società posseduta, passare alla scheda business unit e immettere la percentuale nel campo **% consolidamento**.  

### <a name="to-test-the-data-before-you-consolidate"></a>Per verificare i dati prima del consolidamento
È possibile verificare i dati prima di trasferirli alla società consolidata. [!INCLUDE[d365fin](includes/d365fin_md.md)] cerca le differenze tra le informazioni delle business unit e quelle della società consolidata. Ad esempio, se i numeri di conto o i codici di dimensione sono diversi. È necessario correggere gli eventuali errori prima di eseguire il report. È possibile verificare il database oppure, se si importano dati da un file XML, il file in questione.   

1. Aprire la società consolidata.  
2. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Business Unit**, quindi scegliere il collegamento correlato.  
3. Effettuare una delle seguenti operazioni:  

    * Per verificare un file, scegliere l'azione **Test file**, immettere il nome del file da verificare, quindi scegliere **Stampa**.  
    * Per verificare il database, scegliere **Test database**.  

## <a name="to-run-the-consolidation"></a>Per eseguire il consolidamento
Dopo aver verificato i dati, è possibile trasferirli alla società consolidata.  

1. Accedere alla società consolidata.  
2. In **Gestione ruolo utente Contabile**, scegliere l'azione **Esegui consolidamento**.  
3. Compilare i campi necessari.  
4. Nel campo **Dove**, scegliere **Nome Società**, quindi scegliere la società consolidata nel campo **è**.  

## <a name="to-export-and-import-consolidated-data-between-databases"></a>Per esportare e importare dati consolidati tra database
Se i dati di una business unit si trovano in un database diverso, è necessario esportarli in un file prima di includerli nel consolidamento. Ogni società deve essere esportata separatamente. A questo scopo, viene utilizzato il processo batch **Esporta consolidamento**.  

Dopo avere eseguito il processo batch, vengono elaborati tutti i movimenti dei conti di contabilità generale. Per ogni combinazione di dimensioni selezionate e data, i contenuti dei campi **Importo** dei movimenti vengono sommati ed esportati. La combinazione successiva di dimensioni selezionate e data con lo stesso numero di conto viene elaborata, quindi vengono elaborate le combinazioni con il numero di conto successivo e così via.  

I movimenti esportati contengono i seguenti campi: **Nr. conto**, **Data di registrazione** e **Importo**. Se sono state esportate anche informazioni sulle dimensioni, vengono inclusi anche i codici e i valori delle dimensioni.  

1. Per ogni riga esportata, se il totale dei campi **Importo** è in dare, il numero di conto impostato nel campo **Conto consol. dare** viene esportato nella riga. Se l'importo totale è un credito, il numero corrispondente nel campo **Conto consol. avere** viene esportato nella riga.  
2. La data utilizzata per ogni riga esportata è quella di fine del periodo oppure, se il trasferimento avviene giornalmente, la data esatta del calcolo.  
3. Il valore delle dimensioni esportato per il movimento sarà il valore delle dimensioni della società consolidata impostato nel campo **Cod. consolidamento** per tale valore. Se nel campo **Cod. consolidamento** non è stato immesso un valore delle dimensioni della società consolidata per tale valore, nella riga verrà esportato il valore delle dimensioni stesso.   
4. I file XML, inoltre, contengono i tassi di cambio valuta inclusi nel periodo di consolidamento. I tassi sono inclusi in una sezione separata all'inizio del file.

## <a name="see-also"></a>Vedi anche
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)

