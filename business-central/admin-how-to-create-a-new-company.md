---
title: Come creare una nuova società | Microsoft Docs
description: Quando si crea una nuova società, vengono create tabelle e pagine di RapidStart Services che non contengono dati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c7042e783ec004cb2de637e6544c590bc8b9b81c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187198"
---
# <a name="create-a-new-company"></a><span data-ttu-id="c8b4c-103">Creare una nuova società</span><span class="sxs-lookup"><span data-stu-id="c8b4c-103">Create a New Company</span></span>
<span data-ttu-id="c8b4c-104">Per utilizzare RapidStart Services per [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario dapprima creare una nuova società per la quale si desidera effettuare l'implementazione di un cliente.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="c8b4c-105">Quando si crea una nuova società, le tabelle e le pagine standard di [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono create, ma non sono disponibili dati al loro interno.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="c8b4c-106">Inoltre, è possibile collegare dati di setup specifici alla società dopo l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="c8b4c-107">Le informazioni vengono fornite in un pacchetto di configurazione, un file con estensione rapidstart che offre il contenuto in un formato compresso.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="c8b4c-108">Pacchetti di configurazione di esempio, inclusi i file specifici di ciascun paese/regione, sono inclusi nella società demo CRONUS.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="c8b4c-109">Attenersi alle procedure riportate di seguito per utilizzare il pacchetto di configurazioni di esempio con una nuova società.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="c8b4c-110">Per utilizzare il pacchetto di configurazione BASICCONFIG di esempio</span><span class="sxs-lookup"><span data-stu-id="c8b4c-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="c8b4c-111">Aprire la società CRONUS Italia S.p.A.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="c8b4c-112">Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c8b4c-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="c8b4c-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="c8b4c-114">Scegliere il pacchetto BASICCONFIG dalla lista, quindi scegliere l'azione **Esporta pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="c8b4c-115">Attenersi alla procedura riportata di seguito per creare una nuova società e utilizzare il pacchetto BASICCONFIG come parte del processo.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="c8b4c-116">Per creare una nuova società</span><span class="sxs-lookup"><span data-stu-id="c8b4c-116">To create a new company</span></span>  
1. <span data-ttu-id="c8b4c-117">Creare una nuova società.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-117">Create a new company.</span></span> <span data-ttu-id="c8b4c-118">Per ulteriori informazioni, vedere [Creazione di nuove società in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="c8b4c-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="c8b4c-119">Nella Gestione ruolo utente Implementatore di RapidStart Services, è ora possibile importare il pacchetto di configurazione esportato dalla società CRONUS Italia S.p.A..</span><span class="sxs-lookup"><span data-stu-id="c8b4c-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="c8b4c-120">Dopo aver creato una nuova società, le tabelle vengono automaticamente compilate, anche se non esiste alcun modello della società collegato.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="c8b4c-121">Ad esempio, è possibile esaminare i codici standard per transazioni di registrazione e batch nella pagina **Codice origine**.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="c8b4c-122">Se si immette una versione locale di [!INCLUDE[d365fin](includes/d365fin_md.md)], è consigliabile verificare la tabella e considerare eventuali problemi relativi alla lingua locale.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="c8b4c-123">Informazioni sulle tabelle dati</span><span class="sxs-lookup"><span data-stu-id="c8b4c-123">About Data Tables</span></span>
<span data-ttu-id="c8b4c-124">Le tabelle dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] presentano due tipologie di base: master e setup.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-124">[!INCLUDE[d365fin](includes/d365fin_md.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="c8b4c-125">Quando si imposta una configurazione di società, è possibile utilizzare queste tipologie per identificare la strategia di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="c8b4c-126">Tabelle di dati master</span><span class="sxs-lookup"><span data-stu-id="c8b4c-126">Master Data Tables</span></span>  
<span data-ttu-id="c8b4c-127">Nella seguente tabella vengono elencati alcuni esempi di tabelle di dati master.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="c8b4c-128">Quando si inizializza una nuova società, queste tabelle sono vuote.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="c8b4c-129">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="c8b4c-129">Table No.</span></span>|<span data-ttu-id="c8b4c-130">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="c8b4c-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c8b4c-131">15</span><span class="sxs-lookup"><span data-stu-id="c8b4c-131">15</span></span>|<span data-ttu-id="c8b4c-132">Conto C/G</span><span class="sxs-lookup"><span data-stu-id="c8b4c-132">G/L Account</span></span>|  
|<span data-ttu-id="c8b4c-133">18</span><span class="sxs-lookup"><span data-stu-id="c8b4c-133">18</span></span>|<span data-ttu-id="c8b4c-134">Cliente</span><span class="sxs-lookup"><span data-stu-id="c8b4c-134">Customer</span></span>|  
|<span data-ttu-id="c8b4c-135">23</span><span class="sxs-lookup"><span data-stu-id="c8b4c-135">23</span></span>|<span data-ttu-id="c8b4c-136">Fornitore</span><span class="sxs-lookup"><span data-stu-id="c8b4c-136">Vendor</span></span>|  
|<span data-ttu-id="c8b4c-137">27</span><span class="sxs-lookup"><span data-stu-id="c8b4c-137">27</span></span>|<span data-ttu-id="c8b4c-138">Articolo</span><span class="sxs-lookup"><span data-stu-id="c8b4c-138">Item</span></span>|  
|<span data-ttu-id="c8b4c-139">5050</span><span class="sxs-lookup"><span data-stu-id="c8b4c-139">5050</span></span>|<span data-ttu-id="c8b4c-140">Contatto</span><span class="sxs-lookup"><span data-stu-id="c8b4c-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="c8b4c-141">Tabelle dati di setup</span><span class="sxs-lookup"><span data-stu-id="c8b4c-141">Setup Data Tables</span></span>  
<span data-ttu-id="c8b4c-142">Nella seguente tabella vengono elencate tabelle dei dati di setup, dove vengono acquisite le informazioni di impostazione nel questionario di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="c8b4c-143">Queste tabelle contengono informazioni di base al momento della creazione della società.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="c8b4c-144">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="c8b4c-144">Table No.</span></span>|<span data-ttu-id="c8b4c-145">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="c8b4c-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c8b4c-146">98</span><span class="sxs-lookup"><span data-stu-id="c8b4c-146">98</span></span>|<span data-ttu-id="c8b4c-147">Setup contabilità generale</span><span class="sxs-lookup"><span data-stu-id="c8b4c-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="c8b4c-148">311</span><span class="sxs-lookup"><span data-stu-id="c8b4c-148">311</span></span>|<span data-ttu-id="c8b4c-149">Setup contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="c8b4c-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="c8b4c-150">312</span><span class="sxs-lookup"><span data-stu-id="c8b4c-150">312</span></span>|<span data-ttu-id="c8b4c-151">Setup contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="c8b4c-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="c8b4c-152">313</span><span class="sxs-lookup"><span data-stu-id="c8b4c-152">313</span></span>|<span data-ttu-id="c8b4c-153">Setup magazzino</span><span class="sxs-lookup"><span data-stu-id="c8b4c-153">Inventory Setup</span></span>|  

<span data-ttu-id="c8b4c-154">Oltre alle tabelle dei dati di setup, in [!INCLUDE[d365fin](includes/d365fin_md.md)] sono presenti tabelle dati di tipo setup che specificano le informazioni principali relative alla società e ai relativi processi aziendali.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="c8b4c-155">La tabella riportata di seguito ne elenca alcuni.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="c8b4c-156">Nr. tabella</span><span class="sxs-lookup"><span data-stu-id="c8b4c-156">Table No.</span></span>|<span data-ttu-id="c8b4c-157">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="c8b4c-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c8b4c-158">3</span><span class="sxs-lookup"><span data-stu-id="c8b4c-158">3</span></span>|<span data-ttu-id="c8b4c-159">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="c8b4c-159">Payment Terms</span></span>|  
|<span data-ttu-id="c8b4c-160">4</span><span class="sxs-lookup"><span data-stu-id="c8b4c-160">4</span></span>|<span data-ttu-id="c8b4c-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="c8b4c-161">Currency</span></span>|  
|<span data-ttu-id="c8b4c-162">6</span><span class="sxs-lookup"><span data-stu-id="c8b4c-162">6</span></span>|<span data-ttu-id="c8b4c-163">Gruppi prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="c8b4c-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="c8b4c-164">5700</span><span class="sxs-lookup"><span data-stu-id="c8b4c-164">5700</span></span>|<span data-ttu-id="c8b4c-165">Unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="c8b4c-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="c8b4c-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8b4c-166">See Also</span></span>  
[<span data-ttu-id="c8b4c-167">Applicazione della configurazione a nuove società</span><span class="sxs-lookup"><span data-stu-id="c8b4c-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="c8b4c-168">Impostazione di una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c8b4c-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c8b4c-169">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="c8b4c-169">Administration</span></span>](admin-setup-and-administration.md)
