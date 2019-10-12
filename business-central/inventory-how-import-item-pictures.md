---
title: Importazione di numerose immagini articolo da un file ZIP| Microsoft Docs
description: È possibile importare più immagini articolo contemporaneamente. Assegnare ai file immagine dei nomi che corrispondono ai numeri degli articoli, comprimere i file in un file zip, quindi utilizzare la pagina Importa immagini articolo per gestire le immagini articolo da importare.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cfb80821177c0860413526b5bc529fa1bdeedf7b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309846"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="daf80-104">Importare molteplici immagini articolo</span><span class="sxs-lookup"><span data-stu-id="daf80-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="daf80-105">È possibile importare più immagini articolo contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="daf80-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="daf80-106">Assegnare ai file immagine dei nomi che corrispondono ai numeri degli articoli, comprimere i file in un file ZIP, quindi utilizzare la pagina **Importa immagini articolo** per gestire le immagini articolo da importare.</span><span class="sxs-lookup"><span data-stu-id="daf80-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="daf80-107">Tutti i formati di file comuni sono supportati.</span><span class="sxs-lookup"><span data-stu-id="daf80-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="daf80-108">Per denominare i file immagine con i nile degli articoli e prepare il file ZIP</span><span class="sxs-lookup"><span data-stu-id="daf80-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="daf80-109">Nella posizione in cui le immagini articolo sono archiviate, assegnare un nome a ciascun file in base al numero dell'articolo correlato.</span><span class="sxs-lookup"><span data-stu-id="daf80-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="daf80-110">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="daf80-110">For example:</span></span>

    |<span data-ttu-id="daf80-111">Nr. Articolo</span><span class="sxs-lookup"><span data-stu-id="daf80-111">Item No.</span></span>|<span data-ttu-id="daf80-112">Nome file</span><span class="sxs-lookup"><span data-stu-id="daf80-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="daf80-113">1000</span><span class="sxs-lookup"><span data-stu-id="daf80-113">1000</span></span>|<span data-ttu-id="daf80-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="daf80-114">1000.bmp</span></span>|
    |<span data-ttu-id="daf80-115">1001</span><span class="sxs-lookup"><span data-stu-id="daf80-115">1001</span></span>|<span data-ttu-id="daf80-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="daf80-116">1001.bmp</span></span>|
    |<span data-ttu-id="daf80-117">1002</span><span class="sxs-lookup"><span data-stu-id="daf80-117">1002</span></span>|<span data-ttu-id="daf80-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="daf80-118">1002.bmp</span></span>|

2. <span data-ttu-id="daf80-119">Comprimere tutti i file in un file ZIP.</span><span class="sxs-lookup"><span data-stu-id="daf80-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="daf80-120">Ad esempio, in Windows Explorer, selezionare i file, quindi scegliere **Invia a**, **Cartella compressa**.</span><span class="sxs-lookup"><span data-stu-id="daf80-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="daf80-121">Per importare immagini articolo</span><span class="sxs-lookup"><span data-stu-id="daf80-121">To import item pictures</span></span>
1. <span data-ttu-id="daf80-122">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup magazzino** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="daf80-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="daf80-123">Scegliere l'azione **Importa immagini articolo**.</span><span class="sxs-lookup"><span data-stu-id="daf80-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="daf80-124">Nel campo **Selezionare un file zip**, selezionare la cartella ZIP pertinente quindi scegliere il pulsante **Apri**.</span><span class="sxs-lookup"><span data-stu-id="daf80-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="daf80-125">Una riga per ciascun articolo e immagine viene creata nella pagina **Importa immagini articolo**.</span><span class="sxs-lookup"><span data-stu-id="daf80-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="daf80-126">Per le schede articolo che hanno già un'immagine, la casella di controllo **L'immagine esiste già** è selezionata.</span><span class="sxs-lookup"><span data-stu-id="daf80-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="daf80-127">Se non si desidera sostituire alcuna immagine esistente, deselezionare la casella di controllo **Sostituisci immagini**.</span><span class="sxs-lookup"><span data-stu-id="daf80-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="daf80-128">Se non si desidera sostituire singole immagini esistenti, eliminare le righe in questione.</span><span class="sxs-lookup"><span data-stu-id="daf80-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="daf80-129">Scegliere l'azione **Importa immagini**.</span><span class="sxs-lookup"><span data-stu-id="daf80-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="daf80-130">Il campo **Stato importazione** viene aggiornato per indicare se l'importazione di un'immagine è stata ignorata o completata.</span><span class="sxs-lookup"><span data-stu-id="daf80-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="daf80-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="daf80-131">See Also</span></span>
[<span data-ttu-id="daf80-132">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="daf80-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="daf80-133">Creazione di numerazioni</span><span class="sxs-lookup"><span data-stu-id="daf80-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="daf80-134">Magazzino</span><span class="sxs-lookup"><span data-stu-id="daf80-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="daf80-135">Acquisti</span><span class="sxs-lookup"><span data-stu-id="daf80-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="daf80-136">Vendite</span><span class="sxs-lookup"><span data-stu-id="daf80-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="daf80-137">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="daf80-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
