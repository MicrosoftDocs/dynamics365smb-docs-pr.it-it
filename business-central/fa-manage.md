---
title: Gestire i cespiti
description: Ottenere informazioni sulla funzionalità dei cespiti e una panoramica delle modalità di utilizzo e gestione dei cespiti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Gestire i cespiti

La funzionalità relativa ai cespiti di [!INCLUDE[prod_short](includes/prod_short.md)] fornisce una sintesi dei cespiti e garantisce che l'ammortamento periodico venga calcolato in modo corretto. Consente, inoltre, di tenere traccia dei costi di manutenzione, di gestire polizze assicurative, di registrare transazioni di cespiti e di generare diversi report e statistiche.

## <a name="what-is-a-fixed-asset"></a>Cos'è un cespite?

I cespiti differiscono dagli altri articoli presenti nel magazzino. Un cespite, noto anche come cespite capitale, è una parte tangibile di proprietà, impianti o attrezzature (PP&E) che possiedi o gestisci con l'aspettativa che continui a generare reddito. Un cespite è fisso quando si tratta di un articolo che la tua azienda non consumerà, venderà o convertirà in contanti entro il successivo anno solare. I cespiti sono diversi dai cespiti correnti, che sono in contanti o destinati a essere convertiti in contanti entro i prossimi 12 mesi. I cespiti differiscono anche dall'inventario, poiché l'inventario viene generalmente consumato in breve tempo.

## <a name="types-of-fixed-assets"></a>Tipi di cespiti

Le aziende in genere investono in alcuni tipi di cespiti. Alcuni esempi sono:

- Fabbricati e strutture
- Attrezzature informatiche e software
- Mobilio e arredi
- Macchinario
- Automezzi

## <a name="understanding-fixed-asset-accounting"></a>Informazioni sulla contabilità cespiti

La contabilità cespiti significa tenere record finanziari precisi sui tuoi cespiti capitali. Questi record includono dettagli sulle cinque fasi del ciclo di vita di un cespite. Dopo l'acquisto iniziale, il ciclo di vita di ciascun cespite include almeno tre delle seguenti fasi:

- Acquisizione: aggiungi un nuovo cespite ai tuoi libri contabili.
- Ammortamento: registra il calo periodico del valore di un cespite, per il cui calcolo utilizzi un metodo di ammortamento. Per saperne di più, vedi [Calcolo dell'ammortamento dei cespiti](LocalFunctionality/India/FA_Depreciation.md).
- Rivalutazione: registri una valutazione dell'attuale valore equo di mercato di un cespite. Per ulteriori informazioni, vedi [Rivalutare i cespiti](fa-how-revalue.md).
- Riduzione del valore: registri una riduzione del valore dovuta a eventi o circostanze.
- Smaltimento: vendi, scarti o utilizzi un altro modo per smaltire un cespite alla fine della relativa vita utile.

Gli audit rientrano anche nei controlli dettagliati dei record contabili della tua società dopo la chiusura dei libri contabili per l'esercizio finanziario. Gli audit, sia interni che esterni, sono il modo in cui potresti notare incoerenze o differenze tra le note e lo stato effettivo dei tuoi cespiti. Gli audit promuovono la trasparenza dei tuoi cespiti e della contabilità se stai perdendo più denaro del previsto.

## <a name="video-overview"></a>Video di panoramica

Il video seguente illustra le nozioni di base dei cespiti:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Configurazione iniziale dei cespiti

Per poter gestire i cespiti, devi dapprima completare le seguenti configurazioni:

- Valori predefiniti
- Contabilità cespiti
- Tipi e categorie di registrazione
- Chiavi di allocazione
- Registrazioni cespiti

Per ulteriori informazioni, vedi [Configurazione dei cespiti](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Analisi dei cespiti

In questa sezione vengono descritti gli strumenti analitici che puoi utilizzare per ottenere informazioni dettagliate sui cespiti.

| Per... | Vedere |
| --- | --- |
| Scopri le funzionalità per l'analisi dei dati sui cespiti. | [Panoramica dell'analisi dei cespiti](fa-analytics-overview.md) |
| Esegui analisi ad hoc dei dati relativi ai cespiti direttamente nelle pagine di elenco e nelle query. | [Analisi ad hoc dei dati dei cespiti](ad-hoc-analysis-fa.md) |
| Esplora report integrati per i cespiti. | [Report sui cespiti predefiniti](fa-reports.md) |
| Monitora i costi di manutenzione. | [Monitorare i costi di manutenzione](fa-how-maintain.md#monitor-maintenance-costs)|
| Monitora la copertura assicurativa. | [Monitorare la copertura assicurativa](fa-how-insure.md#to-monitor-insurance-coverage) |
| Visualizzazione dei movimenti contabili di cessione | [Visualizzare i movimenti contabili di cessione](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Visualizza i valori di cessione previsti. | [Visualizzare i valori di cessione previsti](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Registrare i cespiti

Per ogni cespite occorre impostare una scheda che contiene le relative informazioni. Ad esempio, puoi confiugurare fabbricati o apparecchiature di produzione come cespiti principali con un elenco di componenti. Puoi raggruppare i cespiti in vari modi, ad esempio per classe, reparto o ubicazione. Quindi, puoi iniziare ad acquistare, gestire e vendere i cespiti. È possibile anche impostare i cespiti previsti. L'impostazione di budget ti consente di includere qualsiasi vendita e acquisto previsti nei report.

| A  | Vedere |
| --- | --- |
| Gestire budget per cespiti, costi di acquisto previsti, previsioni di cessione dei cespiti e previsioni di ammortamento. |[Gestione dei budget per i cespiti](fa-how-manage-budgets.md) |
| Creazione di cespiti, assegnazione di metodi di ammortamento, registrazione di acquisti, valori di realizzo e stampa di elenchi di cespiti. |[Acquisire cespiti](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Configurare gli ammortamenti per i cespiti

Per tenere traccia degli ammortamenti dei cespiti e altre transazioni finanziarie per cespiti, imposta uno o più registri beni ammortizzabili per ogni cespite. Ecco alcuni passaggi per ammortizzare i cespiti:

1. Esegui un report che calcola l'ammortamento periodico.
1. Compila un giornale di registrazione con i movimenti ottenuti.
1. Effettuare la registrazione.

[!INCLUDE[prod_short](includes/prod_short.md)] supporta diversi metodi di ammortamento. Per saperne di più, vai a [Metodi di ammortamento](fa-depreciation-methods.md). È possibile impostare più registri beni ammortizzabili per ogni cespite per scopi differenti, ad esempio uno per il reporting dell'IVA e un altro per il reporting interno.

| A  | Vedere |
| --- | --- |
| Ulteriori informazioni sui diversi metodi di ammortamento dei cespiti. |[Metodi di ammortamento](fa-depreciation-methods.md) |
| Calcolo dell'ammortamento, registrazione dell'ammortamento e analisi dell'ammortamento nei report sui cespiti. |[Ammortamento dei cespiti](fa-how-depreciate-amortize.md) |
| Visualizza i valori del registro beni ammortizzabili modificati. | [Visualizzare i valori del registro beni ammortizzabili modificati](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Registra manualmente le transazioni dei cespiti nella pagina **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna. | [Impostare l'ammortamento dei cespiti](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Manutenzione e assicurazione dei cespiti

Puoi registrare i costi di manutenzione e la data del prossimo intervento per ogni cespite. Può essere importante tenere traccia delle spese di manutenzione ai fini dell'impostazione del budget e per decidere se un cespite debba essere sostituito. Puoi associare ciascun cespite a una o più polizze assicurative e verificare che i premi della polizza siano allineati al valore dei cespiti.

| A  | Vedere |
| --- | --- |
| Registrare le visite di assistenza, pubblicare e monitorare i costi di manutenzione. |[Gestione dei cespiti](fa-how-maintain.md) |
| Monitora i costi di manutenzione. | [Monitorare i costi di manutenzione](fa-how-maintain.md#monitor-maintenance-costs)|
| Aggiornare informazioni di assicurazione, registrare costi di acquisto in polizze assicurative, modificare la copertura assicurativa, visualizzare le statistiche di assicurazione e creare liste delle polizze assicurative. |[Assicurazione di cespiti](fa-how-insure.md) |
| Monitora la copertura assicurativa. | [Monitorare la copertura assicurativa](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Riclassificare, trasferire, suddividere/comobinare, rettificare il valore, svalutare e smaltire i cespiti

| A  | Vedere |
| --- | --- |
| Riclassificazione dei cespiti, trasferimento dei cespiti in ubicazioni diverse, suddivisione o raggruppamento dei cespiti. |[Trasferimento, divisione o combinazione di cespiti](fa-how-trans-split-combine.md) |
| Rettifica dei valori dei cespiti, registrazione dell'ammortamento e transazioni di svalutazione. |[Rivalutazione dei cespiti](fa-how-revalue.md) |
| Registrazione di transazioni di cessione, visualizzazione dei movimenti contabili di cessione e registrazione di cessioni parziali. |[Smaltimento o ritiro dei cespiti](fa-how-dispose-retire.md) |
| Visualizzazione dei movimenti contabili di cessione | [Visualizzare i movimenti contabili di cessione](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Visualizza i valori di cessione previsti. | [Visualizzare i valori di cessione previsti](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="tips-for-improving-your-fixed-asset-accounting"></a>Suggerimenti per migliorare la contabilità cespiti

Ci sono alcune cose che puoi implementare nella tua strategia contabile per i cespiti che possono aiutarti a garantire la massimizzazione dei tuoi guadagni.

- Stabilisci una soglia per la capitalizzazione. Quando acquisti un articolo, determina un importo fisso per la capitalizzazione. L'importo aiuta a garantire che i tuoi libri contabili siano coerenti e rende più facile per te e il tuo team individuare gli errori contabili.
- Rivaluta il ciclo di vita delle apparecchiature. È importante stimare correttamente il periodo di tempo in cui puoi utilizzare i cespiti per lo scopo originale. Poiché la contabilità e l'ammortamento si basano su stime accurate del ciclo di vita, rivalutale quando necessario perché potrebbero cambiare nel tempo.
- Tagga i cespiti. È essenziale monitorare e taggare i cespiti durante l'intero ciclo di vita perché molti fattori possono influenzarne il valore. L'uso di tag aiuta a tenere traccia dei tuoi articoli durante tutte le fasi del relativo ciclo di vita e aiuta a prevenire i furti, eliminare gli smarrimenti e supportare le statistiche finanziarie.
- Automatizza le informazioni dettagliate con il software di contabilità cespiti. L'automazione delle attività manuali per tenere traccia dei dati con il software di contabilità cespiti semplifica il completamento dei processi. La protezione tramite password può aiutare a fornire l'accesso solo alle persone che ne hanno bisogno e che sono state formate a tale scopo.

## <a name="see-also"></a>Vedere anche

[Impostazione di cespiti](fa-setup.md)  
[Panoramica dell'analisi dei cespiti](fa-analytics-overview.md)  
[Panoramica dei dati finanziari](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le funzionalità visualizzate](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
