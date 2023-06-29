---
title: Analisi dei dati del report con Excel e XML
description: Scopri come utilizzare Excel e XML per analizzare un set di dati di report.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml"></a><a name="analyzing-report-data-with-excel-and-xml"></a>Analisi dei dati del report con Excel e XML

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

In qualità di sviluppatore o utente avanzato, è utile esaminare i dati generati per un determinato set di dati di report mentre crei nuovi report o modifichi quelli esistenti. Per supportare questa funzionalità, puoi esportare un set di dati di report come dati non elaborati in una cartella di lavoro di Excel o in un file XML, direttamente. In Excel, ad esempio puoi quindi eseguire analisi ad hoc dei dati e diagnosticare i problemi.

## <a name="get-started"></a><a name="get-started"></a>Inizia

Per esportare un set di dati del report in una cartella di lavoro di Excel o in un file XML, apri il report nel client, quindi nella pagina di richiesta seleziona **Invia a** > **Documento Microsoft Excel (solo dati)** o **Documento XML**. Il file viene scaricato sul dispositivo.

## <a name="more-about-excel-data-only"></a><a name="more-about-excel-data-only"></a>Maggiori informazioni su Excel (solo dati)

L'opzione **Documento di Microsoft Excel (solo dati)** esporta i risultati del report e i criteri utilizzati per generarli, ma non include il layout del report. Il file Excel includerà l'intero set di dati, come dati non elaborati, organizzato in righe e colonne. Sono incluse tutte le colonne di dati del set di dati del report, indipendentemente dal fatto che siano utilizzate nel layout del report.

Una volta creato il file di Excel puoi iniziare ad analizzare i dati. Ad esempio, puoi filtrare i dati e utilizzare Power Pivot per visualizzarli.

Ogni volta che esporti i risultati, viene creato un nuovo foglio di lavoro. Usando l'opzione **Documento Microsoft Excel (solo dati)** puoi eseguire lo stesso report e riutilizzare le modifiche alla formattazione. Ad esempio, per Power Pivot, puoi eseguire nuovamente il report per un altro periodo di tempo, copiare i risultati nel foglio di lavoro e quindi aggiornare il foglio di lavoro. Puoi anche trovare un'app per la creazione di report in [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Non puoi esportare un report con più di 1.048.576 righe o 16.384 colonne. Con Business Central in locale, il numero massimo di righe esportate potrebbe essere anche inferiore. Business Central Server include un'impostazione di configurazione, denominata **Numero massimo di righe di dati consentite per l'invio a Excel**, per diminuire il limite del valore massimo. Per ulteriori informazioni, vedi [Configurazione di Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) oppure contatta il tuo amministratore.

## <a name="for-administrators"></a><a name="for-administrators"></a>Per gli amministratori

- **Documento Microsoft Excel (solo dati)** è stato introdotto come funzionalità facoltativa nel primo ciclo di rilascio del 2021, aggiornamento 18.3. Per consentire agli utenti l'accesso a questa funzione con il primo ciclo di rilascio del 2021, abilita aggiornamento della funzionalità **Salva set di dati del report in documento di Microsoft Excel** in**Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management). Nel secondo ciclo di rilascio del 2021, questa funzione è diventata permanente, quindi non dovrai abilitarla.

- Per usare **Documento Microsoft Excel (solo dati)**, gli account utente richiedono l'autorizzazione **Consenti l'azione Esporta set di dati del report in Excel**. Puoi concedere agli utenti questa autorizzazione assegnando il set di autorizzazioni **Strumenti per la risoluzione dei problemi** o **Esporta report in Excel**. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  

## <a name="for-developers-and-advanced-users"></a><a name="for-developers-and-advanced-users"></a>Per gli sviluppatori e gli utenti avanzati

L'opzione **Documento Microsoft Excel (solo dati)** esporta tutte le colonne, comprese le colonne che contengono filtri e istruzioni di formattazione per altri valori. Ecco alcuni punti di interesse:

- I dati binari in un campo, come un'immagine, non vengono esportati.

  Nelle colonne che contengono dati binari, i campi includeranno il testo **Dati binari ({0} byte)**, dove **{0}** indica il numero di byte.
- A partire dal secondo ciclo di rilascio di Business Central 2021, il file Excel include anche il foglio di lavoro **Metadati del report**.

  Questo foglio di lavoro mostra i filtri applicati al report e le proprietà generali del report, come il nome, l'ID e i dettagli dell'estensione. I filtri sono mostrati nella colonna **Filtro (DataItem::Table::FilterGroupNo::FieldName)**. I filtri in questa colonna includono i filtri impostati nella pagina di richiesta del report. Include anche i filtri definiti nel codice AL, ad esempio, dalla [proprietà DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) e dalla [proprietà DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Per ulteriori informazioni sulla progettazione del report, vedi [Panoramica dei report](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Utilizzo dei report](ui-work-report.md)  
[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
