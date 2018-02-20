---
title: "Tenere traccia dell'attività dell'utente in un log modifiche| Documenti Microsoft"
Description: You can activate a user log so that you have a history of any changes made to data in tracked tables.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f49e3722f95d4e5a2c8eea83d77175581d93277
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="logging-changes-in-finance-and-operations-business-edition"></a><span data-ttu-id="e4f44-102">Registrazione delle modifiche in Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="e4f44-102">Logging Changes in Finance and Operations, Business edition</span></span> 
<span data-ttu-id="e4f44-103">È possibile abilitare il log modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo da disporre di uno storico delle attività.</span><span class="sxs-lookup"><span data-stu-id="e4f44-103">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="e4f44-104">Il log è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nel log modifiche, i movimenti vengono ordinati cronologicamente e mostrano le modifiche apportate ai campi nelle tabelle specificate.</span><span class="sxs-lookup"><span data-stu-id="e4f44-104">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="e4f44-105">Il log modifiche raccoglie tutte le modifiche apportate alla tabella.</span><span class="sxs-lookup"><span data-stu-id="e4f44-105">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="e4f44-106">Utilizzo del log modifiche</span><span class="sxs-lookup"><span data-stu-id="e4f44-106">Working with the Change Log</span></span>
<span data-ttu-id="e4f44-107">Un problema comune in diversi sistemi finanziari è individuare l'origine degli errori e delle modifiche dei dati.</span><span class="sxs-lookup"><span data-stu-id="e4f44-107">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="e4f44-108">Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e4f44-108">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="e4f44-109">Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database.</span><span class="sxs-lookup"><span data-stu-id="e4f44-109">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="e4f44-110">È necessario specificare cosa si desidera venga registrato per ciascuna tabella e campo, quindi attivare il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="e4f44-110">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="e4f44-111">Il log modifiche viene attivato e disattivato nella finestra **Setup log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="e4f44-111">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="e4f44-112">Quando si attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche.</span><span class="sxs-lookup"><span data-stu-id="e4f44-112">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="e4f44-113">Non è possibile disattivare tale funzione.</span><span class="sxs-lookup"><span data-stu-id="e4f44-113">This cannot be turned off.</span></span>  

<span data-ttu-id="e4f44-114">Nella finestra **Setup log modifiche** se si sceglie l'azione **Tabelle** è possibile specificare le tabelle di cui si desidera tracciare le modifiche e le modifiche da tracciare. [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene traccia anche di una serie di tabelle di sistema.</span><span class="sxs-lookup"><span data-stu-id="e4f44-114">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="e4f44-115">Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella finestra **Movimenti log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="e4f44-115">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="e4f44-116">Se si desidera rimuovere i movimenti, è possibile farlo nella finestra **Elimina mov. log modifiche**, in cui è possibile impostare filtri in base alle date e all'ora.</span><span class="sxs-lookup"><span data-stu-id="e4f44-116">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4f44-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4f44-117">See Also</span></span>
[<span data-ttu-id="e4f44-118">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="e4f44-118">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="e4f44-119">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="e4f44-119">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="e4f44-120">Utilizzo della funzionalità Cerca pagina o report</span><span class="sxs-lookup"><span data-stu-id="e4f44-120">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="e4f44-121">[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="e4f44-121">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="e4f44-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4f44-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

