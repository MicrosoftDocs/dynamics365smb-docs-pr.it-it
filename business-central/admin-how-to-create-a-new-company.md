---
title: Come creare una nuova società | Microsoft Docs
description: Quando si crea una nuova società, vengono create tabelle e pagine di RapidStart Services che non contengono dati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 703b70a608bd6b25b9a3218eb59e8666fcd6a0ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378325"
---
# <a name="create-a-new-company"></a><span data-ttu-id="3bf69-103">Creare una nuova società</span><span class="sxs-lookup"><span data-stu-id="3bf69-103">Create a New Company</span></span>
<span data-ttu-id="3bf69-104">Per utilizzare RapidStart Services per [!INCLUDE[prod_short](includes/prod_short.md)], è necessario dapprima creare una nuova società per la quale si desidera effettuare l'implementazione di un cliente.</span><span class="sxs-lookup"><span data-stu-id="3bf69-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="3bf69-105">Quando si crea una nuova società, le tabelle e le pagine standard di [!INCLUDE[prod_short](includes/prod_short.md)] vengono create, ma non sono disponibili dati al loro interno.</span><span class="sxs-lookup"><span data-stu-id="3bf69-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="3bf69-106">Inoltre, è possibile collegare dati di setup specifici alla società dopo l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="3bf69-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="3bf69-107">Le informazioni vengono fornite in un pacchetto di configurazione, un file con estensione rapidstart che offre il contenuto in un formato compresso.</span><span class="sxs-lookup"><span data-stu-id="3bf69-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="3bf69-108">Pacchetti di configurazione di esempio, inclusi i file specifici di ciascun paese/regione, sono inclusi nella società demo CRONUS.</span><span class="sxs-lookup"><span data-stu-id="3bf69-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="3bf69-109">Attenersi alle procedure riportate di seguito per utilizzare il pacchetto di configurazioni di esempio con una nuova società.</span><span class="sxs-lookup"><span data-stu-id="3bf69-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="3bf69-110">Per utilizzare il pacchetto di configurazione BASICCONFIG di esempio</span><span class="sxs-lookup"><span data-stu-id="3bf69-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="3bf69-111">Aprire la società CRONUS Italia S.p.A.</span><span class="sxs-lookup"><span data-stu-id="3bf69-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="3bf69-112">Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3bf69-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="3bf69-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="3bf69-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="3bf69-114">Scegliere il pacchetto BASICCONFIG dalla lista, quindi scegliere l'azione **Esporta pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="3bf69-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="3bf69-115">Attenersi alla procedura riportata di seguito per creare una nuova società e utilizzare il pacchetto BASICCONFIG come parte del processo.</span><span class="sxs-lookup"><span data-stu-id="3bf69-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="3bf69-116">Per creare una nuova società</span><span class="sxs-lookup"><span data-stu-id="3bf69-116">To create a new company</span></span>  
1. <span data-ttu-id="3bf69-117">Creare una nuova società.</span><span class="sxs-lookup"><span data-stu-id="3bf69-117">Create a new company.</span></span> <span data-ttu-id="3bf69-118">Per ulteriori informazioni, vedere [Creazione di nuove società in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="3bf69-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="3bf69-119">Nella Gestione ruolo utente Implementatore di RapidStart Services, è ora possibile importare il pacchetto di configurazione esportato dalla società CRONUS Italia S.p.A..</span><span class="sxs-lookup"><span data-stu-id="3bf69-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="3bf69-120">Dopo aver creato una nuova società, le tabelle vengono automaticamente compilate, anche se non esiste alcun modello della società collegato.</span><span class="sxs-lookup"><span data-stu-id="3bf69-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="3bf69-121">Ad esempio, è possibile esaminare i codici standard per transazioni di registrazione e batch nella pagina **Codice origine**.</span><span class="sxs-lookup"><span data-stu-id="3bf69-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="3bf69-122">Se si immette una versione locale di [!INCLUDE[prod_short](includes/prod_short.md)], è consigliabile verificare la tabella e considerare eventuali problemi relativi alla lingua locale.</span><span class="sxs-lookup"><span data-stu-id="3bf69-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="3bf69-123">Informazioni sulle tabelle dati</span><span class="sxs-lookup"><span data-stu-id="3bf69-123">About Data Tables</span></span>
<span data-ttu-id="3bf69-124">Le tabelle dati di [!INCLUDE[prod_short](includes/prod_short.md)] presentano due tipologie di base: master e setup.</span><span class="sxs-lookup"><span data-stu-id="3bf69-124">[!INCLUDE[prod_short](includes/prod_short.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="3bf69-125">Quando si imposta una configurazione di società, è possibile utilizzare queste tipologie per identificare la strategia di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3bf69-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="3bf69-126">Tabelle di dati master</span><span class="sxs-lookup"><span data-stu-id="3bf69-126">Master Data Tables</span></span>  
<span data-ttu-id="3bf69-127">Nella seguente tabella vengono elencati alcuni esempi di tabelle di dati master.</span><span class="sxs-lookup"><span data-stu-id="3bf69-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="3bf69-128">Quando si inizializza una nuova società, queste tabelle sono vuote.</span><span class="sxs-lookup"><span data-stu-id="3bf69-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="3bf69-129">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="3bf69-129">Table No.</span></span>|<span data-ttu-id="3bf69-130">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="3bf69-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="3bf69-131">15</span><span class="sxs-lookup"><span data-stu-id="3bf69-131">15</span></span>|<span data-ttu-id="3bf69-132">Conto C/G</span><span class="sxs-lookup"><span data-stu-id="3bf69-132">G/L Account</span></span>|  
|<span data-ttu-id="3bf69-133">18</span><span class="sxs-lookup"><span data-stu-id="3bf69-133">18</span></span>|<span data-ttu-id="3bf69-134">Cliente</span><span class="sxs-lookup"><span data-stu-id="3bf69-134">Customer</span></span>|  
|<span data-ttu-id="3bf69-135">23</span><span class="sxs-lookup"><span data-stu-id="3bf69-135">23</span></span>|<span data-ttu-id="3bf69-136">Fornitore</span><span class="sxs-lookup"><span data-stu-id="3bf69-136">Vendor</span></span>|  
|<span data-ttu-id="3bf69-137">27</span><span class="sxs-lookup"><span data-stu-id="3bf69-137">27</span></span>|<span data-ttu-id="3bf69-138">Articolo</span><span class="sxs-lookup"><span data-stu-id="3bf69-138">Item</span></span>|  
|<span data-ttu-id="3bf69-139">5050</span><span class="sxs-lookup"><span data-stu-id="3bf69-139">5050</span></span>|<span data-ttu-id="3bf69-140">Contatto</span><span class="sxs-lookup"><span data-stu-id="3bf69-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="3bf69-141">Tabelle dati di setup</span><span class="sxs-lookup"><span data-stu-id="3bf69-141">Setup Data Tables</span></span>  
<span data-ttu-id="3bf69-142">Nella seguente tabella vengono elencate tabelle dei dati di setup, dove vengono acquisite le informazioni di impostazione nel questionario di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3bf69-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="3bf69-143">Queste tabelle contengono informazioni di base al momento della creazione della società.</span><span class="sxs-lookup"><span data-stu-id="3bf69-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="3bf69-144">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="3bf69-144">Table No.</span></span>|<span data-ttu-id="3bf69-145">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="3bf69-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="3bf69-146">98</span><span class="sxs-lookup"><span data-stu-id="3bf69-146">98</span></span>|<span data-ttu-id="3bf69-147">Setup contabilità generale</span><span class="sxs-lookup"><span data-stu-id="3bf69-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="3bf69-148">311</span><span class="sxs-lookup"><span data-stu-id="3bf69-148">311</span></span>|<span data-ttu-id="3bf69-149">Setup contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="3bf69-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="3bf69-150">312</span><span class="sxs-lookup"><span data-stu-id="3bf69-150">312</span></span>|<span data-ttu-id="3bf69-151">Setup contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="3bf69-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="3bf69-152">313</span><span class="sxs-lookup"><span data-stu-id="3bf69-152">313</span></span>|<span data-ttu-id="3bf69-153">Setup magazzino</span><span class="sxs-lookup"><span data-stu-id="3bf69-153">Inventory Setup</span></span>|  

<span data-ttu-id="3bf69-154">Oltre alle tabelle dei dati di setup, in [!INCLUDE[prod_short](includes/prod_short.md)] sono presenti tabelle dati di tipo setup che specificano le informazioni principali relative alla società e ai relativi processi aziendali.</span><span class="sxs-lookup"><span data-stu-id="3bf69-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="3bf69-155">La tabella riportata di seguito ne elenca alcuni.</span><span class="sxs-lookup"><span data-stu-id="3bf69-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="3bf69-156">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="3bf69-156">Table No.</span></span>|<span data-ttu-id="3bf69-157">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="3bf69-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="3bf69-158">3</span><span class="sxs-lookup"><span data-stu-id="3bf69-158">3</span></span>|<span data-ttu-id="3bf69-159">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="3bf69-159">Payment Terms</span></span>|  
|<span data-ttu-id="3bf69-160">4</span><span class="sxs-lookup"><span data-stu-id="3bf69-160">4</span></span>|<span data-ttu-id="3bf69-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="3bf69-161">Currency</span></span>|  
|<span data-ttu-id="3bf69-162">6</span><span class="sxs-lookup"><span data-stu-id="3bf69-162">6</span></span>|<span data-ttu-id="3bf69-163">Gruppi prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="3bf69-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="3bf69-164">5700</span><span class="sxs-lookup"><span data-stu-id="3bf69-164">5700</span></span>|<span data-ttu-id="3bf69-165">Unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="3bf69-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="3bf69-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bf69-166">See Also</span></span>  
[<span data-ttu-id="3bf69-167">Applicazione della configurazione a nuove società</span><span class="sxs-lookup"><span data-stu-id="3bf69-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="3bf69-168">Impostazione di una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="3bf69-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="3bf69-169">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="3bf69-169">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]