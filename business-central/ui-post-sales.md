---
title: Registrazione di documenti di vendita | Microsoft Docs
description: Informazioni sulle diverse funzioni di registrazione per registrare documenti di vendita e sul modo in cui aggiornare documenti registrati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 01e831ddddeffe6a64c6de24b4cd8c1b94bad9c3
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796897"
---
# <a name="posting-sales"></a><span data-ttu-id="9406a-103">Registrazione di vendite</span><span class="sxs-lookup"><span data-stu-id="9406a-103">Posting Sales</span></span>
<span data-ttu-id="9406a-104">Nella **Categoria registrazione** in un documento di vendita, è possibile scegliere tra le seguenti funzioni di registrazione:</span><span class="sxs-lookup"><span data-stu-id="9406a-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="9406a-105">**Registra**</span><span class="sxs-lookup"><span data-stu-id="9406a-105">**Post**</span></span>
* <span data-ttu-id="9406a-106">**Report test**</span><span class="sxs-lookup"><span data-stu-id="9406a-106">**Test Report**</span></span>
* <span data-ttu-id="9406a-107">**Registra e invia**</span><span class="sxs-lookup"><span data-stu-id="9406a-107">**Post and Send**</span></span>
* <span data-ttu-id="9406a-108">**Registra e stampa**</span><span class="sxs-lookup"><span data-stu-id="9406a-108">**Post and Print**</span></span>
* <span data-ttu-id="9406a-109">**Registra e invia tramite e-mail**</span><span class="sxs-lookup"><span data-stu-id="9406a-109">**Post and Email**</span></span>
* <span data-ttu-id="9406a-110">**Registra batch**</span><span class="sxs-lookup"><span data-stu-id="9406a-110">**Post Batch**</span></span>
* <span data-ttu-id="9406a-111">**Anteprima registrazione**</span><span class="sxs-lookup"><span data-stu-id="9406a-111">**Preview Posting**</span></span>

<span data-ttu-id="9406a-112">Una volta completate le righe e immesse tutte le informazioni nell'ordine di vendita, è possibile registrarlo.</span><span class="sxs-lookup"><span data-stu-id="9406a-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="9406a-113">Vengono create una spedizione e una fattura.</span><span class="sxs-lookup"><span data-stu-id="9406a-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="9406a-114">Quando un ordine di acquisto viene registrato, il conto del cliente, la contabilità generale e i movimenti contabili articoli vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="9406a-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="9406a-115">Per ciascun ordine di vendita viene creato un movimento di vendita nella tabella **Movimenti C/G**.</span><span class="sxs-lookup"><span data-stu-id="9406a-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="9406a-116">Vengono inoltre creati un movimento nel conto del cliente nella tabella **Mov. contabili clienti** e un movimento C/G nel relativo conto crediti.</span><span class="sxs-lookup"><span data-stu-id="9406a-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="9406a-117">Infine, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento di contabilità generale relativi all'importo dello sconto.</span><span class="sxs-lookup"><span data-stu-id="9406a-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="9406a-118">La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione sconti** della pagina **Setup contabilità clienti**.</span><span class="sxs-lookup"><span data-stu-id="9406a-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="9406a-119">Per ciascuna riga dell'ordine di vendita, verrà creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di vendita contengono numeri di articolo) oppure un movimento C/G nella tabella **Movimenti C/G** (se le righe di vendita contengono un conto C/G).</span><span class="sxs-lookup"><span data-stu-id="9406a-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="9406a-120">Inoltre, gli ordini vendita vengono sempre registrati nelle tabelle **Testate sped. vendita** e **Testate Fatt. Vendita**.</span><span class="sxs-lookup"><span data-stu-id="9406a-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="9406a-121">Quando si registra un ordine, è possibile creare sia una spedizione che una fattura.</span><span class="sxs-lookup"><span data-stu-id="9406a-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="9406a-122">Ciò può avvenire in modo simultaneo oppure indipendente.</span><span class="sxs-lookup"><span data-stu-id="9406a-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="9406a-123">Prima di effettuare la registrazione, è inoltre possibile creare una spedizione parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da spedire** e **Qtà da fatturare** nelle singole righe dell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="9406a-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="9406a-124">Si tenga presente che non è possibile creare una fattura per un articolo che non è stato spedito.</span><span class="sxs-lookup"><span data-stu-id="9406a-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="9406a-125">Ciò significa che è necessario registrare una spedizione prima di emettere una fattura oppure la spedizione e la fattura devono essere contemporanee.</span><span class="sxs-lookup"><span data-stu-id="9406a-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="9406a-126">Una volta completata la registrazione, le righe di vendita registrate vengono rimosse dall'ordine.</span><span class="sxs-lookup"><span data-stu-id="9406a-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="9406a-127">Un messaggio avviserà l'utente che la registrazione è completata.</span><span class="sxs-lookup"><span data-stu-id="9406a-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="9406a-128">Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie pagine che contengono movimenti registrati, ad esempio le pagine **Mov. contabili clienti**, **Movimenti C/G**, **Mov. contabili articoli**, **Spedizioni vendite registrate** e **Fatture di vendita registrate**.</span><span class="sxs-lookup"><span data-stu-id="9406a-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9406a-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9406a-129">See Also</span></span>

[<span data-ttu-id="9406a-130">Vendite</span><span class="sxs-lookup"><span data-stu-id="9406a-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="9406a-131">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="9406a-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="9406a-132">Correggere o annullare le fatture di vendita non pagate</span><span class="sxs-lookup"><span data-stu-id="9406a-132">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="9406a-133">Utilizzo delle funzionalità di informazioni per trovare funzionalità e informazioni</span><span class="sxs-lookup"><span data-stu-id="9406a-133">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="9406a-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9406a-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
