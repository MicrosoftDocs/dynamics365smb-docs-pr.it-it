---
title: 'Procedura: Creare stoccaggi mediante stoccaggi interni | Documenti Microsoft'
description: Dopo avere stoccato gli articoli e prima di prelevarli per soddisfare le richieste di un ordine di produzione o di una spedizione, gli articoli vengono inclusi tra le giacenze disponibili all'interno della warehouse.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6829c5a67f1121ecc135e1183af78b0e602f8f
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-and-put-away-without-a-source-document"></a>Procedura: Selezionare e stoccare senza un documento di origine
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
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Prelievo interno whse.**, quindi scegliere il collegamento correlato.  
2.  Compilare il campo **Nr.** e il campo **A codice collocazione** nella Scheda dettaglio **Generale**. Il campo **A codice collocazione** indica la collocazione da cui devono essere prelevati gli articoli. Ai fini della produzione, questa collocazione rappresenta la collocazione di produzione in entrata o la collocazione del reparto produttivo aperto. Viceversa, per altri scopi scegliere il campo A codice collocazione immettendo il codice per un tipo di collocazione che non viene utilizzata per il prelievo, in genere una collocazione di stazionamento, una collocazione di spedizione o un collocazione ad uso speciale.  
3.  Selezionare un articolo nel campo **Nr. articolo**, quindi immettere le quantità che si desidera prelevare.  
4. Scegliere l'azione **Crea prelievo**. Verrà creata un'istruzione di prelievo indirizzata agli impiegati warehouse.  

## <a name="to-create-an-internal-put-away"></a>Per creare uno stoccaggio interno  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Prelievo interno whse.**, quindi scegliere il collegamento correlato.  
2.  Compilare il campo **Nr.** e il campo **Dal codice collocazione** nella Scheda dettaglio **Generale**. Il campo **Dal codice collocazione** indica la collocazione in cui vengono posizionati gli articoli restituiti alla warehouse, ad esempio dalla produzione.  
3.  Immettere i numeri di articolo e le quantità nelle righe appropriate.  
4.  Selezionare l'azione **Crea stoccaggio**. Verrà creata un'istruzione di stoccaggio indirizzata agli impiegati warehouse.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

