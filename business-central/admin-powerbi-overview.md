---
title: Componente di integrazione Power BI e panoramica dell'architettura per Business Central | Microsoft Docs
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con le app Business Central per Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: d02740b0f4c73b96be9268cfdf5e4c3de157d5d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924530"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a><span data-ttu-id="e0e69-103">Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="e0e69-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="e0e69-104">In questo articolo vengono descritti i diversi aspetti dell'integrazione Power BI con [!INCLUDE[prodshort](includes/prodshort.md)] per comprenderne l'implementazione e l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e0e69-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prodshort](includes/prodshort.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="e0e69-105">Componenti</span><span class="sxs-lookup"><span data-stu-id="e0e69-105">Components</span></span>

<span data-ttu-id="e0e69-106">La tabella seguente descrive i principali componenti coinvolti nell'integrazione Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="e0e69-107">Componente</span><span class="sxs-lookup"><span data-stu-id="e0e69-107">Component</span></span>|<span data-ttu-id="e0e69-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0e69-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="e0e69-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-109">Power BI</span></span>|<span data-ttu-id="e0e69-110">Un servizio di hosting e gestione di report basato su cloud.</span><span class="sxs-lookup"><span data-stu-id="e0e69-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="e0e69-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e0e69-111">Power BI Desktop</span></span>|<span data-ttu-id="e0e69-112">Uno strumento per la creazione di report e dashboard e consente di eseguire report.</span><span class="sxs-lookup"><span data-stu-id="e0e69-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="e0e69-113">È disponibile come download gratuito su Microsoft Store e viene installato localmente.</span><span class="sxs-lookup"><span data-stu-id="e0e69-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prodshort](includes/prodshort.md)]|<span data-ttu-id="e0e69-114">Soluzione online o locale con connettori esposti a Power BI e la capacità di incorporare una parte Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="e0e69-115">Cosa è disponibile dall'inizio</span><span class="sxs-lookup"><span data-stu-id="e0e69-115">What's available from the start</span></span>

<span data-ttu-id="e0e69-116">Nella seguente tabella vengono illustrate le funzionalità disponibili.</span><span class="sxs-lookup"><span data-stu-id="e0e69-116">The following table describes available features.</span></span>

|<span data-ttu-id="e0e69-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e0e69-117">Feature</span></span>|<span data-ttu-id="e0e69-118">Supporto [!INCLUDE[prodshort](includes/prodshort.md)] online o locale</span><span class="sxs-lookup"><span data-stu-id="e0e69-118">[!INCLUDE[prodshort](includes/prodshort.md)] online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="e0e69-119">Connettori Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-119">Power BI connectors</span></span>|<span data-ttu-id="e0e69-120">Entrambe.</span><span class="sxs-lookup"><span data-stu-id="e0e69-120">Both.</span></span> <span data-ttu-id="e0e69-121">Connettori diversi per online e locale.</span><span class="sxs-lookup"><span data-stu-id="e0e69-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="e0e69-122">Stesso connettore utilizzato per Power BI Desktop e il servizio Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="e0e69-123">Esperienza incorporata per la visualizzazione di un determinato report all'interno di un riquadro Dettaglio informazioni in [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="e0e69-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="e0e69-124">Entrambe.</span><span class="sxs-lookup"><span data-stu-id="e0e69-124">Both.</span></span> <span data-ttu-id="e0e69-125">Richiede la configurazione per visualizzare i report in locale.</span><span class="sxs-lookup"><span data-stu-id="e0e69-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="e0e69-126">Gestione dei report Power BI da [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="e0e69-126">Power BI report management from [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="e0e69-127">Online</span><span class="sxs-lookup"><span data-stu-id="e0e69-127">Online</span></span>|
|<span data-ttu-id="e0e69-128">Report Power BI predefiniti nella Gestione ruolo utente distribuiti a Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="e0e69-129">Online</span><span class="sxs-lookup"><span data-stu-id="e0e69-129">Online</span></span>|
|<span data-ttu-id="e0e69-130">App Power BI in Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="e0e69-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="e0e69-131">Online.</span><span class="sxs-lookup"><span data-stu-id="e0e69-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="e0e69-132">Architettura</span><span class="sxs-lookup"><span data-stu-id="e0e69-132">Architecture</span></span>

[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="e0e69-133">si integra con Power BI tramite un connettore utilizzando OData.</span><span class="sxs-lookup"><span data-stu-id="e0e69-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="e0e69-134">L'origine dati per i report Power BI è esposta come servizi web OData.</span><span class="sxs-lookup"><span data-stu-id="e0e69-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Architettura Power BI per l'integrazione con Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="e0e69-136">Flusso generale</span><span class="sxs-lookup"><span data-stu-id="e0e69-136">General Flow</span></span>

<span data-ttu-id="e0e69-137">Il diagramma seguente illustra il flusso di lavoro di base per gli utenti durante la connessione di [!INCLUDE[prodshort](includes/prodshort.md)] a Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prodshort](includes/prodshort.md)] to Power BI.</span></span>

![Flusso di lavoro Power BI per l'integrazione con Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="e0e69-139">L'utente si iscrive per un account Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="e0e69-140">L'utente si connette a Power BI da [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e0e69-140">User connects to Power BI from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>
3. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="e0e69-141">verifica la licenza.</span><span class="sxs-lookup"><span data-stu-id="e0e69-141">verifies the license.</span></span>
4. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="e0e69-142">distribuisce report predefiniti al servizio Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="e0e69-143">Questo passaggio avviene solo per [!INCLUDE[prodshort](includes/prodshort.md)] online.</span><span class="sxs-lookup"><span data-stu-id="e0e69-143">This step only happens for [!INCLUDE[prodshort](includes/prodshort.md)] online.</span></span>
5. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="e0e69-144">rende i report in Power BI disponibili per la selezione in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e0e69-144">makes reports in Power BI available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="e0e69-145">I report predefiniti vengono visualizzati automaticamente nelle parti Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="e0e69-146">L'utente crea un report in Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="e0e69-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="e0e69-147">L'utente pubblica il report nel servizio Power BI.</span><span class="sxs-lookup"><span data-stu-id="e0e69-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="e0e69-148">I report diventano anche disponibili per la selezione in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e0e69-148">The reports are then available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="e0e69-149">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="e0e69-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="e0e69-150">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e0e69-150">See Also</span></span>

[<span data-ttu-id="e0e69-151">Business Central e Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="e0e69-152">Power BI per i consumatori</span><span class="sxs-lookup"><span data-stu-id="e0e69-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="e0e69-153">Il "nuovo look" del servizio Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="e0e69-154">Avvio rapido: connettersi ai dati in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e0e69-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="e0e69-155">Documentazione di Power BI</span><span class="sxs-lookup"><span data-stu-id="e0e69-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="e0e69-156">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="e0e69-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="e0e69-157">Introduzione</span><span class="sxs-lookup"><span data-stu-id="e0e69-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="e0e69-158">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="e0e69-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e0e69-159">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="e0e69-159">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
<span data-ttu-id="e0e69-160">[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="e0e69-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="e0e69-161">[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="e0e69-161">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="e0e69-162">[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="e0e69-162">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
