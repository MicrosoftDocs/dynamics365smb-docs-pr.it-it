---
title: Creare un cliente o un fornitore da un contatto| Documenti Microsoft
description: "Si può registrare un contatto esistente come cliente, fornitore o conto corrente bancario utilizzando i dati esistenti e specificando la relazione d'affari."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 07c56f109ee2e4c348c0f654ceadc4018174c0d5
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="46eea-103">Per creare un contatto da un cliente, un fornitore o un conto corrente bancario</span><span class="sxs-lookup"><span data-stu-id="46eea-103">Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="46eea-104">È possibile registrare alcuni contatti come clienti, fornitori oppure conti correnti bancari esistenti.</span><span class="sxs-lookup"><span data-stu-id="46eea-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="46eea-105">La creazione di un cliente, un fornitore o un conto bancario da un contatto consente di utilizzare i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="46eea-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="46eea-106">Quando si crea un cliente, un fornitore o un conto bancario in questo modo, le informazioni verranno sincronizzate con il contatto.</span><span class="sxs-lookup"><span data-stu-id="46eea-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="46eea-107">La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.</span><span class="sxs-lookup"><span data-stu-id="46eea-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="46eea-108">Prima di poter registrare i contatti in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella finestra **Setup marketing**.</span><span class="sxs-lookup"><span data-stu-id="46eea-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="46eea-109">Se verranno registrati i contatti come conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella finestra **Setup contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="46eea-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="46eea-110">Per creare un contatto come cliente, fornitore o conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="46eea-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="46eea-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="46eea-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="46eea-112">Selezionare il contatto che si desidera creare come cliente, fornitore o conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="46eea-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="46eea-113">Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.</span><span class="sxs-lookup"><span data-stu-id="46eea-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="46eea-114">Scegliere Sì nel messaggio che verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="46eea-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="46eea-115">Le informazioni di contatto vengono trasferite dalla scheda **Contatto** alla scheda **C/C bancario**, alla scheda **Cliente** o alla scheda **Fornitore**.</span><span class="sxs-lookup"><span data-stu-id="46eea-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="46eea-116">È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione.</span><span class="sxs-lookup"><span data-stu-id="46eea-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="46eea-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46eea-117">See Also</span></span>
[<span data-ttu-id="46eea-118">Creare società contatto</span><span class="sxs-lookup"><span data-stu-id="46eea-118">Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="46eea-119">Creare contatti</span><span class="sxs-lookup"><span data-stu-id="46eea-119">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="46eea-120">Setup Relationship Management</span><span class="sxs-lookup"><span data-stu-id="46eea-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="46eea-121">Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="46eea-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="46eea-122">Collegare i contatti con clienti, fornitori o conti correnti bancari esistenti</span><span class="sxs-lookup"><span data-stu-id="46eea-122">Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="46eea-123">Assegnare relazioni d'affari ai contatti</span><span class="sxs-lookup"><span data-stu-id="46eea-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="46eea-124">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="46eea-124">Working with Business Central</span></span>](ui-work-product.md)

