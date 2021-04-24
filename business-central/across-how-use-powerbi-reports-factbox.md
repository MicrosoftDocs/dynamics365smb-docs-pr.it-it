---
title: Visualizzare report Power BI personalizzati per i dati di Business Central | Microsoft Docs
description: Puoi usare i report Power BI per ottenere informazioni aggiuntive sui dati negli elenchi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777518"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="d7124-103">Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="d7124-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="d7124-104">include un elemento di controllo Dettaglio informazioni Power BI su diverse pagine elenco chiave.</span><span class="sxs-lookup"><span data-stu-id="d7124-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="d7124-105">Lo scopo di questo Dettaglio informazioni è di visualizzare i report Power BI che sono correlati ai record negli elenchi, fornendo ulteriori informazioni sui dati.</span><span class="sxs-lookup"><span data-stu-id="d7124-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="d7124-106">L'idea è di spostarsi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata.</span><span class="sxs-lookup"><span data-stu-id="d7124-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="d7124-107">viene fornito con alcuni di questi report.</span><span class="sxs-lookup"><span data-stu-id="d7124-107">comes ready with some of these reports.</span></span> <span data-ttu-id="d7124-108">Puoi anche creare i tuoi report personalizzati che vengono visualizzati in questo Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="d7124-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="d7124-109">La creazione di questi report è simile ad altri report.</span><span class="sxs-lookup"><span data-stu-id="d7124-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="d7124-110">Ma ci sono alcune regole di progettazione che dovrai seguire per assicurarti che i report vengano visualizzati come previsto.</span><span class="sxs-lookup"><span data-stu-id="d7124-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="d7124-111">Queste regole sono spiegate in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="d7124-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="d7124-112">Per informazioni generali sulla creazione e la pubblicazione di report Power BI per Business Central, vedi [Creazione di report Power BI per visualizzare i dati [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="d7124-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d7124-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="d7124-113">Prerequisites</span></span>

- <span data-ttu-id="d7124-114">Un account Power BI.</span><span class="sxs-lookup"><span data-stu-id="d7124-114">A Power BI account.</span></span>
- <span data-ttu-id="d7124-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d7124-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="d7124-116">Crea un report per una pagina di elenco</span><span class="sxs-lookup"><span data-stu-id="d7124-116">Create a report for a list page</span></span>

1. <span data-ttu-id="d7124-117">Avviare Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d7124-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="d7124-118">Seleziona **Ottieni dati** e inizia a scegliere l'origine dati per il report.</span><span class="sxs-lookup"><span data-stu-id="d7124-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="d7124-119">In questa fase, si specificano le pagine di elenco di Business Central che contengono i dati desiderati nel report.</span><span class="sxs-lookup"><span data-stu-id="d7124-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="d7124-120">Ad esempio, per creare un report per la lista di vendita, verificare che il set di dati contenga le informazioni relative alle vendite.</span><span class="sxs-lookup"><span data-stu-id="d7124-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="d7124-121">Per ulteriori informazioni, segui le istruzioni [Aggiungi [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="d7124-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="d7124-122">Imposta il filtro per i report.</span><span class="sxs-lookup"><span data-stu-id="d7124-122">Set the report filter.</span></span>

    <span data-ttu-id="d7124-123">Per aggiornare i dati al record selezionato nell'elenco, aggiungere un filtro al report.</span><span class="sxs-lookup"><span data-stu-id="d7124-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="d7124-124">Il filtro deve includere un campo dell'origine dati utilizzato per identificare in modo univoco ogni record nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d7124-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="d7124-125">Per gli sviluppatori, questo campo è la *chiave primaria*.</span><span class="sxs-lookup"><span data-stu-id="d7124-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="d7124-126">Nella maggior parte dei casi, la chiave primaria per un elenco è **Nr.**</span><span class="sxs-lookup"><span data-stu-id="d7124-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="d7124-127">.</span><span class="sxs-lookup"><span data-stu-id="d7124-127">field.</span></span>

    <span data-ttu-id="d7124-128">Per impostare il filtro, procedi nel seguente modo:</span><span class="sxs-lookup"><span data-stu-id="d7124-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="d7124-129">In **Filtri**, seleziona il campo della chiave primaria dall'elenco dei campi disponibili.</span><span class="sxs-lookup"><span data-stu-id="d7124-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="d7124-130">Trascina il campo sul riquadro **Filtri** e rilascialo nella casella **Filtri su tutte le pagine**.</span><span class="sxs-lookup"><span data-stu-id="d7124-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="d7124-131">Imposta il **Tipo di filtro** su **Filtro di base**.</span><span class="sxs-lookup"><span data-stu-id="d7124-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="d7124-132">Non può essere un filtro di pagina, visivo o avanzato.</span><span class="sxs-lookup"><span data-stu-id="d7124-132">It can't be page, visual, or advanced filter.</span></span>

    ![Impostare il filtro del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="d7124-134">Progetta l'area di disposizione del report.</span><span class="sxs-lookup"><span data-stu-id="d7124-134">Design the report layout.</span></span>

    <span data-ttu-id="d7124-135">Crea l'area di disposizione trascinando i campi e aggiungendo visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d7124-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="d7124-136">Per ulteriori informazioni, vedi [Lavora con la visualizzazione Report in Power BI Desktop](/power-bi/create-reports/desktop-report-view) nella documentazione di Power BI.</span><span class="sxs-lookup"><span data-stu-id="d7124-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="d7124-137">Vedi le sezioni successive sul dimensionamento del report e sull'utilizzo di più pagine.</span><span class="sxs-lookup"><span data-stu-id="d7124-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="d7124-138">Salva e assegna un nome al rapporto.</span><span class="sxs-lookup"><span data-stu-id="d7124-138">Save and name the report.</span></span>

    <span data-ttu-id="d7124-139">È importante assegnare al report un nome che contenga il nome della pagina di elenco associata al report.</span><span class="sxs-lookup"><span data-stu-id="d7124-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="d7124-140">Ad esempio, se il report è per la pagina di elenco **Articoli**, includi la parola *articoli* da qualche parte nel nome.</span><span class="sxs-lookup"><span data-stu-id="d7124-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="d7124-141">Questa convenzione di denominazione non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="d7124-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="d7124-142">Tuttavia, rende la selezione dei report in [!INCLUDE[prod_short](includes/prod_short.md)] più veloce.</span><span class="sxs-lookup"><span data-stu-id="d7124-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="d7124-143">Quando la pagina di selezione del report si apre da una pagina di elenco, viene automaticamente filtrata in base al nome della pagina.</span><span class="sxs-lookup"><span data-stu-id="d7124-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="d7124-144">Questo filtro viene eseguito per limitare i report visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d7124-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="d7124-145">Gli utenti possono rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.</span><span class="sxs-lookup"><span data-stu-id="d7124-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="d7124-146">Quando hai finito, pubblica il report come al solito.</span><span class="sxs-lookup"><span data-stu-id="d7124-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="d7124-147">Per ulteriori informazioni, vedi [Pubblicazione di un report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="d7124-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="d7124-148">Prova il report.</span><span class="sxs-lookup"><span data-stu-id="d7124-148">Test the report.</span></span>

    <span data-ttu-id="d7124-149">Una volta che i rapporti sono stati pubblicati nel tuo spazio di lavoro, dovrebbero essere disponibili dal Dettaglio informazioni di Power BI nella pagina dell'elenco in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7124-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="d7124-150">Per provarlo, segui i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7124-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="d7124-151">Apri [!INCLUDE[prod_short](includes/prod_short.md)] e vai alla pagina dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d7124-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="d7124-152">Se non vedi Dettaglio informazioni di Power BI, vai alla barra delle azioni, quindi seleziona **Azioni** > **Visualizza** > **Mostra/Nascondi report di Power BI**.</span><span class="sxs-lookup"><span data-stu-id="d7124-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="d7124-153">In Dettagli informazioni di Power BI, scegli **Seleziona report**, quindi la casella **Abilita** per il report, quindi seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7124-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="d7124-154">Se progettato correttamente, viene visualizzato il report.</span><span class="sxs-lookup"><span data-stu-id="d7124-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="d7124-155">Imposta le dimensioni e il colore del report</span><span class="sxs-lookup"><span data-stu-id="d7124-155">Set the report size and color</span></span>

<span data-ttu-id="d7124-156">La dimensione del report deve essere impostata su 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="d7124-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="d7124-157">Questa dimensione fornisce il corretto ridimensionamento del report nello spazio disponibile dal controllo del riquadro dettaglio informazioni Power BI in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7124-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d7124-158">Per definire la dimensione del report, posizionare il focus all'esterno dell'area del layout di report e quindi scegliere l'icona del rullo di verniciatura.</span><span class="sxs-lookup"><span data-stu-id="d7124-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Impostare la larghezza e l'altezza del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="d7124-160">È possibile modificare la larghezza e l'altezza del report scegliendo **Personalizzato** nel campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="d7124-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="d7124-161">Se desideri che lo sfondo del report sfumi con il colore di sfondo del controllo del riquadro Dettaglio informazioni di Power BI, imposta un colore di sfondo personalizzato del report *#FFFFFF* (bianco).</span><span class="sxs-lookup"><span data-stu-id="d7124-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="d7124-162">Usa il file del tema di [!INCLUDE [prod_short](includes/prod_short.md)] per creare report con lo stesso stile di colore delle app [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7124-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="d7124-163">Per ulteriori informazioni, vedi [Uso del tema del report [!INCLUDE [prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="d7124-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="d7124-164">Report con più pagine</span><span class="sxs-lookup"><span data-stu-id="d7124-164">Reports with multiple pages</span></span>

<span data-ttu-id="d7124-165">Power BI consente di creare un unico report con più pagine.</span><span class="sxs-lookup"><span data-stu-id="d7124-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="d7124-166">Tuttavia, per i report che verranno visualizzati con le pagine di elenco, non è consigliabile che abbiano più di una pagina.</span><span class="sxs-lookup"><span data-stu-id="d7124-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="d7124-167">Il riquadro Dettaglio informazioni Power BI mostrerà solo la prima pagina del report.</span><span class="sxs-lookup"><span data-stu-id="d7124-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="d7124-168">Risolvere i problemi</span><span class="sxs-lookup"><span data-stu-id="d7124-168">Fixing problems</span></span>

<span data-ttu-id="d7124-169">Questa sezione fornisce istruzioni su come risolvere i problemi che potresti incontrare durante il tentativo di visualizzare un report di Power BI per una pagina di elenco in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7124-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="d7124-170">Non puoi vedere il Dettaglio informazioni di Power BI in una pagina di elenco</span><span class="sxs-lookup"><span data-stu-id="d7124-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="d7124-171">Per impostazione predefinita, il Dettaglio informazioni di Power BI è nascosto alla vista.</span><span class="sxs-lookup"><span data-stu-id="d7124-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="d7124-172">Per visualizzare il Dettaglio informazioni su una pagina, dalla barra delle azioni, seleziona **Azioni** > **Schermo** > **Mostra/Nascondi report Power BI**.</span><span class="sxs-lookup"><span data-stu-id="d7124-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="d7124-173">Non è possibile visualizzare il report nel pannello Seleziona report</span><span class="sxs-lookup"><span data-stu-id="d7124-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="d7124-174">Probabilmente è perché il nome del report non contiene il nome della pagina di elenco visualizzata.</span><span class="sxs-lookup"><span data-stu-id="d7124-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="d7124-175">Rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.</span><span class="sxs-lookup"><span data-stu-id="d7124-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="d7124-176">Il report è caricato ma è vuoto, non filtrato o filtrato in modo errato</span><span class="sxs-lookup"><span data-stu-id="d7124-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="d7124-177">Verificare che il filtro del report contenga la chiave primaria corretta.</span><span class="sxs-lookup"><span data-stu-id="d7124-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="d7124-178">Nella maggior parte dei casi, questo è il campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="d7124-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="d7124-179">ma nella tabella **Movimenti C/G**, ad esempio, è necessario utilizzare il campo **Nr. movimento**.</span><span class="sxs-lookup"><span data-stu-id="d7124-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="d7124-180">Il report è caricato, ma mostra una pagina non prevista</span><span class="sxs-lookup"><span data-stu-id="d7124-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="d7124-181">Verificare che la pagina da visualizzare sia la prima pagina del report.</span><span class="sxs-lookup"><span data-stu-id="d7124-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="d7124-182">Il report viene visualizzato con un bordo grigio indesiderato o è troppo piccolo o troppo grande</span><span class="sxs-lookup"><span data-stu-id="d7124-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="d7124-183">Verificare che la dimensione del report sia impostata su 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="d7124-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="d7124-184">Salvare il report quindi aggiornare la pagina elenco.</span><span class="sxs-lookup"><span data-stu-id="d7124-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="d7124-185">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="d7124-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="d7124-186">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d7124-186">See Also</span></span>

[<span data-ttu-id="d7124-187">Abilitare i dati aziendali per Power BI</span><span class="sxs-lookup"><span data-stu-id="d7124-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="d7124-188">[Uso di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="d7124-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="d7124-189">Preparazione al business</span><span class="sxs-lookup"><span data-stu-id="d7124-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="d7124-190">[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="d7124-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="d7124-191">Finanze</span><span class="sxs-lookup"><span data-stu-id="d7124-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]