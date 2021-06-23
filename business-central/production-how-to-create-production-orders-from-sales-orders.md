---
title: Creare gli ordini di produzione dagli ordini di vendita
description: Puoi creare gli ordini di produzione dagli ordini vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115238"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="1a5c2-103">Creare gli ordini di produzione dagli ordini di vendita</span><span class="sxs-lookup"><span data-stu-id="1a5c2-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="1a5c2-104">È possibile creare ordini di produzione per gli articoli prodotti direttamente dagli ordini di vendita.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="1a5c2-105">Per creare gli ordini di produzione dagli ordini di vendita</span><span class="sxs-lookup"><span data-stu-id="1a5c2-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="1a5c2-106">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1a5c2-107">Selezionare l'ordine di vendita per il quale creare un ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="1a5c2-108">Scegliere l'azione **Pianifica**.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-108">Choose the **Planning** action.</span></span> <span data-ttu-id="1a5c2-109">Nella pagina **Pianifica ordine vendita** è possibile visualizzare la disponibilità dell'articolo presente nell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="1a5c2-110">Selezionare l'azione **Crea ordine produzione**.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="1a5c2-111">Selezionare lo stato e il tipo di ordine.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="1a5c2-112">Scegli il pulsante **Sì** per creare uno o più ordini di produzione per le righe che hanno **Ordine prod.** nel loro campo **Sistema di rifornimento**.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="1a5c2-113">Le righe domanda nell'ordine di produzione creato che hanno **Ord. prod.** nel campo **Sistema di rifornimento** rappresentano gli ordini di produzione sottostanti.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="1a5c2-114">Dopo aver generato tali ordini di produzione, ricordarsi di identificare la domanda di componenti non soddisfatta utilizzando la pagina **Pianificazione ordini** o la funzione **Ripianifica** dagli ordini creati.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="1a5c2-115">Tipo ordine</span><span class="sxs-lookup"><span data-stu-id="1a5c2-115">Order type</span></span>  
<span data-ttu-id="1a5c2-116">È possibile scegliere tra due modi per creare gli ordini di produzione come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="1a5c2-117">Opzione</span><span class="sxs-lookup"><span data-stu-id="1a5c2-117">Option</span></span>|<span data-ttu-id="1a5c2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a5c2-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="1a5c2-119">Ordine articolo</span><span class="sxs-lookup"><span data-stu-id="1a5c2-119">Item Order</span></span>|<span data-ttu-id="1a5c2-120">Viene creato un ordine di produzione per ogni ordine di produzione necessario che è rappresentato da una riga nella finestra **Pianifica ordine vendita**.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="1a5c2-121">Ordine progetto</span><span class="sxs-lookup"><span data-stu-id="1a5c2-121">Project Order</span></span>|<span data-ttu-id="1a5c2-122">Viene creato un ordine di produzione per tutti gli ordini di produzione necessari che sono rappresentati dalle righe nella finestra **Pianifica ordine vendita**.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="1a5c2-123">Quando si utilizzano gli ordini di produzione, il campo **Tipo Origine** dell'ordine di produzione include le **Testate Vendita** e nell'ordine sono disponibili più righe, una per ogni articolo di riga di vendita da produrre.</span><span class="sxs-lookup"><span data-stu-id="1a5c2-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="1a5c2-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1a5c2-124">See Also</span></span>  
[<span data-ttu-id="1a5c2-125">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="1a5c2-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1a5c2-126">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1a5c2-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1a5c2-127">Magazzino</span><span class="sxs-lookup"><span data-stu-id="1a5c2-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1a5c2-128">Acquisti</span><span class="sxs-lookup"><span data-stu-id="1a5c2-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1a5c2-129">[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="1a5c2-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="1a5c2-130">Impostare le procedure ottimali: Pianificazione forniture</span><span class="sxs-lookup"><span data-stu-id="1a5c2-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="1a5c2-131">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a5c2-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
