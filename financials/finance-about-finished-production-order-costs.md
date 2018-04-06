---
title: Informazioni sui costi di un ordine di produzione chiuso | Microsoft Docs
description: "La chiusura di un ordine di produzione è un'attività importante nel completamento del ciclo di vita del costing dell'articolo prodotto. I costi finali, inclusi gli scostamenti in un ambiente con costi standard, i valori effettivi in un ambiente con costi FIFO, medi o LIFO, vengono calcolati tramite il processo batch **Rettifica costo - Movimenti articoli**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 010d4d4568f45cbe8fe13864ac6996de1e224b76
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="2c304-104">Informazioni sui costi di un ordine di produzione chiuso</span><span class="sxs-lookup"><span data-stu-id="2c304-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="2c304-105">La chiusura di un ordine di produzione è un'attività importante nel completamento del ciclo di vita del costing dell'articolo prodotto.</span><span class="sxs-lookup"><span data-stu-id="2c304-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="2c304-106">I costi finali, inclusi gli scostamenti in un ambiente con costi standard, i valori effettivi in un ambiente con costi FIFO, medi o LIFO, vengono calcolati tramite il processo batch **Rettifica costo - Movimenti articoli** che consente la riconciliazione finanziaria dei costi di produzione degli articoli.</span><span class="sxs-lookup"><span data-stu-id="2c304-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="2c304-107">Affinché un ordine di produzione venga considerato per la rettifica del costo, lo stato deve essere impostato come **Completato**.</span><span class="sxs-lookup"><span data-stu-id="2c304-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="2c304-108">È pertanto essenziale che, al completamento, lo stato di un ordine di produzione venga modificato in **Completato**.</span><span class="sxs-lookup"><span data-stu-id="2c304-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="2c304-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c304-109">Example</span></span>  
 <span data-ttu-id="2c304-110">In un ambiente di costi standard, quando si consuma materiale per produrre un articolo, detto semplicemente, il costo dell'articolo più i costi generali e di manodopera confluiscono nel WIP.</span><span class="sxs-lookup"><span data-stu-id="2c304-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="2c304-111">Quando l'articolo viene prodotto, il WIP viene ridotto dell'importo del costo standard dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="2c304-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="2c304-112">In genere, questi costi netti non sono uguali a zero.</span><span class="sxs-lookup"><span data-stu-id="2c304-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="2c304-113">Perché l'importo sia uguale a zero, è necessario eseguire il processo batch **Rettifica costo - Movimenti articoli**, notando che solo gli ordini di produzione con stato **Completato** verranno considerati per la rettifica.</span><span class="sxs-lookup"><span data-stu-id="2c304-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c304-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c304-114">See Also</span></span>  
[<span data-ttu-id="2c304-115">Gestione dei costi di magazzino</span><span class="sxs-lookup"><span data-stu-id="2c304-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="2c304-116">Manufacturing</span><span class="sxs-lookup"><span data-stu-id="2c304-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="2c304-117">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c304-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

