---
title: Utilizzare le situazioni contabili| Documenti Microsoft
description: Descrive come utilizzare le situazioni contabili per creare le visualizzazioni e i report per analizzare i dati finanziari.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7b28d3ec6f4a52c5229d2e121ff1fe8ed847eeb7
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-account-schedules"></a>Utilizzare le situazioni contabili
Utilizzare le situazioni contabili per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. Le situazioni contabili analizzano le cifre nei conti di contabilità generale e confrontano i movimenti di contabilità generale con i movimenti budget di contabilità generale. I risultati vengono visualizzati in grafici nella Gestione ruolo utente, ad esempio il grafico Flusso di cassa.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce alcune situazioni contabili di esempio che è possibile utilizzare immediatamente oppure è possibile impostare le proprie righe e colonne per specificare le cifre da confrontare. È ad esempio possibile creare piani dei conti per calcolare i margini di profitto in dimensioni quali reparti o gruppi di clienti. È possibile creare quanti rendiconti finanziari personalizzati si desidera.  

L'impostazione delle situazioni contabili richiede una comprensione dei dati finanziari nel piano dei conti. Per esempio, è possibile visualizzare i movimenti C/G come percentuali di movimenti budget. Tale operazione richiede che i budget siano creati. Per ulteriori informazioni, vedere [Creare budget C/G](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Categorie di conti e situazioni contabili
Le categorie di conto consentono di modificare il layout dei rendiconti finanziari. Dopo aver impostato le categorie di conto nella finestra **Categorie conto C/G** scegliere l'azione **Genera situazioni contabili**, le situazioni contabili sottostanti i report finanziari principali verranno aggiornate. Alla successiva esecuzione di uno dei report, ad esempio l'estratto conto, nuovi totali e voci secondarie vengono aggiunte, in base alle modifiche. Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Per creare nuove situazioni contabili  
 Utilizzare situazioni contabili per analizzare le cifre nei conti di contabilità generale o confrontare i movimenti di contabilità generale con i movimenti budget di contabilità generale. Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Descr. situazioni contabili** scegliere l'azione **Nuovo** per creare una nuova descrizione situazione contabile.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere l'azione **Modifica situazione contabile**.
5. Compilare i campi necessari nella finestra **Situazione contabile**.  

    Dopo aver creato una nuova situazione contabile e averne impostato le righe, è necessario impostare le colonne. Le colonne possono essere impostate manualmente oppure assegnando un layout di colonne di default alla situazione contabile.
6. Scegliere l'azione **Modifica setup layout colonna**.
7. Compilare i campi necessari nella finestra **Layout colonna**.

> [!NOTE]  
>   Se non è stato assegnato un default layout colonna alla situazione contabile, è necessario impostare le colonne manualmente.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Per creare una colonna per il calcolo delle percentuali  
A volte, potrebbe essere necessario includere in una situazione contabile una colonna per il calcolo delle percentuali di un totale. Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, è possibile inserire una colonna per indicare la percentuale delle vendite totale rappresentata da ogni riga.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.
2. Nella finestra **Descr. situazioni contabili** selezionare una situazione contabile.  
3. Selezionare l'azione **Modifica situazione contabile** per impostare una riga della situazione contabile per calcolare il totale su cui saranno basate le percentuali.  
4. Inserire una riga immediatamente sopra la prima riga per la quale si desidera visualizzare una percentuale.  
5. Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**. Nel campo **Totale** immettere una formula del totale su cui sarà basata la percentuale. Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.  
6. Scegliere l'azione **Modifica setup layout colonna** per impostare una colonna.  
7. Compilare i campi della riga nel modo seguente: nel campo **Tipo colonna** selezionare **Formula**. Nel campo **Formula** immettere una formula per l'importo per il quale si desidera calcolare la percentuale, seguita dalla percentuale (%). Ad esempio, se il numero di colonna N contiene il saldo periodo, immettere **N%**.  
8. Ripetere i passaggi da 4 a 7 per ogni gruppo di righe che di desidera suddividere per percentuale.

## <a name="to-set-up-account-schedules-with-overviews"></a>Per impostare situazioni contabili con sintesi  
È possibile utilizzare una situazione contabile per creare un rendiconto in cui vengono confrontate le cifre C/G con le cifre del budget C/G.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.
2. Nella finestra **Descr. situazioni contabili** selezionare una situazione contabile.  
3. Scegliere l'azione **Modifica situazione contabile**  
4. Nella finestra **Situazione contabile** selezionare il nome della situazione contabile di default nel campo **Nome**.
5. Scegliere l'azione **Inserisci conti**.  
6. Selezionare i conti che si intendono includere nella dichiarazione e selezionare il pulsante **OK**.

    I conti sono stati inseriti nella situazione contabile. È inoltre possibile modificare il layout colonna.  
7. Scegliere l'azione **Sintesi**.  
8. Fare clic sulla Scheda dettaglio **Filtri dimensione** e impostare il filtro budget con il nome di filtro desiderato.  
9. Scegliere il pulsante **OK**.  

Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.

## <a name="see-also"></a>Vedi anche
[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

