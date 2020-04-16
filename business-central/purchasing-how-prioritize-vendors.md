---
title: Assegnare un livello di priorità a un fornitore | Documenti Microsoft
description: È possibile assegnare dei numeri ai fornitori per assegnare loro una priorità e semplificare i suggerimenti di pagamento in Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: cede9a43bb66d314640e0e28443c63c925fd575a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192725"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="ecfe7-103">Attribuire un ordine di priorità ai fornitori</span><span class="sxs-lookup"><span data-stu-id="ecfe7-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ecfe7-104">può fornire suggerimenti di pagamento ai fornitori, ad esempio pagamenti con scadenza a breve termine oppure pagamenti che prevedono uno sconto.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="ecfe7-105">Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="ecfe7-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="ecfe7-106">Innanzitutto, è necessario assegnare una priorità ai fornitori assegnando loro dei numeri.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="ecfe7-107">Per attribuire un ordine di priorità ai fornitori</span><span class="sxs-lookup"><span data-stu-id="ecfe7-107">To prioritize vendors</span></span>
1. <span data-ttu-id="ecfe7-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="ecfe7-109">Selezionare il fornitore appropriato e scegliere **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="ecfe7-110">Nel campo **Priorità** immettere un numero.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-110">In the **Priority** field, enter a number.</span></span>

<span data-ttu-id="ecfe7-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)] il numero più basso, escluso lo 0, ha la massima priorità.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-111">[!INCLUDE[d365fin](includes/d365fin_md.md)] considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="ecfe7-112">Così, ad esempio, se si usano 1, 2 e 3, 1 avrà la massima priorità.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="ecfe7-113">Se non si desidera dare la priorità a un fornitore, lasciare vuoto il campo **Priorità**.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="ecfe7-114">Quindi, se si usa la funzione di suggerimento di pagamento, il fornitore si troverà dopo tutti i fornitori che hanno un numero di priorità.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="ecfe7-115">Si possono immettere tutti i livelli di priorità necessari.</span><span class="sxs-lookup"><span data-stu-id="ecfe7-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="ecfe7-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ecfe7-116">See Also</span></span>
[<span data-ttu-id="ecfe7-117">Impostazioni acquisti</span><span class="sxs-lookup"><span data-stu-id="ecfe7-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="ecfe7-118">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="ecfe7-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ecfe7-119">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ecfe7-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
