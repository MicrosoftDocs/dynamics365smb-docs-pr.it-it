---
title: "Tenere traccia dell'attività dell'utente in un log modifiche| Documenti Microsoft"
Description: "È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="logging-changes-in-dynamics-365-for-financials"></a><span data-ttu-id="be52c-103">Registrazione di modifiche in Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="be52c-103">Logging Changes in Dynamics 365 for Financials</span></span>
<span data-ttu-id="be52c-104">È possibile abilitare il log modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo da disporre di uno storico delle attività.</span><span class="sxs-lookup"><span data-stu-id="be52c-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="be52c-105">Il log è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nel log modifiche, i movimenti vengono ordinati cronologicamente e mostrano le modifiche apportate ai campi nelle tabelle specificate.</span><span class="sxs-lookup"><span data-stu-id="be52c-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="be52c-106">Il log modifiche raccoglie tutte le modifiche apportate alla tabella.</span><span class="sxs-lookup"><span data-stu-id="be52c-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="be52c-107">Utilizzo del log modifiche</span><span class="sxs-lookup"><span data-stu-id="be52c-107">Working with the change log</span></span>
<span data-ttu-id="be52c-108">Un problema comune in diversi sistemi finanziari è individuare l'origine degli errori e delle modifiche dei dati.</span><span class="sxs-lookup"><span data-stu-id="be52c-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="be52c-109">Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="be52c-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="be52c-110">Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database.</span><span class="sxs-lookup"><span data-stu-id="be52c-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="be52c-111">È necessario specificare cosa si desidera venga registrato per ciascuna tabella e campo, quindi attivare il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="be52c-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="be52c-112">Il log modifiche viene attivato e disattivato nella finestra **Setup log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="be52c-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="be52c-113">Quando si attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="be52c-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="be52c-114">Non è possibile disattivare tale funzione.</span><span class="sxs-lookup"><span data-stu-id="be52c-114">This cannot be turned off.</span></span>  

<span data-ttu-id="be52c-115">Nella finestra **Setup log modifiche** se si sceglie l'azione **Tabelle** è possibile specificare le tabelle di cui si desidera tracciare le modifiche e le modifiche da tracciare. [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene traccia anche di una serie di tabelle di sistema.</span><span class="sxs-lookup"><span data-stu-id="be52c-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="be52c-116">Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella finestra **Movimenti log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="be52c-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="be52c-117">Se si desidera rimuovere i movimenti, è possibile farlo nella finestra **Elimina mov. log modifiche**, in cui è possibile impostare filtri in base alle date e all'ora.</span><span class="sxs-lookup"><span data-stu-id="be52c-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be52c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be52c-118">See Also</span></span>
[<span data-ttu-id="be52c-119">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="be52c-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="be52c-120">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="be52c-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="be52c-121">Utilizzo della funzionalità Cerca pagina o report</span><span class="sxs-lookup"><span data-stu-id="be52c-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="be52c-122">[Procedura: Gestire gli utenti e le autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="be52c-122">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="be52c-123">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be52c-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

