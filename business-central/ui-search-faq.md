---
title: Domande frequenti relative alle informazioni | Documenti Microsoft
description: Questo articolo risponde alle domande che i partner e i clienti spesso chiedono sulla nuova funzione delle informazioni.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 70ab7fb07cda5ce9d86b3f39dd14321829e85a52
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="tell-me-faq"></a><span data-ttu-id="8a977-103">Domande frequenti relative alle informazioni</span><span class="sxs-lookup"><span data-stu-id="8a977-103">Tell Me FAQ</span></span>
<span data-ttu-id="8a977-104">Questo argomento risponde alle domande che gli utenti avanzati spesso pongono sulla nuova funzionalità delle informazioni, che ha sostituito la precedente funzionalità di ricerca della pagina nota come **Trova pagine e report**.</span><span class="sxs-lookup"><span data-stu-id="8a977-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="8a977-105">Tutte le azioni della pagina corrente sono individuabili nelle informazioni?</span><span class="sxs-lookup"><span data-stu-id="8a977-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="8a977-106">No.</span><span class="sxs-lookup"><span data-stu-id="8a977-106">No.</span></span> <span data-ttu-id="8a977-107">Le azioni in parti, come la parte relativa alle righe di vendita o riquadri Dettaglio informazioni, non vengono visualizzate nelle informazioni.</span><span class="sxs-lookup"><span data-stu-id="8a977-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="8a977-108">I risultati vengono filtrati in base alle autorizzazioni?</span><span class="sxs-lookup"><span data-stu-id="8a977-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="8a977-109">Se l'utente non dispone di AccessByPermissions, le azioni non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="8a977-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="8a977-110">Tuttavia, le pagine e i report vengono visualizzati nei risultati ma richiedono che l'utente disponga dell'autorizzazione per accedervi.</span><span class="sxs-lookup"><span data-stu-id="8a977-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="8a977-111">Un messaggio verrà visualizzato se l'utente non dispone dell'autorizzazione per visualizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8a977-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="8a977-112">Le informazioni mostrano i contenuti delle personalizzazioni o delle estensioni di terze parti installate?</span><span class="sxs-lookup"><span data-stu-id="8a977-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="8a977-113">Le azioni, le pagine e i report che provengono da estensioni vengono acquisiti dalle informazioni, ma non la documentazione della guida personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8a977-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="8a977-114">Per informazioni tecniche su come rendere visibili le pagine e i report personalizzati, vedere [Aggiunta di pagine e report alla ricerca](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="8a977-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="8a977-115">Quali sono le differenze dalla funzionalità precedente di ricerca della pagina?</span><span class="sxs-lookup"><span data-stu-id="8a977-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="8a977-116">La ricerca della pagina si è evoluta nelle informazione per aiutare a svolgere rapidamente il lavoro.</span><span class="sxs-lookup"><span data-stu-id="8a977-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="8a977-117">La ricerca della pagina potrebbe essere utile per passare a pagine o report.</span><span class="sxs-lookup"><span data-stu-id="8a977-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="8a977-118">A livello tecnico, le informazioni non si basano più sul concetto di MenuSuite precedente.</span><span class="sxs-lookup"><span data-stu-id="8a977-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="8a977-119">Utilizzo [!INCLUDE[d365fin](includes/d365fin_md.md)] in locale.</span><span class="sxs-lookup"><span data-stu-id="8a977-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8a977-120">La funzionalità delle informazioni è inclusa.</span><span class="sxs-lookup"><span data-stu-id="8a977-120">Does that include Tell Me?</span></span>
<span data-ttu-id="8a977-121">È possibile utilizzare le informazioni nel client Web locale per trovare azioni, pagine e report, ma non documentazione.</span><span class="sxs-lookup"><span data-stu-id="8a977-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation.</span></span> <span data-ttu-id="8a977-122">Gli utenti che si connettono a [!INCLUDE[d365fin](includes/d365fin_md.md)] dal client Dynamics NAV continuano a utilizzare la ricerca della pagina.</span><span class="sxs-lookup"><span data-stu-id="8a977-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="8a977-123">Le informazioni sono disponibili per tutti i fattori di forma?</span><span class="sxs-lookup"><span data-stu-id="8a977-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="8a977-124">Le informazioni sono disponibili solo nel client Web o nell'app desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="8a977-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="8a977-125">I risultati della documentazione sono disponibili in tutte le lingue?</span><span class="sxs-lookup"><span data-stu-id="8a977-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="8a977-126">Gli articoli della guida vengono visualizzati nella lingua specificata in **Impostazioni personali**, se la guida è disponibile in tale lingua.</span><span class="sxs-lookup"><span data-stu-id="8a977-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a977-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a977-127">See Also</span></span>  
[<span data-ttu-id="8a977-128">Individuazione di funzionalità e informazioni</span><span class="sxs-lookup"><span data-stu-id="8a977-128">Finding Features and Information</span></span>](ui-search.md)

