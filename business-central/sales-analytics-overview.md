---
title: Analisi delle vendite
description: 'Business Central contiene molte funzionalità che ti consentono di raccogliere, analizzare e condividere dati sulle vendite preziosi per business intelligence e processo decisionale nell''organizzazione dedicate alle vendite.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analisi delle vendite

Le aziende acquisiscono moltissimi dati durante le attività quotidiane che supportano la business Intelligence (BI) per i responsabili vendite:

- Opportunità
- Offerte di vendita
- Ordini di vendita
- Fatture di vendita

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce funzionalità che facilitano la raccolta, l'analisi e la condivisione dei dati sulle vendite dell'organizzazione.

- Analisi ad hoc negli elenchi
- Analisi ad hoc dei dati in Excel (utilizzando Apri in Excel)
- Strumenti di analisi delle vendite integrati
- Report sulle vendite predefiniti

Ognuna di queste funzionalità presenta vantaggi e svantaggi, a seconda del tipo di analisi dei dati e del ruolo dell'utente. Per ulteriori informazioni, vedi [Panoramica di analisi, business intelligence e reporting](reports-bi-reporting.md).

Questo articolo illustra come utilizzare queste funzionalità analitiche per ottenere informazioni dettagliate sulle vendite.

## Esigenze di analisi nelle vendite

Quando pensi alle esigenze di analisi nella gestione delle vendite, potrebbe essere utile utilizzare un modello basato su un utente tipo che descrive diverse esigenze di analisi ad alto livello.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrazione di diversi utenti per l'analisi" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Persone che ricoprono ruoli diversi hanno esigenze diverse in termini di dati e li utilizzano in modi diversi. Ad esempio, gli addetti alla gestione dei cespiti e alla finanza interagiscono con i dati in modo diverso rispetto agli addetti alle vendite.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrazione di come utenti diversi hanno esigenze di analisi diverse." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Ruolo              | Aggregazione dei dati  | Modi tipici di consumare dati                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO / DF / DG    | Dati sulle prestazioni  | KPI <br> Dashboard <br> Report finanziari           |
|Direttore vendite      | Tendenze, sintesi | Report manageriali predefiniti <br> Analisi ad hoc      | 
|Manager contabilità/Addetto alle vendite | Dati dettagliati     | Report operativi predefiniti <br> Dati delle attività visualizzate |

<!-- 
## Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Utilizzare il reporting finanziario per produrre rendiconti finanziari e indicatori KPI relativi alle vendite

La funzionalità **Reporting finanziario** fornisce informazioni dettagliate sui dati finanziari mostrati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget. Specificamente per la gestione delle vendite, puoi impostare report finanziari sui conti C/G utilizzati per tenere traccia delle registrazioni delle vendite.

Le dimensioni svolgono un ruolo importante nella business intelligence. Una dimensione corrisponde ai dati che aggiungi a un movimento come parametro. Le dimensioni ti consentono di raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti. Tra altri scopi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano report finanziari. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

Per ulteriori informazioni sui report finanziari, vedi [Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md).

## Reporting finanziario in business unit o persone giuridiche relative alle vendite

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)] nelle filiali che devono generare report per le organizzazioni padre. [!INCLUDE [prod_short](includes/prod_short.md)] offre ai contabili strumenti che li aiutano a trasferire i movimenti C/G da due o più società (filiali) a una società consolidata. In particolare per la gestione delle vendite, potresti voler consolidare i movimenti C/G per i tuoi conti vendite per tenere traccia degli indicatori KPI di vendita in business unit o persone giuridiche.

Per ulteriori informazioni, vedi [Consolidamento della società](finance-consolidated-company-reporting.md).

## Analisi ad hoc dei dati sulle vendite

A volte, devi solo verificare se i numeri si sommano correttamente o confermare rapidamente una cifra. Le seguenti funzionalità sono ottime per le analisi ad hoc:

- Analisi dei dati nelle pagine degli elenchi di contabilità
- Apri in Excel

La funzionalità Analisi dati ti consente di aprire quasi tutte le pagine di elenco, ad esempio **Movimenti C/G**, **Movimenti contabili clienti**, **Movimenti contabili articoli** o **Fatture registrate**, accedere alla modalità di analisi e quindi raggruppare, filtrare e ruotare i dati come necessario.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili clienti." lightbox="media/data-analysis-customer-ledger-entries.png":::

Allo stesso modo, puoi usare l'azione **Apri in Excel** per aprire una pagina di elenco, eventualmente filtrare l'elenco in un sottoinsieme di dati e quindi utilizzare Excel per utilizzare i dati. Ad esempio, utilizzando funzionalità come Analizza dati, Analisi what-if o Foglio previsioni.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nei dati dei movimenti contabili clienti utilizzando Excel." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Se configuri OneDrive per le funzionalità di sistema, la cartella di lavoro di Excel si apre nel browser.

Per ulteriori informazioni su come eseguire analisi ad hoc sui dati relativi alle vendite, vedi [Analisi ad hoc dei dati sulle vendite](ad-hoc-analysis-sales.md). 

## Report predefiniti per le vendite

[!INCLUDE [prod_short](includes/prod_short.md)] include diversi report integrati, funzioni di tracciamento e strumenti per aiutare le organizzazioni dedicate alle vendite a creare report sui propri dati.

Per ottenere una panoramica dei report disponibili, scegli **Tutti i report** nel riquadro superiore della tua home page. Questa azione apre Esplora ruoli, il cui contenuto viene filtrato in base alle funzionalità nell'opzione **Report e analisi**. Per ulteriori informazioni, vedi [Ricerca di report con Esplora ruoli](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Esempio di report sul centro ruoli vendite." lightbox="media/report-explorer-sales.png":::

I report predefiniti sono disponibili in due versioni:

- Progettati per la stampa (pdf).
- Progettati per l'analisi in Excel.

Per ulteriori informazioni sui report relativi alle vendite, vedi [Report sulle vendite integrati](sales-reports.md).

## Analisi delle vendite visualizzate

[!INCLUDE [prod_short](includes/prod_short.md)] include varie pagine che forniscono panoramiche sulle vendite e attività da svolgere. Ecco alcuni esempi per iniziare:

- [Aprire l'elenco **Offerte vendita**](https://businesscentral.dynamics.com/?page=9300)
- [Aprire l'elenco **Ordini di vendita**](https://businesscentral.dynamics.com/?page=9305)
- [Aprire l'elenco **Fatture vendite registrate**](https://businesscentral.dynamics.com/?page=143)
- [Aprire l'elenco **Ordini di reso vendita**](https://businesscentral.dynamics.com/?page=9304)
- [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)
- [Calcolare le date di consegna di ordini di vendita](sales-date-calculation-for-sales.md)
- [Rintracciare i colli](sales-how-track-packages.md)
- [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)
- [Stato dell'ordine di vendita programmato](sales-how-to-create-blanket-sales-orders.md#to-view-the-status-of-a-blanket-sales-order)
- [Visualizzare le righe degli ordini di vendita programmati registrate e non registrate](sales-how-to-create-blanket-sales-orders.md#to-view-unposted-and-posted-blanket-sales-order-lines)


### Mostrare movimenti e saldi di contabilità generale relativi alle vendite dalla pagina Piano dei conti

La pagina Piano dei conti mostra tutti i conti C/G con numeri aggregati registrati nella contabilità generale. Da questa pagina puoi fare cose come:  

- Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
- Esaminare un elenco delle categorie di registrazione per il conto in questione.
- Visualizza i saldi attivi e passivi separatamente per un singolo conto.

Specificamente per le vendite, puoi creare una visualizzazione nella pagina Piano dei conti che mostri solo i conti utilizzati per registrare movimenti di vendite.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esempio di come la pagina Piano dei conti mostra informazioni finanziarie" lightbox="media/chart-of-accounts-page.png":::

Per saperne di più, vedi [Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)

### Analizzare i dati per dimensioni (relative alle vendite)

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini vendita. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto o ubicazione, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare una struttura complessa del piano dei conti.

Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

## Vedere anche

[Consolidamento società](finance-consolidated-company-reporting.md)   
[Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)  
[Gestione dei report finanziari in business unit o persone giuridiche](finance-consolidated-company-reporting.md)  
[Analisi ad hoc dei dati sulle vendite](ad-hoc-analysis-sales.md)   
[Report sulle vendite predefiniti](sales-reports.md)   
[Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)   
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
