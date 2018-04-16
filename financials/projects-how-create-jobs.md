---
title: Creare una scheda commessa per una commessa e specificare i task| Documenti Microsoft
description: "Per un nuovo progetto, è possibile creare una scheda commessa contenente i task commesse e le righe pianificazione, per semplificare la gestione dell'avanzamento e del budget."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ece0a95f83868ac2657fdf41330e7d0a9cce37d6
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-jobs"></a>Creare commesse
Quando si inizia un nuovo progetto, è necessario creare una scheda commessa con i task commessa e le righe di pianificazione commessa integrati. La scheda è strutturata su due livelli.  

Il primo livello è costituito dai task commessa. Occorre creare almeno un task per commessa perché tutte le operazioni di registrazione fanno riferimento a un task commessa. L'impostazione di almeno un task nella commessa consente di impostare le righe di pianificazione commessa e di registrare il consumo nella commessa.

Il secondo livello è costituito dalle righe di pianificazione commessa, che consentono di specificare l'utilizzo dettagliato delle risorse, degli articoli e di diverse spese di contabilità generale.

La struttura a livelli consente di dividere la commessa in task meno complessi e pertanto di dettagliare maggiormente le fasi di definizione del budget, dell'offerta e della registrazione. Inoltre, consente di ottenere informazioni dettagliate sullo stato di avanzamento di una commessa. Ad esempio, è possibile verificare se si stanno soddisfacendo le attività cardine definite o se si stanno rispettano le previsioni di budget.

> [!NOTE]  
>   L'azione **Nuova commessa** in Gestione ruolo utente **Manager progetto** avvia una finestra di configurazione guidata che aiuta a creare una commessa con task e righe di pianificazione integrati. Di seguito viene descritto come eseguire i passaggi manualmente.

## <a name="to-create-a-job-card"></a>Per creare una scheda commessa
Creare una scheda commessa, quindi creare le righe del task commessa e le relative righe di pianificazione commessa.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per specificare la commessa utilizzando le informazioni di altre commesse, scegliere l'azione **Copia commessa**, compilare i necessari campi, quindi scegliere **OK**.

> [!NOTE]  
>   Se con la commessa si stanno utilizzando i fogli presenze, è necessario designare un responsabile. La persona può approvare i fogli presenze per i task degli impiegati associati alla commessa. Per ulteriori informazioni, vedere [Impostare fogli presenze](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Per creare i task di una commessa
Una parte fondamentale nella creazione di una nuova commessa consiste nello specificare i vari task implicati nella commessa. A tale scopo, è necessario aggiungere nuove righe nella Scheda dettaglio **Task** della finestra **Scheda commessa**, un task per ogni riga. Ogni commessa deve avere almeno un task.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.
2. Aprire la scheda commessa di una commessa interessata.
3. Nella Scheda dettaglio **Task** compilare i campi secondo le necessità su una nuova riga.
4. Per far rientrare i task e creare così una gerarchia, scegliere l'azione **Task**, quindi l'azione **Indentazione task commesse**.
5. Ripetere i passaggi 3 e 4 per i task con cui si desidera completare la commessa.
6. Per specificare i task commesse utilizzando le informazioni di altri task commesse, scegliere l'azione **Copia task commessa da**, compilare i campi necessari, quindi scegliere **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Per creare le righe di pianificazione per una commessa
È possibile perfezionare i nuovi task commessa nelle righe di pianificazione commessa. Una riga di pianificazione può essere utilizzata per acquisire le informazioni di cui si desidera tenere traccia per una commessa. È possibile utilizzare le righe di pianificazione per aggiungere informazioni relative, ad esempio, alle risorse o agli articoli necessari per l'esecuzione della commessa. Se ad esempio si crea un task per ottenere l'approvazione di una commessa da parte del cliente, è possibile associarlo a righe di pianificazione per articoli quali la riunione con il cliente e l'assegnazione di una risorsa.  

Una riga di pianificazione commessa può contenere uno dei seguenti tipi.  

| Tipo | Descrizione |
| --- | --- |
| **Budget** |Fornisce le stime di utilizzo e di costo per la commessa, generalmente in un tipo di progetto Time and Material. Le righe di pianificazione di questo tipo non possono essere fatturate. |
| **Fatturabile** |Fornisce le stime di fatturazione per il cliente, in genere in un progetto a prezzo fisso. |
| **Sia Budget sia fatturabile** |Fornisce un utilizzo a budget pari a ciò che si desidera fatturare. |

**Nota**. Quando si immettono le informazioni nelle righe di pianificazione commessa, i dati sui costi vengono inseriti automaticamente. Ad esempio, il costo, il prezzo e lo sconto per le risorse e gli articoli si basano inizialmente sulle informazioni definite nelle schede risorsa e articolo.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.
2. Aprire una scheda commessa di interesse.
3. Selezionare un task commessa per il quale il campo **Tipo task commessa** contiene **Registrazione**, quindi scegliere l'azione **Righe pianificazione commessa**.  
4. Nella finestra **Righe pianificazione commessa**, in una nuova riga compilare i campi secondo le esigenze.
5. Ripetere i passaggi 3 e 4 per tutte le righe di pianificazione richieste per il task commessa.

## <a name="see-also"></a>Vedi anche
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

