---
title: 'Procedura: Preparare i report di transazioni IVA'
description: È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e594d05d02f94a944f6fe83bc53d7c610a07e8f7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382897"
---
# <a name="prepare-for-vat-transactions-reports"></a><span data-ttu-id="8f881-103">Preparare i report di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="8f881-103">Prepare for VAT Transactions Reports</span></span>
<span data-ttu-id="8f881-104">È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA.</span><span class="sxs-lookup"><span data-stu-id="8f881-104">You must submit periodic reports to the tax authorities to list all transactions that include VAT.</span></span> <span data-ttu-id="8f881-105">L'autorità fiscale stabilisce le soglie richieste per la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="8f881-105">The tax authority establishes the thresholds at which reporting is required.</span></span> <span data-ttu-id="8f881-106">Attualmente, la soglia è impostata su zero, a indicare che tutte le transazioni vengono dichiarate.</span><span class="sxs-lookup"><span data-stu-id="8f881-106">Currently, the threshold is set at zero, meaning that all transactions are to be reported.</span></span> <span data-ttu-id="8f881-107">Per prepararsi per le dichiarazioni, è necessario impostare la registrazione IVA in modo da includere gli importi di dichiarazione della transazione IVA.</span><span class="sxs-lookup"><span data-stu-id="8f881-107">To prepare for these reports, you must set up VAT posting to include VAT transaction report amounts.</span></span>  

## <a name="to-set-up-vat-transaction-amounts"></a><span data-ttu-id="8f881-108">Per impostare gli importi delle transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="8f881-108">To set up VAT transaction amounts</span></span>  

1.  <span data-ttu-id="8f881-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup registrazioni IVA** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8f881-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Posting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8f881-110">Scegliere l'azione **Importo report transazioni IVA**.</span><span class="sxs-lookup"><span data-stu-id="8f881-110">Choose the **VAT Transaction Report Amount** action.</span></span>  
3.  <span data-ttu-id="8f881-111">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8f881-111">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8f881-112">Campo</span><span class="sxs-lookup"><span data-stu-id="8f881-112">Field</span></span>|<span data-ttu-id="8f881-113">Description</span><span class="sxs-lookup"><span data-stu-id="8f881-113">Description</span></span>|  
    |------------------------------------|---------------------------------------|  
    |<span data-ttu-id="8f881-114">**Persona fisica**</span><span class="sxs-lookup"><span data-stu-id="8f881-114">**Individual Person**</span></span>|<span data-ttu-id="8f881-115">Selezionare se questo cliente è una persona fisica.</span><span class="sxs-lookup"><span data-stu-id="8f881-115">Select if this customer is an individual person.</span></span>|  
    |<span data-ttu-id="8f881-116">**Soggetto residente**</span><span class="sxs-lookup"><span data-stu-id="8f881-116">**Resident**</span></span>|<span data-ttu-id="8f881-117">Specificare se il cliente è residente in Italia.</span><span class="sxs-lookup"><span data-stu-id="8f881-117">Specify if the customer is a resident in Italy.</span></span><br /><br /> <span data-ttu-id="8f881-118">Se un cliente non è un residente, è necessario specificare anche un rappresentante fiscale nella Scheda dettaglio **Commercio estero**.</span><span class="sxs-lookup"><span data-stu-id="8f881-118">If a customer is not a resident, you must also specify a tax representative on the **Foreign Trade** FastTab.</span></span>|  
    |<span data-ttu-id="8f881-119">**Primo nome**</span><span class="sxs-lookup"><span data-stu-id="8f881-119">**First Name**</span></span>|<span data-ttu-id="8f881-120">Specifica il nome della persona.</span><span class="sxs-lookup"><span data-stu-id="8f881-120">Specifies the first name of the person.</span></span>|  
    |<span data-ttu-id="8f881-121">**Cognome**</span><span class="sxs-lookup"><span data-stu-id="8f881-121">**Last Name**</span></span>|<span data-ttu-id="8f881-122">Specifica il cognome della persona.</span><span class="sxs-lookup"><span data-stu-id="8f881-122">Specifies the last name of the person.</span></span>|  
    |<span data-ttu-id="8f881-123">**Data di nascita**</span><span class="sxs-lookup"><span data-stu-id="8f881-123">**Date of Birth**</span></span>|<span data-ttu-id="8f881-124">Specifica la data di nascita della persona.</span><span class="sxs-lookup"><span data-stu-id="8f881-124">Specifies the date of birth of the person.</span></span>|  
    |<span data-ttu-id="8f881-125">**Luogo di nascita**</span><span class="sxs-lookup"><span data-stu-id="8f881-125">**Place of Birth**</span></span>|<span data-ttu-id="8f881-126">Specifica il luogo di nascita della persona.</span><span class="sxs-lookup"><span data-stu-id="8f881-126">Specifies the place of birth of the person.</span></span>|  

3.  <span data-ttu-id="8f881-127">Se il cliente non è in residente in Italia e non è una persona fisica, è necessario specificare un rappresentante fiscale per il cliente.</span><span class="sxs-lookup"><span data-stu-id="8f881-127">If the customer is not resident in Italy and is not an individual person, you must specify a tax representative for the customer.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8f881-128">Prima di poter specificare un rappresentante fiscale, è necessario creare il rappresentante fiscale come contatto.</span><span class="sxs-lookup"><span data-stu-id="8f881-128">Before you can specify a tax representative, you must have created the tax representative as a contact.</span></span>  

### <a name="to-specify-a-tax-representative-for-a-non-resident-customer"></a><span data-ttu-id="8f881-129">Per specificare un rappresentante fiscale per un cliente non residente</span><span class="sxs-lookup"><span data-stu-id="8f881-129">To specify a tax representative for a non-resident customer</span></span>  

1.  <span data-ttu-id="8f881-130">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8f881-130">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f881-131">Selezionare un cliente.</span><span class="sxs-lookup"><span data-stu-id="8f881-131">Select a customer.</span></span>
2.  <span data-ttu-id="8f881-132">Compilare i campi nella Scheda dettaglio **Commercio estero** come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="8f881-132">On the **Foreign Trade** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8f881-133">Campo</span><span class="sxs-lookup"><span data-stu-id="8f881-133">Field</span></span>|<span data-ttu-id="8f881-134">Description</span><span class="sxs-lookup"><span data-stu-id="8f881-134">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8f881-135">**Tipo di rappresentante fiscale**</span><span class="sxs-lookup"><span data-stu-id="8f881-135">**Tax Representative Type**</span></span>|<span data-ttu-id="8f881-136">Specifica se il rappresentante fiscale è un cliente o un contatto.</span><span class="sxs-lookup"><span data-stu-id="8f881-136">Specifies if the tax representative is a customer or a contact.</span></span> <span data-ttu-id="8f881-137">È necessario impostare il campo su **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="8f881-137">You must set this field to **Contact**.</span></span>|  
    |<span data-ttu-id="8f881-138">**Nr. rappresentante fiscale**</span><span class="sxs-lookup"><span data-stu-id="8f881-138">**Tax Representative No.**</span></span>|<span data-ttu-id="8f881-139">Specificare il contatto che è il rappresentante fiscale per il cliente.</span><span class="sxs-lookup"><span data-stu-id="8f881-139">Specify the contact that is the tax representative for this customer.</span></span>|  

    <span data-ttu-id="8f881-140">È necessario impostare le informazioni di modo che [!INCLUDE[prod_short](../../includes/prod_short.md)] terrà traccia delle nuove transazioni che corrispondono alle soglie specificate dalle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="8f881-140">You have set up information so that [!INCLUDE[prod_short](../../includes/prod_short.md)] will track new transactions with VAT that meet the thresholds that are specified by the tax authorities.</span></span> <span data-ttu-id="8f881-141">Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="8f881-141">Before you create the first VAT transaction report, you should prepare the existing data.</span></span> <span data-ttu-id="8f881-142">Per ulteriori informazioni, vedere [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md).</span><span class="sxs-lookup"><span data-stu-id="8f881-142">For more information, see [Update VAT Transactions Data](how-to-update-vat-transactions-data.md).</span></span> <span data-ttu-id="8f881-143">È quindi possibile creare i report transazioni IVA.</span><span class="sxs-lookup"><span data-stu-id="8f881-143">You can then create VAT transactions reports.</span></span> <span data-ttu-id="8f881-144">Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).</span><span class="sxs-lookup"><span data-stu-id="8f881-144">For more information, see [Create Electronic VAT Transactions Reports](how-to-create-electronic-vat-transactions-reports.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8f881-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f881-145">See Also</span></span>  
 <span data-ttu-id="8f881-146">[Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md) </span><span class="sxs-lookup"><span data-stu-id="8f881-146">[Update VAT Transactions Data](how-to-update-vat-transactions-data.md) </span></span>  
 <span data-ttu-id="8f881-147">[Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md) </span><span class="sxs-lookup"><span data-stu-id="8f881-147">[Create Electronic VAT Transactions Reports](how-to-create-electronic-vat-transactions-reports.md) </span></span>  
 [<span data-ttu-id="8f881-148">IVA italiana</span><span class="sxs-lookup"><span data-stu-id="8f881-148">Italian VAT</span></span>](italian-vat.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]