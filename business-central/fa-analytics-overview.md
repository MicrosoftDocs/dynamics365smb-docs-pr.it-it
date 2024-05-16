---
title: Analisi dei cespiti
description: 'Scopri come raccogliere, analizzare e condividere dati sui cespiti per la business intelligence.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analisi dei cespiti

Le aziende con cespiti acquisiscono molti dati su di essi durante le attività quotidiane. Questi dati supportano una preziosa business intelligence (BI) per i gestori di cespiti:

- Acquisizioni di cespiti
- Ammortamenti di cespiti
- Assicurazione e riparazioni
- Budget per cespiti

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce funzionalità che facilitano la raccolta, l'analisi e la condivisione dei dati sui cespiti dell'organizzazione:

- Reporting finanziario (per rendiconti finanziari e indicatori KPI su conti cespiti)
- Analisi ad hoc negli elenchi
- Analisi ad hoc dei dati in Excel (utilizzando Apri in Excel)
- Strumenti di analisi di cespiti predefiniti
- Report sui cespiti predefiniti

> [!NOTE]
> L'analisi per i cespiti è leggermente diversa rispetto ad altre aree. Devi analizzare i dati già presenti, come acquisizioni di asset, ammortamenti e assicurazioni, ma anche dati su operazioni future, come ammortamenti e il ritiro dei cespiti. Per quest'ultimo tipo di analisi, [!INCLUDE[prod_short](includes/prod_short.md)] include report integrati in grado di calcolare questi numeri.

Ogni funzionalità presenta vantaggi e svantaggi, a seconda del tipo di analisi dei dati e del ruolo dell'utente. Per ulteriori informazioni, vedi [Panoramica di analisi, business intelligence e reporting](reports-bi-reporting.md).

In questo articolo vengono descritte le modalità di utilizzo di queste funzionalità analitiche per ottenere informazioni dettagliate sui cespiti.

## Esigenze analitiche nella gestione dei cespiti

Quando si pensa alle esigenze di analisi nella gestione dei cespiti, potrebbe essere utile utilizzare un modello basato su utenti tipo che descrive le esigenze di analisi ad alto livello.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrazione di diversi utenti tipo per l'analisi" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Persone che ricoprono ruoli diversi hanno esigenze diverse in termini di dati e li utilizzano in modi diversi. Ad esempio, gli addetti alla gestione dei cespiti e alla finanza interagiscono con i dati in modo diverso rispetto agli addetti alle vendite.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrazione di come utenti tipo diversi hanno esigenze di analisi diverse." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Ruolo              | Aggregazione dei dati  | Modi tipici di consumare dati                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|DF / DO / DG                 | Dati sulle prestazioni  | KPI <br> Dashboard <br> Report finanziari           |
|Gestione cespiti/Controller   | Tendenze, sintesi | Report manageriali predefiniti <br> Analisi ad hoc      | 
|Addetto contabile                      | Dati dettagliati     | Report operativi predefiniti <br> Dati delle attività visualizzate |

## Indicatori KPI di gestione cespiti

Un indicatore KPI è un valore misurabile che mostra l'efficacia con cui stai raggiungendo i tuoi obiettivi. Nella gestione dei cespiti, le persone spesso utilizzano i seguenti indicatori KPI per monitorare l'uso dei cespiti della propria organizzazione:

- Fatturato cespiti totale
- Rendimento dei cespiti

## Utilizzare il reporting finanziario per produrre rendiconti finanziari e indicatori KPI relativi ai cespiti

La funzionalità **Reporting finanziario** fornisce informazioni dettagliate sui dati finanziari mostrati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget. Specificamente per la gestione dei cespiti, puoi impostare report finanziari sui conti C/G utilizzati per tenere traccia delle registrazioni dei cespiti.

Le dimensioni svolgono un ruolo importante nella business intelligence. Una dimensione corrisponde ai dati che puoi aggiungere a un movimento come parametro. Le dimensioni ti consentono di raggruppare movimenti con caratteristiche simili, ad esempio clienti, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Tra altri scopi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano report finanziari. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

Per ulteriori informazioni sul reporting finanziario, vedi [Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md).

## Reporting finanziario in business unit o persone giuridiche (relative ai cespiti)

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)]nelle filiali che generano report per le organizzazioni padre. [!INCLUDE [prod_short](includes/prod_short.md)] offre ai contabili strumenti che li aiutano a trasferire i movimenti C/G da due o più società (filiali) a una società consolidata. In particolare per la gestione dei cespiti, potresti voler consolidare i movimenti C/G per i tuoi conti cespiti per tenere traccia degli indicatori KPI dei cespiti in business unit o persone giuridiche.

Per ulteriori informazioni, vedi [Consolidamento della società](finance-consolidated-company-reporting.md).

## Analisi ad hoc dei dati dei cespiti

A volte, devi solo verificare se i numeri si sommano correttamente o confermare rapidamente una cifra. Le seguenti funzionalità sono ottime per le analisi ad hoc:

- Analisi dei dati nelle pagine degli elenchi di contabilità
- Apri in Excel

La funzionalità Analisi dati ti consente di aprire quasi tutte le pagine di elenco, ad esempio **Movimenti C/G** o **Movimenti contabili cespiti**, accedere alla modalità di analisi e quindi raggruppare, filtrare e ruotare i dati come necessario.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili cespiti per visualizzare il valore di un cespite." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

Allo stesso modo, puoi usare l'azione **Apri in Excel** per aprire una pagina di elenco per i movimenti C/G, eventualmente filtrare l'elenco in un sottoinsieme di dati e quindi utilizzare Excel per utilizzare i dati. Ad esempio, utilizzando funzionalità come Analizza dati, Analisi what-if o Foglio previsioni.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Se configuri OneDrive per le funzionalità di sistema, la cartella di lavoro di Excel si apre nel browser usando Excel per il Web. 

Per ulteriori informazioni su come eseguire analisi ad hoc sui registri dei cespiti, vedi [Analisi ad hoc dei cespiti](ad-hoc-analysis-fa.md).


## Report predefiniti per cespiti

[!INCLUDE [prod_short](includes/prod_short.md)] include diversi report predefiniti, funzioni di tracciamento e strumenti utili per i revisori o i controllori che generano report sui cespiti.

Per ottenere una panoramica dei report disponibili, scegli **Tutti i report** nella parte superiore della tua home page. Questa azione apre la pagina Esplora ruoli, il cui contenuto viene filtrato in base alle funzionalità nell'opzione **Report e analisi**. Per trovare report relativi ai cespiti, nel campo **Trova**, immetti **cespiti**. Per ulteriori informazioni, vedi [Ricerca di report con Esplora ruoli](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Esempio di report sul centro ruoli finanziario." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Per ulteriori informazioni sui report relativi ai cespiti, vedi [Report integrati sui cespiti](fa-reports.md).

## Analisi dei cespiti visualizzati

[!INCLUDE [prod_short](includes/prod_short.md)] include varie pagine che forniscono panoramiche sugli acquisti e attività da svolgere. Ecco alcuni esempi per iniziare:

- [Calcolo dell'ammortamento, registrazione dell'ammortamento e analisi dell'ammortamento.](fa-how-depreciate-amortize.md)
- [Monitorare i costi di manutenzione](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Monitorare la copertura assicurativa](fa-how-insure.md#to-monitor-insurance-coverage)
- [Visualizzare i valori del registro beni ammortizzabili modificati](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Visualizzare i movimenti contabili di cessione](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Visualizzare i valori di cessione previsti](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### Mostrare movimenti e saldi di contabilità generale relativi ai cespiti dalla pagina Piano dei conti

La pagina Piano dei conti mostra tutti i conti C/G con numeri aggregati nella contabilità generale. Da questa pagina puoi fare cose come:  

- Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
- Esaminare un elenco delle categorie di registrazione per il conto in questione.
- Visualizza i saldi attivi e passivi separatamente per un singolo conto.

Specificamente per i cespiti, puoi creare una visualizzazione nella pagina Piano dei conti che mostri solo i conti utilizzati per registrare movimenti di cespiti.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esempio di come la pagina Piano dei conti mostra informazioni finanziarie" lightbox="media/chart-of-accounts-page.png":::

Per saperne di più, vedi [Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)

### Analizzare i dati per dimensioni (relative ai cespiti)

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio registrazioni di cespiti. Ad esempio, le dimensioni possono indicare il reparto o l'ubicazione di provenienza del movimento.  

Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto o ubicazione, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare una struttura complessa del piano dei conti.

Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)

## Vedere anche

[Gestione dei report finanziari in business unit o persone giuridiche](finance-consolidated-company-reporting.md)  
[Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)  
[Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)  
[Analisi ad hoc dei dati dei cespiti](ad-hoc-analysis-fa.md)   
[Report sui cespiti predefiniti](fa-reports.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
