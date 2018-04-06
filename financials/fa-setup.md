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
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ca21ece631fdd07cb95ffdaaa350506b4a8c9e1
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="fac3f-103">Impostazione di cespiti</span><span class="sxs-lookup"><span data-stu-id="fac3f-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="fac3f-104">Per poter utilizzare i cespiti, è necessario definire alcune opzioni:</span><span class="sxs-lookup"><span data-stu-id="fac3f-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="fac3f-105">Come assicurare, gestire e ammortizzare i cespiti.</span><span class="sxs-lookup"><span data-stu-id="fac3f-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="fac3f-106">Come si registrano i costi e altri valori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="fac3f-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="fac3f-107">Nella tabella sottostante sono presenti collegamenti a ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="fac3f-107">The table below has links to more information.</span></span> <span data-ttu-id="fac3f-108">Dopo aver impostato tali opzioni, è possibile avviare diverse attività.</span><span class="sxs-lookup"><span data-stu-id="fac3f-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="fac3f-109">Per ulteriori informazioni, vedere [Cespiti](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="fac3f-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="fac3f-110">È possibile registrare le transazioni dei cespiti nella finestra **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna.</span><span class="sxs-lookup"><span data-stu-id="fac3f-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="fac3f-111">Nella Guida per i cespiti viene descritto solo come utilizzare la finestra **Reg. cespiti in G/L**.</span><span class="sxs-lookup"><span data-stu-id="fac3f-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="fac3f-112">Quando si abilita un'attività del cespite nella sezione **Integrazione C/G** della finestra **Scheda registro beni ammortizz.**, la finestra **Registrazioni cespiti in C/G** viene utilizzata per registrare le transazioni dell'attività in questione.</span><span class="sxs-lookup"><span data-stu-id="fac3f-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="fac3f-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="fac3f-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="fac3f-114">Per</span><span class="sxs-lookup"><span data-stu-id="fac3f-114">To</span></span> | <span data-ttu-id="fac3f-115">Vedere</span><span class="sxs-lookup"><span data-stu-id="fac3f-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="fac3f-116">Impostare i conti C/G di default, le chiavi di allocazione, le definizioni di registrazioni e i batch per la registrazione del cespite e impostare le classi e le sottoclassi e dei cespiti, ad esempio materiali e immateriali.</span><span class="sxs-lookup"><span data-stu-id="fac3f-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="fac3f-117">Impostare i valori generali per i cespiti</span><span class="sxs-lookup"><span data-stu-id="fac3f-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="fac3f-118">Creare registri beni ammortizzabili, definire diversi metodi di ammortamento, integrare con la contabilità generale e abilitare la duplicazione dei movimenti in più registri.</span><span class="sxs-lookup"><span data-stu-id="fac3f-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="fac3f-119">Impostare l'ammortamento dei cespiti</span><span class="sxs-lookup"><span data-stu-id="fac3f-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="fac3f-120">Abilitare l'assicurazione dei cespiti, impostare le informazioni generali dell'assicurazione, una scheda assicurazione per ogni polizza e preparare le registrazioni per registrare i costi delle assicurazioni.</span><span class="sxs-lookup"><span data-stu-id="fac3f-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="fac3f-121">Impostare l'assicurazione cespiti</span><span class="sxs-lookup"><span data-stu-id="fac3f-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="fac3f-122">Abilitare la manutenzione dei cespiti, impostare le informazioni di manutenzione generali, i conti di registrazione di manutenzione e definire i tipi di lavoro di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="fac3f-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="fac3f-123">Per impostare la manutenzione cespiti</span><span class="sxs-lookup"><span data-stu-id="fac3f-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="fac3f-124">Ulteriori informazioni sui diversi metodi di ammortamento del cespite.</span><span class="sxs-lookup"><span data-stu-id="fac3f-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="fac3f-125">Metodi ammortamento</span><span class="sxs-lookup"><span data-stu-id="fac3f-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="fac3f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fac3f-126">See Also</span></span>
[<span data-ttu-id="fac3f-127">Cespiti</span><span class="sxs-lookup"><span data-stu-id="fac3f-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="fac3f-128">Finanze</span><span class="sxs-lookup"><span data-stu-id="fac3f-128">Finance</span></span>](finance.md)  
<span data-ttu-id="fac3f-129">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="fac3f-129">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="fac3f-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fac3f-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

