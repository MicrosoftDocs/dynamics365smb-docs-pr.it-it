---
title: Analisi ad hoc dei dati sulle vendite
description: Informazioni su come utilizzare la modalità di analisi dei dati per analizzare i dati di vendita.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-sales-data"></a>Analisi ad hoc dei dati sulle vendite

Questo articolo spiega come utilizzare la funzionalità **Analisi dei dati** per analizzare i dati di vendita direttamente dalle pagine di elenco e dalle query. Non è necessario eseguire un report o passare a un'altra applicazione, come Excel. La funzionalità fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "Miei clienti" o "Statistiche vendite" o qualsiasi altra visualizzazione tu possa immaginare. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

Utilizza le seguenti pagine di elenco per analisi ad hoc dei processi di vendita:

- [Ordini di vendita](https://businesscentral.dynamics.com/?page=9305)
- Movimenti C/G
- [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25)
- Movimenti contabili articoli
- Fatture di vendita registrate
- Ordini di reso vendita

## <a name="sales-ad-hoc-analysis-scenarios"></a>Scenari di analisi di vendita ad hoc

Utilizza la funzione **Analisi dei dati** per un rapido controllo dei fatti e un'analisi ad hoc:

- Se non vuoi eseguire un report.
- Se non esiste un report per la tua esigenza specifica.
- Se desideri eseguire rapidamente l'iterazione per ottenere una buona panoramica di una parte della tua attività.

Le sezioni seguenti forniscono esempi di scenari di vendita in [!INCLUDE [prod_short](includes/prod_short.md)].

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
| [Vendite (volume delle vendite previsto)](#example-sales-expected-sales-volume) | Analizza il volume delle vendite previsto. | [Ordini di vendita](https://businesscentral.dynamics.com/?page=9305) | **Nome cliente di vendita**, **Nr. cliente di vendita**, **Nr.** , **Importo**, **Data documento (anno)** e **Data documento (mese)**. |
| [Vendite (vendite clienti per volume)](#example-sales-customer-sales-by-volume) | Ottieni una panoramica dei clienti che acquistano di più o devono di più. | [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) | **Ragione Sociale**, **N. documento**, **Importo** e **Importo residuo**. |
| [Finanza (Contabilità clienti)](#example-finance-accounts-receivables) | Per vedere ciò che ti devono i tuoi clienti, ad esempio suddiviso in intervalli di tempo per quando gli importi sono dovuti. | [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) | **Ragione Sociale**, **Scadenza** e **Importo residuo**. |

## <a name="example-sales-expected-sales-volume"></a>Esempio: Vendite (volume delle vendite previsto)

Per analizzare il volume delle vendite previsto e gli importi delle vendite per gli ordini non spediti per ciascun cliente per anno o mese, procedi nel seguente modo:

1. Apri l'elenco [Ordini vendita](https://businesscentral.dynamics.com/?page=9305) e attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva la modalità **Pivot** (situata direttamente sopra il campo **Ricerca**).
1. Trascina i campi **Nome cliente di vendita**, **Nr. cliente di vendita** e **Nr.** nell'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Trascina il campo **Importo** nell'area **Valori**.
1. Trascina i campi **Data documento (anno)** e **Data documento (mese)** nell'area **Etichette di colonna**. Trascina i campi in quest'ordine.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri aggiuntivi**. Il menu si trova nella parte destra della pagina, appena sotto il menu **Colonne**.
1. Rinomina la scheda di analisi in **Volume di vendite previsto** o qualcosa che descriva questa analisi.

## <a name="example-sales-customer-sales-by-volume"></a>Esempio: Vendite (vendite clienti per volume)

Per produrre una panoramica dei clienti che acquistano di più o devono di più, procedi come segue:

1. Apri l'elenco [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) e attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Trascina il campo **Ragione Sociale** nell'area **Gruppi di righe** e il campo **Documento numero** sottostante.
1. Scegli i campi **Importo** e **Importo residuo**.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri aggiuntivi**. Il menu si trova nella parte destra della pagina, appena sotto il menu **Colonne**.
1. Rinomina la scheda di analisi in **Cliente per volume di vendite** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili clienti." lightbox="media/data-analysis-customer-ledger-entries.png":::

## <a name="example-finance-accounts-receivables"></a>Esempio: Finanza (Contabilità clienti)

Per vedere ciò che ti devono i tuoi clienti, magari suddiviso in intervalli di tempo per quando gli importi sono dovuti, segui questi passaggi:

1. Apri l'elenco [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) e attiva la modalità di analisi.
1. Nel menu **Colonne**, rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva la modalità **Pivot** (situata direttamente sopra il campo **Ricerca**).
1. Trascina il campo **Ragione sociale** nell'area **Gruppi di righe** e trascina il campo **Importo rimanente** nell'area **Valori**.
1. Trascina il campo **Data scadenza (mese)** nell'area **Etichette di colonna**.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri aggiuntivi**. Il menu si trova nella parte destra della pagina, appena sotto il menu **Colonne**.
1. Rinomina la scheda di analisi in **Scadenziari per mese** o qualcosa che descriva questa analisi.

## <a name="data-foundation-for-ad-hoc-analysis-on-sales"></a>Base dati per analisi ad hoc sulle vendite

Dopo aver immesso le informazioni su un ordine di vendita e aggiunto tutte le righe dell'ordine di vendita, puoi registrare l'ordine. La registrazione crea una spedizione e una fattura. [!INCLUDE [prod_short](includes/prod_short.md)] aggiorna il conto, la contabilità generale e i movimenti contabili articoli del cliente.

- Per ciascun ordine di vendita, viene creata una tabella **Movimento C/G**. Vengono inoltre creati un movimento nel conto del cliente nella tabella **Mov. contabili clienti** e un movimento C/G nel relativo conto crediti. Inoltre, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento di contabilità generale relativi all'importo dello sconto.
- Per ciascuna riga dell'ordine di vendita, viene creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di vendita contengono numeri di articolo) oppure un movimento C/G nella tabella **Movimenti C/G** (se le righe di vendita contengono un conto C/G). Inoltre, gli ordini vendita vengono sempre registrati nelle tabelle **Testate sped. vendita** e **Testate Fatt. Vendita**.

Per ulteriori informazioni sulla registrazione delle vendite, vai a [Registrazione di vendite](ui-post-sales.md).

## <a name="see-also"></a>Vedere anche

[Registrazione di vendite](ui-post-sales.md)  
[Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md)  
[Panoramica delle analisi delle vendite](sales-analytics-overview.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Panoramica delle vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
