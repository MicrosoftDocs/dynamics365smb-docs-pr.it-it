---
title: Analisi sugli acquisti
description: 'Business Central contiene molte funzionalità che ti consentono di raccogliere, analizzare e condividere dati sulle vendite preziosi per business intelligence e processo decisionale nell''organizzazione dedicata agli acquisti.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analisi sugli acquisti

Le aziende acquisiscono moltissimi dati durante le attività quotidiane che supportano la business Intelligence (BI) per i responsabili acquisti:

- Offerte acquisto
- Ordini acquisto
- Fatture di acquisto

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce funzionalità che facilitano la raccolta, l'analisi e la condivisione dei dati sugli acquisti dell'organizzazione.

- Analisi ad hoc negli elenchi
- Analisi ad hoc dei dati in Excel (utilizzando Apri in Excel)
- Report sulle vendite predefiniti

Ognuna di queste funzionalità presenta vantaggi e svantaggi, a seconda del tipo di analisi dei dati e del ruolo dell'utente. Per ulteriori informazioni, vedi [Panoramica di analisi, business intelligence e reporting](reports-bi-reporting.md).

Questo articolo illustra come utilizzare queste funzionalità analitiche per ottenere informazioni dettagliate sugli acquisti.

## Esigenze di analisi per gli acquisti

Quando pensi alle esigenze di analisi per gli acquisti, potrebbe essere utile utilizzare un modello basato su un utente tipo che descrive diverse esigenze di analisi ad alto livello.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrazione di diversi utenti per l'analisi" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Persone che ricoprono ruoli diversi hanno esigenze diverse in termini di dati e li utilizzano in modi diversi. Ad esempio, gli addetti alla gestione dei cespiti e alla finanza interagiscono con i dati in modo diverso rispetto agli addetti alle vendite.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrazione di come utenti tipo diversi hanno esigenze di analisi diverse." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Ruolo              | Aggregazione dei dati  | Modi tipici di consumare dati                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|DO / CSO / DF / DG    | Dati sulle prestazioni  | KPI <br> Dashboard <br> Report finanziari           |
|Manager acquisti      | Tendenze, sintesi | Report manageriali predefiniti <br> Analisi ad hoc      | 
|Responsabile acquisti/Addetto acquisti | Dati dettagliati     | Report operativi predefiniti <br> Dati delle attività visualizzate |

<!-- 
## Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## Utilizzare il reporting finanziario per produrre rendiconti finanziari e indicatori KPI (relativi agli acquisti)

La funzionalità **Reporting finanziario** fornisce informazioni dettagliate sui dati finanziari mostrati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget. Specificamente per gli acquisti, puoi impostare report finanziari sui conti C/G utilizzati per tenere traccia delle registrazioni degli acquisti.

Le dimensioni svolgono un ruolo importante nella business intelligence. Una dimensione corrisponde ai dati che puoi aggiungere a un movimento come parametro. Le dimensioni ti consentono di raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree e prodotti e quindi recuperare facilmente questi gruppi per l'analisi. Tra altri scopi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano report finanziari. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

Per ulteriori informazioni sui report finanziari, vedi [Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md).

## Reporting finanziario in business unit o persone giuridiche (relative agli acquisti)

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)] nelle filiali che devono generare report per le organizzazioni padre. [!INCLUDE [prod_short](includes/prod_short.md)] offre ai contabili strumenti che li aiutano a trasferire i movimenti C/G da due o più società (filiali) a una società consolidata. In particolare per la gestione degli acquisti, potresti voler consolidare i movimenti C/G per i tuoi conti acquisti per tenere traccia degli indicatori KPI di vendita in business unit o persone giuridiche.

Per ulteriori informazioni, vedi [Consolidamento della società](finance-consolidated-company-reporting.md).

## Analisi ad hoc dei dati sugli acquisti

A volte, devi solo verificare se i numeri si sommano correttamente o confermare rapidamente una cifra. Le seguenti funzionalità sono ottime per le analisi ad hoc:

- Analisi dei dati nelle pagine degli elenchi di contabilità
- Apri in Excel

La funzionalità **Analisi dati** ti consente di aprire quasi tutte le pagine di elenco, ad esempio **Ordini acquisto**, **Fatture di acquisto registrate**, **Movimenti contabili fornitori** o **Movimenti C/G**, accedere alla modalità di analisi e quindi raggruppare, filtrare e ruotare i dati come necessario.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili clienti." lightbox="media/data-analysis-vendor-ledger-entries.png":::

Allo stesso modo, puoi usare l'azione **Apri in Excel** per aprire una pagina di elenco, filtrare l'elenco in un sottoinsieme di dati e quindi utilizzare Excel per utilizzare i dati. Ad esempio, utilizzando funzionalità come Analizza dati, Analisi what-if o Foglio previsioni.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nei dati dei movimenti contabili clienti utilizzando Excel." lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Se configuri OneDrive per le funzionalità di sistema, la cartella di lavoro di Excel si apre nel browser.

Per ulteriori informazioni su come eseguire analisi ad hoc sui dati relativi agli acquisti, vedi [Analisi ad hoc dei dati sugli acquisti](ad-hoc-analysis-purchasing.md).

## Report predefiniti per gli acquisti

[!INCLUDE [prod_short](includes/prod_short.md)] include diversi report integrati, funzioni di tracciamento e strumenti per aiutare le organizzazioni dedicate agli acquisti a creare report sui propri dati.

Per ottenere una panoramica dei report disponibili, scegli **Tutti i report** nella parte superiore della tua home page. Questa azione apre Esplora ruoli, il cui contenuto viene filtrato in base alle funzionalità nell'opzione **Report e analisi**. Per ulteriori informazioni, vedi [Ricerca di report con Esplora ruoli](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Esempio di report in Gestione ruolo utente XXX." lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Per ulteriori informazioni sui report relativi agli acquisti, vedi [Report sugli acquisti integrati](purchase-reports.md).

## Analisi degli acquisti visualizzate

[!INCLUDE [prod_short](includes/prod_short.md)] include varie pagine che forniscono panoramiche sugli acquisti e attività da svolgere. Ecco un esempio per iniziare:

- [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)  
- [Calcolare le date per gli acquisti](purchasing-date-calculation-for-purchases.md)
- [Visualizzare i movimenti contabili di acquisto](purchasing-how-record-purchases.md#viewing-ledger-entries)


### Mostrare movimenti e saldi C/G relativi agli acquisti dalla pagina Piano dei conti

La pagina Piano dei conti mostra tutti i conti C/G con numeri aggregati registrati nella contabilità generale. Da questa pagina puoi fare cose come:  

- Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
- Esaminare un elenco delle categorie di registrazione per il conto in questione.
- Visualizza i saldi attivi e passivi separatamente per un singolo conto.

Specificamente per gli acquisti, puoi creare una visualizzazione nella pagina Piano dei conti che mostri solo i conti utilizzati per registrare movimenti di acquisto.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esempio di come la pagina Piano dei conti mostra informazioni finanziarie" lightbox="media/chart-of-accounts-page.png":::

Per saperne di più, vedi [Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)

### Analizzare i dati per dimensioni (relative agli acquisti)

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini di acquisto. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto o ubicazione, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare una struttura complessa del piano dei conti.

Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

## Vedere anche

[Consolidamento società](finance-consolidated-company-reporting.md)  
[Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)  
[Gestione dei report finanziari in business unit o persone giuridiche](finance-consolidated-company-reporting.md)  
[Analisi ad hoc dei dati sugli acquisti](ad-hoc-analysis-purchasing.md)  
[Report sugli acquisti integrati](purchase-reports.md)  
[Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]