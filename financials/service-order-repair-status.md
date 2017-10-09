---
title: Impostare gli stati per gli ordini di assistenza e le riparazioni | Documenti Microsoft
description: "È necessario impostare nove opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a>Procedura: Impostare gli stati per gli ordini di assistenza e le riparazioni
È necessario impostare opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza. È necessario impostare almeno nove opzioni di stato di riparazione che indichino le situazioni o le azioni intraprese durante le operazioni di assistenza effettuate sull'articolo.  

È possibile impostare il livello di priorità per le opzioni relative allo stato dell'ordine di assistenza. Esistono quattro livelli di priorità: Alta, Medio Alta, Medio Bassa, Bassa.  
  
Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine di assistenza, lo stato dell'ordine di assistenza viene aggiornato. Lo stato di riparazione di ogni articolo in assistenza è collegato allo stato dell'ordine di assistenza. Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine di assistenza, viene selezionato lo stato dell'ordine con la priorità più alta.  

## <a name="to-set-up-a-repair-status"></a>Per impostare uno stato di riparazione  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Stato riparazione**, quindi scegliere il collegamento correlato. 2. Creare un nuovo stato di riparazione.  
3. Compilare i campi **Codice** e **Descrizione**.  
4. Nel campo **Stato ordine assistenza** selezionare lo stato dell'ordine a cui collegare lo stato della riparazione. Nel campo **Priorità** viene visualizzata la priorità corrispondente allo stato dell'ordine di assistenza scelto.  
5. Scegliere lo stato di riparazione. È possibile sceglierne uno solo.  
6. Per poter registrare ordini di assistenza, inclusi articoli in assistenza, con questo stato di riparazione, scegliere il campo **Registrazione permessa**.  
7. Per modificare manualmente l'opzione di stato dell'ordine di assistenza in **Non iniziato** negli ordini che contengono articoli in assistenza con questo stato di riparazione, selezionare la casella di controllo **Stato Non iniziato abilitato**.  
8. Analogamente, selezionare le caselle di controllo **Stato In Corso abilitato**, **Stato Completato abilitato** e **Stato In attesa abilitato**.
  
## <a name="to-set-up-service-status-priorities"></a>Per impostare le priorità di stato di assistenza  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Stato ordine assistenza**, quindi scegliere il collegamento correlato.  
2. Selezionare lo stato dell'ordine di assistenza per cui si desidera impostare una priorità.  
3. Nel campo **Priorità** scegliere la priorità che si desidera assegnare a questo stato dell'ordine di assistenza. Ripetere questo passaggio per ogni stato.  
  
## <a name="see-also"></a>Vedi anche  
[Informazioni su stato ordine assistenza e stato riparazione]()  
[Impostazione della gestione assistenza](service-setup-service.md)  

