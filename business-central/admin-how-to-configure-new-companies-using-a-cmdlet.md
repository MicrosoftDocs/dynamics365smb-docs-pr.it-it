---
title: "Configurare le nuove società utilizzando un cmdlet | Documenti Microsoft"
description: "In vari scenari è possibile che si desideri caricare e importare un pacchetto di configurazione senza coinvolgere gli utenti o utilizzare l'interfaccia utente di RapidStart Services. A tal fine, utilizzare un cmdlet di Windows PowerShell."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="3853f-104">Configurare nuove società utilizzando un cmdlet</span><span class="sxs-lookup"><span data-stu-id="3853f-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="3853f-105">In vari scenari è possibile che si desideri caricare e importare un pacchetto di configurazione senza coinvolgere gli utenti o utilizzare l'interfaccia utente di RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="3853f-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="3853f-106">A tal fine, utilizzare un cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3853f-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="3853f-107">Gli scenari in cui questo può risultare utile includono:</span><span class="sxs-lookup"><span data-stu-id="3853f-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="3853f-108">Eseguire l'importazione di dati tra più installazioni di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3853f-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="3853f-109">Configurazione delle aree di applicazione aggiuntive per più clienti.</span><span class="sxs-lookup"><span data-stu-id="3853f-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="3853f-110">Per distribuire un pacchetto di configurazione utilizzando un cmdlet</span><span class="sxs-lookup"><span data-stu-id="3853f-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="3853f-111">Preparare un pacchetto di RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="3853f-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="3853f-112">Ad esempio, è possibile creare un pacchetto per importare determinati valori e i nomi della tabella e dei campi in cui inserire tali valori.</span><span class="sxs-lookup"><span data-stu-id="3853f-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="3853f-113">Installare il pacchetto in un computer in cui verrà eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3853f-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="3853f-114">Aprire [!INCLUDE[d365fin](includes/d365fin_md.md)] Administration Shell.</span><span class="sxs-lookup"><span data-stu-id="3853f-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="3853f-115">Immettere **Invoke-NAVCodeUnit** e specificare le informazioni simili al seguente esempio.</span><span class="sxs-lookup"><span data-stu-id="3853f-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="3853f-116">Il cmdlet consente di importare il pacchetto in ogni società.</span><span class="sxs-lookup"><span data-stu-id="3853f-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="3853f-117">Gli utenti possono iniziare a utilizzare la nuova funzionalità immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3853f-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3853f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3853f-118">See Also</span></span>  
[<span data-ttu-id="3853f-119">Configurare nuove società</span><span class="sxs-lookup"><span data-stu-id="3853f-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="3853f-120">Applicazione della configurazione a nuove società</span><span class="sxs-lookup"><span data-stu-id="3853f-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="3853f-121">Impostare una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="3853f-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="3853f-122">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="3853f-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="3853f-123">Microsoft Dynamics NAV - Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3853f-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

