---
title: Utilizzo dei layout di Excel
description: Scopri come creare e modificare i layout di report creati con Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 45f321afeb411eee4cb9f9dd215cefc393f58458
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529570"
---
# <a name="working-with-excel-layouts"></a>Utilizzo dei layout di Excel

I layout di report di Excel si basano sulle cartelle di lavoro Microsoft Excel (file .xlsx). Consentono di creare report utilizzando le familiari funzionalità di Excel per il riepilogo, l'analisi e la presentazione dei dati, come formule, tabelle pivot e grafici pivot.

![Mostra un esempio di layout di Excel.](media/excel-layout-2.png)

Questo articolo spiega alcune delle cose più importanti che devi sapere per iniziare a usare i layout di Excel.

## <a name="why-use-excel-layouts"></a>Perché utilizzare i layout di Excel?

Ecco alcuni altri vantaggi dell'utilizzo dei layout di Excel:

- Creare report interattivi utilizzando visualizzazioni come filtri dei dati
- Visualizzare i dati non elaborati dal set di dati del report per comprendere come funziona il report e da dove provengono i dati degli oggetti visivi
- Utilizza le funzionalità integrate di Office per eseguire la post-elaborazione dei report sottoposti a rendering, ad esempio:
  - [Protezione dei fogli di lavoro](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Applicazione di etichette di sensibilità](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Aggiunta di commenti e note](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Previsione e analisi](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Usa i componenti aggiuntivi installati e le integrazioni di app, come flussi Power Automate o OneDrive.

## <a name="get-started"></a>Inizia

Ci sono fondamentalmente due attività coinvolte nella creazione di un layout di Excel su un report:

1. Crea il nuovo file di layout di Excel.
2. Aggiungi il nuovo layout al report.

## <a name="task-1-create-the-excel-layout-file"></a>Attività 1. Crea il nuovo file di layout di Excel

Esistono tre modi per creare un file di layout Excel per un report, come spiegato in questa sezione

### <a name="from-any-report"></a>[Da un report](#tab/any-report)

È possibile utilizzare i passaggi seguenti per creare un layout di Excel da un report, indipendentemente dal tipo di layout corrente. Il layout di Excel conterrà il foglio **Dati** necessario e una tabella, un foglio **Metadati del report** e nient'altro.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Nell'elenco **Layout report** seleziona un layout per il report quindi scegli l'azione **Esegui report**.
3. Nella pagina della richiesta di report, seleziona **Invia a** > **Documento di Microsoft Excel (solo dati)** > **OK**.

   Questo passaggio scarica una cartella di lavoro di Excel che contiene il set di dati del report.
4. Apri il file scaricato in Excel, apporta le modifiche e salva il file.

### <a name="from-another-excel-layout-on-a-report"></a>[Da un altro layout di Excel su un report](#tab/other-layout)

Se esiste già un layout di Excel per un report, utilizza il layout esistente come punto di partenza. Esistono due approcci per ottenere una copia del layout. È possibile esportare il layout esistente dalla pagina **Layout report** o scaricare il layout dalla pagina di richiesta del report. In entrambi i modi scarichi un file di layout di Excel che include tutti i fogli del file esistente. La differenza è che dalla pagina di richiesta, il layout includerà i dati effettivi. I dati non sono necessari, ma aiutano durante la progettazione del layout.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Approccio 1: esportare il layout dalla pagina **Layout report**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleziona il layout di Excel dall'elenco, quindi scegli l'azione **Esporta layout** nella parte superiore della pagina.
3. Apri il file in Excel, apporta le modifiche e salva il file.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Approccio 2: scaricare il layout dalla pagina di richiesta di report

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Nell'elenco **Layout report** seleziona un layout per il report quindi scegli l'azione **Esegui report**.
3. Nella pagina di richiesta di report, seleziona **Scarica**.
4. Apri il file in Excel, apporta le modifiche e salva il file.

### <a name="from-al-code"></a>[Dal codice AL](#tab/from-code)

Questo modo è il più avanzato. Richiede la conoscenza del codice AL, quindi si rivolge ai programmatori. I layout di Excel, in questo caso, fanno parte di un pacchetto di estensione che devi installare. Per ulteriori informazioni, vedi [Creazione di un report con layout di Excel](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) nella Guida per sviluppatori e professionisti IT.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Attività 2. Aggiungi il nuovo file di layout al report

Una volta ottenuto il file di layout di Excel, l'attività successiva consiste nell'aggiungerlo come nuovo layout per il report.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleziona **Nuovo layout**.
3. Imposta **ID report** sul report.
4. Immetti un nome in **Nome layout**.
5. Imposta **Opzioni di formattazione** su **Excel**.
6. Seleziona **OK** > **Scegli** di aprire Esplora file sul tuo dispositivo. 
7. Trova e seleziona il file di Excel quindi seleziona **Apri**.

   Il file selezionato viene caricato nel layout e torni alla pagina **Layout report**.
8. Se vuoi vedere come appare il report con il nuovo layout, seleziona il layout nell'elenco, quindi seleziona **Esegui report**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Informazioni sui layout di Excel

Ci sono alcune cose che dovresti sapere o considerare quando inizi a creare o apportare modifiche ai layout di Excel. Ogni layout di Excel deve includere due elementi: un foglio **Dati** e una tabella **Dati**. Questi elementi formano la base del layout definendo i dati aziendali da Business Central con cui puoi lavorare. Puoi pensare al foglio **Dati** come un tipo di contratto per il layout nei dati aziendali. Utilizzerai questi dati come fonte di calcoli e visualizzazioni che desideri presentare in altri fogli.

Esistono alcuni requisiti specifici per la struttura della cartella di lavoro di Excel. Se i requisiti non sono soddisfatti, avrai problemi nell'utilizzo del layout. Il diagramma e la tabella seguenti delineano gli elementi di un layout di Excel e i requisiti.

[![Mostra i diversi elementi di un layout di Excel.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|No.|Elemento|Descrizione|Obbligatorio|
|---|-------|----|---|
|1|Foglio **Dati**|<ul><li>Deve avere il nome **Dati**</li><li>Può includere solo una tabella e la tabella deve essere denominata **Dati**</li></ul>|![È obbligatorio](media/check.png) | 
|2|Tabella **Dati**|<ul><li>Deve avere il nome **Dati**</li><li>Deve avere almeno una colonna.</li><li>Può includere solo colonne che si trovano nel set di dati del report.</li><li>Deve iniziare nella prima cella **A1** del foglio **Dati**</li></ul>|![È obbligatorio](media/check.png)|
|3|Fogli di presentazione|<ul><li>Utilizzati per presentare i dati.</li><li>I dati provengono dal foglio **Dati**. </li></ul>||
|4|Foglio **Metadati del report**|<ul><li>Inclusi automaticamente se il layout è stato creato esportando un altro report come Excel</li><li>Contiene le informazioni generali sul report</li><li>Può essere eliminato</li></ul>|

Per riassumere cosa puoi e non puoi fare sul foglio **Dati**:

- Non cambiare il nome del foglio **Dati** della tabella **Dati** o delle colonne.
- Puoi eliminare o nascondere le colonne.
- Non aggiungere colonne a meno che non siano incluse nel set di dati del report.
- Puoi posizionare i fogli in qualsiasi ordine. Ad esempio, il foglio **Dati** può essere il primo o l'ultimo.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedi anche

[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Modificare il layout del report corrente](ui-how-change-layout-currently-used-report.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  
[Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analisi dei dati del report con Excel](report-analyze-excel.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
