---
title: Funzionalità di accessibilità
description: Tasti di scelta rapida e altre funzionalità di accessibilità.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1098e0998369e15bd9484ba33b808b9b435b538c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192125"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="5be5b-103">Accessibilità e tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="5be5b-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="5be5b-104">In questo argomento vengono fornite informazioni sulle funzionalità che rendono [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibile per gli utenti con esigenze particolari.</span><span class="sxs-lookup"><span data-stu-id="5be5b-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="5be5b-105">supporta le seguenti funzionalità di accessibilità:</span><span class="sxs-lookup"><span data-stu-id="5be5b-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="5be5b-106">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="5be5b-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="5be5b-107">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="5be5b-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="5be5b-108">Spostamento</span><span class="sxs-lookup"><span data-stu-id="5be5b-108">Navigation</span></span>  

-   <span data-ttu-id="5be5b-109">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="5be5b-109">Headings</span></span>  

-   <span data-ttu-id="5be5b-110">Testo alternativo per le immagini e i collegamenti</span><span class="sxs-lookup"><span data-stu-id="5be5b-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="5be5b-111">Supporto per le tecnologie per l'accessibilità comuni</span><span class="sxs-lookup"><span data-stu-id="5be5b-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

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

##  <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="5be5b-112">Spostamento</span><span class="sxs-lookup"><span data-stu-id="5be5b-112">Navigation</span></span>  
 <span data-ttu-id="5be5b-113">È possibile spostarsi tra schede e azioni nella barra multifunzione, elementi nella barra di spostamento e altri comandi nelle pagine e nei report di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="5be5b-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="5be5b-114">Per spostare lo stato attivo da un comando, scheda o azione all'altro, premere il tasto TAB per spostarsi in avanti.</span><span class="sxs-lookup"><span data-stu-id="5be5b-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="5be5b-115">Premere MAIUSC + TAB per spostarsi all'indietro.</span><span class="sxs-lookup"><span data-stu-id="5be5b-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="5be5b-116">Utilizzando l'ordine delle schede è inoltre possibile passare, ad esempio, dalla pagina principale del browser alle finestre di dialogo che richiedono conferma o alla pagina di connessione e viceversa.</span><span class="sxs-lookup"><span data-stu-id="5be5b-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="headings"></a><a name="Headings"></a> <span data-ttu-id="5be5b-117">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="5be5b-117">Headings</span></span>  
 <span data-ttu-id="5be5b-118">L'origine HTML per il contenuto di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizza tag per aiutare gli utenti della tecnologia per l'accessibilità a comprendere la struttura e il contenuto della pagina.</span><span class="sxs-lookup"><span data-stu-id="5be5b-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="5be5b-119">Ad esempio, nelle pagine di elenchi, le colonne vengono definite in tag TH e le intestazioni di colonna sono impostate con l'attributo TITLE all'interno del tag.</span><span class="sxs-lookup"><span data-stu-id="5be5b-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="5be5b-120">Le didascalie per elementi quali Schede dettaglio, Riquadri Dettaglio informazioni e campi sono incluse nei tag delle intestazioni (H1, H2, H3 e H4).</span><span class="sxs-lookup"><span data-stu-id="5be5b-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="5be5b-121">Immagine e collegamenti</span><span class="sxs-lookup"><span data-stu-id="5be5b-121">Image and Links</span></span>  
 <span data-ttu-id="5be5b-122">Un testo descrittivo per le immagini è impostato con l'attributo ALT all'interno del tag IMG.</span><span class="sxs-lookup"><span data-stu-id="5be5b-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="5be5b-123">Un testo descrittivo per i collegamenti ipertestuali è impostato con l'attributo TITLE all'interno del tag A.</span><span class="sxs-lookup"><span data-stu-id="5be5b-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="5be5b-124">Tecnologie per l'accessibilità</span><span class="sxs-lookup"><span data-stu-id="5be5b-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="5be5b-125">supporta diverse tecnologie per l'accessibilità, ad esempio il contrasto elevato, le utilità per la lettura dello schermo e il software di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="5be5b-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="5be5b-126">Alcune tecnologie per l'accessibilità potrebbero non funzionare correttamente con determinati elementi nelle pagine di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5be5b-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="5be5b-127">Per ulteriori informazioni sull'accessibilità</span><span class="sxs-lookup"><span data-stu-id="5be5b-127">For more accessibility information</span></span>  
<span data-ttu-id="5be5b-128">È possibile trovare informazioni aggiuntive sull'accessibilità con i prodotti Microsoft e le tecnologie per l'accessibilità sul sito Web [Accessibilità di Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="5be5b-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="5be5b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5be5b-129">See Also</span></span>
[<span data-ttu-id="5be5b-130">Introduzione</span><span class="sxs-lookup"><span data-stu-id="5be5b-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="5be5b-131">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5be5b-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5be5b-132">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="5be5b-132">Frequently Asked Questions</span></span>](across-faq.md)  
