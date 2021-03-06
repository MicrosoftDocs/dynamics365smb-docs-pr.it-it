---
title: 'Procedura: Creare ordini di assemblaggio programmati | Documenti Microsoft'
description: Creare ordini di vendita programmati per articoli di assemblaggio personalizzati prima di creare periodicamente gli ordini di vendita effettivi in base al contratto degli ordini programmati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9e96cf7edd4a2080b92c88215f67e93bc4e0f7f8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772981"
---
# <a name="create-blanket-assembly-orders"></a>Creare ordini di assemblaggio programmati
È possibile utilizzare gestione assemblaggio per personalizzare un articolo di assemblaggio nella richiesta di un cliente durante il processo di vendita. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

 Come per qualsiasi altro tipo di articolo, è anche possibile creare ordini di vendita programmati per gli articoli di assemblaggio personalizzati prima di creare periodicamente gli ordini di vendita effettivi in base al contratto degli ordini programmati. Questo processo prevede diversi passaggi aggiuntivi se viene confrontato alla creazione di un ordine di vendita programmato normale e utilizza una variazione di un ordine di assemblaggio collegato, ossia un ordine di assemblaggio programmato.

> [!NOTE]  
>  Come in tutti gli ordini programmati, le quantità negli ordini di assemblaggio programmati sono solo previsioni e non diventano operative finché non viene effettuata la conversione in ordini di assemblaggio effettivi. Di conseguenza, le funzionalità dell'ordine, ad esempio calcolo della disponibilità, impegno e tracciabilità dell'articolo, non sono attive negli ordini di assemblaggio programmati.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Per creare un ordine di assemblaggio programmato per un articolo assemblato su ordine  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita programmati** e quindi scegliere il collegamento correlato.  
2. Creare un nuovo ordine di vendita programmato con una riga per un articolo di assemblaggio. Per ulteriori informazioni, vedere [Creare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md).  
3. Nel campo **Qtà per assemblaggio su ordine** nella riga dell'ordine di assemblaggio programmato, immettere la quantità completa.

    > [!NOTE]  
    >  Non è consigliabile creare contratti di ordini programmati per un importo parziale. Di conseguenza, è necessario immettere la stessa quantità immessa nel campo **Quantità** della riga dell'ordine di vendita programmato.  

4. Scegliere l'azione **Assemblaggio su ordine**, quindi l'azione **Righe di assemblaggio su ordine**. In alternativa, scegliere il campo **Qtà per assemblaggio su ordine** della riga.  
5. Nella pagina **Righe di assemblaggio su ordine** esaminare o modificare le righe dell'ordine di assemblaggio in base al contratto di ordini programmati stipulato con il cliente. Se si desidera visualizzare altre informazioni, scegliere l'azione **Mostra documento** per aprire l'ordine di assemblaggio programmato completo. Non è possibile modificare il contenuto della maggior parte dei campi né effettuare la registrazione.  
6. Dopo avere rettificato le righe dell'ordine di assemblaggio in base al contratto di ordine programmato, chiudere la pagina **Righe di assemblaggio su ordine** per tornare alla pagina **Ordini vendita programmati**.  
7. Quando il cliente richiede la creazione di un ordine di vendita in base all'ordine di vendita programmato concordato, creare un ordine di vendita per l'articolo o gli articoli di assemblaggio concordati. Per ulteriori informazioni, vedere [Creare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md).

L'ordine di assemblaggio programmato collegato ed eventuali personalizzazioni sono collegati al nuovo ordine di vendita per preparare l'assemblaggio dell'articolo o degli articoli da vendere.  

## <a name="see-also"></a>Vedi anche
[Creare ordini vendita programmati](sales-how-to-create-blanket-sales-orders.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]