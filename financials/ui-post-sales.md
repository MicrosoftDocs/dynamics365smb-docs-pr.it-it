---
title: "Informazioni sulle modalità di registrazione dei documenti vendita | Documenti Microsoft"
description: Informazioni sulle diverse funzioni di registrazione per i documenti di vendita.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f0ba4e8bb0770f612594e6af8a47838852a3d25
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="posting-sales"></a><span data-ttu-id="b8dee-103">Registrazione di vendite</span><span class="sxs-lookup"><span data-stu-id="b8dee-103">Posting Sales</span></span>
<span data-ttu-id="b8dee-104">Nella **Categoria registrazione** in un documento di vendita, è possibile scegliere tra le seguenti funzioni di registrazione:</span><span class="sxs-lookup"><span data-stu-id="b8dee-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="b8dee-105">**Registra**</span><span class="sxs-lookup"><span data-stu-id="b8dee-105">**Post**</span></span>
* <span data-ttu-id="b8dee-106">**Report test**</span><span class="sxs-lookup"><span data-stu-id="b8dee-106">**Test Report**</span></span>
* <span data-ttu-id="b8dee-107">**Registra e invia**</span><span class="sxs-lookup"><span data-stu-id="b8dee-107">**Post and Send**</span></span>
* <span data-ttu-id="b8dee-108">**Registra e stampa**</span><span class="sxs-lookup"><span data-stu-id="b8dee-108">**Post and Print**</span></span>
* <span data-ttu-id="b8dee-109">**Registra e invia tramite e-mail**</span><span class="sxs-lookup"><span data-stu-id="b8dee-109">**Post and Email**</span></span>
* <span data-ttu-id="b8dee-110">**Registra batch**</span><span class="sxs-lookup"><span data-stu-id="b8dee-110">**Post Batch**</span></span>
* <span data-ttu-id="b8dee-111">**Anteprima registrazione**</span><span class="sxs-lookup"><span data-stu-id="b8dee-111">**Preview Posting**</span></span>

<span data-ttu-id="b8dee-112">Una volta completate le righe e immesse tutte le informazioni nell'ordine di vendita, è possibile registrarlo.</span><span class="sxs-lookup"><span data-stu-id="b8dee-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="b8dee-113">Vengono create una spedizione e una fattura.</span><span class="sxs-lookup"><span data-stu-id="b8dee-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="b8dee-114">Quando un ordine di acquisto viene registrato, il conto del cliente, la contabilità generale e i movimenti contabili articoli vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="b8dee-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="b8dee-115">Per ciascun ordine di vendita viene creato un movimento di vendita nella tabella **Movimenti C/G**.</span><span class="sxs-lookup"><span data-stu-id="b8dee-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="b8dee-116">Vengono inoltre creati un movimento nel conto del cliente nella tabella **Mov. contabili clienti** e un movimento C/G nel relativo conto crediti.</span><span class="sxs-lookup"><span data-stu-id="b8dee-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="b8dee-117">Infine, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento di contabilità generale relativi all'importo dello sconto.</span><span class="sxs-lookup"><span data-stu-id="b8dee-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="b8dee-118">La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione sconti** della finestra **Setup contabilità clienti e vendite**.</span><span class="sxs-lookup"><span data-stu-id="b8dee-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="b8dee-119">Per ciascuna riga dell'ordine di vendita, verrà creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di vendita contengono numeri di articolo) oppure un movimento C/G nella tabella **Movimenti C/G** (se le righe di vendita contengono un conto C/G).</span><span class="sxs-lookup"><span data-stu-id="b8dee-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="b8dee-120">Inoltre, gli ordini vendita vengono sempre registrati nelle tabelle **Testate sped. vendita** e **Testate Fatt. Vendita**.</span><span class="sxs-lookup"><span data-stu-id="b8dee-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="b8dee-121">Quando si registra un ordine, è possibile creare sia una spedizione che una fattura.</span><span class="sxs-lookup"><span data-stu-id="b8dee-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="b8dee-122">Ciò può avvenire in modo simultaneo oppure indipendente.</span><span class="sxs-lookup"><span data-stu-id="b8dee-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="b8dee-123">Prima di effettuare la registrazione, è inoltre possibile creare una spedizione parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da spedire** e **Qtà da fatturare** nelle singole righe dell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="b8dee-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="b8dee-124">Si tenga presente che non è possibile creare una fattura per un articolo che non è stato spedito.</span><span class="sxs-lookup"><span data-stu-id="b8dee-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="b8dee-125">Ciò significa che è necessario registrare una spedizione prima di emettere una fattura oppure la spedizione e la fattura devono essere contemporanee.</span><span class="sxs-lookup"><span data-stu-id="b8dee-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="b8dee-126">Una volta completata la registrazione, le righe di vendita registrate vengono rimosse dall'ordine.</span><span class="sxs-lookup"><span data-stu-id="b8dee-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="b8dee-127">Un messaggio avviserà l'utente che la registrazione è completata.</span><span class="sxs-lookup"><span data-stu-id="b8dee-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="b8dee-128">Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie finestre che contengono movimenti registrati, ad esempio le finestre **Mov. contabili clienti**, **Movimenti C/G**, **Mov. contabili articoli**, **Spedizioni vendite registrate** e **Fatture di vendita registrate**.</span><span class="sxs-lookup"><span data-stu-id="b8dee-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8dee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8dee-129">See Also</span></span>
[<span data-ttu-id="b8dee-130">Vendite</span><span class="sxs-lookup"><span data-stu-id="b8dee-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="b8dee-131">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="b8dee-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="b8dee-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8dee-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


