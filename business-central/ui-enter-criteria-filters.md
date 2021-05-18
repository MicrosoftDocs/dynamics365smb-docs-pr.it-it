---
title: Ricerca, filtro e ordinamento di elenchi | Documenti Microsoft
description: Utilizzare in modo efficiente gli elenchi cercando nei dati, ordinando colonne e perfezionando i risultati con simboli di filtro e tasti di scelta rapida da tastiera.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a27556350851de61bd31504d0c29ef60df6d890a
ms.sourcegitcommit: 921f0c4043dcda2fb8fc35df1b64310bf32270d7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017176"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="56665-103">Ricerca, filtro e ordinamento</span><span class="sxs-lookup"><span data-stu-id="56665-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="56665-104">Ordinamento, ricerca e filtro sono alcune delle operazioni che semplificano l'individuazione, l'analisi e la limitazione di record in un elenco o in un XMLport</span><span class="sxs-lookup"><span data-stu-id="56665-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="56665-105">o report.</span><span class="sxs-lookup"><span data-stu-id="56665-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="56665-106">È possibile collegare alcune o tutte le procedure contemporaneamente a rapidamente per trovare o analizzare rapidamente i dati.</span><span class="sxs-lookup"><span data-stu-id="56665-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="56665-107">Per i report e gli XMLport, è possibile impostare filtri come negli elenchi per delimitare i dati da includere in report o XMLport, ma non è possibile ordinare e cercare.</span><span class="sxs-lookup"><span data-stu-id="56665-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="56665-108">Quando si visualizzano i dati come riquadri, è possibile cercare e utilizzare i filtri.</span><span class="sxs-lookup"><span data-stu-id="56665-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="56665-109">Per utilizzare il set completo delle potenti funzionalità di ordinamento, ricerca e filtro, scegliere l'icona ![Mostra come lista](media/ui_show_as_list_icon.png "Freccia sinistra Mostra come lista") per visualizzare i record in forma di elenco.</span><span class="sxs-lookup"><span data-stu-id="56665-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="56665-110">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="56665-110">Sorting</span></span>

<span data-ttu-id="56665-111">L'ordinamento consente di ottenere in modo semplice e rapido una panoramica dei dati.</span><span class="sxs-lookup"><span data-stu-id="56665-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="56665-112">Ad esempio, se si dispone di molti clienti, si potrebbe ordinarli in base a **Nr. cliente**, **Codice valuta** o **Codice paese** per ottenere la panoramica desiderata.</span><span class="sxs-lookup"><span data-stu-id="56665-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="56665-113">Per ordinare un elenco, è possibile:</span><span class="sxs-lookup"><span data-stu-id="56665-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="56665-114">Selezionare il testo di un'intestazione di colonna per passare dall'ordinamento ascendente a quello discendente e viceversa, oppure</span><span class="sxs-lookup"><span data-stu-id="56665-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="56665-115">Scegliere la freccia del menu a discesa nell'intestazione della colonna, quindi scegliere l'azione **Ascendente** o **Discendente**.</span><span class="sxs-lookup"><span data-stu-id="56665-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="56665-116">L'ordinamento non è supportato nelle immagini, nei campi BLOB, in FlowFilter e nei campi che non appartengono a una tabella.</span><span class="sxs-lookup"><span data-stu-id="56665-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="56665-117">Ricerca</span><span class="sxs-lookup"><span data-stu-id="56665-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="56665-118">Nella parte superiore di ogni pagina elenco, è presente l'azione **Cerca** ![Cerca nell'elenco](media/ui-search/search-list.png "Icona Cerca nell'elenco") che fornisce un modo rapido e semplice per ridurre i record in un elenco e visualizzare solo i record che contengono i dati che si intende visualizzare.</span><span class="sxs-lookup"><span data-stu-id="56665-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="56665-119">Per cercare, è sufficiente selezionare l'azione **Cerca**, quindi nella casella digitare il testo che si sta cercando.</span><span class="sxs-lookup"><span data-stu-id="56665-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="56665-120">È possibile immettere lettere, numeri e altri simboli.</span><span class="sxs-lookup"><span data-stu-id="56665-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="56665-121">In generale, la ricerca tenta di trovare il testo corrispondente in tutti i campi,</span><span class="sxs-lookup"><span data-stu-id="56665-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="56665-122">non fa la distinzione tra maiuscole e minuscole e trova il testo corrispondente ovunque nel campo (all'inizio, alla fine o nel mezzo).</span><span class="sxs-lookup"><span data-stu-id="56665-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="56665-123">È possibile premere **F3** per attivare e disattivare la casella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="56665-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="56665-124">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="56665-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="56665-125">La ricerca non restituisce i valori di immagini, campi BLOB, FlowFilters, FlowField e altri campi che non fanno parte di una tabella.</span><span class="sxs-lookup"><span data-stu-id="56665-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="56665-126">Perfezionamento della ricerca con criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="56665-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="56665-127">È possibile effettuare una ricerca più precisa utilizzando operatori di filtro, espressioni e token di filtro.</span><span class="sxs-lookup"><span data-stu-id="56665-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="56665-128">A differenza dei filtri, questi vengono applicati a tutti i campi quando utilizzati nella casella di ricerca, rendendoli meno efficienti dei filtri.</span><span class="sxs-lookup"><span data-stu-id="56665-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="56665-129">Per trovare solo i valori dei campi che corrispondono esattamente all'intero testo e all'uso di maiuscole/minuscole, posizionare il testo di ricerca tra virgolette singole `''` (ad esempio `'man'`).</span><span class="sxs-lookup"><span data-stu-id="56665-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="56665-130">Per trovare valori di campo che iniziano con un determinato testo e corrispondono all'uso di maiuscole/minuscole, posizionare `*` dopo il testo di ricerca (ad esempio `man*`).</span><span class="sxs-lookup"><span data-stu-id="56665-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="56665-131">Per trovare valori di campo che terminano con un determinato testo e corrispondono all'utilizzo di maiuscole/minuscole, posizionare `*` prima del testo di ricerca (ad esempio `*man`).</span><span class="sxs-lookup"><span data-stu-id="56665-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="56665-132">Quando si utilizza `''` o `*`, la ricerca è sensibile alla distinzione maiuscola/minuscola.</span><span class="sxs-lookup"><span data-stu-id="56665-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="56665-133">Se si desidera ignorare la distinzione tra maiuscole e minuscole, posizionare `@` prima del testo di ricerca, (ad esempio `@man*`).</span><span class="sxs-lookup"><span data-stu-id="56665-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="56665-134">Nella tabella seguente sono riportati alcuni esempi per spiegare come è possibile utilizzare la funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="56665-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="56665-135">Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="56665-135">Search Criteria</span></span>|<span data-ttu-id="56665-136">Trova…</span><span class="sxs-lookup"><span data-stu-id="56665-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="56665-137">oppure</span><span class="sxs-lookup"><span data-stu-id="56665-137">or</span></span> <br />`Man`|<span data-ttu-id="56665-138">Tutti i record con campi che contengono il testo **man**, indipendentemente dall'uso di maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="56665-139">Ad esempio, **Manchester**, **manual** o **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="56665-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="56665-140">Tutti i record con campi che contengono solo il testo **Man**, che corrisponde all'uso di maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="56665-141">Tutti i record con campi che iniziano con il testo <b>man</b>, corrispondenti all'uso di maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="56665-142">Ad esempio, **Manchester**, ma non **manual** o **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="56665-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="56665-143">Tutti i record con campi che iniziano con il testo **man**, indipendentemente dall'uso di maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="56665-144">Ad esempio, **Manchester** e **manual**, ma non **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="56665-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="56665-145">Tutti i record con campi che finiscono con il testo **man**, indipendentemente dall'uso di maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="56665-146">Ad esempio, **Sportsman**, ma non **Manchester** o **manual**.</span><span class="sxs-lookup"><span data-stu-id="56665-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="56665-147">Filtro</span><span class="sxs-lookup"><span data-stu-id="56665-147">Filtering</span></span>

<span data-ttu-id="56665-148">I filtri forniscono un modo più avanzato e versatile per controllare quali record sono inclusi in un elenco in un report o in XMLport.</span><span class="sxs-lookup"><span data-stu-id="56665-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="56665-149">Esistono due principali differenze tra la ricerca e il filtro, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="56665-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="56665-150">**Ricerca**</span><span class="sxs-lookup"><span data-stu-id="56665-150">**Searching**</span></span> | <span data-ttu-id="56665-151">**Filtri**</span><span class="sxs-lookup"><span data-stu-id="56665-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="56665-152">**Campi applicabili**</span><span class="sxs-lookup"><span data-stu-id="56665-152">**Applicable Fields**</span></span> | <span data-ttu-id="56665-153">Cerca in tutti i campi visibili nella pagina.</span><span class="sxs-lookup"><span data-stu-id="56665-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="56665-154">Filtra uno o più campi singolarmente, selezionando da qualsiasi campo sulla tabella, inclusi i campi che non sono visibili sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="56665-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="56665-155">**Corrispondenza**</span><span class="sxs-lookup"><span data-stu-id="56665-155">**Matching**</span></span> | <span data-ttu-id="56665-156">Visualizza i record con campi che corrispondono al testo di ricerca, indipendentemente dall'uso di maiuscole/minuscole. o dal posizionamento del testo nel campo.</span><span class="sxs-lookup"><span data-stu-id="56665-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="56665-157">Visualizza i record in cui il campo corrisponde esattamente al filtro, incluse maiuscole e minuscole, a meno che non vengano inseriti simboli di filtro speciali.</span><span class="sxs-lookup"><span data-stu-id="56665-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="56665-158">Il filtro consente di visualizzare record per account o clienti specifici, date, importi e altre informazioni specificando i criteri di filtro.</span><span class="sxs-lookup"><span data-stu-id="56665-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="56665-159">Solo i record che soddisfano i criteri vengono visualizzati nell'elenco o inclusi in un report, processo batch o XMLport.</span><span class="sxs-lookup"><span data-stu-id="56665-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="56665-160">Se si specificano i criteri per più campi, verranno visualizzati solo i record che soddisfano tutti i criteri.</span><span class="sxs-lookup"><span data-stu-id="56665-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="56665-161">Per gli elenchi, i filtri vengono visualizzati in un riquadro filtri visualizzato a sinistra dell'elenco quando viene attivato.</span><span class="sxs-lookup"><span data-stu-id="56665-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="56665-162">Per report, processi batch e XMLport, i filtri sono visibili direttamente nella pagina di richiesta.</span><span class="sxs-lookup"><span data-stu-id="56665-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="56665-163">Filtro con campi di tipo opzione</span><span class="sxs-lookup"><span data-stu-id="56665-163">Filtering with Option Fields</span></span>

<span data-ttu-id="56665-164">Per i campi "ordinari" che contengono dati, data di impostazione o dati aziendali, è possibile impostare filtri selezionando i dati e digitando valori di filtro e quindi utilizzare i simboli per definire criteri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="56665-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="56665-165">Per ulteriori informazioni, vedere [Immissione dei criteri di filtro](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="56665-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="56665-166">Tuttavia, per i campi di tipo **Opzione**, è possibile soltanto impostare un filtro selezionando una o più opzioni da un elenco a discesa delle opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="56665-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="56665-167">Un esempio di campo di tipo opzione è il campo **Stato** nella pagina **Ordini vendita**.</span><span class="sxs-lookup"><span data-stu-id="56665-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="56665-168">Quando si selezionano più opzioni come valore di filtro, la relazione tra le opzioni viene definita come *O*.</span><span class="sxs-lookup"><span data-stu-id="56665-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="56665-169">Ad esempio, se si selezionano le caselle di controllo **Aperto** e **Rilasciato** nel campo di filtro **Stato** della pagina **Ordini vendita**, significa che sono visualizzati gli ordini vendita aperti o rilasciati.</span><span class="sxs-lookup"><span data-stu-id="56665-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="56665-170">Impostazione di filtri negli elenchi</span><span class="sxs-lookup"><span data-stu-id="56665-170">Setting Filters on Lists</span></span>

<span data-ttu-id="56665-171">Negli elenchi, i filtri vengono impostati utilizzando il riquadro filtri.</span><span class="sxs-lookup"><span data-stu-id="56665-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="56665-172">Per visualizzare il riquadro filtri per un elenco, selezionare la freccia rivolta verso il basso accanto al nome della pagina, quindi selezionare l'azione **Mostra riquadro Filtri**.</span><span class="sxs-lookup"><span data-stu-id="56665-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="56665-173">In alternativa, premere **MAIUSC+F3**.</span><span class="sxs-lookup"><span data-stu-id="56665-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="56665-174">Per visualizzare il riquadro filtri per una colonna in un elenco, selezionare la freccia rivolta verso il basso quindi selezionare l'azione **Filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="56665-175">In alternativa, premere **MAIUSC+F3**.</span><span class="sxs-lookup"><span data-stu-id="56665-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="56665-176">Il riquadro filtri si apre con la colonna selezionata visualizzata come campo di filtro nella sezione **Filtra elenco per**.</span><span class="sxs-lookup"><span data-stu-id="56665-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="56665-177">Il riquadro filtri visualizza i filtri correnti per un elenco e consente di impostare filtri personalizzati in uno o più campi scegliendo l'azione **+ Filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="56665-178">Un riquadro dei filtri è diviso in tre sezioni: **Visualizzazioni**, **Filtra elenco per** e **Filtra totali per**:</span><span class="sxs-lookup"><span data-stu-id="56665-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="56665-179">**Visualizzazioni**</span><span class="sxs-lookup"><span data-stu-id="56665-179">**Views**</span></span>

  <span data-ttu-id="56665-180">Alcuni elenchi includono la sezione **Visualizzazioni**.</span><span class="sxs-lookup"><span data-stu-id="56665-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="56665-181">Le visualizzazioni sono variazioni dell'elenco che sono state preconfigurate con i filtri.</span><span class="sxs-lookup"><span data-stu-id="56665-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="56665-182">È possibile definire e salvare tutte le visualizzazioni desiderate per elenco.</span><span class="sxs-lookup"><span data-stu-id="56665-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="56665-183">Le visualizzazioni saranno disponibili su qualsiasi dispositivo a cui si accede.</span><span class="sxs-lookup"><span data-stu-id="56665-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="56665-184">Per ulteriori informazioni, vedere [Salvare e personalizzare visualizzazioni elenco](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="56665-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="56665-185">**Filtra elenco per**</span><span class="sxs-lookup"><span data-stu-id="56665-185">**Filter list by**</span></span>

  <span data-ttu-id="56665-186">Questa sezione consente di aggiungere filtri in campi specifici per ridurre il numero di record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="56665-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="56665-187">Per aggiungere un filtro, scegliere l'azione **+ Filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="56665-188">Quindi, digitare il nome del campo in base al quale filtrare l'elenco o selezionare un campo dall'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="56665-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="56665-189">**Filtra totali per**</span><span class="sxs-lookup"><span data-stu-id="56665-189">**Filter totals by**</span></span>

  <span data-ttu-id="56665-190">Alcuni elenchi che visualizzano campi calcolati, come importi e quantità, includeranno la sezione **Filtra totali per** in cui è possibile impostare varie dimensioni che influenzano i calcoli.</span><span class="sxs-lookup"><span data-stu-id="56665-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="56665-191">Per aggiungere un filtro, scegliere l'azione **+ Filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="56665-192">Quindi, digitare il nome del campo in base al quale filtrare l'elenco o selezionare un campo dall'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="56665-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="56665-193">I filtri nella sezione **Filtra totali per** sono controllati da FlowFilter nella progettazione della pagina.</span><span class="sxs-lookup"><span data-stu-id="56665-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="56665-194">Per informazioni tecniche, vedere [FlowFilter](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="56665-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="56665-195">È possibile impostare un filtro semplice direttamente in un elenco utilizzando il riquadro filtri, ovvero un filtro che visualizza solo i record con lo stesso valore della cella selezionata.</span><span class="sxs-lookup"><span data-stu-id="56665-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="56665-196">Selezionare un cella nell'elenco, selezionare la freccia rivolta verso il basso quindi scegliere l'azione **Filtra in base a questo valore**.</span><span class="sxs-lookup"><span data-stu-id="56665-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="56665-197">In alternativa, premere **ALT+F3**.</span><span class="sxs-lookup"><span data-stu-id="56665-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="56665-198">Impostazione di filtri in report, processi batch e XMLport</span><span class="sxs-lookup"><span data-stu-id="56665-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="56665-199">Per report e XMLport, i filtri sono visibili direttamente nella pagina di richiesta.</span><span class="sxs-lookup"><span data-stu-id="56665-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="56665-200">La pagina di richiesta visualizza gli ultimi filtri utilizzati in base alla selezione effettuata nel campo **Utilizza valori predefiniti da**.</span><span class="sxs-lookup"><span data-stu-id="56665-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="56665-201">Per ulteriori informazioni, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="56665-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="56665-202">La sezione **Filtro** principale mostra i campi di filtro predefiniti utilizzati per delimitare i record da includere in report o XMLport.</span><span class="sxs-lookup"><span data-stu-id="56665-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="56665-203">Per aggiungere un filtro, scegliere l'azione **+ Filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="56665-204">Quindi, digitare il nome del campo in base al quale filtrare o selezionare un campo dall'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="56665-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="56665-205">Nella sezione **Filtra totali per**, è possibile regolare varie dimensioni che influenzano i calcoli in report o XMLport.</span><span class="sxs-lookup"><span data-stu-id="56665-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="56665-206">Per aggiungere un filtro, scegliere l'azione **+ Filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="56665-207">Quindi, digitare il nome del campo in base al quale filtrare o selezionare un campo dall'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="56665-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="56665-208">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="56665-208">Entering Filter Criteria</span></span>

<span data-ttu-id="56665-209">Nel riquadro filtri e in una pagina di richiesta, i criteri di filtro vengono immessi nella casella sotto il campo di filtro.</span><span class="sxs-lookup"><span data-stu-id="56665-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="56665-210">Il tipo di campo di filtro determina quali criteri è possibile immettere.</span><span class="sxs-lookup"><span data-stu-id="56665-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="56665-211">Ad esempio, il filtro di un campo con valori fissi consente solo di scegliere da tali valori.</span><span class="sxs-lookup"><span data-stu-id="56665-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="56665-212">Per ulteriori informazioni sui simboli speciali del filtro, vedere [Criteri e simboli di filtro](#FilterCriteria) e [Token di filtro](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="56665-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="56665-213">Le colonne che hanno già dei filtri sono indicate dall'icona ![icona Filtro](media/ui-search/filter-icon.png "Icona Filtro") nell'intestazione della colonna.</span><span class="sxs-lookup"><span data-stu-id="56665-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="56665-214">Per rimuovere un filtro, fare clic sulla freccia rivolta verso il basso, quindi scegliere l'azione **Cancella filtro**.</span><span class="sxs-lookup"><span data-stu-id="56665-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="56665-215">Accelerare la ricerca e l'analisi dei dati utilizzando combinazioni di tasti di scelta rapida da tastiera.</span><span class="sxs-lookup"><span data-stu-id="56665-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="56665-216">Ad esempio, selezionare un campo, usare **MAIUSC + ALT + F3** per aggiungere quel campo al riquadro dei filtri, digitare i criteri del filtro, usare **CTRL + INVIO** per tornare alle righe, selezionare un altro campo e usare **ALT + F3** per filtrare tale valore.</span><span class="sxs-lookup"><span data-stu-id="56665-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="56665-217">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="56665-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="56665-218"><a name="FilterCriteria"> </a>Criteri e operatori di filtro</span><span class="sxs-lookup"><span data-stu-id="56665-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="56665-219">Quando si impostano criteri in un filtro, è possibile immettere tutti i numeri e le lettere in genere utilizzati nel campo.</span><span class="sxs-lookup"><span data-stu-id="56665-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="56665-220">È inoltre possibile utilizzare un set di simboli speciali come operatori per filtrare ulteriormente i risultati.</span><span class="sxs-lookup"><span data-stu-id="56665-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="56665-221">Le sezioni seguenti descrivono questi simboli e come utilizzarli come operatori nei filtri.</span><span class="sxs-lookup"><span data-stu-id="56665-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="56665-222">Per ulteriori informazioni su come filtrare date e orari, vedere [Lavorare con le date e gli orari del calendario ](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="56665-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="56665-223">Potrebbero verificarsi situazioni in cui il valore in base al quale si desidera filtrare contiene un simbolo che è un operatore.</span><span class="sxs-lookup"><span data-stu-id="56665-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="56665-224">Per ulteriori informazioni sulla gestione di queste situazioni, vedere [Filtrare in base a valori che contengono simboli](#symbols).</span><span class="sxs-lookup"><span data-stu-id="56665-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="56665-225">Se sono presenti più di 200 operatori in un singolo filtro, il sistema raggrupperà automaticamente alcune espressioni tra parentesi `()` ai fini del trattamento.</span><span class="sxs-lookup"><span data-stu-id="56665-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="56665-226">Ciò non ha alcun effetto sul filtro o sui risultati.</span><span class="sxs-lookup"><span data-stu-id="56665-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="56665-227">(..) Intervallo</span><span class="sxs-lookup"><span data-stu-id="56665-227">(..) Interval</span></span>

|<span data-ttu-id="56665-228">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-228">Sample Expression</span></span>|<span data-ttu-id="56665-229">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="56665-230">Numeri da 1100 a 2100</span><span class="sxs-lookup"><span data-stu-id="56665-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="56665-231">Fino a 2500 compreso.</span><span class="sxs-lookup"><span data-stu-id="56665-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="56665-232">Le date fino al 31/12/00 incluso</span><span class="sxs-lookup"><span data-stu-id="56665-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="56665-233">Informazioni sul periodo contabile 8 e successivi</span><span class="sxs-lookup"><span data-stu-id="56665-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="56665-234">Dalla data di inizio fino al 23-mese corrente-anno corrente ore 23:59:59</span><span class="sxs-lookup"><span data-stu-id="56665-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="56665-235">Dal 23-mese corrente-anno corrente ore 0:00:00 alla fine</span><span class="sxs-lookup"><span data-stu-id="56665-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="56665-236">Dal 22-mese corrente-anno corrente ore 0:00:00 fino al 23-mese corrente-anno corrente ore 23:59:59</span><span class="sxs-lookup"><span data-stu-id="56665-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="56665-237">(&#124;) Oppure</span><span class="sxs-lookup"><span data-stu-id="56665-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="56665-238">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-238">Sample Expression</span></span>|<span data-ttu-id="56665-239">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="56665-240">Numeri con 1200 o 1300</span><span class="sxs-lookup"><span data-stu-id="56665-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="56665-241">(<>) Diverso da</span><span class="sxs-lookup"><span data-stu-id="56665-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="56665-242">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-242">Sample Expression</span></span>|<span data-ttu-id="56665-243">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="56665-244">Tutti i numeri tranne 0</span><span class="sxs-lookup"><span data-stu-id="56665-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="56665-245">SQL Server Option consente di combinare questo simbolo con un'espressione contenente caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="56665-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="56665-246"><>A\*, ad esempio, si riferisce a un testo diverso da qualunque testo che inizia con la lettera A.</span><span class="sxs-lookup"><span data-stu-id="56665-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="56665-247">(>) Maggiore di</span><span class="sxs-lookup"><span data-stu-id="56665-247">(>) Greater than</span></span>  

|<span data-ttu-id="56665-248">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-248">Sample Expression</span></span>|<span data-ttu-id="56665-249">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="56665-250">Numeri maggiori di 1200</span><span class="sxs-lookup"><span data-stu-id="56665-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="56665-251">(>=) Maggiore di o uguale a</span><span class="sxs-lookup"><span data-stu-id="56665-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="56665-252">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-252">Sample Expression</span></span>|<span data-ttu-id="56665-253">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="56665-254">Numeri maggiori o uguali a 1200</span><span class="sxs-lookup"><span data-stu-id="56665-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="56665-255">(<) Minore di</span><span class="sxs-lookup"><span data-stu-id="56665-255">(<) Less than</span></span>  

|<span data-ttu-id="56665-256">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-256">Sample Expression</span></span>|<span data-ttu-id="56665-257">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="56665-258">Numeri minori di 1200</span><span class="sxs-lookup"><span data-stu-id="56665-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="56665-259">(<=) Minore di o uguale a</span><span class="sxs-lookup"><span data-stu-id="56665-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="56665-260">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-260">Sample Expression</span></span>|<span data-ttu-id="56665-261">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="56665-262">Numeri minori o uguali a 1200</span><span class="sxs-lookup"><span data-stu-id="56665-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="56665-263">(&) E</span><span class="sxs-lookup"><span data-stu-id="56665-263">(&) And</span></span>  

|<span data-ttu-id="56665-264">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-264">Sample Expression</span></span>|<span data-ttu-id="56665-265">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="56665-266">Numeri maggiori di 200 e minori di 1200.</span><span class="sxs-lookup"><span data-stu-id="56665-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="56665-267">('') Una corrispondenza esatta di carattere</span><span class="sxs-lookup"><span data-stu-id="56665-267">('') An exact character match</span></span>  

|<span data-ttu-id="56665-268">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-268">Sample Expression</span></span>|<span data-ttu-id="56665-269">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="56665-270">Testo con corrispondenza esatta a **man** e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="56665-271">(@) Senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="56665-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="56665-272">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-272">Sample Expression</span></span>|<span data-ttu-id="56665-273">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="56665-274">Testo che inizia con **man** e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="56665-275">(\*) Un numero indefinito di caratteri non noti</span><span class="sxs-lookup"><span data-stu-id="56665-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="56665-276">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-276">Sample Expression</span></span>|<span data-ttu-id="56665-277">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="56665-278">Testo contenente **Co** e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="56665-279">Testo che termina con **Co** e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="56665-280">Testo che inizia con **Co** e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="56665-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="56665-281">(?) Un carattere non noto</span><span class="sxs-lookup"><span data-stu-id="56665-281">(?) One unknown character</span></span>  

|<span data-ttu-id="56665-282">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-282">Sample Expression</span></span>|<span data-ttu-id="56665-283">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="56665-284">Testo come **Marco** o **Mario**</span><span class="sxs-lookup"><span data-stu-id="56665-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="56665-285">Espressioni di formato combinate</span><span class="sxs-lookup"><span data-stu-id="56665-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="56665-286">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-286">Sample Expression</span></span>|<span data-ttu-id="56665-287">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="56665-288">Include qualsiasi record con il numero 5999 oppure con un numero compreso tra 8100 e 8490.</span><span class="sxs-lookup"><span data-stu-id="56665-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="56665-289">Include record con un numero minore o uguale a 1299 oppure un numero uguale a 1400 o maggiore, vale a dire tutti i numeri tranne quelli compresi tra 1300 e 1399.</span><span class="sxs-lookup"><span data-stu-id="56665-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="56665-290">Include record con numeri maggiori di 50 e minori di 100, vale a dire i numeri compresi tra 51 e 99.</span><span class="sxs-lookup"><span data-stu-id="56665-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="56665-291">Filtrare in base a valori che contengono simboli</span><span class="sxs-lookup"><span data-stu-id="56665-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="56665-292">Potrebbero verificarsi casi in cui i valori dei campi contengono uno dei seguenti simboli:</span><span class="sxs-lookup"><span data-stu-id="56665-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="56665-293">(</span><span class="sxs-lookup"><span data-stu-id="56665-293">(</span></span>
- <span data-ttu-id="56665-294">)</span><span class="sxs-lookup"><span data-stu-id="56665-294">)</span></span>
- =
- <span data-ttu-id="56665-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="56665-295">&#124;</span></span>

<span data-ttu-id="56665-296">Se si desidera filtrare in base a uno qualsiasi di questi simboli, inserire l'espressione di filtro tra virgolette singole (`'<expression with symbol>'`).</span><span class="sxs-lookup"><span data-stu-id="56665-296">If you want to filter on any of these symbols, place the filter expression in single quotes (`'<expression with symbol>'`).</span></span> <span data-ttu-id="56665-297">Ad esempio, se si desidera filtrare i record che iniziano con il testo *J & V*, l'espressione di filtro è `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="56665-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="56665-298">Questo requisito non è necessario per altri simboli.</span><span class="sxs-lookup"><span data-stu-id="56665-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="56665-299"><a name="FilterTokens"> </a>Token di filtro</span><span class="sxs-lookup"><span data-stu-id="56665-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="56665-300">Quando si immettono i criteri di filtro, è anche possibile digitare parole che hanno un significato speciale, chiamate token di filtro.</span><span class="sxs-lookup"><span data-stu-id="56665-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="56665-301">Dopo aver immesso la parola token, la parola viene sostituita dal valore o dai valori che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="56665-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="56665-302">I token di filtro semplificano l'operazione di filtro riducendo la necessità di passare ad altre pagine per cercare i valori che si desidera aggiungere al filtro.</span><span class="sxs-lookup"><span data-stu-id="56665-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="56665-303">Le tabelle seguenti descrivono alcuni dei token che è possibile immettere a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="56665-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="56665-304">Un'organizzazione potrebbe utilizzare token personalizzati.</span><span class="sxs-lookup"><span data-stu-id="56665-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="56665-305">Per informazioni sul set completo di token disponibili o per aggiungere altri token personalizzati, contattare l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="56665-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="56665-306">Per informazioni tecniche vedere [Aggiunta di token di filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="56665-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="56665-307">(%me or %userid) Record assegnati all'utente</span><span class="sxs-lookup"><span data-stu-id="56665-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="56665-308">Utilizzare `%me` o `%userid` quando si filtrano i campi che contengono l'ID utente, quale il campo **Assegnato a ID utente**, per visualizzare tutti i record assegnati all'utente.</span><span class="sxs-lookup"><span data-stu-id="56665-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="56665-309">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-309">Sample Expression</span></span>|<span data-ttu-id="56665-310">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="56665-311">oppure</span><span class="sxs-lookup"><span data-stu-id="56665-311">or</span></span><br />`%userid`|<span data-ttu-id="56665-312">Record assegnati all'account utente.</span><span class="sxs-lookup"><span data-stu-id="56665-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="56665-313">(%mycustomers) clienti in Clienti personali</span><span class="sxs-lookup"><span data-stu-id="56665-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="56665-314">Utilizzare `%mycustomers` nel campo **Nessuno** cliente per visualizzare tutti i record per i clienti inclusi nell'elenco **Clienti personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="56665-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="56665-315">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-315">Sample Expression</span></span>|<span data-ttu-id="56665-316">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="56665-317">Clienti in **Clienti personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="56665-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="56665-318">(%myitems) Articoli in Articoli personali</span><span class="sxs-lookup"><span data-stu-id="56665-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="56665-319">Utilizzare `%myitems` nel campo **Nessuno** articolo per visualizzare tutti i record per gli articoli inclusi nell'elenco **Articoli personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="56665-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="56665-320">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-320">Sample Expression</span></span>|<span data-ttu-id="56665-321">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="56665-322">Articoli in **Articoli personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="56665-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="56665-323">(%myvendors) Fornitori in Fornitori personali</span><span class="sxs-lookup"><span data-stu-id="56665-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="56665-324">Utilizzare `%myvendors` nel campo **Nessuno** fornitori per visualizzare tutti i record per i fornitori inclusi nell'elenco **Fornitori personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="56665-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="56665-325">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="56665-325">Sample Expression</span></span>|<span data-ttu-id="56665-326">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="56665-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="56665-327">Fornitori in **Fornitori personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="56665-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="56665-328">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="56665-328">See Also</span></span>

[<span data-ttu-id="56665-329">Domande frequenti su ricerca e filtro</span><span class="sxs-lookup"><span data-stu-id="56665-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.yml)  
[<span data-ttu-id="56665-330">Salvare e personalizzare visualizzazioni elenco</span><span class="sxs-lookup"><span data-stu-id="56665-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="56665-331">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56665-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]