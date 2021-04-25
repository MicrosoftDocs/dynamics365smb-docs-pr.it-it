---
title: 'Procedura: Impostare impiegati warehouse | Documenti Microsoft'
description: Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4a2ebf2d28833b9cb79c5711fd0314134dfc0915
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784169"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="d5070-103">Impostare impiegati warehouse</span><span class="sxs-lookup"><span data-stu-id="d5070-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="d5070-104">Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.</span><span class="sxs-lookup"><span data-stu-id="d5070-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="d5070-105">Mediante questa impostazione dell'utente vengono filtrate tutte le attività di warehouse del database in base all'ubicazione dell'impiegato in modo che l'impiegato possa eseguire esclusivamente le attività di warehouse nella posizione di default.</span><span class="sxs-lookup"><span data-stu-id="d5070-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="d5070-106">Un utente può essere assegnato a ubicazioni aggiuntive non di default per le quali l'impiegato può visualizzare le righe delle attività ma non eseguire le attività.</span><span class="sxs-lookup"><span data-stu-id="d5070-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="d5070-107">Per impostare impiegati warehouse</span><span class="sxs-lookup"><span data-stu-id="d5070-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="d5070-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d5070-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d5070-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d5070-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="d5070-110">Selezionare il campo **ID utente** quindi selezionare l'utente da aggiungere come impiegato warehouse.</span><span class="sxs-lookup"><span data-stu-id="d5070-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="d5070-111">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5070-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="d5070-112">Nel campo **Cod. ubicazione**, immettere il codice dell'ubicazione in cui l'utente lavorerà.</span><span class="sxs-lookup"><span data-stu-id="d5070-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="d5070-113">Selezionare la casella di controllo **Default** per definire l'unica ubicazione in cui l'impiegato può eseguire attività di warehouse.</span><span class="sxs-lookup"><span data-stu-id="d5070-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="d5070-114">Ripetere i passaggi indicati per assegnare altri impiegati a ubicazioni o per assegnare ubicazioni non di default agli impiegati warehouse esistenti.</span><span class="sxs-lookup"><span data-stu-id="d5070-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d5070-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5070-115">See Also</span></span>  
[<span data-ttu-id="d5070-116">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="d5070-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="d5070-117">Magazzino</span><span class="sxs-lookup"><span data-stu-id="d5070-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d5070-118">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="d5070-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="d5070-119">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="d5070-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="d5070-120">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="d5070-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="d5070-121">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5070-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]