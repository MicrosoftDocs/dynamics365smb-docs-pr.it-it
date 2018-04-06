---
title: 'Procedura: Impostare impiegati warehouse | Documenti Microsoft'
description: "Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45a5f7e2140bffd192ecb586e45cc44894752656
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="da587-103">Impostare impiegati warehouse</span><span class="sxs-lookup"><span data-stu-id="da587-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="da587-104">Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.</span><span class="sxs-lookup"><span data-stu-id="da587-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="da587-105">Mediante questa impostazione dell'utente vengono filtrate tutte le attività di warehouse del database in base all'ubicazione dell'impiegato in modo che l'impiegato possa eseguire esclusivamente le attività di warehouse nella posizione di default.</span><span class="sxs-lookup"><span data-stu-id="da587-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="da587-106">Un utente può essere assegnato a ubicazioni aggiuntive non di default per le quali l'impiegato può visualizzare le righe delle attività ma non eseguire le attività.</span><span class="sxs-lookup"><span data-stu-id="da587-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="da587-107">Per impostare impiegati warehouse</span><span class="sxs-lookup"><span data-stu-id="da587-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="da587-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Impiegati warehouse**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="da587-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="da587-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="da587-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="da587-110">Selezionare il campo **ID utente** quindi selezionare l'utente da aggiungere come impiegato warehouse.</span><span class="sxs-lookup"><span data-stu-id="da587-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="da587-111">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="da587-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="da587-112">Nel campo **Cod. ubicazione**, immettere il codice dell'ubicazione in cui l'utente lavorerà.</span><span class="sxs-lookup"><span data-stu-id="da587-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="da587-113">Selezionare la casella di controllo **Default** per definire l'unica ubicazione in cui l'impiegato può eseguire attività di warehouse.</span><span class="sxs-lookup"><span data-stu-id="da587-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="da587-114">Ripetere i passaggi indicati per assegnare altri impiegati a ubicazioni o per assegnare ubicazioni non di default agli impiegati warehouse esistenti.</span><span class="sxs-lookup"><span data-stu-id="da587-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="da587-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da587-115">See Also</span></span>  
[<span data-ttu-id="da587-116">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="da587-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="da587-117">Magazzino</span><span class="sxs-lookup"><span data-stu-id="da587-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="da587-118">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="da587-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="da587-119">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="da587-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="da587-120">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="da587-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="da587-121">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da587-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

