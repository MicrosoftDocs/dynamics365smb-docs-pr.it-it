---
title: Gestire gli intenti di accesso al database in Business Central | Microsoft Docs
description: Modifica l'intento di accesso al database per report, pagine API e query.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 98105cb3e3634169b31a850f20a65a3854b006b4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911557"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="42f6a-103">Gestione dell'intento di accesso al database</span><span class="sxs-lookup"><span data-stu-id="42f6a-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="42f6a-104">In qualità di utente con privilegi avanzati o amministratore, puoi modificare l'intento di accesso al database su report, pagine di tipo API e query per migliorare le prestazioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="42f6a-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="42f6a-105">Sintesi</span><span class="sxs-lookup"><span data-stu-id="42f6a-105">Overview</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="42f6a-106">può essere configurata per utilizzare repliche di sola lettura del database primario (lettura-scrittura).</span><span class="sxs-lookup"><span data-stu-id="42f6a-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="42f6a-107">L'uso della replica del database riduce il carico sul database primario.</span><span class="sxs-lookup"><span data-stu-id="42f6a-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="42f6a-108">In alcuni casi, migliorerà anche le prestazioni durante la visualizzazione dei dati nel client.</span><span class="sxs-lookup"><span data-stu-id="42f6a-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="42f6a-109">Le repliche sono utili per oggetti, come report, query e pagine API, che vengono utilizzati solo per visualizzare i dati, non per modificarli.</span><span class="sxs-lookup"><span data-stu-id="42f6a-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="42f6a-110">Quando gli oggetti vengono eseguiti, l'intento di accesso al database determina se utilizzare una replica di sola lettura, se disponibile, o il database primario.</span><span class="sxs-lookup"><span data-stu-id="42f6a-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="42f6a-111">Report, pagine API e query sono sviluppati con un intento di accesso al database predefinito (vedere [Proprietà DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="42f6a-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="42f6a-112">La pagina **Elenco di intenti di accesso al database** consente di ignorare l'intento di accesso al database predefinito per gli oggetti quando vengono eseguiti.</span><span class="sxs-lookup"><span data-stu-id="42f6a-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="42f6a-113">In termini di database, questa funzione è comunemente nota come *scale-out di lettura*. Per ulteriori informazioni sullo scale-out di lettura e sull'intento di accesso ai dati in [!INCLUDE[prodshort](includes/prodshort.md)], vedere [Utilizzo dello scale-out di lettura per prestazioni migliori](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) nella Guida di amministrazione e per sviluppatori di [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="42f6a-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prodshort](includes/prodshort.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prodshort](includes/prodshort.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="42f6a-114">Per modificare l'intento di accesso al database</span><span class="sxs-lookup"><span data-stu-id="42f6a-114">To change the database access intent</span></span>

1. <span data-ttu-id="42f6a-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elenco di intenti di accesso al database** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="42f6a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="42f6a-116">La pagina elenca tutti i report, le pagine e le query.</span><span class="sxs-lookup"><span data-stu-id="42f6a-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="42f6a-117">La colonna **Intento di accesso** include uno dei seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="42f6a-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="42f6a-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="42f6a-118">**Setting**</span></span>|<span data-ttu-id="42f6a-119">**descrizione**</span><span class="sxs-lookup"><span data-stu-id="42f6a-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="42f6a-120">**Default**</span><span class="sxs-lookup"><span data-stu-id="42f6a-120">**Default**</span></span>|<span data-ttu-id="42f6a-121">Indica che l'oggetto utilizza l'intento di accesso al database predefinito.</span><span class="sxs-lookup"><span data-stu-id="42f6a-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="42f6a-122">**Consenti scrittura**</span><span class="sxs-lookup"><span data-stu-id="42f6a-122">**Allow Write**</span></span>|<span data-ttu-id="42f6a-123">Imposta l'oggetto per utilizzare il database primario, consentendo all'utente di modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="42f6a-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="42f6a-124">**Sola lettura**</span><span class="sxs-lookup"><span data-stu-id="42f6a-124">**Read Only**</span></span>|<span data-ttu-id="42f6a-125">Imposta l'oggetto per utilizzare la replica del database, il che significa che l'utente può solo visualizzare i dati, non modificarli.</span><span class="sxs-lookup"><span data-stu-id="42f6a-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="42f6a-126">Scegliere l'azione **Modifica lista**.</span><span class="sxs-lookup"><span data-stu-id="42f6a-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="42f6a-127">Nella pagina **Modifica - Elenco intenti di accesso al database**, modifica il campo **Intento di accesso** per gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="42f6a-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42f6a-128">Se un oggetto modificabile, come la scheda cliente, è impostato su **Sola lettura**, il database primario verrà comunque utilizzato, indipendentemente dall'intento di accesso, consentendo agli utenti di apportare modifiche normalmente.</span><span class="sxs-lookup"><span data-stu-id="42f6a-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="42f6a-129">Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="42f6a-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="42f6a-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="42f6a-130">See Also</span></span>
[<span data-ttu-id="42f6a-131">Funzionalità aziendale</span><span class="sxs-lookup"><span data-stu-id="42f6a-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="42f6a-132">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="42f6a-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="42f6a-133">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="42f6a-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="42f6a-134">Introduzione</span><span class="sxs-lookup"><span data-stu-id="42f6a-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
