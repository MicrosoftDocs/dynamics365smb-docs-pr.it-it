---
title: Come prenotare gli articoli
description: È possibile impegnare gli articoli per ordini di vendita, ordini di acquisto e ordini di produzione. È possibile impegnare gli articoli in magazzino o in entrata nelle righe del documento aperto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 498, 497
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6dcd912dfae36e31bd2642b5f1427483f3095c19
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148566"
---
# <a name="reserve-items"></a>Prenotare articoli
È possibile impegnare gli articoli per ordini di vendita, ordini di acquisto, ordini di assistenza, ordini di assemblaggio e ordini di produzione. È possibile impegnare gli articoli in magazzino o in entrata nelle righe del giornale di registrazione o del documento aperto. Eseguire l'operazione nella pagina **Impegno**.

In ogni riga della pagina **Impegno** che si apre per impegnare gli articoli, vengono visualizzate informazioni su un tipo di riga (vendite, acquisti, registrazioni) o movimento di magazzino. Le righe contengono il numero di articoli disponibili per l'impegno da ogni tipo di riga o di movimento.

## <a name="to-reserve-items-for-sales"></a>Per impegnare articoli per la vendita
Di seguito viene descritto come impegnare gli articoli da un ordine di vendita. I passaggi sono simili a quelli degli ordini di assemblaggio, assistenza e acquisto.  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2.  Nella Scheda dettaglio **Righe** di un ordine di vendita scegliere l'azione **Impegna**. Verrà visualizzata la pagina **Impegni**.  
3. Selezionare la riga dalla quale si desidera impegnare gli articoli.  
4. Selezionare una delle seguenti azioni.  

    |**Funzione**|**Descrizione**|
    |------------------|---------------------|  
    |**Impegno Automatico**|Per impegnare automaticamente gli articoli nella pagina **Impegno**.|  
    |**Impegna da Riga Corrente**|per impegnare gli articoli dal documento nella riga selezionata.|  
    |**Annulla impegno da riga corrente**|per annullare l'impegno degli articoli dal documento sulla riga selezionata.|

> [!NOTE]  
>  Se per l'ordine di vendita esistono righe di tracciabilità articolo, il sistema di impegno richiederà l'esecuzione di passaggi speciali. Per ulteriori informazioni, vedere [Per impegnare un numero seriale o di lotto specifico](inventory-how-to-reserve-items.md#to-reserve-a-specific-serial-or-lot-number).  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Per impegnare articoli per le righe degli ordini di produzione  
È possibile impegnare articoli per ordini di produzione. È però necessario distinguere tra righe degli ordini di produzione, ossia l'articolo padre, e componenti.

Nella seguente procedura viene utilizzato un ordine produzione confermato.   
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ord. produzione confermato**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di produzione confermato per il quale si vogliono impegnare gli articoli padre.  
3. Selezionare la riga dell'ordine di produzione pertinente.  
4. Nella Scheda dettaglio **Righe** scegliere l'azione **Impegna**.
5. Selezionare la riga **Riga vendite, Ordine** nella pagina **Impegni**, quindi scegliere l'azione **Impegna da riga corrente**.  

La quantità immessa nella riga dell'ordine di produzione confermato viene ora impegnata.

## <a name="to-reserve-items-for-production-order-components"></a>Per impegnare gli articoli per i componenti degli ordini di produzione  
È possibile impegnare articoli per ordini di produzione. È però necessario distinguere tra righe degli ordini di produzione, ossia l'articolo padre, e componenti.

Nella seguente procedura viene utilizzato un ordine produzione confermato.    
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ord. produzione confermato**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di produzione confermato per il quale si vogliono impegnare gli articoli del componente.  
3. Selezionare la riga dell'ordine di produzione pertinente.  
4. Nella Scheda dettaglio **Righe** selezionare **Riga**, quindi scegliere **Componenti**.  
5. Selezionare la riga componente pertinente.  
6. Nella Scheda dettaglio **Righe** scegliere l'azione **Impegna**.  
7. Selezionare una riga nella pagina **Impegni**, quindi scegliere l'azione **Impegna da riga corrente**.  

La quantità immessa nella riga del componente di produzione confermato viene ora impegnata.

## <a name="to-change-a-reservation"></a>Per modificare un impegno  
A volte, può essere necessario modificare un impegno su un articolo.   
1. Dalla riga del documento da cui è stato effettuato l'impegno, nella Scheda dettaglio **Righe**, scegliere l'azione **Impegna**.  
2. Nella pagina **Impegni**, selezionare l'azione **Movimenti impegni**.
3. Nella pagina **Movimenti impegni** aggiornare il campo **Quantità** nella riga che si desidera modificare.
4. Confermare il messaggio successivo, scegliendo il pulsante **OK**.

## <a name="to-cancel-a-reservation"></a>Per annullare un impegno  
A volte può essere necessario annullare un impegno su un articolo.   
1. Dalla riga del documento da cui si desidera annullare un impegno, nella Scheda dettaglio **Righe**, scegliere l'azione **Impegna**.  
2. Nella pagina **Impegni**, selezionare l'azione **Movimenti impegni**.  
3.  Nella pagina **Mov. impegni**, selezionare l'azione **Annulla impegno**.  
4.  Confermare il messaggio successivo, scegliendo il pulsante **OK**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Per impegnare un numero seriale o di lotto specifico  
Dai documenti in uscita per gli articoli tracciati, ad esempio ordini di vendita o liste di componenti di produzione, è possibile impegnare numeri seriali o di lotto specifici. Ciò può risultare utile, ad esempio, se si necessita di componenti di produzione da un lotto specifico per assicurare la coerenza con i batch di produzione precedenti o perché un cliente ha richiesto un numero seriale specifico. Per ulteriori informazioni, vedere [Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md).

Ciò è denominato impegno specifico, in quanto viene impegnata una quantità dell'articolo X appartenente al lotto X. Se si impegnano semplicemente quantità dell'articolo X, si tratta di impegno normale, non specifico. Per ulteriori informazioni, vedere [Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md).

La seguente procedura è basata su un ordine di vendita.    
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi scegli il collegamento correlato.  
2. Creare una riga di ordine di vendita per un articolo tracciato.  
3. Assegnare i numeri di serie e di lotto alla riga dell'ordine di vendita. Per ulteriori informazioni, vedere [Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md).
4. Nella riga ordine di vendita scegliere l'azione **Impegna**.  
5. Scegliere il pulsante **Sì** per impegnare numeri seriali o di lotto specifici.  
6. Nella pagina **Lista tracciabilità articolo** selezionare la combinazione dei numeri seriali e di lotto specifici appena assegnati.  
7. Fare clic su **OK** per aprire la pagina **Impegno** in cui viene visualizzato solo l'approvvigionamento con il numero di tracciabilità articolo specificato. Se vi sono impegni non specifici per numeri di tracciabilità articolo specificati per la riga, viene visualizzato un messaggio che indica la quantità già impegnata.  
8. Scegliere l'azione **Impegno automatico** o **Impegna da riga corrente** per creare l'impegno per numeri di tracciabilità articolo specifici.

## <a name="see-also"></a>Vedi anche
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]