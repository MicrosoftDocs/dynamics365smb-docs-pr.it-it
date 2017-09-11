---
title: Cercare i documenti senza allegati| Documenti Microsoft
Description: "È possibile cercare i movimenti di contabilità generale per i documenti di vendita e di acquisto registrati che non presentano documenti elettronici in entrata, quali fatture importate."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 263146eca72e4c83b4ad6887a84844e7aa15dd87
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="0a2b2-103">Procedura: Trovare documenti registrati senza record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="0a2b2-103">How to: Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="0a2b2-104">Nelle finestre **Piano dei conti** e **Movimenti C/G** è possibile utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti di vendita e di acquisto registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-104">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="0a2b2-105">Per trovare documenti registrati senza record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="0a2b2-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="0a2b2-106">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a2b2-107">Selezionare una riga relativa a un conto CO/GE per quei movimenti di contabilità generale di cui si desidera vedere i documenti di vendita e di acquisto registrati senza record di documenti in entrata. Quindi scegliere l'azione **Documenti registrati senza documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="0a2b2-108">In alternativa, scegliere l'azione **Movimenti contabili**.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="0a2b2-109">Nella finestra **Movimenti C/G**, scegliere l'azione **Documenti registrati senza documenti in entrata**.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-109">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="0a2b2-110">Viene visualizzata la finestra **Documenti registrati senza documento in entrata** che mostra i documenti di vendita e di acquisto registrati senza i record di documenti in entrata rappresentati dai movimenti di contabilità generale nel conto COGE per il quale è stata aperta la finestra.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-110">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="0a2b2-111">La finestra può visualizzare un massimo di 1.000 righe.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-111">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="0a2b2-112">Per impostazione predefinita, il campo **Filtro data** contiene quindi un filtro che limita la visualizzazione ai movimenti con date di registrazione dall'inizio del periodo contabile alla data del lavoro.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="0a2b2-113">Per connettere i documenti trovati a record di documento in entrata esistenti</span><span class="sxs-lookup"><span data-stu-id="0a2b2-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="0a2b2-114">Nella finestra **Documenti registrati senza documento in entrata** selezionare la riga relativa a un documento registrato che si desidera connettere a un record di documento in entrata esistente, quindi scegliere l'azione **Documenti registrati senza documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-114">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="0a2b2-115">Nella finestra **Documenti in entrata** selezionare il record di documento in entrata che si desidera connettere al documento registrato trovato, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-115">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="0a2b2-116">Nella finestra **Documenti registrati senza documento in entrata**, il record di documento in entrata selezionato è ora connesso al documento registrato, come indicato nel Dettaglio informazioni **File documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-116">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="0a2b2-117">Se nella finestra **Documenti in entrata** non è presente un record di documento in entrata adeguato, è possibile crearlo.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-117">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="0a2b2-118">Per ulteriori informazioni, vedere [Procedura: Creare i record di documenti in entrata](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="0a2b2-118">For more information, see [How to: Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0a2b2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a2b2-119">See Also</span></span>
[<span data-ttu-id="0a2b2-120">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="0a2b2-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="0a2b2-121">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="0a2b2-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="0a2b2-122">Acquisti</span><span class="sxs-lookup"><span data-stu-id="0a2b2-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0a2b2-123">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a2b2-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

