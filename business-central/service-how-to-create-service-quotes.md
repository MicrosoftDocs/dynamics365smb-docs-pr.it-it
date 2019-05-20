---
title: Creare offerte di assistenza | Documenti Microsoft
description: La pagina **Offerte assistenza** consente di creare documenti in cui vengono immesse informazioni relative a un servizio di assistenza, ad esempio riparazione e manutenzione, svolto su articoli in assistenza su richiesta del cliente. Un'offerta di assistenza può essere utilizzata come bozza preliminare di un ordine di assistenza e può essere in seguito convertita in un ordine.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 44ffab92930237c5496860771f41b4951b15b0ff
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250666"
---
# <a name="create-service-quotes"></a><span data-ttu-id="36440-104">Creare offerte di assistenza</span><span class="sxs-lookup"><span data-stu-id="36440-104">Create Service Quotes</span></span>
<span data-ttu-id="36440-105">Le offerte di assistenza possono essere considerate come ordini di assistenza di base.</span><span class="sxs-lookup"><span data-stu-id="36440-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="36440-106">In effetti, sono quasi identici.</span><span class="sxs-lookup"><span data-stu-id="36440-106">In fact, they are almost identical.</span></span> <span data-ttu-id="36440-107">Entrambi includono informazioni come l'identità del cliente, il tipo di ordine, l'articolo che necessita di assistenza, nonché informazioni di fatturazione, spedizione e relative al lavoro di assistenza effettivo.</span><span class="sxs-lookup"><span data-stu-id="36440-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="36440-108">Un'offerta di assistenza può essere utilizzata come bozza preliminare di un ordine di assistenza e può essere in seguito convertita in un ordine.</span><span class="sxs-lookup"><span data-stu-id="36440-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="36440-109">Per creare un'offerta di assistenza</span><span class="sxs-lookup"><span data-stu-id="36440-109">To create a service quote</span></span>  
1. <span data-ttu-id="36440-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Offerte assistenza** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="36440-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="36440-111">Creare una nuova offerta di assistenza.</span><span class="sxs-lookup"><span data-stu-id="36440-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="36440-112">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="36440-112">In the **No.**</span></span> <span data-ttu-id="36440-113">immettere un numero per l'offerta di assistenza.</span><span class="sxs-lookup"><span data-stu-id="36440-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="36440-114">In alternativa, se è stata impostata una numerazione per le offerte di assistenza nella pagina **Setup gest. assist.**, per selezionare il successivo numero di offerta di assistenza disponibile, premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="36440-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="36440-115">Nel campo **Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="36440-115">In the **Customer No.**</span></span>  <span data-ttu-id="36440-116">selezionare il cliente appropriato dalla lista.</span><span class="sxs-lookup"><span data-stu-id="36440-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="36440-117">I campi del cliente vengono compilati automaticamente con le informazioni della scheda **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="36440-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="36440-118">Se una scheda **Cliente** non esiste per il cliente in questione ed è stato impostato un modello cliente, è possibile creare il cliente a partire dall'offerta di assistenza.</span><span class="sxs-lookup"><span data-stu-id="36440-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="36440-119">Compilare i campi appropriati e scegliere l'azione **Crea cliente**.</span><span class="sxs-lookup"><span data-stu-id="36440-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="36440-120">In base alle impostazioni nella Scheda dettaglio **Campi obbligatori** della pagina **Setup gest. assist.** potrebbe essere necessario compilare il campo **Tipo ordine assistenza** e il campo **Cod. agente**.</span><span class="sxs-lookup"><span data-stu-id="36440-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="36440-121">Compilare le righe di articolo in assistenza.</span><span class="sxs-lookup"><span data-stu-id="36440-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="36440-122">Registrare i costi previsti nelle righe di assistenza.</span><span class="sxs-lookup"><span data-stu-id="36440-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36440-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36440-123">See Also</span></span>  
[<span data-ttu-id="36440-124">Creare ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="36440-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="36440-125">Utilizzare i compiti di assistenza</span><span class="sxs-lookup"><span data-stu-id="36440-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 