---
title: Vendere articoli di assemblaggio su ordine e articoli di magazzino insieme
description: 'Se una parte di un articolo da assemblare per magazzino non è disponibile, puoi creare un ordine di assemblaggio per la quantità rimanente.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Vendere articoli di assemblaggio su ordine e articoli di magazzino insieme

Se il campo **Criteri di assemblaggio** nella scheda articolo di un articolo di assemblaggio contiene **assemblaggio per magazzino**, l'ordine di vendita presuppone che l'articolo sia già assemblato e possa essere prelevato dal magazzino, se disponibile. Di conseguenza, un ordine di assemblaggio non viene automaticamente creato e collegato alla riga dell'ordine di vendita. Tuttavia, se una parte o tutta la quantità non è disponibile, puoi creare un ordine di assemblaggio per la quantità rimanente. A tal fine, compila il campo **Qtà per assemblaggio su ordine** nella riga dell'ordine di vendita. Questa impostazione ti consente di assemblare l'articolo su ordine anche se è impostato per l'assemblaggio per magazzino.  

Hai una flessibilità simile quando vendi articoli assemblati su ordine e una parte della quantità è già in magazzino. Ti consigliamo di detrarre tale quantità dall'ordine di assemblaggio. Per ulteriori informazioni sulla vendita di articoli di magazzino, vai a [Vendere gli articoli di magazzino nei flussi da assemblare su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Alcune regole si applicano al campo **Qtà da spedire** nelle righe dell'ordine di vendita che contengono una combinazione di quantità per l'assemblaggio su ordine e quantità di magazzino. Per saperne di più sulle regole, vai a [Scenari di combinazione](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> La procedura seguente non include i passaggi dell'ordine di vendita che occorre eseguire prima di creare un ordine di assemblaggio per le quantità non disponibili.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Per vendere articoli di assemblaggio su ordine e articoli di magazzino insieme

1. In una riga dell'ordine di vendita per un articolo impostato per l'assemblaggio per magazzino, immetti una quantità che supera quella di magazzino nel campo **Quantità**. Viene visualizzata la pagina **Controllo disponibilità**. Per ulteriori informazioni sulla disponibilità degli articoli, vai a [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md).
2. Nel campo **Qtà. per assemblaggio su ordine** immetti il valore del campo **Quantità totale**.  
3. Applica le modifiche necessarie ai componenti di assemblaggio. Per ulteriori informazioni vedi [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  
4. Rilascia l'ordine di vendita per rendere gli articoli disponibili per il prelievo e per l'assemblaggio degli articoli non disponibili. Per ulteriori informazioni sui passaggio di assemblaggio standard, vedi [Assemblare articoli](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Il campo **Codice collocazione** nell'ordine di vendita può contenere il valore del campo **Cod. coll. sp. ass. su ordine** o del campo **Cod. coll. art. da assembl.** nella scheda ubicazione. In tal caso, il campo **Codice collocazione** nella riga dell'ordine di vendita può essere errato in questa combinazione di quantità di assemblaggio su ordine e assemblaggio per magazzino. Ti consigliamo di verificare che la collocazione nel campo **Cod. collocazione** funzioni per tutte le quantità. In alternativa, immettere due quantità diverse in righe separate dell'ordine di vendita.  

## <a name="see-also"></a>Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
