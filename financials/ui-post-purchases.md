---
title: "Informazioni sulle modalità di registrazione dei documenti di acquisto | Documenti Microsoft"
description: Informazioni sulle diverse funzioni di registrazione per i documenti di acquisto.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="posting-purchases"></a><span data-ttu-id="13b56-103">Registrazione di acquisti</span><span class="sxs-lookup"><span data-stu-id="13b56-103">Posting Purchases</span></span>
<span data-ttu-id="13b56-104">Nella **Categoria registrazione** in un documento di acquisto, è possibile scegliere tra le seguenti funzioni di registrazione:</span><span class="sxs-lookup"><span data-stu-id="13b56-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="13b56-105">**Registra**</span><span class="sxs-lookup"><span data-stu-id="13b56-105">**Post**</span></span>
* <span data-ttu-id="13b56-106">**Anteprima registrazione**</span><span class="sxs-lookup"><span data-stu-id="13b56-106">**Preview Posting**</span></span>
* <span data-ttu-id="13b56-107">**Registra e stampa**</span><span class="sxs-lookup"><span data-stu-id="13b56-107">**Post and Print**</span></span>
* <span data-ttu-id="13b56-108">**Report test**</span><span class="sxs-lookup"><span data-stu-id="13b56-108">**Test Report**</span></span>
* <span data-ttu-id="13b56-109">**Registra batch**</span><span class="sxs-lookup"><span data-stu-id="13b56-109">**Post Batch**</span></span>

<span data-ttu-id="13b56-110">Una volta completate le righe e immesse tutte le informazioni nell'ordine di acquisto, è possibile registrarlo, ovvero creare una ricezione e una fattura.</span><span class="sxs-lookup"><span data-stu-id="13b56-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="13b56-111">Quando un ordine di acquisto viene registrato, il conto del fornitore, la contabilità generale e i movimenti contabili articoli vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="13b56-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="13b56-112">Per ciascun ordine di acquisto viene creato un movimento di acquisto nella tabella **Movimenti C/G**.</span><span class="sxs-lookup"><span data-stu-id="13b56-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="13b56-113">Vengono inoltre creati un movimento nel conto del fornitore nella tabella **Mov. contabili fornitori** e un movimento C/G nel relativo conto passività verso il fornitore.</span><span class="sxs-lookup"><span data-stu-id="13b56-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="13b56-114">Infine, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento C/G relativi all'importo dello sconto.</span><span class="sxs-lookup"><span data-stu-id="13b56-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="13b56-115">La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione sconti** della finestra **Setup contabilità fornitori e acquisti**.</span><span class="sxs-lookup"><span data-stu-id="13b56-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="13b56-116">Per ciascuna riga dell'ordine di acquisto, verrà creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di acquisto contengono numeri di articoli) o verrà creato un movimento C/G nella tabella **Movimento C/G** (se le righe di acquisto contengono un conto C/G).</span><span class="sxs-lookup"><span data-stu-id="13b56-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="13b56-117">Inoltre, gli ordini di acquisto vengono sempre registrati nelle tabelle **Testata carico acq.** e **Testate fatt. acq**.</span><span class="sxs-lookup"><span data-stu-id="13b56-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="13b56-118">Prima di avviare la registrazione, è possibile stampare un report di test in cui sono indicate tutte le informazioni contenute nell'ordine di acquisto, insieme a eventuali errori.</span><span class="sxs-lookup"><span data-stu-id="13b56-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="13b56-119">Per stampare il report, scegliere **Registrazione**, quindi **Report test**.</span><span class="sxs-lookup"><span data-stu-id="13b56-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="13b56-120">Quando si registra un ordine, è possibile creare sia un carico che una fattura.</span><span class="sxs-lookup"><span data-stu-id="13b56-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="13b56-121">Ciò può avvenire in modo simultaneo oppure indipendente.</span><span class="sxs-lookup"><span data-stu-id="13b56-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="13b56-122">Prima di effettuare la registrazione, è inoltre possibile creare una ricevuta parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da ricevere** e **Qtà da fatturare** delle singole righe dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="13b56-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="13b56-123">Si tenga presente che non è possibile creare una fattura per un articolo che non è stato ricevuto.</span><span class="sxs-lookup"><span data-stu-id="13b56-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="13b56-124">Questo significa che è necessario registrare una ricezione prima di emettere una fattura oppure la ricezione e la fattura devono essere contemporanee.</span><span class="sxs-lookup"><span data-stu-id="13b56-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="13b56-125">È possibile effettuare la registrazione oppure effettuare la registrazione e stampare.</span><span class="sxs-lookup"><span data-stu-id="13b56-125">You can either post, or post and print.</span></span> <span data-ttu-id="13b56-126">Quando si seleziona Registra e stampa, viene stampato un report al momento della registrazione dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="13b56-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="13b56-127">È inoltre possibile scegliere la funzione **Registra batch** che consente di registrare più ordini contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="13b56-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="13b56-128">Una volta completata la registrazione, le righe di acquisto registrate vengono rimosse dall'ordine.</span><span class="sxs-lookup"><span data-stu-id="13b56-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="13b56-129">Un messaggio avviserà l'utente che la registrazione è completata.</span><span class="sxs-lookup"><span data-stu-id="13b56-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="13b56-130">Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie finestre che contengono movimenti registrati, come ad esempio le finestre **Movimenti contabili fornitori**, **Movimenti C/G**, **Mov. contabili articoli**, **Ricezioni acquisti** e **Fatture acquisto registrate**.</span><span class="sxs-lookup"><span data-stu-id="13b56-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="13b56-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13b56-131">See Also</span></span>
[<span data-ttu-id="13b56-132">Acquisti</span><span class="sxs-lookup"><span data-stu-id="13b56-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="13b56-133">Contabilizzare documenti e registrazioni</span><span class="sxs-lookup"><span data-stu-id="13b56-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="13b56-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13b56-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


