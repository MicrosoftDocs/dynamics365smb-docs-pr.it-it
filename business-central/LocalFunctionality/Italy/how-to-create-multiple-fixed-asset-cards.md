---
title: 'Procedura: Creazione di più schede cespite'
description: Durante la registrazione delle fatture di acquisto è possibile creare automaticamente più schede cespite.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d3f7edde01c763b02453e094efac8a541b3ea9d9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919995"
---
# <a name="create-multiple-fixed-asset-cards"></a><span data-ttu-id="318c2-103">Creazione di più schede cespite</span><span class="sxs-lookup"><span data-stu-id="318c2-103">Create Multiple Fixed Asset Cards</span></span>
<span data-ttu-id="318c2-104">Durante la registrazione delle fatture di acquisto è possibile creare automaticamente più schede cespite.</span><span class="sxs-lookup"><span data-stu-id="318c2-104">You can create multiple fixed asset cards automatically during purchase invoice posting.</span></span> <span data-ttu-id="318c2-105">Se ad esempio la società acquista 200 computer dello stesso tipo dallo stesso fornitore, non è necessario creare manualmente una scheda cespite per ogni computer, ma tali schede possono essere create automaticamente.</span><span class="sxs-lookup"><span data-stu-id="318c2-105">For example, if your company purchases 200 computers of the same kind from the same vendor, you do not have to manually create a fixed asset card for each computer; the fixed asset cards can be created automatically.</span></span>  

## <a name="to-create-multiple-fixed-asset-cards"></a><span data-ttu-id="318c2-106">Per creare più schede cespite</span><span class="sxs-lookup"><span data-stu-id="318c2-106">To create multiple fixed asset cards</span></span>  

1.  <span data-ttu-id="318c2-107">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="318c2-107">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="318c2-108">Scegliere l'azione **Liste**, quindi l'azione **Cespiti**.</span><span class="sxs-lookup"><span data-stu-id="318c2-108">Choose the **Lists** action, and then choose the **Fixed Assets** action.</span></span>  
3.  <span data-ttu-id="318c2-109">Nella pagina **Lista cespiti**, scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="318c2-109">On the **Fixed Asset List** page, choose the **New** action.</span></span>  
4.  <span data-ttu-id="318c2-110">Compilare i campi della pagina **Scheda cespite**.</span><span class="sxs-lookup"><span data-stu-id="318c2-110">On the **Fixed Asset Card** page, fill in the relevant fields.</span></span>  

    <span data-ttu-id="318c2-111">Verrà utilizzato il valore del campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="318c2-111">You will use the value of the **No.**</span></span> <span data-ttu-id="318c2-112">quando successivamente si generano i cespiti residui.</span><span class="sxs-lookup"><span data-stu-id="318c2-112">field when you generate the remaining fixed assets later.</span></span>  

5.  <span data-ttu-id="318c2-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="318c2-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="318c2-114">Creare un nuovo ordine di acquisto o aprire l'ordine di acquisto esistente.</span><span class="sxs-lookup"><span data-stu-id="318c2-114">Create a new purchase order, or open the existing purchase order.</span></span>  
7.  <span data-ttu-id="318c2-115">Espandere la Scheda dettaglio **Righe**.</span><span class="sxs-lookup"><span data-stu-id="318c2-115">Expand the **Lines** FastTab.</span></span>  
8.  <span data-ttu-id="318c2-116">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="318c2-116">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="318c2-117">Campo</span><span class="sxs-lookup"><span data-stu-id="318c2-117">Field</span></span>|<span data-ttu-id="318c2-118">Description</span><span class="sxs-lookup"><span data-stu-id="318c2-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="318c2-119">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="318c2-119">**Type**</span></span>|<span data-ttu-id="318c2-120">Selezionare **Cespite**.</span><span class="sxs-lookup"><span data-stu-id="318c2-120">Select **Fixed Asset**.</span></span>|  
    |<span data-ttu-id="318c2-121">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="318c2-121">**No.**</span></span>|<span data-ttu-id="318c2-122">Specificare il numero del cespite.</span><span class="sxs-lookup"><span data-stu-id="318c2-122">Specify the fixed asset number.</span></span><br /><br /> <span data-ttu-id="318c2-123">**NOTA:** deve corrispondere al numero di cespite immesso nell'elenco **Cespite**.</span><span class="sxs-lookup"><span data-stu-id="318c2-123">**NOTE:** This should be the same fixed asset number that you entered in the **Fixed Asset** list.</span></span>|  
    |<span data-ttu-id="318c2-124">**Nr. di schede cespite**</span><span class="sxs-lookup"><span data-stu-id="318c2-124">**No. of Fixed Asset Cards**</span></span>|<span data-ttu-id="318c2-125">Specificare il numero di duplicati corrispondente per il cespite.</span><span class="sxs-lookup"><span data-stu-id="318c2-125">Specify the relevant number of duplicates for your fixed asset.</span></span><br /><br /> <span data-ttu-id="318c2-126">**NOTA:** durante la registrazione della fattura vengono automaticamente generate schede cespite duplicate, che vengono aggiunte all'elenco di cespiti.</span><span class="sxs-lookup"><span data-stu-id="318c2-126">**NOTE:** During invoice posting, duplicate fixed asset cards are automatically generated and added to the fixed asset list.</span></span> <span data-ttu-id="318c2-127">L'unica differenza tra le varie schede cespite duplicate è il numero assegnato a ciascun cespite.</span><span class="sxs-lookup"><span data-stu-id="318c2-127">The only difference between the duplicate fixed asset cards is the number assigned to each fixed asset.</span></span>|  

9. <span data-ttu-id="318c2-128">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="318c2-128">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="318c2-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="318c2-129">See Also</span></span>  
 [<span data-ttu-id="318c2-130">Cespiti</span><span class="sxs-lookup"><span data-stu-id="318c2-130">Fixed Assets</span></span>](../../fa-manage.md)  
 [<span data-ttu-id="318c2-131">Cespiti italiani</span><span class="sxs-lookup"><span data-stu-id="318c2-131">Italian Fixed Assets</span></span>](italian-fixed-assets.md)
