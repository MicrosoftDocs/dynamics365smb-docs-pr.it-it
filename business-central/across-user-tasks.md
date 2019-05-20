---
title: Assegnazione e gestione di task | Documenti Microsoft
description: Ottenere informazioni su come assegnare task agli utenti, incluso il proprio contabile, in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 5befadf7a162cc2094fbb1ef426e25d02d50e856
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241170"
---
# <a name="define-user-tasks"></a><span data-ttu-id="36915-103">Definisci task dell'utente</span><span class="sxs-lookup"><span data-stu-id="36915-103">Define User Tasks</span></span>
<span data-ttu-id="36915-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile creare task per ricordare le attività da svolgere.</span><span class="sxs-lookup"><span data-stu-id="36915-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="36915-105">È possibile creare task per se stessi, ma è anche possibile assegnarli ad altri utenti o che un'altra persona nell'organizzazione assegni un task all'utente.</span><span class="sxs-lookup"><span data-stu-id="36915-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="36915-106">Gestione dei task degli utenti</span><span class="sxs-lookup"><span data-stu-id="36915-106">Managing User Tasks</span></span>
<span data-ttu-id="36915-107">La pagina **Task dell'utente** mostra tutti i task e consente di creare e assegnare facilmente nuovi task.</span><span class="sxs-lookup"><span data-stu-id="36915-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="36915-108">Quando si crea un task, è possibile specificare la data di inizio e di fine e aggiungere un collegamento alla pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] in cui l'utente deve svolgere l'attività.</span><span class="sxs-lookup"><span data-stu-id="36915-108">When you create a task, you can specify the start date and due date, and you can add a link to the page in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="36915-109">Ad esempio, è possibile creare un task per se stessi per visualizzare tutte le fatture di vendita registrate.</span><span class="sxs-lookup"><span data-stu-id="36915-109">For example, you can create a task for yourself to view all posted sales invoices.</span></span> <span data-ttu-id="36915-110">In tal caso, collegare il task alla pagina 143, Fatture di vendita registrate.</span><span class="sxs-lookup"><span data-stu-id="36915-110">In that case, you link the task to page 143, Posted Sales Invoices.</span></span>  

<span data-ttu-id="36915-111">![Esempio di un task dell'utente](media/across-user-tasks/sample-user-task.png "Esempio di un task dell'utente")</span><span class="sxs-lookup"><span data-stu-id="36915-111">![Example of a User Task](media/across-user-tasks/sample-user-task.png "Example of a user task")</span></span>

> [!TIP]  
>  <span data-ttu-id="36915-112">Utilizzare la funzionalità di ricerca nel campo **Pagina**, quindi utilizzare il campo **Cerca pagina o report** per identificare la pagina che si desidera.</span><span class="sxs-lookup"><span data-stu-id="36915-112">Use the look-up in the **Page** field and then use the **Search for Page or Report** field to find the page that you want.</span></span> <span data-ttu-id="36915-113">Per ulteriori informazioni, vedere [Ricerca di una pagina o di un report](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="36915-113">For more information, see [Searching for a Page or Report](ui-search.md).</span></span>  

### <a name="picking-up-user-tasks"></a><span data-ttu-id="36915-114">Selezione dei task degli utenti</span><span class="sxs-lookup"><span data-stu-id="36915-114">Picking Up User Tasks</span></span>
<span data-ttu-id="36915-115">Nelle Gestioni ruolo utente di Manager aziendale, Contabile e Addetto contabile, un riquadro mostra i task in sospeso assegnati all'utente.</span><span class="sxs-lookup"><span data-stu-id="36915-115">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="36915-116">Per selezionare un task, sceglierlo dall'elenco dei task in sospeso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="36915-116">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="36915-117">Nella barra multifunzione, il collegamento **Vai a elemento task** apre la pagina in cui è possibile svolgere l'attività.</span><span class="sxs-lookup"><span data-stu-id="36915-117">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="36915-118">Una volta completato il task, contrassegnarlo come completato.</span><span class="sxs-lookup"><span data-stu-id="36915-118">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="36915-119">Eliminazione di task degli utenti</span><span class="sxs-lookup"><span data-stu-id="36915-119">Deleting User Tasks</span></span>
<span data-ttu-id="36915-120">Se si desidera eliminare tutti o alcuni task dell'utente, è possibile utilizzare il report **Elimina task dell'utente**.</span><span class="sxs-lookup"><span data-stu-id="36915-120">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="36915-121">Nella pagina di richiesta, è possibile impostare i filtri per determinare quali task devono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="36915-121">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="36915-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36915-122">See Also</span></span>
[<span data-ttu-id="36915-123">Ricerca di una pagina o di un report</span><span class="sxs-lookup"><span data-stu-id="36915-123">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="36915-124">[Esperienze di contabile in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="36915-124">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  
