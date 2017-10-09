---
title: Creare ed eseguire un processo batch | Documenti Microsoft
description: "È possibile eseguire i processi batch per elaborare i dati e aggiornare le informazioni, ad esempio, per attività contabili periodiche oppure per effettuare dei calcoli."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6844d5fe3efba5349eef166161c5956116bc7fc0
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-run-batch-jobs"></a><span data-ttu-id="c9c51-103">Procedura: Eseguire i processi batch</span><span class="sxs-lookup"><span data-stu-id="c9c51-103">How to: Run Batch Jobs</span></span>
<span data-ttu-id="c9c51-104">Un processo batch è una routine che elabora i dati in batch, come, ad esempio, il processo **Rettifica tassi di cambio**.</span><span class="sxs-lookup"><span data-stu-id="c9c51-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="c9c51-105">Alcuni processi batch eseguono attività contabili periodiche, ad esempio la chiusura del conto economico alla fine di un anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="c9c51-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="c9c51-106">Molti processi batch eseguono attività di calcolo, ad esempio il calcolo degli interessi finanziari, la rettifica dei tassi di cambio e il calcolo dei prezzi unitari.</span><span class="sxs-lookup"><span data-stu-id="c9c51-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="c9c51-107">Un processo batch è simile a un report, con la differenza che il processo batch utilizza il risultato delle attività che esegue per aggiornare direttamente le informazioni, anziché stampare i risultati.</span><span class="sxs-lookup"><span data-stu-id="c9c51-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="c9c51-108">Per eseguire un processo batch</span><span class="sxs-lookup"><span data-stu-id="c9c51-108">To run a batch job</span></span>
1. <span data-ttu-id="c9c51-109">Per aprire la finestra di richiesta del processo batch pertinente, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere il nome del processo batch, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c9c51-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="c9c51-110">Se per il processo batch è disponibile una Scheda dettaglio **Opzioni**, completarne i campi per determinare l'operazione che sarà eseguita dal processo batch.</span><span class="sxs-lookup"><span data-stu-id="c9c51-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="c9c51-111">È possibile che la finestra contenga una o più Schede dettaglio con filtri, che è possibile utilizzare per limitare i dati inclusi nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="c9c51-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="c9c51-112">È possibile immettere criteri nei filtri consigliati o aggiungere altri filtri.</span><span class="sxs-lookup"><span data-stu-id="c9c51-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="c9c51-113">Scegliere **OK** per avviare il processo batch.</span><span class="sxs-lookup"><span data-stu-id="c9c51-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9c51-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9c51-114">See Also</span></span>
[<span data-ttu-id="c9c51-115">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="c9c51-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="c9c51-116">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9c51-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

