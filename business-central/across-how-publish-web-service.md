---
title: Esporre oggetti come servizi Web | Microsoft Docs
description: Pubblicare oggetti come servizi Web per renderli immediatamente disponibili per la propria soluzione di Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/04/2020
ms.author: edupont
ms.openlocfilehash: 4e09df754895a8d0d3a1cc1ed84a7c8332e32880
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030246"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="3b8c8-103">Pubblicare un servizio Web</span><span class="sxs-lookup"><span data-stu-id="3b8c8-103">Publish a Web Service</span></span>

<span data-ttu-id="3b8c8-104">I servizi Web sono un modo semplice ed efficace per rendere le funzionalità di applicazioni disponibili a vari sistemi e utenti esterni.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3b8c8-105">include vari oggetti che, per impostazione predefinita, vengono esposti come servizi Web in seguito all'integrazione in altri servizi Microsoft, ma è anche possibile aggiungere altri servizi Web.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="3b8c8-106">Si configura un servizio Web nel client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3b8c8-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="3b8c8-107">È necessario pubblicare il servizio Web per renderlo disponibile alle richieste di assistenza nella rete.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="3b8c8-108">Gli utenti possono individuare i servizi Web puntando un browser al percorso del server e richiedendo un elenco dei servizi disponibili.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="3b8c8-109">Quando si pubblica un servizio Web, diviene immediatamente disponibile in rete per gli utenti autenticati.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="3b8c8-110">Tutti gli utenti autorizzati possono accedere ai metadati per i servizi Web, ma solo gli utenti che dispongono di permessi sufficienti possono accedere ai dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="3b8c8-111">Creazione e pubblicazione di un servizio Web</span><span class="sxs-lookup"><span data-stu-id="3b8c8-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="3b8c8-112">I seguenti passaggi illustrano come creare e pubblicare un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="3b8c8-113">Per creare e pubblicare un servizio Web</span><span class="sxs-lookup"><span data-stu-id="3b8c8-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="3b8c8-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Servizi Web** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3b8c8-115">Nella pagina **Servizi Web** selezionare **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="3b8c8-116">**Codeunit** e **Pagina** sono tipi validi per servizi Web SOAP.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="3b8c8-117">**Pagina** e **Query** sono tipi validi per i servizi Web OData.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="3b8c8-118">Inoltre, se il database contiene più società, è possibile scegliere un ID oggetto specifico di una delle società.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="3b8c8-119">Il nome del servizio è visibile agli utenti del servizio Web e poiché è la base per l'identificazione e la distinzione dei servizi Web, è importante che sia un nome significativo.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="3b8c8-120">Selezionare la casella di controllo nella colonna **Pubblicato**.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="3b8c8-121">Quando si pubblica il servizio Web, nei campi **URL OData** e **URL SOAP** è possibile vedere gli URL che sono generati per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="3b8c8-122">È possibile verificare il servizio web immediatamente selezionando i collegamenti nei campi **URL SOAP** e **URL OData**.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="3b8c8-123">In alternativa, è possibile copiare il valore del campo e salvarlo per un successivo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3b8c8-124">Per le codeunit pubblicate come servizio Web SOAP, i metodi esposti nella codeunit devono essere contrassegnati come `[External]` nel codice.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-124">For codeunits that are published as a SOAP web service, the methods exposed in the codeunit must be marked as `[External]` in the code.</span></span>

<span data-ttu-id="3b8c8-125">Dopo la pubblicazione di un servizio Web, questo è immediatamente disponibile per le parti esterne.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-125">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="3b8c8-126">È possibile verificare la disponibilità del servizio Web utilizzando un browser, oppure è possibile scegliere il collegamento nei campi **URL SOAP** e **URL OData** nella pagina **Servizi Web**.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-126">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="3b8c8-127">La procedura seguente illustra come verificare la disponibilità del servizio Web per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-127">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="3b8c8-128">Per verificare la disponibilità di un servizio Web</span><span class="sxs-lookup"><span data-stu-id="3b8c8-128">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="3b8c8-129">Nel browser immettere l'URL pertinente.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-129">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="3b8c8-130">Nella seguente tabella sono illustrati i tipi di URL che è possibile immettere per tipi di servizi Web diversi.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-130">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="3b8c8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b8c8-131">Type</span></span>|<span data-ttu-id="3b8c8-132">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b8c8-132">Syntax</span></span>|<span data-ttu-id="3b8c8-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="3b8c8-133">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="3b8c8-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="3b8c8-134">SOAP</span></span>|<span data-ttu-id="3b8c8-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/</span><span class="sxs-lookup"><span data-stu-id="3b8c8-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/</span></span> |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |<span data-ttu-id="3b8c8-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="3b8c8-136">OData V4</span></span>|<span data-ttu-id="3b8c8-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*</span><span class="sxs-lookup"><span data-stu-id="3b8c8-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*</span></span>|<span data-ttu-id="3b8c8-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span><span class="sxs-lookup"><span data-stu-id="3b8c8-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span></span><br/>    <span data-ttu-id="3b8c8-139">Per la ragione sociale viene osservata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-139">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="3b8c8-140">Esaminare le informazioni visualizzate nel browser.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="3b8c8-141">Verificare che sia possibile visualizzare il nome del servizio Web creato.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-141">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="3b8c8-142">Quando si accede a un servizio Web e si desidera scrivere i dati di nuovo in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario specificare il nome della società.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="3b8c8-143">È possibile specificare la società come parte di URI come illustrato negli esempi, oppure è possibile specificare la società come parte dei parametri di query.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="3b8c8-144">Ad esempio, gli URI successivi scelgono lo stesso servizio Web OData e sono entrambi URI validi.</span><span class="sxs-lookup"><span data-stu-id="3b8c8-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="3b8c8-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3b8c8-145">See Also</span></span>

[<span data-ttu-id="3b8c8-146">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="3b8c8-146">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="3b8c8-147">Servizi Web di Business Central per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3b8c8-147">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
