---
title: Aggiornamento di un'integrazione con Dynamics 365 Sales
description: Informazioni su come passare l'integrazione di Dynamics 365 Business Central con Dynamics 365 Sales alla versione più recente.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6528a05d0d2b43d39f0f2fafa26d71b03d0d2511
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013719"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="a081d-103">Aggiornamento di un'integrazione con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a081d-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a081d-104">si integra con [!INCLUDE[prod_short](includes/cds_long_md.md)], che semplifica la connessione e la sincronizzazione dei dati con altre applicazioni di Dynamics 365, come [!INCLUDE[crm_md](includes/crm_md.md)] o anche le app che crei autonomamente.</span><span class="sxs-lookup"><span data-stu-id="a081d-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="a081d-105">Se stai effettuando l'integrazione per la prima volta, ti consigliamo di farlo tramite [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a081d-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="a081d-106">Per ulteriori informazioni, vedi [Integrazione con Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="a081d-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="a081d-107">Se hai già integrato [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puoi continuare a sincronizzare i dati utilizzando la tua configurazione.</span><span class="sxs-lookup"><span data-stu-id="a081d-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="a081d-108">Tuttavia, se aggiorni [!INCLUDE[prod_short](includes/prod_short.md)] o disattivi la tua integrazione [!INCLUDE[crm_md](includes/crm_md.md)], per riattivarla devi connetterti tramite [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a081d-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="a081d-109">La riconnessione tramite [!INCLUDE[prod_short](includes/cds_long_md.md)] applicherà le impostazioni di sincronizzazione predefinite e sovrascriverà tutte le configurazioni a tua disposizione.</span><span class="sxs-lookup"><span data-stu-id="a081d-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="a081d-110">Ad esempio, verranno applicati i mapping di tabella predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a081d-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="a081d-111">Per aggiornare la connessione per utilizzare Dataverse</span><span class="sxs-lookup"><span data-stu-id="a081d-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="a081d-112">Apri la pagina **Setup connessione a Microsoft Dynamics 365** e disattiva l'interruttore **Abilitato** per eseguire la disconnessione di [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a081d-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="a081d-113">Apri la pagina **Setup connessione a Dataverse** e scegli l'interruttore **Abilitato** per attivare la connessione a [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a081d-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   <span data-ttu-id="a081d-114">Dopo aver abilitato la connessione, la soluzione di integrazione di Business Central viene distribuita a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a081d-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="a081d-115">Scegli **Ridistribuzione soluzione di integrazione** per reinstallare la soluzione di integrazione di Business Central.</span><span class="sxs-lookup"><span data-stu-id="a081d-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="a081d-116">Nella pagina **Setup connessione a Microsoft Dynamics 365**, attiva l'interruttore **Abilitato** per eseguire di nuovo la connessione a [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a081d-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="a081d-117">Ciò consente l'integrazione di tabelle specifiche in [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio ordini vendita, offerte e fatture.</span><span class="sxs-lookup"><span data-stu-id="a081d-117">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="a081d-118">Nella pagina **Impostazione della connessione di vendita**, scegli **Usa impostazione di sincronizzazione predefinita** per inizializzare i mapping della tabella di integrazione per [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a081d-118">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="a081d-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a081d-119">See Also</span></span>
[<span data-ttu-id="a081d-120">Integrazione con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a081d-120">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="a081d-121">Integrazione con Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="a081d-121">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)
