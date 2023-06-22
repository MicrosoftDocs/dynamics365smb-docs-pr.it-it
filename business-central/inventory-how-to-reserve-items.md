---
title: Come prenotare gli articoli
description: 'È possibile impegnare gli articoli per ordini di vendita, ordini di acquisto e ordini di produzione. Puoi anche impegnare gli articoli in magazzino o in entrata nelle righe del documento aperto.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 08/11/2022
ms.author: edupont
---
# <a name="reserve-items" />Prenotare articoli

È possibile impegnare gli articoli per ordini di vendita, ordini di acquisto, ordini di assistenza, ordini di assemblaggio, ordini di trasferimento e ordini di produzione. Puoi anche impegnare gli articoli in magazzino o in entrata nelle righe del giornale di registrazione o del documento aperto. Lo fai nella pagina **Prenotazione**.

In ogni riga che apri per impegnare gli articoli nella pagina **Impegno** vengono visualizzate informazioni su un tipo di riga (vendite, acquisti, registrazioni) o movimento di magazzino. Le righe contengono il numero di articoli disponibili per l'impegno da ogni tipo di riga o di movimento.

## <a name="reserve-items-for-sales" />Impegnare articoli per la vendita

La seguente procedure descrive come impegnare gli articoli da un ordine di vendita. I passaggi sono simili a quelli degli ordini di assemblaggio, trasferimento, assistenza e acquisto.
  
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Scegli l'ordine di vendita.
3. Nella Scheda dettaglio **Righe** scegliere l'azione **Impegna**. Verrà visualizzata la pagina **Impegni**.  
4. Seleziona la riga dalla quale vuoi impegnare gli articoli.  
5. Selezionare una delle seguenti azioni.  

    |**Funzione**|**Descrizione**|
    |------------------|---------------------|  
    |**Impegno Automatico**|Per impegnare automaticamente gli articoli nella pagina **Impegno**.|  
    |**Impegna da Riga Corrente**|per impegnare gli articoli dal documento nella riga selezionata.|  
    |**Annulla impegno da riga corrente**|per annullare l'impegno degli articoli dal documento sulla riga selezionata.|

> [!NOTE]  
> Se per l'ordine di vendita esistono righe di tracciabilità articolo, il sistema di impegno richiederà l'esecuzione di passaggi speciali. Per ulteriori informazioni, vedi la sezione [Per impegnare un numero seriale o di lotto specifico](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## <a name="reserve-an-item-for-a-production-order-line" />Impegnare articoli per le righe degli ordini di produzione

È possibile impegnare articoli per ordini di produzione. È però necessario distinguere tra righe degli ordini di produzione, ossia l'articolo padre, e componenti.

Nella seguente procedura viene utilizzato un ordine produzione confermato.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ord. produzione confermato**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di produzione confermato per il quale si vogliono impegnare gli articoli padre.  
3. Selezionare la riga dell'ordine di produzione pertinente.  
4. Nella Scheda dettaglio **Righe** scegliere l'azione **Impegna**.
5. Seleziona la riga **Riga vendite, Ordine** nella pagina **Impegni**, quindi scegli l'azione **Impegna da riga corrente**.  

La quantità immessa nella riga dell'ordine di produzione confermato viene ora impegnata.

## <a name="reserve-items-for-production-order-components" />Impegnare gli articoli per i componenti degli ordini di produzione

È possibile impegnare articoli per ordini di produzione. È però necessario distinguere tra righe degli ordini di produzione, ossia l'articolo padre, e componenti.

Nella seguente procedura viene utilizzato un ordine produzione confermato.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ord. produzione confermato**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di produzione confermato per il quale si vogliono impegnare gli articoli del componente.  
3. Selezionare la riga dell'ordine di produzione pertinente.  
4. Nella Scheda dettaglio **Righe** seleziona **Riga**, quindi scegli **Componenti**.  
5. Selezionare la riga componente pertinente.  
6. Nella Scheda dettaglio **Righe** scegli l'azione **Impegna**.  
7. Seleziona una riga nella pagina **Impegni**, quindi scegli l'azione **Impegna da riga corrente**.  

La quantità immessa nella riga del componente di produzione confermato viene ora impegnata.

## <a name="change-a-reservation" />Modificare un impegno

A volte, può essere necessario modificare un impegno su un articolo.

1. Dalla riga del documento da cui hai effettuato l'impegno, nella Scheda dettaglio **Righe**, scegli l'azione **Impegna**.  
2. Nella pagina **Impegni**, selezionare l'azione **Movimenti impegni**.
3. Nella pagina **Movimenti impegni** aggiorna il campo **Quantità** nella riga che vuoi modificare.
4. Conferma il messaggio successivo, scegliendo il pulsante **OK**.

## <a name="cancel-a-reservation" />Annullare un impegno

A volte può essere necessario annullare un impegno su un articolo.

1. Dalla riga del documento da cui vuoi annullare un impegno, nella Scheda dettaglio **Righe**, scegli l'azione **Impegna**.  
2. Nella pagina **Impegni**, seleziona l'azione **Movimenti impegni**.  
3. Nella pagina **Mov. impegni**, selezionare l'azione **Annulla impegno**.  
4. Conferma il messaggio successivo, scegliendo il pulsante **OK**.  

## <a name="reserve-a-specific-serial-or-lot-number" />Impegnare un numero seriale o di lotto specifico

Dai documenti in uscita per gli articoli tracciati, ad esempio ordini di vendita o liste di componenti di produzione, è possibile impegnare numeri seriali o di lotto specifici. Ciò può risultare utile, ad esempio, se si necessita di componenti di produzione da un lotto specifico per assicurare la coerenza con i batch di produzione precedenti o perché un cliente ha richiesto un numero seriale specifico. Per ulteriori informazioni, vedi [Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md).

Questa procedura è denominata impegno specifico, in quanto viene impegnata una quantità dell'articolo X appartenente al lotto X. Se si impegnano solo le quantità dell'articolo X, si tratta di impegno normale, non specifico. Ulteriori informazioni in [Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md).

La seguente procedura è basata su un ordine di vendita.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi scegli il collegamento correlato.  
2. Creare una riga di ordine di vendita per un articolo tracciato.  
3. Assegnare i numeri di serie e di lotto alla riga dell'ordine di vendita. Per ulteriori informazioni, vedi [Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md).
4. Nella riga ordine di vendita scegliere l'azione **Impegna**.  
5. Scegliere il pulsante **Sì** per impegnare numeri seriali o di lotto specifici.  
6. Nella pagina **Lista tracciabilità articolo** seleziona la combinazione dei numeri seriali e di lotto specifici assegnati.  
7. Fare clic su **OK** per aprire la pagina **Impegno** in cui viene visualizzato solo l'approvvigionamento con il numero di tracciabilità articolo specificato. Se vi sono impegni non specifici per numeri di tracciabilità articolo specificati per la riga, viene visualizzato un messaggio che indica la quantità già impegnata.  
8. Scegli l'azione **Impegno automatico** o **Impegna da riga corrente** per creare l'impegno per numeri di tracciabilità articolo specifici.

## <a name="see-related-microsoft-trainingtrainingmodulesmanage-outbound-serial-lot-numbers" />Vedi il relativo [training Microsoft](/training/modules/manage-outbound-serial-lot-numbers/)

## <a name="see-also" />Vedere anche

[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Utilizzare i numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
