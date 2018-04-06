---
title: Modificare l'aspetto di un report selezionando un layout diverso | Documenti Microsoft
description: "È possibile utilizzare diversi layout per un report e passate tra i layout per modificare l'aspetto di un report."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cea5e41e53106fafdaaf3d3f59e50d03da953f87
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="d9350-103">Modificare il layout attualmente utilizzato in un report</span><span class="sxs-lookup"><span data-stu-id="d9350-103">Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="d9350-104">Un report può essere impostato con diversi layout di report, che è possibile alternare a seconda delle necessità.</span><span class="sxs-lookup"><span data-stu-id="d9350-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="d9350-105">In base ai layout disponibili per un report, è possibile scegliere di utilizzare un layout di report RDLC o Word predefinito o un layout personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d9350-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="d9350-106">Per ulteriori informazioni sui layout di report RDLC e Word, sui layout personalizzati integrati e altro ancora, vedere [Gestire i layout dei report](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="d9350-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="d9350-107">Per modificare il layout utilizzato in un report</span><span class="sxs-lookup"><span data-stu-id="d9350-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="d9350-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Selezione layout report**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d9350-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="d9350-109">Nella finestra **Selezione layout report** sono elencati tutti i report disponibili per la società che è specificata nel campo Società nella parte superiore della finestra.</span><span class="sxs-lookup"><span data-stu-id="d9350-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="d9350-110">Il campo Layout selezionato specifica il layout che attualmente è utilizzato nel report.</span><span class="sxs-lookup"><span data-stu-id="d9350-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="d9350-111">Impostare il campo **Società** nella parte superiore della finestra alla società che include il report.</span><span class="sxs-lookup"><span data-stu-id="d9350-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="d9350-112">Per modificare il layout utilizzato da un report, nella riga del report nell'elenco, impostare il campo **Layout selezionato** su una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="d9350-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="d9350-113">RDLC (predefinito) utilizza nel report il layout di report RDLC integrato.</span><span class="sxs-lookup"><span data-stu-id="d9350-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="d9350-114">Word (predefinito) utilizza nel report il layout di report Word integrato.</span><span class="sxs-lookup"><span data-stu-id="d9350-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="d9350-115">Personalizzato utilizza nel report un layout personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d9350-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="d9350-116">È possibile visualizzare i layout personalizzati disponibili per il report nel Dettaglio informazioni Parte di layout report.</span><span class="sxs-lookup"><span data-stu-id="d9350-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="d9350-117">Se non esistono layout personalizzati per il report, è necessario innanzitutto creare uno.</span><span class="sxs-lookup"><span data-stu-id="d9350-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="d9350-118">Se si seleziona questa opzione, andare alla procedura descritta di seguito per specificare il layout personalizzato da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d9350-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="d9350-119">Se si sceglie **RDLC (predefinito)** o **Word (predefinito)** e si visualizza un messaggio di errore che indica che il report non dispone di un layout del tipo specificato, è necessario selezionare un'altra opzione di layout o creare un layout di report personalizzato del tipo che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d9350-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="d9350-120">Se è stato selezionato un layout di report RDLC o Word predefinito, non sono necessarie ulteriori azioni e il layout verrà utilizzato alla successiva esecuzione del report.</span><span class="sxs-lookup"><span data-stu-id="d9350-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="d9350-121">Per specificare un layout personalizzato in un report</span><span class="sxs-lookup"><span data-stu-id="d9350-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="d9350-122">Specificare quale layout personalizzato utilizzare nel report dalla finestra **Layout report personalizzati**.</span><span class="sxs-lookup"><span data-stu-id="d9350-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="d9350-123">Se la finestra **Layout report personalizzati** non è aperta, nel campo **Descrizione layout report** scegliere il pulsante di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d9350-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="d9350-124">Nella finestra **Layout report personalizzati** selezionare la riga di layout personalizzato che si desidera utilizzare, quindi chiudere la finestra.</span><span class="sxs-lookup"><span data-stu-id="d9350-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="d9350-125">Verrà visualizzata nuovamente la finestra **Selezione layout report**.</span><span class="sxs-lookup"><span data-stu-id="d9350-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="d9350-126">Il nome del layout personalizzato selezionato viene visualizzato nel campo **Descrizione layout personalizzato**.</span><span class="sxs-lookup"><span data-stu-id="d9350-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="d9350-127">Il layout personalizzato verrà utilizzato la volta successiva che si esegue il report.</span><span class="sxs-lookup"><span data-stu-id="d9350-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9350-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9350-128">See Also</span></span>
[<span data-ttu-id="d9350-129">Gestione dei layout di report</span><span class="sxs-lookup"><span data-stu-id="d9350-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="d9350-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9350-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

