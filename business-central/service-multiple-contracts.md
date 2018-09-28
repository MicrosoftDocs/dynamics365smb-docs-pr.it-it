---
title: Contratti multipli | Documenti Microsoft
description: "A seconda degli accordi a livello di assistenza stipulati con un cliente, può essere necessario utilizzare più di un contratto di assistenza per gestire un articolo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 58e92211695ea3a8d8c4137c699794f935c1bc69
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="multiple-contracts"></a><span data-ttu-id="138f4-103">Contratti multipli</span><span class="sxs-lookup"><span data-stu-id="138f4-103">Multiple Contracts</span></span>
<span data-ttu-id="138f4-104">A seconda degli accordi a livello di assistenza stipulati con un cliente, può essere necessario utilizzare più di un contratto di assistenza per gestire un articolo.</span><span class="sxs-lookup"><span data-stu-id="138f4-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="138f4-105">Tramite la gestione di un articolo in assistenza in più contratti, è possibile effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="138f4-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="138f4-106">Emettere contratti diversi per lo stesso articolo in assistenza.</span><span class="sxs-lookup"><span data-stu-id="138f4-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="138f4-107">Fornire l'assistenza necessaria per le varie parti separatamente.</span><span class="sxs-lookup"><span data-stu-id="138f4-107">Service parts separately.</span></span>  
* <span data-ttu-id="138f4-108">Prendere in considerazione competenze diverse per fornire assistenza per aspetti differenti di un articolo in assistenza, ad esempio i componenti meccanici e il software.</span><span class="sxs-lookup"><span data-stu-id="138f4-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="138f4-109">Specificare tempi di risposta e frequenze differenti per l'assistenza a parti differenti di un articolo.</span><span class="sxs-lookup"><span data-stu-id="138f4-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="138f4-110">Determinare tipi di attività diversi da eseguire su un articolo in assistenza quando l'articolo richiede tipi di intervento differenti in periodi di tempo diversi.</span><span class="sxs-lookup"><span data-stu-id="138f4-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="138f4-111">Selezionare e assegnare un numero di contratto appropriato a una riga di articolo in assistenza quando si crea un ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="138f4-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="138f4-112">Gestire informazioni finanziarie di interesse sugli articoli in assistenza e sugli accordi a livello di assistenza.</span><span class="sxs-lookup"><span data-stu-id="138f4-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="138f4-113">Si prendano in considerazione i seguenti esempi di utilizzo di contratti multipli.</span><span class="sxs-lookup"><span data-stu-id="138f4-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="138f4-114">Creazione di contratti multipli per un articolo in assistenza</span><span class="sxs-lookup"><span data-stu-id="138f4-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="138f4-115">È possibile creare manualmente un contratto o un'offerta di contratto di assistenza per articoli in assistenza già registrati in contratti non annullati relativi allo stesso cliente.</span><span class="sxs-lookup"><span data-stu-id="138f4-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="138f4-116">A tale scopo, seguire la procedura standard di creazione per i contratti e le offerte di contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="138f4-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="138f4-117">Per ulteriori informazioni, vedere [Utilizzare contratti e offerte di contratto di assistenza](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="138f4-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="138f4-118">Quando in una riga di contratto si aggiunge un articolo in assistenza registrato in altri contratti di assistenza o altre offerte di contratto, viene visualizzato un messaggio di avviso che comunica che l'articolo in assistenza appartiene già a uno o più contratti di assistenza o a una o più offerte di contratto.</span><span class="sxs-lookup"><span data-stu-id="138f4-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="138f4-119">Se si risponde affermativamente a questo messaggio, le informazioni di interesse relative all'articolo in assistenza verranno copiate in una nuova riga di contratto.</span><span class="sxs-lookup"><span data-stu-id="138f4-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="138f4-120">Copia di documenti</span><span class="sxs-lookup"><span data-stu-id="138f4-120">Copying Documents</span></span>  
<span data-ttu-id="138f4-121">È possibile creare automaticamente un contratto di assistenza o un'offerta di contratto per gli articoli in assistenza già registrati in altri contratti di assistenza o altre offerte di contratto tramite la funzione **Copia documento**.</span><span class="sxs-lookup"><span data-stu-id="138f4-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="138f4-122">Creazione di ordini di assistenza per contratti multipli</span><span class="sxs-lookup"><span data-stu-id="138f4-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="138f4-123">È possibile creare manualmente un ordine di assistenza per un articolo in assistenza registrato in più contratti attivi.</span><span class="sxs-lookup"><span data-stu-id="138f4-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="138f4-124">Un contratto di assistenza è attivo quando è firmato e non è scaduto.</span><span class="sxs-lookup"><span data-stu-id="138f4-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="138f4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="138f4-125">See Also</span></span>  
[<span data-ttu-id="138f4-126">Adempimento dei contratti di assistenza</span><span class="sxs-lookup"><span data-stu-id="138f4-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="138f4-127">Creare ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="138f4-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  

