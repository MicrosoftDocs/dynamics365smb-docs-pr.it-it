---
title: Creare ed eseguire un processo batch | Documenti Microsoft
description: "È possibile eseguire i processi batch per elaborare i dati e aggiornare le informazioni, ad esempio, per attività contabili periodiche oppure per effettuare dei calcoli."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9a6435120d122db894bcd6c953da5ab8ea78420b
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="run-batch-jobs"></a><span data-ttu-id="f4bd8-103">Eseguire i processi batch</span><span class="sxs-lookup"><span data-stu-id="f4bd8-103">Run Batch Jobs</span></span>
<span data-ttu-id="f4bd8-104">Un processo batch è una routine che elabora i dati in batch, come, ad esempio, il processo **Rettifica tassi di cambio**.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="f4bd8-105">Alcuni processi batch eseguono attività contabili periodiche, ad esempio la chiusura del conto economico alla fine di un anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="f4bd8-106">Molti processi batch eseguono attività di calcolo, ad esempio il calcolo degli interessi finanziari, la rettifica dei tassi di cambio e il calcolo dei prezzi unitari.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="f4bd8-107">Un processo batch è simile a un report, con la differenza che il processo batch utilizza il risultato delle attività che esegue per aggiornare direttamente le informazioni, anziché stampare i risultati.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="f4bd8-108">Per eseguire un processo batch</span><span class="sxs-lookup"><span data-stu-id="f4bd8-108">To run a batch job</span></span>
1. <span data-ttu-id="f4bd8-109">Per aprire la finestra di richiesta del processo batch pertinente, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere il nome del processo batch e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-109">To open the request window for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="f4bd8-110">Se per il processo batch è disponibile una Scheda dettaglio **Opzioni**, completarne i campi per determinare l'operazione che sarà eseguita dal processo batch.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="f4bd8-111">È possibile che la finestra contenga una o più Schede dettaglio con filtri, che è possibile utilizzare per limitare i dati inclusi nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="f4bd8-112">È possibile immettere criteri nei filtri consigliati o aggiungere altri filtri.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="f4bd8-113">Scegliere **OK** per avviare il processo batch.</span><span class="sxs-lookup"><span data-stu-id="f4bd8-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4bd8-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4bd8-114">See Also</span></span>
[<span data-ttu-id="f4bd8-115">Ricerca, filtro e ordinamento di dati</span><span class="sxs-lookup"><span data-stu-id="f4bd8-115">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="f4bd8-116">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f4bd8-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

