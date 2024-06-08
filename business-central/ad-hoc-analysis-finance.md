---
title: Analisi ad hoc dei dati finanziari
description: Informazioni su come utilizzare la modalità di analisi dei dati per analizzare i dati finanziari.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-finance-data"></a>Analisi ad hoc dei dati finanziari

Questo articolo spiega come utilizzare la funzionalità **Analisi dei dati** per analizzare i dati finanziari direttamente dalle pagine di elenco e dalle query. Non è necessario eseguire un report o passare a un'altra applicazione, come Excel. La funzionalità fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Alcuni esempi sono "Totale attività nel tempo", "Contabilità clienti", "Contabilità fornitori" o qualsiasi altra visualizzazione tu possa immaginare. Per ulteriori informazioni su come utilizzare la funzionalità **Analisi dei dati**, vai a [Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md).

Utilizza le seguenti pagine di elenco per iniziare a eseguire analisi ad hoc dei processi finanziari:

- [Movimenti C/G](https://businesscentral.dynamics.com/?page=20)
- [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25)
- [Mov. contabili fornitori](https://businesscentral.dynamics.com/?page=29)

## <a name="ad-hoc-analysis-scenarios-in-finance"></a>Scenari di analisi ad hoc in finanza

Utilizza la funzione **Analisi dei dati** per un rapido controllo dei fatti e un'analisi ad hoc:

- Se non vuoi eseguire un report.
- Se non esiste un report per la tua esigenza specifica.
- Se desideri eseguire rapidamente l'iterazione per ottenere una buona panoramica di una parte della tua attività.

Le sezioni seguenti forniscono esempi di scenari finanziari in [!INCLUDE [prod_short](includes/prod_short.md)].

| Ad area | Per... | Apri questa pagina in modalità di analisi | Utilizzando questi campi |
| ---- | ----- | ------------------------------- |------------------- |
|[Esempio: Finanza (contabilità clienti)](#example-finance-accounts-receivable) | Per vedere ciò che ti devono i tuoi clienti, ad esempio suddiviso in intervalli di tempo per quando gli importi sono dovuti. | [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) | **Ragione Sociale**, **Scadenza** e **Importo residuo** |
| [Finanza (Contabilità fornitori)](#example-finance-accounts-payable) | Per vedere ciò che ti devono i tuoi fornitori, magari suddiviso in intervalli di tempo per quando gli importi sono dovuti. | [Mov. contabili fornitori](https://businesscentral.dynamics.com/?page=29) | **Nome fornitore**, **Tipo documento**, **Nr. documento**, **Data scadenza (anno)**, **Data scadenza (mese)** e **Importo residuo**. |
| [Finanza (fatture di vendita per conto Co.Ge.)](#example-finance-sales-invoices-by-gl-account) | Scopri come le tue fatture di vendita vengono distribuite sui conti Co.Ge. dal piano dei conti, ad esempio, suddivise in intervalli di tempo in cui sono stati registrati gli importi. | [Movimenti C/G](https://businesscentral.dynamics.com/?page=20) | **Nome conto Co.Ge.**, **Codice sorgente**, **Nome conto Co.Ge.**,  **N. conto Co.Ge.**, **Importo debito**, **Importo credito**, **Data di pubblicazione Anno**, **Data di pubblicazione Trimestre** e **Data di pubblicazione Data Mese** |
| [Finanza (Conto economico)](#example-finance-income-statement) | Visualizza il tuo reddito sui conti economici dal piano dei conti, ad esempio, suddiviso in intervalli di tempo in cui sono stati registrati gli importi. | [Movimenti C/G](https://businesscentral.dynamics.com/?page=20) | **Nr. conto C/G**, **Data di registrazione** e **Quantità**. |
| [Finanza (totale attività)](#example-finance-total-assets) | Visualizza le attività sui conti cespiti dal piano dei conti, ad esempio, suddiviso in intervalli di tempo in cui sono stati registrati gli importi. | [Movimenti C/G](https://businesscentral.dynamics.com/?page=20) | **Nr. conto C/G**, **Data di registrazione** e **Quantità**. |

### <a name="example-finance-accounts-receivable"></a>Esempio: Finanza (contabilità clienti)

Per vedere ciò che ti devono i tuoi clienti, magari suddiviso in intervalli di tempo per quando gli importi sono dovuti, segui questi passaggi:

1. Apri l'elenco [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo *Ricerca* sulla destra).
1. Attiva l'interruttore **Modalità* Pivot** (situato sopra il campo **Cerca** sulla destra).
1. Trascina il campo **Ragione sociale** nell'area **Gruppi di righe** e trascina il campo **Importo rimanente** nell'area **Valori**.
1. Trascina il campo **Data scadenza (mese)** nell'area **Etichette di colonna**.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri analisi** (che si trova sotto il menu **Colonne** sulla destra).
1. Rinomina la scheda di analisi in **Scadenziari per mese** o qualcosa che descriva questa analisi.

### <a name="example-finance-accounts-payable"></a>Esempio: Finanza (Contabilità fornitori)

Per vedere ciò che devi ai tuoi fornitori, magari suddiviso in intervalli di tempo per quando gli importi sono dovuti, segui questi passaggi:

1. Apri la pagina elenco [Movimenti contabili fornitori](https://businesscentral.dynamics.com/?page=29) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina i campi **Nome fornitore**, **Tipo di documento** e **Nr. documento** nell'area **Gruppi di righe**, quindi trascina il campo **Importo residuo** nell'area **Valori**.
1. Trascina i campi **Data scadenza (anno)** e **Data scadenza (mese)** nell'area **Etichette di colonna**. Trascina i campi in quest'ordine.
1. Per eseguire l'analisi per un determinato anno o trimestre, applica un filtro nel menu **Filtri analisi** (che si trova sotto il menu **Colonne** sulla destra).
1. Rinomina la scheda di analisi in **Scadenziari fornitori per mese** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili clienti." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### <a name="example-finance-sales-invoices-by-gl-account"></a>Esempio: Finanza (fatture di vendita per conto Co.Ge.)

Per visualizzare la distribuzione delle fatture di vendita sui conti Co.Ge. dal piano dei conti, ad esempio, suddivise in intervalli di tempo in base ai quali sono stati registrati gli importi, attenersi alla seguente procedura:

1. Apri la pagina [Movimenti contabili generali](https://businesscentral.dynamics.com/?page=20) .
1. Aggiungi i campi **Nome conto Co.Ge.** e **Codice sorgente** personalizzando la pagina. Nel menu  **Impostazioni** , scegli **Personalizza**.
1. Esci dalla modalità di personalizzazione.
1. Scegli :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Nel menu  **Filtri di analisi**, imposta un filtro nel campo **Codice sorgente** su **VENDITE**. Se disponi di personalizzazioni che aggiungono altri valori, puoi aggiungere anche quelle.
1. Nel menu **Colonne**, rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca**).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina i campi **Nome conto Co.Ge.** e **N. conto Co.Ge.** su **Area gruppi di righe** .
1. Trascina i campi **Importo debito** e **Importo credito** su **Valori** zona.
1. Trascina  **Anno data di pubblicazione**, **Trimestre data di pubblicazione** e **Mese data di pubblicazione** campi nell'area **Etichette colonna** .
1. Rinomina la scheda di analisi in **Disaggregazione fatture per account** o qualcosa che descriva questa analisi.

L'immagine seguente mostra il risultato di questi passaggi.

:::image type="content" source="media/data-analysis-gl-entries-invoices.png" alt-text="Esempio di come eseguire l'analisi dei dati nella pagina Movimenti contabili C/G (per comprendere le registrazioni delle vendite)." lightbox="media/data-analysis-gl-entries-invoices.png":::

### <a name="example-finance-income-statement"></a>Esempio: Finanza (Conto economico)

Per vedere il tuo reddito sui conti economici dal piano dei conti, ad esempio, suddiviso in intervalli di tempo in cui sono stati registrati gli importi, segui questi passaggi:

1. Apri l'elenco [Movimenti C/G](https://businesscentral.dynamics.com/?page=20) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina il campo **Nr. conto C/G** nell'area **Gruppi di righe** e trascina il campo **Importo rimanente** nell'area **Valori**.
1. Trascina il campo **Data di registrazione (mese)** nell'area **Etichette di colonna**.
1. Per il conto economico, filtra in base ai conti che utilizzi. Nei dati demo [!INCLUDE [prod_short](includes/prod_short.md)], questi conti iniziano con "4", ma il tuo piano dei conti potrebbe essere diverso. Imposta un filtro sui conti nel menu **Filtri analisi** (situato sotto il menu **Colonne** sulla destra).

   > [!TIP]
   > Per vedere quali conti sono utilizzati nella tua configurazione, esegui il report [Bilancio di verifica per periodo](https://businesscentral.dynamics.com/?report=38).

1. Rinomina la scheda di analisi in **Ricavi per mese** o qualcosa che descriva questa analisi.

### <a name="example-finance-total-assets"></a>Esempio: Finanza (totale attività)

Per vedere le tue attività sui conti cespiti dal piano dei conti, ad esempio, suddiviso in intervalli di tempo in cui sono stati registrati gli importi, procedi come segue:

1. Apri l'elenco [Movimenti C/G](https://businesscentral.dynamics.com/?page=20) e scegli l'icona :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entra in modalità analisi"::: per attivare la modalità di analisi.
1. Vai al menu **Colonne** e rimuovi tutte le colonne (seleziona la casella accanto al campo **Ricerca** sulla destra).
1. Attiva l'interruttore **Modalità Pivot** (situato sopra il campo **Ricerca** a destra).
1. Trascina il campo **Nr. conto C/G** nell'area **Gruppi di righe** e trascina il campo **Importo rimanente** nell'area **Valori**.
1. Trascina il campo **Data di registrazione (mese)** nell'area **Etichette di colonna**.
1. Per il conto delle attività totali, filtra in base ai conti che utilizzi. Nei dati demo [!INCLUDE [prod_short](includes/prod_short.md)], questi conti iniziano con "10", ma il tuo piano dei conti potrebbe essere diverso. Imposta un filtro sui conti appropriati nel menu **Filtri aggiuntivi** (situato sotto il menu **Colonne** sulla destra).

   > [!TIP]
   > Per vedere quali conti sono utilizzati nella tua configurazione, esegui il report [Bilancio di verifica per periodo](https://businesscentral.dynamics.com/?report=38).

1. Rinomina la scheda di analisi in **Ricavi per mese** o qualcosa che descriva questa analisi.

## <a name="data-foundation-for-ad-hoc-analysis-on-finance"></a>Base dati per analisi ad hoc sulla finanza

Quando si registrano i giornali di registrazione, [!INCLUDE [prod_short](includes/prod_short.md)] crea movimenti nella tabella **Movimento C/G**. Pertanto, l'analisi ad hoc sulla finanza generale viene in genere eseguita nella pagina [Movimenti C/G](https://businesscentral.dynamics.com/?page=20) . Per la contabilità clienti e fornitori, è possibile analizzare rispettivamente [Movimenti contabili clienti](https://businesscentral.dynamics.com/?page=25) e [Movimenti contabili fornitori](https://businesscentral.dynamics.com/?page=29).

Per saperne di più, vai ai seguenti articoli:

- [Base dati per analisi ad hoc sulle vendite](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Base dati per analisi ad hoc sugli acquisti](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## <a name="see-also"></a>Vedere anche

[Analizzare dati di elenco e query con la modalità di analisi](analysis-mode.md)  
[Panoramica di Analisi finanziaria](bi.md)  
[Panoramica di analisi, business Intelligence e reporting](reports-bi-reporting.md)  
[Panoramica dei dati finanziari](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
