---
title: Vendere gli articoli di magazzino nei flussi da assemblare su ordine
description: Gli articoli assemblati su ordine vengono assemblati per gli ordini di vendita tramite un ordine di assemblaggio.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows"></a><a name="selling-inventory-items-in-assemble-to-order-flows"></a>Vendere gli articoli di magazzino nei flussi di assemblaggio su ordine

Se il campo **Criteri di assemblaggio** nella scheda articolo di un articolo di assemblaggio contiene **Assemblaggio su ordine**, il processo dell'ordine di vendita presuppone che l'articolo non sia in magazzino e debba essere assemblato per l'ordine di vendita. Quando aggiungi l'articolo a una riga dell'ordine di vendita, [!INCLUDE [prod_short](includes/prod_short.md)] crea un ordine di assemblaggio collegato all'ordine di vendita. Per ulteriori informazioni su come vendere gli articoli assemblati su ordine, vai a [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md). Tuttavia, se parte della quantità dell'ordine di vendita è già disponibile in magazzino, puoi ridurre la quantità dell'ordine di assemblaggio modificando il campo **Qtà per assemblaggio su ordine** nella riga dell'ordine di vendita.  

È relativamente raro che le aziende vendano articoli di magazzino come articoli da assemblare su ordine. Gli articoli assemblati su ordine in genere non sono standard. Sono personalizzati per soddisfare le esigenze specifiche del cliente. Tuttavia, potresti avere quantità di articoli da assemblare su ordine nel magazzino a causa di resi o annullamenti di ordini. Tali quantità devono essere prelevate e vendute prima che ne vengano assemblate di nuove.  

> [!NOTE]  
> Per verificare se gli articoli assemblati su ordine sono già disponibili per gli ordini di assemblaggio, utilizza il riquadro Dettaglio informazioni **Dettagli riga di vendita** nell'ordine cliente.  

Puoi fare cose simili quando vendi articoli di assemblaggio dall'inventario e parte o tutta la quantità non è disponibile. È possibile fornire la quantità mancante tramite un ordine di assemblaggio. Per ulteriori informazioni sulla vendita di inventario e articoli di assemblaggio, vai a [Vedere insieme articoli assemblaggio su ordine e articoli in magazzino](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Alcune regole si applicano al campo **Qtà da spedire** nelle righe dell'ordine di vendita che contengono una combinazione di quantità per l'assemblaggio su ordine e quantità di magazzino. Per saperne di più sulle regole, vai a [Scenari di combinazione](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Nella procedura, le quantità di assemblaggio su ordine vengono sostituite con le quantità di magazzino in una riga dell'ordine di vendita. I seguenti passaggi forniscono una panoramica:

1. Determina la disponibilità.
2. Riduci la quantità dall'ordine di assemblaggio collegato.
3. Prenota la quantità di inventario per assicurarti che venga prelevata e spedita per l'ordine.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Per vendere gli articoli di magazzino nei flussi da assemblare su ordine

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Creare un ordine di vendita. Per ulteriori informazioni su come creare gli ordini di vendita, vedi [Vendere prodotti](sales-how-sell-products.md).  
3. In una riga dell'ordine di vendita contenente un articolo assemblato su ordine immetti la quantità nel campo **Quantità**.  
4. Nel riquadro Dettaglio informazioni **Dettagli righe vendite** determina se tutta o parte della quantità richiesta è disponibile.  
5. Nel campo **Qtà per assemblaggio su ordine** dedurre la quantità disponibile in modo che solo la quantità non disponibile venga assemblata su ordine. Il campo **Quantità impegnata** viene diminuito di conseguenza per indicare che il collegamento da ordine a ordine, o impegno, si applica solo alla quantità da assemblare.  
6. Nella Scheda dettaglio **Righe** scegliere **Funzioni** e quindi scegliere l'azione **Impegna**.  
7. Nella pagina **Impegni** selezionare la riga o le righe del movimento contabile articolo che contengono le quantità disponibili, scegliere l'azione **Impegna da riga corrente**, quindi fare clic su **OK**.  

    Nella pagina **Quantità impegnata** della finestra **Ordine vendita** verrà indicato che l'intera quantità per la riga dell'ordine è impegnata. Il campo **Qtà per assemblaggio su ordine** riflette ancora la quantità che deve essere assemblata.  

8. Rilascia l'ordine di vendita per rendere gli articoli disponibili per il prelievo e per l'assemblaggio degli articoli non disponibili. Per ulteriori informazioni sugli articoli di assemblaggio, vai a [Articoli di assemblaggio](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Il campo **Codice collocazione** nell'ordine di vendita può contenere il valore del campo **Cod. coll. sp. ass. su ordine** o del campo **Cod. coll. art. da assembl.** nella scheda ubicazione. In tal caso, il campo **Codice collocazione** nella riga dell'ordine di vendita può essere errato in questa combinazione di quantità di assemblaggio su ordine e assemblaggio per magazzino. Ti consigliamo di verificare che la collocazione nel campo **Cod. collocazione** funzioni per tutte le quantità. In alternativa, immettere due quantità diverse in righe separate dell'ordine di vendita.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
