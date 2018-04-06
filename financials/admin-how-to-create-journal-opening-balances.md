---
title: Creare bilanci di apertura delle registrazioni | Documenti Microsoft
description: "Business Central comprende diversi processi batch spediti al fine di agevolare il trasferimento dei saldi del conto esistenti a una società appena configurata. È possibile trasferire facilmente questi dati con le registrazioni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: be45ed1de52c92722d801da344163fdffc2a9073
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="336d6-104">Creare bilanci di apertura delle registrazioni</span><span class="sxs-lookup"><span data-stu-id="336d6-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="336d6-105"> comprende diversi processi batch spediti al fine di agevolare il trasferimento dei saldi del conto esistenti a una società appena configurata.</span><span class="sxs-lookup"><span data-stu-id="336d6-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="336d6-106">È possibile trasferire questi dati con la registrazione di clienti, fornitori, magazzino o C/G.</span><span class="sxs-lookup"><span data-stu-id="336d6-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="336d6-107">Il primo passaggio consiste di creare un pacchetto di configurazione che include le tabelle di setup di queste registrazioni.</span><span class="sxs-lookup"><span data-stu-id="336d6-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="336d6-108">La procedura seguente presuppone che questo passaggio sia completato.</span><span class="sxs-lookup"><span data-stu-id="336d6-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="336d6-109">Per ulteriori informazioni, vedere [Impostare la configurazione della società](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="336d6-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="336d6-110">Questa procedura descrive i passaggi successivi, tra cui il collegamento del pacchetto fornito da un partner.</span><span class="sxs-lookup"><span data-stu-id="336d6-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="336d6-111">Prima di iniziare, assicurarsi di essere nella pagina Gestione ruolo utente Implementatore di RapidStart Services in quanto fornisce il contesto corretto per il lavoro di configurazione.</span><span class="sxs-lookup"><span data-stu-id="336d6-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="336d6-112">Per ulteriori informazioni, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="336d6-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="336d6-113">Per collegare i movimenti in una registrazione a una nuova società</span><span class="sxs-lookup"><span data-stu-id="336d6-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="336d6-114">Configurare una nuova società e collegarla a un pacchetto di configurazione.</span><span class="sxs-lookup"><span data-stu-id="336d6-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="336d6-115">Per ulteriori informazioni, vedere [Configurare una società con la procedura guidata RapidStart Services](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="336d6-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="336d6-116">La nuova società non contiene informazioni sui bilanci di apertura delle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="336d6-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="336d6-117">Aprire il foglio di lavoro configurazione e importare dati esistenti relativi a clienti, articoli, fornitori, nonché la contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="336d6-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="336d6-118">Per ulteriori informazioni, vedere [Eseguire la migrazione dei dati dei clienti](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="336d6-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="336d6-119">Scegliere, ad esempio, l'azione **Crea righe registrazioni in C/G**.</span><span class="sxs-lookup"><span data-stu-id="336d6-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="336d6-120">Compilare la Scheda dettaglio **Opzioni** come appropriato e impostare i filtri in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="336d6-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="336d6-121">Ad esempio, immettere un nome nel campo **Definizione registrazioni**.</span><span class="sxs-lookup"><span data-stu-id="336d6-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="336d6-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="336d6-122">Choose the **OK** button.</span></span> <span data-ttu-id="336d6-123">I record sono ora contenuti nella registrazione, ma gli importi sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="336d6-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="336d6-124">Esportare la tabella delle registrazioni in Excel e immettere manualmente le informazioni relative a registrazioni e contropartita dei dati legacy.</span><span class="sxs-lookup"><span data-stu-id="336d6-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="336d6-125">Importare e collegare le informazioni della tabella nella nuova società.</span><span class="sxs-lookup"><span data-stu-id="336d6-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="336d6-126">Le righe di registrazione sono pronte per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="336d6-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="336d6-127">Nel foglio di lavoro configurazione, selezionare la tabella delle righe di registrazione, quindi scegliere l'azione **Dati database**.</span><span class="sxs-lookup"><span data-stu-id="336d6-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="336d6-128">Esaminare le informazioni, quindi scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="336d6-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="336d6-129">Ripetere i passaggi per importare e registrare altri bilanci di apertura.</span><span class="sxs-lookup"><span data-stu-id="336d6-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="336d6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="336d6-130">See Also</span></span>  
[<span data-ttu-id="336d6-131">Applicazione della configurazione a nuove società</span><span class="sxs-lookup"><span data-stu-id="336d6-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="336d6-132">Impostare una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="336d6-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="336d6-133">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="336d6-133">Administration</span></span>](admin-setup-and-administration.md)

