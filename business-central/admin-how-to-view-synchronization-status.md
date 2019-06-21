---
title: Visualizzare lo stato di una sincronizzazione | Microsoft Docs
description: Ottenere informazioni su come visualizzare lo stato di un singolo processo di sincronizzazione.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620886"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="1b3ae-103">Visualizzare lo stato di una sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="1b3ae-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="1b3ae-104">È possibile visualizzare lo stato dei singoli processi di sincronizzazione che sono stati eseguiti per l'integrazione di [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1b3ae-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="1b3ae-105">Ciò include i processi di sincronizzazione che sono stati eseguiti dai processi di sincronizzazione manuale e della coda processi sui record del client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1b3ae-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1b3ae-106">Ciò risulta utile per risolvere problemi di sincronizzazione perché consente di accedere ai dettagli degli errori specifici.</span><span class="sxs-lookup"><span data-stu-id="1b3ae-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="1b3ae-107">Per visualizzare problemi di sincronizzazione relativi a record associati</span><span class="sxs-lookup"><span data-stu-id="1b3ae-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="1b3ae-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Errori di sincronizzazione dati associati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1b3ae-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b3ae-109">Nella pagina **Errori di sincronizzazione dati associati** vengono visualizzati i problemi verificatisi durante la sincronizzazione di record associati.</span><span class="sxs-lookup"><span data-stu-id="1b3ae-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="1b3ae-110">È possibile filtrare e ordinare record ed eseguire azioni come **Ripristina** o **Elimina record** per risolvere i problemi singolarmente.</span><span class="sxs-lookup"><span data-stu-id="1b3ae-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="1b3ae-111">Per visualizzare il registro di sincronizzazione per specifici record (sincronizzati manualmente)</span><span class="sxs-lookup"><span data-stu-id="1b3ae-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="1b3ae-112">Aprire, ad esempio, un cliente, un articolo o qualunque altro record che esegue la sincronizzazione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Sales</span><span class="sxs-lookup"><span data-stu-id="1b3ae-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="1b3ae-113">Scegliere l'azione **Registro sincronizzazione** per visualizzare il registro di sincronizzazione per un record selezionato.</span><span class="sxs-lookup"><span data-stu-id="1b3ae-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="1b3ae-114">Ad esempio, un cliente specifico sincronizzato manualmente.</span><span class="sxs-lookup"><span data-stu-id="1b3ae-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b3ae-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1b3ae-115">See Also</span></span>  
[<span data-ttu-id="1b3ae-116">Configurare l'integrazione di Dynamics 365 for Sales in Business Central</span><span class="sxs-lookup"><span data-stu-id="1b3ae-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="1b3ae-117">Utilizzo di Dynamics 365 for Sales da Business Central</span><span class="sxs-lookup"><span data-stu-id="1b3ae-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
