---
title: Collegare i movimenti in diverse valute| Documenti Microsoft
description: "Se si effettua una vendita in una valuta e si riceve il pagamento in un'altra, è possibile collegare il movimento contabile in più valute."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="39c69-103">Procedura: Abilitare il collegamento dei movimenti contabili fornitore in valute diverse</span><span class="sxs-lookup"><span data-stu-id="39c69-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="39c69-104">Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare il pagamento all'acquisto.</span><span class="sxs-lookup"><span data-stu-id="39c69-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="39c69-105">In modo analogo, se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile collegare il pagamento alla fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="39c69-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="39c69-106">Nella procedura riportata di seguito viene descritto come configurare questa impostazione per i movimenti contabili fornitori nella finestra **Setup contabilità fornitori e acquisti**.</span><span class="sxs-lookup"><span data-stu-id="39c69-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="39c69-107">L'impostazione è simile per i movimenti contabili clienti nella finestra **Setup contabilità clienti e vendite**.</span><span class="sxs-lookup"><span data-stu-id="39c69-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="39c69-108">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="39c69-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="39c69-109">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="39c69-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="39c69-110">Per abilitare il collegamento dei movimenti contabili fornitore in valute diverse</span><span class="sxs-lookup"><span data-stu-id="39c69-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="39c69-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup contabilità fornitori e acquisti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="39c69-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="39c69-112">Nel campo **Collegamenti tra valute** selezionare una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="39c69-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="39c69-113">Opzione</span><span class="sxs-lookup"><span data-stu-id="39c69-113">Option</span></span> | <span data-ttu-id="39c69-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39c69-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="39c69-115">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39c69-115">None</span></span> |<span data-ttu-id="39c69-116">Collegamento fra valute non consentito.</span><span class="sxs-lookup"><span data-stu-id="39c69-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="39c69-117">UE</span><span class="sxs-lookup"><span data-stu-id="39c69-117">EMU</span></span> |<span data-ttu-id="39c69-118">Collegamento fra valute UE consentito.</span><span class="sxs-lookup"><span data-stu-id="39c69-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="39c69-119">Tutto</span><span class="sxs-lookup"><span data-stu-id="39c69-119">All</span></span> |<span data-ttu-id="39c69-120">Collegamento fra tutte le valute consentito</span><span class="sxs-lookup"><span data-stu-id="39c69-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="39c69-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c69-121">See Also</span></span>
[<span data-ttu-id="39c69-122">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="39c69-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="39c69-123">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="39c69-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="39c69-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39c69-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

