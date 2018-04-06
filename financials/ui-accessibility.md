---
title: "Funzionalità di accessibilità"
description: "Tasti di scelta rapida e altre funzionalità di accessibilità."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/04/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: a9e622dbf9b9edf5e74386dd5c651d7b585d3b46
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="accessibility-and-keyboard-shortcuts-in-included365finincludesd365finmdmd"></a><span data-ttu-id="6460d-103">Accessibilità e tasti di scelta rapida in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="6460d-103">Accessibility and Keyboard Shortcuts in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="6460d-104">In questo argomento vengono fornite informazioni sulle funzionalità che rendono [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibile per gli utenti con esigenze particolari.</span><span class="sxs-lookup"><span data-stu-id="6460d-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6460d-105"> supporta le seguenti funzionalità di accessibilità:</span><span class="sxs-lookup"><span data-stu-id="6460d-105"> supports the following accessibility features:</span></span>  

-   <span data-ttu-id="6460d-106">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="6460d-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="6460d-107">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="6460d-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="6460d-108">Spostamento</span><span class="sxs-lookup"><span data-stu-id="6460d-108">Navigation</span></span>  

-   <span data-ttu-id="6460d-109">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="6460d-109">Headings</span></span>  

-   <span data-ttu-id="6460d-110">Testo alternativo per le immagini e i collegamenti</span><span class="sxs-lookup"><span data-stu-id="6460d-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="6460d-111">Supporto per le tecnologie per l'accessibilità comuni</span><span class="sxs-lookup"><span data-stu-id="6460d-111">Support for common assistive technologies</span></span>  

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

##  <a name="Navigation"></a> <span data-ttu-id="6460d-112">Spostamento</span><span class="sxs-lookup"><span data-stu-id="6460d-112">Navigation</span></span>  
 <span data-ttu-id="6460d-113">È possibile spostarsi tra schede e azioni nella barra multifunzione, elementi nel riquadro di spostamento e altri comandi nelle pagine e nei report di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="6460d-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation pane, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="6460d-114">Per spostare lo stato attivo da un comando, scheda o azione all'altro, premere il tasto TAB per spostarsi in avanti.</span><span class="sxs-lookup"><span data-stu-id="6460d-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="6460d-115">Premere MAIUSC + TAB per spostarsi all'indietro.</span><span class="sxs-lookup"><span data-stu-id="6460d-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="6460d-116">Utilizzando l'ordine delle schede è inoltre possibile passare, ad esempio, dalla finestra principale del browser alle finestre di dialogo che richiedono conferma o alla finestra di connessione e viceversa.</span><span class="sxs-lookup"><span data-stu-id="6460d-116">By using the tab order, you can also switch between the main browser window and dialog boxes that request confirmation, for example, or the login window.</span></span>  

##  <a name="Headings"></a> <span data-ttu-id="6460d-117">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="6460d-117">Headings</span></span>  
 <span data-ttu-id="6460d-118">L'origine HTML per il contenuto di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizza tag per aiutare gli utenti della tecnologia per l'accessibilità a comprendere la struttura e il contenuto della pagina.</span><span class="sxs-lookup"><span data-stu-id="6460d-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="6460d-119">Ad esempio, nelle pagine di elenchi, le colonne vengono definite in tag TH e le intestazioni di colonna sono impostate con l'attributo TITLE all'interno del tag.</span><span class="sxs-lookup"><span data-stu-id="6460d-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="6460d-120">Le didascalie per elementi quali Schede dettaglio, Riquadri Dettaglio informazioni e campi sono incluse nei tag delle intestazioni (H1, H2, H3 e H4).</span><span class="sxs-lookup"><span data-stu-id="6460d-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="Images"></a> <span data-ttu-id="6460d-121">Immagine e collegamenti</span><span class="sxs-lookup"><span data-stu-id="6460d-121">Image and Links</span></span>  
 <span data-ttu-id="6460d-122">Un testo descrittivo per le immagini è impostato con l'attributo ALT all'interno del tag IMG.</span><span class="sxs-lookup"><span data-stu-id="6460d-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="6460d-123">Un testo descrittivo per i collegamenti ipertestuali è impostato con l'attributo TITLE all'interno del tag A.</span><span class="sxs-lookup"><span data-stu-id="6460d-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="AssistiveTech"></a> <span data-ttu-id="6460d-124">Tecnologie per l'accessibilità</span><span class="sxs-lookup"><span data-stu-id="6460d-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6460d-125"> supporta diverse tecnologie per l'accessibilità, ad esempio il contrasto elevato, le utilità per la lettura dello schermo e il software di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="6460d-125"> supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="6460d-126">Alcune tecnologie per l'accessibilità potrebbero non funzionare correttamente con determinati elementi nelle pagine di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6460d-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="6460d-127">Per ulteriori informazioni sull'accessibilità</span><span class="sxs-lookup"><span data-stu-id="6460d-127">For more accessibility information</span></span>  
<span data-ttu-id="6460d-128">È possibile trovare informazioni aggiuntive sull'accessibilità con i prodotti Microsoft e le tecnologie per l'accessibilità sul sito Web [Accessibilità di Microsoft](http://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="6460d-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](http://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="6460d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6460d-129">See Also</span></span>
<span data-ttu-id="6460d-130">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="6460d-130">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="6460d-131">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6460d-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6460d-132">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="6460d-132">Frequently Asked Questions</span></span>](across-faq.md)  

