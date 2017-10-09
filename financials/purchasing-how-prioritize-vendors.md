---
title: "Assegnare un livello di priorità a un fornitore | Documenti Microsoft"
description: "È possibile assegnare dei numeri ai fornitori per assegnare loro una priorità e semplificare i suggerimenti di pagamento in Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2c91b28daf27ddd2b698ffe4338bbf92fd1f9adf
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-prioritize-vendors"></a><span data-ttu-id="5fee9-103">Procedura: Attribuire un ordine di priorità ai fornitori</span><span class="sxs-lookup"><span data-stu-id="5fee9-103">How to: Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5fee9-104"> può fornire suggerimenti di pagamento ai fornitori, ad esempio pagamenti con scadenza a breve termine oppure pagamenti che prevedono uno sconto.</span><span class="sxs-lookup"><span data-stu-id="5fee9-104"> can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="5fee9-105">Per ulteriori informazioni, vedere [Procedura: Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="5fee9-105">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="5fee9-106">Innanzitutto, è necessario assegnare una priorità ai fornitori assegnando loro dei numeri.</span><span class="sxs-lookup"><span data-stu-id="5fee9-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="5fee9-107">Per attribuire un ordine di priorità ai fornitori</span><span class="sxs-lookup"><span data-stu-id="5fee9-107">To prioritize vendors</span></span>
1. <span data-ttu-id="5fee9-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fornitori**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="5fee9-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fee9-109">Selezionare il fornitore appropriato e scegliere **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="5fee9-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="5fee9-110">Nel campo **Priorità** immettere un numero.</span><span class="sxs-lookup"><span data-stu-id="5fee9-110">In the **Priority** field, enter a number.</span></span>

<span data-ttu-id="5fee9-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)] il numero più basso, escluso lo 0, ha la massima priorità.</span><span class="sxs-lookup"><span data-stu-id="5fee9-111">[!INCLUDE[d365fin](includes/d365fin_md.md)] considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="5fee9-112">Così, ad esempio, se si usano 1, 2 e 3, 1 avrà la massima priorità.</span><span class="sxs-lookup"><span data-stu-id="5fee9-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="5fee9-113">Se non si desidera dare la priorità a un fornitore, lasciare vuoto il campo **Priorità**.</span><span class="sxs-lookup"><span data-stu-id="5fee9-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="5fee9-114">Quindi, se si usa la funzione di suggerimento di pagamento, il fornitore si troverà dopo tutti i fornitori che hanno un numero di priorità.</span><span class="sxs-lookup"><span data-stu-id="5fee9-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="5fee9-115">Si possono immettere tutti i livelli di priorità necessari.</span><span class="sxs-lookup"><span data-stu-id="5fee9-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fee9-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fee9-116">See Also</span></span>
[<span data-ttu-id="5fee9-117">Impostazioni acquisti</span><span class="sxs-lookup"><span data-stu-id="5fee9-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="5fee9-118">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="5fee9-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="5fee9-119">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fee9-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

