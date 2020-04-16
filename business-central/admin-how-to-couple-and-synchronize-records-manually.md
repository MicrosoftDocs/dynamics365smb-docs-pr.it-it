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
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196665"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="63149-103">Associare e sincronizzare i record manualmente</span><span class="sxs-lookup"><span data-stu-id="63149-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="63149-104">In questo argomento viene descritto come associare uno o più record in [!INCLUDE[d365fin](includes/d365fin_md.md)] a record in Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="63149-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="63149-105">L'associazione di record consente di visualizzare le infomazioni di Common Data Service da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa.</span><span class="sxs-lookup"><span data-stu-id="63149-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="63149-106">L'associazione consente inoltre di sincronizzare dati tra i record.</span><span class="sxs-lookup"><span data-stu-id="63149-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="63149-107">È possibile associare i record esistenti, oppure creare e associare nuovi record.</span><span class="sxs-lookup"><span data-stu-id="63149-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="63149-108">L'associazione e la sincronizzazione dei dati è disponibile solo se l'amministratore di sistema ha creato una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="63149-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="63149-109">Un modo rapido di verificare è di aprire la scheda **Cliente** e di cercare l'azione **Imposta associazione**.</span><span class="sxs-lookup"><span data-stu-id="63149-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="63149-110">Se l'azione è disponibile, le app sono collegate.</span><span class="sxs-lookup"><span data-stu-id="63149-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="63149-111">Esempio di video</span><span class="sxs-lookup"><span data-stu-id="63149-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="63149-112">Per associare un record</span><span class="sxs-lookup"><span data-stu-id="63149-112">To couple a record</span></span>  
1.  <span data-ttu-id="63149-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare.</span><span class="sxs-lookup"><span data-stu-id="63149-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="63149-114">Ad esempio, la scheda Cliente o Contatto.</span><span class="sxs-lookup"><span data-stu-id="63149-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="63149-115">È inoltre possibile aprire la pagina elenco e selezionare il record che si desidera associare.</span><span class="sxs-lookup"><span data-stu-id="63149-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="63149-116">Scegliere l'azione **Imposta associazione**.</span><span class="sxs-lookup"><span data-stu-id="63149-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="63149-117">Compilare i campi e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="63149-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="63149-118">Per sincronizzare un singolo record</span><span class="sxs-lookup"><span data-stu-id="63149-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="63149-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare.</span><span class="sxs-lookup"><span data-stu-id="63149-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="63149-120">Ad esempio, la scheda Cliente o Contatto.</span><span class="sxs-lookup"><span data-stu-id="63149-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="63149-121">Scegliere l'azione **Sincronizza adesso**.</span><span class="sxs-lookup"><span data-stu-id="63149-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="63149-122">Se un record può essere sincronizzato in una direzione, selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="63149-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="63149-123">Per sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="63149-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="63149-124">In [!INCLUDE[crm_md](includes/crm_md.md)], aprire il modulo del record da associare.</span><span class="sxs-lookup"><span data-stu-id="63149-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="63149-125">Ad esempio, la scheda Account o il modulo scheda Contatto.</span><span class="sxs-lookup"><span data-stu-id="63149-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="63149-126">Scegli l'azione **[!INCLUDE[d365fin](includes/d365fin_md.md)]** nella barra multifunzione per aprire e associare automaticamente il record.</span><span class="sxs-lookup"><span data-stu-id="63149-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="63149-127">È possibile sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)] automaticamente solo quando **Sinc. solo record associati** è disabilitata e la direzione di sincronizzazione è impostata su Bidirezionale o Da tabella di integrazione nella pagina **Integration Table Mapping** per il record.</span><span class="sxs-lookup"><span data-stu-id="63149-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="63149-128">Per ulteriori informazioni, vedere [Mappatura delle tabelle e dei campi da sincronizzare](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="63149-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="63149-129">Per sincronizzare più record</span><span class="sxs-lookup"><span data-stu-id="63149-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="63149-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la pagina elenco per il record, ad esempio le pagine elenco Clienti o Contatti.</span><span class="sxs-lookup"><span data-stu-id="63149-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="63149-131">Selezionare i record che si intende sincronizzare, quindi scegliere **Sincronizza adesso**.</span><span class="sxs-lookup"><span data-stu-id="63149-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="63149-132">Se i record possono essere sincronizzati in una direzione, selezionare l'opzione che specifica la direzione e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="63149-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="63149-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="63149-133">See Also</span></span>  
[<span data-ttu-id="63149-134">Utilizzo di Dynamics 365 Sales da Business Central</span><span class="sxs-lookup"><span data-stu-id="63149-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
