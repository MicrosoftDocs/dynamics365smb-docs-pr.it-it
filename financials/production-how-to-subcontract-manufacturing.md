---
title: "Come gestire le attività di conto lavoro | Microsoft Docs"
description: "Dopo avere creato l'ordine di acquisto nel prospetto conto lavoro, è possibile registrarlo."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2796da1b41569c8c950dc844fc31eaf4f0179efa
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="subcontract-manufacturing"></a>Gestire le attività di conto lavoro
L'utilizzo di un conto lavoro per le operazioni eseguite da un fornitore è prassi comune in numerose aziende manifatturiere. Il conto lavoro può verificarsi raramente oppure essere parte integrante di tutti i processi di produzione.

Nel programma sono disponibili diversi strumenti per la gestione delle attività di conto lavoro:  

- Aree di produzione con fornitore assegnato: questa funzionalità consente di impostare un'area di produzione associata a un fornitore (terzista). Questa è detta un'area di produzione conto lavoro. È possibile specificare un'area di produzione conto lavoro in un'operazione del ciclo, il che consente di elaborare facilmente l'attività in conto lavoro. Inoltre, il costo dell'operazione può essere designato a livello di ciclo o di area di produzione.  
- Costo area di produzione basato su unità o tempo: questa funzionalità consente di specificare se i costi associati all'area di produzione sono basati sul tempo di produzione o su un addebito fisso per unità. Benché i terzisti utilizzino in genere una spesa fissa per unità da addebitare per i propri servizi, il programma è in grado di gestire entrambe le opzioni (tempo di produzione e addebito fisso per unità).  
- Prospetto conto lavoro: questa funzionalità consente di trovare gli ordini di produzione con il materiale pronto da inviare a un terzista e di creare automaticamente ordini di acquisto per le operazioni di conto lavoro dai cicli degli ordini di produzione. Gli addebiti dell'ordine di acquisto vengono quindi automaticamente registrati nell'ordine di produzione durante la registrazione dell'ordine di acquisto. È possibile accedere e utilizzare da un prospetto conto lavoro solo gli ordini di produzione con stato rilasciato.  

## <a name="subcontract-work-centers"></a>Area di produzione conto lavoro  
Le aree di produzione conto lavoro vengono impostate allo stesso modo delle aree di produzione normali, ma con ulteriori informazioni. Tali aree vengono assegnate ai cicli analogamente alle altre aree di produzione.  

### <a name="subcontract-work-center-fields"></a>Campi Area di produzione conto lavoro  
Il campo **Nr. terzista** designa l'area di produzione come area di produzione conto lavoro. È possibile immettere il numero di un terzista che approvvigiona l'area di produzione. Questo campo può essere utilizzato per amministrare le aree di produzione non interne ma che eseguono l'elaborazione sotto contratto.  

Se il conto lavoro con il fornitore prevede un costo diverso per ogni processo, è possibile selezionare il campo **Costo unitario specifico**. In questo modo, è possibile impostare un costo in ogni riga del ciclo ed evitare di dover reimmettere ogni ordine di acquisto. Il costo nella riga del ciclo viene utilizzato per l'elaborazione al posto del costo indicato nei campi relativi al costo delle aree di produzione. Selezionare il campo **Costo unitario specifico** per calcolare i costi per il fornitore in base all'operazione del ciclo.  

Se il conto lavoro prevede un unico costo per fornitore, lasciare vuoto il campo **Costo unitario specifico**. I costi verranno impostati compilando i campi **Costo unitario diretto**, **% costi indiretti** e **Coeff. costi generali**.  

### <a name="routings-that-use-subcontract-work-centers"></a>Cicli che utilizzano aree di produzione conto lavoro  
Le aree di produzione conto lavoro possono essere utilizzate per operazioni nei cicli allo stesso modo delle aree di produzione normali.  

È possibile impostare un ciclo in cui venga utilizzata un'area di produzione esterna come passaggio operativo standard. In alternativa, è possibile modificare il ciclo per un determinato ordine di produzione in modo da includere un'operazione esterna. Questo metodo può risultare necessario in una situazione di emergenza, ad esempio in caso di malfunzionamento di un server, oppure durante un periodo temporaneo di maggiore domanda, in cui il lavoro normalmente eseguito internamente deve essere inviato a un terzista.  

Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).  

## <a name="subcontracting-worksheet"></a>Prospetto conto lavoro  
Dopo avere calcolato il prospetto conto lavoro, viene creato il documento pertinente, in questo caso un ordine di acquisto.  

# <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Calcolare i prospetti conto lavoro e creare gli ordini di acquisto conto lavoro
La finestra **Prospetto conto lavoro** funziona come il **Prospetto pianific.** nel calcolo dell'approvvigionamento necessario, in questo caso degli ordini di acquisto, che si esaminano nel prospetto e quindi si creano mediante la funzione **Esegui messaggi di azione**.  

> [!NOTE]  
>  È possibile accedere e utilizzare da un prospetto conto lavoro solo gli ordini di produzione con stato **Rilasciato**.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Per calcolare il prospetto conto lavoro  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Prospetto conto lavoro**, quindi scegliere il collegamento correlato.  
2.  Per calcolare il prospetto, scegliere l'azione **Calcolo conto lavoro**.  
3.  Nella finestra **Calcolo conto lavoro** impostare i filtri per le operazioni in conto lavoro o le aree di produzione in cui vengono effettuate, per calcolare soltanto gli ordini di produzione desiderati.  
4.  Scegliere il pulsante **OK**.  

    Esaminare le righe nella finestra **Prospetto conto lavoro**. Le informazioni presenti in questo prospetto provengono dall'ordine di produzione e dalle righe del ciclo dell'ordine di produzione e vengono trasmesse all'ordine di acquisto quando questo viene creato. Analogamente agli altri prospetti, è possibile eliminare una riga dal prospetto senza influire sulle informazioni generali. Le informazioni verranno visualizzate di nuovo alla successiva esecuzione della funzione **Calcolo conto lavoro**.  

### <a name="to-create-the-subcontract-purchase-order"></a>Per creare l'ordine di acquisto conto lavoro  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Prospetto conto lavoro**, quindi scegliere il collegamento correlato.  
2.  Nel gruppo **Processo** della scheda **Azioni** scegliere **Esegui messaggi di azione**.  
3.  Selezionare il campo **Stampa ordini** per stampare l'ordine di acquisto mentre viene creato.  
4.  Scegliere il pulsante **OK**.  

Se tutte le operazioni di conto lavoro devono essere inviate alla stessa ubicazione fornitore, allora verrà creato un unico ordine di acquisto.  

Le righe del prospetto trasformate in ordine di acquisto vengono eliminate dal prospetto. Una volta creato un ordine di acquisto, non verrà nuovamente visualizzato nel prospetto.  

## <a name="posting-subcontract-purchase-orders"></a>Registrazione di ordini di acquisto conto lavoro  
Dopo avere creato gli ordini di acquisto conto lavoro, è possibile registrarli. La ricezione dell'ordine comporta la pubblicazione di un movimento contabile capacità nell'ordine di produzione, mentre la fatturazione dell'ordine comporta la registrazione del costo diretto dell'ordine di acquisto nell'ordine di produzione.  

Quando l'acquisto viene registrato come ricevuto, viene automaticamente registrato un movimento delle registrazioni di output per l'ordine di produzione. Questa opzione è valida solo se l'operazione di conto lavoro è l'ultima del ciclo ordine di produzione.  

> [!CAUTION]  
>  È possibile che non si desideri registrare automaticamente l'output per un ordine di produzione in corso quando vengono ricevuti gli articoli in conto lavoro. I motivi potrebbero essere che la quantità di output prevista che è stata registrata potrebbe essere diversa dalla quantità effettiva e che la data di registrazione dell'output automatico è fuorviante.  
>   
>  Per evitare che l'output previsto di un ordine di produzione venga registrato quando vengono ricevuti gli acquisti di conto lavoro, verificare che l'operazione in conto lavoro non sia l'ultima. In alternativa, inserire una nuova ultima operazione per la quantità di output finale.

## <a name="to-post-a-subcontract-purchase-order"></a>Per registrare un ordine di acquisto conto lavoro  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini acquisto**, quindi selezionare il collegamento correlato.  
2.  Aprire un ordine di acquisto creato dal prospetto conto lavoro.  

    Nelle righe ordine di acquisto è possibile visualizzare le stesse informazioni presenti nel prospetto. I campi **Nr. ordine produzione**, **Nr. riga ordine prod.**, **Nr. operazione** e **Nr. area produzione** vengono compilati con le informazioni dall'ordine di produzione di origine.  

3.  Scegliere l'azione **Registra**.  

Quando l'acquisto viene registrato come ricevuto, viene automaticamente registrato un movimento delle registrazioni di output per l'ordine di produzione. Questa opzione è valida solo se l'operazione di conto lavoro è l'ultima del ciclo ordine di produzione.  

> [!CAUTION]  
>  È possibile che non si desideri registrare automaticamente l'output per un ordine di produzione in corso quando vengono ricevuti gli articoli in conto lavoro. I motivi potrebbero essere che la quantità di output prevista che è stata registrata potrebbe essere diversa dalla quantità effettiva e che la data di registrazione dell'output automatico è fuorviante.  
>   
>  Per evitare che l'output previsto di un ordine di produzione venga registrato quando vengono ricevuti gli acquisti di conto lavoro, verificare che l'operazione in conto lavoro non sia l'ultima. In alternativa, inserire una nuova ultima operazione per la quantità di output finale.  

Quando l'ordine di acquisto viene registrato come fatturato, il costo diretto dell'ordine di acquisto viene registrato nell'ordine di produzione.  

## <a name="see-also"></a>Vedi anche  
[Manufacturing](production-manage-manufacturing.md)    
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)      
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

