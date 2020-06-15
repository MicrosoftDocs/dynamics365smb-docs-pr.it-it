---
title: Come bloccare le vendite per i clienti
description: Se necessario, è possibile impedire a un cliente di essere incluso nei documenti di vendita e in altre transazioni di vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7cc82ab0aaf28b355117571d0d2cc5869141693f
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410718"
---
# <a name="block-customers"></a><span data-ttu-id="7476a-103">Blocca clienti</span><span class="sxs-lookup"><span data-stu-id="7476a-103">Block Customers</span></span>
<span data-ttu-id="7476a-104">È possibile bloccare un cliente, ad esempio a causa di insolvenza, in modo che il cliente non possa essere aggiunto ai documenti di vendita o che non sia possibile registrare transazioni per il cliente.</span><span class="sxs-lookup"><span data-stu-id="7476a-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="7476a-105">Oltre a bloccare un cliente, è possibile impostare le transazioni crediti v/clienti per il cliente con stato in sospeso collegato ai solleciti.</span><span class="sxs-lookup"><span data-stu-id="7476a-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="7476a-106">Per ulteriori informazioni, vedere [Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="7476a-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="7476a-107">Nella seguente tabella vengono illustrate le opzioni per bloccare i clienti.</span><span class="sxs-lookup"><span data-stu-id="7476a-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="7476a-108">Opzione</span><span class="sxs-lookup"><span data-stu-id="7476a-108">Option</span></span>|<span data-ttu-id="7476a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7476a-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="7476a-110">**Vuoto**</span><span class="sxs-lookup"><span data-stu-id="7476a-110">**Blank**</span></span>|<span data-ttu-id="7476a-111">Per il cliente sono consentite tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="7476a-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="7476a-112">**Spedizione**</span><span class="sxs-lookup"><span data-stu-id="7476a-112">**Ship**</span></span>|<span data-ttu-id="7476a-113">Non è possibile creare nuovi ordini e nuove spedizioni per il cliente.</span><span class="sxs-lookup"><span data-stu-id="7476a-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="7476a-114">È possibile fatturare le spedizioni esistenti non ancora fatturate.</span><span class="sxs-lookup"><span data-stu-id="7476a-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="7476a-115">**Fattura**</span><span class="sxs-lookup"><span data-stu-id="7476a-115">**Invoice**</span></span>|<span data-ttu-id="7476a-116">Non è possibile creare nuovi ordini, nuove spedizioni o nuove fatture per il cliente.</span><span class="sxs-lookup"><span data-stu-id="7476a-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="7476a-117">Non è possibile fatturare le spedizioni esistenti non ancora fatturate.</span><span class="sxs-lookup"><span data-stu-id="7476a-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="7476a-118">Puoi comunque inviare promemoria e note di addebito interessi al cliente.</span><span class="sxs-lookup"><span data-stu-id="7476a-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="7476a-119">**Tutto**</span><span class="sxs-lookup"><span data-stu-id="7476a-119">**All**</span></span>|<span data-ttu-id="7476a-120">Non è consentita alcuna transazione, inclusi i pagamenti, per il cliente.</span><span class="sxs-lookup"><span data-stu-id="7476a-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="7476a-121">Per bloccare un cliente</span><span class="sxs-lookup"><span data-stu-id="7476a-121">To block a customer</span></span>  
1. <span data-ttu-id="7476a-122">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="7476a-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="7476a-123">Selezionare un cliente, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="7476a-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="7476a-124">Nel campo **Bloccato**, scegliere cosa bloccare, come descritto nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="7476a-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="7476a-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7476a-125">See Also</span></span>  
[<span data-ttu-id="7476a-126">Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="7476a-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="7476a-127">Riscuotere i saldi inevasi</span><span class="sxs-lookup"><span data-stu-id="7476a-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="7476a-128">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="7476a-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
