---
title: Impostare la manutenzione cespiti| Documenti Microsoft
description: Per gestire la riparazione e l'assistenza del cespite, specificare le informazioni di manutenzione generali, i codici per il tipo di lavoro e un conto registrazione per i costi.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cdf1183fb5383311dc34d8c2c619a1eddf7e8851
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-maintenance"></a><span data-ttu-id="d6f2c-103">Procedura: Impostare la manutenzione cespiti</span><span class="sxs-lookup"><span data-stu-id="d6f2c-103">How to: Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="d6f2c-104">Per gestire la manutenzione dei cespiti, è prima necessario impostare alcune informazioni generali di manutenzione, un conto analitico per i costi di manutenzione e i codici di manutenzione per i tipi di lavoro, ad esempio assistenza di routine o riparazione.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="d6f2c-105">Per impostare le informazioni generali di manutenzione</span><span class="sxs-lookup"><span data-stu-id="d6f2c-105">To set up general maintenance information</span></span>
<span data-ttu-id="d6f2c-106">Se vengono impostati campi per la manutenzione è possibile registrare le spese di manutenzione dalla registrazione cespiti.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="d6f2c-107">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cespiti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6f2c-108">Selezionare il cespite per cui si desidera definire la copertura assicurativa, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="d6f2c-109">Compilare i campi appropriati nella Scheda dettaglio **Manutenzione**.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="d6f2c-110">Per impostare i codici di manutenzione</span><span class="sxs-lookup"><span data-stu-id="d6f2c-110">To set up maintenance codes</span></span>
<span data-ttu-id="d6f2c-111">Quando si registrano dei costi di manutenzione dalle registrazioni COGE, si compila il campo **Cod. manutenzione** per registrare il tipo di manutenzione eseguita, ad esempio assistenza di routine o riparazione.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="d6f2c-112">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Manutenzione**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6f2c-113">Nella finestra **Manutenzione**, impostare i codici per i diversi tipi di lavoro di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="d6f2c-114">Per impostare i conti spesa manutenzione</span><span class="sxs-lookup"><span data-stu-id="d6f2c-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="d6f2c-115">Per registrare i costi di manutenzione occorre prima immettere un numero di conto nella finestra **Cat. Reg. Cespite**.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="d6f2c-116">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. cespiti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6f2c-117">Compilare il campo **Conto Spesa Manutenzione** per ogni categoria di registrazione.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6f2c-118">Per definire che i costi di manutenzione vengano allocati ai reparti o ai progetti, impostare le chiavi di allocazione.</span><span class="sxs-lookup"><span data-stu-id="d6f2c-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="d6f2c-119">Per ulteriori informazioni, vedere [Procedura: Impostare le funzionalità generali per i cespiti](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="d6f2c-119">For more information, see [How to: Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d6f2c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6f2c-120">See Also</span></span>
[<span data-ttu-id="d6f2c-121">Impostazione di cespiti</span><span class="sxs-lookup"><span data-stu-id="d6f2c-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="d6f2c-122">Cespiti</span><span class="sxs-lookup"><span data-stu-id="d6f2c-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="d6f2c-123">Finanze</span><span class="sxs-lookup"><span data-stu-id="d6f2c-123">Finance</span></span>](finance.md)  
<span data-ttu-id="d6f2c-124">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="d6f2c-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="d6f2c-125">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6f2c-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

