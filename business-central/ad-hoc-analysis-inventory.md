---
title: Analisi ad hoc dei dati di magazzino
description: Informazioni su come utilizzare la modalità di analisi dei dati per analizzare i dati di magazzino.
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

# Analisi ad hoc dei dati di magazzino

Questo articolo spiega come utilizzare la funzionalità **Analisi dei dati** per analizzare i dati di magazzino direttamente dalle pagine di elenco e dalle query. Non è necessario eseguire un report o passare a un'altra applicazione, come Excel. La funzionalità fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "stock in scadenza" o "venditori principali" o qualsiasi altra visualizzazione tu possa immaginare. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

Utilizza le seguenti pagine di elenco per analisi ad hoc dei processi di magazzino:

- [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38)

## Scenari di analisi di magazzino ad hoc

Utilizza la funzione **Analisi dei dati** per un rapido controllo dei fatti e un'analisi ad hoc:

- Se non vuoi eseguire un report.
- Se non esiste un report per la tua esigenza specifica.
- Se desideri eseguire rapidamente l'iterazione per ottenere una buona panoramica di una parte della tua attività.

Le sezioni seguenti forniscono esempi di scenari di magazzino in [!INCLUDE [prod_short](includes/prod_short.md)].

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
| [Scorte disponibili](#example-inventory-on-hand) | Ottieni una panoramica degli articoli disponibili nel tuo magazzino. | [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) | **Nr. articolo**, **Quantità residua** |
|[Esempio: tenere traccia delle scorte in scadenza o vecchie](#example-track-expiring-or-old-stock) | Ottieni una panoramica degli articoli nel tuo magazzino che sono rimasti in stock per molto tempo e non vendono bene. | [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) | **Anno data di registrazione**, **Mese data di registrazione**, **Nr. articolo**, **Data di registrazione**, **Tipo movimento**, **Quantità** e **Quantità residua**. |
| [Articoli restituiti per motivo del reso](#example-returned-items-by-return-reason) | Ottieni una panoramica dei prodotti restituiti dai clienti, classificati in base al motivo del reso. Utilizza questa opzione per l'analisi del controllo di qualità. | [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) | **Cod. causa di reso**, **Mese data di registrazione**, **Quantità** , **Importo costo**, **Data di registrazione**, **Tipo documento**, **N. articolo** e **Nr. Documento**. |
| Produttività del magazzino | Ottieni una panoramica degli acquisti e delle vendite nel tuo magazzino per mese o trimestre. | [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) | **Anno data di registrazione**, **Mese data di registrazione**, **Nr. articolo**, **Quantità**, **Importo delle vendite**, **Importo del costo (effettivo)** e **Mese data di registrazione** |
| [Movimenti di magazzino] | Ottieni una panoramica di come le merci nel tuo magazzino si spostano tra le sedi. | [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) | **Codice ubicazione**, **Quantità**, **Data di registrazione**, **Nr. articolo** |

## Esempio: scorte disponibili

Per analizzare gli articoli del tuo magazzino che sono in stock, procedi nel seguente modo:

1. Apri l'elenco [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Trascina il campo **Nr. articolo** nell'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Trascina il campo **Quantità residua** nell'area **Valori**.
1. Imposta un filtro **Diverso da** su **0** in **Quantità residua**. Se non consenti livelli di stock negativi, imposta un filtro **Maggiore di** su **0**.
1. Facoltativamente, aggiungi altri campi all'analisi e magari ruota la posizione o altri campi.
1. Rinomina la scheda di analisi in **Scorte disponibili** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Esempio di come eseguire un'analisi sulle scorte disponibili." lightbox="media/data-analysis-inventory-on-hand.png":::

## Esempio: tenere traccia delle scorte in scadenza o vecchie

Per analizzare gli articoli nel tuo magazzino che sono rimasti in stock per molto tempo e non vendono bene, segui questi passaggi.

1. Apri l'elenco [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Trascina i campi **Anno data di registrazione**, **Mese data di registrazione** e **Nr. articolo** sull'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Nell'area **Colonne**, scegli i campi **Data di registrazione**, **Tipo movimento**, **Quantità** e **Quantità rimanente**.
1. Imposta un filtro **Meno di** su **Data di registrazione** per definire cosa intendi per "vecchio".
1. Rinomina la scheda di analisi in **Scorte vecchie** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Esempio di come eseguire un'analisi dei dati sullo stock scaduto nella pagina Movimenti contabili articoli." lightbox="media/data-analysis-inventory-dead-stock.png":::

## Esempio: articoli restituiti per motivo del reso

Per analizzare gli articoli restituiti ordinati in base ai motivi del reso, procedi nel seguente modo:

1. Apri l'elenco [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38).
1. Aggiungi il campo **Cod. causa di reso** 'personalizzando la pagina. Nel menu  **Impostazioni** , scegli **Personalizza**.
1. Esci dalla modalità di personalizzazione.
1. Scegli :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Trascina i campi **Cod. causa di reso** e **Mese data di registrazione** sull'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Trascina i campi **Quantità** e **Importo costo** sull'area **Valori**.
1. Aggiungi eventuali altri campi che desideri nell'analisi e abilitali nell'area **Colonne**. Ad esempio, potresti aggiungere **Data di registrazione**, **Tipo documento**, **Nr. articolo .** e  **Nr. documento**.
1. Rinomina la scheda di analisi in **Articoli restituiti per motivo del reso** o qualcosa che descriva questa analisi.  

## Esempio: produttività del magazzino

1. Apri l'elenco [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina i campi **Anno data di registrazione**, **Mese data di registrazione** e **Nr. articolo** sull'area **Gruppi di righe**.
1. Trascina i campi **Quantità**, **Importo vendite** e **Importo costo (effettivo)** sull'area **Valori**.
1. Trascina il campo **Data di registrazione (mese)** nell'area **Gruppi di colonne**.
1. Rinomina la scheda di analisi in **Produttività del magazzino per mese** o qualcosa che descriva questa analisi.  

## Movimenti di magazzino

Per tenere traccia dei movimenti di magazzino tra le ubicazioni, procedi nel seguente modo:

1. Apri l'elenco [Movimenti contabili articoli](https://businesscentral.dynamics.com/?page=38) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Trascina il campo **Codice ubicazione** nell'area **Gruppi di righe**.
1. Trascina il campo **Quantità** nell'area **Valori**.
1. Aggiungi eventuali altri campi che desideri nell'analisi e abilitali nell'area **Colonne**. Ad esempio, potresti aggiungere il campo **Nr. articolo**.
1. Rinomina la scheda di analisi in **Movimenti di magazzino** o qualcosa che descriva questa analisi.  

   > [!TIP]
   > Se aggiungi il campo Data di registrazione, puoi anche tenere traccia dei movimenti nel tempo.

## Base dati per analisi ad hoc sul magazzino

Quando registri un ordine di acquisto, [!INCLUDE [prod_short](includes/prod_short.md)] aggiorna il conto del cliente, la contabilità generale e i movimenti contabili articoli.

- Per ogni riga dell'ordine di vendita, viene creato un movimento contabile articoli nella tabella **Mov. Contabile Articoli** (se le righe di vendita contengono numeri di articolo). Inoltre, gli ordini vendita vengono sempre registrati nelle tabelle **Testate sped. vendita** e **Testate Fatt. Vendita**. Per ulteriori informazioni sulla registrazione delle vendite, vai a [Registrazione di vendite](ui-post-sales.md).

Quando registri un documento di acquisto, [!INCLUDE [prod_short](includes/prod_short.md)] aggiorna il conto del fornitore, la contabilità generale, i movimenti contabili articoli e i movimenti contabili risorse.

- Per ciascuna riga di acquisto, a seconda dei casi, vengono creati movimenti nella tabella **Mov. Contabile Articoli** (se la riga di acquisto è di tipo Articolo). Inoltre, i documenti di acquisto vengono sempre registrati nelle tabelle **Testata carico acq.** e **Testate fatt. acq**. Per ulteriori informazioni, vedi [Registrazione di acquisti](purchasing-how-record-purchases.md#posting-purchases).

## Vedere anche

[Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md)  
[Panoramica dell'analisi di magazzino](inventory-analytics-overview.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Panoramica dell'inventario](inventory-manage-inventory.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]