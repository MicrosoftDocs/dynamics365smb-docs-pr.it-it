---
title: Creare offerte di assistenza | Documenti Microsoft
description: "La finestra **Offerte assistenza** consente di creare documenti in cui vengono immesse informazioni relative a un servizio di assistenza, ad esempio riparazione e manutenzione, svolto su articoli in assistenza su richiesta del cliente. Un'offerta di assistenza può essere utilizzata come bozza preliminare di un ordine di assistenza e può essere in seguito convertita in un ordine."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9d4f8d21d0c79adbac238b2d26accc4c08656c77
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="create-service-quotes"></a><span data-ttu-id="2e0f8-104">Creare offerte di assistenza</span><span class="sxs-lookup"><span data-stu-id="2e0f8-104">Create Service Quotes</span></span>
<span data-ttu-id="2e0f8-105">Le offerte di assistenza possono essere considerate come ordini di assistenza di base.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="2e0f8-106">In effetti, sono quasi identici.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-106">In fact, they are almost identical.</span></span> <span data-ttu-id="2e0f8-107">Entrambi includono informazioni come l'identità del cliente, il tipo di ordine, l'articolo che necessita di assistenza, nonché informazioni di fatturazione, spedizione e relative al lavoro di assistenza effettivo.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="2e0f8-108">Un'offerta di assistenza può essere utilizzata come bozza preliminare di un ordine di assistenza e convertita in un ordine in seguito.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="2e0f8-109">Per creare un'offerta di assistenza</span><span class="sxs-lookup"><span data-stu-id="2e0f8-109">To create a service quote</span></span>  
1. <span data-ttu-id="2e0f8-110">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Offerte assistenza**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2e0f8-111">Creare una nuova offerta di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="2e0f8-112">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="2e0f8-112">In the **No.**</span></span> <span data-ttu-id="2e0f8-113">immettere un numero per l'offerta di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="2e0f8-114">In alternativa, se è stata impostata una numerazione per le offerte di assistenza nella finestra **Setup gest. assist.**, per selezionare il successivo numero di offerta di assistenza disponibile, premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="2e0f8-115">Nel campo **Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="2e0f8-115">In the **Customer No.**</span></span>  <span data-ttu-id="2e0f8-116">selezionare il cliente appropriato dalla lista.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="2e0f8-117">I campi del cliente vengono compilati automaticamente con le informazioni della scheda **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="2e0f8-118">Se una scheda **Cliente** non esiste per il cliente in questione ed è stato impostato un modello cliente, è possibile creare il cliente a partire dall'offerta di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="2e0f8-119">Compilare i campi appropriati e scegliere l'azione **Crea cliente**.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="2e0f8-120">In base alle impostazioni nella Scheda dettaglio **Campi obbligatori** della finestra **Setup gest. assist.** potrebbe essere necessario compilare il campo **Tipo ordine assistenza** e il campo **Cod. agente**.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="2e0f8-121">Compilare le righe di articolo in assistenza.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="2e0f8-122">Registrare i costi previsti nelle righe di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2e0f8-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e0f8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e0f8-123">See Also</span></span>  
[<span data-ttu-id="2e0f8-124">Creare ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="2e0f8-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="2e0f8-125">Utilizzare i compiti di assistenza</span><span class="sxs-lookup"><span data-stu-id="2e0f8-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
