---
title: Creare pacchetti di configurazione di società personalizzati | Documenti Microsoft
description: Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti. È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 99fad48961dc201a25af061cf982a1c65d9446bd
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878867"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="031fd-104">Creare pacchetti di configurazione di società personalizzati</span><span class="sxs-lookup"><span data-stu-id="031fd-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="031fd-105">Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti.</span><span class="sxs-lookup"><span data-stu-id="031fd-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="031fd-106">È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="031fd-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="031fd-107">In generale, creare un pacchetto di configurazione per area funzionale, ad esempio, creare un pacchetto per la propria funzionalità di produzione.</span><span class="sxs-lookup"><span data-stu-id="031fd-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="031fd-108">Che consente di collegare e impostare nuove aree in una società in base alla necessità</span><span class="sxs-lookup"><span data-stu-id="031fd-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="031fd-109">Un altro approccio consiste nel creare un pacchetto che include le tabelle che definiscono il setup, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="031fd-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="031fd-110">Setup cespiti</span><span class="sxs-lookup"><span data-stu-id="031fd-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="031fd-111">Setup contabilità generale</span><span class="sxs-lookup"><span data-stu-id="031fd-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="031fd-112">Setup magazzino</span><span class="sxs-lookup"><span data-stu-id="031fd-112">Inventory Setup</span></span>  
-   <span data-ttu-id="031fd-113">Setup manufacturing</span><span class="sxs-lookup"><span data-stu-id="031fd-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="031fd-114">Setup contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="031fd-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="031fd-115">Setup marketing</span><span class="sxs-lookup"><span data-stu-id="031fd-115">Marketing Setup</span></span>  
-   <span data-ttu-id="031fd-116">Setup assistenza</span><span class="sxs-lookup"><span data-stu-id="031fd-116">Service Setup</span></span>  
-   <span data-ttu-id="031fd-117">Setup contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="031fd-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="031fd-118">Setup warehouse</span><span class="sxs-lookup"><span data-stu-id="031fd-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="031fd-119">Setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="031fd-119">General Posting Setup</span></span>  
-   <span data-ttu-id="031fd-120">Setup registrazioni IVA</span><span class="sxs-lookup"><span data-stu-id="031fd-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="031fd-121">Setup registrazione magazzino</span><span class="sxs-lookup"><span data-stu-id="031fd-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="031fd-122">Per visualizzare un elenco completo di tabelle di setup, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup manuale** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="031fd-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="031fd-123">Per creare un pacchetto di configurazione di società personalizzato</span><span class="sxs-lookup"><span data-stu-id="031fd-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="031fd-124">Creare una nuova società.</span><span class="sxs-lookup"><span data-stu-id="031fd-124">Create a new company.</span></span> <span data-ttu-id="031fd-125">Per ulteriori informazioni, vedere [Creazione di nuove società in Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="031fd-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="031fd-126">Impostare la nuova società nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="031fd-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="031fd-127">Compilare tutte le tabelle di setup necessarie.</span><span class="sxs-lookup"><span data-stu-id="031fd-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="031fd-128">Apre la nuova società.</span><span class="sxs-lookup"><span data-stu-id="031fd-128">Open the new company.</span></span>
5. <span data-ttu-id="031fd-129">Aprire la pagina **Foglio di lavoro configurazione**.</span><span class="sxs-lookup"><span data-stu-id="031fd-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="031fd-130">Aggiungere al prospetto le tabelle da trasferire a un'altra società.</span><span class="sxs-lookup"><span data-stu-id="031fd-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="031fd-131">Assegnare le righe del prospetto al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="031fd-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="031fd-132">Creare un questionario per le tabelle di setup utilizzate con maggiore frequenza.</span><span class="sxs-lookup"><span data-stu-id="031fd-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="031fd-133">Creare modelli di configurazione per facilitare la creazione di dati master, ad esempio clienti o articoli.</span><span class="sxs-lookup"><span data-stu-id="031fd-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="031fd-134">Esportare il pacchetto come file con estensione rapidstart.</span><span class="sxs-lookup"><span data-stu-id="031fd-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="031fd-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="031fd-135">See Also</span></span>  
[<span data-ttu-id="031fd-136">Impostazione di una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="031fd-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="031fd-137">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="031fd-137">Administration</span></span>](admin-setup-and-administration.md)
