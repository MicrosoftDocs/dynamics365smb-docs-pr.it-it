---
title: Esecuzione di previsioni di flusso di cassa utilizzando i report finanziari
description: In questa procedura dettagliata viene descritto come utilizzare i report finanziari per effettuare previsioni del flusso di cassa in Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: edupont
---
# Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando i report finanziari

In questa procedura dettagliata viene descritto come utilizzare la funzionalità dei report finanziari per effettuare previsioni del flusso di cassa. I report finanziari consentono di effettuare i calcoli che non possono essere eseguiti direttamente nel piano dei conti di cassa. Nei report finanziari puoi impostare i subtotali relativi agli incassi e alle uscite di cassa. I subtotali possono essere inclusi nei nuovi totali che potranno essere utilizzati per effettuare le previsioni del flusso di cassa.  

## Informazioni sulla procedura dettagliata

In questa procedura dettagliata sono descritti i task seguenti:  

- Impostazione di un nuovo nome del report finanziario del flusso di cassa.  
- Impostazione delle righe di report finanziario.  
- Impostazione di una nuova definizione di colonna.  
- Assegnazione di una definizione di colonna a un report finanziario.  
- Visualizzazione e stampa della previsione del flusso di cassa.  

### Prerequisiti

Per completare questa procedura dettagliata, sarà necessario:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Un prospetto del flusso di cassa con righe registrate  

## Ruoli

Questa procedura dettagliata comprende task svolti dal ruolo utente seguente:  

- Controller  

## Scenario

Ken è un manager presso CRONUS che effettua previsioni del flusso di cassa mensili. Egli include interessi, vendite, acquisti e cespiti nelle previsioni che presenta alla DF Sara per un'opinione in merito.  

## Impostazione di un nuovo nome del report finanziario

Il nome del report finanziario è il nome assegnato alla previsione del flusso di cassa che include una serie di righe definite e una definizione di colonna.  

### Impostare un nuovo nome del report finanziario  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.  
2. Sulla pagina **Report finanziari** scegli **Nuovo** per creare un nuovo nome per il report finanziario del flusso di cassa.  
3. Nel campo **Nome** immettere **Previsione**.  
4. Nel campo **Descrizione** immettere **Previsione flusso di cassa**.  
5. Lascia i campi **Definizione riga** e **Definizione colonna** vuoti.

## Impostazione delle righe di definizione di riga

Dopo aver impostato il nome di un report finanziario, Ken definisce ogni riga nel report finanziario del flusso di cassa. Definisce le righe che possono essere visualizzate nei report, nonché le righe utilizzate solo per scopi di calcolo.  

### Impostare le righe di definizione di riga  

1. Sulla pagina **Report finanziari** seleziona il nuovo report finanziario **Previsione** che hai creato, quindi scegli l'azione **Modifica definizione riga**.  
2. Nella pagina **Definizione riga** immetti ogni riga come indicato nella tabella riportata di seguito.  

    > [!TIP]  
    > Utilizza la funzione **Inserisci conti di costo e nolo** per contrassegnare rapidamente i conti di cassa nel relativo piano e copiarli nelle righe della definizione riga.  

    | Numero di riga | Descrizione              | Tipo totale            | Totale | Tipo di riga   | Tipo di importo | Mostra |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Contabilità clienti              | Conti movimento flusso di cassa | 10       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Ordini vendita aperti        | Conti movimento flusso di cassa | 20       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Noleggi                  | Conti movimento flusso di cassa | 30       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Beni finanziari         | Conti movimento flusso di cassa | 40       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Cessione cespiti    | Conti movimento flusso di cassa | 50       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Investimenti privati      | Conti movimento flusso di cassa | 60       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Carichi vari   | Conti movimento flusso di cassa | 70       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Ordini assistenza aperti      | Conti movimento flusso di cassa | 80       |Saldo periodo | Importo netto  | Sì  |
    | R20     | Incassi totali      | Formula                  | R10      |Saldo periodo | Importo netto  | Sì  |
    | R30     | Contabilità fornitori                 | Conti movimento flusso di cassa | 1010     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Ordini acquisto aperti     | Conti movimento flusso di cassa | 1020     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Costi personale          | Conti movimento flusso di cassa | 1030     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Costi di gestione            | Conti movimento flusso di cassa | 1040     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Costi finanziari            | Conti movimento flusso di cassa | 1050     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Investimenti              | Conti movimento flusso di cassa | 1070     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Consumi privati     | Conti movimento flusso di cassa | 1090     |Saldo periodo | Importo netto  | Sì  |
    | R30     | IVA a debito                  | Conti movimento flusso di cassa | 1100     |Saldo periodo | Importo netto  | Sì  |
    | R30     | Altre spese           | Conti movimento flusso di cassa | 1110     |Saldo periodo | Importo netto  | Sì  |
    | R40     | Uscite di cassa totali | Formula                  | R30      |Saldo periodo | Importo netto  | Sì  |
    | R50     | Surplus                  | Formula                  | R20+R40  |Saldo periodo | Importo netto  | Sì  |
    | R60     | Investimenti flusso di cassa          | Conti movimento flusso di cassa | 2100     |Saldo periodo | Importo netto  | Sì  |
    | R70     | Flusso di cassa totale          | Formula                  | R50+R60  |Saldo periodo | Importo netto  | Sì  |

    > [!NOTE]
    > Il numero di riga R10 viene utilizzato per acquisire i totali conto relativi alla contabilità clienti. Il numero di riga R20 viene utilizzato per calcolare la somma di tutti gli incassi. Il numero di riga R30 viene utilizzato per acquisire i totali conto relativi alla contabilità fornitori. Il numero di riga R40 viene utilizzato per calcolare la somma di tutte le uscite di cassa. Il numero di riga R50 viene utilizzato per acquisire la somma del surplus di cassa. Il numero di riga R60 viene utilizzato per acquisire i fondi liquidi. Il numero di riga R70 viene utilizzato per calcolare il flusso di cassa previsto.

## Impostazione di una nuova definizione di colonna

Prima di poter stampare la previsione del flusso di cassa, Ken deve creare la definizione di colonna per le informazioni numeriche. Nelle colonne definisce le informazioni che desidera utilizzare dalle righe.

- La prima colonna è contrassegnata dal numero *C10* con il titolo **Importo** e contiene il saldo periodo.  
- La seconda colonna è contrassegnata dal numero *C20* con il titolo **Saldo alla data** e contiene le transazioni per il periodo.  
- La terza colonna è contrassegnata dal numero *C30* con il titolo **Anno intero** e contiene il saldo periodo nei saldi dell'intero anno fiscale.  
- Ken assegna infine la definizione di colonna come opzione predefinita per il report finanziario **Previsione**.  

### Impostare una nuova definizione di colonna

1. Sulla pagina **Report finanziari** seleziona il nome del nuovo report finanziario **Previsione** che hai creato. Nel gruppo **Processo** della scheda **Pagina iniziale** scegli **Modifica definizione colonna**.

2. Crea una nuova definizione di colonna con il nome **Flusso di cassa**.

3. Scegli il pulsante **OK**.

4. Immettere ogni riga esattamente come indicato nella tabella riportata di seguito.

    |Nr. colonna|Testata colonna|Tipo colonna|Tipo movimento contabile|Tipo importo|Mostra|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Importo|Saldo periodo|Movimenti|Importo netto|Sempre|  
    |C20|Importo fino alla data|Saldo alla data|Movimenti|Importo netto|Sempre|  
    |C30|Anno fiscale intero|Anno fiscale intero|Movimenti|Importo netto|Sempre|

## Assegnazione della definizione di colonna al nome del report finanziario

Ken è ora pronto per assegnare la definizione di colonna al nome del report finanziario.  

### Assegnare la definizione di colonna al nome del report finanziario

1. Sulla pagina **Report finanziari** seleziona il nuovo report finanziario **Previsione**, quindi scegli l'azione **Modifica definizione colonna**.  
2. Nel campo **Nome** seleziona la definizione di colonna **Flusso di cassa** da assegnare come definizione di colonna predefinita.  

## Visualizzare e stampare la previsione del flusso di cassa

1. Sulla pagina **Report finanziari** scegli il report finanziario **Previsione** per visualizzare la previsione del flusso di cassa.  
2. Nella pagina **Report finanziario** è possibile selezionare un importo e quindi visualizzare i movimenti di previsione del flusso di cassa che compongono l'importo. Inoltre, è possibile visualizzare la formula utilizzata per calcolare l'importo. È anche possibile filtrare gli importi per data e dimensioni.  
3. Scegliere l'azione **Stampa** per stampare la previsione del flusso di cassa.  

## Vedi il relativo [training Microsoft](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## Vedere anche

[Utilizzare i report finanziari](bi-how-work-account-schedule.md)  
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
