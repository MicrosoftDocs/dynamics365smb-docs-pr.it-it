---
title: 'Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando le situazioni contabili'
description: Informazioni su come utilizzare le situazioni contabili per effettuare previsioni del flusso di cassa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48a176c4c363c4a33ae336d754be71c9f7dd0aeb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772106"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando le situazioni contabili

In questa procedura dettagliata viene descritto come utilizzare le situazioni contabili per effettuare previsioni del flusso di cassa. Le situazioni contabili consentono di effettuare i calcoli che non possono essere eseguiti direttamente nel piano dei conti di cassa. Nelle situazioni contabili è possibile impostare i subtotali relativi agli incassi e alle uscite di cassa. I subtotali possono essere inclusi nei nuovi totali che potranno essere utilizzati per effettuare le previsioni del flusso di cassa.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata

In questa procedura dettagliata sono descritti i task seguenti:  

- Impostazione di un nuovo nome della situazione contabile del conto di cassa.  
- Impostazione delle righe della situazione contabile.  
- Impostazione di un nuovo layout colonna.  
- Assegnazione di un layout colonna a una situazione contabile.  
- Visualizzazione e stampa della previsione del flusso di cassa.  

### <a name="prerequisites"></a>Prerequisiti

Per completare questa procedura dettagliata, sarà necessario:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Registrazione delle righe del prospetto del flusso di cassa  

## <a name="roles"></a>Ruoli

Questa procedura dettagliata comprende task svolti dal ruolo utente seguente:  

- Controller  

## <a name="story"></a>Scenario

Ken è un manager presso CRONUS che effettua previsioni del flusso di cassa mensili. Egli include interessi, vendite, acquisti e cespiti nella previsione che presenta alla DF Sara per un'opinione in merito.  

## <a name="setting-up-a-new-account-schedule-name"></a>Impostazione di un nuovo nome della situazione contabile

Una situazione contabile è costituita da un nome della situazione contabile del conto di cassa con una serie di righe e da un layout colonna.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Per impostare un nuovo nome situazione contabile  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Situazioni contabili** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Descr. situazioni contabili** scegliere l'azione **Nuovo** per creare un nuovo nome della situazione contabile del conto di cassa.  
3. Nel campo **Nome** immettere **Previsione**.  
4. Nel campo **Descrizione** immettere **Previsione flusso di cassa**.  
5. Lasciare vuoti i campi **Default layout colonna** e **Nome visual. analisi**.  

## <a name="setting-up-account-schedule-lines"></a>Impostazione delle righe della situazione contabile

Dopo aver impostato un nome della situazione contabile, Ken definisce tutte le righe che verranno visualizzate nella situazione contabile del conto di cassa. Egli definisce le righe che possono essere visualizzate nei report, nonché le righe utilizzate solo per scopi di calcolo.  

### <a name="to-set-up-account-schedule-lines"></a>Per impostare le righe della situazione contabile  

1. Nella pagina **Descr. situazioni contabili** selezionare il nuovo nome della situazione contabile **Previsione** creato e quindi scegliere l'azione **Modifica situazione contabile**.  
2. Nella pagina **Situazione contabile** immettere ogni riga come indicato nella tabella riportata di seguito.  

    > [!TIP]  
    >  Utilizzando la funzione **Inserisci conti di costo e nolo**, è possibile contrassegnare rapidamente i conti di cassa del relativo piano e copiarli nelle righe della situazione contabile.  

    | Nr. riga | Descrizione              | Tipo totale            | Totale | Tipo di riga   | Tipo importo | Mostra |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Ordini vendita aperti        | Conti movimento flusso di cassa | 20       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Noleggi                  | Conti movimento flusso di cassa | 30       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Beni finanziari         | Conti movimento flusso di cassa | 40       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Cessione cespiti    | Conti movimento flusso di cassa | 50       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Investimenti privati      | Conti movimento flusso di cassa | 60       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Carichi vari   | Conti movimento flusso di cassa | 70       |Saldo periodo | Importo netto  | Sì  |
    | R10     | Ordini assistenza aperti      | Conti movimento flusso di cassa | 80       |Saldo periodo | Importo netto  | Sì  |
    | R20     | Incassi totali      | Formula                  | R10      |Saldo periodo | Importo netto  | Sì  |
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

## <a name="setting-up-a-new-column-layout"></a>Impostazione di un nuovo layout colonna

Prima di poter stampare la previsione del flusso di cassa, Ken deve creare il layout colonna per le informazioni numeriche. Nelle colonne definisce le informazioni che desidera utilizzare dalle righe.

- La prima colonna è contrassegnata dal numero *C10* con il titolo **Importo** e contiene il saldo periodo.  
- La seconda colonna è contrassegnata dal numero *C20* con il titolo **Saldo alla data** e contiene le transazioni per il periodo.  
- La terza colonna è contrassegnata dal numero *C30* con il titolo **Anno intero** e contiene il saldo periodo nei saldi dell'intero anno fiscale.  
- Ken assegna infine il layout colonna come layout colonna di default per la situazione contabile **Previsione**.  

## <a name="to-set-up-a-new-column-layout"></a>Per impostare un nuovo layout colonna

1. Nella finestra **Descr. situazioni contabili** selezionare il nome della nuova situazione contabile **Previsione** creata. Nel gruppo **Processo** della scheda **Pagina iniziale** scegliere **Modifica setup layout colonna**.

    > [!TIP]
    > È possibile trovare la stessa azione nella pagina **Situazione contabile** qualora sia ancora in corso la modifica della situazione contabile **Previsione**.

2. Creare un nuovo layout colonna con il nome **Flusso di cassa**.

3. Scegliere il pulsante OK.

4. Immettere ogni riga esattamente come indicato nella tabella riportata di seguito.

    |Nr. colonna|Testata colonna|Tipo colonna|Tipo movimento contabile|Tipo importo|Mostra|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Importo|Saldo periodo|Movimenti|Importo netto|Sempre|  
    |C20|Importo fino alla data|Saldo alla data|Movimenti|Importo netto|Sempre|  
    |C30|Anno fiscale intero|Anno fiscale intero|Movimenti|Importo netto|Sempre|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Assegnazione del layout colonna al nome situaz. contabile.

Ken è ora pronto per assegnare il layout colonna al nome della situazione contabile.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Per assegnare il layout colonna al nome situaz. contabile.  

1. Nella pagina **Situazione contabile** in cui si utilizza la situazione contabile **Previsione**, scegliere l'azione **Modifica setup layout colonna**.  
2. Nel campo **Nome layout colonna** selezionare il layout colonna **Flusso di cassa** da assegnare come layout colonna di default.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Per visualizzare e stampare la previsione del flusso di cassa

1. Nella pagina **Descr. situazioni contabili**, scegliere l'azione **Sintesi** per visualizzare la previsione del flusso di cassa.  
2. Nella pagina **Sintesi situaz. contabile** è possibile selezionare un importo e quindi visualizzare i movimenti di previsione del flusso di cassa che compongono l'importo. Inoltre, è possibile visualizzare la formula utilizzata per calcolare l'importo. È anche possibile filtrare gli importi per data e dimensioni.  
3. Scegliere l'azione **Stampa** per stampare la previsione del flusso di cassa.  

## <a name="see-also"></a>Vedere anche

[Utilizzare le situazioni contabili](bi-how-work-account-schedule.md)  
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]