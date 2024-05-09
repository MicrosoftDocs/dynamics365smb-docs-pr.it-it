---
title: Analisi ad hoc negli acquisti
description: Scopri come utilizzare la modalità di analisi dei dati per analizzare i dati negli acquisti.
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

# Analisi ad hoc negli acquisti

In questo articolo viene descritto come analizzare i dati sugli acquisti delle pagine elenco e delle query utilizzando la funzionalità **Analisi dei dati**. La funzionalità ti consente di analizzare i dati direttamente dalla pagina, senza dover eseguire un report o aprire un'altra applicazione come Excel. Analisi dei dati fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "Fornitori personali" o "Statistiche acquisti" o qualsiasi altra visualizzazione tu possa immaginare. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

Utilizza le seguenti pagine di elenco per analisi ad hoc dei processi di acquisto:

- [Ordini acquisto](https://businesscentral.dynamics.com/?page=9307)
- [Righe acquisto](https://businesscentral.dynamics.com/?page=518)
- [Fatture di acquisto registrate](https://businesscentral.dynamics.com/?page=146)
- [Mov. contabili fornitori](https://businesscentral.dynamics.com/?page=29)
- [Movimenti C/G](https://businesscentral.dynamics.com/?page=20)

## Scenari di analisi ad hoc per gli acquisti

Utilizza la funzione **Analisi dei dati** per un rapido controllo dei fatti e un'analisi ad hoc:

- Se non vuoi eseguire un report
- Se non esiste un report per le tue esigenze specifiche
- Se desideri eseguire rapidamente l'iterazione per ottenere una buona panoramica di una parte della tua attività.

Le sezioni seguenti forniscono esempi di scenari di acquisto in [!INCLUDE [prod_short](includes/prod_short.md)].

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
| [Panoramica di GRNI](#example-goods-received-not-invoiced-grni-overview) | Ottieni una panoramica Merci ricevute, non fatturate (GRNI) per tutti i fornitori. | **Tipo**, **Importo carichi non fatt. (VL)** (filtro su questi campi), **N. fornitore**, **Nr. documento**, **Nr.** e **Amt. Ric. Non fatturato (LCY)** <br> **NOTE:** per aggiungere questi campi, devi personalizzare la pagina. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md). | 
| [Finanza (Contabilità fornitori)](#example-finance-accounts-payable) | Per vedere ciò che ti devono i tuoi fornitori, magari suddiviso in intervalli di tempo per quando gli importi sono dovuti. | [Mov. contabili fornitori](https://businesscentral.dynamics.com/?page=29) | **Nome fornitore**, **Tipo documento**, **Nr. documento**, **Data scadenza (anno)**, **Data scadenza (mese)** e **Importo residuo**. |

## Esempio: panoramica Merci ricevute, non fatturate (GRNI)

Per creare una panoramica Merci ricevute, non fatturate (GRNI) tra i fornitori, procedi come segue:
 
1. Apri la pagina elenco [Righe acquisto](https://businesscentral.dynamics.com/?page=518).
1. Personalizza la pagina per aggiungere il campo **Importo ricevuto non fatturato**. Per personalizzare la pagina, scegli **Impostazioni**, quindi **Personalizza**.
1. Attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Nel menu **Filtri aggiuntivi** (a destra della pagina, appena sotto il menu **Colonne**), imposta i seguenti filtri:
    - **Tipo = Articolo**
    - **Importo carichi non fatt. (VL) > 0**. 
1. Trascina i campi **N. fornitore**, **Nr. documento** e **Nr.** nell'area **Gruppi di righe**. Trascina i campi in quest'ordine.
1. Aggiungi il campo **Importo carichi non fatt. (VL)** per includerlo nella panoramica.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri aggiuntivi**. Il menu si trova nella parte destra della pagina, appena sotto il menu **Colonne**.
1. Rinomina la scheda di analisi in **Merci ricevute, non fatturate (GRNI)** o qualcosa che descriva questa analisi.

## Esempio: Finanza (Contabilità fornitori)

Per vedere ciò che devi ai tuoi fornitori, magari suddiviso in intervalli di tempo per quando gli importi sono dovuti, segui questi passaggi:

1. Apri la pagina elenco [Movimenti contabili fornitori](https://businesscentral.dynamics.com/?page=29) e attiva la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva la modalità **Pivot** (situata direttamente sopra il campo **Ricerca**).
1. Trascina i campi **Nome fornitore**, **Tipo di documento** e **Nr. documento** nell'area **Gruppi di righe**, quindi trascina il campo **Importo residuo** nell'area **Valori**.
1. Trascina i campi **Data scadenza (anno)** e **Data scadenza (mese)** nell'area **Etichette di colonna**. Trascina i campi in quest'ordine.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri aggiuntivi** (a destra della pagina, appena sotto il menu **Colonne**).
1. Rinomina la scheda di analisi in **Scadenziari fornitori per mese** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili clienti." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## Base dati per analisi ad hoc sugli acquisti

Quando registri un documento di acquisto, [!INCLUDE [prod_short](includes/prod_short.md)] aggiorna il conto del fornitore, la contabilità generale, i movimenti contabili articoli e i movimenti contabili risorse:

- Per ciascun documento di acquisto viene creato un movimento di acquisto nella tabella **Movimenti C/G**. Vengono inoltre creati un movimento nel conto del fornitore nella tabella **Movimento contabile fornitore** e un movimento C/G nel conto passività pertinente. Inoltre, la registrazione dell'acquisto potrebbe generare un movimento IVA e un movimento C/G relativi all'importo dello sconto.
- Per ogni riga di acquisto, se applicabile, verranno create le seguenti voci:
  - La tabella **Movimento contabile articolo** se la riga di acquisto è di tipo Articolo.
  - La tabella **Movimento C/G** se le righe di acquisto sono di tipo Conto G/C.
  - Tabella **Movimento contabile risorsa** se la riga di acquisto è di tipo Risorsa.
- Inoltre, i documenti di acquisto vengono sempre registrati nelle tabelle **Testata carico acq.** e **Testate fatt. acq**.

Per ulteriori informazioni, vedi [Registrazione di acquisti](purchasing-how-record-purchases.md#posting-purchases).

## Vedere anche

[Registrazione di acquisti](purchasing-how-record-purchases.md#posting-purchases)  
[Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md)  
[Panoramica degli acquisti](purchasing-manage-purchasing.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Panoramica degli acquisti](purchasing-manage-purchasing.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]