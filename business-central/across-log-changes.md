---
title: Revisione delle modifiche | Microsoft Docs
description: È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate. È anche possibile tenere traccia delle attività con determinati tipi di registri attività.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 43aea054ce4e66e9108f408d96c2eb491351b382
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304933"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="7715f-104">Revisione delle modifiche in Business Central</span><span class="sxs-lookup"><span data-stu-id="7715f-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="7715f-105">È possibile abilitare il log modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo da disporre di uno storico delle attività.</span><span class="sxs-lookup"><span data-stu-id="7715f-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="7715f-106">Il log è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nella pagina **Movimenti log modifiche**, i movimenti vengono ordinati cronologicamente e mostrano le modifiche apportate ai campi nelle tabelle specificate.</span><span class="sxs-lookup"><span data-stu-id="7715f-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="7715f-107">Il log modifiche raccoglie tutte le modifiche apportate alla tabella.</span><span class="sxs-lookup"><span data-stu-id="7715f-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="7715f-108">Le modifiche di un utente non sono visibili in **Movimenti log modifiche** fino al riavvio della sessione dell'utente, che avviene nei seguenti casi:</span><span class="sxs-lookup"><span data-stu-id="7715f-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="7715f-109">La sessione è scaduta ed è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7715f-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="7715f-110">L'utente ha selezionato un'altra società o gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="7715f-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="7715f-111">L'utente si è disconnesso e connesso di nuovo.</span><span class="sxs-lookup"><span data-stu-id="7715f-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="7715f-112">Utilizzo del log modifiche</span><span class="sxs-lookup"><span data-stu-id="7715f-112">Working with the Change Log</span></span>

<span data-ttu-id="7715f-113">Un problema comune in diversi sistemi finanziari è individuare l'origine degli errori e delle modifiche dei dati.</span><span class="sxs-lookup"><span data-stu-id="7715f-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="7715f-114">Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="7715f-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="7715f-115">Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database.</span><span class="sxs-lookup"><span data-stu-id="7715f-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="7715f-116">È necessario specificare cosa si desidera venga registrato per ciascuna tabella e campo, quindi attivare il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="7715f-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="7715f-117">Il log modifiche viene attivato e disattivato nella pagina **Setup log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="7715f-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="7715f-118">Quando un utente attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="7715f-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="7715f-119">Nella pagina **Setup log modifiche** se si sceglie l'azione **Tabelle** è possibile specificare le tabelle di cui si desidera tracciare le modifiche e le modifiche da tracciare. [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene traccia anche di una serie di tabelle di sistema.</span><span class="sxs-lookup"><span data-stu-id="7715f-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="7715f-120">Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella pagina **Movimenti log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="7715f-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="7715f-121">Se si desidera rimuovere i movimenti, è possibile farlo nella pagina **Elimina mov. log modifiche**, in cui è possibile impostare filtri in base alle date e all'ora.</span><span class="sxs-lookup"><span data-stu-id="7715f-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="7715f-122">Utilizzare log di attività</span><span class="sxs-lookup"><span data-stu-id="7715f-122">Working with Activity Logs</span></span>

<span data-ttu-id="7715f-123">Da alcune pagine in [!INCLUDE [prodshort](includes/prodshort.md)], è possibile visualizzare un log attività che mostra lo stato e gli eventuali errori nei file esportati da o importati in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="7715f-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="7715f-124">Le informazioni vengono visualizzate nella finestra **Log attività** in base alla pagina di contesto dalla quale viene aperta.</span><span class="sxs-lookup"><span data-stu-id="7715f-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="7715f-125">Ad esempio, è possibile aprire la finestra dalle pagine **Setup servizio di scambio documenti**, **Documento in entrata**, **Fattura vendita registrata** e **Note cr. vendita registrate**.</span><span class="sxs-lookup"><span data-stu-id="7715f-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="7715f-126">È possibile svuotare l'elenco dei movimenti del log o semplicemente cancellare l'elenco dei movimenti più vecchi di 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="7715f-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7715f-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7715f-127">See Also</span></span>
[<span data-ttu-id="7715f-128">Modificare le impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="7715f-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="7715f-129">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="7715f-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="7715f-130">Individuare pagine e informazioni con la funzionalità delle informazioni</span><span class="sxs-lookup"><span data-stu-id="7715f-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="7715f-131">[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="7715f-131">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="7715f-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7715f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
