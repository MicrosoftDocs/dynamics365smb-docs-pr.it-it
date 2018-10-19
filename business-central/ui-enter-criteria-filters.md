---
title: Ricerca, filtro e ordinamento di elenchi | Documenti Microsoft
description: Utilizzare in modo efficiente gli elenchi cercando nei dati, ordinando colonne e perfezionando i risultati con potenti simboli di filtro e tasti di scelta rapida da tastiera.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1ee115c258c25d8b695a0394dbaa11247b9b8ab
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="022f6-103">Ricerca, filtro e ordinamento di elenchi</span><span class="sxs-lookup"><span data-stu-id="022f6-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="022f6-104">La ricerca e l'individuazione di record in un elenco risultano più semplici grazie a l'ordinamento, la ricerca e il filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="022f6-105">di ordinamento, ricerca e filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="022f6-106">È possibile collegare alcune o tutte le procedure contemporaneamente a rapidamente per trovare o analizzare rapidamente i dati.</span><span class="sxs-lookup"><span data-stu-id="022f6-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="022f6-107">Quando si visualizzano i dati come riquadri, è possibile cercare e utilizzare il filtro di base.</span><span class="sxs-lookup"><span data-stu-id="022f6-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="022f6-108">Per utilizzare il set completo di potenti funzionalità per l'ordinamento, la ricerca e il filtro, scegliere l'icona ![Mostra come lista](media/ui_show_as_list_icon.png "Icona Mostra come lista") per visualizzare in forma di elenco.</span><span class="sxs-lookup"><span data-stu-id="022f6-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="022f6-109">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="022f6-109">Sorting</span></span>
<span data-ttu-id="022f6-110">L'ordinamento consente di ottenere in modo semplice e rapido una panoramica dei dati.</span><span class="sxs-lookup"><span data-stu-id="022f6-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="022f6-111">Se si dispone di molti clienti, ad esempio, è possibile scegliere di ordinarli in base a **Nr. cliente**, **Cat. reg. cliente**, **Codice valuta**, **Codice paese** o **Identificativo fiscale** per ottenere la panoramica desiderata.</span><span class="sxs-lookup"><span data-stu-id="022f6-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="022f6-112">Per ordinare un elenco, fare clic sull'intestazione di una colonna per passare dall'ordine crescente a quello decrescente e viceversa, oppure scegliere la piccola freccia verso il basso nell'intestazione della colonna e scegliere **Crescente** o **Decrescente**.</span><span class="sxs-lookup"><span data-stu-id="022f6-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="022f6-113">L'ordinamento non è supportato nelle immagini, nei campi BLOB, in FlowFilter e nei campi che non appartengono a una tabella.</span><span class="sxs-lookup"><span data-stu-id="022f6-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="022f6-114">Ricerca</span><span class="sxs-lookup"><span data-stu-id="022f6-114">Searching</span></span>
<span data-ttu-id="022f6-115"><!--## Searching by using the Quick Filter --> Nella parte superiore di ogni pagina elenco, c'è un'icona ![Icona di ricerca](media/ui-search/search-list.png "Icona di ricerca") **Cerca** che fornisce un modo rapido e semplice per ridurre i record in un elenco e visualizzare solo quei record che contengono i dati che interessa vedere.</span><span class="sxs-lookup"><span data-stu-id="022f6-115"><!--## Searching by using the Quick Filter --> At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="022f6-116">Per cercare, è sufficiente selezionare l'icona di ricerca, quindi nella casella digitare il testo che si sta cercando.</span><span class="sxs-lookup"><span data-stu-id="022f6-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="022f6-117">È possibile immettere lettere, numeri e altri simboli.</span><span class="sxs-lookup"><span data-stu-id="022f6-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tune-the-search"></a><span data-ttu-id="022f6-118">Perfezionare la ricerca</span><span class="sxs-lookup"><span data-stu-id="022f6-118">Fine-tune the search</span></span>
<span data-ttu-id="022f6-119">In generale, la ricerca tenterà di far corrispondere il testo in tutti i campi, non distingue tra caratteri maiuscoli e minuscoli (in altre parole, maiuscole e minuscole) e corrisponderà al testo inserito nel campo (all'inizio, alla fine o al centro).</span><span class="sxs-lookup"><span data-stu-id="022f6-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anwhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="022f6-120">Tuttavia, è possibile effettuare una ricerca più precisa utilizzando i seguenti caratteri speciali:</span><span class="sxs-lookup"><span data-stu-id="022f6-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="022f6-121">Per trovare solo i valori dei campi che corrispondono esattamente all'intero testo e al caso, posizionare il testo di ricerca tra virgolette singole `''` (ad esempio `'man'`).</span><span class="sxs-lookup"><span data-stu-id="022f6-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="022f6-122">Per trovare valori di campo che iniziano con un determinato testo e corrispondono al caso, posizionare `*` dopo il testo di ricerca (ad esempio `man*`).</span><span class="sxs-lookup"><span data-stu-id="022f6-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="022f6-123">Per trovare valori di campo che terminano con un determinato testo e corrispondono al caso, posizionare `*` prima del testo di ricerca (ad esempio `*man`).</span><span class="sxs-lookup"><span data-stu-id="022f6-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="022f6-124">Quando si utilizza `''` o `*`, la ricerca è sensibile alla distinzione maiuscola/minuscola.</span><span class="sxs-lookup"><span data-stu-id="022f6-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="022f6-125">Se si desidera ignorare la distinzione tra maiuscole e minuscole, posizionare `@` prima del testo di ricerca, (ad esempio `@man*`).</span><span class="sxs-lookup"><span data-stu-id="022f6-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="022f6-126">Nella tabella seguente sono riportati alcuni esempi per spiegare come è possibile utilizzare la funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="022f6-126">The following table provides some examples to explain how you can use the search.</span></span>


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|<span data-ttu-id="022f6-127">Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="022f6-127">Search Criteria</span></span>|<span data-ttu-id="022f6-128">Trova…</span><span class="sxs-lookup"><span data-stu-id="022f6-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="022f6-129">oppure</span><span class="sxs-lookup"><span data-stu-id="022f6-129">or</span></span> <br />`Man`|<span data-ttu-id="022f6-130">Tutti i record con campi che contengono il testo **man**, indipendentemente dal caso.</span><span class="sxs-lookup"><span data-stu-id="022f6-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="022f6-131">Ad esempio, **Manchester**, **manual** o **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="022f6-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="022f6-132">Tutti i record con campi che contengono solo il testo **Man**, che corrisponde al caso.</span><span class="sxs-lookup"><span data-stu-id="022f6-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="022f6-133">Tutti i record con campi che iniziano con il testo <b>man</b>, con corrispondenza al caso.</span><span class="sxs-lookup"><span data-stu-id="022f6-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="022f6-134">Ad esempio, **Manchester**, ma non **manual** o **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="022f6-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="022f6-135">Tutti i record con campi che iniziano con il testo **man**, indipendentemente dal caso.</span><span class="sxs-lookup"><span data-stu-id="022f6-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="022f6-136">Ad esempio, **Manchester** e **manual**, ma non **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="022f6-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="022f6-137">Tutti i record con campi che finiscono con il testo **man**, indipendentemente dal caso.</span><span class="sxs-lookup"><span data-stu-id="022f6-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="022f6-138">Ad esempio, **Sportsman**, ma non **Manchester** o **manual**.</span><span class="sxs-lookup"><span data-stu-id="022f6-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="022f6-139">È possibile premere F3 per attivare e disattivare la casella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="022f6-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="022f6-140">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="022f6-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <a name="filtering"></a><span data-ttu-id="022f6-141">Filtro</span><span class="sxs-lookup"><span data-stu-id="022f6-141">Filtering</span></span>
<span data-ttu-id="022f6-142">l filtraggio fornisce un modo più avanzato e versatile per controllare quali record vengono visualizzati in un elenco.</span><span class="sxs-lookup"><span data-stu-id="022f6-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="022f6-143">Esistono due principali differenze tra la ricerca e il filtro, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="022f6-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="022f6-144">**Ricerca**</span><span class="sxs-lookup"><span data-stu-id="022f6-144">**Searching**</span></span> | <span data-ttu-id="022f6-145">**Filtri**</span><span class="sxs-lookup"><span data-stu-id="022f6-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="022f6-146">**Campi applicabili**</span><span class="sxs-lookup"><span data-stu-id="022f6-146">**Applicable fields**</span></span> | <span data-ttu-id="022f6-147">Cerca in tutti i campi visibili nella pagina.</span><span class="sxs-lookup"><span data-stu-id="022f6-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="022f6-148">Filtra uno o più campi singolarmente, selezionando da qualsiasi campo sulla tabella, inclusi i campi che non sono visibili sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="022f6-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="022f6-149">**Corrispondenza**</span><span class="sxs-lookup"><span data-stu-id="022f6-149">**Matching**</span></span> | <span data-ttu-id="022f6-150">Visualizza i record con campi che corrispondono al testo di ricerca, indipendentemente dal caso o dal posizionamento del testo.</span><span class="sxs-lookup"><span data-stu-id="022f6-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="022f6-151">Visualizza i record in cui il campo corrisponde esattamente al filtro e fa distinzione tra maiuscole e minuscole, a meno che non vengano inseriti simboli di filtro speciali.</span><span class="sxs-lookup"><span data-stu-id="022f6-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="022f6-152">Il filtro consente di visualizzare record per account o clienti specifici, date, importi e altre informazioni specificando i criteri di filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="022f6-153">Solo i record che rispondono a tali criteri vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="022f6-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="022f6-154">Se si specificano i criteri per più campi, verranno visualizzati solo i record che soddisfano tutti i criteri.</span><span class="sxs-lookup"><span data-stu-id="022f6-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="022f6-155">Utilizzo del riquadro dei filtri</span><span class="sxs-lookup"><span data-stu-id="022f6-155">Working in the filter pane</span></span>
<span data-ttu-id="022f6-156">Il riquadro dei filtri visualizza i filtri correnti per un elenco e consente di impostare i propri filtri personalizzati su uno o più campi.</span><span class="sxs-lookup"><span data-stu-id="022f6-156">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="022f6-157">La figura seguente mostra un riquadro dei filtri di esempio per un elenco di offerte di vendita.</span><span class="sxs-lookup"><span data-stu-id="022f6-157">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="022f6-158">![Panoramica del riquadro Filtro ](media/filter-pane-overview.png "Icona Filtro")</span><span class="sxs-lookup"><span data-stu-id="022f6-158">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="022f6-159">Per visualizzare il riquadro dei filtri, utilizzare i tasti di scelta rapida **MAIUSC+F3**.</span><span class="sxs-lookup"><span data-stu-id="022f6-159">To display the filter pane, use the **Shift+F3** keyboard shortcut.</span></span> <span data-ttu-id="022f6-160">Per gli elenchi all'interno di Gestione ruolo utente, è possibile anche scegliere la freccia verso il basso accanto al titolo della pagina nella barra di spostamento sopra l'elenco, quindi scegliere **Mostra riquadro filtri**.</span><span class="sxs-lookup"><span data-stu-id="022f6-160">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane**.</span></span>

<span data-ttu-id="022f6-161">![Mostra riquadro Filtri](media/open-filter-pane.png "Mostra riquadro Filtri")</span><span class="sxs-lookup"><span data-stu-id="022f6-161">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="022f6-162">Un riquadro dei filtri è diviso in tre sezioni: **Visualizzazioni**, **Filtra elenco per** e **Filtra totali per**:</span><span class="sxs-lookup"><span data-stu-id="022f6-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="022f6-163">**Visualizzazioni**</span><span class="sxs-lookup"><span data-stu-id="022f6-163">**Views**</span></span>

  <span data-ttu-id="022f6-164">Alcuni elenchi includono la sezione **Visualizzazioni**.</span><span class="sxs-lookup"><span data-stu-id="022f6-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="022f6-165">Le visualizzazioni sono variazioni dell'elenco che sono state preconfigurate con i filtri.</span><span class="sxs-lookup"><span data-stu-id="022f6-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="022f6-166">Per passare a una diversa visualizzazione del tuo elenco, selezionare semplicemente un altro collegamento.</span><span class="sxs-lookup"><span data-stu-id="022f6-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="022f6-167">È possibile modificare temporaneamente i filtri su una visualizzazione, ma le modifiche non verranno salvate in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="022f6-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="022f6-168">**Filtra elenco per**</span><span class="sxs-lookup"><span data-stu-id="022f6-168">**Filter list by**</span></span>

  <span data-ttu-id="022f6-169">La sezione **Filtra elenco per:** consente di aggiungere filtri in campi specifici per ridurre il numero di record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="022f6-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="022f6-170">Per aggiungere un filtro, selezionare **+ Filtro** , selezionare il campo che si desidera filtrare da qualsiasi campo nella tabella, quindi inserire i criteri di filtro nella casella.</span><span class="sxs-lookup"><span data-stu-id="022f6-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="022f6-171">**Filtra totali per**</span><span class="sxs-lookup"><span data-stu-id="022f6-171">**Filter totals by**</span></span>

  <span data-ttu-id="022f6-172">Alcuni elenchi che visualizzano campi calcolati, come importi e quantità, includeranno la sezione **Filtra totali per** in cui è possibile impostare varie dimensioni che influenzano i calcoli.</span><span class="sxs-lookup"><span data-stu-id="022f6-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="022f6-173">Ad esempio, è possibile analizzare rapidamente il piano dei conti filtrando gli importi in un periodo specifico oppure è possibile visualizzare i totali per gli ordini di vendita solo da un determinato magazzino.</span><span class="sxs-lookup"><span data-stu-id="022f6-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="022f6-174">Per aggiungere un filtro, selezionare **+ Filtro**, selezionare una delle dimensioni predefinite e quindi aggiungere i criteri di filtro nella casella.</span><span class="sxs-lookup"><span data-stu-id="022f6-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="022f6-175">I filtri nella sezione **Filtra totali per** sono controllati da FlowFilter nella progettazione della pagina.</span><span class="sxs-lookup"><span data-stu-id="022f6-175">Filters in the **Filter totals by** section are controlled by FlowFilters in the page design.</span></span> <span data-ttu-id="022f6-176">Per informazioni tecniche, vedere [FlowFilter](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="022f6-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="022f6-177">Immissione dei criteri di filtro nel riquadro dei filtri</span><span class="sxs-lookup"><span data-stu-id="022f6-177">Entering filter criteria in the filter pane</span></span>
<span data-ttu-id="022f6-178">Per selezionare un campo da filtrare, effettuare una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="022f6-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="022f6-179">Nel riquadro dei filtri, scegliere **+ Campo**.</span><span class="sxs-lookup"><span data-stu-id="022f6-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="022f6-180">Digitare il nome del campo che si desidera filtrare o selezionare un campo dal menu che visualizza tutti i campi nella tabella.</span><span class="sxs-lookup"><span data-stu-id="022f6-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="022f6-181">In una colonna, scegliere la freccia verso il basso, quindi selezionare **Filtra...**. Questo aprirà il riquadro dei filtri e aggiungerà la colonna al riquadro dei filtri.</span><span class="sxs-lookup"><span data-stu-id="022f6-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="022f6-182">A questo punto è possibile immettere o selezionare i criteri di filtro nella casella.</span><span class="sxs-lookup"><span data-stu-id="022f6-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="022f6-183">Il tipo di campo filtrato determina i criteri che si possono inserire.</span><span class="sxs-lookup"><span data-stu-id="022f6-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="022f6-184">Ad esempio, il filtro di un campo con valori fissi consente solo di scegliere da tali valori.</span><span class="sxs-lookup"><span data-stu-id="022f6-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="022f6-185">Per ulteriori informazioni sui simboli speciali del filtro, vedere [Criteri e simboli di filtro](#FilterCriteria) e [Token di filtro](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="022f6-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="022f6-186">Le colonne che hanno già dei filtri sono indicate dall'intestazione dall'![icona Filtro](media/ui-search/filter-icon.png "icona Filtro") nell'intestazione della colonna.</span><span class="sxs-lookup"><span data-stu-id="022f6-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="022f6-187">Per rimuovere un filtro, selezionare l'intestazione della colonna, quindi **Cancella filtro**.</span><span class="sxs-lookup"><span data-stu-id="022f6-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-the-filter-pane"></a><span data-ttu-id="022f6-188">Immissione dei criteri di filtro senza il riquadro dei filtri</span><span class="sxs-lookup"><span data-stu-id="022f6-188">Entering filter criteria without the filter pane</span></span>
<span data-ttu-id="022f6-189">È possibile specificare semplici filtri direttamente all'interno dell'elenco senza dover utilizzare il riquadro dei filtri.</span><span class="sxs-lookup"><span data-stu-id="022f6-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="022f6-190">Con qualsiasi campo selezionato su una riga, usa **ALT+F3** per visualizzare solo i record che hanno lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="022f6-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="022f6-191">È quindi possibile selezionare un altro campo e utilizzare di nuovo gli stessi tasti di scelta rapida per continuare a perfezionare i filtri.</span><span class="sxs-lookup"><span data-stu-id="022f6-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="022f6-192">Se il campo selezionato è già filtrato, **ALT + F3** cancellerà quel filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="022f6-193">Accelerare la ricerca e l'analisi dei dati utilizzando combinazioni di tasti di scelta rapida da tastiera.</span><span class="sxs-lookup"><span data-stu-id="022f6-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="022f6-194">Ad esempio, selezionare un campo, usare **MAIUSC + ALT + F3** per aggiungere quel campo al riquadro dei filtri, digitare i criteri del filtro, usare **CTRL + INVIO** per tornare alle righe, selezionare un altro campo e usare **ALT + F3** per filtrare tale valore.</span><span class="sxs-lookup"><span data-stu-id="022f6-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="022f6-195">Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="022f6-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="022f6-196"><a name="FilterCriteria"> </a>Criteri e simboli di filtro</span><span class="sxs-lookup"><span data-stu-id="022f6-196"><a name="FilterCriteria"> </a>Filter criteria and symbols</span></span>
<span data-ttu-id="022f6-197">Quando si impostano criteri in un filtro, è possibile immettere tutti i numeri e le lettere in genere consentiti nel campo.</span><span class="sxs-lookup"><span data-stu-id="022f6-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="022f6-198">È inoltre possibile utilizzare alcuni simboli speciali per filtrare ulteriormente i risultati.</span><span class="sxs-lookup"><span data-stu-id="022f6-198">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="022f6-199">Nella tabella seguente sono inclusi i simboli che è possibile utilizzare nei filtri.</span><span class="sxs-lookup"><span data-stu-id="022f6-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="022f6-200">Per date e ore, è anche possibile fare riferimento a [Utilizzo di date e orari del calendario](ui-enter-date-ranges.md) per informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="022f6-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="022f6-201">In alcuni casi è possibile che alcuni valori campo contengano tali simboli e che si intenda filtrarli.</span><span class="sxs-lookup"><span data-stu-id="022f6-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="022f6-202">Per farlo, è necessario includere l'espressione di filtro contenente il simbolo tra virgolette (").</span><span class="sxs-lookup"><span data-stu-id="022f6-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="022f6-203">Ad esempio, se si desidera filtrare i record che iniziano con il testo *S&R*, l'espressione di filtro è `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="022f6-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>  

### <a name="-interval"></a><span data-ttu-id="022f6-204">(..) Intervallo</span><span class="sxs-lookup"><span data-stu-id="022f6-204">(..) Interval</span></span>

|<span data-ttu-id="022f6-205">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-205">Sample Expression</span></span>|<span data-ttu-id="022f6-206">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-206">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="022f6-207">Numeri da 1100 a 2100</span><span class="sxs-lookup"><span data-stu-id="022f6-207">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="022f6-208">Fino a 2500 compreso.</span><span class="sxs-lookup"><span data-stu-id="022f6-208">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="022f6-209">Le date fino al 31/12/00 incluso</span><span class="sxs-lookup"><span data-stu-id="022f6-209">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="022f6-210">Informazioni sul periodo contabile 8 e successivi</span><span class="sxs-lookup"><span data-stu-id="022f6-210">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="022f6-211">Dalla data di inizio fino al 23-mese corrente-anno corrente ore 23:59:59</span><span class="sxs-lookup"><span data-stu-id="022f6-211">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="022f6-212">Dal 23-mese corrente-anno corrente ore 0:00:00 alla fine</span><span class="sxs-lookup"><span data-stu-id="022f6-212">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="022f6-213">Dal 22-mese corrente-anno corrente ore 0:00:00 fino al 23-mese corrente-anno corrente ore 23:59:59</span><span class="sxs-lookup"><span data-stu-id="022f6-213">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="022f6-214">(&#124;) Oppure</span><span class="sxs-lookup"><span data-stu-id="022f6-214">(&#124;) Either/or</span></span>  

|<span data-ttu-id="022f6-215">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-215">Sample Expression</span></span>|<span data-ttu-id="022f6-216">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-216">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="022f6-217">\`1200</span><span class="sxs-lookup"><span data-stu-id="022f6-217">\`1200</span></span>|<span data-ttu-id="022f6-218">1300\`</span><span class="sxs-lookup"><span data-stu-id="022f6-218">1300\`</span></span>|<span data-ttu-id="022f6-219">Numeri con 1200 o 1300</span><span class="sxs-lookup"><span data-stu-id="022f6-219">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="022f6-220">(<>) Diverso da</span><span class="sxs-lookup"><span data-stu-id="022f6-220">(<>) Not equal to</span></span>  

|<span data-ttu-id="022f6-221">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-221">Sample Expression</span></span>|<span data-ttu-id="022f6-222">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="022f6-223">Tutti i numeri tranne 0</span><span class="sxs-lookup"><span data-stu-id="022f6-223">All numbers except 0</span></span><br /><br /> <span data-ttu-id="022f6-224">SQL Server Option consente di combinare questo simbolo con un'espressione contenente caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="022f6-224">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="022f6-225"><>A\*, ad esempio, si riferisce a un testo diverso da qualunque testo che inizia con la lettera A.</span><span class="sxs-lookup"><span data-stu-id="022f6-225">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="022f6-226">(>) Maggiore di</span><span class="sxs-lookup"><span data-stu-id="022f6-226">(>) Greater than</span></span>  

|<span data-ttu-id="022f6-227">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-227">Sample Expression</span></span>|<span data-ttu-id="022f6-228">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-228">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="022f6-229">Numeri maggiori di 1200</span><span class="sxs-lookup"><span data-stu-id="022f6-229">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="022f6-230">(>=) Maggiore di o uguale a</span><span class="sxs-lookup"><span data-stu-id="022f6-230">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="022f6-231">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-231">Sample Expression</span></span>|<span data-ttu-id="022f6-232">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="022f6-233">Numeri maggiori o uguali a 1200</span><span class="sxs-lookup"><span data-stu-id="022f6-233">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="022f6-234">(<) Minore di</span><span class="sxs-lookup"><span data-stu-id="022f6-234">(<) Less than</span></span>  

|<span data-ttu-id="022f6-235">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-235">Sample Expression</span></span>|<span data-ttu-id="022f6-236">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-236">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="022f6-237">Numeri minori di 1200</span><span class="sxs-lookup"><span data-stu-id="022f6-237">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="022f6-238">(<=) Minore di o uguale a</span><span class="sxs-lookup"><span data-stu-id="022f6-238">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="022f6-239">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-239">Sample Expression</span></span>|<span data-ttu-id="022f6-240">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-240">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="022f6-241">Numeri minori o uguali a 1200</span><span class="sxs-lookup"><span data-stu-id="022f6-241">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="022f6-242">(&) E</span><span class="sxs-lookup"><span data-stu-id="022f6-242">(&) And</span></span>  

|<span data-ttu-id="022f6-243">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-243">Sample Expression</span></span>|<span data-ttu-id="022f6-244">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-244">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="022f6-245">Numeri maggiori di 200 e minori di 1200.</span><span class="sxs-lookup"><span data-stu-id="022f6-245">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="022f6-246">('') Una corrispondenza esatta di carattere</span><span class="sxs-lookup"><span data-stu-id="022f6-246">('') An exact character match</span></span>  

|<span data-ttu-id="022f6-247">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-247">Sample Expression</span></span>|<span data-ttu-id="022f6-248">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-248">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="022f6-249">Testo con corrispondenza esatta a man e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="022f6-249">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="022f6-250">(@) Senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="022f6-250">(@) Case insensitive</span></span>  

|<span data-ttu-id="022f6-251">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-251">Sample Expression</span></span>|<span data-ttu-id="022f6-252">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-252">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="022f6-253">Testo che inizia con man e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="022f6-253">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="022f6-254">(\*) Un numero indefinito di caratteri non noti</span><span class="sxs-lookup"><span data-stu-id="022f6-254">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="022f6-255">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-255">Sample Expression</span></span>|<span data-ttu-id="022f6-256">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-256">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="022f6-257">Testo contenente "Co" per il quale viene osservata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="022f6-257">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="022f6-258">Testo che termina con "Co" e per il quale viene osservata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="022f6-258">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="022f6-259">Testo che inizia con "Co" e per il quale viene osservata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="022f6-259">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="022f6-260">Non è possibile utilizzare `*` per filtrare i campi di opzione (enumerazione), ad esempio il campo **Stato** negli ordini di vendita.</span><span class="sxs-lookup"><span data-stu-id="022f6-260">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="022f6-261">Per immettere un filtro per il tipo di campo, è possibile immettere il valore numerico come parametro di filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-261">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="022f6-262">Ad esempio, nel campo **Stato** in un ordine di vendita con i valori **Aperto**, **Rilasciato**, **In attesa di approvazione** e **Pagamento anticipato in sospeso,** utilizzare i valori `0`, `1`, `2` e `3` per filtrare in base a queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="022f6-262">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="022f6-263">(?) Un carattere non noto</span><span class="sxs-lookup"><span data-stu-id="022f6-263">(?) One unknown character</span></span>  

|<span data-ttu-id="022f6-264">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-264">Sample Expression</span></span>|<span data-ttu-id="022f6-265">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="022f6-266">Testo come Marco o Mario</span><span class="sxs-lookup"><span data-stu-id="022f6-266">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="022f6-267">Espressioni di formato combinate</span><span class="sxs-lookup"><span data-stu-id="022f6-267">Combined format expressions</span></span>  

|<span data-ttu-id="022f6-268">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-268">Sample Expression</span></span>|<span data-ttu-id="022f6-269">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="022f6-270">\`5999</span><span class="sxs-lookup"><span data-stu-id="022f6-270">\`5999</span></span>|<span data-ttu-id="022f6-271">8100..8490\`</span><span class="sxs-lookup"><span data-stu-id="022f6-271">8100..8490\`</span></span>|<span data-ttu-id="022f6-272">Include qualsiasi record con il numero 5999 oppure con un numero compreso tra 8100 e 8490.</span><span class="sxs-lookup"><span data-stu-id="022f6-272">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="022f6-273">\`..1299</span><span class="sxs-lookup"><span data-stu-id="022f6-273">\`..1299</span></span>|<span data-ttu-id="022f6-274">1400..\`</span><span class="sxs-lookup"><span data-stu-id="022f6-274">1400..\`</span></span>|<span data-ttu-id="022f6-275">Include record con un numero minore o uguale a 1299 oppure un numero uguale a 1400 o maggiore, vale a dire tutti i numeri tranne quelli compresi tra 1300 e 1399.</span><span class="sxs-lookup"><span data-stu-id="022f6-275">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="022f6-276">Include record con numeri maggiori di 50 e minori di 100, vale a dire i numeri compresi tra 51 e 99.</span><span class="sxs-lookup"><span data-stu-id="022f6-276">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="022f6-277"><a name="FilterTokens"> </a>Token di filtro</span><span class="sxs-lookup"><span data-stu-id="022f6-277"><a name="FilterTokens"> </a>Filter tokens</span></span>
<span data-ttu-id="022f6-278">Quando si immettono i criteri di filtro, è anche possibile digitare parole che hanno un significato speciale, chiamate token di filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-278">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="022f6-279">Dopo aver immesso la parola token, la parola viene sostituita dal valore o dai valori che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="022f6-279">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="022f6-280">Ciò semplifica il filtro riducendo la necessità di passare ad altre pagine per cercare i valori che si desidera aggiungere al filtro.</span><span class="sxs-lookup"><span data-stu-id="022f6-280">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="022f6-281">Le tabelle seguenti descrivono alcuni dei token che è possibile immettere a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="022f6-281">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="022f6-282">Un'organizzazione potrebbe utilizzare token personalizzati.</span><span class="sxs-lookup"><span data-stu-id="022f6-282">Your organization may use custom tokens.</span></span> <span data-ttu-id="022f6-283">Per informazioni sul set completo di token disponibili o per aggiungere altri token personalizzati, contattare l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="022f6-283">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="022f6-284">Per informazioni tecniche vedere [Aggiunta di token di filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span><span class="sxs-lookup"><span data-stu-id="022f6-284">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="022f6-285">(%me or %userid) Record assegnati all'utente</span><span class="sxs-lookup"><span data-stu-id="022f6-285">(%me or %userid) Records assigned to you</span></span>

<span data-ttu-id="022f6-286">Utilizzare `%me` o `%userid` quando si filtrano i campi che contengono l'ID utente, quale il campo **Assegnato a ID utente**, per visualizzare tutti i record assegnati all'utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-286">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="022f6-287">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-287">Sample Expression</span></span>|<span data-ttu-id="022f6-288">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-288">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="022f6-289">oppure</span><span class="sxs-lookup"><span data-stu-id="022f6-289">or</span></span><br />`%userid`|<span data-ttu-id="022f6-290">Record assegnati all'account utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-290">Records the are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="022f6-291">(%mycustomers) clienti in Clienti personali</span><span class="sxs-lookup"><span data-stu-id="022f6-291">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="022f6-292">Utilizzare `%mycustomers` nel campo **Nessuno** cliente per visualizzare tutti i record per i clienti inclusi nell'elenco **Clienti personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-292">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="022f6-293">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-293">Sample Expression</span></span>|<span data-ttu-id="022f6-294">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-294">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="022f6-295">Clienti in **Clienti personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-295">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="022f6-296">(%myitems) Articoli in Articoli personali</span><span class="sxs-lookup"><span data-stu-id="022f6-296">(%myitems) Items in My Items</span></span>

<span data-ttu-id="022f6-297">Utilizzare `%myitems` nel campo **Nessuno** articolo per visualizzare tutti i record per gli articoli inclusi nell'elenco **Articoli personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-297">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="022f6-298">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-298">Sample Expression</span></span>|<span data-ttu-id="022f6-299">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-299">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="022f6-300">Articoli in **Articoli personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-300">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="022f6-301">(%myvendors) Fornitori in Fornitori personali</span><span class="sxs-lookup"><span data-stu-id="022f6-301">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="022f6-302">Utilizzare `%myvendors` nel campo **Nessuno** fornitori per visualizzare tutti i record per i fornitori inclusi nell'elenco **Fornitori personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-302">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="022f6-303">espressione di esempio</span><span class="sxs-lookup"><span data-stu-id="022f6-303">Sample Expression</span></span>|<span data-ttu-id="022f6-304">Record visualizzati</span><span class="sxs-lookup"><span data-stu-id="022f6-304">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="022f6-305">Fornitori in **Fornitori personali** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="022f6-305">Venders in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="022f6-306">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="022f6-306">See Also</span></span>
<span data-ttu-id="022f6-307">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="022f6-307">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="022f6-308">Domande comuni su ricerca e filtro</span><span class="sxs-lookup"><span data-stu-id="022f6-308">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)

