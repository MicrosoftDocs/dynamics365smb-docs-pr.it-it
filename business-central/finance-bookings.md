---
title: Fatturazione delle prenotazioni in Business Central | Documenti Microsoft
description: "Informazioni su come è possibile eseguire la fatturazione da Microsoft Bookings in Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8637df3f579af920168f059812b34ae5d0023afc
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="76867-103">Fatturazione in blocco per Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="76867-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="76867-104">Se la società utilizza l'app Bookings in Office 365, è possibile eseguire la fatturazione in blocco per gli appuntamenti.</span><span class="sxs-lookup"><span data-stu-id="76867-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="76867-105">La finestra **Bookings non fatturato** di [!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce un elenco delle prenotazioni completate della società.</span><span class="sxs-lookup"><span data-stu-id="76867-105">The **Uninvoiced Bookings** window in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="76867-106">Nella pagina è possibile selezionare rapidamente gli appuntamenti da fatturare e creare fatture in bozza per i servizi forniti.</span><span class="sxs-lookup"><span data-stu-id="76867-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="76867-107">Connessione a Bookings</span><span class="sxs-lookup"><span data-stu-id="76867-107">Connect to Bookings</span></span>
<span data-ttu-id="76867-108">Per collegare [!INCLUDE[d365fin](includes/d365fin_md.md)] a Bookings, è necessario specificare la società Bookings, cosa sincronizzazione con Bookings, la frequenza di sincronizzare e i modelli da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="76867-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="76867-109">Impostare queste informazioni nella finestra **Setup sincronizzazione registrazione** che è possibile aprire dalla finestra **Setup sincronizzazione con Exchange** che è possibile trovare tramite la [Ricerca](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="76867-109">You set up this information in the **Booking Sync. Setup** window, which you can launch from the **Exchange Sync. Setup** window, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="76867-110">Ad esempio, se si desidera sincronizzare i clienti tra Bookings e [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario specificare il modello di default da utilizzare per aggiungere i nuovi clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)] sulla base dei clienti nella società Bookings.</span><span class="sxs-lookup"><span data-stu-id="76867-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="76867-111">Fattura appuntamenti</span><span class="sxs-lookup"><span data-stu-id="76867-111">Invoice Appointments</span></span>
<span data-ttu-id="76867-112">Quando è tempo di inviare le fatture per le prenotazioni completate, aprire la finestra **Bookings non fatturato**.</span><span class="sxs-lookup"><span data-stu-id="76867-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** window.</span></span> <span data-ttu-id="76867-113">In base alla frequenza della sincronizzazione delle informazioni, l'elenco è lungo o breve.</span><span class="sxs-lookup"><span data-stu-id="76867-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="76867-114">È possibile creare fatture per tutte le prenotazioni della lista o per una prenotazione alla volta.</span><span class="sxs-lookup"><span data-stu-id="76867-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="76867-115">È possibile selezionare uno o più movimenti dell'elenco e fatturare solo quelli.</span><span class="sxs-lookup"><span data-stu-id="76867-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="76867-116">Il supporto per la fatturazione degli appuntamenti da Bookings è più semplice del flusso di lavoro completo per l'utilizzo di offerte di vendita, ordini di vendita e fatture di vendita.</span><span class="sxs-lookup"><span data-stu-id="76867-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="76867-117">Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="76867-117">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="76867-118">È possibile scegliere di vendere i servizi con [!INCLUDE[d365fin](includes/d365fin_md.md)] o decidere di utilizzare Bookings, in base alle esigenze aziendali.</span><span class="sxs-lookup"><span data-stu-id="76867-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="76867-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76867-119">See Also</span></span>
[<span data-ttu-id="76867-120">Finanze</span><span class="sxs-lookup"><span data-stu-id="76867-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="76867-121">Fatturare le vendite</span><span class="sxs-lookup"><span data-stu-id="76867-121">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="76867-122">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="76867-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="76867-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="76867-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

