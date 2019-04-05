---
title: Sincronizzare i contatti con clienti e fornitori| Documenti Microsoft
description: È possibile associare o sincronizzare le informazioni di contatto dei contatti che sono anche clienti, fornitori o conti correnti bancari, in modo da aggiornate le informazioni una volta sola.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 4785e0644e2cb4c615ed79fbd23bef74d25ca547
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801334"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="20e6b-103">Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="20e6b-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="20e6b-104">Se alcuni contatti sono anche clienti, fornitori o conti correnti bancari, è possibile sincronizzare le informazioni di contatto con il relativo cliente, fornitore o conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="20e6b-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="20e6b-105">La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.</span><span class="sxs-lookup"><span data-stu-id="20e6b-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="20e6b-106">Differenti modi di sincronizzare i contatti con clienti, fornitori e conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="20e6b-106">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="20e6b-107">È possibile sincronizzare i contatti con clienti, fornitori o i conti correnti bancari grazie a tre metodi:</span><span class="sxs-lookup"><span data-stu-id="20e6b-107">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="20e6b-108">collegare i contatti con clienti, fornitori o conti correnti bancari esistenti dalla scheda contatto.</span><span class="sxs-lookup"><span data-stu-id="20e6b-108">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="20e6b-109">Per ulteriori informazioni, vedere [Collegare i contatti con clienti, fornitori e conti correnti bancari](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="20e6b-109">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="20e6b-110">Creare clienti, fornitori o conti correnti bancari dal contatto.</span><span class="sxs-lookup"><span data-stu-id="20e6b-110">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="20e6b-111">Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="20e6b-111">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="20e6b-112">creare contatti da clienti, fornitori o conti correnti bancari.</span><span class="sxs-lookup"><span data-stu-id="20e6b-112">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="20e6b-113">Per ulteriori informazioni, vedere [Creare un contatto per una società da un cliente, fornitore o conto corrente bancario](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="20e6b-113">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="20e6b-114">Conseguenze della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="20e6b-114">Consequences of Synchronization</span></span>
<span data-ttu-id="20e6b-115">Quando il contatto è sincronizzato con il cliente, il fornitore, il conto corrente bancario:</span><span class="sxs-lookup"><span data-stu-id="20e6b-115">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="20e6b-116">è necessario aggiornare le informazioni solo in una scheda.</span><span class="sxs-lookup"><span data-stu-id="20e6b-116">You only have to update information in one place.</span></span> <span data-ttu-id="20e6b-117">Se ad esempio si modifica il numero di telefono del contatto, viene effettuato automaticamente lo stesso aggiornamento nel cliente, nel fornitore o nel conto corrente bancario;</span><span class="sxs-lookup"><span data-stu-id="20e6b-117">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="20e6b-118">se si è specificata una numerazione per i contatti, quando si crea una scheda cliente, una scheda fornitore o una scheda conto corrente bancario, viene creata automaticamente una scheda contatto per il cliente, il fornitore o il conto corrente bancario;</span><span class="sxs-lookup"><span data-stu-id="20e6b-118">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="20e6b-119">dal contatto è possibile creare offerte e ordini di vendita, oltre a offerte e ordini di acquisto;</span><span class="sxs-lookup"><span data-stu-id="20e6b-119">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="20e6b-120">è possibile registrare le interazioni quando si eseguono azioni specifiche, quali la stampa di ordini e ordini programmati, la creazione di ordini assistenza vendita, l'invio di e-mail e così via;</span><span class="sxs-lookup"><span data-stu-id="20e6b-120">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="20e6b-121">se si elimina un contatto collegato a un cliente, un fornitore o un conto corrente bancario, viene eliminato solo il contatto;</span><span class="sxs-lookup"><span data-stu-id="20e6b-121">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="20e6b-122">il cliente, il fornitore o il conto corrente bancario correlato non viene eliminato;</span><span class="sxs-lookup"><span data-stu-id="20e6b-122">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="20e6b-123">se si elimina un cliente, un fornitore o un conto corrente bancario collegato a un contatto, il contatto non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="20e6b-123">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="20e6b-124">Alcuni dettagli, relativi ad esempio a fatturazione e registrazione, non vengono visualizzati nella scheda contatto.</span><span class="sxs-lookup"><span data-stu-id="20e6b-124">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="20e6b-125">È quindi possibile aggiungerli manualmente alla scheda cliente, fornitore o conto corrente bancario quando si creano contatti come clienti, fornitori o conti correnti bancari.</span><span class="sxs-lookup"><span data-stu-id="20e6b-125">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="20e6b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20e6b-126">See Also</span></span>
[<span data-ttu-id="20e6b-127">Gestione dei contatti</span><span class="sxs-lookup"><span data-stu-id="20e6b-127">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="20e6b-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20e6b-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
