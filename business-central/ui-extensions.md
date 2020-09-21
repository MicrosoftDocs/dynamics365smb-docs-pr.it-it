---
title: Installare le estensioni per personalizzare Business Central | Documenti Microsoft
description: Informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle estensioni.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765923"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="cdf92-103">Personalizzazione di Business Central con le estensioni</span><span class="sxs-lookup"><span data-stu-id="cdf92-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="cdf92-104">È possibile modificare [!INCLUDE[d365fin](includes/d365fin_md.md)] installando estensioni che, ad esempio, aggiungano funzionalità, modifichino il comportamento o permettano di accedere a nuovi servizi online.</span><span class="sxs-lookup"><span data-stu-id="cdf92-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="cdf92-105">Per installare le estensioni da AppSource o aggiungere estensioni per tenant, è necessario avere le autorizzazioni giuste.</span><span class="sxs-lookup"><span data-stu-id="cdf92-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="cdf92-106">È necessario essere membri del gruppo utenti D365 EXTENSION MGMT oppure disporre dell'autorizzazione D365 EXTENSION MGMT impostata.</span><span class="sxs-lookup"><span data-stu-id="cdf92-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="cdf92-107">Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda.</span><span class="sxs-lookup"><span data-stu-id="cdf92-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="cdf92-108">Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="cdf92-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="cdf92-109">Il caricamento di estensioni per tenant e l'installazione di estensioni AppSource non sono supportati tramite la pagina **Gestione delle estensioni** per installazioni locali.</span><span class="sxs-lookup"><span data-stu-id="cdf92-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="cdf92-110">La prima volta che si avvia [!INCLUDE[d365fin](includes/d365fin_md.md)], alcune estensioni risultano già installate.</span><span class="sxs-lookup"><span data-stu-id="cdf92-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="cdf92-111">Con il tempo verranno rese disponibili altre estensioni e sarà possibile scegliere se installarle o meno.</span><span class="sxs-lookup"><span data-stu-id="cdf92-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="cdf92-112">Ad esempio, Microsoft fornisce un'estensione che consente l'integrazione con PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="cdf92-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="cdf92-113">Questa estensione è installata per impostazione di default.</span><span class="sxs-lookup"><span data-stu-id="cdf92-113">This extension is installed by default.</span></span>
<span data-ttu-id="cdf92-114">Se tuttavia diventa disponibile un'altra estensione che offre l'integrazione con un altro servizio di pagamento, è possibile installare la nuova estensione e scegliere quale dei due servizi utilizzare.</span><span class="sxs-lookup"><span data-stu-id="cdf92-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="cdf92-115">Le estensioni vengono gestite nella pagina **Gestione estensioni**.</span><span class="sxs-lookup"><span data-stu-id="cdf92-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="cdf92-116">È possibile accedere a questa pagina dalla home page.</span><span class="sxs-lookup"><span data-stu-id="cdf92-116">You can access this page from Home.</span></span> <span data-ttu-id="cdf92-117">In alternativa, scegliere l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo superiore destro, immettere **Estensione**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="cdf92-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="cdf92-118">Per ulteriori informazioni, vedere [Installazione e disinstallazione delle estensioni](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="cdf92-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="cdf92-119">Se si prevede di dover accedere a un'estensione, ma non è possibile individuare la relativa funzionalità, controllare la pagina **Gestione estensioni**, se l'estensione non è elencata, è possibile installarla come descritto nella sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="cdf92-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="cdf92-120">Le nuove estensioni non saranno subito disponibili in AppSource dopo l'annuncio di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="cdf92-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="cdf92-121">Seguire gli aggiornamenti sulla disponibilità delle estensioni tramite il sito Web [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="cdf92-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="cdf92-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdf92-122">See Also</span></span>

[<span data-ttu-id="cdf92-123">Estensione di Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="cdf92-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="cdf92-124">Estensioni per Business Central fornite da altri provider</span><span class="sxs-lookup"><span data-stu-id="cdf92-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="cdf92-125">Impostare il servizio Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="cdf92-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="cdf92-126">Abilitare i pagamenti clienti attraverso PayPal</span><span class="sxs-lookup"><span data-stu-id="cdf92-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="cdf92-127">Migrazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="cdf92-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="cdf92-128">Impostazione dell'estensione dei codici postali GetAddress.io per il Regno Unito</span><span class="sxs-lookup"><span data-stu-id="cdf92-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="cdf92-129">[Estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] fornite da altri provider](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="cdf92-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="cdf92-130">Introduzione</span><span class="sxs-lookup"><span data-stu-id="cdf92-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
