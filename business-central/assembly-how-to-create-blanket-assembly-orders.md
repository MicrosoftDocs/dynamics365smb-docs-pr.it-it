---
title: Creare ordini di assemblaggio programmati
description: Creare ordini di vendita programmati per articoli di assemblaggio personalizzati prima di creare periodicamente gli ordini di vendita effettivi in base al contratto degli ordini programmati.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-blanket-assembly-orders"></a>Creare ordini di assemblaggio programmati

Puoi utilizzare la gestione assemblaggio per personalizzare un articolo di assemblaggio nella richiesta di un cliente durante il processo di vendita. Per ulteriori informazioni, vedi [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

 Come per qualsiasi altro tipo di articolo, è anche possibile creare ordini di vendita programmati per gli articoli di assemblaggio personalizzati prima di creare periodicamente gli ordini di vendita effettivi in base al contratto degli ordini programmati. Questo processo prevede diversi passaggi aggiuntivi se viene confrontato alla creazione di un ordine di vendita programmato normale e utilizza una variazione di un ordine di assemblaggio collegato, ossia un ordine di assemblaggio programmato.

> [!NOTE]  
>  Come in tutti gli ordini programmati, le quantità negli ordini di assemblaggio programmati sono solo previsioni e non diventano operative finché non viene effettuata la conversione in ordini di assemblaggio effettivi. Di conseguenza, le funzionalità dell'ordine, ad esempio calcolo della disponibilità, impegno e tracciabilità dell'articolo, non sono attive negli ordini di assemblaggio programmati.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Per creare un ordine di assemblaggio programmato per un articolo assemblato su ordine

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita programmati**, quindi scegli il collegamento correlato.  
2. Creare un nuovo ordine di vendita programmato con una riga per un articolo di assemblaggio. Per ulteriori informazioni, vedere [Creare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md).  
3. Nel campo **Qtà per assemblaggio su ordine** nella riga dell'ordine di assemblaggio programmato, immettere la quantità completa.

    > [!NOTE]  
    >  Non è consigliabile creare contratti di ordini programmati per un importo parziale. Di conseguenza, è necessario immettere la stessa quantità immessa nel campo **Quantità** della riga dell'ordine di vendita programmato.  

4. Scegliere l'azione **Assemblaggio su ordine**, quindi l'azione **Righe di assemblaggio su ordine**. In alternativa, scegliere il campo **Qtà per assemblaggio su ordine** della riga.  
5. Nella pagina **Righe di assemblaggio su ordine** esaminare o modificare le righe dell'ordine di assemblaggio in base al contratto di ordini programmati stipulato con il cliente. Se si desidera visualizzare altre informazioni, scegliere l'azione **Mostra documento** per aprire l'ordine di assemblaggio programmato completo. Non è possibile modificare il contenuto della maggior parte dei campi né effettuare la registrazione.  
6. Dopo avere rettificato le righe dell'ordine di assemblaggio in base al contratto di ordine programmato, chiudere la pagina **Righe di assemblaggio su ordine** per tornare alla pagina **Ordini vendita programmati**.  
7. Quando il cliente richiede la creazione di un ordine di vendita in base all'ordine di vendita programmato concordato, creare un ordine di vendita per l'articolo o gli articoli di assemblaggio concordati. Per ulteriori informazioni, vedere [Creare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md).

L'ordine di assemblaggio programmato collegato ed eventuali personalizzazioni sono collegati al nuovo ordine di vendita per preparare l'assemblaggio dell'articolo o degli articoli da vendere.  

## <a name="see-also"></a>Vedere anche

[Creare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
