---
title: Dettagli di progettazione - Disponibilità nella warehouse
description: Scopri i diversi fattori che influenzano la disponibilità degli articoli nella warehouse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# <a name="design-details-availability-in-the-warehouse"></a>Dettagli di progettazione: Disponibilità nella warehouse

Rimani aggiornato sulla disponibilità degli articoli per assicurarti che gli ordini in uscita vengano elaborati in modo efficiente e che i tuoi tempi di consegna siano ottimali.  

La disponibilità può variare, a seconda di diversi fattori. Ad esempio:

* Allocazioni a livello di collocazione quando si verificano attività di warehouse come prelievi e movimenti.
* Quando il sistema di prenotazione dell'inventario impone restrizioni da rispettare.

Prima di allocare le quantità ai prelievi per i flussi in uscita, [!INCLUDE [prod_short](includes/prod_short.md)] verifica che tutte le condizioni siano soddisfatte.

Quando le condizioni non sono soddisfatte, vengono visualizzati i messaggi di errore. Un messaggio tipico è il generico "Niente da gestire". da gestire". Il messaggio può essere visualizzato per varie ragioni, nei flussi in uscita e in entrata, dove una riga di documento contiene il campo **Qtà da gestire**.

## <a name="bin-content-and-reservations"></a>Contenuto collocazione e impegni

Le quantità di articoli esistono sia come movimenti warehouse che come movimenti contabili articoli nell'inventario. Questi due tipi di movimento contengono informazioni differenti sulla posizione degli articoli e sulla loro disponibilità. I movimenti warehouse definiscono la disponibilità di un articolo per collocazione e per tipo di collocazione, che è denominato anche contenuto collocazione. I movimenti contabili articoli definiscono la disponibilità di un articolo in base al relativo impegno per i documenti in uscita.  

[!INCLUDE [prod_short](includes/prod_short.md)] calcola la quantità disponibile per il prelievo quando il contenuto della collocazione è abbinato agli impegni.  

## <a name="quantity-available-to-pick"></a>Quantità disponibile per il prelievo

[!INCLUDE [prod_short](includes/prod_short.md)] riserva gli articoli per le spedizioni di ordini di vendita in sospeso in modo che non vengano prelevati per altri ordini di vendita spediti prima. [!INCLUDE [prod_short](includes/prod_short.md)] sottrae le quantità di articoli che sono già in lavorazione, come segue:

* Quantità riservate per altri documenti in uscita.
* Quantità nei documenti di prelievo esistenti.
* Quantità prelevate ma non ancora spedite o consumate.  

Il risultato è calcolato dinamicamente e viene visualizzato nel campo **Qtà disponibile da prelevare** della pagina **Prospetto prelievi**. Il valore viene calcolato anche quando gli utenti creano prelievi warehouse direttamente per i documenti in uscita. I seguenti sono esempi di documenti in uscita:

* Ordini vendita
* Consumo produzione
* Trasferimenti in uscita

Il risultato è disponibile in questi documenti nei campi relativi alla quantità, come il campo **Qtà. da gestire**.  

> [!NOTE]  
> Per la priorità degli impegni, la quantità da impegnare viene sottratta dalla quantità disponibile per il prelievo. Ad esempio, se la quantità disponibile nelle collocazioni di prelievo è 5 unità, ma 100 unità si trovano nelle collocazioni di stoccaggio, quando impegni più di 5 unità per un altro ordine, verrà visualizzato un messaggio di errore perché la quantità supplementare deve essere disponibile nelle collocazioni di prelievo.  

### <a name="calculating-the-quantity-available-to-pick"></a>Calcolo della quantità disponibile da prelevare

[!INCLUDE [prod_short](includes/prod_short.md)] calcola la quantità disponibile da prelevare come segue:  

quantità disponibile per il prelievo = quantità in collocazioni prelievo - quantità in prelievi e movimenti - (quantità impegnata in collocazioni prelievo + quantità impegnata in prelievi e movimenti)  

Nel seguente diagramma vengono mostrati i differenti elementi del calcolo.  

![Disponibile per il prelievo, con sovrapposizione di impegno.](media/design_details_warehouse_management_availability_2.png "Disponibile per il prelievo, con sovrapposizione di impegno")  

## <a name="quantity-available-to-reserve"></a>Quantità disponibile da impegnare

Poiché i concetti del contenuto delle condizioni e dell'impegno coesistono, la quantità di articoli disponibili per l'impegno deve essere allineata alle allocazioni ai documenti di warehouse in uscita.  

È possibile impegnare tutti gli articoli di magazzino, ad eccezione degli articoli per i quali è stata avviata l'elaborazione in uscita. La quantità disponibile per l'impegno è definita come quantità su tutti i documenti e in tutti i tipi di collocazione. Fanno eccezione le seguenti quantità in uscita:  

* Quantità nei documenti di prelievo non registrati  
* Quantità in collocazioni di spedizione  
* Quantità nelle collocazioni articoli per produzione  
* Quantità nelle collocazioni produzione aperte  
* Quantità nelle collocazioni di assemblaggio  
* Quantità nelle collocazioni di rettifica  

Il risultato viene visualizzato nel campo **Quantità totale disponibile** della pagina **Impegni**.  

In una riga di impegno, la quantità che non può essere impegnata, in quanto è allocata nella warehouse, viene visualizzata nel campo **Qtà. allocata in warehouse** della pagina **Impegni**.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Calcolo della quantità disponibile da impegnare

[!INCLUDE [prod_short](includes/prod_short.md)] calcola la quantità disponibile da impegnare come segue:  

quantità disponibile per l'impegno = quantità totale a magazzino - quantità in prelievi e movimenti per i documenti di origine - quantità impegnata - quantità in collocazioni in uscita  

Nel seguente diagramma vengono mostrati i differenti elementi del calcolo.  

![Disponibile per la prenotazione, per allocazioni warehouse.](media/design_details_warehouse_management_availability_3.png "Disponibile per la prenotazione, per allocazioni warehouse")  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Visualizzare la disponibilità degli articoli](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
