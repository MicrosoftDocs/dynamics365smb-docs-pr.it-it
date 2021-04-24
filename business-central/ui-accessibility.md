---
title: Funzionalità di accessibilità
description: Tasti di scelta rapida e altre funzionalità di accessibilità.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c303c39850e22d3df375838d42703133428b4c7d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772356"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="23fed-103">Accessibilità e tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="23fed-103">Accessibility and Keyboard Shortcuts</span></span>

<span data-ttu-id="23fed-104">In questo argomento vengono fornite informazioni sulle funzionalità che rendono [!INCLUDE[prod_short](includes/prod_short.md)] disponibile per gli utenti con esigenze particolari.</span><span class="sxs-lookup"><span data-stu-id="23fed-104">This topic provides information about the features that make [!INCLUDE[prod_short](includes/prod_short.md)] readily available to people with disabilities.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="23fed-105">supporta le seguenti funzionalità di accessibilità:</span><span class="sxs-lookup"><span data-stu-id="23fed-105">supports the following accessibility features:</span></span>  

- <span data-ttu-id="23fed-106">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="23fed-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="23fed-107">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="23fed-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

- <span data-ttu-id="23fed-108">Spostamento</span><span class="sxs-lookup"><span data-stu-id="23fed-108">Navigation</span></span>  

- <span data-ttu-id="23fed-109">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="23fed-109">Headings</span></span>  

- <span data-ttu-id="23fed-110">Testo alternativo per le immagini e i collegamenti</span><span class="sxs-lookup"><span data-stu-id="23fed-110">Alternative text for images and links</span></span>  

- <span data-ttu-id="23fed-111">Supporto per le tecnologie per l'accessibilità comuni</span><span class="sxs-lookup"><span data-stu-id="23fed-111">Support for common assistive technologies</span></span>  

- <span data-ttu-id="23fed-112">Utilizzare i tasti di scelta rapida per ingrandire o ridurre qualsiasi pagina</span><span class="sxs-lookup"><span data-stu-id="23fed-112">Use keyboard shortcuts to zoom in or out on any page</span></span>

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[prod_short](includes/prod_short.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

## <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="23fed-113">Spostamento</span><span class="sxs-lookup"><span data-stu-id="23fed-113">Navigation</span></span>  
 <span data-ttu-id="23fed-114">È possibile spostarsi tra schede e azioni nella barra multifunzione, elementi nella barra di spostamento e altri comandi nelle pagine e nei report di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="23fed-114">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[prod_short](includes/prod_short.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="23fed-115">Per spostare lo stato attivo da un comando, scheda o azione all'altro, premere il tasto TAB per spostarsi in avanti.</span><span class="sxs-lookup"><span data-stu-id="23fed-115">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="23fed-116">Premere MAIUSC + TAB per spostarsi all'indietro.</span><span class="sxs-lookup"><span data-stu-id="23fed-116">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="23fed-117">Utilizzando l'ordine delle schede è inoltre possibile passare, ad esempio, dalla pagina principale del browser alle finestre di dialogo che richiedono conferma o alla pagina di connessione e viceversa.</span><span class="sxs-lookup"><span data-stu-id="23fed-117">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

## <a name="headings-in-content"></a><a name="Headings"></a> <span data-ttu-id="23fed-118">Intestazioni nel contenuto</span><span class="sxs-lookup"><span data-stu-id="23fed-118">Headings in Content</span></span>
 
 <span data-ttu-id="23fed-119">L'origine HTML per il contenuto di [!INCLUDE[prod_short](includes/prod_short.md)] utilizza tag per aiutare gli utenti della tecnologia per l'accessibilità a comprendere la struttura e il contenuto della pagina.</span><span class="sxs-lookup"><span data-stu-id="23fed-119">The HTML source for [!INCLUDE[prod_short](includes/prod_short.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="23fed-120">Ad esempio, nelle pagine di elenchi, le colonne vengono definite in tag TH e le intestazioni di colonna sono impostate con l'attributo TITLE all'interno del tag.</span><span class="sxs-lookup"><span data-stu-id="23fed-120">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="23fed-121">Le didascalie per elementi quali Schede dettaglio, Riquadri Dettaglio informazioni e campi sono incluse nei tag delle intestazioni (H1, H2, H3 e H4).</span><span class="sxs-lookup"><span data-stu-id="23fed-121">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

## <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="23fed-122">Immagine e collegamenti</span><span class="sxs-lookup"><span data-stu-id="23fed-122">Image and Links</span></span>

 <span data-ttu-id="23fed-123">Un testo descrittivo per le immagini è impostato con l'attributo ALT all'interno del tag IMG.</span><span class="sxs-lookup"><span data-stu-id="23fed-123">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="23fed-124">Un testo descrittivo per i collegamenti ipertestuali è impostato con l'attributo TITLE all'interno del tag A.</span><span class="sxs-lookup"><span data-stu-id="23fed-124">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="23fed-125">Tecnologie per l'accessibilità</span><span class="sxs-lookup"><span data-stu-id="23fed-125">Assistive Technologies</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="23fed-126">supporta diverse tecnologie per l'accessibilità, ad esempio il contrasto elevato, le utilità per la lettura dello schermo e il software di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="23fed-126">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="23fed-127">Alcune tecnologie per l'accessibilità potrebbero non funzionare correttamente con determinati elementi nelle pagine di [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="23fed-127">Some assistive technologies may not work well with certain elements in [!INCLUDE[prod_short](includes/prod_short.md)] pages.</span></span>  

## <a name="zoom"></a><a name="zoom"></a> <span data-ttu-id="23fed-128">Zoom</span><span class="sxs-lookup"><span data-stu-id="23fed-128">Zoom</span></span>

<span data-ttu-id="23fed-129">La maggior parte dei browser utilizza tasti di scelta rapida standard per ingrandire e ridurre la pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="23fed-129">Most browsers use standard keyboard shortcuts to zoom in and out on the current page.</span></span> <span data-ttu-id="23fed-130">Questi tasti di scelta rapida non sono specifici per [!INCLUDE [prod_short](includes/prod_short.md)], ma funzionano quando si utilizza [!INCLUDE [prod_short](includes/prod_short.md)] in un browser.</span><span class="sxs-lookup"><span data-stu-id="23fed-130">These keyboard shortcuts are not specific to [!INCLUDE [prod_short](includes/prod_short.md)], but they work when you use [!INCLUDE [prod_short](includes/prod_short.md)] in a browser.</span></span> <span data-ttu-id="23fed-131">Per un elenco dei tasti di scelta rapida supportati, vedere [Tasti di scelta rapida per ingrandire e ridurre](keyboard-shortcuts.md#zoomshortcuts).</span><span class="sxs-lookup"><span data-stu-id="23fed-131">For a list of supported keyboard shortcuts, see [Keyboard Shortcuts for Zooming In and Out](keyboard-shortcuts.md#zoomshortcuts).</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="23fed-132">Per ulteriori informazioni sull'accessibilità</span><span class="sxs-lookup"><span data-stu-id="23fed-132">For more accessibility information</span></span>

<span data-ttu-id="23fed-133">È possibile trovare informazioni aggiuntive sull'accessibilità con i prodotti Microsoft e le tecnologie per l'accessibilità sul sito Web [Accessibilità di Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="23fed-133">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="23fed-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="23fed-134">See Also</span></span>

[<span data-ttu-id="23fed-135">Preparazione al business</span><span class="sxs-lookup"><span data-stu-id="23fed-135">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="23fed-136">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="23fed-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="23fed-137">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="23fed-137">Frequently Asked Questions</span></span>](across-faq.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]