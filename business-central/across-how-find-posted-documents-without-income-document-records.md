---
title: Cercare i documenti senza allegati| Documenti Microsoft
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b1cf93c93ac9de204fafce1ada3c3e5687cbd682
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="61de4-102">Trovare documenti registrati senza record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="61de4-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="61de4-103">Nelle finestre **Piano dei conti** e **Movimenti C/G** è possibile utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti di vendita e di acquisto registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati.</span><span class="sxs-lookup"><span data-stu-id="61de4-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="61de4-104">Per trovare documenti registrati senza record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="61de4-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="61de4-105">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="61de4-105">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="61de4-106">Selezionare una riga relativa a un conto CO/GE per quei movimenti di contabilità generale di cui si desidera vedere i documenti di vendita e di acquisto registrati senza record di documenti in entrata. Quindi scegliere l'azione **Documenti registrati senza documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="61de4-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="61de4-107">In alternativa, scegliere l'azione **Movimenti contabili**.</span><span class="sxs-lookup"><span data-stu-id="61de4-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="61de4-108">Nella finestra **Movimenti C/G**, scegliere l'azione **Documenti registrati senza documenti in entrata**.</span><span class="sxs-lookup"><span data-stu-id="61de4-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="61de4-109">Viene visualizzata la finestra **Documenti registrati senza documento in entrata** che mostra i documenti di vendita e di acquisto registrati senza i record di documenti in entrata rappresentati dai movimenti di contabilità generale nel conto COGE per il quale è stata aperta la finestra.</span><span class="sxs-lookup"><span data-stu-id="61de4-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="61de4-110">La finestra può visualizzare un massimo di 1.000 righe.</span><span class="sxs-lookup"><span data-stu-id="61de4-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="61de4-111">Per impostazione predefinita, il campo **Filtro data** contiene quindi un filtro che limita la visualizzazione ai movimenti con date di registrazione dall'inizio del periodo contabile alla data del lavoro.</span><span class="sxs-lookup"><span data-stu-id="61de4-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="61de4-112">Per connettere i documenti trovati a record di documento in entrata esistenti</span><span class="sxs-lookup"><span data-stu-id="61de4-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="61de4-113">Nella finestra **Documenti registrati senza documento in entrata** selezionare la riga relativa a un documento registrato che si desidera connettere a un record di documento in entrata esistente, quindi scegliere l'azione **Documenti registrati senza documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="61de4-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="61de4-114">Nella finestra **Documenti in entrata** selezionare il record di documento in entrata che si desidera connettere al documento registrato trovato, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="61de4-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="61de4-115">Nella finestra **Documenti registrati senza documento in entrata**, il record di documento in entrata selezionato è ora connesso al documento registrato, come indicato nel Dettaglio informazioni **File documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="61de4-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="61de4-116">Se nella finestra **Documenti in entrata** non è presente un record di documento in entrata adeguato, è possibile crearlo.</span><span class="sxs-lookup"><span data-stu-id="61de4-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="61de4-117">Per ulteriori informazioni, vedere [Creare i record di documenti in entrata](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="61de4-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="61de4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61de4-118">See Also</span></span>
[<span data-ttu-id="61de4-119">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="61de4-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="61de4-120">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="61de4-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="61de4-121">Acquisti</span><span class="sxs-lookup"><span data-stu-id="61de4-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="61de4-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61de4-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

