---
title: Come utilizzare famiglie di articoli nella produzione | Microsoft Docs
description: L'operazione principale da eseguire per personalizzare un calendario di base per la propria società, o per uno dei partner commerciali, è la modifica dello stato dei giorni lavorativi e non lavorativi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4c926b8f7663c805f07bcd7c85339b109f85a7ff
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383202"
---
# <a name="work-with-production-families"></a><span data-ttu-id="0ab31-103">Utilizzare famiglie di prodotti</span><span class="sxs-lookup"><span data-stu-id="0ab31-103">Work with Production Families</span></span>
<span data-ttu-id="0ab31-104">Una famiglia di prodotti consiste in un gruppo di articoli individuali la cui relazione si basa sulla similarità dei rispettivi processi di lavorazione.</span><span class="sxs-lookup"><span data-stu-id="0ab31-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="0ab31-105">Formando delle famiglie di produzione, è possibile che alcuni articoli siano lavorati due o più volte nel corso di una produzione; questa operazione ottimizzerà il consumo di materiale.</span><span class="sxs-lookup"><span data-stu-id="0ab31-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="0ab31-106">Nel campo **Quantità** della pagina **Famiglie di prodotti**, immettere la quantità che sarà prodotta quando l'intera famiglia sarà stata lavorata una volta.</span><span class="sxs-lookup"><span data-stu-id="0ab31-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="0ab31-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="0ab31-107">Example</span></span>
<span data-ttu-id="0ab31-108">Nei processi di perforazione, è possibile che da una lamina vengano prodotti contemporaneamente quattro pezzi di un articolo e 10 pezzi di un altro articolo differente.</span><span class="sxs-lookup"><span data-stu-id="0ab31-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="0ab31-109">La perforatrice perforerà tutti i 14 pezzi in un'unica fase.</span><span class="sxs-lookup"><span data-stu-id="0ab31-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="0ab31-110">La creazione di famiglie di produzione riduce le quantità di scarto perché ciò che generalmente costituisce gli scarti rimanenti dalla produzione di pezzi di grandi dimensioni viene utilizzato per produrre i pezzi di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0ab31-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="0ab31-111">Per impostare una famiglia di prodotti</span><span class="sxs-lookup"><span data-stu-id="0ab31-111">To set up a production family</span></span>
1. <span data-ttu-id="0ab31-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Famiglie** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0ab31-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="0ab31-113">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0ab31-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="0ab31-114">Per produrre in base a una famiglia di prodotti</span><span class="sxs-lookup"><span data-stu-id="0ab31-114">To produce based on a production family</span></span>
1. <span data-ttu-id="0ab31-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ord. produzione confermati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0ab31-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0ab31-116">Creare un nuovo ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="0ab31-116">Create a new production order.</span></span> <span data-ttu-id="0ab31-117">Per ulteriori informazioni, vedere [Creare ordini di produzione](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="0ab31-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="0ab31-118">Nel campo **Tipo origine**, selezionare **Famiglie di prodotti**.</span><span class="sxs-lookup"><span data-stu-id="0ab31-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="0ab31-119">Nel campo **Nr. risorsa**, selezionare la famiglia di prodotti pertinente.</span><span class="sxs-lookup"><span data-stu-id="0ab31-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ab31-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ab31-120">See Also</span></span>
[<span data-ttu-id="0ab31-121">Creare le distinte base di produzione</span><span class="sxs-lookup"><span data-stu-id="0ab31-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="0ab31-122">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="0ab31-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="0ab31-123">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="0ab31-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="0ab31-124">[Pianif.](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="0ab31-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="0ab31-125">Magazzino</span><span class="sxs-lookup"><span data-stu-id="0ab31-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0ab31-126">Acquisti</span><span class="sxs-lookup"><span data-stu-id="0ab31-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0ab31-127">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ab31-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]