---
title: Specificare il layout di un assegno| Documenti Microsoft
description: È possibile progettare e stampare gli assegni in modi diversi per conformità agli standard.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243597"
---
# <a name="define-check-layouts"></a><span data-ttu-id="c9f43-103">Definire i layout degli assegni</span><span class="sxs-lookup"><span data-stu-id="c9f43-103">Define Check Layouts</span></span>
<span data-ttu-id="c9f43-104">È possibile progettare i controlli per assicurare la conformità agli standard definiti dalle autorità locali.</span><span class="sxs-lookup"><span data-stu-id="c9f43-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="c9f43-105">Le immagini degli assegni possono essere stampati in inglese, francese, o spagnolo.</span><span class="sxs-lookup"><span data-stu-id="c9f43-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="c9f43-106">Gli assegni sono stati progettati per la stampa dei formati di immagine sia degli Stati Uniti che del Canada con formato assegno-matrice- assegno o matrice-matrice-assegno.</span><span class="sxs-lookup"><span data-stu-id="c9f43-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="c9f43-107">Per definire i layout degli assegni</span><span class="sxs-lookup"><span data-stu-id="c9f43-107">To define check layouts</span></span>
1. <span data-ttu-id="c9f43-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Selezioni report C/C bancari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c9f43-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9f43-109">Nella pagina **Selez. report - C/C bancario**, nel campo **Utilizzo** selezionare **Assegno**.</span><span class="sxs-lookup"><span data-stu-id="c9f43-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="c9f43-110">Selezionare uno dei seguenti ID report:</span><span class="sxs-lookup"><span data-stu-id="c9f43-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="c9f43-111">ID report</span><span class="sxs-lookup"><span data-stu-id="c9f43-111">Report ID</span></span> | <span data-ttu-id="c9f43-112">Nome report</span><span class="sxs-lookup"><span data-stu-id="c9f43-112">Report Name</span></span> | <span data-ttu-id="c9f43-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9f43-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c9f43-114">1401</span><span class="sxs-lookup"><span data-stu-id="c9f43-114">1401</span></span> |<span data-ttu-id="c9f43-115">Seleziona</span><span class="sxs-lookup"><span data-stu-id="c9f43-115">Check</span></span> |<span data-ttu-id="c9f43-116">Questo è il report predefinito.</span><span class="sxs-lookup"><span data-stu-id="c9f43-116">This is the default report.</span></span> |
  | <span data-ttu-id="c9f43-117">10411</span><span class="sxs-lookup"><span data-stu-id="c9f43-117">10411</span></span> |<span data-ttu-id="c9f43-118">Assegno (Matrice/Matrice/Assegno)</span><span class="sxs-lookup"><span data-stu-id="c9f43-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="c9f43-119">Il report è progettato per stampare gli assegni in formato Matrice/Matrice/Assegno.</span><span class="sxs-lookup"><span data-stu-id="c9f43-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="c9f43-120">10412</span><span class="sxs-lookup"><span data-stu-id="c9f43-120">10412</span></span> |<span data-ttu-id="c9f43-121">Assegno (Matrice/Assegno/Matrice)</span><span class="sxs-lookup"><span data-stu-id="c9f43-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="c9f43-122">Il report è progettato per stampare gli assegni in formato Matrice/Assegno/Matrice.</span><span class="sxs-lookup"><span data-stu-id="c9f43-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="c9f43-123">10413</span><span class="sxs-lookup"><span data-stu-id="c9f43-123">10413</span></span> |<span data-ttu-id="c9f43-124">Tre Assegni per pagina</span><span class="sxs-lookup"><span data-stu-id="c9f43-124">Three Checks per Page</span></span> |<span data-ttu-id="c9f43-125">Questo report è progettato per stampare tre assegni su ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="c9f43-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="c9f43-126">Dopo aver impostato i layout dell'asegno, è possibile stampare assegni nella pagina **Registrazioni pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="c9f43-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="c9f43-127">Per ulteriori informazioni, vedere [Utilizzo degli assegni](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="c9f43-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c9f43-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9f43-128">See Also</span></span>
[<span data-ttu-id="c9f43-129">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="c9f43-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="c9f43-130">[Gestione di conti correnti bancari](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="c9f43-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="c9f43-131">Completare i processi di fine periodo</span><span class="sxs-lookup"><span data-stu-id="c9f43-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="c9f43-132">[Utilizzo di [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9f43-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c9f43-133">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="c9f43-133">General Business Functionality</span></span>](ui-across-business-areas.md)
