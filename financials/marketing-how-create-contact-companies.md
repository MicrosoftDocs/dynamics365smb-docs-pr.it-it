---
title: "Creare società contatto| Documenti Microsoft"
description: "Descrive come creare un contatto per ogni società nuova o potenziale con cui si interagisce o si hanno relazioni."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6a1141c352dd93657d32bb83067ce32077901a47
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-create-contact-companies"></a><span data-ttu-id="768fc-103">Procedura: creare società contatto</span><span class="sxs-lookup"><span data-stu-id="768fc-103">How to: Create Contact Companies</span></span>
<span data-ttu-id="768fc-104">È possibile creare un contatto per ogni nuova società con cui si interagisce, ad esempio cliente, fornitore, potenziale cliente, banca, studio legale, consulente e così via.</span><span class="sxs-lookup"><span data-stu-id="768fc-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="768fc-105">Esistono due modi per creare un contatto: da zero o da un cliente, un fornitore o da un conto corrente bancario esistente.</span><span class="sxs-lookup"><span data-stu-id="768fc-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="768fc-106">Prima di creare un contatto, si consiglia di verificare le impostazioni nella finestra **Setup marketing**.</span><span class="sxs-lookup"><span data-stu-id="768fc-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="768fc-107">Per ulteriori informazioni, vedere [Setup Relationship Management](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="768fc-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="768fc-108">Creare una società contatto da zero</span><span class="sxs-lookup"><span data-stu-id="768fc-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="768fc-109">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Contatti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="768fc-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="768fc-110">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="768fc-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="768fc-111">Nel campo **Nr. campo** inserire un numero per il contatto.</span><span class="sxs-lookup"><span data-stu-id="768fc-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="768fc-112">In alternativa, se è stata impostata una numerazione per i contatti nella finestra **Setup marketing**, è possibile premere INVIO per selezionare il successivo numero di contatto disponibile.</span><span class="sxs-lookup"><span data-stu-id="768fc-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="768fc-113">Impostare il **Tipo** su **Società**.</span><span class="sxs-lookup"><span data-stu-id="768fc-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="768fc-114">Compilare gli altri campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="768fc-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="768fc-115">Per creare un contatto per una società da un cliente, fornitore o conto corrente bancario</span><span class="sxs-lookup"><span data-stu-id="768fc-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="768fc-116">Se è già stato impostato un numero di clienti, fornitori e conti correnti bancari, è possibile creare contatti sulla base dei dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="768fc-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="768fc-117">Quando si crea un contatto in questo modo, le informazioni di contatto verranno sincronizzate con clienti, fornitori, o le informazioni del conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="768fc-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="768fc-118">Prima di creare la società contatto in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella finestra **Setup marketing**.</span><span class="sxs-lookup"><span data-stu-id="768fc-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="768fc-119">Se verranno creati i contatti da conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella finestra **Setup contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="768fc-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="768fc-120">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report") e immettere una delle seguenti opzioni, in base a dove si desidera creare contatti, quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="768fc-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="768fc-121">**Crea contatti da clienti**</span><span class="sxs-lookup"><span data-stu-id="768fc-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="768fc-122">**Crea contatti da fornitori**</span><span class="sxs-lookup"><span data-stu-id="768fc-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="768fc-123">**Crea contatti da conti correnti bancari**</span><span class="sxs-lookup"><span data-stu-id="768fc-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="768fc-124">Nella finestra del processo batch che si apre, nella sezione **Cliente**, **Fornitore** o **Conti correnti bancari**, impostare i filtri se si desidera creare contatti rispettivamente da clienti, fornitori o conti correnti bancari specifici.</span><span class="sxs-lookup"><span data-stu-id="768fc-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="768fc-125">Scegliere **OK** per avviare la creazione di contatti.</span><span class="sxs-lookup"><span data-stu-id="768fc-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="768fc-126">Ai nuovi contatti verranno assegnati numeri contatto successivi all'interno della numerazione.</span><span class="sxs-lookup"><span data-stu-id="768fc-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="768fc-127">Ai nuovi contatti creati verrà assegnata la relazione d'affari per i fornitori specificata nella finestra **Setup marketing**.</span><span class="sxs-lookup"><span data-stu-id="768fc-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="768fc-128">È anche possibile creare un cliente, fornitore o conto corrente bancario da un contatto.</span><span class="sxs-lookup"><span data-stu-id="768fc-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="768fc-129">Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="768fc-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="768fc-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="768fc-130">See Also</span></span>
[<span data-ttu-id="768fc-131">Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="768fc-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="768fc-132">Assegnare relazioni d'affari ai contatti</span><span class="sxs-lookup"><span data-stu-id="768fc-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="768fc-133">Assegnare settori industriali a un contatto</span><span class="sxs-lookup"><span data-stu-id="768fc-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="768fc-134">Assegnare gruppi di mailing a un contatto</span><span class="sxs-lookup"><span data-stu-id="768fc-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="768fc-135">Procedura: Creare contatti</span><span class="sxs-lookup"><span data-stu-id="768fc-135">How to: Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="768fc-136">Utilizzo di Financials</span><span class="sxs-lookup"><span data-stu-id="768fc-136">Working with Financials</span></span>](ui-work-product.md)

