---
title: Estensioni per la migrazione al cloud
description: Utilizzare le estensioni di migrazione cloud per migrare i dati locali in Business Central online. Queste estensioni spostano i dati locali nel cloud in modo da poter utilizzare Business Central online con i dati esistenti.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f02face497affd1fd1467c118e10e69f2be39b85
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889126"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a><span data-ttu-id="9d8f1-104">Estensioni per la migrazione al cloud per la migrazione a Business Central Online</span><span class="sxs-lookup"><span data-stu-id="9d8f1-104">Cloud Migration Extensions for Migrating to Business Central Online</span></span>

<span data-ttu-id="9d8f1-105">A seconda della soluzione locale, è necessario utilizzare estensioni diverse per connettere i dati con [!INCLUDE[prod_short](includes/prod_short.md)] online allo scopo di migrare la soluzione nel cloud.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="9d8f1-106">Se si utilizza uno dei prodotti locali supportati, è possibile configurare un ambiente cloud basato sull'estensione di uno specifico prodotto.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="9d8f1-107">Una volta configurato l'ambiente cloud, sarà possibile migrare i dati dalla soluzione locale a [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9d8f1-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9d8f1-108">Ciò consente di sfruttare appieno i vantaggi del cloud per l'azienda, come approfondimenti migliorati sul business, intelligenza artificiale, accesso a più dispositivi, sempre e ovunque.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="9d8f1-109">Per ulteriori informazioni, vedere [Migrazione dei dati locali in Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) nel contenuto amministrativo per [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9d8f1-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="9d8f1-110">Business Central in locale</span><span class="sxs-lookup"><span data-stu-id="9d8f1-110">Business Central on-premises</span></span>

<span data-ttu-id="9d8f1-111">Se si utilizza una distribuzione locale di [!INCLUDE[prod_short](includes/prod_short.md)], acquisire l'estensione **Cloud intelligente base** e l'estensione **Cloud intelligente Business Central** e quindi eseguire la guida al setup assistito **Setup di migrazione cloud**.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="9d8f1-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="9d8f1-112">Dynamics GP</span></span>

<span data-ttu-id="9d8f1-113">Se si utilizza Dynamics GP, acquisire le estensioni **Estensione Cloud intelligente base** e **Cloud intelligente Dynamics GP**, quindi eseguire la guida al setup assistito **Setup di migrazione cloud**.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9d8f1-114">La migrazione da Dynamics GP utilizzando la guida al setup assistito **Setup migrazione cloud** è attualmente supportata solo per i seguenti mercati: Stati Uniti, Canada, Regno Unito.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="9d8f1-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="9d8f1-115">Dynamics SL</span></span>

<span data-ttu-id="9d8f1-116">Se si utilizza Dynamics SL, acquisire le estensioni **Estensione Cloud intelligente base**, **Cloud intelligente Microsoft Dynamics SL** e **SmartList di cronologia Microsoft Dynamics SL**, quindi eseguire la guida al setup assistito **Setup di migrazione cloud**.</span><span class="sxs-lookup"><span data-stu-id="9d8f1-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d8f1-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9d8f1-117">See Also</span></span>

[<span data-ttu-id="9d8f1-118">Estensione migrazione Cloud base</span><span class="sxs-lookup"><span data-stu-id="9d8f1-118">Cloud Migration Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
[<span data-ttu-id="9d8f1-119">Migrazione dei dati locali in Business Central Online</span><span class="sxs-lookup"><span data-stu-id="9d8f1-119">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]