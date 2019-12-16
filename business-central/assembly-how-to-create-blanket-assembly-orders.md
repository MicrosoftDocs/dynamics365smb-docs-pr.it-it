---
title: 'Procedura: Creare ordini di assemblaggio programmati | Documenti Microsoft'
description: Creare ordini di vendita programmati per articoli di assemblaggio personalizzati prima di creare periodicamente gli ordini di vendita effettivi in base al contratto degli ordini programmati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d15ecfe1d334c07c757cba10647267ae89fea629
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880882"
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
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
