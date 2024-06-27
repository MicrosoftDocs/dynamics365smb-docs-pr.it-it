---
title: Analisi ad hoc dei dati di sostenibilità
description: Scopri come utilizzare la modalità di analisi dei dati per analizzare i dati di sostenibilità.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analisi ad hoc dei dati di sostenibilità

Questo articolo spiega come utilizzare la funzionalità **Analisi dei dati** per analizzare i dati di sostenibilità direttamente dalle pagine di elenco e dalle query. Non è necessario eseguire un report o passare a un'altra applicazione, come Excel. La funzionalità fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "Panoramica emissioni" o "Emissione per ambito" o qualsiasi altra visualizzazione tu possa immaginare. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

Utilizza le seguenti pagine di elenco per analisi ad hoc dei dati di sostenibilità:

- [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220)

## Scenari di analisi ad hoc di sostenibilità

Utilizza la funzione **Analisi dei dati** per un rapido controllo dei fatti e un'analisi ad hoc:

- Se non vuoi eseguire un report.
- Se non esiste un report per la tua esigenza specifica.
- Se desideri eseguire rapidamente l'iterazione per ottenere una buona panoramica di una parte della tua attività.

Le sezioni seguenti forniscono esempi di scenari di sostenibilità in [!INCLUDE [prod_short](includes/prod_short.md)].

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
| [Panoramica emissioni (somma per categoria)](#example-emission-overview-sum-by-category) | Analizza le tue emissioni per categoria. | [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) | **Categoria conto**, **Nome conto**, **Emissione NH4**, **Emissioni CO2** e **Emissioni N2O**.|
| [Emissioni medie per categoria](#example-average-emissions-by-category) | Analizza le tue emissioni medie per categoria. | [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) | **Categoria conto**, **Nome conto**, **Emissione NH4**, **Emissioni CO2** e **Emissioni N2O**.|
| [Emissioni per ambito](#example-emissions-by-scope) | Analizza le tue emissioni per ambito. | [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) | **Ambito emissioni**, **Categoria conto**, **Emissione NH4**, **Emissioni CO2** e **Emissioni N2O**.|

## Esempio: panoramica emissioni (somma per categoria)

Per analizzare le tue emissioni per categoria, segui questa procedura:

1. Apri la pagina [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) e attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva la modalità **Pivot** (situata direttamente sopra il campo **Ricerca**).
1. Trascina i campi **Categoria conto** e **Nome conto** sull'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Trascina i campi **Emissione NH4**, **Emissione CO2** e **Emissione N2O** sull'area **Valori**.
1. Rinomina la scheda di analisi in **Panoramica emissioni (somma)** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Esempio 1 di come eseguire l'analisi dei dati nella pagina Movimenti contabili sostenibilità." lightbox="media/data-analysis-sustainability-entries.png":::

## Esempio: emissioni medie per categoria

Per analizzare le tue emissioni medie per categoria, segui questa procedura:

1. Apri la pagina [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) e attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva la modalità **Pivot** (situata direttamente sopra il campo **Ricerca**).
1. Trascina i campi **Categoria conto** e **Nome conto** sull'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Trascina i campi **Emissione NH4**, **Emissione CO2** e **Emissione N2O** sull'area **Valori**.
1. Per ciascun campo nell'area **Valori**, selezionali e modifica la funzione di aggregazione in `Average`.
1. Rinomina la scheda di analisi in **Panoramica emissioni (media)** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Esempio 2 di come eseguire l'analisi dei dati nella pagina Movimenti contabili sostenibilità." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Esempio: emissioni per ambito

Per analizzare le tue emissioni per ambito, segui questa procedura:

1. Apri la pagina [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) e attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva la modalità **Pivot** (situata direttamente sopra il campo **Ricerca**).
1. Trascina i campi **Ambito emissioni** e **Categoria conto** sull'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Trascina i campi **Emissione NH4**, **Emissione CO2** e **Emissione N2O** sull'area **Valori**.
1. Rinomina la scheda di analisi in **Panoramica emissioni per ambito** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Esempio 3 di come eseguire l'analisi dei dati nella pagina Movimenti contabili sostenibilità." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Base dati per analisi ad hoc sulla sostenibilità

Le informazioni immesse in una registrazione sostenibilità sono temporanee e puoi modificarle mentre si trovano nella registrazione. Quando si esegue una registrazione sostenibilità, le informazioni vengono trasferite ai movimenti contabili sostenibilità in singoli conti di sostenibilità, dove non puoi modificarle. Si possono tuttavia inserire storni o correzioni dei movimenti. La pagina elenco [Movimenti contabili sostenibilità](https://businesscentral.dynamics.com/?page=6220) è la principale fonte di dati per analisi ad hoc dei dati di sostenibilità.

Per ulteriori informazioni sulla registrazione di movimenti di sostenibilità, vedi [Registrare movimenti di sostenibilità](finance-sustainability-journal.md).

## Vedere anche

[Registrare movimenti di sostenibilità](finance-sustainability-journal.md)  
[Report per la sostenibilità predefiniti](sustainability-reports.md)   
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Panoramica della gestione della sostenibilità](finance-manage-sustainability.md)   
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
