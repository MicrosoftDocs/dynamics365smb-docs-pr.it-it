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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "940245"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="dfd99-103">Visualizzare lo stato di una sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="dfd99-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="dfd99-104">È possibile visualizzare lo stato dei singoli processi di sincronizzazione che sono stati eseguiti per l'integrazione di [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dfd99-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="dfd99-105">Ciò include i processi di sincronizzazione che sono stati eseguiti dai processi di sincronizzazione manuale e della coda processi sui record del client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dfd99-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="dfd99-106">Ciò risulta utile per risolvere problemi di sincronizzazione perché consente di accedere ai dettagli degli errori specifici.</span><span class="sxs-lookup"><span data-stu-id="dfd99-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="dfd99-107">Per visualizzare tutti i problemi di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="dfd99-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="dfd99-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Errori di sincronizzazione dati associati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="dfd99-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfd99-109">Nella pagina **Errori di sincronizzazione dati associati** è possibile visualizzare tutti i problemi verificatesi nella sincronizzazione dei dati tra [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrare e ordinare i record nella pagina per tabella e messaggio di errore e intraprendere azioni come **Riprova** o **Rimuovi associazione** per risolvere problemi singolarmente o in blocco.</span><span class="sxs-lookup"><span data-stu-id="dfd99-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="dfd99-110">Per visualizzare il registro di sincronizzazione per specifici record (sincronizzati manualmente)</span><span class="sxs-lookup"><span data-stu-id="dfd99-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="dfd99-111">Aprire, ad esempio, il cliente, l'articolo o qualunque altro record che esegue la sincronizzazione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Sales</span><span class="sxs-lookup"><span data-stu-id="dfd99-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="dfd99-112">Scegliere l'azione **Registro sincronizzazione** per visualizzare il registro di sincronizzazione per il record selezionato, ad esempio, lo specifico cliente che è stato sincronizzato manualmente</span><span class="sxs-lookup"><span data-stu-id="dfd99-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="dfd99-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dfd99-113">See Also</span></span>  
[<span data-ttu-id="dfd99-114">Configurare l'integrazione di Dynamics 365 for Sales in Business Central</span><span class="sxs-lookup"><span data-stu-id="dfd99-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="dfd99-115">Utilizzo di Dynamics 365 for Sales da Business Central</span><span class="sxs-lookup"><span data-stu-id="dfd99-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
