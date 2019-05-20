---
title: Personalizzare segnali visivi sull'attività di una pila | Documenti Microsoft
description: Impostare un indicatore colorato sulla sezione Pila per fornire un segnale visivo per personalizzato per l'attività di una pila.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: f79f1a65ee17d8ca46a8ecf1cd9d49c5246bef63
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248113"
---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="0c19f-103">Impostare un indicatore colorato nelle pile</span><span class="sxs-lookup"><span data-stu-id="0c19f-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="0c19f-104">È possibile impostare le pile che vengono visualizzate in Gestione ruolo utente degli utenti in modo che includano un indicatore che cambia colore in base ai valori dei dati presenti nelle pile.</span><span class="sxs-lookup"><span data-stu-id="0c19f-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="0c19f-105">L'indicatore viene visualizzato come una barra colorata lungo il bordo superiore della pila.</span><span class="sxs-lookup"><span data-stu-id="0c19f-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="0c19f-106">Fornisce un segnale visivo dello stato dell'attività della pila, che può indicare le condizioni favorevoli o sfavorevoli per spingere l'utente a intraprendere un'azione.</span><span class="sxs-lookup"><span data-stu-id="0c19f-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="0c19f-107">Ad esempio, se una pila visualizza le fatture di vendita in corso, è possibile impostare l'indicatore in modo che appaia verde (favorevole) quando il totale delle fatture di vendita in corso è minore di 10 e rosso (sfavorevole) quando il totale è maggiore di 20.</span><span class="sxs-lookup"><span data-stu-id="0c19f-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="0c19f-108">Nella pagina **Setup pila**, si impostano gli indicatori di tutte le pile disponibili nel database della società.</span><span class="sxs-lookup"><span data-stu-id="0c19f-108">From the **Cue Setup** page, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="0c19f-109">Per impostare l'indicatore, specificare fino a due valori di soglia che definiscono tre intervalli dei valori dei dati (basso, medio e alto) e a cui è possibile applicare un colore diverso (o stile).</span><span class="sxs-lookup"><span data-stu-id="0c19f-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="0c19f-110">Per impostare indicatori colorati nelle pile</span><span class="sxs-lookup"><span data-stu-id="0c19f-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="0c19f-111">In **Attività**, nella pagina Gestione ruolo utente, scegliere **Imposta pile**.</span><span class="sxs-lookup"><span data-stu-id="0c19f-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="0c19f-112">Verrà visualizzata la pagina **Setup pila**.</span><span class="sxs-lookup"><span data-stu-id="0c19f-112">The **Cue Setup** page appears.</span></span> <span data-ttu-id="0c19f-113">Nella pagina sono elencati gli indicatori attualmente impostati nelle pile.</span><span class="sxs-lookup"><span data-stu-id="0c19f-113">The page lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="0c19f-114">Per modificare un indicatore, modificare i campi e modificare, ad esempio, i valori per le diverse soglie.</span><span class="sxs-lookup"><span data-stu-id="0c19f-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="0c19f-115">Nella tabella seguente sono elencati i colori corrispondenti alle opzioni dei campi **Stile intervallo inferiore**, **Stile intervallo medio** e **Stile intervallo superiore**.</span><span class="sxs-lookup"><span data-stu-id="0c19f-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="0c19f-116">Opzione</span><span class="sxs-lookup"><span data-stu-id="0c19f-116">Option</span></span> | <span data-ttu-id="0c19f-117">Colore</span><span class="sxs-lookup"><span data-stu-id="0c19f-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="0c19f-118">**Nessuno**</span><span class="sxs-lookup"><span data-stu-id="0c19f-118">**None**</span></span> |<span data-ttu-id="0c19f-119">Nessun colore (lo stesso colore della sezione Pila)</span><span class="sxs-lookup"><span data-stu-id="0c19f-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="0c19f-120">**Favorevole**</span><span class="sxs-lookup"><span data-stu-id="0c19f-120">**Favorable**</span></span> |<span data-ttu-id="0c19f-121">Verde</span><span class="sxs-lookup"><span data-stu-id="0c19f-121">Green</span></span> |
| <span data-ttu-id="0c19f-122">**Sfavorevole**</span><span class="sxs-lookup"><span data-stu-id="0c19f-122">**Unfavorable**</span></span> |<span data-ttu-id="0c19f-123">Rosso</span><span class="sxs-lookup"><span data-stu-id="0c19f-123">Red</span></span> |
| <span data-ttu-id="0c19f-124">**Ambiguo**</span><span class="sxs-lookup"><span data-stu-id="0c19f-124">**Ambiguous**</span></span> |<span data-ttu-id="0c19f-125">Giallo</span><span class="sxs-lookup"><span data-stu-id="0c19f-125">Yellow</span></span> |
| <span data-ttu-id="0c19f-126">**Subordinato**</span><span class="sxs-lookup"><span data-stu-id="0c19f-126">**Subordinate**</span></span> |<span data-ttu-id="0c19f-127">Grigio</span><span class="sxs-lookup"><span data-stu-id="0c19f-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="0c19f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c19f-128">See Also</span></span>
<span data-ttu-id="0c19f-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c19f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
