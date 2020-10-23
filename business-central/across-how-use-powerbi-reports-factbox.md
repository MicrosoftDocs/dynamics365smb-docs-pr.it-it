---
title: Visualizzare report Power BI personalizzati per i dati di Business Central | Microsoft Docs
description: È possibile usare i report Power BI per ottenere informazioni aggiuntive sui dati negli elenchi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 04c0c5d203e78c2ae0be48609a5ee90f45b83c6f
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968387"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a><span data-ttu-id="3b200-103">Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="3b200-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

[!INCLUDE[prodlong](includes/prodlong.md)] <span data-ttu-id="3b200-104">include un elemento di controllo Dettaglio informazioni in una serie di pagine elenco chiave che offrono informazioni aggiuntive sui dati in elenco.</span><span class="sxs-lookup"><span data-stu-id="3b200-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="3b200-105">Spostandosi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata.</span><span class="sxs-lookup"><span data-stu-id="3b200-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="3b200-106">È possibile creare report personalizzati da visualizzare in questo controllo.</span><span class="sxs-lookup"><span data-stu-id="3b200-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="3b200-107">Tuttavia, esistono alcune regole da seguire per garantire che i report funzionino come previsto.</span><span class="sxs-lookup"><span data-stu-id="3b200-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="3b200-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3b200-108">Prerequisites</span></span>

- <span data-ttu-id="3b200-109">Un account Power BI.</span><span class="sxs-lookup"><span data-stu-id="3b200-109">A Power BI account.</span></span>
- <span data-ttu-id="3b200-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="3b200-110">Power BI Desktop.</span></span>

<span data-ttu-id="3b200-111">Per ulteriori informazioni su come iniziare, vedere [Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="3b200-111">For more information about getting started, see [Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="3b200-112">Definizione del set di dati del report</span><span class="sxs-lookup"><span data-stu-id="3b200-112">Defining the report data set</span></span>

<span data-ttu-id="3b200-113">Specificare l'origine dati che contiene i dati relativi all'elenco.</span><span class="sxs-lookup"><span data-stu-id="3b200-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="3b200-114">Ad esempio, per creare un report per la lista di vendita, verificare che il set di dati contenga le informazioni relative alle vendite.</span><span class="sxs-lookup"><span data-stu-id="3b200-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="3b200-115">Definizione del filtro report</span><span class="sxs-lookup"><span data-stu-id="3b200-115">Defining the report filter</span></span>

<span data-ttu-id="3b200-116">Per aggiornare i dati al record selezionato nell'elenco, aggiungere un filtro al report.</span><span class="sxs-lookup"><span data-stu-id="3b200-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="3b200-117">Il filtro deve includere un campo dell'origine dati utilizzata come *chiave primaria*.</span><span class="sxs-lookup"><span data-stu-id="3b200-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="3b200-118">Nella maggior parte dei casi, la chiave primaria per un elenco è **Nr.**</span><span class="sxs-lookup"><span data-stu-id="3b200-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="3b200-119">.</span><span class="sxs-lookup"><span data-stu-id="3b200-119">field.</span></span>

<span data-ttu-id="3b200-120">Per definire un filtro per il report, selezionare la chiave primaria dall'elenco dei campi disponibili e quindi trascinare il campo nella sezione **Filtro Report**.</span><span class="sxs-lookup"><span data-stu-id="3b200-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="3b200-121">Il filtro deve essere un filtro di report di base definito per tutte le pagine.</span><span class="sxs-lookup"><span data-stu-id="3b200-121">The filter must be a basic report filter that's defined for all pages.</span></span> <span data-ttu-id="3b200-122">Non può essere un filtro di pagina, visivo o avanzato.</span><span class="sxs-lookup"><span data-stu-id="3b200-122">It can't be page, visual, or advanced filter.</span></span>

![Impostare il filtro del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="3b200-124">Impostazione della dimensione e del colore del report</span><span class="sxs-lookup"><span data-stu-id="3b200-124">Setting the report size and color</span></span>

<span data-ttu-id="3b200-125">La dimensione del report deve essere impostata su 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="3b200-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="3b200-126">Questa dimensione fornisce il corretto ridimensionamento del report nello spazio disponibile dal controllo del riquadro dettaglio informazioni Power BI in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3b200-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3b200-127">Per definire la dimensione del report, posizionare il focus all'esterno dell'area del layout di report e quindi scegliere l'icona del rullo di verniciatura.</span><span class="sxs-lookup"><span data-stu-id="3b200-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Impostare la larghezza e l'altezza del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="3b200-129">È possibile modificare la larghezza e l'altezza del report scegliendo **Personalizzato** nel campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="3b200-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="3b200-130">Se si desidera che lo sfondo del report sfumi con il colore di sfondo del controllo del riquadro dettaglio informazioni di Power BI, impostare un colore di sfondo personalizzato del report *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="3b200-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="3b200-131">Uso dei report con più pagine</span><span class="sxs-lookup"><span data-stu-id="3b200-131">Using reports with multiple pages</span></span>

<span data-ttu-id="3b200-132">Power BI consente di creare un unico report con più pagine.</span><span class="sxs-lookup"><span data-stu-id="3b200-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="3b200-133">Tuttavia, per i report che verranno visualizzati con le pagine di elenco, non è consigliabile che abbiano più di una pagina.</span><span class="sxs-lookup"><span data-stu-id="3b200-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="3b200-134">Il riquadro Dettaglio informazioni Power BI mostrerà solo la prima pagina del report.</span><span class="sxs-lookup"><span data-stu-id="3b200-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="3b200-135">Assegnazione di un nome al report</span><span class="sxs-lookup"><span data-stu-id="3b200-135">Naming the report</span></span>

<span data-ttu-id="3b200-136">Assegnare al report un nome che contenga il nome della pagina di elenco associata al report.</span><span class="sxs-lookup"><span data-stu-id="3b200-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="3b200-137">Ad esempio, se il report è per la pagina di elenco **Fornitore**, includere la parola *fornitore* da qualche parte nel nome.</span><span class="sxs-lookup"><span data-stu-id="3b200-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="3b200-138">Questa convenzione di denominazione non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="3b200-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="3b200-139">Tuttavia, rende la selezione dei report in [!INCLUDE[d365fin](includes/d365fin_md.md)] più veloce.</span><span class="sxs-lookup"><span data-stu-id="3b200-139">However, it makes selecting reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] quicker.</span></span> <span data-ttu-id="3b200-140">Quando la pagina di selezione del report si apre da una pagina di elenco, viene automaticamente filtrata in base al nome della pagina.</span><span class="sxs-lookup"><span data-stu-id="3b200-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="3b200-141">Questo filtro viene eseguito per limitare i report visualizzati.</span><span class="sxs-lookup"><span data-stu-id="3b200-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="3b200-142">Gli utenti possono rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.</span><span class="sxs-lookup"><span data-stu-id="3b200-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="3b200-143">Risolvere i problemi</span><span class="sxs-lookup"><span data-stu-id="3b200-143">Fixing problems</span></span>

<span data-ttu-id="3b200-144">In questa sezione viene fornita una soluzione alternativa per i problemi più comuni che si verificano quando si creano report Power BI.</span><span class="sxs-lookup"><span data-stu-id="3b200-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="3b200-145">Non è possibile visualizzare un report nella pagina Seleziona report</span><span class="sxs-lookup"><span data-stu-id="3b200-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="3b200-146">Probabilmente è perché il nome del report non contiene il nome della pagina di elenco.</span><span class="sxs-lookup"><span data-stu-id="3b200-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="3b200-147">Rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.</span><span class="sxs-lookup"><span data-stu-id="3b200-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="3b200-148">Il report è caricato ma è vuoto, non filtrato o filtrato in modo errato</span><span class="sxs-lookup"><span data-stu-id="3b200-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="3b200-149">Verificare che il filtro del report contenga la chiave primaria corretta.</span><span class="sxs-lookup"><span data-stu-id="3b200-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="3b200-150">Nella maggior parte dei casi, questo è il campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="3b200-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="3b200-151">ma nella tabella **Movimenti C/G**, ad esempio, è necessario utilizzare il campo **Nr. movimento**.</span><span class="sxs-lookup"><span data-stu-id="3b200-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="3b200-152">Il report è caricato, ma mostra una pagina non prevista</span><span class="sxs-lookup"><span data-stu-id="3b200-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="3b200-153">Verificare che la pagina da visualizzare sia la prima pagina del report.</span><span class="sxs-lookup"><span data-stu-id="3b200-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="3b200-154">Il report viene visualizzato con un bordo grigio indesiderato o è troppo piccolo o troppo grande</span><span class="sxs-lookup"><span data-stu-id="3b200-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="3b200-155">Verificare che la dimensione del report sia impostata su 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="3b200-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="3b200-156">Salvare il report quindi aggiornare la pagina elenco.</span><span class="sxs-lookup"><span data-stu-id="3b200-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3b200-157">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="3b200-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="3b200-158">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3b200-158">See Also</span></span>

[<span data-ttu-id="3b200-159">Abilitare i dati aziendali per Power BI</span><span class="sxs-lookup"><span data-stu-id="3b200-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="3b200-160">[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="3b200-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="3b200-161">Introduzione</span><span class="sxs-lookup"><span data-stu-id="3b200-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="3b200-162">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3b200-162">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="3b200-163">Finanze</span><span class="sxs-lookup"><span data-stu-id="3b200-163">Finance</span></span>](finance.md)  
