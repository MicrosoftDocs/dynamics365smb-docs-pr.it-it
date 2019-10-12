---
title: Risoluzione dei problemi relativi agli errori di sincronizzazione | Microsoft Docs
description: Fornisce alcune indicazioni per l'identificazione e la risoluzione degli errori di sincronizzazione.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304260"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="d0253-103">Risoluzione dei problemi relativi agli errori di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="d0253-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="d0253-104">Ci sono molte parti mobili coinvolte nell'integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] e a volte le cose vanno male.</span><span class="sxs-lookup"><span data-stu-id="d0253-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="d0253-105">Questo argomento evidenzia alcuni degli errori tipici che si verificano e fornisce alcuni suggerimenti su come risolverli.</span><span class="sxs-lookup"><span data-stu-id="d0253-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="d0253-106">Gli errori si verificano spesso a causa di un'operazione che un utente ha eseguito per i record associati o di un errore di impostazione dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0253-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="d0253-107">Per gli errori relativi ai record associati, gli utenti possono risolverli da soli.</span><span class="sxs-lookup"><span data-stu-id="d0253-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="d0253-108">Questi errori sono causati da azioni quali l'eliminazione di un record in una, ma non entrambe, le app aziendali e quindi la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0253-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="d0253-109">Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="d0253-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="d0253-110">Gli errori correlati all'impostazione dell'integrazione richiedono in genere l'attenzione dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="d0253-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="d0253-111">È possibile visualizzare questi errori nella pagina **Errori di sincronizzazione integrazione**.</span><span class="sxs-lookup"><span data-stu-id="d0253-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="d0253-112">Esempi di alcuni problemi tipici sono:</span><span class="sxs-lookup"><span data-stu-id="d0253-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="d0253-113">Le autorizzazioni e i ruoli assegnati agli utenti non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="d0253-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="d0253-114">L'account amministratore è stato specificato come utente di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0253-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="d0253-115">La password dell'utente di integrazione è impostata per richiedere una modifica quando l'utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="d0253-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="d0253-116">I tassi di cambio per le valute non sono specificati nell'una o nell'altra app.</span><span class="sxs-lookup"><span data-stu-id="d0253-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="d0253-117">È necessario risolvere manualmente gli errori, ma in alcuni casi la pagina risulta utile.</span><span class="sxs-lookup"><span data-stu-id="d0253-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="d0253-118">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d0253-118">For example:</span></span>  

* <span data-ttu-id="d0253-119">I campi **Origine** e **Destinazione** possono contenere collegamenti al record in cui è stato trovato l'errore.</span><span class="sxs-lookup"><span data-stu-id="d0253-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="d0253-120">Fare clic sul collegamento per aprire il record e analizzare l'errore.</span><span class="sxs-lookup"><span data-stu-id="d0253-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="d0253-121">Le azioni **Elimina movimenti risalenti a più di 7 giorni prima**e **Elimina tutti i movimenti** puliranno l'elenco.</span><span class="sxs-lookup"><span data-stu-id="d0253-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="d0253-122">In genere, si utilizzano queste azioni dopo aver risolto la causa di un errore che interessa molti record.</span><span class="sxs-lookup"><span data-stu-id="d0253-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="d0253-123">Tuttavia, prestare attenzione.</span><span class="sxs-lookup"><span data-stu-id="d0253-123">Use caution, however.</span></span> <span data-ttu-id="d0253-124">Queste azioni potrebbero eliminare errori che sono ancora rilevanti.</span><span class="sxs-lookup"><span data-stu-id="d0253-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0253-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d0253-125">See Also</span></span>
<span data-ttu-id="d0253-126">[Integrazione con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="d0253-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="d0253-127">[Impostazione di account utente per l'integrazione con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="d0253-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="d0253-128">[Impostare una connessione a [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="d0253-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="d0253-129">Associare e sincronizzare i record manualmente</span><span class="sxs-lookup"><span data-stu-id="d0253-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="d0253-130">Visualizzare lo stato di una sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="d0253-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  