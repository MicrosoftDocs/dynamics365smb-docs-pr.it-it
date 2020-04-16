---
title: Informazioni sulla contabilità generale e COA| Documenti Microsoft
description: Descrive la contabilità generale, il piano dei conti e le categorie dei conti.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: ce221fed4704a278e7227affe13516303613c9cf
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183766"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="e5134-103">Informazioni sulla contabilità generale e COA</span><span class="sxs-lookup"><span data-stu-id="e5134-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="e5134-104">La contabilità generale memorizza i dati finanziari e il piano dei conti indica in conti in cui sono registrati tutti i movimenti C/G.</span><span class="sxs-lookup"><span data-stu-id="e5134-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e5134-105">include un piano dei conti standard pronto per supportare l'azienda.</span><span class="sxs-lookup"><span data-stu-id="e5134-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="e5134-106">Setup contabilità generale e setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="e5134-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="e5134-107">Il setup della contabilità generale svolge un ruolo fondamentale nei processi finanziari perché definisce il modo in cui vengono registrati i dati.</span><span class="sxs-lookup"><span data-stu-id="e5134-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="e5134-108">Nella pagina **Setup contabilità generale** è possibile specificare le modalità di gestione di determinate questioni contabili relative alla società, quali:</span><span class="sxs-lookup"><span data-stu-id="e5134-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="e5134-109">Dettagli relativi all'arrotondamento delle fatture</span><span class="sxs-lookup"><span data-stu-id="e5134-109">Invoice rounding details</span></span>  
* <span data-ttu-id="e5134-110">Formati indirizzi</span><span class="sxs-lookup"><span data-stu-id="e5134-110">Address formats</span></span>  
* <span data-ttu-id="e5134-111">Report finanziari</span><span class="sxs-lookup"><span data-stu-id="e5134-111">Financial reporting</span></span>  

<span data-ttu-id="e5134-112">Analogamente, nella pagina **Setup registrazioni COGE** è possibile specificare come si desidera impostare le combinazioni di categorie di registrazione business generale e le categorie di registrazione di articoli e servizi.</span><span class="sxs-lookup"><span data-stu-id="e5134-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="e5134-113">Le categorie di registrazione associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e5134-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="e5134-114">Compilare una riga per ogni combinazione di categorie di registrazione business e di categorie di registrazione articoli/servizi.</span><span class="sxs-lookup"><span data-stu-id="e5134-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="e5134-115">Per ulteriori informazioni, vedere [Setup categorie di registrazione](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="e5134-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="e5134-116">Piano dei Conti</span><span class="sxs-lookup"><span data-stu-id="e5134-116">The Chart of Accounts</span></span>
<span data-ttu-id="e5134-117">Nel piano dei conti sono visualizzati tutti i conti C/G.</span><span class="sxs-lookup"><span data-stu-id="e5134-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="e5134-118">Tramite il piano dei conti è possibile eseguire operazioni, quali:</span><span class="sxs-lookup"><span data-stu-id="e5134-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="e5134-119">Visualizzare i report che mostrano i movimenti e i saldi di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e5134-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="e5134-120">Chiudere il conto economico.</span><span class="sxs-lookup"><span data-stu-id="e5134-120">Close your income statement.</span></span>  
* <span data-ttu-id="e5134-121">Aprire la scheda del conto C/G per aggiungere o modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e5134-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="e5134-122">Visualizzare una lista delle categorie di registrazione che registrano nel conto.</span><span class="sxs-lookup"><span data-stu-id="e5134-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="e5134-123">Visualizzare i saldi attivi e passivi separatamente per un singolo conto</span><span class="sxs-lookup"><span data-stu-id="e5134-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="e5134-124">È possibile aggiungere, modificare o eliminare i conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e5134-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="e5134-125">Tuttavia, per evitare le differenze, non è possibile eliminare un conto di contabilità generale se i relativi dati vengono utilizzato nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="e5134-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="e5134-126">Categorie di conti</span><span class="sxs-lookup"><span data-stu-id="e5134-126">Account Categories</span></span>
<span data-ttu-id="e5134-127">È possibile personalizzare la struttura dei rendiconti finanziari mappando i conti di contabilità generale alle categorie dei conti.</span><span class="sxs-lookup"><span data-stu-id="e5134-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="e5134-128">La pagina **Categorie conto C/G** visualizza le categorie e le sottocategorie principali esistenti e i conti C/G assegnati ad esse.</span><span class="sxs-lookup"><span data-stu-id="e5134-128">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="e5134-129">È possibile creare nuove sottocategorie e assegnarle categorie ai conti esistenti.</span><span class="sxs-lookup"><span data-stu-id="e5134-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="e5134-130">È possibile creare un gruppo di categoria definendo un'indentazione di altre categorie in una riga nella pagina **Categorie conto C/G**.</span><span class="sxs-lookup"><span data-stu-id="e5134-130">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="e5134-131">Ciò consente di ottenere una panoramica, in quanto ogni raggruppamento mostra un saldo totale.</span><span class="sxs-lookup"><span data-stu-id="e5134-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="e5134-132">Ad esempio, è possibile creare sottocategorie per i diversi tipi di cespiti e quindi creare gruppi di categorie per cespiti rispetto a cespiti correnti.</span><span class="sxs-lookup"><span data-stu-id="e5134-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="e5134-133">È possibile specificare se i conti di questa sottocategoria devono essere inclusi in determinati tipi di report.</span><span class="sxs-lookup"><span data-stu-id="e5134-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="e5134-134">Le categorie di conto consentono di definire il layout dei rendiconti finanziari.</span><span class="sxs-lookup"><span data-stu-id="e5134-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="e5134-135">Ad esempio, l'estratto conto di default presenta una sottocategoria relativa ai contanti nei cespiti correnti.</span><span class="sxs-lookup"><span data-stu-id="e5134-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="e5134-136">Se si desidera che nell'estratto conto vengano considerate la piccola cassa e il conto assegni, è possibile:</span><span class="sxs-lookup"><span data-stu-id="e5134-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="e5134-137">Aggiungere due nuove sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="e5134-137">Add two new subcategories.</span></span> <span data-ttu-id="e5134-138">Una per la piccola cassa e una per il conto assegni.</span><span class="sxs-lookup"><span data-stu-id="e5134-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="e5134-139">Specificare la definizione report addizionale **Conti cassa** per queste sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="e5134-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="e5134-140">Applicare un rientro sotto la sottocategoria **Contanti**.</span><span class="sxs-lookup"><span data-stu-id="e5134-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="e5134-141">Alla successiva creazione di situazioni contabili, l'estratto conto mostrerà un saldo totale per la cassa contanti e due righe con saldi per la piccola cassa e il conto assegni.</span><span class="sxs-lookup"><span data-stu-id="e5134-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e5134-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5134-142">See Also</span></span>
[<span data-ttu-id="e5134-143">Finanze</span><span class="sxs-lookup"><span data-stu-id="e5134-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="e5134-144">Impostazione o modifica del piano dei conti</span><span class="sxs-lookup"><span data-stu-id="e5134-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="e5134-145">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="e5134-145">Business Intelligence</span></span>](bi.md)  
