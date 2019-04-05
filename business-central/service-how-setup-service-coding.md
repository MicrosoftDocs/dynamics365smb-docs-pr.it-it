---
title: Impostare codici per servizi standard | Documenti Microsoft
description: Informazioni su come impostare i codici per le attività di assistenza eseguite di frequente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: b9bf54d61ba71281a7069a6977ad1264637eba46
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801585"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="bd8a7-103">Impostare codici di servizio standard</span><span class="sxs-lookup"><span data-stu-id="bd8a7-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="bd8a7-104">Quando si presta un tipo di assistenza standard, è spesso necessario creare documenti di assistenza le cui righe contengono informazioni simili.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="bd8a7-105">Per facilitare la creazione di queste righe, è possibile impostare dei codici di servizio standard aventi un insieme predefinito di righe di assistenza.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="bd8a7-106">Quando si sceglie il codice in un documento di assistenza, le righe vengono immesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="bd8a7-107">È possibile impostare un qualsiasi numero di codici di servizio standard e a ogni codice può essere collegato un numero illimitato di righe di assistenza di tipo diverso, tra cui articolo, risorsa, costo o testo standard.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="bd8a7-108">Vengono create righe di assistenza per ciascun codice di servizio standard nella scheda **Codice servizio standard**.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="bd8a7-109">A questo punto è possibile assegnare codici di servizio standard a gruppi di articoli in assistenza nella pagina **Cod. gr. art. ass. standard**.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="bd8a7-110">Successivamente, quando si crea un documento di assistenza, è possibile utilizzare l'azione **Ottieni codici servizio std.** per aggiungere righe di assistenza.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="bd8a7-111">È possibile utilizzare la stessa procedura per creare righe nei documenti di vendita e acquisto.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="bd8a7-112">Per altre informazioni, vedere [Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="bd8a7-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="bd8a7-113">Per impostare un codice di servizio standard</span><span class="sxs-lookup"><span data-stu-id="bd8a7-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="bd8a7-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Codici servizio standard** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bd8a7-115">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="bd8a7-116">Compilare le righe di assistenza collegate al codice specifico.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="bd8a7-117">Per assegnare un codice di servizio standard a un gruppo di articoli in assistenza</span><span class="sxs-lookup"><span data-stu-id="bd8a7-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="bd8a7-118">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi articoli in assistenza** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bd8a7-119">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="bd8a7-120">Compilare le righe di assistenza collegate al codice specifico.</span><span class="sxs-lookup"><span data-stu-id="bd8a7-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd8a7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd8a7-121">See Also</span></span>
[<span data-ttu-id="bd8a7-122">Gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="bd8a7-122">Service Management</span></span>](service-service.md)