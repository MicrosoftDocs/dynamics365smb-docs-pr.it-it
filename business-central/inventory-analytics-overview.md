---
title: Analisi dell'inventario
description: 'Business Central contiene molte funzionalità che ti consentono di raccogliere, analizzare e condividere dati sul magazino per business intelligence e processo decisionale nell''organizzazione.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="inventory-analytics"></a>Analisi dell'inventario

Le aziende acquisiscono moltissimi dati durante le attività quotidiane che supportano la business Intelligence (BI) per i responsabili di magazzino:

- Spedizione della merce quando gli ordini di vendita vengono evasi.
- Entrate degli articoli quando gli ordini di acquisto vengono evasi.
- Spostamenti di articoli tra ubicazioni.

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce funzionalità che facilitano la raccolta, l'analisi e la condivisione dei dati sul magazzino dell'organizzazione.

- Analisi ad hoc negli elenchi
- Analisi ad hoc dei dati in Excel (utilizzando Apri in Excel)
- Strumenti di analisi di magazzino integrati
- Report predefiniti per il magazzino

Ognuna di queste funzionalità presenta vantaggi e svantaggi, a seconda del tipo di analisi dei dati e del ruolo dell'utente. Per ulteriori informazioni, vedi [Panoramica di analisi, business intelligence e reporting](reports-bi-reporting.md).

Questo articolo illustra come utilizzare queste funzionalità analitiche per ottenere informazioni dettagliate sul magazzino.

## <a name="analytics-needs-in-inventory"></a>Esigenze di analisi nel magazzino

Quando pensi alle esigenze di analisi nella gestione del magazzino, potrebbe essere utile utilizzare un modello basato su un utente tipo che descrive diverse esigenze di analisi ad alto livello.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrazione di diversi utenti per l'analisi" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Persone che ricoprono ruoli diversi hanno esigenze diverse in termini di dati e li utilizzano in modi diversi. Ad esempio, gli addetti alla gestione dei cespiti e alla finanza interagiscono con i dati in modo diverso rispetto agli addetti alle vendite.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrazione di come utenti tipo diversi hanno esigenze di analisi diverse." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Ruolo              | Aggregazione dei dati  | Modi tipici di consumare dati                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|DO / DF / DG    | Dati sulle prestazioni  | KPI, dashboard, report finanziari           |
|Gestione inventario  | Tendenze, sintesi | Report gestionali integrati, analisi ad hoc      | 
|Addetto al magazzino   | Dati dettagliati     | Report operativi integrati, dati delle attività su schermo |

<!-- 
## <a name="inventory-kpis"></a>Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-inventory"></a>Utilizzare il reporting finanziario per produrre rendiconti finanziari e indicatori KPI relativi al magazzino

La funzionalità **Reporting finanziario** fornisce informazioni dettagliate sui dati finanziari mostrati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget. Specificamente per la gestione del magazzino, puoi impostare report finanziari sui conti C/G utilizzati per tenere traccia delle registrazioni di magazzino.

Le dimensioni svolgono un ruolo importante nella business intelligence. Una dimensione corrisponde ai dati che aggiungi a un movimento come parametro. Le dimensioni ti consentono di raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti. Tra altri scopi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano report finanziari. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

Per ulteriori informazioni sui report finanziari, vedi [Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-inventory"></a>Reporting finanziario in business unit o persone giuridiche (relative al magazzino)

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)] nelle filiali che devono generare report per le organizzazioni padre. [!INCLUDE [prod_short](includes/prod_short.md)] offre ai contabili strumenti che li aiutano a trasferire i movimenti C/G da due o più società (filiali) a una società consolidata. In particolare per la gestione del magazzino, potresti voler consolidare i movimenti C/G per i tuoi conti di magazzino per tenere traccia degli indicatori KPI di vendita in business unit o persone giuridiche.

Per ulteriori informazioni, vedi [Consolidamento della società](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-inventory-data"></a>Analisi ad hoc dei dati di magazzino

A volte, devi solo verificare se i numeri si sommano correttamente o confermare rapidamente una cifra. Le seguenti funzionalità sono ottime per le analisi ad hoc:

- Analisi dei dati nelle pagine degli elenchi di contabilità
- Apri in Excel

La funzionalità Analisi dati ti consente di aprire quasi tutte le pagine di elenco, ad esempio **Movimenti contabili articoli** accedere alla modalità di analisi e quindi raggruppare, filtrare e ruotare i dati come necessario.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Esempio di come eseguire un'analisi dei dati sullo stock scaduto nella pagina Movimenti contabili articoli." lightbox="media/data-analysis-inventory-dead-stock.png":::

Allo stesso modo, puoi usare l'azione **Apri in Excel** per aprire una pagina di elenco, eventualmente filtrare l'elenco in un sottoinsieme di dati e quindi utilizzare Excel per utilizzare i dati. Ad esempio, utilizzando funzionalità come Analizza dati, Analisi what-if o Foglio previsioni.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Se configuri OneDrive per le funzionalità di sistema, la cartella di lavoro di Excel si apre nel browser.

Per ulteriori informazioni su come eseguire analisi ad hoc sui dati di magazzino, vedi [Analisi ad hoc dei dati di inventario](ad-hoc-analysis-inventory.md).

## <a name="built-in-reports-for-inventory"></a>Report predefiniti per il magazzino

[!INCLUDE [prod_short](includes/prod_short.md)] include diversi report integrati, funzioni di tracciamento e strumenti per aiutare le organizzazioni dedicate al magazzino a creare report sui propri dati.

Per ottenere una panoramica dei report disponibili, scegli **Tutti i report** nella home page. Questa azione apre Esplora report, il cui contenuto viene filtrato in base alle funzionalità nell'opzione **Report e analisi**. Sotto l'intestazione **Vendite e marketing**, seleziona **Esplora**. Per ulteriori informazioni, vedi [Ricerca di report con Esplora ruoli](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Esempio di report sul centro ruoli vendite." lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Per ulteriori informazioni sui report relativi al magazzino, vedi [Report di inventario e warehouse predefiniti](inventory-WMS-reports.md).

## <a name="on-screen-inventory-analytics"></a>Analisi del magazzino visualizzate

[!INCLUDE [prod_short](includes/prod_short.md)] include varie pagine che forniscono panoramiche sul magazzino e attività da svolgere. Ecco alcuni esempi per iniziare:

- [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)
- [Tracciare gli articoli con numeri di serie, di lotto e di collo](inventory-how-work-item-tracking.md)
- [Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)
- [Controllare la riconciliazione tra il movimento contabile di inventario e la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Visualizzare gli articoli sottoposti a cross-dock in una spedizione o in un prospetto prelievi](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Il modulo delle vendite include anche pagine di analisi relative all'inventario:

- [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)
- [Calcolare le date di consegna di ordini di vendita](sales-date-calculation-for-sales.md)
- [Rintracciare i colli](sales-how-track-packages.md)

### <a name="show-inventory-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Mostrare movimenti e saldi C/G relativi al magazzino dalla pagina Piano dei conti

La pagina **Piano dei conti** mostra tutti i conti C/G con numeri aggregati registrati nella contabilità generale. Da questa pagina puoi fare cose come:  

- Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
- Esaminare un elenco delle categorie di registrazione per il conto in questione.
- Visualizza i saldi attivi e passivi separatamente per un singolo conto.

Specificamente per la gestione del magazzino, puoi creare una visualizzazione nella pagina Piano dei conti che mostri solo i conti utilizzati per registrare movimenti di magazzino.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esempio di come la pagina Piano dei conti mostra informazioni finanziarie" lightbox="media/chart-of-accounts-page.png":::

Per saperne di più, vedi [Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)

### <a name="analyze-inventory-data-by-dimensions"></a>Analizzare i dati sul magazzino per dimensioni

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini vendita. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto o ubicazione, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare una struttura complessa del piano dei conti.

Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Vedere anche

[Consolidamento società](finance-consolidated-company-reporting.md)   
[Preparare report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)  
[Gestione dei report finanziari in business unit o persone giuridiche](finance-consolidated-company-reporting.md)  
[Analisi ad hoc dei dati di inventario](ad-hoc-analysis-inventory.md)  
[Report di inventario e warehouse predefiniti](inventory-WMS-reports.md)  
[Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)   
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
