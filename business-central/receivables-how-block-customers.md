---
title: Come bloccare le vendite di articoli per i clienti dalle vendite o dagli acquisti
description: In Business Central, un articolo può essere contrassegnato come bloccato per la vendita, per l'acquisto o per tutti gli scopi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2b0d5b15571b7e8af1ed1dbee22859f4c131aa3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316622"
---
# <a name="block-customers"></a><span data-ttu-id="1c61c-103">Blocca clienti</span><span class="sxs-lookup"><span data-stu-id="1c61c-103">Block Customers</span></span>
<span data-ttu-id="1c61c-104">È possibile bloccare un cliente, ad esempio a causa di insolvenza, in modo che il cliente non possa essere aggiunto ai documenti di vendita o che non sia possibile registrare transazioni per il cliente.</span><span class="sxs-lookup"><span data-stu-id="1c61c-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="1c61c-105">Oltre a bloccare un cliente, è possibile impostare le transazioni crediti v/clienti per il cliente con stato in sospeso collegato ai solleciti.</span><span class="sxs-lookup"><span data-stu-id="1c61c-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="1c61c-106">Per ulteriori informazioni, vedere [Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="1c61c-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="1c61c-107">Nella seguente tabella vengono illustrate le diverse opzioni di blocco.</span><span class="sxs-lookup"><span data-stu-id="1c61c-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="1c61c-108">Opzione</span><span class="sxs-lookup"><span data-stu-id="1c61c-108">Option</span></span>|<span data-ttu-id="1c61c-109">Description</span><span class="sxs-lookup"><span data-stu-id="1c61c-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="1c61c-110">**Vuoto**</span><span class="sxs-lookup"><span data-stu-id="1c61c-110">**Blank**</span></span>|<span data-ttu-id="1c61c-111">Per il cliente sono consentite tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="1c61c-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="1c61c-112">**Spedizione**</span><span class="sxs-lookup"><span data-stu-id="1c61c-112">**Ship**</span></span>|<span data-ttu-id="1c61c-113">Non è possibile creare nuovi ordini e nuove spedizioni per il cliente.</span><span class="sxs-lookup"><span data-stu-id="1c61c-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="1c61c-114">È possibile fatturare le spedizioni esistenti non ancora fatturate.</span><span class="sxs-lookup"><span data-stu-id="1c61c-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="1c61c-115">**Fattura**</span><span class="sxs-lookup"><span data-stu-id="1c61c-115">**Invoice**</span></span>|<span data-ttu-id="1c61c-116">Non è possibile creare nuovi ordini, nuove spedizioni o nuove fatture per il cliente.</span><span class="sxs-lookup"><span data-stu-id="1c61c-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="1c61c-117">Non è possibile fatturare le spedizioni esistenti non ancora fatturate.</span><span class="sxs-lookup"><span data-stu-id="1c61c-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="1c61c-118">**Tutto**</span><span class="sxs-lookup"><span data-stu-id="1c61c-118">**All**</span></span>|<span data-ttu-id="1c61c-119">Non è consentita alcuna transazione, inclusi i pagamenti, per il cliente.</span><span class="sxs-lookup"><span data-stu-id="1c61c-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="1c61c-120">Per bloccare un cliente</span><span class="sxs-lookup"><span data-stu-id="1c61c-120">To block a customer</span></span>  
1. <span data-ttu-id="1c61c-121">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1c61c-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="1c61c-122">Selezionare un cliente, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="1c61c-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="1c61c-123">Compilare il campo **Bloccato** con una delle opzioni descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1c61c-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c61c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c61c-124">See Also</span></span>  
[<span data-ttu-id="1c61c-125">Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="1c61c-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="1c61c-126">Riscuotere i saldi inevasi</span><span class="sxs-lookup"><span data-stu-id="1c61c-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="1c61c-127">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="1c61c-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
