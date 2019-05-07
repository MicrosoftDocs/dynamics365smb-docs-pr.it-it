---
title: Come immettere dati nei campi| Microsoft Docs
description: Ottenere informazioni su funzionalità generali che consentono di immettere dati nei campi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "929075"
---
# <a name="entering-data"></a><span data-ttu-id="8f08c-103">Immissione di dati</span><span class="sxs-lookup"><span data-stu-id="8f08c-103">Entering Data</span></span>

<span data-ttu-id="8f08c-104">Sono disponibili numerose funzionalità generali che consentono di immettere dati più facilmente, più velocemente e in modo più preciso.</span><span class="sxs-lookup"><span data-stu-id="8f08c-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="8f08c-105">In questo articolo sono descritte tutte le funzionalità generali per l'immissione di dati.</span><span class="sxs-lookup"><span data-stu-id="8f08c-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="8f08c-106">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8f08c-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="8f08c-107">Esistono vari tasti di scelta rapida che consentono di lavorare “senza mouse" e velocizzare l'immissione di dati, in particolare con immissioni su larga scala e task di digitazione ripetitive.</span><span class="sxs-lookup"><span data-stu-id="8f08c-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="8f08c-108">Per ulteriori informazioni sui tasti di scelta rapida, vedere [Tasti di scelta rapida](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="8f08c-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="8f08c-109">Alcuni dei tasti di scelta rapida vengono discussi in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="8f08c-110">Accelerazione dell'immissione di dati utilizzando Accesso rapido</span><span class="sxs-lookup"><span data-stu-id="8f08c-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="8f08c-111">Accesso rapido è una funzionalità concepita per l'immissione di dati utilizzando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="8f08c-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="8f08c-112">La funzionalità di Accesso rapido viene utilizzata nei campi (come nelle pagine scheda) e negli elenchi (righe e colonne).</span><span class="sxs-lookup"><span data-stu-id="8f08c-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="8f08c-113">È utile quando si eseguono task di digitazione ripetitive che richiedono la creazione di più record in sequenza, ad esempio un batch di ordini di vendita o la registrazione di nuovi articoli.</span><span class="sxs-lookup"><span data-stu-id="8f08c-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="8f08c-114">È possibile che si abbia già una certa familiarità nell'utilizzo del tasto TAB per spostarsi da un campo in una pagina al campo modificabile successivo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="8f08c-115">Uno svantaggio inerente all'utilizzo del tasto TAB è che sposta sempre lo stato attivo al campo seguente in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="8f08c-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="8f08c-116">Accesso rapido funziona in un altro modo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="8f08c-117">Con Accesso rapido, si utilizza il tasto INVIO per spostarsi solo nei campi a cui si è interessati, ignorando i campi non modificabili e i campi che in genere non vengono compilati.</span><span class="sxs-lookup"><span data-stu-id="8f08c-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="8f08c-118">È possibile che questo comportamento sia già stato osservato in alcune pagine.</span><span class="sxs-lookup"><span data-stu-id="8f08c-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="8f08c-119">Questo perché l'applicazione designa già i campi da includere quando si preme INVIO e quali ignorare.</span><span class="sxs-lookup"><span data-stu-id="8f08c-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="8f08c-120">È possibile personalizzare Accesso rapido personalizzando l'area di lavoro e ottimizzando il modo di immissione dei dati in ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="8f08c-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="8f08c-121">Funzionamento di Accesso rapido</span><span class="sxs-lookup"><span data-stu-id="8f08c-121">How Quick Entry Works</span></span>

<span data-ttu-id="8f08c-122">Ogni campo può essere contrassegnato come *incluso in Accesso rapido* o *escluso da Accesso rapido*.</span><span class="sxs-lookup"><span data-stu-id="8f08c-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="8f08c-123">I campi inclusi in Accesso rapido verranno inclusi nel percorso quando si preme INVIO; i campi che sono esclusi da Accesso rapido, non lo saranno.</span><span class="sxs-lookup"><span data-stu-id="8f08c-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="8f08c-124">Al termine dell'immissione dei dati in un campo, premere semplicemente INVIO per confermare le modifiche e accedere al campo seguente.</span><span class="sxs-lookup"><span data-stu-id="8f08c-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="8f08c-125">Per invertire la direzione e accedere al campo precedente, premere MAIUSC+INVIO.</span><span class="sxs-lookup"><span data-stu-id="8f08c-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="8f08c-126">Per ulteriori informazioni sui tasti di scelta rapida, vedere [Tasti di scelta rapida di Accesso rapido](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="8f08c-126">For more information about shortcuts, see [Quick Entry keyboard shortcuts](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="8f08c-127">Suggerimenti e consigli</span><span class="sxs-lookup"><span data-stu-id="8f08c-127">Tips and tricks</span></span>
<span data-ttu-id="8f08c-128">Di seguito vengono fornite alcune informazioni utili sull'utilizzo di Accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="8f08c-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="8f08c-129">È disponibile per qualsiasi campo modificabile.</span><span class="sxs-lookup"><span data-stu-id="8f08c-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="8f08c-130">Funziona anche con colonne e righe.</span><span class="sxs-lookup"><span data-stu-id="8f08c-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="8f08c-131">Non impedisce l'accesso ad altri elementi di una pagina, ad esempio le azioni.</span><span class="sxs-lookup"><span data-stu-id="8f08c-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="8f08c-132">Questi sono sempre accessibili utilizzando TAB e MAIUSC+TAB.</span><span class="sxs-lookup"><span data-stu-id="8f08c-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="8f08c-133">Le Schede dettaglio non devono essere espanse per utilizzare Accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="8f08c-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="8f08c-134">Se il campo Accesso rapido successivo si trova in una Scheda dettaglio compressa, quella scheda verrà espansa automaticamente e lo stato attivo sarà sul campo designato.</span><span class="sxs-lookup"><span data-stu-id="8f08c-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="8f08c-135">Il funzionamento di Accesso rapido è indipendente dal fatto che i campi siano obbligatori o meno.</span><span class="sxs-lookup"><span data-stu-id="8f08c-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="8f08c-136">È quindi opportuno assicurarsi che i campi obbligatori siano inclusi in Accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="8f08c-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="8f08c-137">Per impostazione predefinita, la maggior parte dei campi vengono automaticamente inclusi in Accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="8f08c-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="8f08c-138">Quindi inizialmente la task escluderà probabilmente i campi da Accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="8f08c-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="8f08c-139">Come modificare i campi Accesso rapido</span><span class="sxs-lookup"><span data-stu-id="8f08c-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="8f08c-140">Per modificare quali campi sono inclusi o esclusi da Accesso rapido in una pagina, si utilizza la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="8f08c-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="8f08c-141">Avviare la personalizzazione selezionando l'icona ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente") e quindi **Personalizza**.</span><span class="sxs-lookup"><span data-stu-id="8f08c-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="8f08c-142">Selezionare un campo che si desidera modificare, o negli elenchi, selezionare l'intestazione di colonna corrispondente, quindi scegliere **Includi in Accesso rapido** o **Escludi da Accesso rapido**.</span><span class="sxs-lookup"><span data-stu-id="8f08c-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="8f08c-143">Per ulteriori informazioni sulla personalizzazione, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="8f08c-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="8f08c-144">Campi obbligatori</span><span class="sxs-lookup"><span data-stu-id="8f08c-144">Mandatory Fields</span></span>

<span data-ttu-id="8f08c-145">Quando si immettono dati nelle pagine, alcuni campi sono contrassegnati con un asterisco rosso.</span><span class="sxs-lookup"><span data-stu-id="8f08c-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="8f08c-146">L'asterisco rosso significa che il campo deve essere compilato per completare un determinato processo che utilizza il campo, ad esempio registrare una transazione che utilizza il valore nel campo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="8f08c-147">Anche se il campo contiene un asterisco rosso, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="8f08c-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="8f08c-148">L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="8f08c-149">Trovare dati durante la digitazione</span><span class="sxs-lookup"><span data-stu-id="8f08c-149">Finding Data As You Type</span></span>

 <span data-ttu-id="8f08c-150">Quando si inizia a digitare dei caratteri in un campo, un elenco a discesa visualizza i valori di campo possibili.</span><span class="sxs-lookup"><span data-stu-id="8f08c-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="8f08c-151">L'elenco cambia se si digitano ulteriori caratteri ed è possibile selezionare il valore corretto quando viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8f08c-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="8f08c-152">In molti campi è disponibile un pulsante Freccia GIÙ che è possibile selezionare.</span><span class="sxs-lookup"><span data-stu-id="8f08c-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="8f08c-153">Facendo clic sulla freccia, è possibile ottenere un elenco di tutti i dati disponibili in un quel campo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="8f08c-154">Il pulsante ha due funzioni, a seconda del tipo di campo:</span><span class="sxs-lookup"><span data-stu-id="8f08c-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="8f08c-155">Lookup - Vengono visualizzate informazioni di un'altra tabella che possono essere immesse nel campo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="8f08c-156">È possibile selezionare soltanto un dato alla volta.</span><span class="sxs-lookup"><span data-stu-id="8f08c-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="8f08c-157">DropDown - Vengono visualizzate le scelte possibili per il campo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="8f08c-158">È possibile selezionare soltanto una delle opzioni.</span><span class="sxs-lookup"><span data-stu-id="8f08c-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="8f08c-159">Copiare e incollare campi e righe</span><span class="sxs-lookup"><span data-stu-id="8f08c-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="8f08c-160">È possibile copiare una o più righe da un elenco o un singolo campo in una pagina e quindi incollare ciò che è stato copiato nella stessa pagina, in un'altra pagina o in un documento esterno (ad esempio di Microsoft Excel o Outlook).</span><span class="sxs-lookup"><span data-stu-id="8f08c-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="8f08c-161">In breve, per copiare, premere CTRL + C (cmd + C in macOS) sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="8f08c-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="8f08c-162">Per incollare, premere CTRL + V (cmd + V in macOS).</span><span class="sxs-lookup"><span data-stu-id="8f08c-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="8f08c-163">In un elenco, per copiare il campo nella stessa colonna della riga precedente e incollarlo nella riga corrente, premere F8.</span><span class="sxs-lookup"><span data-stu-id="8f08c-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="8f08c-164">Per ulteriori informazioni, vedere [Copiare e incollare in Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="8f08c-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="8f08c-165">Spostamento dello stato attivo sulle voci</span><span class="sxs-lookup"><span data-stu-id="8f08c-165">Focusing on Line Items</span></span>

<span data-ttu-id="8f08c-166">Quando si lavora su documenti che includono la parte Voci, ad esempio un ordine di vendita o una fattura, è possibile passare a un'altra visualizzazione per spostare lo stato attivo solo sulle voci, essenzialmente espandendo la parte Voci affinché occupi l'intera area di lavoro, nascondendo altre parti della pagina ad eccezione dell'area Azioni nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="8f08c-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="8f08c-167">In questo modo si ha una migliore panoramica delle voci e maggiore spazio per utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="8f08c-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="8f08c-168">Ciò è particolarmente utile quando si lavora con elenchi di voci di grandi dimensioni e si desidera un'immissione di dati rapida.</span><span class="sxs-lookup"><span data-stu-id="8f08c-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="8f08c-169">Un altro vantaggio è che fornisce una funzionalità di filtro avanzata, come in altre elenchi, e quindi la ricerca nelle voci diventa più semplice.</span><span class="sxs-lookup"><span data-stu-id="8f08c-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switch-the-focus-on-and-off"></a><span data-ttu-id="8f08c-170">Attivare/disattivare lo stato attivo</span><span class="sxs-lookup"><span data-stu-id="8f08c-170">Switch the Focus On and Off</span></span>

<span data-ttu-id="8f08c-171">Per spostare lo stato attivo sulle voci, selezionare un punto qualsiasi nella parte Voci, quindi scegliere l'![icona Modalità stato attivo](media/focus-mode.png "icona Modalità stato attivo") nell'angolo in alto a destra oppure premere CTRL+MAIUSC+F12.</span><span class="sxs-lookup"><span data-stu-id="8f08c-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="8f08c-172">Per passare di nuovo alla visualizzazione normale, scegliere l'![icona Modalità messa a fuoco](media/focus-mode.png "icona Modalità messa a fuoco") o premere di nuovo CTRL+MAIUSC+F12.</span><span class="sxs-lookup"><span data-stu-id="8f08c-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="8f08c-173">Filtri delle voci</span><span class="sxs-lookup"><span data-stu-id="8f08c-173">Filtering the Line Items</span></span>

<span data-ttu-id="8f08c-174">Per avviare il filtro, selezionare l'![icona riquadro Filtro](media/open-filter-pane-icon.png "Icona riquadro Filtro") nella parte superiore dell'elenco o premere **MAIUSC+F3** per aprire il riquadro Filtro.</span><span class="sxs-lookup"><span data-stu-id="8f08c-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="8f08c-175">il riquadro Filtro viene utilizzato come qualsiasi altro elenco.</span><span class="sxs-lookup"><span data-stu-id="8f08c-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="8f08c-176">Per ulteriori informazioni, vedere [Filtri](ui-enter-criteria-filters.md#Filtering).</span><span class="sxs-lookup"><span data-stu-id="8f08c-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="8f08c-177">I filtri sono particolarmente utili quando si visualizzano e analizzano i documenti più lunghi.</span><span class="sxs-lookup"><span data-stu-id="8f08c-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="8f08c-178">Ad esempio, si supponga di aprire una fattura di vendita registrata e di filtrare le voci per visualizzare tutte quelle che hanno un singolo sconto maggiore del 5% oppure per visualizzare solo accessori per biciclette con la parola “pro" nel nome.</span><span class="sxs-lookup"><span data-stu-id="8f08c-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="8f08c-179">Immettere quantità mediante calcolo</span><span class="sxs-lookup"><span data-stu-id="8f08c-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="8f08c-180">Quando si immettono numeri nei campi numerici come il campo **Quantità** in una riga di registrazione magazzino, è possibile immettere la formula invece della quantità della somma.</span><span class="sxs-lookup"><span data-stu-id="8f08c-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="8f08c-181">Esempi</span><span class="sxs-lookup"><span data-stu-id="8f08c-181">Examples</span></span>  

-   <span data-ttu-id="8f08c-182">Se si immette 19+19, il valore del campo viene calcolato in 38.</span><span class="sxs-lookup"><span data-stu-id="8f08c-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="8f08c-183">Se si immette 41-9, il valore del campo viene calcolato in 32.</span><span class="sxs-lookup"><span data-stu-id="8f08c-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="8f08c-184">Se si immette 12\*4, il valore del campo viene calcolato in 48.</span><span class="sxs-lookup"><span data-stu-id="8f08c-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="8f08c-185">Se si immette 12/4, il valore del campo viene calcolato in 3.</span><span class="sxs-lookup"><span data-stu-id="8f08c-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="8f08c-186">Immettere numeri negativi</span><span class="sxs-lookup"><span data-stu-id="8f08c-186">Entering Negative Numbers</span></span>

<span data-ttu-id="8f08c-187">È possibile immettere numeri negativi in due modi.</span><span class="sxs-lookup"><span data-stu-id="8f08c-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="8f08c-188">Il numero -20,5 può essere immesso come:</span><span class="sxs-lookup"><span data-stu-id="8f08c-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="8f08c-189">-20,5</span><span class="sxs-lookup"><span data-stu-id="8f08c-189">-20.5</span></span>  

    <span data-ttu-id="8f08c-190">oppure</span><span class="sxs-lookup"><span data-stu-id="8f08c-190">or</span></span>
-   <span data-ttu-id="8f08c-191">20,5-</span><span class="sxs-lookup"><span data-stu-id="8f08c-191">20.5-</span></span>  

 <span data-ttu-id="8f08c-192">In entrambi i casi, l'importo verrà registrato come -20,5.</span><span class="sxs-lookup"><span data-stu-id="8f08c-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="8f08c-193">Se l'ultimo carattere dell'espressione è un **+** o un **-**, l'intera espressione verrà registrata con tale segno.</span><span class="sxs-lookup"><span data-stu-id="8f08c-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="8f08c-194">Ad esempio **10-20+** restituirà 10 e non -10.</span><span class="sxs-lookup"><span data-stu-id="8f08c-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="8f08c-195">Immissione di date e ore</span><span class="sxs-lookup"><span data-stu-id="8f08c-195">Entering Dates and Times</span></span>

<span data-ttu-id="8f08c-196">È possibile immettere date e ore in tutti i campi riservati alle date (campi di data).</span><span class="sxs-lookup"><span data-stu-id="8f08c-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="8f08c-197">È possibile immettere date con o senza separatori.</span><span class="sxs-lookup"><span data-stu-id="8f08c-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="8f08c-198">La modalità di immissione di date e ore dipende dalle impostazioni di **Area geografica**.</span><span class="sxs-lookup"><span data-stu-id="8f08c-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="8f08c-199">Per ulteriori informazioni, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8f08c-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="8f08c-200">Immissione di date</span><span class="sxs-lookup"><span data-stu-id="8f08c-200">Entering Dates</span></span>

<span data-ttu-id="8f08c-201">Per i campi di date, è possibile utilizzare Selezione dati, che consente di selezionare una data da un calendario, oppure immettere manualmente le date.</span><span class="sxs-lookup"><span data-stu-id="8f08c-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="8f08c-202">Questa sezione fornisce una breve panoramica della modalità di immissione di date.</span><span class="sxs-lookup"><span data-stu-id="8f08c-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="8f08c-203">Per ulteriori informazioni, vedere [Utilizzo di date e orari del calendario](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="8f08c-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="8f08c-204">Per l'immissione manuale di date, è possibile due, quattro, sei o otto cifre:</span><span class="sxs-lookup"><span data-stu-id="8f08c-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="8f08c-205">Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f08c-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="8f08c-206">Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f08c-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="8f08c-207">Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="8f08c-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="8f08c-208">È inoltre possibile immettere una data composta da un giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno. Lu25 o lu25, ad esempio, indica lunedì nella settimana numero 25.</span><span class="sxs-lookup"><span data-stu-id="8f08c-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="8f08c-209">Anziché immettere una data specifica, è possibile immettere uno di questi codici.</span><span class="sxs-lookup"><span data-stu-id="8f08c-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="8f08c-210">Code</span><span class="sxs-lookup"><span data-stu-id="8f08c-210">Code</span></span>|<span data-ttu-id="8f08c-211">Risultato</span><span class="sxs-lookup"><span data-stu-id="8f08c-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="8f08c-212">t</span><span class="sxs-lookup"><span data-stu-id="8f08c-212">t</span></span>|<span data-ttu-id="8f08c-213">Specifica la data odierna (la data di sistema del computer).</span><span class="sxs-lookup"><span data-stu-id="8f08c-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="8f08c-214">P</span><span class="sxs-lookup"><span data-stu-id="8f08c-214">p</span></span>|<span data-ttu-id="8f08c-215">Specifica un periodo contabile, dove `p` indica il primo periodo contabile, `p2` indica il secondo periodo contabile e così via.</span><span class="sxs-lookup"><span data-stu-id="8f08c-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="8f08c-216">w</span><span class="sxs-lookup"><span data-stu-id="8f08c-216">w</span></span>|<span data-ttu-id="8f08c-217">Specifica la data di lavoro impostata nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8f08c-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="8f08c-218">Per modificare la data di lavoro, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8f08c-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="8f08c-219">Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.</span><span class="sxs-lookup"><span data-stu-id="8f08c-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="8f08c-220">c</span><span class="sxs-lookup"><span data-stu-id="8f08c-220">c</span></span>|<span data-ttu-id="8f08c-221">Indica che la data dopo `c`è una data di chiusura, ad esempio `C123101`.</span><span class="sxs-lookup"><span data-stu-id="8f08c-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="8f08c-222">Immissione di ore</span><span class="sxs-lookup"><span data-stu-id="8f08c-222">Entering Times</span></span>

<span data-ttu-id="8f08c-223">Quando si immette l'ora, è possibile inserire qualsiasi separatore tra le unità. L'immissione di un separatore è tuttavia facoltativa.</span><span class="sxs-lookup"><span data-stu-id="8f08c-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="8f08c-224">Non è necessario immettere i minuti, i secondi o l'indicazione AM/PM.</span><span class="sxs-lookup"><span data-stu-id="8f08c-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="8f08c-225">Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8f08c-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="8f08c-226">Movimento</span><span class="sxs-lookup"><span data-stu-id="8f08c-226">Entry</span></span>|<span data-ttu-id="8f08c-227">Interpretazione</span><span class="sxs-lookup"><span data-stu-id="8f08c-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="8f08c-228">5</span><span class="sxs-lookup"><span data-stu-id="8f08c-228">5</span></span>|<span data-ttu-id="8f08c-229">05.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-229">05:00:00</span></span>|  
|<span data-ttu-id="8f08c-230">5:30</span><span class="sxs-lookup"><span data-stu-id="8f08c-230">5:30</span></span>|<span data-ttu-id="8f08c-231">05.30.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-231">05:30:00</span></span>|  
|<span data-ttu-id="8f08c-232">0530</span><span class="sxs-lookup"><span data-stu-id="8f08c-232">0530</span></span>|<span data-ttu-id="8f08c-233">05.30.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-233">05:30:00</span></span>|  
|<span data-ttu-id="8f08c-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="8f08c-234">5:30:5</span></span>|<span data-ttu-id="8f08c-235">05.30.05</span><span class="sxs-lookup"><span data-stu-id="8f08c-235">05:30:05</span></span>|  
|<span data-ttu-id="8f08c-236">053005</span><span class="sxs-lookup"><span data-stu-id="8f08c-236">053005</span></span>|<span data-ttu-id="8f08c-237">05.30.05</span><span class="sxs-lookup"><span data-stu-id="8f08c-237">05:30:05</span></span>|  
|<span data-ttu-id="8f08c-238">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="8f08c-238">5:30:5,50</span></span>|<span data-ttu-id="8f08c-239">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="8f08c-239">05:30:05.5</span></span>|  
|<span data-ttu-id="8f08c-240">053005050</span><span class="sxs-lookup"><span data-stu-id="8f08c-240">053005050</span></span>|<span data-ttu-id="8f08c-241">05.30.05,05</span><span class="sxs-lookup"><span data-stu-id="8f08c-241">05:30:05.05</span></span>|  

 <span data-ttu-id="8f08c-242">Se non si utilizza un separatore, è necessario immettere due cifre per ciascuna unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="8f08c-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="8f08c-243">Immissione di date e ore</span><span class="sxs-lookup"><span data-stu-id="8f08c-243">Entering Datetimes</span></span>

<span data-ttu-id="8f08c-244">Quando si immettono date e ore, è necessario inserire uno spazio tra la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="8f08c-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="8f08c-245">Nella tabella seguente sono elencati i vari formati in cui è possibile immettere la data e l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8f08c-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="8f08c-246">Movimento</span><span class="sxs-lookup"><span data-stu-id="8f08c-246">Entry</span></span>|<span data-ttu-id="8f08c-247">Interpretazione</span><span class="sxs-lookup"><span data-stu-id="8f08c-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="8f08c-248">131202 132455</span><span class="sxs-lookup"><span data-stu-id="8f08c-248">131202 132455</span></span>|<span data-ttu-id="8f08c-249">13/12/02 13.24.55</span><span class="sxs-lookup"><span data-stu-id="8f08c-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="8f08c-250">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="8f08c-250">1-12-02 10</span></span>|<span data-ttu-id="8f08c-251">01/12/02 10.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="8f08c-252">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="8f08c-252">1.12.02 5</span></span>|<span data-ttu-id="8f08c-253">01/12/02 05.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="8f08c-254">1.12.02</span><span class="sxs-lookup"><span data-stu-id="8f08c-254">1.12.02</span></span>|<span data-ttu-id="8f08c-255">01/12/02 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-256">11 12</span><span class="sxs-lookup"><span data-stu-id="8f08c-256">11 12</span></span>|<span data-ttu-id="8f08c-257">11-mese corrente-anno corrente 12.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="8f08c-258">1112 12</span><span class="sxs-lookup"><span data-stu-id="8f08c-258">1112 12</span></span>|<span data-ttu-id="8f08c-259">11-12-anno corrente 12.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="8f08c-260">t o today</span><span class="sxs-lookup"><span data-stu-id="8f08c-260">t or today</span></span>|<span data-ttu-id="8f08c-261">Data odierna 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-262">t time</span><span class="sxs-lookup"><span data-stu-id="8f08c-262">t time</span></span>|<span data-ttu-id="8f08c-263">Ora corrente in data odierna</span><span class="sxs-lookup"><span data-stu-id="8f08c-263">today's date actual time</span></span>|  
|<span data-ttu-id="8f08c-264">t 10:30</span><span class="sxs-lookup"><span data-stu-id="8f08c-264">t 10:30</span></span>|<span data-ttu-id="8f08c-265">Data odierna 10.30.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="8f08c-266">t 3:3:3</span><span class="sxs-lookup"><span data-stu-id="8f08c-266">t 3:3:3</span></span>|<span data-ttu-id="8f08c-267">Data odierna 03.03.03</span><span class="sxs-lookup"><span data-stu-id="8f08c-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="8f08c-268">w o workdate</span><span class="sxs-lookup"><span data-stu-id="8f08c-268">w or workdate</span></span>|<span data-ttu-id="8f08c-269">Data del lavoro 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-270">lu o lunedì</span><span class="sxs-lookup"><span data-stu-id="8f08c-270">m or Monday</span></span>|<span data-ttu-id="8f08c-271">Lunedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-272">ma o martedì</span><span class="sxs-lookup"><span data-stu-id="8f08c-272">tu or Tuesday</span></span>|<span data-ttu-id="8f08c-273">Martedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-274">me o mercoledì</span><span class="sxs-lookup"><span data-stu-id="8f08c-274">we or Wednesday</span></span>|<span data-ttu-id="8f08c-275">Mercoledì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-276">gi o giovedì</span><span class="sxs-lookup"><span data-stu-id="8f08c-276">th or Thursday</span></span>|<span data-ttu-id="8f08c-277">Giovedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-278">ve o venerdì</span><span class="sxs-lookup"><span data-stu-id="8f08c-278">f or Friday</span></span>|<span data-ttu-id="8f08c-279">Venerdì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-280">sa o sabato</span><span class="sxs-lookup"><span data-stu-id="8f08c-280">s or Saturday</span></span>|<span data-ttu-id="8f08c-281">Sabato della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-282">do o domenica</span><span class="sxs-lookup"><span data-stu-id="8f08c-282">su or Sunday</span></span>|<span data-ttu-id="8f08c-283">Domenica della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="8f08c-284">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="8f08c-284">tu 10:30</span></span>|<span data-ttu-id="8f08c-285">Martedì della settimana corrente 10.30.00</span><span class="sxs-lookup"><span data-stu-id="8f08c-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="8f08c-286">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="8f08c-286">tu 3:3:3</span></span>|<span data-ttu-id="8f08c-287">Martedì della settimana corrente 03.03.03</span><span class="sxs-lookup"><span data-stu-id="8f08c-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="8f08c-288">Immissione della durata</span><span class="sxs-lookup"><span data-stu-id="8f08c-288">Entering Duration</span></span>

<span data-ttu-id="8f08c-289">È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.</span><span class="sxs-lookup"><span data-stu-id="8f08c-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="8f08c-290">Di seguito vengono forniti alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="8f08c-290">Here are some examples.</span></span>  

|<span data-ttu-id="8f08c-291">Durata</span><span class="sxs-lookup"><span data-stu-id="8f08c-291">Duration</span></span>|<span data-ttu-id="8f08c-292">Unità di misura\*\*</span><span class="sxs-lookup"><span data-stu-id="8f08c-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="8f08c-293">2h</span><span class="sxs-lookup"><span data-stu-id="8f08c-293">2h</span></span>|<span data-ttu-id="8f08c-294">2 ore</span><span class="sxs-lookup"><span data-stu-id="8f08c-294">2 hrs</span></span>|  
|<span data-ttu-id="8f08c-295">6h 30 m</span><span class="sxs-lookup"><span data-stu-id="8f08c-295">6h 30 m</span></span>|<span data-ttu-id="8f08c-296">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="8f08c-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="8f08c-297">6.5h</span><span class="sxs-lookup"><span data-stu-id="8f08c-297">6.5h</span></span>|<span data-ttu-id="8f08c-298">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="8f08c-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="8f08c-299">90m</span><span class="sxs-lookup"><span data-stu-id="8f08c-299">90m</span></span>|<span data-ttu-id="8f08c-300">1 ora 30 minuti</span><span class="sxs-lookup"><span data-stu-id="8f08c-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="8f08c-301">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="8f08c-301">2d 6h 30m</span></span>|<span data-ttu-id="8f08c-302">2 giorni 6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="8f08c-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="8f08c-303">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="8f08c-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="8f08c-304">2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi</span><span class="sxs-lookup"><span data-stu-id="8f08c-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="8f08c-305">È inoltre possibile immettere un numero in modo che venga automaticamente convertito in una durata.</span><span class="sxs-lookup"><span data-stu-id="8f08c-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="8f08c-306">Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.</span><span class="sxs-lookup"><span data-stu-id="8f08c-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="8f08c-307">Per visualizzare l'unità di misura utilizzata in un campo di durata, immettere un numero e controllare l'unità di misura in cui viene convertito.</span><span class="sxs-lookup"><span data-stu-id="8f08c-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="8f08c-308">Il numero 5 viene convertito in 5 h se l'unità di misura è l'ora.</span><span class="sxs-lookup"><span data-stu-id="8f08c-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="8f08c-309">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f08c-309">See Also</span></span>  
 [<span data-ttu-id="8f08c-310">Ricerca, filtro e ordinamento di elenchi</span><span class="sxs-lookup"><span data-stu-id="8f08c-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="8f08c-311">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f08c-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
