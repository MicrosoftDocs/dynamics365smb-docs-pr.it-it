---
title: "Creare pacchetti di configurazione di società personalizzati | Documenti Microsoft"
description: "Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti. È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="52dab-104">Creare pacchetti di configurazione di società personalizzati</span><span class="sxs-lookup"><span data-stu-id="52dab-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="52dab-105">Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti.</span><span class="sxs-lookup"><span data-stu-id="52dab-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="52dab-106">È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="52dab-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="52dab-107">In generale, creare un pacchetto di configurazione per area funzionale, ad esempio, creare un pacchetto per la propria funzionalità di produzione.</span><span class="sxs-lookup"><span data-stu-id="52dab-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="52dab-108">Che consente di collegare e impostare nuove aree in una società in base alla necessità</span><span class="sxs-lookup"><span data-stu-id="52dab-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="52dab-109">Un altro approccio consiste nel creare un pacchetto che include le tabelle che definiscono il setup, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="52dab-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="52dab-110">Setup cespiti</span><span class="sxs-lookup"><span data-stu-id="52dab-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="52dab-111">Setup contabilità generale</span><span class="sxs-lookup"><span data-stu-id="52dab-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="52dab-112">Setup magazzino</span><span class="sxs-lookup"><span data-stu-id="52dab-112">Inventory Setup</span></span>  
-   <span data-ttu-id="52dab-113">Setup manufacturing</span><span class="sxs-lookup"><span data-stu-id="52dab-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="52dab-114">Setup contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="52dab-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="52dab-115">Setup marketing</span><span class="sxs-lookup"><span data-stu-id="52dab-115">Marketing Setup</span></span>  
-   <span data-ttu-id="52dab-116">Setup assistenza</span><span class="sxs-lookup"><span data-stu-id="52dab-116">Service Setup</span></span>  
-   <span data-ttu-id="52dab-117">Setup contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="52dab-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="52dab-118">Setup warehouse</span><span class="sxs-lookup"><span data-stu-id="52dab-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="52dab-119">Setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="52dab-119">General Posting Setup</span></span>  
-   <span data-ttu-id="52dab-120">Setup registrazioni IVA</span><span class="sxs-lookup"><span data-stu-id="52dab-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="52dab-121">Setup registrazione magazzino</span><span class="sxs-lookup"><span data-stu-id="52dab-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="52dab-122">Per visualizzare una lista completa di tabelle di setup, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="52dab-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="52dab-123">Per creare un pacchetto di configurazione di società personalizzato</span><span class="sxs-lookup"><span data-stu-id="52dab-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="52dab-124">Creare un nuovo [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="52dab-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="52dab-125">***IMPOSSIBILE Collegamento alla Guida per "Creazione di un nuovo tenant"***.</span><span class="sxs-lookup"><span data-stu-id="52dab-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="52dab-126">Creare una nuova società per il modello della soluzione o del settore.</span><span class="sxs-lookup"><span data-stu-id="52dab-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="52dab-127">Per ulteriori informazioni, vedere [Creare una nuova società](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="52dab-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="52dab-128">Impostare la nuova società nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="52dab-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="52dab-129">Compilare tutte le tabelle di setup necessarie.</span><span class="sxs-lookup"><span data-stu-id="52dab-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="52dab-130">Apre la nuova società.</span><span class="sxs-lookup"><span data-stu-id="52dab-130">Open the new company.</span></span>
5. <span data-ttu-id="52dab-131">Aprire la finestra **Foglio di lavoro configurazione**.</span><span class="sxs-lookup"><span data-stu-id="52dab-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="52dab-132">Aggiungere al prospetto le tabelle da trasferire a un'altra società.</span><span class="sxs-lookup"><span data-stu-id="52dab-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="52dab-133">Assegnare le righe del prospetto al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="52dab-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="52dab-134">Creare un questionario per le tabelle di setup utilizzate con maggiore frequenza.</span><span class="sxs-lookup"><span data-stu-id="52dab-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="52dab-135">Creare modelli di configurazione per facilitare la creazione di dati master, ad esempio clienti o articoli.</span><span class="sxs-lookup"><span data-stu-id="52dab-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="52dab-136">Esportare il pacchetto come file con estensione rapidstart.</span><span class="sxs-lookup"><span data-stu-id="52dab-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52dab-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52dab-137">See Also</span></span>  
[<span data-ttu-id="52dab-138">Impostare una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="52dab-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="52dab-139">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="52dab-139">Administration</span></span>](admin-setup-and-administration.md)

