---
title: 'Procedura: Spostare componenti in un''area di operazione nelle configurazioni della warehouse di base | Documenti Microsoft'
description: Se le operazioni di elaborazione dell'articolo si verificano nell'ubicazione della warehouse, potrebbe essere necessario spostare gli articoli tra le collocazioni interne in modo che corrispondano ai documenti di origine interni, ad esempio produzione, assemblaggio o ordini di assistenza per l'ubicazione.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5e271b160d8a4969be296861f6746163fcfea6ba
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base
Se le operazioni di elaborazione dell'articolo si verificano nell'ubicazione della warehouse, potrebbe essere necessario spostare gli articoli tra le collocazioni interne in modo che corrispondano ai documenti di origine interni, ad esempio produzione, assemblaggio o ordini di assistenza per l'ubicazione.  

> [!NOTE]  
>  Per informazioni sullo spostamento di articoli tra collocazioni senza documenti di origine, vedere Movimentazione interna.  

Nelle configurazioni warehouse avanzate, ovvero ubicazioni che utilizzano il campo di setup **Stoccaggi e prelievi guidati**, è possibile utilizzare la finestra **Prospetto movimentazioni** per spostare gli articoli tra le collocazioni. Per ulteriori informazioni, vedere [Spostare articoli nelle configurazioni della warehouse di base](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Nelle configurazioni di warehouse di base, ovvero ubicazioni che utilizzano il campo di setup **Collocazione obbligatoria** e il campo di setup **Richiesto prelievo**, è possibile registrare le movimentazioni di articoli nelle aree delle operazioni interne in base ai documenti di origine interni nei seguenti modi:  

-   Tramite la finestra **Movimento di magazzino**.  
-   Con la finestra **Prelievi magazzino**.  

> [!NOTE]  
>  I prelievi magazzino registrano inoltre i movimenti contabili articoli negativi come consumo e sono supportati solo per i componenti di produzione. Per ulteriori informazioni, vedere la finestra Prelievo magazzino.  

Per informazioni dettagliate sui movimenti di magazzino, vedere la finestra Movimento di magazzino.  

Due diversi ruoli possono creare il movimento di magazzino iniziale. Un addetto all'assemblaggio, ad esempio, può crearlo da un ordine di assemblaggio rilasciato in modo che venga visualizzato nell'elenco dell'addetto warehouse relativo al lavoro da svolgere. Per creare un movimento di magazzino per le righe ordini di assemblaggio i cui componenti sono pronti per essere spostati nelle relative collocazioni specificate, l'addetto all'assemblaggio utilizza la funzione **Crea movimento di magazzino**.  

In alternativa, un lavoratore warehouse può crearlo scegliendo l'ordine di assemblaggio rilasciato in questione. Questa funzionalità è descritta nella procedura seguente.  

> [!NOTE]  
>  Se la movimentazione riguarda un ordine di assemblaggio in cui l'articolo è assemblato in base a un ordine di vendita, è possibile definire che il documento di movimento di magazzino viene creato automaticamente quando si crea il documento di prelievo magazzino che accetta l'articolo di assemblaggio completato e registra la spedizione. Per impostare questa operazione, selezionare il campo **Crea movimenti automaticamente** nella finestra **Setup assemblaggio**.  
>   
>  Per ulteriori informazioni sugli ordini di assemblaggio e nelle configurazioni di base della warehouse, vedere la sezione "Gestione di articoli da assemblare su ordine con prelievi magazzino" in [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md).  

La procedura seguente mostra come creare un movimento di magazzino nella finestra **Movimento di magazzino** facendo riferimento a un ordine di assemblaggio rilasciato come documento di origine. La procedura è la stessa quando si spostano componenti per gli ordini di produzione e gli ordini di assistenza.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Per spostare componenti in un'area di operazione nelle configurazioni di warehouse di base  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Movimento di magazzino**, quindi scegliere il collegamento pertinente.  
2.  Nella Scheda dettaglio **Generale** compilare il campo **Nr.** . È possibile premere INVIO per selezionare la numerazione.  
3.  Nel campo **Cod. ubicazione** immettere l'ubicazione in cui si verifica la movimentazione.  
4.  Scegliere l'azione **Prendi documenti origine**. In alternativa, compilare il campo **Documento origine**, quindi fare clic sul pulsante **AssistEdit** nel campo **Nr. origine**.  
5.  Nella finestra **Documenti origine** selezionare l'ordine di assemblaggio per cui si desidera spostare i componenti, quindi fare clic sul pulsante **OK**.  

    Per ogni componente necessario che può essere spostato, viene generata una riga Prendere e una riga Mettere nella finestra **Movimenti di magazzino**. Tutti i campi tranne il campo **Qtà da gestire** sono precompilati in base alle righe del documento di origine. Il campo **Qtà da gestire** è uguale a zero fino a quando non si immette la quantità effettivamente spostata.  

    È possibile modificare il codice collocazione in una riga Prendere, ma solo in base alla disponibilità. Scegliendo il pulsante **AssistEdit** nel campo **Cod. collocazione** in una riga Prendere, la finestra **Contenuto collocazioni** viene aperta e mostra solo le collocazioni in cui il componente è disponibile.  

    Non è possibile modificare il codice collocazione in una riga Mettere. Solo il codice collocazione definito nella riga componente del documento di origine viene accettato. Ciò supporta il principio secondo cui il ruolo che richiede un componente, ovvero un addetto all'assemblaggio in questa procedura, sa dove deve essere inserito il componente. Se si desidera inserire i componenti in una collocazione diversa, è necessario innanzitutto modificare il codice collocazione specificato nella riga componenti, quindi ricreare le righe movimenti di magazzino.  
6.  Nel campo **Qtà da gestire** immettere la quantità parziale o completa effettivamente spostata. Il valore nelle righe Prendere e Mettere deve essere identico. In caso contrario, non è possibile registrare la movimentazione.  

    > [!NOTE]  
    >  Come in altre attività di warehouse, è possibile suddividere la riga Posizione selezionando l'azione **Azioni** e scegliendo l'azione **Dividi riga**. In questo caso, la somma delle due righe divise Mettere deve essere uguale alla quantità nella riga Prendere.  

7.  Al momento di registrare le movimentazioni effettuate, scegliere l'azione **Registra movimentazioni inv.**.  

    I movimenti warehouse vengono creati in modo da riflettere la presenza dei componenti nelle collocazioni specificate nelle righe ordine di assemblaggio.  

    > [!NOTE]  
    >  A differenza di quando si spostano componenti con un prelievo magazzino, il consumo non viene registrato quando si registra un movimento di magazzino. Tale passaggio deve essere eseguito separatamente registrando l'output e il consumo dell'ordine di assemblaggio. Per ulteriori informazioni, vedere Ordine di assemblaggio.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

