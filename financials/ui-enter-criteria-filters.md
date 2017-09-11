---
title: Definire criteri di ricerca nei filtri | Documenti Microsoft
description: Descrive come utilizzare i filtri, come il Filtro rapido, per perfezionare i risultati nella ricerca dei dati.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="46ff4-103">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="46ff4-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="46ff4-104">Quando si desidera cercare dei dati, ad esempio nomi e indirizzi dei clienti o gruppi di prodotti, si immettono dei criteri.</span><span class="sxs-lookup"><span data-stu-id="46ff4-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="46ff4-105">Nei criteri di ricerca è possibile utilizzare nel campo specificato tutti i numeri e le lettere che normalmente si utilizzano.</span><span class="sxs-lookup"><span data-stu-id="46ff4-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="46ff4-106">È inoltre possibile utilizzare alcuni simboli speciali per filtrare ulteriormente i risultati.</span><span class="sxs-lookup"><span data-stu-id="46ff4-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="46ff4-107">Ricerca con l'utilizzo di Filtro rapido</span><span class="sxs-lookup"><span data-stu-id="46ff4-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="46ff4-108">È possibile aggiungere filtri a tutte le pagine, utilizzando la funzione Filtro rapido.</span><span class="sxs-lookup"><span data-stu-id="46ff4-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="46ff4-109">Questa funzione viene abilitata scegliendo l'icona della lente di ingrandimento che si trova nell'angolo superiore destro di una pagina.</span><span class="sxs-lookup"><span data-stu-id="46ff4-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="46ff4-110">Questo tipo di filtro viene utilizzato per una rapida immissione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="46ff4-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="46ff4-111">Il Filtro rapido consente di filtrare i dati facilmente immettendo testo normale, ma non offre molte opzioni di criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="46ff4-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="46ff4-112">A seconda se si immette il testo normale o il testo con i simboli, il filtro rapido funziona in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="46ff4-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="46ff4-113">Se si immette testo normale nei criteri di ricerca, i criteri di ricerca vengono interpretati come una ricerca senza distinzione tra maiuscole e minuscole contenente un determinato testo.</span><span class="sxs-lookup"><span data-stu-id="46ff4-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="46ff4-114">Se si immette del testo includendo dei simboli nei criteri di ricerca, i criteri di ricerca vengono interpretati esattamente così come sono stati immessi e la ricerca rileva la differenza tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="46ff4-115">Criteri di Filtro rapido</span><span class="sxs-lookup"><span data-stu-id="46ff4-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="46ff4-116">Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="46ff4-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="46ff4-117">Interpretato come...</span><span class="sxs-lookup"><span data-stu-id="46ff4-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="46ff4-118">Reso come...</span><span class="sxs-lookup"><span data-stu-id="46ff4-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="46ff4-119">man</span><span class="sxs-lookup"><span data-stu-id="46ff4-119">man</span></span></TD>
    <TD><span data-ttu-id="46ff4-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="46ff4-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="46ff4-121">Tutti i record che contengono il testo <b>man</b> e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="46ff4-122">se</span><span class="sxs-lookup"><span data-stu-id="46ff4-122">se</span></span></TD>
    <TD><span data-ttu-id="46ff4-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="46ff4-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="46ff4-124">Tutti i record che contengono il testo <b>e</b> e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="46ff4-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="46ff4-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="46ff4-126">Inizia con <b>Man</b> e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="46ff4-127">Tutti i record che iniziano con il testo <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="46ff4-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="46ff4-128">'man'</span><span class="sxs-lookup"><span data-stu-id="46ff4-128">'man'</span></span></TD>
    <TD><span data-ttu-id="46ff4-129">Un testo esatto e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="46ff4-130">Tutti i record che corrispondono esattamente a <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="46ff4-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="46ff4-131">@man*</span><span class="sxs-lookup"><span data-stu-id="46ff4-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="46ff4-132">Inizia con e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="46ff4-133">Tutti i record che iniziano con <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="46ff4-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="46ff4-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="46ff4-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="46ff4-135">Termina con e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46ff4-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="46ff4-136">Tutti i record che terminano con <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="46ff4-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="46ff4-137">Non è possibile utilizzare i carattere jolly quando si filtrano i campi di enumerazione, come il campo **Stato** negli ordini di vendita.</span><span class="sxs-lookup"><span data-stu-id="46ff4-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="46ff4-138">Per immettere un filtro per il tipo di campo, è possibile immettere il valore numerico come parametro di filtro.</span><span class="sxs-lookup"><span data-stu-id="46ff4-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="46ff4-139">Ad esempio, nel campo **Stato** in un ordine di vendita con i valori **Aperto**, **Rilasciato**, **In attesa di approvazione**e **Pagamento anticipato in sospeso**, utilizzare i valori **0**, **1**, **2**e **3** per filtrare in base a queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="46ff4-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="46ff4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46ff4-140">See Also</span></span>
<span data-ttu-id="46ff4-141">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46ff4-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

