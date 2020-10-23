---
title: 'Procedura: Rintracciare i colli | Documenti Microsoft'
description: È possibile utilizzare il servizio di tracciabilità degli spedizionieri per vedere lo stato di avanzamento di una consegna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b0cf72609a180d271604dd276f840efbc6b1aa6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910657"
---
# <a name="track-packages"></a><span data-ttu-id="f1eee-103">Rintracciare i colli</span><span class="sxs-lookup"><span data-stu-id="f1eee-103">Track Packages</span></span>

<span data-ttu-id="f1eee-104">Molti spedizionieri forniscono dei servizi via Internet che consentono di seguire il percorso di pacchi che sono stati loro affidati.</span><span class="sxs-lookup"><span data-stu-id="f1eee-104">A number of shipping agents provide services on the Internet that allow you to track parcels you have handed over to the agent.</span></span> <span data-ttu-id="f1eee-105">Se ci si avvale di spedizionieri che offrono questo tipo di servizio può risultare molto utile impostare delle informazioni di base che vengono utilizzate per rintracciare automaticamente le spedizioni registrate, fatture di vendita registrate, note di credito di vendita registrate e carichi da reso registrati.</span><span class="sxs-lookup"><span data-stu-id="f1eee-105">If you use one or more of these shipping agents, you can set up certain basic information and use the automatic tracking feature from posted shipments, posted sales invoices, posted sales credit memos, and posted return receipts.</span></span> <span data-ttu-id="f1eee-106">Per ulteriori informazioni, vedere [Impostare gli spedizionieri](sales-how-to-set-up-shipping-agents.md).</span><span class="sxs-lookup"><span data-stu-id="f1eee-106">For more information, see [Set Up Shipping Agents](sales-how-to-set-up-shipping-agents.md).</span></span>  

<span data-ttu-id="f1eee-107">La seguente procedura mostra come tenere traccia di un collo da una spedizione di vendita registrata, ma gli stessi passaggi valgono per abilitare il tracciamento del collo dalle pagine Fattura vendita registrata, Nota credito vendita registrata e Carico da reso registrato.</span><span class="sxs-lookup"><span data-stu-id="f1eee-107">The following procedure shows how to track a package from a posted sales shipment, but the same steps apply to enable package tracking from the Posted Sales Invoice, Posted Sales Credit Memo, and Posted Return Receipt pages.</span></span>  

## <a name="to-track-a-package"></a><span data-ttu-id="f1eee-108">Per rintracciare un collo</span><span class="sxs-lookup"><span data-stu-id="f1eee-108">To track a package</span></span>

1. <span data-ttu-id="f1eee-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Spedizioni vendita registrate** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f1eee-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipment**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1eee-110">Aprire la spedizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="f1eee-110">Open the relevant shipment.</span></span>
3. <span data-ttu-id="f1eee-111">Scegliere l'azione **Aggiorna documento**.</span><span class="sxs-lookup"><span data-stu-id="f1eee-111">Choose the **Update Document** action.</span></span>
4. <span data-ttu-id="f1eee-112">Nel campo **Nr. identificazione collo**</span><span class="sxs-lookup"><span data-stu-id="f1eee-112">In the **Package Tracking No.**</span></span> <span data-ttu-id="f1eee-113">immettere il numero di collo che è stato comunicato dallo spedizioniere.</span><span class="sxs-lookup"><span data-stu-id="f1eee-113">field, enter the package number you have received from the shipping agent.</span></span> <span data-ttu-id="f1eee-114">Aggiornare **Spedizioniere** se necessario e chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="f1eee-114">Update **Shipping Agent** if needed and close the page.</span></span>
5. <span data-ttu-id="f1eee-115">Scegliere l'azione **Traccia collo**.</span><span class="sxs-lookup"><span data-stu-id="f1eee-115">Choose the **Track Package** action.</span></span>

<span data-ttu-id="f1eee-116">La pagina di tracciabilità dello spedizioniere viene aperta nel browser predefinito.</span><span class="sxs-lookup"><span data-stu-id="f1eee-116">Your default browser opens the shipping agent's tracking page.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1eee-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1eee-117">See Also</span></span>

[<span data-ttu-id="f1eee-118">Impostare gli spedizionieri</span><span class="sxs-lookup"><span data-stu-id="f1eee-118">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="f1eee-119">Vendite</span><span class="sxs-lookup"><span data-stu-id="f1eee-119">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f1eee-120">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="f1eee-120">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="f1eee-121">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="f1eee-121">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="f1eee-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1eee-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
