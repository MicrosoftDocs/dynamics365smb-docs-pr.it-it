---
title: Impostare contratti di assistenza | Documenti Microsoft
description: Informazioni su come impostare i contratti di assistenza.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b221b125a65dbad46b56172bc267a5da382dc765
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-service-contracts"></a><span data-ttu-id="ed48e-103">Impostare i contratti di assistenza</span><span class="sxs-lookup"><span data-stu-id="ed48e-103">Set Up Service Contracts</span></span>
<span data-ttu-id="ed48e-104">Prima di poter utilizzare i contratti, è necessario impostare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ed48e-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="ed48e-105">**Gruppi contratti assistenza**: raggruppano i contratti di assistenza in qualche modo correlati tra di loro.</span><span class="sxs-lookup"><span data-stu-id="ed48e-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="ed48e-106">**Gruppi conto del contratto di assistenza**: raggruppano i conti dei contratti di assistenza per le fatture di assistenza create per i contratti di assistenza.</span><span class="sxs-lookup"><span data-stu-id="ed48e-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="ed48e-107">È possibile assegnare tali gruppi ai contratti di assistenza.</span><span class="sxs-lookup"><span data-stu-id="ed48e-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="ed48e-108">**Modelli di contratto**: definiscono i layout dei contratti che includono i dettagli dei contratti di assistenza utilizzati più comunemente.</span><span class="sxs-lookup"><span data-stu-id="ed48e-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="ed48e-109">È possibile creare le offerte di contratto di assistenza utilizzando i modelli.</span><span class="sxs-lookup"><span data-stu-id="ed48e-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="ed48e-110">Quando si crea un'offerta di contratto, i campi vengono automaticamente riempiti con il contenuto dei campi del modello.</span><span class="sxs-lookup"><span data-stu-id="ed48e-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="ed48e-111">**Modelli clienti**: consentono di creare delle offerte per i contatti o i potenziali clienti che non sono registrati come clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed48e-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="ed48e-112">Per impostare un gruppo di contratti di assistenza</span><span class="sxs-lookup"><span data-stu-id="ed48e-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="ed48e-113">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Gruppi contratti assistenza**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ed48e-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ed48e-114">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ed48e-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ed48e-115">Scegliere la casella di controllo **Sc. solo su ordini contr.** se si desidera che gli sconti contratto o assistenza siano validi solo per gli ordini di assistenza contratto, ad esempio la manutenzione.</span><span class="sxs-lookup"><span data-stu-id="ed48e-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="ed48e-116">Per impostare un gruppo conto dei contratti di assistenza</span><span class="sxs-lookup"><span data-stu-id="ed48e-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="ed48e-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Gruppi conto contratto assist.**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ed48e-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ed48e-118">Creare un nuovo gruppo di conto dei contratti dei assistenza.</span><span class="sxs-lookup"><span data-stu-id="ed48e-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="ed48e-119">Compilare i campi **Codice** e **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="ed48e-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="ed48e-120">Questi campi forniscono una descrizione del gruppo conto contratti di assistenza.</span><span class="sxs-lookup"><span data-stu-id="ed48e-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="ed48e-121">Compilare il campo **Conto contratto non prepagato**, quindi scegliere il numero di conto di contabilità generale per il conto non prepagato.</span><span class="sxs-lookup"><span data-stu-id="ed48e-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="ed48e-122">Nel campo **Conto contratto prepagato** scegliere il numero di conto di contabilità generale per il conto prepagato.</span><span class="sxs-lookup"><span data-stu-id="ed48e-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="ed48e-123">Per impostare un modello di contratto</span><span class="sxs-lookup"><span data-stu-id="ed48e-123">To set up a contract template</span></span>  
1. <span data-ttu-id="ed48e-124">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modelli contratti assistenza**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ed48e-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ed48e-125">Creare un nuovo modello di contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="ed48e-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="ed48e-126">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="ed48e-126">In the **No.**</span></span> <span data-ttu-id="ed48e-127">immettere un numero per il modello di contratto.</span><span class="sxs-lookup"><span data-stu-id="ed48e-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="ed48e-128">In alternativa, se è stata impostata una numerazione per i modelli di contratti nella finestra **Setup gest. assist.**, è possibile premere INVIO per inserire il successivo numero di modello di contratto disponibile.</span><span class="sxs-lookup"><span data-stu-id="ed48e-128">Alternatively, if you have set up number series for contract templates in the **Service Mgt. Setup** window, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="ed48e-129">Compilare gli altri campi, se pertinenti.</span><span class="sxs-lookup"><span data-stu-id="ed48e-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="ed48e-130">Nella Scheda dettaglio **Fattura** compilare i campi **Codice gr. conto contratto assist.**, **Periodo di fatturazione** e così via.</span><span class="sxs-lookup"><span data-stu-id="ed48e-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="ed48e-131">Compilare gli altri campi, se pertinenti.</span><span class="sxs-lookup"><span data-stu-id="ed48e-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="ed48e-132">Scegliere l'azione **Sconti assistenza** per aggiungere sconti contrattuali.</span><span class="sxs-lookup"><span data-stu-id="ed48e-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="ed48e-133">Per impostare un modello di cliente</span><span class="sxs-lookup"><span data-stu-id="ed48e-133">To set up a customer template</span></span>  
1. <span data-ttu-id="ed48e-134">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modelli cliente**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ed48e-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ed48e-135">Creare una nuova scheda modello cliente.</span><span class="sxs-lookup"><span data-stu-id="ed48e-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="ed48e-136">Nella Scheda dettaglio **Generale** immettere un codice e una descrizione per il modello cliente rispettivamente nei campi **Codice** e **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="ed48e-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="ed48e-137">Per definire i criteri di ricerca, compilare gli altri campi, ad esempio **Cod. paese**, **Cod. regione** e **Cod. lingua**.</span><span class="sxs-lookup"><span data-stu-id="ed48e-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="ed48e-138">Compilare i campi **Cat. Reg. Business** e **Cat. Reg. Cliente**.</span><span class="sxs-lookup"><span data-stu-id="ed48e-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed48e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed48e-139">See Also</span></span>
[<span data-ttu-id="ed48e-140">Impostazione della gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="ed48e-140">Setting Up Service Management</span></span>](service-setup-service.md)
