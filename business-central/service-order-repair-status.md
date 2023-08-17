---
title: Impostare gli stati per gli ordini di assistenza e le riparazioni | Documenti Microsoft
description: È necessario impostare nove opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Come impostare gli stati per gli ordini di assistenza e le riparazioni

È necessario impostare opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza. È necessario impostare almeno nove opzioni di stato di riparazione che indichino le situazioni o le azioni intraprese durante le operazioni di assistenza effettuate sull'articolo.  

È possibile impostare il livello di priorità per le opzioni relative allo stato dell'ordine di assistenza. Le quattro priorità sono **Alta**, **Medio Alta**, **Medio Bassa** e **Bassa**.  

Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine di assistenza, lo stato dell'ordine di assistenza viene aggiornato. Lo stato di riparazione di ogni articolo in assistenza è collegato allo stato dell'ordine di assistenza. Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine di assistenza, viene selezionato lo stato dell'ordine con la priorità più alta.  

Prima di poter impostare uno stato di riparazione, è necessario impostare le priorità dello stato di assistenza.

## <a name="to-set-up-service-status-priorities"></a>Per impostare le priorità di stato di assistenza

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stato ordine assistenza**, quindi scegli il collegamento correlato.  
2. Selezionare lo stato dell'ordine di assistenza per cui si desidera impostare una priorità.  
3. Nel campo **Priorità** scegliere la priorità che si desidera assegnare a questo stato dell'ordine di assistenza.  

Ripetere i passaggi 2 e 3 per impostare la priorità per ciascuna delle quattro opzioni di stato, ovvero **Non iniziato**, **In corso**, **Completato** e **In attesa**.  

## <a name="to-set-up-a-repair-status"></a>Per impostare uno stato di riparazione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stato riparazione**, quindi scegli il collegamento correlato.
2. Creare un nuovo stato di riparazione.  
3. Compilare i campi **Codice** e **Descrizione**.  
4. Nel campo **Stato ordine assistenza** selezionare lo stato dell'ordine a cui collegare lo stato della riparazione. Nel campo **Priorità** viene visualizzata la priorità corrispondente allo stato dell'ordine di assistenza scelto.  
5. Scegliere lo stato di riparazione. È possibile sceglierne uno solo. Lo stato di riparazione non può essere collegato a più di una opzione di stato di riparazione.  
6. Per poter registrare ordini di assistenza, inclusi articoli in assistenza, con questo stato di riparazione, scegliere il campo **Registrazione permessa**.  
7. Per modificare manualmente l'opzione di stato dell'ordine di assistenza in **Non iniziato** negli ordini che contengono articoli in assistenza con questo stato di riparazione, selezionare la casella di controllo **Stato Non iniziato abilitato**.  
8. Analogamente, selezionare le caselle di controllo **Stato In Corso abilitato**, **Stato Completato abilitato** e **Stato In attesa abilitato**.

Ripetere i passaggi indicati per ogni opzione dello stato di riparazione che si intende creare.

## <a name="see-also"></a>Vedere anche

[Stato ordine assistenza e stato riparazione](service-service-order-status-and-repair-status.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
