---
title: Gestire gli intenti di accesso al database in Business Central | Microsoft Docs
description: Modifica l'intento di accesso al database per report, pagine API e query.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 502add82d2f70f6ffd13ae04f7eb6d214105fb63
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378600"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="54c79-103">Gestione dell'intento di accesso al database</span><span class="sxs-lookup"><span data-stu-id="54c79-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="54c79-104">In qualità di utente con privilegi avanzati o amministratore, puoi modificare l'intento di accesso al database su report, pagine di tipo API e query per migliorare le prestazioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="54c79-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="54c79-105">Sintesi</span><span class="sxs-lookup"><span data-stu-id="54c79-105">Overview</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="54c79-106">può essere configurata per utilizzare repliche di sola lettura del database primario (lettura-scrittura).</span><span class="sxs-lookup"><span data-stu-id="54c79-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="54c79-107">L'uso della replica del database riduce il carico sul database primario.</span><span class="sxs-lookup"><span data-stu-id="54c79-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="54c79-108">In alcuni casi, migliorerà anche le prestazioni durante la visualizzazione dei dati nel client.</span><span class="sxs-lookup"><span data-stu-id="54c79-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="54c79-109">Le repliche sono utili per oggetti, come report, query e pagine API, che vengono utilizzati solo per visualizzare i dati, non per modificarli.</span><span class="sxs-lookup"><span data-stu-id="54c79-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="54c79-110">Quando gli oggetti vengono eseguiti, l'intento di accesso al database determina se utilizzare una replica di sola lettura, se disponibile, o il database primario.</span><span class="sxs-lookup"><span data-stu-id="54c79-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="54c79-111">Report, pagine API e query sono sviluppati con un intento di accesso al database predefinito (vedere [Proprietà DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="54c79-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="54c79-112">La pagina **Elenco di intenti di accesso al database** consente di ignorare l'intento di accesso al database predefinito per gli oggetti quando vengono eseguiti.</span><span class="sxs-lookup"><span data-stu-id="54c79-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="54c79-113">In termini di database, questa funzione è comunemente nota come *scale-out di lettura*. Per ulteriori informazioni sullo scale-out di lettura e sull'intento di accesso ai dati in [!INCLUDE[prod_short](includes/prod_short.md)], vedere [Utilizzo dello scale-out di lettura per prestazioni migliori](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) nella Guida di amministrazione e per sviluppatori di [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="54c79-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="54c79-114">Per modificare l'intento di accesso al database</span><span class="sxs-lookup"><span data-stu-id="54c79-114">To change the database access intent</span></span>

1. <span data-ttu-id="54c79-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elenco di intenti di accesso al database** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="54c79-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="54c79-116">La pagina elenca tutti i report, le pagine e le query.</span><span class="sxs-lookup"><span data-stu-id="54c79-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="54c79-117">La colonna **Intento di accesso** include uno dei seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="54c79-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="54c79-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="54c79-118">**Setting**</span></span>|<span data-ttu-id="54c79-119">**descrizione**</span><span class="sxs-lookup"><span data-stu-id="54c79-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="54c79-120">**Default**</span><span class="sxs-lookup"><span data-stu-id="54c79-120">**Default**</span></span>|<span data-ttu-id="54c79-121">Indica che l'oggetto utilizza l'intento di accesso al database predefinito.</span><span class="sxs-lookup"><span data-stu-id="54c79-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="54c79-122">**Consenti scrittura**</span><span class="sxs-lookup"><span data-stu-id="54c79-122">**Allow Write**</span></span>|<span data-ttu-id="54c79-123">Imposta l'oggetto per utilizzare il database primario, consentendo all'utente di modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="54c79-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="54c79-124">**Sola lettura**</span><span class="sxs-lookup"><span data-stu-id="54c79-124">**Read Only**</span></span>|<span data-ttu-id="54c79-125">Imposta l'oggetto per utilizzare la replica del database, il che significa che l'utente può solo visualizzare i dati, non modificarli.</span><span class="sxs-lookup"><span data-stu-id="54c79-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="54c79-126">Scegliere l'azione **Modifica lista**.</span><span class="sxs-lookup"><span data-stu-id="54c79-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="54c79-127">Nella pagina **Modifica - Elenco intenti di accesso al database**, modifica il campo **Intento di accesso** per gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="54c79-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54c79-128">Se un oggetto modificabile, come la scheda cliente, è impostato su **Sola lettura**, il database primario verrà comunque utilizzato, indipendentemente dall'intento di accesso, consentendo agli utenti di apportare modifiche normalmente.</span><span class="sxs-lookup"><span data-stu-id="54c79-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="54c79-129">Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="54c79-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="54c79-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="54c79-130">See Also</span></span>
[<span data-ttu-id="54c79-131">Funzionalità aziendale</span><span class="sxs-lookup"><span data-stu-id="54c79-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="54c79-132">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="54c79-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="54c79-133">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54c79-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="54c79-134">Introduzione</span><span class="sxs-lookup"><span data-stu-id="54c79-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]