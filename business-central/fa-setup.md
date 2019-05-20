---
title: Impostare cespiti| Documenti Microsoft
description: Informazioni sulla sequenza di attività da eseguire per impostare i cespiti, ad esempio macchinari o edifici.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c7a8ac11ffe4d9a1e19956a40ae57a62b43c096f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242861"
---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="ea928-103">Impostazione di cespiti</span><span class="sxs-lookup"><span data-stu-id="ea928-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="ea928-104">Per poter utilizzare i cespiti, è necessario definire alcune opzioni:</span><span class="sxs-lookup"><span data-stu-id="ea928-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="ea928-105">Come assicurare, gestire e ammortizzare i cespiti.</span><span class="sxs-lookup"><span data-stu-id="ea928-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="ea928-106">Come si registrano i costi e altri valori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="ea928-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="ea928-107">Nella tabella sottostante sono presenti collegamenti a ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="ea928-107">The table below has links to more information.</span></span> <span data-ttu-id="ea928-108">Dopo aver impostato tali opzioni, è possibile avviare diverse attività.</span><span class="sxs-lookup"><span data-stu-id="ea928-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="ea928-109">Per ulteriori informazioni, vedere [Cespiti](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="ea928-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ea928-110">È possibile registrare le transazioni dei cespiti nella pagina **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna.</span><span class="sxs-lookup"><span data-stu-id="ea928-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** pages, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="ea928-111">Nella Guida per i cespiti viene descritto solo come utilizzare la pagina **Reg. cespiti in G/L**.</span><span class="sxs-lookup"><span data-stu-id="ea928-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** page.</span></span>  

<span data-ttu-id="ea928-112">Quando si abilita un'attività del cespite nella sezione **Integrazione C/G** della pagina **Scheda registro beni ammortizz.**, la pagina **Registrazioni cespiti in C/G** viene utilizzata per registrare le transazioni dell'attività in questione.</span><span class="sxs-lookup"><span data-stu-id="ea928-112">When you enable a fixed asset activity in the **G/L Integration** section on the **Depreciation Book Card** page, the **Fixed Asset G/L Journal** page is used to post transactions for the activity.</span></span>

<span data-ttu-id="ea928-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="ea928-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="ea928-114">Per</span><span class="sxs-lookup"><span data-stu-id="ea928-114">To</span></span> | <span data-ttu-id="ea928-115">Vedere</span><span class="sxs-lookup"><span data-stu-id="ea928-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="ea928-116">Impostare i conti C/G di default, le chiavi di allocazione, le definizioni di registrazioni e i batch per la registrazione del cespite e impostare le classi e le sottoclassi e dei cespiti, ad esempio materiali e immateriali.</span><span class="sxs-lookup"><span data-stu-id="ea928-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="ea928-117">Impostare i valori generali per i cespiti</span><span class="sxs-lookup"><span data-stu-id="ea928-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="ea928-118">Creare registri beni ammortizzabili, definire diversi metodi di ammortamento, integrare con la contabilità generale e abilitare la duplicazione dei movimenti in più registri.</span><span class="sxs-lookup"><span data-stu-id="ea928-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="ea928-119">Impostare l'ammortamento dei cespiti</span><span class="sxs-lookup"><span data-stu-id="ea928-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="ea928-120">Abilitare l'assicurazione dei cespiti, impostare le informazioni generali dell'assicurazione, una scheda assicurazione per ogni polizza e preparare le registrazioni per registrare i costi delle assicurazioni.</span><span class="sxs-lookup"><span data-stu-id="ea928-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="ea928-121">Impostare l'assicurazione cespiti</span><span class="sxs-lookup"><span data-stu-id="ea928-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="ea928-122">Abilitare la manutenzione dei cespiti, impostare le informazioni di manutenzione generali, i conti di registrazione di manutenzione e definire i tipi di lavoro di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="ea928-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="ea928-123">Per impostare la manutenzione cespiti</span><span class="sxs-lookup"><span data-stu-id="ea928-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="ea928-124">Ulteriori informazioni sui diversi metodi di ammortamento del cespite.</span><span class="sxs-lookup"><span data-stu-id="ea928-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="ea928-125">Metodi di ammortamento</span><span class="sxs-lookup"><span data-stu-id="ea928-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="ea928-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea928-126">See Also</span></span>
[<span data-ttu-id="ea928-127">Cespiti</span><span class="sxs-lookup"><span data-stu-id="ea928-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="ea928-128">Finanze</span><span class="sxs-lookup"><span data-stu-id="ea928-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="ea928-129">Introduzione</span><span class="sxs-lookup"><span data-stu-id="ea928-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ea928-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea928-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
