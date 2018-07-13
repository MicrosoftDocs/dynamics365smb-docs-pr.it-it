---
title: "Gestione della contabilità fornitori| Documenti Microsoft"
description: "Panoramica su come gestire la contabilità fornitori, inclusi i pagamenti fornitore, i creditori, i debiti e saldi scaduti."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 1682db5bd62f980e8789613cd2ca4169f98e839d
ms.contentlocale: it-it
ms.lasthandoff: 06/01/2018

---
# <a name="managing-payables"></a><span data-ttu-id="f3ccc-103">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="f3ccc-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f3ccc-104"> consente di gestire in modo efficace il conto pagamenti fornitori.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-104"> has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="f3ccc-105">Pagamenti</span><span class="sxs-lookup"><span data-stu-id="f3ccc-105">Payments</span></span>
<span data-ttu-id="f3ccc-106">Consente di assegnare priorità ai pagamenti, tenere conto delle penalità per i pagamenti scaduti e gestire gli sconti per i pagamenti anticipati.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="f3ccc-107">È possibile contabilizzare i pagamenti in una registrazione COGE, quindi stampare gli assegni prima delle registrazioni di pagamento.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="f3ccc-108">È possibile collegare i pagamenti per consentire la chiusura delle fatture al momento della registrazione del pagamento o in un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="f3ccc-109">Il **Metodo collegamento PA** specificato per il fornitore ( **Scheda fornitore**) determina se il pagamento viene collegato manualmente o automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="f3ccc-110">Le transazioni possono essere sempre collegate manualmente.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-110">You can always apply transactions manually.</span></span> <span data-ttu-id="f3ccc-111">Tuttavia, se il metodo di collegamento per il fornitore è **Collega alla più vecchia** e non si specifica un documento cui collegare il pagamento, questo viene collegato al movimento aperto meno recente relativo al fornitore.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="f3ccc-112">Sugg. pagamenti fornitore</span><span class="sxs-lookup"><span data-stu-id="f3ccc-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f3ccc-113"> può fornire suggerimenti di pagamento ai fornitori, ad esempio pagamenti con scadenza a breve termine oppure pagamenti che prevedono uno sconto.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-113"> can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="f3ccc-114">Il suggerimento di pagamento può includere un importo indicato come fondi disponibili per il pagamento e il diritto all'applicazione di sconti sul pagamento.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="f3ccc-115">Emettere assegni</span><span class="sxs-lookup"><span data-stu-id="f3ccc-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f3ccc-116"> consente di emettere assegni ai fornitori manualmente ed elettronicamente.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-116"> lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="f3ccc-117">È possibile eseguire entrambe le operazioni nella finestra **Registrazioni pagamenti**, in cui è possibile anche annullare assegni e visualizzare movimenti contabili degli assegni.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="f3ccc-118">Esportare pagamenti in un file della banca</span><span class="sxs-lookup"><span data-stu-id="f3ccc-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="f3ccc-119">Quando si è pronti a pagare un fornitore, nella finestra **Registrazioni pagamenti** è possibile esportare un file con le informazioni di pagamento dalle righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="f3ccc-120">È quindi possibile caricare il file sul sito elettronico della banca per elaborare i trasferimenti di denaro.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="f3ccc-121">Se non si desidera registrare una riga di registrazione pagamenti per un pagamento esportato, ad esempio perché si sta attendendo dalla banca la conferma della transazione, è possibile eliminare la riga di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="f3ccc-122">In seguito quando si crea una riga di registrazione pagamenti per pagare l'importo residuo della fattura, il campo **Importo totale esportato** visualizza la quantità dell'importo pagamento già esportata.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="f3ccc-123">Inoltre, è possibile trovare informazioni dettagliate sul totale esportato scegliendo il pulsante **Movimenti dei registri di bonifici**.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="f3ccc-124">Se si aspetta di registrare i pagamenti fino a dopo che la banca ha confermato l'elaborazione delle transazioni, sono disponibili due modi per evitare di riesportare casualmente i pagamenti per i documenti aperti:</span><span class="sxs-lookup"><span data-stu-id="f3ccc-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="f3ccc-125">Nelle registrazioni pagamenti con le righe di pagamento suggerite, è possibile ordinare la colonna **Esportato su file pagamento** o **Importo totale esportato** e poi eliminare i suggerimenti di pagamento per le fatture aperte per le quali i pagamenti sono già stati effettuati e per le quali non si desidera creare pagamenti.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="f3ccc-126">**Nota:** potrebbe essere necessario aggiungere queste colonne alla lista.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="f3ccc-127">Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="f3ccc-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="f3ccc-128">In alternativa, nel processo batch di **Sugg. pagamenti fornitore**, in cui vengono specificati i pagamenti da inserire nelle registrazioni pagamenti, è possibile indicare di non inserire le righe delle registrazioni pagamenti che sono già state esportate, scegliendo la casella di controllo **Ignora pagamenti esportati**.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3ccc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3ccc-129">See Also</span></span>
[<span data-ttu-id="f3ccc-130">Metodi di pagamento</span><span class="sxs-lookup"><span data-stu-id="f3ccc-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="f3ccc-131">Finanze</span><span class="sxs-lookup"><span data-stu-id="f3ccc-131">Finance</span></span>](finance.md)  
<span data-ttu-id="f3ccc-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3ccc-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

