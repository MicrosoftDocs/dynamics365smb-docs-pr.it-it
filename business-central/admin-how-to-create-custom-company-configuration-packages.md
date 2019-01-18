---
title: "Creare pacchetti di configurazione di società personalizzati | Documenti Microsoft"
description: "Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti. È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 868972e4d53d858834ba5985a3de3ffa1d4dcc6b
ms.contentlocale: it-it
ms.lasthandoff: 11/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="39061-104">Creare pacchetti di configurazione di società personalizzati</span><span class="sxs-lookup"><span data-stu-id="39061-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="39061-105">Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti.</span><span class="sxs-lookup"><span data-stu-id="39061-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="39061-106">È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="39061-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="39061-107">In generale, creare un pacchetto di configurazione per area funzionale, ad esempio, creare un pacchetto per la propria funzionalità di produzione.</span><span class="sxs-lookup"><span data-stu-id="39061-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="39061-108">Che consente di collegare e impostare nuove aree in una società in base alla necessità</span><span class="sxs-lookup"><span data-stu-id="39061-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="39061-109">Un altro approccio consiste nel creare un pacchetto che include le tabelle che definiscono il setup, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="39061-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="39061-110">Setup cespiti</span><span class="sxs-lookup"><span data-stu-id="39061-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="39061-111">Setup contabilità generale</span><span class="sxs-lookup"><span data-stu-id="39061-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="39061-112">Setup magazzino</span><span class="sxs-lookup"><span data-stu-id="39061-112">Inventory Setup</span></span>  
-   <span data-ttu-id="39061-113">Setup manufacturing</span><span class="sxs-lookup"><span data-stu-id="39061-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="39061-114">Setup contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="39061-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="39061-115">Setup marketing</span><span class="sxs-lookup"><span data-stu-id="39061-115">Marketing Setup</span></span>  
-   <span data-ttu-id="39061-116">Setup assistenza</span><span class="sxs-lookup"><span data-stu-id="39061-116">Service Setup</span></span>  
-   <span data-ttu-id="39061-117">Setup contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="39061-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="39061-118">Setup warehouse</span><span class="sxs-lookup"><span data-stu-id="39061-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="39061-119">Setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="39061-119">General Posting Setup</span></span>  
-   <span data-ttu-id="39061-120">Setup registrazioni IVA</span><span class="sxs-lookup"><span data-stu-id="39061-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="39061-121">Setup registrazione magazzino</span><span class="sxs-lookup"><span data-stu-id="39061-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="39061-122">Per visualizzare un elenco completo di tabelle di setup, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="39061-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="39061-123">Per creare un pacchetto di configurazione di società personalizzato</span><span class="sxs-lookup"><span data-stu-id="39061-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="39061-124">Creare un nuovo [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="39061-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="39061-125">***IMPOSSIBILE Collegamento alla Guida per "Creazione di un nuovo tenant"***.</span><span class="sxs-lookup"><span data-stu-id="39061-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="39061-126">Creare una nuova società per il modello della soluzione o del settore.</span><span class="sxs-lookup"><span data-stu-id="39061-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="39061-127">Per ulteriori informazioni, vedere [Creare una nuova società](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="39061-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="39061-128">Impostare la nuova società nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="39061-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="39061-129">Compilare tutte le tabelle di setup necessarie.</span><span class="sxs-lookup"><span data-stu-id="39061-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="39061-130">Apre la nuova società.</span><span class="sxs-lookup"><span data-stu-id="39061-130">Open the new company.</span></span>
5. <span data-ttu-id="39061-131">Aprire la pagina **Foglio di lavoro configurazione**.</span><span class="sxs-lookup"><span data-stu-id="39061-131">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="39061-132">Aggiungere al prospetto le tabelle da trasferire a un'altra società.</span><span class="sxs-lookup"><span data-stu-id="39061-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="39061-133">Assegnare le righe del prospetto al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="39061-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="39061-134">Creare un questionario per le tabelle di setup utilizzate con maggiore frequenza.</span><span class="sxs-lookup"><span data-stu-id="39061-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="39061-135">Creare modelli di configurazione per facilitare la creazione di dati master, ad esempio clienti o articoli.</span><span class="sxs-lookup"><span data-stu-id="39061-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="39061-136">Esportare il pacchetto come file con estensione rapidstart.</span><span class="sxs-lookup"><span data-stu-id="39061-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="39061-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39061-137">See Also</span></span>  
[<span data-ttu-id="39061-138">Impostare una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="39061-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="39061-139">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="39061-139">Administration</span></span>](admin-setup-and-administration.md)

