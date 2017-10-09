---
title: Specificare il layout di un assegno| Documenti Microsoft
description: "È possibile progettare e stampare gli assegni in modi diversi per conformità agli standard."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="af1de-103">Procedura: Definire i layout degli assegni</span><span class="sxs-lookup"><span data-stu-id="af1de-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="af1de-104">È possibile progettare i controlli per assicurare la conformità agli standard definiti dalle autorità locali.</span><span class="sxs-lookup"><span data-stu-id="af1de-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="af1de-105">Le immagini degli assegni possono essere stampati in inglese, francese, o spagnolo.</span><span class="sxs-lookup"><span data-stu-id="af1de-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="af1de-106">Gli assegni sono stati progettati per la stampa dei formati di immagine sia degli Stati Uniti che del Canada con formato assegno-matrice- assegno o matrice-matrice-assegno.</span><span class="sxs-lookup"><span data-stu-id="af1de-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="af1de-107">Per definire i layout degli assegni</span><span class="sxs-lookup"><span data-stu-id="af1de-107">To define check layouts</span></span>
1. <span data-ttu-id="af1de-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Selezioni report C/C bancari**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="af1de-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="af1de-109">Nella finestra **Selez. report - C/C bancario**, nel campo **Utilizzo** selezionare **Assegno**.</span><span class="sxs-lookup"><span data-stu-id="af1de-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="af1de-110">Selezionare uno dei seguenti ID report:</span><span class="sxs-lookup"><span data-stu-id="af1de-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="af1de-111">ID report</span><span class="sxs-lookup"><span data-stu-id="af1de-111">Report ID</span></span> | <span data-ttu-id="af1de-112">Nome report</span><span class="sxs-lookup"><span data-stu-id="af1de-112">Report Name</span></span> | <span data-ttu-id="af1de-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af1de-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="af1de-114">1401</span><span class="sxs-lookup"><span data-stu-id="af1de-114">1401</span></span> |<span data-ttu-id="af1de-115">Seleziona</span><span class="sxs-lookup"><span data-stu-id="af1de-115">Check</span></span> |<span data-ttu-id="af1de-116">Questo è il report predefinito.</span><span class="sxs-lookup"><span data-stu-id="af1de-116">This is the default report.</span></span> |
| <span data-ttu-id="af1de-117">10401</span><span class="sxs-lookup"><span data-stu-id="af1de-117">10401</span></span> |<span data-ttu-id="af1de-118">Assegno (Matrice/Matrice/Assegno)</span><span class="sxs-lookup"><span data-stu-id="af1de-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="af1de-119">Il report è progettato per stampare gli assegni in formato Matrice/Matrice/Assegno.</span><span class="sxs-lookup"><span data-stu-id="af1de-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="af1de-120">10411</span><span class="sxs-lookup"><span data-stu-id="af1de-120">10411</span></span> |<span data-ttu-id="af1de-121">Assegno (Matrice/Assegno/Matrice)</span><span class="sxs-lookup"><span data-stu-id="af1de-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="af1de-122">Il report è progettato per stampare gli assegni in formato Matrice/Assegno/Matrice.</span><span class="sxs-lookup"><span data-stu-id="af1de-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="af1de-123">Dopo aver impostato i layout dell'asegno, è possibile stampare assegni nella finestra **Registrazioni pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="af1de-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="af1de-124">Per ulteriori informazioni, vedere [Procedura: Utilizzo degli assegni](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="af1de-124">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="af1de-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af1de-125">See Also</span></span>
[<span data-ttu-id="af1de-126">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="af1de-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="af1de-127">[Gestione di conti correnti bancari](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="af1de-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="af1de-128">Completare i processi di fine periodo</span><span class="sxs-lookup"><span data-stu-id="af1de-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="af1de-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af1de-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="af1de-130">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="af1de-130">General Business Functionality</span></span>](ui-across-business-areas.md)

