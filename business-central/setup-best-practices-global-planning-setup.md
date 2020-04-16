---
title: Impostare le procedure ottimali per il setup di pianificazione globale | Microsoft Docs
description: La Scheda dettaglio Pianificazione della pagina Setup manufacturing contiene vari campi che definiscono le regole globali per la pianificazione forniture.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c19f527f4d9c06aa28212e7519fee67c6dfd042b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192224"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="10cfc-103">Impostare le procedure ottimali: Setup di pianificazione globale</span><span class="sxs-lookup"><span data-stu-id="10cfc-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="10cfc-104">La Scheda dettaglio **Pianificazione** della pagina **Setup manufacturing** contiene vari campi che definiscono le regole globali per la pianificazione forniture.</span><span class="sxs-lookup"><span data-stu-id="10cfc-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="10cfc-105">Nella seguente tabella vengono fornite le procedure consigliate sulla modalità di impostazione dei campi dei parametri di pianificazione globali selezionati.</span><span class="sxs-lookup"><span data-stu-id="10cfc-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="10cfc-106">Per ulteriori informazioni su un campo, scegliere il collegamento nella colonna **Campo setup**.</span><span class="sxs-lookup"><span data-stu-id="10cfc-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="10cfc-107">Campo Setup</span><span class="sxs-lookup"><span data-stu-id="10cfc-107">Setup field</span></span>|<span data-ttu-id="10cfc-108">Procedura consigliata</span><span class="sxs-lookup"><span data-stu-id="10cfc-108">Best practice</span></span>|<span data-ttu-id="10cfc-109">Commento</span><span class="sxs-lookup"><span data-stu-id="10cfc-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="10cfc-110">Usa previsioni per le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="10cfc-110">Use Forecast on Locations</span></span>|<span data-ttu-id="10cfc-111">Selezionare se vi sono previsioni per ubicazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="10cfc-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="10cfc-112">Componenti nell'ubicazione</span><span class="sxs-lookup"><span data-stu-id="10cfc-112">Components at Location</span></span>|<span data-ttu-id="10cfc-113">Se gli articoli non sono definiti come unità di stockkeeping, selezionare il codice ubicazione della warehouse principale.</span><span class="sxs-lookup"><span data-stu-id="10cfc-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="10cfc-114">Ciò è valido anche se si utilizza solo la richiesta di approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="10cfc-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="10cfc-115">Livello di overflow vuoto</span><span class="sxs-lookup"><span data-stu-id="10cfc-115">Blank Overflow Level</span></span>|<span data-ttu-id="10cfc-116">Selezionare **Consenti calcolo di default** se si sta migrando da Microsoft Dynamics NAV 5.0 o versione precedente.</span><span class="sxs-lookup"><span data-stu-id="10cfc-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="10cfc-117">Utilizzare solo se si desidera consentire a tutti o alcuni articoli di eseguire l'overflow del punto di riordino.</span><span class="sxs-lookup"><span data-stu-id="10cfc-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="10cfc-118">Periodo di stabilizzazione di default</span><span class="sxs-lookup"><span data-stu-id="10cfc-118">Default Dampener Period</span></span>|<span data-ttu-id="10cfc-119">Impostare un valore compreso tra 1D e 5D.</span><span class="sxs-lookup"><span data-stu-id="10cfc-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="10cfc-120">Se non si è esperti della pianificazione in [!INCLUDE[d365fin](includes/d365fin_md.md)], impostare un periodo più lungo.</span><span class="sxs-lookup"><span data-stu-id="10cfc-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="10cfc-121">Quando gli utenti sono più esperti sui diversi motivi dei messaggi di azione, abbreviare il periodo di stabilizzazione per consentire più suggerimenti di modifica.</span><span class="sxs-lookup"><span data-stu-id="10cfc-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="10cfc-122">Quantità di smorzamento di default</span><span class="sxs-lookup"><span data-stu-id="10cfc-122">Default Dampener Quantity</span></span>|<span data-ttu-id="10cfc-123">Impostare tra il 5 e il 20 percento della dimensione del lotto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="10cfc-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="10cfc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10cfc-124">See Also</span></span>  
 <span data-ttu-id="10cfc-125">[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="10cfc-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="10cfc-126">[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="10cfc-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="10cfc-127">Impostare aree di applicazione complesse utilizzando le procedure ottimali</span><span class="sxs-lookup"><span data-stu-id="10cfc-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="10cfc-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10cfc-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
