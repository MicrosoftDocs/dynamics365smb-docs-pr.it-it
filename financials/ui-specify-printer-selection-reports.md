---
title: Impostare report da stampare su stampanti specifiche | Documenti Microsoft
description: Informazioni su come specificare una stampante per un report utilizzando la finestra Selezioni stampante.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9612d1b0859639bf25713dd8bcfbebdaacd3517e
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="dc5b3-103">Specificare la selezione della stampante per i report</span><span class="sxs-lookup"><span data-stu-id="dc5b3-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="dc5b3-104">Questa pagina è vuota perché non è ancora possibile impostare stampanti specifiche per report specifici.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="dc5b3-105">Stiamo lavorando per trovare una soluzione.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-105">We are working on solving this.</span></span>

<span data-ttu-id="dc5b3-106">Nel frattempo, quando si desidera stampare un report, è necessario scaricarlo come documento PDF prima di tutto scegliendo il pulsante **Invia a**.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-106">In the meantime, when you want to print a report, you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="dc5b3-107">Selezionare quindi il tipo di file in cui il report deve essere scaricato e scegliere **Documento PDF**.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="dc5b3-108">A questo punto è possibile aprire il documento PDF immediatamente e stamparlo oppure salvarlo e stamparlo in seguito.</span><span class="sxs-lookup"><span data-stu-id="dc5b3-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a><span data-ttu-id="dc5b3-109">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc5b3-109">See Also</span></span>
<span data-ttu-id="dc5b3-110">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dc5b3-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="dc5b3-111">Eseguire i processi batch</span><span class="sxs-lookup"><span data-stu-id="dc5b3-111">Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="dc5b3-112">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="dc5b3-112">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  

