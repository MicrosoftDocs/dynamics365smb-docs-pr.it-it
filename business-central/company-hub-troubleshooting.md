---
title: Risoluzione dei problemi nell'hub aziendale
description: Informazioni sulle soluzioni alternative per problemi nell'hub aziendale in Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f348de3e8116efd789f85f1b011ecc7013bf2b1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927695"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="fac73-103">Risoluzione dei problemi dell'hub aziendale</span><span class="sxs-lookup"><span data-stu-id="fac73-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="fac73-104">Anche aggiungere le società al dashboard dell'hub aziendale è facile, ma in questo articolo vengono tratti i problemi che potrebbero verificarsi.</span><span class="sxs-lookup"><span data-stu-id="fac73-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="fac73-105">Controlla errori</span><span class="sxs-lookup"><span data-stu-id="fac73-105">Check errors</span></span>

<span data-ttu-id="fac73-106">Usare l'azione **Controlla errori** per visualizzare un elenco di errori recenti.</span><span class="sxs-lookup"><span data-stu-id="fac73-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="fac73-107">È possibile visualizzare ulteriori dettagli per ogni errore e pulire il log eliminando le voci precedenti.</span><span class="sxs-lookup"><span data-stu-id="fac73-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="fac73-108">Connessione non riuscita</span><span class="sxs-lookup"><span data-stu-id="fac73-108">Connection failed</span></span>

<span data-ttu-id="fac73-109">Ci possono essere un paio di motivi per cui non è possibile connettersi a una società, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fac73-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="fac73-110">L'URL nel campo **Collegamento ambiente** non è valido.</span><span class="sxs-lookup"><span data-stu-id="fac73-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="fac73-111">Andare alla pagina **Collegamenti ambiente**, aprire l'ambiente a cui non è possibile connettersi, quindi scegliere l'azione **Test della connessione**.</span><span class="sxs-lookup"><span data-stu-id="fac73-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="fac73-112">La società del cliente è attualmente non in linea, ad esempio se è in corso un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fac73-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="fac73-113">Nel dashboard, scegli la voce di menu **Strumenti** e quindi **Controlla errori**.</span><span class="sxs-lookup"><span data-stu-id="fac73-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="fac73-114">Verrà visualizzato un elenco con dettagli tecnici, in modo che sia possibile contattare l'amministratore se sono presenti errori.</span><span class="sxs-lookup"><span data-stu-id="fac73-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="fac73-115">Ad esempio, il messaggio di errore simile al seguente: "*Il server ha rifiutato le credenziali del cliente*" suggerisce che l'utente non dispone delle autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="fac73-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="fac73-116">Non si dispone dell'accesso a tutte le società nell'ambiente a cui si sta tentando di connettersi</span><span class="sxs-lookup"><span data-stu-id="fac73-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="fac73-117">In [!INCLUDE [prodshort](includes/prodshort.md)], un'organizzazione può avere più business unit denominate società ed è possibile che non si disponga dell'accesso a tutte le società.</span><span class="sxs-lookup"><span data-stu-id="fac73-117">In [!INCLUDE [prodshort](includes/prodshort.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="fac73-118">Collaborare con l'amministratore o il cliente in modo che sia possibile accedere alle società con si desidera lavorare.</span><span class="sxs-lookup"><span data-stu-id="fac73-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="fac73-119">I dati non vengono aggiornati</span><span class="sxs-lookup"><span data-stu-id="fac73-119">Data does not refresh</span></span>

<span data-ttu-id="fac73-120">Quando si aggiunge una società o si richiede un aggiornamento dei dati, [!INCLUDE [prodshort](includes/prodshort.md)] recupera i dati.</span><span class="sxs-lookup"><span data-stu-id="fac73-120">When you add a company or request a refresh of the data, [!INCLUDE [prodshort](includes/prodshort.md)] fetches the data.</span></span> <span data-ttu-id="fac73-121">Tuttavia è necessario aggiornare la pagina manualmente, ad esempio con l'azione **Ricarica tutte le società**, aggiornando la pagina del browser, uscendo e quindi rientrando nel dashboard o in altri modi simili.</span><span class="sxs-lookup"><span data-stu-id="fac73-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="fac73-122">Se è stata aggiunta una società, ma non viene visualizzata nell'elenco, è anche possibile utilizzare l'azione **Ricarica tutte le società** per aggiornare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="fac73-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="fac73-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fac73-123">See also</span></span>

[<span data-ttu-id="fac73-124">Gestire il lavoro tra più aziende nell'hub aziendale</span><span class="sxs-lookup"><span data-stu-id="fac73-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="fac73-125">Aggiungere società all'hub aziendale</span><span class="sxs-lookup"><span data-stu-id="fac73-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="fac73-126">Esperienze contabile in Business Central</span><span class="sxs-lookup"><span data-stu-id="fac73-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  
