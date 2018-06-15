---
title: Configurazione dei modelli API | Microsoft Docs
description: Descrive i passaggi da seguire per configurare modelli di API per Dynamics 365 Business Central.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: it-it
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a><span data-ttu-id="55047-103">Configurazione di modelli di API</span><span class="sxs-lookup"><span data-stu-id="55047-103">Configuring API Templates</span></span>
<span data-ttu-id="55047-104">La libreria di API per [!INCLUDE[d365fin_md](includes/d365fin_md.md)] fornisce una rappresentazione semplificata delle entità sottostanti.</span><span class="sxs-lookup"><span data-stu-id="55047-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="55047-105">Tutte le proprietà dell'applicazione non sono esposte tramite l'API associata.</span><span class="sxs-lookup"><span data-stu-id="55047-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="55047-106">La finestra **Setup API** consente di definire modelli utilizzati per popolare le proprietà vuote in un'entità quando si crea un'azione POST tramite l'API.</span><span class="sxs-lookup"><span data-stu-id="55047-106">The **API Setup** window allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="55047-107">Ad esempio, se per l'entità articolo viene definito un modello di configurazione, quando viene creato un nuovo record di articolo tramite l'API articoli, tutte le proprietà per il nuovo articolo che non sono definite nella chiamata API verranno popolate dal modello selezionato.</span><span class="sxs-lookup"><span data-stu-id="55047-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="55047-108">Se, ad esempio, non è definito alcun valore per il campo **Cat. reg. articolo/servizio** tramite l'API, ma un valore è definito nel modello selezionato, al nuovo articolo verrà applicato il valore del gruppo di registrazione definito nel modello.</span><span class="sxs-lookup"><span data-stu-id="55047-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="55047-109">Impostazione del modello di entità</span><span class="sxs-lookup"><span data-stu-id="55047-109">Setting up the Entity Template</span></span>
<span data-ttu-id="55047-110">Per utilizzare i modelli con la libreria di API, è prima necessario definire e impostare le proprietà per i modelli.</span><span class="sxs-lookup"><span data-stu-id="55047-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="55047-111">È possibile impostare questi modelli nella finestra **Modelli di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="55047-111">You can set up these templates in the **Configuration Templates** window.</span></span> <span data-ttu-id="55047-112">Per ulteriori informazioni, vedere [Preparare la migrazione dei dati dei clienti](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="55047-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="55047-113">Assegnare il modello a un'API</span><span class="sxs-lookup"><span data-stu-id="55047-113">Assign the template to an API</span></span>

<span data-ttu-id="55047-114">Per assegnare un modello a un'API, è necessario seguire questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="55047-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="55047-115">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup API**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="55047-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="55047-116">Scegliere **Nuovo** e quindi scegliere il valore **Ordine** per importare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="55047-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="55047-117">Se è presente più di un modello selezionato per un'API (ID pagina), i modelli vengono applicati nell'ordine definito nella colonna **Order**.</span><span class="sxs-lookup"><span data-stu-id="55047-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="55047-118">Quando ciascun modello viene applicato, i valori dei campi definiti nel modello vengono applicati solo ai campi che non hanno ancora definito un valore, esplicitamente nell'API o in un modello precedentemente applicato nell'ordine.</span><span class="sxs-lookup"><span data-stu-id="55047-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="55047-119">Selezionare un valore **ID pagina**.</span><span class="sxs-lookup"><span data-stu-id="55047-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="55047-120">Questa è la pagina per l'API a cui verrà applicato il modello.</span><span class="sxs-lookup"><span data-stu-id="55047-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="55047-121">La ricerca **ID pagina** fornisce un elenco di tutte le API disponibili nella libreria.</span><span class="sxs-lookup"><span data-stu-id="55047-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="55047-122">Selezionare un valore nel campo **Codice modello**.</span><span class="sxs-lookup"><span data-stu-id="55047-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="55047-123">Il codice modello è il codice per il modello definito nella finestra **Modelli di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="55047-123">The template code is the code for the template that was defined in the **Configuration Templates** window.</span></span> <span data-ttu-id="55047-124">I valori del modello definiti vengono applicati all'API.</span><span class="sxs-lookup"><span data-stu-id="55047-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="55047-125">Nel campo **Condizioni** specificare quale modello deve essere applicato.</span><span class="sxs-lookup"><span data-stu-id="55047-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="55047-126">Il modello definito viene applicato a un nuovo record creato tramite l'API se, e solo se, le condizioni definite nel campo **Condizioni** sono soddisfatte dai valori già definiti per la nuova istanza dell'entità.</span><span class="sxs-lookup"><span data-stu-id="55047-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="55047-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55047-127">See Also</span></span>
[<span data-ttu-id="55047-128">Documentazione API</span><span class="sxs-lookup"><span data-stu-id="55047-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="55047-129">[Sviluppo di app Connect per [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="55047-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="55047-130">Abilitare le API</span><span class="sxs-lookup"><span data-stu-id="55047-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="55047-131">Endpoint per le API</span><span class="sxs-lookup"><span data-stu-id="55047-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="55047-132">Impostare una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="55047-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="55047-133">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="55047-133">Administration</span></span>](admin-setup-and-administration.md)
