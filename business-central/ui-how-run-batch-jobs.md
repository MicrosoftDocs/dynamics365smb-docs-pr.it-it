---
title: Creare ed eseguire un processo batch | Documenti Microsoft
description: È possibile eseguire i processi batch per elaborare i dati e aggiornare le informazioni, ad esempio, per attività contabili periodiche oppure per effettuare dei calcoli.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 05b65f5b001259fff25d0f59dfc6267d9ee00c7f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782255"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="bc366-103">Eseguire processi batch e XMLports</span><span class="sxs-lookup"><span data-stu-id="bc366-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="bc366-104">Un processo batch è una routine che elabora i dati in batch, come, ad esempio, il processo **Rettifica tassi di cambio**.</span><span class="sxs-lookup"><span data-stu-id="bc366-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="bc366-105">Alcuni processi batch eseguono attività contabili periodiche, ad esempio la chiusura del conto economico alla fine di un anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="bc366-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="bc366-106">Molti processi batch eseguono attività di calcolo, ad esempio il calcolo degli interessi finanziari, la rettifica dei tassi di cambio e il calcolo dei prezzi unitari.</span><span class="sxs-lookup"><span data-stu-id="bc366-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="bc366-107">Un processo batch è simile a un report, con la differenza che il processo batch utilizza il risultato delle attività che esegue per aggiornare direttamente le informazioni, anziché stampare i risultati.</span><span class="sxs-lookup"><span data-stu-id="bc366-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="bc366-108">È possibile pianificare l'esecuzione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="bc366-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="bc366-109">Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="bc366-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="bc366-110">Per eseguire un processo batch</span><span class="sxs-lookup"><span data-stu-id="bc366-110">To run a batch job</span></span>
1. <span data-ttu-id="bc366-111">Per aprire la pagina di richiesta del processo batch pertinente, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere il nome del processo batch e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bc366-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="bc366-112">Se per il processo batch è disponibile una Scheda dettaglio **Opzioni**, completarne i campi per determinare l'operazione che sarà eseguita dal processo batch.</span><span class="sxs-lookup"><span data-stu-id="bc366-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="bc366-113">È possibile che la pagina contenga una o più Schede dettaglio con filtri, che è possibile utilizzare per limitare i dati inclusi nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="bc366-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="bc366-114">È possibile immettere criteri nei filtri consigliati o aggiungere altri filtri.</span><span class="sxs-lookup"><span data-stu-id="bc366-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="bc366-115">Scegliere **OK** per avviare il processo batch.</span><span class="sxs-lookup"><span data-stu-id="bc366-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc366-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bc366-116">See Also</span></span>
[<span data-ttu-id="bc366-117">Ricerca, filtro e ordinamento di elenchi</span><span class="sxs-lookup"><span data-stu-id="bc366-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="bc366-118">Utilizzare le code processi per pianificare le attività</span><span class="sxs-lookup"><span data-stu-id="bc366-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="bc366-119">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc366-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]