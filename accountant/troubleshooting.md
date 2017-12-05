---
title: Risoluzione dei problemi o soluzioni alternative | Documenti Microsoft
description: Informazioni sulle soluzioni alternative per problemi di Accountant Hub per Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: it-it
ms.lasthandoff: 11/10/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="9ba3f-103">Risoluzione dei problemi [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ba3f-103">Troubleshooting [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="9ba3f-104">L'iscrizione a [!INCLUDE[d365acc](includes/d365acc_md.md)] è facile e può essere effettuata molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-104">Signing up for [!INCLUDE[d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="9ba3f-105">Anche aggiungere i clienti al dashboard è facile, ma in questo articolo vengono tratti i problemi che potrebbero verificarsi.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a><span data-ttu-id="9ba3f-106">Quale indirizzo e-mail posso utilizzare con [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span><span class="sxs-lookup"><span data-stu-id="9ba3f-106">What email address can I use with [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span></span>
[!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="9ba3f-107"> richiede l'utilizzo di un indirizzo e-mail di lavoro o della scuola.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-107"> requires that you use a work or school email address to sign up.</span></span> [!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="9ba3f-108"> non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-108"> does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="9ba3f-109">Questo include indirizzi di outlook.com, hotmail.com, gmail.com e altri simili.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="9ba3f-110">Se si prova a effettuare l'iscrizione con un indirizzo e-mail personale, si riceve un messaggio che richiede di utilizzare un indirizzo e-mail un lavoro o di scuola.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="9ba3f-111">Perché non posso collegarmi ai dati del cliente?</span><span class="sxs-lookup"><span data-stu-id="9ba3f-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="9ba3f-112">Questo potrebbe verificarsi per diversi motivi, tra cui i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ba3f-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="9ba3f-113">L'URL nel campo **URL cliente** non è valido.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="9ba3f-114">Vai a **Gestisci clienti**, apri il cliente a cui non è possibile connettersi e quindi scegli **Esegui test URL cliente**.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="9ba3f-115">La società del cliente è attualmente non in linea, ad esempio se è in corso un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9ba3f-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="9ba3f-116">Nel dashboard, scegli la voce di menu **Strumenti** e quindi **Controlla errori**.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="9ba3f-117">Verrà visualizzato un elenco con dettagli tecnici, in modo che sia possibile contattare l'amministratore se sono presenti errori.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="9ba3f-118">Ad esempio, il messaggio di errore simile al seguente: "Il server ha rifiutato le credenziali del cliente" suggerisce che l'utente non dispone delle autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="9ba3f-119">Non è stato ricevuto un messaggio e-mail del cliente con invito per [!INCLUDE[d365fin](includes/d365fin_md.md)] oppure non è stata aperto il collegamento nell'e-mail o non è stato accettato l'invito</span><span class="sxs-lookup"><span data-stu-id="9ba3f-119">You have not received an email from your client that invites them to their [!INCLUDE[d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="9ba3f-120">È necessario aprire il collegamento in questione e seguire i passaggi che consentono di aggiungersi al [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9ba3f-121">Sino a quel momento, non è possibile accedere ai dati.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="9ba3f-122">Non è possibile accedere a tutte le società presenti [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-122">You do not have access to all companies in your client's [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="9ba3f-123">Il cliente dispone di più business unit o società in [!INCLUDE[d365fin](includes/d365fin_md.md)] e l'invito non include sempre tutte le società.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-123">Your client can have multiple business units or companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="9ba3f-124">Collaborare con il cliente in modo che non sia possibile accedere alle società con cui il cliente desidera che tu lavori.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="9ba3f-125">Perché i dati non vengono aggiornati nel dashboard?</span><span class="sxs-lookup"><span data-stu-id="9ba3f-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="9ba3f-126">Quando si aggiunge un cliente o si richiede un aggiornamento dei dati, [!INCLUDE[d365acc](includes/d365acc_md.md)] recupera i dati.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-126">When you add a client or request a refresh of the data, [!INCLUDE[d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="9ba3f-127">Tuttavia è necessario aggiornare la finestra manualmente, ad esempio con l'azione Rivisualizza tutte le società, aggiornando la finestra del browser, uscendo e quindi rientrando nel dashboard o in altri modi simili.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="9ba3f-128">Si tratta di un problema noto su cui stiamo lavorando per la risoluzione in un aggiornamento successivo.</span><span class="sxs-lookup"><span data-stu-id="9ba3f-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ba3f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ba3f-129">See Also</span></span>
<span data-ttu-id="9ba3f-130">[Introduzione a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="9ba3f-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="9ba3f-131">[Aggiungere clienti al dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span><span class="sxs-lookup"><span data-stu-id="9ba3f-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

