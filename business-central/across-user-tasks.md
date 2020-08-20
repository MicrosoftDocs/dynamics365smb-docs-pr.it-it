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
ms.date: 07/14/2020
ms.author: edupont
ms.openlocfilehash: e1e6520aeb39a77ecfcbf652b8c328d1595d6f6f
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577203"
---
# <a name="define-user-tasks"></a><span data-ttu-id="1e363-103">Definisci task dell'utente</span><span class="sxs-lookup"><span data-stu-id="1e363-103">Define User Tasks</span></span>

<span data-ttu-id="1e363-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile creare task per ricordare le attività da svolgere.</span><span class="sxs-lookup"><span data-stu-id="1e363-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="1e363-105">È possibile creare task per se stessi, ma è anche possibile assegnarli ad altri utenti o che un'altra persona nell'organizzazione assegni un task all'utente.</span><span class="sxs-lookup"><span data-stu-id="1e363-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="1e363-106">Gestione dei task degli utenti</span><span class="sxs-lookup"><span data-stu-id="1e363-106">Managing User Tasks</span></span>

<span data-ttu-id="1e363-107">La pagina **Task dell'utente** mostra tutti i task e consente di creare e assegnare facilmente nuovi task.</span><span class="sxs-lookup"><span data-stu-id="1e363-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="1e363-108">Quando si crea un task, è possibile specificare la data di inizio e di fine e aggiungere un collegamento alla pagina o al report in [!INCLUDE[d365fin](includes/d365fin_md.md)] in cui l'utente deve svolgere l'attività.</span><span class="sxs-lookup"><span data-stu-id="1e363-108">When you create a task, you can specify the start date and due date, and you can add a link to the page or report in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="1e363-109">Ad esempio, è possibile creare un task per se stessi o un collaboratore per visualizzare tutte le fatture di vendita registrate.</span><span class="sxs-lookup"><span data-stu-id="1e363-109">For example, you can create a task for yourself or a coworker to view all posted sales invoices.</span></span> <span data-ttu-id="1e363-110">In tal caso, collegare il task alla pagina 143, **Fatture di vendita registrate**.</span><span class="sxs-lookup"><span data-stu-id="1e363-110">In that case, you link the task to page 143, **Posted Sales Invoices**.</span></span> <span data-ttu-id="1e363-111">Nello screenshot seguente, qualcuno sta creando un'attività per MeganB per rivedere le fatture di vendita registrate.</span><span class="sxs-lookup"><span data-stu-id="1e363-111">In the following screenshot, someone is creating a task for MeganB to review the posted sales invoices.</span></span>  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Esempio di un'attività utente":::

> [!TIP]  
> <span data-ttu-id="1e363-113">Utilizzare la funzionalità di ricerca nel campo **Pagina**, quindi utilizzare il campo **Cerca** per identificare la pagina che si desidera.</span><span class="sxs-lookup"><span data-stu-id="1e363-113">Use the look-up in the **Page** field and then use the **Search** field to find the page that you want.</span></span>  
>
> <span data-ttu-id="1e363-114">È possibile collegare a qualsiasi pagina, ma non è possibile collegare singole voci, quindi rendere la descrizione il più esplicita possibile, ad esempio scrivendo "Osservare il cliente n.</span><span class="sxs-lookup"><span data-stu-id="1e363-114">You can link to any page, but you cannot link to individual entries, so make the description as explicit as possible, such as writing "Please take a look at customer no.</span></span> <span data-ttu-id="1e363-115">10000 e assicurarsi che non abbia pagamenti scaduti.".</span><span class="sxs-lookup"><span data-stu-id="1e363-115">10000 and make sure they don't have overdue payments.".</span></span>

### <a name="picking-up-user-tasks"></a><span data-ttu-id="1e363-116">Selezione dei task degli utenti</span><span class="sxs-lookup"><span data-stu-id="1e363-116">Picking Up User Tasks</span></span>

<span data-ttu-id="1e363-117">Nelle Gestioni ruolo utente di Manager aziendale, Contabile e Addetto contabile, un riquadro mostra i task in sospeso assegnati all'utente.</span><span class="sxs-lookup"><span data-stu-id="1e363-117">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="1e363-118">Per selezionare un task, sceglierlo dall'elenco dei task in sospeso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1e363-118">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="1e363-119">Nella barra multifunzione, il collegamento **Vai a elemento task** apre la pagina in cui è possibile svolgere l'attività.</span><span class="sxs-lookup"><span data-stu-id="1e363-119">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="1e363-120">Una volta completato il task, contrassegnarlo come completato.</span><span class="sxs-lookup"><span data-stu-id="1e363-120">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="1e363-121">Eliminazione di task degli utenti</span><span class="sxs-lookup"><span data-stu-id="1e363-121">Deleting User Tasks</span></span>

<span data-ttu-id="1e363-122">Se si desidera eliminare tutti o alcuni task dell'utente, è possibile utilizzare il report **Elimina task dell'utente**.</span><span class="sxs-lookup"><span data-stu-id="1e363-122">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="1e363-123">Nella pagina di richiesta, è possibile impostare i filtri per determinare quali task devono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="1e363-123">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e363-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e363-124">See Also</span></span>

[<span data-ttu-id="1e363-125">Ricerca di una pagina o di un report</span><span class="sxs-lookup"><span data-stu-id="1e363-125">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="1e363-126">[Esperienze di contabile in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="1e363-126">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  
