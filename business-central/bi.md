---
title: Analisi finanziaria in Business Central
description: 'Business Central contiene molte funzionalità che ti consentono di raccogliere, analizzare e condividere dati aziendali preziosi per la business intelligence e il processo decisionale.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analisi finanziaria in Business Central

Le aziende acquisiscono un'enorme quantità di dati durante le attività quotidiane che supportano una preziosa Business Intelligence (BI) per i decisori: 

- Dati sulle vendite
- Acquisti
- Costi operativi
- Stipendi dei dipendenti
- Budget

[!INCLUDE[prod_short](includes/prod_short.md)] contiene molte funzionalità che facilitano la raccolta, l'analisi e la condivisione dei dati finanziari dell'organizzazione.

- Reporting finanziario (per rendiconti finanziari e indicatori KPI)
- Analisi ad hoc negli elenchi
- Analisi ad hoc dei dati in Excel (utilizzando Apri in Excel)
- Report finanziari predefiniti

Ognuna di queste funzionalità presenta vantaggi e svantaggi, a seconda del tipo di analisi dei dati e del ruolo dell'utente. Per ulteriori informazioni, vedi [Panoramica di analisi, business intelligence e reporting](reports-bi-reporting.md).

Questo articolo illustra come utilizzare queste funzionalità analitiche per fornire informazioni finanziarie.

## Esigenze di analisi in ambito finanziario

Quando si pensa alle esigenze di analisi in ambito finanziario, potrebbe essere utile utilizzare un modello mentale basato su utenti descritti ad alto livello e sulle loro diverse esigenze di analisi.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrazione di diversi utenti per l'analisi" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Persone che ricoprono ruoli diversi hanno esigenze diverse in termini di dati e li utilizzano in modi diversi. Ad esempio, gli addetti alla finanza interagiscono con i dati in modo diverso rispetto agli addetti alle vendite.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrazione di come utenti diversi hanno esigenze di analisi diverse." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Ruolo              | Aggregazione dei dati  | Modi tipici di consumare dati                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|DF/DG          | Dati sulle prestazioni  | KPI <br> Dashboard <br> Report finanziari           |
|Gestione interessi | Tendenze, sintesi | Report manageriali predefiniti <br> Analisi ad hoc      | 
|Addetto contabile         | Dati dettagliati     | Report operativi predefiniti <br> Dati delle attività visualizzate |

## Indicatori KPI finanziari

Un indicatore KPI è un valore misurabile che mostra l'efficacia con cui stai raggiungendo i tuoi obiettivi. Nel settore finanziario, le persone spesso utilizzano i seguenti KPI per monitorare la salute finanziaria della propria organizzazione:

- Marg. prof. lordo
- Margine di profitto netto
- Capitale d'esercizio
- Rapporto corrente/rapido
- Leva finanziaria, nota anche come moltiplicatore azionario
- Rapporto debiti rispetto a patrimonio netto
- Fatturato cespiti totale
- Rendimento del capitale proprio
- Rendimento dei cespiti

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Utilizzo del reporting finanziario per produrre rendiconti finanziari e indicatori KPI

La funzionalità **Report finanziari** ti offre informazioni sui dati finanziari mostrati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget. La visualizzazione dei risultati nei grafici e nei report nella home page, quali il piano del flusso di cassa e i report Conto economico e Conto patrimoniale.

Le dimensioni svolgono un ruolo importante nella business intelligence. Una dimensione corrisponde ai dati che puoi aggiungere a un movimento come parametro. Le dimensioni ti consentono di raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Tra altri scopi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano report finanziari. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

> [!TIP]
> Un modo rapido per analizzare i dati transazionali consiste nel filtrare i totali nel piano dei conti e le voci in tutte le pagine **Voci** in base alle dimensioni. Cerca l'azione **Imposta filtro dimensione**.  

Nella tabella seguente viene descritta una sequenza di attività nel reporting finanziario, con collegamenti agli articoli che li descrivono.  

| A | Vedere |
| --- | --- |
| Creare nuovi report finanziari per definire i rendiconti finanziari per il reporting o la visualizzazione in grafici.| [Preparare i report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)|
| Utilizza i conti statistici per integrare le informazioni nei report finanziari. I conti statistici ti consentono di aggiungere metriche basate su dati non transazionali. Puoi aggiungere i dati non transazionali come unità basate su numeri, ad esempio numero di dipendenti, metratura o numero di clienti con conti scaduti. | [Analizzare i dati con conti statistici](bi-use-statistical-accounts.md) |
| Scopri come impostare un nuovo report finanziario attraverso esempi. | [Procedura dettagliata: utilizzo del reporting finanziario per eseguire previsioni di flusso di cassa](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analizza le prestazioni finanziarie impostando indicatori di prestazioni chiave (KPI) basati su report finanziari, che poi pubblichi come servizi web. Gli indicatori KPI report finanziario pubblicati possono essere visualizzati su un sito Web o essere importati in Microsoft Excel utilizzando i servizi Web OData. |[Impostare e pubblicare servizi Web KPI basati sui report finanziari](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Impostare le visualizzazioni per analizzare i dati utilizzando le dimensioni.|[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)|
| Creare nuovi report di analisi per vendite, acquisti e magazzino e impostare modelli di analisi. |[Creare report di analisi](bi-how-create-analysis-views-reports.md)|

## Reporting finanziario in business unit o persone giuridiche

Alcune organizzazioni usano [!INCLUDE [prod_short](includes/prod_short.md)] in più business unit o persone giuridiche. Altre usano [!INCLUDE [prod_short](includes/prod_short.md)] nelle filiali che devono riferire nelle organizzazioni madri. [!INCLUDE [prod_short](includes/prod_short.md)] offre ai contabili strumenti che li aiutano a trasferire i movimenti C/G da due o più società (filiali) a una società consolidata.  

Per ulteriori informazioni, vedi [Consolidamento della società](finance-consolidated-company-reporting.md).

## Analisi ad hoc dei dati finanziari

A volte, devi solo verificare se i numeri si sommano correttamente o confermare rapidamente una cifra. Le seguenti funzionalità sono ottime per le analisi ad hoc:

- Analisi dei dati nelle pagine degli elenchi di contabilità
- Apri in Excel

La funzionalità Analisi dati ti consente di aprire quasi una pagina di elenco, ad esempio Movimenti C/G, Movimenti contabili cespiti, Movimenti contabili assegni o Movimenti contabili C/C bancari, accedere alla modalità di analisi e quindi raggruppare, filtrare e ruotare i dati come necessario.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina dei movimenti C/G." lightbox="media/data-analysis-gl-entries.png":::

Allo stesso modo, puoi usare l'azione **Apri in Excel** per aprire una pagina di elenco per i movimenti C/G, eventualmente filtrare l'elenco in un sottoinsieme di dati e quindi utilizzare Excel per utilizzare i dati. Ad esempio, utilizzando funzionalità come Analizza dati, Analisi what-if o Foglio previsioni.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nei dati dei movimenti C/G utilizzando Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Se configuri OneDrive per le funzionalità di sistema, la cartella di lavoro di Excel si apre nel browser usando Excel per il Web. 

<!-- Not ready yet
For more information on how to do ad-hoc analysis on ledgers, see [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md). 
-->
## Report predefiniti per la finanza

[!INCLUDE [prod_short](includes/prod_short.md)] include diversi report predefiniti, funzioni di tracciamento e strumenti utili per i revisori o i controllori responsabili della creazione di report per il reparto finanziario.

Per ottenere una panoramica dei report disponibili, puoi fare clic su **Tutti i report** nel riquadro superiore della tua home page. Si apre Esplora ruoli, il cui contenuto viene filtrato in base alle funzionalità nell'opzione **Report e analisi**. Per ulteriori informazioni, vai [Ricerca di report con Esplora ruoli](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Esempio di report sul centro ruoli finanziario." lightbox="media/report-explorer-finance.png":::

I report predefiniti sono disponibili in due versioni:

- Progettati per la stampa (pdf).
- Progettati per l'analisi in Excel.

Per ulteriori informazioni, vedi queste panoramiche per i report pertinenti per il settore finanziario.

- [Report Excel finanziari predefiniti](finance-analyze-excel.md)
- [Report finanziari chiave predefiniti](finance-reports.md)
- [Report sui cespiti predefiniti](fa-reports.md)
- [Report di contabilità clienti predefiniti](receivables-reports.md)
- [Report di contabilità fornitori predefiniti](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Pagine di attività finanziarie visualizzate

[!INCLUDE [prod_short](includes/prod_short.md)] include varie pagine che forniscono panoramiche finanziarie e attività da svolgere.

### Mostrare movimenti e saldi di contabilità generale dalla pagina Piano dei conti

La pagina Piano dei conti mostra tutti i conti di contabilità generale con numeri aggregati su quanto registrato nella contabilità generale. Da questa pagina puoi fare cose come:  

- Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.  
- Esaminare un elenco delle categorie di registrazione per il conto in questione.
- Visualizza i saldi attivi e passivi separatamente per un singolo conto.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esempio di come la pagina Piano dei conti mostra informazioni finanziarie" lightbox="media/chart-of-accounts-page.png":::

Per saperne di più, vedi [Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)

### Visualizzare gli importi effettivi rispetto agli importi budget per tutti i conti e per diversi periodi

Come parte della raccolta, dell'analisi e della condivisione dei dati della società, potresti voler visualizzare gli importi effettivi rispetto agli importi budget per tutti i conti e per diversi periodi. Puoi eseguire questa operazione nella pagina **Piano dei conti** scegliendo l'azione **Saldo budget C/G**.

Per saperne di più, vai [Analizzare importi effettivi e importi budget](bi-how-analyze-actual-versus-budget.md).

### Analizzare i dati per dimensioni

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini vendita. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto e progetto, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare una struttura complessa del piano dei conti.

Nelle analisi finanziarie, una dimensione corrisponde ai dati che aggiungi a un movimento C/G come una specie di contrassegno. Tali dati vengono utilizzati per raggruppare movimenti C/G con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Puoi usare le dimensioni per i movimenti in registrazioni, documenti e budget. Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)

### Analisi del flusso di cassa

Nella home page Addetto contabile, in **Prestazioni finanziarie**, i grafici Ciclo di cassa, Flusso di cassa ed Entrate e uscite consentono di analizzare il flusso di cassa:

- Esaminare le cifre per un periodo utilizzando il cursore della sequenza temporale.
- Filtrare il grafico scegliendo l'origine nella legenda.
- Modificare la durata del periodo oppure passare al periodo precedente o successivo, selezionando le opzioni nel menu a discesa Prestazioni finanziarie.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Esempio di come appaiono gli elementi visivi del flusso di cassa nel centro ruolo contabile" lightbox="media/cashflow-accountant-rolecentre.png":::

Per esaminare la previsione, oltre ai movimenti previsti, è possibile analizzarne il prospetto flussi di cassa. Ad esempio, è possibile vedere come la previsione:

- Gestisce le vendite e gli acquisti confermati.
- Sottrae i debiti e aggiunge i crediti.
- Salta gli ordini di vendita e di acquisto doppi.

Per saperne di più, vedi [Analisi del flusso di cassa dell'azienda](finance-analyze-cash-flow.md).

## Vedere anche

[Gestione dei report finanziari in business unit o persone giuridiche](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Preparare i report finanziari con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)  
<!-- [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md)   -->
[Informazioni sul piano dei conti](finance-general-ledger.md#the-chart-of-accounts)  
[Report Excel finanziari predefiniti](finance-analyze-excel.md)  
[Report finanziari chiave predefiniti](finance-reports.md)  
[Report sui cespiti predefiniti](fa-reports.md)  
[Report di contabilità clienti predefiniti](receivables-reports.md)  
[Report di contabilità fornitori predefiniti](payables-reports.md)  
[Panoramica dei dati finanziari](finance.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)   
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
