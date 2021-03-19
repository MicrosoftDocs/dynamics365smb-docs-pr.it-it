---
title: Migrare i dati da Dynamics GP prima della 15.3 | Microsoft Docs
description: Prima dell'aggiornamento 15.3 è possibile utilizzare l'estensione per la migrazione dei dati di Dynamics GP per migrare i dati relativi a clienti, fornitori, articoli di magazzino, conti C/G, transazioni aperte di contabilità fornitori e clienti di e conti da Dynamics GP a Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: 986612a04ea75e89c2ef7cc983af4ae507738871
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377300"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="55c41-103">Estensione di migrazione dei dati Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="55c41-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="55c41-104">Questa estensione è deprecata nell'aggiornamento 15.3.</span><span class="sxs-lookup"><span data-stu-id="55c41-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="55c41-105">Si consiglia agli utenti che desiderano migrare da Dynamics GP di iniziare utilizzando la procedura **Migrazione cloud**.</span><span class="sxs-lookup"><span data-stu-id="55c41-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="55c41-106">L'estensione **Migrazione cloud** ha funzionalità più efficaci e porta più dati in Business Central da Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="55c41-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="55c41-107">Per ulteriori informazioni, vedere [Migrare a Business Central Online da Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) nel contenuto amministrativo per [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="55c41-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="55c41-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="55c41-108">See Also</span></span>

[<span data-ttu-id="55c41-109">Estensioni cloud intelligente per la migrazione al cloud</span><span class="sxs-lookup"><span data-stu-id="55c41-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="55c41-110">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="55c41-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="55c41-111">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="55c41-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="55c41-112">Migrare a Business Central Online da Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="55c41-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  


[!INCLUDE[footer-include](includes/footer-banner.md)]