---
title: Programmazione dell'esecuzione di un report per una data e un'ora specifiche | Documenti Microsoft
description: Informazioni su come inserire un report in una coda di processi e programmare per l'elaborazione per una data e un'ora specifiche.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, job queue
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0b97a5e48c4b339375ca9ad8cbe8388c5d47bb44
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="schedule-a-report-to-run"></a><span data-ttu-id="a4ae1-103">Programmare l'esecuzione di un report</span><span class="sxs-lookup"><span data-stu-id="a4ae1-103">Schedule a Report to Run</span></span>
<span data-ttu-id="a4ae1-104">È possibile pianificare l'esecuzione di un report per data e orario specifici.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-104">You can schedule a report to run at a specific date and time.</span></span> <span data-ttu-id="a4ae1-105">I report previsti vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-105">Scheduled reports are entered in the job queue and processed at the scheduled time, similar to other jobs.</span></span> <span data-ttu-id="a4ae1-106">È possibile salvare il report elaborato in un file, ad esempio un file Excel, Word, PDF, o stamparlo con una stampante selezionata, o semplicemente elaborare il report.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-106">You can choose to save the processed report to a file, such as an Excel, Word, or PDF, print it to a selected printer, or process the report only.</span></span> <span data-ttu-id="a4ae1-107">Se si sceglie di salvare il report in un file, il report elaborato viene inviato nell'area **Report elaborati** della home page, dove è possibile visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-107">If you choose to save the report to a file, then the processed report is sent to the **Report Inbox** area on your Home page, where you can view it.</span></span>

<span data-ttu-id="a4ae1-108">È possibile programmare un report quando si apre un report.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-108">You can schedule a report when you open a report.</span></span> <span data-ttu-id="a4ae1-109">Scegliere l'azione **Programmazione**, quindi immettere informazioni, come la stampante e la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-109">You choose the **Schedule** action and then you enter information such as printer, and time and date.</span></span> <span data-ttu-id="a4ae1-110">Il report viene aggiunto alla coda processi e sarà eseguito alla data specificata.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-110">The report is then added to the job queue and will be run at the specified time.</span></span> <span data-ttu-id="a4ae1-111">Quando il report viene elaborato, l'elemento verrà rimosso dalla coda commesse.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-111">When the report is processed, the item will be removed from the job queue.</span></span> <span data-ttu-id="a4ae1-112">Se il report elaborato è stato salvato in un file, sarà disponibile nell'area **Report elaborati**.</span><span class="sxs-lookup"><span data-stu-id="a4ae1-112">If you saved the processed report to a file, it will be available in the **Report Inbox** area.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4ae1-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4ae1-113">See Also</span></span>
[<span data-ttu-id="a4ae1-114">Specificare la selezione della stampante per i report</span><span class="sxs-lookup"><span data-stu-id="a4ae1-114">Specify Printer Selection for Reports</span></span>](ui-specify-printer-selection-reports.md)  
<span data-ttu-id="a4ae1-115">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a4ae1-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

