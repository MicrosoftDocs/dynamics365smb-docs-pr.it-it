---
title: Analisi ad hoc dei dati dei cespiti
description: Scopri come utilizzare la modalità di analisi dei dati per analizzare i dati dei cespiti.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Analisi ad hoc dei dati dei cespiti

Questo articolo spiega come utilizzare la funzionalità **Analisi dei dati** per analizzare i dati dei cespiti direttamente dalle pagine di elenco e dalle query. Non è necessario eseguire un report o passare a un'altra applicazione, come Excel. La funzionalità fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "Totale attività", "Ammortamenti nel tempo" o qualsiasi altra visualizzazione tu possa immaginare. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

Utilizza le seguenti pagine di elenco per iniziare a eseguire analisi ad hoc dei processi dei cespiti:

- [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604)
- [Movimenti C/G](https://businesscentral.dynamics.com/?page=20)

## <a name="fixed-assets-ad-hoc-analysis-scenarios"></a>Scenari di analisi ad hoc dei cespiti

Utilizza la funzione **Analisi dei dati** per un rapido controllo dei fatti e un'analisi ad hoc:

- Se non vuoi eseguire un report.
- Se non esiste un report per la tua esigenza specifica.
- Se desideri eseguire rapidamente l'iterazione per ottenere una buona panoramica di una parte della tua attività.

Le sezioni seguenti forniscono esempi di scenari di cespiti in [!INCLUDE [prod_short](includes/prod_short.md)].

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
| [Cespiti (valore corrente)](#example-fixed-assets-current-value) | Tenere traccia del valore dei cespiti, sia su tutti i cespiti che su un singolo cespite. | [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) | **Registro beni ammortizzabili**, **Nr. Cespite**, **Data reg. cespite**, **Tipo reg. cespite** e **Importo** |
| [Variazioni del valore dei cespiti nel tempo](#example-asset-value-changes-over-time) | Tenere traccia delle variazioni del valore dei cespiti nel tempo. | [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) | **Tipo reg. cespite**, **Data reg. cespite** e **Importo** |
|[Ammortamenti dei cespiti nel tempo](#example-fixed-asset-depreciations-over-time) | Tenere traccia degli ammortamenti nel tempo, sia su tutti i cespiti che su un singolo cespite. | [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) | **Registro beni ammortizzabili**, **Nr. Cespite**, **Anno reg. cespite**, **Mese reg. cespite**, **Importo** e **Tipo reg. cespite** |

### <a name="example-fixed-assets-current-value"></a>Esempio: valore corrente dei cespiti

Per tenere traccia del valore di uno o più cespiti, segui questa procedura:

1. Apri l'elenco [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Trascina i campi **Registro beni ammortizzabili** e **Nr. Cespite** sull'area **Gruppi di righe**.
1. Scegli i campi **Data reg. cespite** e **Tipo reg. cespite**.
1. Trascina il campo **Importo** nell'area **Valori**.
1. Rinomina la scheda di analisi in **Panoramica cespiti - Valore** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili cespiti per visualizzare il valore di un cespite." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### <a name="example-asset-value-changes-over-time"></a>Esempio: tenere traccia dei cambiamenti del valore dei cespiti nel tempo

Per tenere traccia delle variazioni del valore dei cespiti nel tempo, segui questi passaggi:

1. Apri l'elenco [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina il campo **Tipo reg. cespite** nell'area **Gruppi di righe**.
1. Trascina i campi **Anno reg. cespite** e **Mese reg. cespite** nell'area **Etichette di colonna**.
1. Trascina il campo **Importo** nell'area **Valori**.
1. Rinomina la scheda di analisi in **Variazioni del valore dei cespiti nel tempo** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili cespiti per vedere le variazioni del valore dei cespiti nel tempo." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### <a name="example-fixed-asset-depreciations-over-time"></a>Esempio: ammortamenti dei cespiti nel tempo

Per tener traccia dell'ammortamento di uno o più cespiti, segui questa procedura:

1. Apri l'elenco [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina i campi **Registro beni ammortizzabili** e **Nr. Cespite** sull'area **Gruppi di righe**.
1. Trascina i campi **Anno reg. cespite** e **Mese reg. cespite** nell'area **Etichette di colonna**.
1. Trascina il campo **Importo** nell'area **Valori**.
1. Nel campo del filtro **Tipo reg. cespite** scegli **Ammortamento**.
1. Rinomina la scheda di analisi in **Ammortamenti nel tempo** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili cespiti per visualizzare l'ammortamento nel tempo." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-fixed-assets"></a>Base dati per analisi ad hoc sui cespiti

Quando si registrano i giornali di registrazione cespiti, [!INCLUDE [prod_short](includes/prod_short.md)] crea movimenti nella tabella **Movimento cespite**. Pertanto, l'analisi ad hoc sui cespiti viene in genere eseguita nella pagina [Movimenti contabili cespiti](https://businesscentral.dynamics.com/?page=5604) .

## <a name="contributors"></a>Collaboratori

*Microsoft gestisce questo articolo. Parti degli esempi sono state originariamente scritte dal seguente collaboratore.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)] Consulente

## <a name="see-also"></a>Vedere anche

[Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md)  
[Panoramica dell'analisi dei cespiti](fa-analytics-overview.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Panoramica dei cespiti](fa-manage.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
