---
title: 'Procedura: Preparare i report di transazioni IVA'
description: È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 85a21861550f76fdeb269a37883f5e42aea3b823
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241806"
---
# <a name="prepare-for-vat-transactions-reports"></a><span data-ttu-id="503ea-103">Preparare i report di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="503ea-103">Prepare for VAT Transactions Reports</span></span>
<span data-ttu-id="503ea-104">È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA.</span><span class="sxs-lookup"><span data-stu-id="503ea-104">You must submit periodic reports to the tax authorities to list all transactions that include VAT.</span></span> <span data-ttu-id="503ea-105">L'autorità fiscale stabilisce le soglie richieste per la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="503ea-105">The tax authority establishes the thresholds at which reporting is required.</span></span> <span data-ttu-id="503ea-106">Attualmente, la soglia è impostata su zero, a indicare che tutte le transazioni vengono dichiarate.</span><span class="sxs-lookup"><span data-stu-id="503ea-106">Currently, the threshold is set at zero, meaning that all transactions are to be reported.</span></span> <span data-ttu-id="503ea-107">Per prepararsi per le dichiarazioni, è necessario impostare la registrazione IVA in modo da includere gli importi di dichiarazione della transazione IVA.</span><span class="sxs-lookup"><span data-stu-id="503ea-107">To prepare for these reports, you must set up VAT posting to include VAT transaction report amounts.</span></span>  

## <a name="to-set-up-vat-transaction-amounts"></a><span data-ttu-id="503ea-108">Per impostare gli importi delle transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="503ea-108">To set up VAT transaction amounts</span></span>  

1.  <span data-ttu-id="503ea-109">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="503ea-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Posting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="503ea-110">Scegliere l'azione **Importo report transazioni IVA**.</span><span class="sxs-lookup"><span data-stu-id="503ea-110">Choose the **VAT Transaction Report Amount** action.</span></span>  
3.  <span data-ttu-id="503ea-111">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="503ea-111">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="503ea-112">Campo</span><span class="sxs-lookup"><span data-stu-id="503ea-112">Field</span></span>|<span data-ttu-id="503ea-113">Description</span><span class="sxs-lookup"><span data-stu-id="503ea-113">Description</span></span>|  
    |------------------------------------|---------------------------------------|  
    |<span data-ttu-id="503ea-114">**Persona fisica**</span><span class="sxs-lookup"><span data-stu-id="503ea-114">**Individual Person**</span></span>|<span data-ttu-id="503ea-115">Selezionare se questo cliente è una persona fisica.</span><span class="sxs-lookup"><span data-stu-id="503ea-115">Select if this customer is an individual person.</span></span>|  
    |<span data-ttu-id="503ea-116">**Soggetto residente**</span><span class="sxs-lookup"><span data-stu-id="503ea-116">**Resident**</span></span>|<span data-ttu-id="503ea-117">Specificare se il cliente è residente in Italia.</span><span class="sxs-lookup"><span data-stu-id="503ea-117">Specify if the customer is a resident in Italy.</span></span><br /><br /> <span data-ttu-id="503ea-118">Se un cliente non è un residente, è necessario specificare anche un rappresentante fiscale nella Scheda dettaglio **Commercio estero**.</span><span class="sxs-lookup"><span data-stu-id="503ea-118">If a customer is not a resident, you must also specify a tax representative on the **Foreign Trade** FastTab.</span></span>|  
    |<span data-ttu-id="503ea-119">**Primo nome**</span><span class="sxs-lookup"><span data-stu-id="503ea-119">**First Name**</span></span>|<span data-ttu-id="503ea-120">Specifica il nome della persona.</span><span class="sxs-lookup"><span data-stu-id="503ea-120">Specifies the first name of the person.</span></span>|  
    |<span data-ttu-id="503ea-121">**Cognome**</span><span class="sxs-lookup"><span data-stu-id="503ea-121">**Last Name**</span></span>|<span data-ttu-id="503ea-122">Specifica il cognome della persona.</span><span class="sxs-lookup"><span data-stu-id="503ea-122">Specifies the last name of the person.</span></span>|  
    |<span data-ttu-id="503ea-123">**Data di nascita**</span><span class="sxs-lookup"><span data-stu-id="503ea-123">**Date of Birth**</span></span>|<span data-ttu-id="503ea-124">Specifica la data di nascita della persona.</span><span class="sxs-lookup"><span data-stu-id="503ea-124">Specifies the date of birth of the person.</span></span>|  
    |<span data-ttu-id="503ea-125">**Luogo di nascita**</span><span class="sxs-lookup"><span data-stu-id="503ea-125">**Place of Birth**</span></span>|<span data-ttu-id="503ea-126">Specifica il luogo di nascita della persona.</span><span class="sxs-lookup"><span data-stu-id="503ea-126">Specifies the place of birth of the person.</span></span>|  

3.  <span data-ttu-id="503ea-127">Se il cliente non è in residente in Italia e non è una persona fisica, è necessario specificare un rappresentante fiscale per il cliente.</span><span class="sxs-lookup"><span data-stu-id="503ea-127">If the customer is not resident in Italy and is not an individual person, you must specify a tax representative for the customer.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="503ea-128">Prima di poter specificare un rappresentante fiscale, è necessario creare il rappresentante fiscale come contatto.</span><span class="sxs-lookup"><span data-stu-id="503ea-128">Before you can specify a tax representative, you must have created the tax representative as a contact.</span></span>  

### <a name="to-specify-a-tax-representative-for-a-non-resident-customer"></a><span data-ttu-id="503ea-129">Per specificare un rappresentante fiscale per un cliente non residente</span><span class="sxs-lookup"><span data-stu-id="503ea-129">To specify a tax representative for a non-resident customer</span></span>  

1.  <span data-ttu-id="503ea-130">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="503ea-130">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="503ea-131">Selezionare un cliente.</span><span class="sxs-lookup"><span data-stu-id="503ea-131">Select a customer.</span></span>
2.  <span data-ttu-id="503ea-132">Compilare i campi nella Scheda dettaglio **Commercio estero** come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="503ea-132">On the **Foreign Trade** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="503ea-133">Campo</span><span class="sxs-lookup"><span data-stu-id="503ea-133">Field</span></span>|<span data-ttu-id="503ea-134">Description</span><span class="sxs-lookup"><span data-stu-id="503ea-134">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="503ea-135">**Tipo di rappresentante fiscale**</span><span class="sxs-lookup"><span data-stu-id="503ea-135">**Tax Representative Type**</span></span>|<span data-ttu-id="503ea-136">Specifica se il rappresentante fiscale è un cliente o un contatto.</span><span class="sxs-lookup"><span data-stu-id="503ea-136">Specifies if the tax representative is a customer or a contact.</span></span> <span data-ttu-id="503ea-137">È necessario impostare il campo su **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="503ea-137">You must set this field to **Contact**.</span></span>|  
    |<span data-ttu-id="503ea-138">**Nr. rappresentante fiscale**</span><span class="sxs-lookup"><span data-stu-id="503ea-138">**Tax Representative No.**</span></span>|<span data-ttu-id="503ea-139">Specificare il contatto che è il rappresentante fiscale per il cliente.</span><span class="sxs-lookup"><span data-stu-id="503ea-139">Specify the contact that is the tax representative for this customer.</span></span>|  

    <span data-ttu-id="503ea-140">È necessario impostare le informazioni di modo che [!INCLUDE[d365fin](../../includes/d365fin_md.md)] terrà traccia delle nuove transazioni che corrispondono alle soglie specificate dalle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="503ea-140">You have set up information so that [!INCLUDE[d365fin](../../includes/d365fin_md.md)] will track new transactions with VAT that meet the thresholds that are specified by the tax authorities.</span></span> <span data-ttu-id="503ea-141">Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="503ea-141">Before you create the first VAT transaction report, you should prepare the existing data.</span></span> <span data-ttu-id="503ea-142">Per ulteriori informazioni, vedere [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md).</span><span class="sxs-lookup"><span data-stu-id="503ea-142">For more information, see [Update VAT Transactions Data](how-to-update-vat-transactions-data.md).</span></span> <span data-ttu-id="503ea-143">È quindi possibile creare i report transazioni IVA.</span><span class="sxs-lookup"><span data-stu-id="503ea-143">You can then create VAT transactions reports.</span></span> <span data-ttu-id="503ea-144">Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).</span><span class="sxs-lookup"><span data-stu-id="503ea-144">For more information, see [Create Electronic VAT Transactions Reports](how-to-create-electronic-vat-transactions-reports.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="503ea-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="503ea-145">See Also</span></span>  
 <span data-ttu-id="503ea-146">[Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md) </span><span class="sxs-lookup"><span data-stu-id="503ea-146">[Update VAT Transactions Data](how-to-update-vat-transactions-data.md) </span></span>  
 <span data-ttu-id="503ea-147">[Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md) </span><span class="sxs-lookup"><span data-stu-id="503ea-147">[Create Electronic VAT Transactions Reports](how-to-create-electronic-vat-transactions-reports.md) </span></span>  
 [<span data-ttu-id="503ea-148">IVA italiana</span><span class="sxs-lookup"><span data-stu-id="503ea-148">Italian VAT</span></span>](italian-vat.md)
