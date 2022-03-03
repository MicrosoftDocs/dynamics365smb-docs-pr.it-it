---
title: Creare stoccaggi mediante stoccaggi interni
description: Questo argomento illustra come prelevare e stoccare senza un documento di origine, come creare un prelievo interno e come creare uno stoccaggio interno.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 609564faa1e0d5b1e7c364360315ca71b9ba3d06
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140087"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Selezionare e stoccare senza un documento di origine
Dopo avere stoccato gli articoli e prima di prelevarli per soddisfare le richieste di un ordine di produzione o di una spedizione, gli articoli vengono inclusi tra le giacenze disponibili all'interno della warehouse.  

È possibile che, in circostanze particolari, gli articoli debbano essere prelevati temporaneamente dalle collocazioni di prelievo della warehouse per essere utilizzati, ad esempio, come modelli in contesti di vendita dimostrativi. Tali articoli sono ancora di proprietà della società e fanno ancora parte delle giacenze a magazzino, ma non sono disponibili per il prelievo. Gli articoli vengono registrati in una collocazione ad uso speciale creata a tale scopo e, benché tecnicamente siano ancora registrati nella warehouse, fisicamente possano trovarsi in una sala riunioni o in un salone di esposizione.  

In altre circostanze, è possibile che l'unità di produzione abbia bisogno di alcuni componenti non previsti per un processo. In tal caso, è possibile prelevare articoli per le collocazioni di produzione utilizzando la funzione di prelievo interno. Al termine del processo e una volta realizzato l'output di produzione, è necessario registrare il consumo degli articoli e svuotare la collocazione di produzione, il che comporta, a sua volta, una diminuzione della quantità dell'articolo nell'ubicazione.  

Analogamente, gli articoli possono essere restituiti alla warehouse per lo stoccaggio. È ad esempio possibile che determinati articoli siano stati prelevati dalle giacenze disponibili per un ordine di produzione e che non siano stati utilizzati. Per reintegrarli nuovamente nelle giacenze disponibili, è necessario stoccarli nella collocazione.  

**Stoccaggi interni** consente di eseguire stoccaggi senza dover fare riferimento a uno specifico documento di origine. È possibile impostare facilmente tutte le informazioni necessarie per la creazione di un'istruzione di warehouse di stoccaggio.  

> [!NOTE]  
>  Se non si utilizzano i prelievi interni e gli stoccaggi interni, è possibile apportare queste rettifiche tramite lo spostamento degli articoli da una collocazione a un'altra o la registrazione delle rettifiche della quantità in una collocazione.  
>   
>  Quando per una determinata ubicazione sono previsti stoccaggi e prelievi guidati, e si utilizzano pertanto i tipi di collocazione, non è possibile spostare manualmente gli articoli all'interno o all'esterno di una collocazione di tipo Ricevi poiché gli articoli presenti in questo tipo di collocazione devono essere registrati come stoccati prima di essere inseriti nella giacenza disponibile.  

## <a name="to-create-an-internal-pick"></a>Per creare un prelievo interno  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievo int. whse.**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare il campo **Nr.** , il campo **Codice ubicazione** e il campo **A codice collocazione** nella Scheda dettaglio **Generale**. Il campo **A codice collocazione** indica la collocazione in cui si desidera inserire gli articoli prelevati. Ai fini della produzione, questa collocazione rappresenta la collocazione di produzione in entrata o la collocazione del reparto produttivo aperto. Viceversa, per altri scopi scegliere un codice collocazione per un tipo di collocazione che non viene utilizzata per il prelievo, in genere una collocazione di stazionamento, una collocazione di spedizione o un collocazione ad uso speciale.  
4.  Selezionare un articolo nel campo **Nr. articolo**, quindi immettere le quantità che si desidera prelevare.  
5. Scegliere l'azione **Crea prelievo**. Verrà creata un'istruzione di prelievo indirizzata agli impiegati warehouse. In alternativa, è possibile scegliere l'azione **Rilascia** e creare prelievi warehouse utilizzando il **Prospetto prelievi**. Per ulteriori informazioni, vedere [Pianificare i prelievi nei prospetti](warehouse-how-to-plan-picks-in-worksheets.md).

## <a name="to-create-an-internal-put-away"></a>Per creare uno stoccaggio interno  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggio int. whse.**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Nella testata di un nuovo stoccaggio interno compilare almeno **Nr.** e **Cod. ubicazione**.
4. Compilare una riga per ciascun articolo che si desidera trasferire nella warehouse. È sufficiente compilare i campi **Nr. articolo** e **Quantità**.

  > [!NOTE]  
  > Quando si sceglie il campo **Nr. articolo**, viene visualizzata la finestra **Lista contenuto collocazione** anziché la finestra **Elenco articoli**. Questo si verifica perché si sta eseguendo lo stoccaggio di un articolo contenuto in una particolare collocazione, ovvero un *contenuto collocazione* e non semplicemente un articolo, e si conosce già la collocazione da cui l'articolo deve essere prelevato.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Per immettere nelle righe l'intero contenuto della collocazione o il contenuto di collocazioni specifiche nell'ubicazione, scegliere l'azione **Ottieni contenuto collocazione**.  
6. Selezionare l'azione **Crea stoccaggio**. Verrà creata un'istruzione di stoccaggio indirizzata agli impiegati warehouse. In alternativa, è possibile scegliere l'azione **Rilascia** e creare stoccaggi warehouse utilizzando il **Prospetto stoccaggi**. Per ulteriori informazioni, vedere [Pianificare stoccaggi nei prospetti](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Vedere anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
