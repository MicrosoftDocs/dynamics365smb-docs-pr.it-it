---
title: Tenere traccia dell'attività dell'utente in un log modifiche| Documenti Microsoft
description: È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc14d11bf75ea39553c1ed04986273903874a0e1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "915432"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="7359b-103">Revisione delle modifiche in Business Central</span><span class="sxs-lookup"><span data-stu-id="7359b-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="7359b-104">È possibile abilitare il log modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo da disporre di uno storico delle attività.</span><span class="sxs-lookup"><span data-stu-id="7359b-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="7359b-105">Il log è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nella pagina **Movimenti log modifiche**, i movimenti vengono ordinati cronologicamente e mostrano le modifiche apportate ai campi nelle tabelle specificate.</span><span class="sxs-lookup"><span data-stu-id="7359b-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="7359b-106">Il log modifiche raccoglie tutte le modifiche apportate alla tabella.</span><span class="sxs-lookup"><span data-stu-id="7359b-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="7359b-107">Le modifiche di un utente non sono visibili in **Movimenti log modifiche** fino al riavvio della sessione dell'utente, che avviene nei seguenti casi:</span><span class="sxs-lookup"><span data-stu-id="7359b-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="7359b-108">La sessione è scaduta ed è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7359b-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="7359b-109">L'utente ha selezionato un'altra società o gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="7359b-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="7359b-110">L'utente si è disconnesso e connesso di nuovo.</span><span class="sxs-lookup"><span data-stu-id="7359b-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="7359b-111">Utilizzo del log modifiche</span><span class="sxs-lookup"><span data-stu-id="7359b-111">Working with the Change Log</span></span>

<span data-ttu-id="7359b-112">Un problema comune in diversi sistemi finanziari è individuare l'origine degli errori e delle modifiche dei dati.</span><span class="sxs-lookup"><span data-stu-id="7359b-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="7359b-113">Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="7359b-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="7359b-114">Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database.</span><span class="sxs-lookup"><span data-stu-id="7359b-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="7359b-115">È necessario specificare cosa si desidera venga registrato per ciascuna tabella e campo, quindi attivare il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="7359b-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="7359b-116">Il log modifiche viene attivato e disattivato nella pagina **Setup log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="7359b-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="7359b-117">Quando un utente attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="7359b-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="7359b-118">Nella pagina **Setup log modifiche** se si sceglie l'azione **Tabelle** è possibile specificare le tabelle di cui si desidera tracciare le modifiche e le modifiche da tracciare. [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene traccia anche di una serie di tabelle di sistema.</span><span class="sxs-lookup"><span data-stu-id="7359b-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="7359b-119">Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella pagina **Movimenti log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="7359b-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="7359b-120">Se si desidera rimuovere i movimenti, è possibile farlo nella pagina **Elimina mov. log modifiche**, in cui è possibile impostare filtri in base alle date e all'ora.</span><span class="sxs-lookup"><span data-stu-id="7359b-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7359b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7359b-121">See Also</span></span>
[<span data-ttu-id="7359b-122">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="7359b-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="7359b-123">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="7359b-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="7359b-124">Utilizzo delle funzionalità di informazioni per trovare funzionalità e informazioni</span><span class="sxs-lookup"><span data-stu-id="7359b-124">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="7359b-125">[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="7359b-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="7359b-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7359b-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
