---
title: 'Procedura: Impostazione dell''ammortamento compresso dei cespiti'
description: "È possibile comprimere l'ammortamento dei cespiti in sottoclassi e decidere di visualizzare solo la somma totale per sottoclasse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 653867f64b54bd8bf6ec4fff75d233c8f342b9d1
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-compressed-depreciation-of-fixed-assets"></a><span data-ttu-id="bd8be-103">Impostazione dell'ammortamento compresso dei cespiti</span><span class="sxs-lookup"><span data-stu-id="bd8be-103">Set Up Compressed Depreciation of Fixed Assets</span></span>
<span data-ttu-id="bd8be-104">È possibile comprimere l'ammortamento dei cespiti in sottoclassi e decidere di visualizzare solo la somma totale per sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="bd8be-104">You can compress fixed asset depreciation into subclasses and choose to display only the total sum by subclass.</span></span> <span data-ttu-id="bd8be-105">È possibile decidere di registrare solo i totali di ammortamento raggruppati per categoria.</span><span class="sxs-lookup"><span data-stu-id="bd8be-105">You can choose to post only the depreciation totals of assets that are grouped by category.</span></span> <span data-ttu-id="bd8be-106">Questo è particolarmente importante per le società che dispongono di più cespiti suddivisi in molti articoli singoli.</span><span class="sxs-lookup"><span data-stu-id="bd8be-106">This is particularly important for companies that have multiple fixed assets divided into many individual items.</span></span>  

<span data-ttu-id="bd8be-107">Durante il calcolo dell'ammortamento, viene generata una riga per ogni cespite.</span><span class="sxs-lookup"><span data-stu-id="bd8be-107">When you calculate depreciation, one line is generated for each fixed asset.</span></span> <span data-ttu-id="bd8be-108">Ad esempio, se si registrano gli ammortamenti per 100 cespiti, vengono generate 100 righe che vengono registrate sia nella contabilità generale che nei movimenti contabili cespiti.</span><span class="sxs-lookup"><span data-stu-id="bd8be-108">For example, posting depreciations for 100 assets generates 100 lines that are posted to both the general ledger and fixed asset ledger entries.</span></span>  

## <a name="to-set-up-compressed-depreciation-of-fixed-assets"></a><span data-ttu-id="bd8be-109">Per impostare l'ammortamento compresso dei cespiti</span><span class="sxs-lookup"><span data-stu-id="bd8be-109">To set up compressed depreciation of fixed assets</span></span>  

1.  <span data-ttu-id="bd8be-110">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registri beni ammortizz.**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bd8be-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Depreciation Books**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bd8be-111">Nella finestra **Lista reg. reni ammortizz.**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="bd8be-111">In the **Depreciation Book List** window, select the relevant depreciation book, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="bd8be-112">Per registrare solo i totali dell'ammortamento delle risorse raggruppate per categoria, nella finestra **Scheda registro beni ammortizz.**, nella Scheda dettaglio **Generale**, selezionare la casella di controllo **Raggruppa scritture amm.**.</span><span class="sxs-lookup"><span data-stu-id="bd8be-112">To post only the depreciation totals of assets that are grouped by category, in the **Depreciation Book Card** window, on the **General** FastTab, select the **Compress Depreciation** check box.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="bd8be-113">Verranno compresse più righe di ammortamento nella contabilità generale e visualizzate in un unico movimento suddiviso per categorie di cespiti.</span><span class="sxs-lookup"><span data-stu-id="bd8be-113">Multiple depreciation lines are then compressed in the general ledger and are displayed in a single entry that is divided by fixed asset categories.</span></span>  

4.  <span data-ttu-id="bd8be-114">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd8be-114">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd8be-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd8be-115">See Also</span></span>  
 <span data-ttu-id="bd8be-116">[Impostare l'ammortamento dei cespiti](../../fa-how-setup-depreciation.md) </span><span class="sxs-lookup"><span data-stu-id="bd8be-116">[Set Up Fixed Asset Depreciation](../../fa-how-setup-depreciation.md) </span></span>  
 <span data-ttu-id="bd8be-117">[Cespiti italiani](italian-fixed-assets.md) </span><span class="sxs-lookup"><span data-stu-id="bd8be-117">[Italian Fixed Assets](italian-fixed-assets.md) </span></span>  
 <span data-ttu-id="bd8be-118">[Impostare metodi di ammortamento alternativi](how-to-set-up-alternate-depreciation-methods.md) </span><span class="sxs-lookup"><span data-stu-id="bd8be-118">[Set Up Alternate Depreciation Methods](how-to-set-up-alternate-depreciation-methods.md) </span></span>  
 <span data-ttu-id="bd8be-119">[Creare più schede cespite](how-to-create-multiple-fixed-asset-cards.md) </span><span class="sxs-lookup"><span data-stu-id="bd8be-119">[Create Multiple Fixed Asset Cards](how-to-create-multiple-fixed-asset-cards.md) </span></span>  
 [<span data-ttu-id="bd8be-120">Stampare report dei registri dei beni ammortizzabili</span><span class="sxs-lookup"><span data-stu-id="bd8be-120">Print Depreciation Book Reports</span></span>](how-to-print-depreciation-book-reports.md)

