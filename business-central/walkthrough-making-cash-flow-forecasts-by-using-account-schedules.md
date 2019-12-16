---
title: 'Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando le situazioni contabili | Documenti Microsoft'
description: In questa procedura dettagliata viene descritto come utilizzare le situazioni contabili per effettuare previsioni del flusso di cassa. Le situazioni contabili consentono di effettuare i calcoli che non possono essere eseguiti direttamente nel piano dei conti di cassa. Nelle situazioni contabili è possibile impostare i subtotali relativi agli incassi e alle uscite di cassa. I subtotali possono essere inclusi nei nuovi totali che potranno essere utilizzati per effettuare le previsioni del flusso di cassa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 13086d536bb1c2ea3b67c3e11d1327b045a2e744
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876921"
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

- Aver installato [!INCLUDE[d365fin](includes/d365fin_md.md)].  
- Registrazione delle righe del prospetto del flusso di cassa.  

## <a name="roles"></a>Ruoli  
Questa procedura dettagliata comprende task svolti dal ruolo utente seguente:  

- Controller  

## <a name="story"></a>Scenario  
Ken è un manager presso CRONUS che effettua previsioni del flusso di cassa mensili. Egli include interessi, vendite, acquisti e cespiti nella previsione che presenta alla DF Sara per un'opinione in merito.  

## <a name="setting-up-a-new-account-schedule-name"></a>Impostazione di un nuovo nome della situazione contabile  
Una situazione contabile è costituita da un nome della situazione contabile del conto di cassa con una serie di righe e da un layout colonna.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Per impostare un nuovo nome situazione contabile  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Situazioni contabili** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Descr. situazioni contabili** scegliere l'azione **Nuovo** per creare un nuovo nome della situazione contabile del conto di cassa.  
3.  Nel campo **Nome** immettere **Previsione**.  
4.  Nel campo **Descrizione** immettere **Previsione flusso di cassa**.  
5.  Lasciare vuoti i campi **Default layout colonna** e **Nome visual. analisi**.  

## <a name="setting-up-account-schedule-lines"></a>Impostazione delle righe della situazione contabile  
Dopo aver impostato un nome della situazione contabile, Ken definisce tutte le righe che verranno visualizzate nella situazione contabile del conto di cassa. Egli definisce le righe che possono essere visualizzate nei report, nonché le righe utilizzate solo per scopi di calcolo.  

### <a name="to-set-up-account-schedule-lines"></a>Per impostare le righe della situazione contabile  

1.  Nella pagina **Descr. situazioni contabili** selezionare il nuovo nome della situazione contabile **Previsione** creato e quindi scegliere l'azione **Modifica situazione contabile**.  
2.  Nella pagina **Situazione contabile** immettere ogni riga esattamente come indicato nella tabella riportata di seguito.  

    > [!NOTE]  
    >  Utilizzando la funzione **Inserisci conti di costo e nolo**, è possibile contrassegnare rapidamente i conti di cassa del relativo piano e copiarli nelle righe della situazione contabile.  

    |Nr. riga|Descrizione|Tipo totale|Totale|Tipo di riga|Tipo importo|Mostra|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |C10|Importo|Saldo periodo|Movimenti|Importo netto|Sempre|  
    |C20|Importo fino alla data|Saldo alla data|Movimenti|Importo netto|Sempre|  
    |C30|Anno fiscale intero|Anno fiscale intero|Movimenti|Importo netto|Sempre|  

4.  Scegliere il pulsante **OK**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Assegnazione del layout colonna al nome situaz. contabile.  
Ken è ora pronto per assegnare il layout colonna al nome della situazione contabile.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Per assegnare il layout colonna al nome situaz. contabile.  

1.  Nella pagina **Descr. situazioni contabili** selezionare **Previsione** nel campo **Nome**.  
2.  Nel campo **Default layout colonna** selezionare il layout colonna **Flusso di cassa** da assegnare come layout colonna predefinito.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Per visualizzare e stampare la previsione del flusso di cassa  
1.  Nella pagina **Descr. situazioni contabili**, scegliere l'azione **Sintesi** per visualizzare la previsione del flusso di cassa.  
2.  Nella pagina **Sintesi situaz. contabile** è possibile selezionare un importo e quindi visualizzare i movimenti di previsione del flusso di cassa che compongono l'importo. Inoltre, è possibile visualizzare la formula utilizzata per calcolare l'importo. È anche possibile filtrare gli importi per data e dimensioni.  
3.  Scegliere l'azione **Stampa** per stampare la previsione del flusso di cassa.  

## <a name="see-also"></a>Vedi anche  
 [Utilizzare le situazioni contabili](bi-how-work-account-schedule.md)   
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
