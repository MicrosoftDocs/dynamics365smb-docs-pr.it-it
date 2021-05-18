---
title: Aggiornamento di un'integrazione con Dynamics 365 Sales
description: Informazioni su come passare l'integrazione di Dynamics 365 Business Central con Dynamics 365 Sales alla versione più recente.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025810"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="08f43-103">Aggiornamento di un'integrazione con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="08f43-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="08f43-104">si integra con [!INCLUDE[prod_short](includes/cds_long_md.md)], che semplifica la connessione e la sincronizzazione dei dati con altre applicazioni di Dynamics 365, come [!INCLUDE[crm_md](includes/crm_md.md)] o anche le app che crei autonomamente.</span><span class="sxs-lookup"><span data-stu-id="08f43-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="08f43-105">Se stai effettuando l'integrazione per la prima volta, ti consigliamo di farlo tramite [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="08f43-106">Per ulteriori informazioni, vedi [Integrazione con Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="08f43-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="08f43-107">Se hai già integrato [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puoi continuare a sincronizzare i dati utilizzando la tua configurazione.</span><span class="sxs-lookup"><span data-stu-id="08f43-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="08f43-108">Tuttavia, se aggiorni [!INCLUDE[prod_short](includes/prod_short.md)] o disattivi la tua integrazione [!INCLUDE[crm_md](includes/crm_md.md)], per riattivarla devi connetterti tramite [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="08f43-109">La riconnessione tramite [!INCLUDE[prod_short](includes/cds_long_md.md)] applicherà le impostazioni di sincronizzazione predefinite e sovrascriverà tutte le configurazioni a tua disposizione.</span><span class="sxs-lookup"><span data-stu-id="08f43-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="08f43-110">Ad esempio, verranno applicati i mapping di tabella predefiniti.</span><span class="sxs-lookup"><span data-stu-id="08f43-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="08f43-111">Per aggiornare la connessione per utilizzare Dataverse</span><span class="sxs-lookup"><span data-stu-id="08f43-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="08f43-112">Apri la pagina **Setup connessione a Microsoft Dynamics 365** e disattiva l'interruttore **Abilitato** per eseguire la disconnessione di [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="08f43-113">Apri la pagina **Setup connessione a Dataverse** e scegli l'interruttore **Abilitato** per attivare la connessione a [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="08f43-114">Dopo aver abilitato la connessione, la soluzione di integrazione di Business Central viene distribuita a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="08f43-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="08f43-115">Scegli **Ridistribuzione soluzione di integrazione** per reinstallare la soluzione di integrazione di Business Central.</span><span class="sxs-lookup"><span data-stu-id="08f43-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="08f43-116">Nella pagina **Setup connessione a Microsoft Dynamics 365**, attiva l'interruttore **Abilitato** per eseguire di nuovo la connessione a [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="08f43-117">Dopo aver abilitato la connessione, la soluzione di integrazione di Business Central viene distribuita a [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="08f43-118">Ciò consente l'integrazione di tabelle specifiche in [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio ordini vendita, offerte e fatture.</span><span class="sxs-lookup"><span data-stu-id="08f43-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="08f43-119">Scegli **Ridistribuzione soluzione di integrazione** per reinstallare la soluzione di integrazione di Business Central.</span><span class="sxs-lookup"><span data-stu-id="08f43-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="08f43-120">Nella pagina **Impostazione della connessione di vendita**, scegli **Usa impostazione di sincronizzazione predefinita** per inizializzare i mapping della tabella di integrazione per [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08f43-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="08f43-121">L'uso dell'azione **Usa impostazione di sincronizzazione predefinita** applicherà le mappature della tabella di integrazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="08f43-121">Using the **Use Default Synchronization Setup** action will apply the default integration table mappings.</span></span> <span data-ttu-id="08f43-122">Tutte le mappature personalizzate verranno sovrascritte.</span><span class="sxs-lookup"><span data-stu-id="08f43-122">All custom mappings will be overwritten.</span></span> <span data-ttu-id="08f43-123">Se si dispone di mappature personalizzate che si desidera mantenere, è consigliabile esportarle in Excel o parlare con il proprio partner Microsoft di altri metodi per conservare le mappature personalizzate.</span><span class="sxs-lookup"><span data-stu-id="08f43-123">If you have custom mappings that you want to keep, we recommend that you export them to Excel or talk to your Microsoft partner about other ways to keep your custom mappings.</span></span>    

## <a name="see-also"></a><span data-ttu-id="08f43-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="08f43-124">See Also</span></span>
[<span data-ttu-id="08f43-125">Integrazione con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="08f43-125">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="08f43-126">Integrazione con Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="08f43-126">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]