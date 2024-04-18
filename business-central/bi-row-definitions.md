---
title: Definizioni di riga nel reporting finanziario
description: Descrive il funzionamento delle definizioni di riga nel reporting finanziario.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Definizioni di riga nel reporting finanziario

Le definizioni di riga nei report finanziari forniscono un'area per i calcoli che non possono essere effettuati direttamente nel piano dei conti. Ad esempio, puoi creare subtotali per gruppi di conti e quindi includere quel totale in altri totali. Puoi anche calcolare passaggi intermedi che non vengono visualizzati nel report finale.

## Creare o modificare una definizione di riga

Segui questi passaggi per creare o modificare una definizione di riga:

1. Nella pagina **Report finanziari** seleziona il report finanziario pertinente e quindi scegli l'azione **Modifica definizione riga**.
1. Scegli le azioni **Inserisci conti C/G**, **Inserisci conti di cassa**, e **Inserisci tipi di costo** per creare una riga per ogni elemento finanziario che vuoi analizzare. Ad esempio, potresti avere una riga per i cespiti correnti e un'altra riga per i cespiti. Per avere un'idea, esplora i report finanziari nella società demo CRONUS.

    > [!NOTE]
    > Il campo **Nr. riga** mostra i primi 10 caratteri di un identificatore, ad esempio un numero di conto. Se aggiungi elementi con identificatori che iniziano con gli stessi 10 caratteri, avrai duplicati nel campo **Nr. riga** . Se necessario, puoi modificare manualmente gli identificatori dopo aver inserito gli elementi. Gli identificatori completi vengono visualizzati nel campo **Totale**.

> [!NOTE]
> Le colonne definite in ciascuna riga nella definizione di riga rappresentano la colonna tre e le colonne successive nella pagina **Report finanziario**. Le prime due colonne, **Nr. riga** e **Descrizione**, sono fisse.  

## Definizioni di riga integrate

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce definizioni di riga di esempio che possono aiutarti a iniziare rapidamente a configurare report finanziari che soddisfano le tue esigenze.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> I report finanziari di esempio in [!INCLUDE[prod_short](includes/prod_short.md)] non sono pronti per essere utilizzati immediatamente. A seconda del modo in cui imposti i conti C/G, le dimensioni, le categorie di conti C/G e i budget, modifica le definizioni di riga e di colonna di esempio e i report finanziari che le utilizzano in base alla tua configurazione.

## Usare le categorie di conto C/G per modificare il layout dei rendiconti finanziari

Le categorie di conto C/G consentono di modificare il layout dei rendiconti finanziari. Ad esempio, dopo aver impostato le categorie di conto nella pagina **Categorie conto C/G**, puoi scegliere l'azione **Genera report finanziari** e aggiornare i report finanziari sottostanti per i report finanziari principali. Alla successiva esecuzione di uno di questi report, ad esempio il report **Conto patrimoniale**, vengono aggiunti nuovi totali e voci secondarie.

Un altro vantaggio derivante dall'utilizzo di categorie di conto C/G rispetto ai conti C/G nelle definizioni di riga è che una modifica nella struttura del piano dei conti non influisce sui report finanziari.

> [!NOTE]
> Le categorie di conto di livello superiore, come ad esempio il nodo **Passività**, sono fisse e non è possibile aggiungerne altre. Tuttavia, è possibile eliminare e aggiungere categorie di conto ai livelli inferiori e definire la modalità di visualizzazione del report finanziario correlato nei report.
>
> Ti consigliamo di creare e strutturare da zero le proprie categorie di conto C/G di livello inferiore, se necessario in una gerarchia, anziché tentare di riorganizzare quelle esistenti. Ad esempio, è possibile ristrutturare il nodo **Passività** per contenere un nuovo nodo **Equità** seguito dai nodi **Passività correnti** e **Debiti a lungo termine**. Per saperne di più, vedi [Mapping dei conti di contabilità generale alle categorie di conti](finance-general-ledger.md#account-categories).

## Procedure consigliate per utilizzare definizioni di riga

Le definizioni di riga non hanno una versione. Quando modifichi una definizione di riga, la versione precedente viene sostituita quando la modifica viene salvata nel database. L'elenco seguente contiene alcune procedure consigliate per l'utilizzo delle definizioni di riga:

- Se aggiungi definizioni di riga, scegli un buon codice e compila il campo descrizione con un testo significativo mentre sai ancora per quale motivo usi la definizione di riga. Queste informazioni aiutano i tuoi colleghi (e te stesso in futuro) a lavorare con Financial Reporting e magari a modificare la definizione di riga.
- Prima di modificare una definizione di riga, prendine una copia come backup, nel caso in cui la modifica non funzioni come previsto. Puoi semplicemente copiare la definizione (dargli un nome appropriato) o esportarla. Per saperne di più, vedi [Importare o esportare le definizioni di riga](#import-or-export-financial-reporting-row-definitions).
- Se hai bisogno di una nuova copia di una definizione che [!INCLUDE[prod_short](includes/prod_short.md)] fornisce, un modo semplice di ottenerne una è creare una nuova società che contenga solo i dati di setup. Quindi, esporta la definizione e importala nella società in cui la definizione necessita di un aggiornamento.

## Importare o esportare definizioni di riga di reporting finanziario

Puoi importare ed esportare definizioni di riga finanziarie come pacchetti di configurazione RapidStart. Ad esempio, i pacchetti di configurazione sono utili per condividere le informazioni con altre società. Il pacchetto viene creato in un file .rapidstart, che comprime il contenuto.

> [!NOTE]
> Quando importi definizioni di riga di reporting finanziario, i record esistenti con lo stesso nome di quelli che stai importando vengono sostituiti con nuove definizioni. Il pacchetto di configurazione per una definizione di report non sovrascriverà alcuna definizione di riga o di colonna esistente utilizzata nella definizione di report.

Per importare o esportare definizioni di riga di report finanziari, procedi come segue:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Definizioni di riga** e scegli il collegamento correlato.
1. Scegli la definizione di riga, quindi scegli l'azione **Importa definizione di riga** o **Esporta definizione di riga**, a seconda di cosa vuoi fare.

## Vedere anche

[Definizioni di colonna nel reporting finanziario](bi-column-definitions.md)  
[Preparare il reporting finanziario](bi-how-work-account-schedule.md)  
[Business Intelligence finanziario](bi.md)  
[Dati finanziari](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
