---
title: Impostare cespiti| Documenti Microsoft
description: "Informazioni sulla sequenza di attività da eseguire per impostare i cespiti, ad esempio macchinari o edifici."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="ae7ee-103">Impostazione di cespiti</span><span class="sxs-lookup"><span data-stu-id="ae7ee-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="ae7ee-104">Per poter utilizzare i cespiti, è necessario definire alcune opzioni:</span><span class="sxs-lookup"><span data-stu-id="ae7ee-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="ae7ee-105">Come assicurare, gestire e ammortizzare i cespiti.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="ae7ee-106">Come si registrano i costi e altri valori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="ae7ee-107">Nella tabella sottostante sono presenti collegamenti a ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-107">The table below has links to more information.</span></span> <span data-ttu-id="ae7ee-108">Dopo aver impostato tali opzioni, è possibile avviare diverse attività.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="ae7ee-109">Per ulteriori informazioni, vedere [Cespiti](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="ae7ee-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ae7ee-110">È possibile registrare le transazioni dei cespiti nella finestra **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="ae7ee-111">Nella Guida per i cespiti viene descritto solo come utilizzare la finestra **Reg. cespiti in G/L**.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="ae7ee-112">Quando si abilita un'attività del cespite nella sezione **Integrazione C/G** della finestra **Scheda registro beni ammortizz.**, la finestra **Registrazioni cespiti in C/G** viene utilizzata per registrare le transazioni dell'attività in questione.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="ae7ee-113">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="ae7ee-114">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di Financials](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="ae7ee-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="ae7ee-115">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="ae7ee-116">Per</span><span class="sxs-lookup"><span data-stu-id="ae7ee-116">To</span></span> | <span data-ttu-id="ae7ee-117">Vedere</span><span class="sxs-lookup"><span data-stu-id="ae7ee-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="ae7ee-118">Impostare i conti C/G di default, le chiavi di allocazione, le definizioni di registrazioni e i batch per la registrazione del cespite e impostare le classi e le sottoclassi e dei cespiti, ad esempio materiali e immateriali.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="ae7ee-119">Procedura: Impostare i valori generali per i cespiti</span><span class="sxs-lookup"><span data-stu-id="ae7ee-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="ae7ee-120">Creare registri beni ammortizzabili, definire diversi metodi di ammortamento, integrare con la contabilità generale e abilitare la duplicazione dei movimenti in più registri.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="ae7ee-121">Procedura: Impostare l'ammortamento cespiti</span><span class="sxs-lookup"><span data-stu-id="ae7ee-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="ae7ee-122">Abilitare l'assicurazione dei cespiti, impostare le informazioni generali dell'assicurazione, una scheda assicurazione per ogni polizza e preparare le registrazioni per registrare i costi delle assicurazioni.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="ae7ee-123">Procedura: Impostare l'assicurazione cespiti</span><span class="sxs-lookup"><span data-stu-id="ae7ee-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="ae7ee-124">Abilitare la manutenzione dei cespiti, impostare le informazioni di manutenzione generali, i conti di registrazione di manutenzione e definire i tipi di lavoro di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="ae7ee-125">Procedura: Impostare la manutenzione cespiti</span><span class="sxs-lookup"><span data-stu-id="ae7ee-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="ae7ee-126">Ulteriori informazioni sui diversi metodi di ammortamento del cespite.</span><span class="sxs-lookup"><span data-stu-id="ae7ee-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="ae7ee-127">Metodi ammortamento</span><span class="sxs-lookup"><span data-stu-id="ae7ee-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="ae7ee-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae7ee-128">See Also</span></span>
[<span data-ttu-id="ae7ee-129">Cespiti</span><span class="sxs-lookup"><span data-stu-id="ae7ee-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="ae7ee-130">Finanze</span><span class="sxs-lookup"><span data-stu-id="ae7ee-130">Finance</span></span>](finance.md)  
<span data-ttu-id="ae7ee-131">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="ae7ee-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="ae7ee-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae7ee-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

