---
title: Associare e sincronizzare i record manualmente | Microsoft Docs
description: La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record in una tabella in Business Central e nell'entità Dynamics 365 Sales che sono associati.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308118"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="481cc-103">Associare e sincronizzare i record manualmente</span><span class="sxs-lookup"><span data-stu-id="481cc-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="481cc-104">In questo argomento viene descritto come associare uno o più record in [!INCLUDE[d365fin](includes/d365fin_md.md)] a record in [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="481cc-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="481cc-105">L'associazione di record consente di visualizzare le infomazioni di [!INCLUDE[crm_md](includes/crm_md.md)] da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa.</span><span class="sxs-lookup"><span data-stu-id="481cc-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="481cc-106">L'associazione consente inoltre di sincronizzare dati tra i record.</span><span class="sxs-lookup"><span data-stu-id="481cc-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="481cc-107">È possibile associare i record esistenti, oppure creare e associare nuovi record.</span><span class="sxs-lookup"><span data-stu-id="481cc-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="481cc-108">L'associazione e la sincronizzazione con [!INCLUDE[crm_md](includes/crm_md.md)] sono disponibili solo se l'amministratore di sistema ha creato una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="481cc-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="481cc-109">Un modo rapido di verificare è di aprire la scheda **Cliente** e di cercare l'azione **Imposta associazione**.</span><span class="sxs-lookup"><span data-stu-id="481cc-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="481cc-110">Se l'azione è disponibile, le app sono collegate.</span><span class="sxs-lookup"><span data-stu-id="481cc-110">If the action is available, the apps are connected.</span></span>   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="481cc-111">Per associare un record</span><span class="sxs-lookup"><span data-stu-id="481cc-111">To couple a record</span></span>  
1.  <span data-ttu-id="481cc-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare.</span><span class="sxs-lookup"><span data-stu-id="481cc-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="481cc-113">Ad esempio, la scheda Cliente o Contatto.</span><span class="sxs-lookup"><span data-stu-id="481cc-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="481cc-114">È inoltre possibile aprire la pagina elenco e selezionare il record che si desidera associare.</span><span class="sxs-lookup"><span data-stu-id="481cc-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="481cc-115">Scegliere l'azione **Imposta associazione**.</span><span class="sxs-lookup"><span data-stu-id="481cc-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="481cc-116">Compilare i campi e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="481cc-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="481cc-117">Per sincronizzare un singolo record</span><span class="sxs-lookup"><span data-stu-id="481cc-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="481cc-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare.</span><span class="sxs-lookup"><span data-stu-id="481cc-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="481cc-119">Ad esempio, la scheda Cliente o Contatto.</span><span class="sxs-lookup"><span data-stu-id="481cc-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="481cc-120">Scegliere l'azione **Sincronizza adesso**.</span><span class="sxs-lookup"><span data-stu-id="481cc-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="481cc-121">Se un record può essere sincronizzato da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="481cc-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="481cc-122">Per sincronizzare più record</span><span class="sxs-lookup"><span data-stu-id="481cc-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="481cc-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la pagina elenco per il record, ad esempio le pagine elenco Clienti o Contatti.</span><span class="sxs-lookup"><span data-stu-id="481cc-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="481cc-124">Selezionare i record che si intende sincronizzare, quindi scegliere **Sincronizza adesso**.</span><span class="sxs-lookup"><span data-stu-id="481cc-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="481cc-125">Se i record possono essere sincronizzati da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="481cc-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="481cc-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="481cc-126">See Also</span></span>  
[<span data-ttu-id="481cc-127">Utilizzo di Dynamics 365 Sales da Business Central</span><span class="sxs-lookup"><span data-stu-id="481cc-127">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
