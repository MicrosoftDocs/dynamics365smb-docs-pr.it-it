---
title: 'Panoramica di analisi, business Intelligence e reporting'
description: Fornisce una panoramica di tutte le funzionalità di Business Intelligence e reporting supportate in Business Central.
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# Panoramica di analisi, business Intelligence e reporting

Le piccole e medie imprese usano le funzionalità di analisi e report integrate che possono utilizzare immediatamente per tenere traccia della propria attività. [!INCLUDE[prod_short](includes/prod_short.md)] fornisce report e strumenti di analisi che coprono processi aziendali di base e complessi per tali organizzazioni. Puoi anche eseguire analisi ad hoc direttamente dalla tua home page.  

## Esigenze di analisi nelle organizzazioni

Quando si pensa alle esigenze di analisi nelle organizzazioni, potrebbe essere utile utilizzare un modello mentale basato su utenti descritti ad alto livello e sulle loro diverse esigenze di analisi.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrazione di diversi utenti per l'analisi" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Il modello si basa sul fatto che ruoli diversi in un’organizzazione hanno esigenze diverse in termini di dati. Più in alto viene posizionato un ruolo nell'organigramma, maggiore sarà la quantità di dati aggregati necessari a chi ha quel ruolo per svolgere il proprio lavoro.

I ruoli hanno spesso modalità di consumo e analisi dei dati preferite, modalità che riflettono il livello di aggregazione dei dati di cui hanno bisogno.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrazione di come utenti diversi hanno esigenze di analisi diverse." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Utilizza le sezioni seguenti per ulteriori informazioni sulle modalità di consumare i dati da [!INCLUDE[prod_short](includes/prod_short.md)]:

- Report finanziari
- Indicatori KPI e dashboard
- Analisi ad hoc
- Report

## Utilizzo di Report finanziari per produrre rendiconti finanziari e indicatori KPI

La funzionalità Report finanziari ti offrono informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Screenshot di un report finanziario." lightbox="media/acc_schedule_13_columns.jpg":::

Le dimensioni svolgono un ruolo importante nella business intelligence. Una dimensione corrisponde ai dati che puoi aggiungere a un movimento come parametro. Le dimensioni ti consentono di raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Tra altri scopi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano report finanziari. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

Per ulteriori informazioni sui rendiconti finanziari e sugli indicatori KPI, vai a [Utilizzo del reporting finanziario per produrre rendiconti finanziari e indicatori KPI](bi.md).

## Uso di indicatori KPI per soddisfare gli obiettivi aziendali

Un indicatore KPI è un valore misurabile che mostra l'efficacia con cui stai raggiungendo i tuoi obiettivi. Considera gli indicatori KPI come la scorecard della tua società, un modo di determinare se stai raggiungendo o meno i tuoi obiettivi.

L'identificazione e il monitoraggio degli identificatori KPI ti consentono di sapere se la tua azienda è sulla strada giusta o se dovresti cambiare rotta. Se utilizzati correttamente, gli indicatori KPI sono strumenti potenti che ti aiutano a:

- Monitorare la solidità finanziaria della società.
- Misurare i progressi rispetto agli obiettivi strategici.
- Individuare i problemi in anticipo.
- Apportare modifiche tempestive alle tattiche.
- Motivare i membri del team.
- Prendere decisioni migliori e più velocemente.

Per ulteriori informazioni sugli indicatori KPI, vedi [Uso degli indicatori KPI per soddisfare gli obiettivi aziendali](./analytics-about-kpis.md)

## Analisi dei dati ad hoc

A volte potresti semplicemente voler verificare se i numeri si sommano correttamente, confermare o sfatare rapidamente un'ipotesi sull'attività o magari cercare anomalie nei tuoi dati finanziari. Per le analisi ad hoc, potresti non disporre di un report predefinito utile per rispondere alle tue domande. Per le analisi ad hoc, utilizza queste due funzionalità:

- Analisi dei dati nelle pagine degli elenchi di contabilità
- Apri in Excel

La funzionalità Analisi dati ti consente di aprire quasi tutte le pagine di elenco, ad esempio Movimenti C/G o Movimenti contabili clienti, accedere alla modalità di analisi e quindi raggruppare, filtrare e ruotare i dati come necessario. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina dei movimenti C/G." lightbox="media/data-analysis-gl-entries.png":::

Allo stesso modo, puoi usare l'azione **Apri in Excel** per aprire una pagina di elenco, eventualmente filtrare l'elenco in un sottoinsieme di dati e quindi utilizzare Excel per utilizzare i dati. Ad esempio, utilizzando funzionalità come Analizza dati, Analisi what-if o Foglio previsioni.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nei dati dei movimenti C/G utilizzando Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Se configuri OneDrive per le funzionalità di sistema, la cartella di lavoro di Excel si apre nel browser usando Excel per il Web.

Per ulteriori informazioni sulle analisi ad-hoc, vai a [Analisi dei dati ad hoc](reports-adhoc-analysis.md).

## Report

Un report in [!INCLUDE[prod_short](includes/prod_short.md)] raccoglie informazioni in base a una serie di criteri specificati. I report consentono di organizzare e presentare le informazioni in un formato di facile lettura che puoi utilizzare in Excel, stampare o salvare come file.  

Come esempio di report interattivo in Excel, il report ***Scadenziario clienti** ti consente di analizzare ciò che i tuoi clienti ti devono e quando i pagamenti sono dovuti.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Esempio del report Scadenzari clienti in Excel." lightbox="media/aged-accounts-receivables-excel.png":::

Per gli scadenziari clienti, [!INCLUDE[prod_short](includes/prod_short.md)] include anche un report progettato per la stampa. La possibilità di stampare è utile se preferisci avere i dati in un file .pdf.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Esempio del report Scadenzari clienti in pdf." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] viene fornito con più di 300 report predefiniti che puoi utilizzare per supportare i tuoi processi aziendali con informazioni dettagliate basati sui dati. Per ottenere una rapida panoramica di tutti i report disponibili per il tuo ruolo, puoi aprire Esplora report da Gestione ruolo utente, da tutte le pagine di elenco e da **Dimmi**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Esempio di come Esplora report mostra tutti i report per un ruolo." lightbox="media/report-explorer-finance.png":::

Per ulteriori informazioni sull'utilizzo di Esplora report per visualizzare tutti i report predefiniti, vedi [Esplorazione di report per ruolo](ui-role-explorer.md).

La tabella seguente elenca gli articoli su come utilizzare report predefiniti in [!INCLUDE[prod_short](includes/prod_short.md)].

| A  | Vedere |
| --- | --- |
| Scopri come utilizzare report (segnalibro, esegui, stampa, pianifica e modifica il layout). | [Usare i report nel lavoro quotidiano](reports-use-reports.md) |
| Per informazioni su quali report predefiniti sono disponibili, vedi [!INCLUDE[prod_short](includes/prod_short.md)]. |[Panoramica del report](reports-available-reports.md)| 
| Utilizza Esplora report per visualizzare tutti i report predefiniti. | [Esplorazione di report per ruolo](ui-role-explorer.md) |

## Strumenti di Business Intelligence e reporting esterni

Se preferisci utilizzare strumenti di Business Intelligence non incorporati in [!INCLUDE[prod_short](includes/prod_short.md)], la tabella seguente fornisce collegamenti a indicazioni sugli strumenti e sulle modalità di utilizzo degli strumenti esterni.

| A  | Vedere |
| --- | --- |
| Usare Power BI con dati di Business Central | [Utilizzo di Power BI con Business Central](admin-powerbi.md) |
| Integra gli strumenti di business intelligence esterni con [!INCLUDE[prod_short](includes/prod_short.md)].| [Strumenti di Business Intelligence esterni](reports-external-analysis.md) |
| Estrarre dati in data warehouse o data lake| [Come estrarre dati in data warehouse o data lake](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Analizzare i dati di Business Central in Microsoft Fabric| [Introduzione a Microsoft Fabric e Business Central](admin-fabric.md) |
| Leggere dati da Business Central utilizzando API | [API di Business Central v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## Vedere anche

[Utilizzo del reporting finanziario per produrre rendiconti finanziari e indicatori KPI](bi.md)  
[Uso degli indicatori KPI per soddisfare gli obiettivi aziendali](analytics-about-kpis.md)  
[Eseguire analisi dei dati ad hoc](reports-adhoc-analysis.md)  
[Usare report nel lavoro quotidiano](reports-use-reports.md)  
[Panoramica di report predefiniti](reports-available-reports.md)  
[Esplorazione di report per ruolo](ui-role-explorer.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
