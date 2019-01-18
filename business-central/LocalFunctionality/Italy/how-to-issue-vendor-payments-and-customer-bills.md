---
title: 'Procedura: Emettere pagamenti fornitori ed effetti clienti'
description: "La funzionalità di pagamento degli effetti cliente e fornitore supporta i formati SEPA oltre ai formati di file italiani."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: b84d4eeee1697dcb3341764b3ea716188b81c857
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="issue-vendor-payments-and-customer-bills"></a><span data-ttu-id="d2074-103">Emettere pagamenti fornitori ed effetti clienti</span><span class="sxs-lookup"><span data-stu-id="d2074-103">Issue Vendor Payments and Customer Bills</span></span>
<span data-ttu-id="d2074-104">La funzionalità di pagamento degli effetti cliente e fornitore supporta i formati SEPA oltre ai formati di file italiani.</span><span class="sxs-lookup"><span data-stu-id="d2074-104">The vendor and customer bill pay feature supports SEPA-based formats in addition to Italian file formats.</span></span> <span data-ttu-id="d2074-105">È possibile pagare i fornitori in base al bonifico SEPA standard e riscuotere i pagamenti dai clienti in base al metodo di addebito diretto SEPA standard.</span><span class="sxs-lookup"><span data-stu-id="d2074-105">You can pay vendors according to the SEPA Credit Transfer standard and collect payment from customers according to the SEPA Direct Debit standard.</span></span> <span data-ttu-id="d2074-106">Di seguito viene descritto il processo per l'invio del pagamento a un fornitore con bonifico SEPA.</span><span class="sxs-lookup"><span data-stu-id="d2074-106">The following procedure describes the process for sending a SEPA-based payment to a vendor.</span></span> <span data-ttu-id="d2074-107">I passaggi sono simili per la riscossione del pagamento da un cliente.</span><span class="sxs-lookup"><span data-stu-id="d2074-107">The steps are similar for collecting payment from a customer.</span></span>  

 <span data-ttu-id="d2074-108">Prima di avviare la seguente procedura, controllare che le informazioni sulla banca della società siano state immesse nella pagina **Scheda conto corrente bancario**.</span><span class="sxs-lookup"><span data-stu-id="d2074-108">Before starting the following procedure, make sure that information for your company's bank has been provided on the **Bank Account Card** page.</span></span> <span data-ttu-id="d2074-109">Nella scheda. includere le informazioni per i seguenti campi:</span><span class="sxs-lookup"><span data-stu-id="d2074-109">On the card, include information for the following fields:</span></span>  

- <span data-ttu-id="d2074-110">IBAN</span><span class="sxs-lookup"><span data-stu-id="d2074-110">IBAN</span></span>  
- <span data-ttu-id="d2074-111">Codice SWIFT (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="d2074-111">SWIFT Code (optional)</span></span>  
- <span data-ttu-id="d2074-112">Formato esportazione pagamento</span><span class="sxs-lookup"><span data-stu-id="d2074-112">Payment Export Format</span></span>  
- <span data-ttu-id="d2074-113">Nr serie ID msg CT SEPA</span><span class="sxs-lookup"><span data-stu-id="d2074-113">SEPA CT Msg. ID No.</span></span> <span data-ttu-id="d2074-114">Serie</span><span class="sxs-lookup"><span data-stu-id="d2074-114">Series</span></span>  

<span data-ttu-id="d2074-115">Inoltre, occorre inserire una fattura di acquisito registrata e con cui è possibile inviare un pagamento.</span><span class="sxs-lookup"><span data-stu-id="d2074-115">In addition, there must be a posted purchased invoice against which you can send a payment.</span></span>  

## <a name="to-issue-payment-to-a-vendor"></a><span data-ttu-id="d2074-116">Per emettere il pagamento per un fornitore</span><span class="sxs-lookup"><span data-stu-id="d2074-116">To issue payment to a vendor</span></span>  

1. <span data-ttu-id="d2074-117">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fornitori**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d2074-117">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d2074-118">Selezionare il fornitore al quale si desidera inviare il pagamento.</span><span class="sxs-lookup"><span data-stu-id="d2074-118">Select the vendor to which you want to send payment.</span></span> <span data-ttu-id="d2074-119">Nella Scheda dettaglio **Pagamento**, nel campo **Codice metodo di pagamento** scegliere l'opzione **TRASFBANC**.</span><span class="sxs-lookup"><span data-stu-id="d2074-119">On the **Payment** FastTab, in the **Payment Method Code** field, choose the **TRASFBANC** option.</span></span>
3. <span data-ttu-id="d2074-120">Scegliere l'azione **C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="d2074-120">Choose the **Bank Accounts** action.</span></span>  
4. <span data-ttu-id="d2074-121">In **Lista C/C bancari fornitori**, selezionare il conto C/C bancari del fornitore e scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="d2074-121">In the **Vendor Bank Account List**, select the vendor's bank account, and then choose the **Edit** action.</span></span>
5. <span data-ttu-id="d2074-122">Nella Scheda dettaglio **Trasferimento**, specificare le informazioni relative al campo **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="d2074-122">On the **Transfer** FastTab, specify information for the **IBAN** field.</span></span>  
6. <span data-ttu-id="d2074-123">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2074-123">Choose the **OK** button.</span></span>  
7. <span data-ttu-id="d2074-124">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Cerca pagina o report"), immettere **Distinta fornitore**, quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d2074-124">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Bill Card**, and then choose the related link.</span></span>  
8. <span data-ttu-id="d2074-125">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d2074-125">Choose the **New** action.</span></span>  
9.  <span data-ttu-id="d2074-126">Nella Scheda dettaglio **Generale**, immettere le informazioni nei seguenti campi: **Nr. conto bancario** del fornitore e **Codice metodo di pagamento**.</span><span class="sxs-lookup"><span data-stu-id="d2074-126">On the **General** FastTab, enter information in the following fields: **Bank Account No.** of the vendor and **Payment Method Code**.</span></span>  
10. <span data-ttu-id="d2074-127">Scegliere l'azione **Suggerisci Pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="d2074-127">Choose the **Suggest Payment** action.</span></span>
11. <span data-ttu-id="d2074-128">Impostare i filtri appropriati e scegliere il pulsante **OK** per eseguire il processo batch.</span><span class="sxs-lookup"><span data-stu-id="d2074-128">Set filters, as appropriate, and then choose the **OK** button to run the batch job.</span></span>  
12. <span data-ttu-id="d2074-129">Scegliere l'azione **Crea Distinta**.</span><span class="sxs-lookup"><span data-stu-id="d2074-129">Choose the **Create List** action.</span></span>
13. <span data-ttu-id="d2074-130">Scegliere il pulsante **Sì** per inviare il pagamento dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="d2074-130">Choose the **Yes** button to send the bill payment.</span></span>  
14. <span data-ttu-id="d2074-131">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Distinta effetti fornitore emessa**, quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d2074-131">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Bill List Issued**, and choose the related link.</span></span>
15. <span data-ttu-id="d2074-132">Selezionare l'utente dall'elenco quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="d2074-132">Select the bill payment that you issued from the list, and then choose the **Edit** action.</span></span> <span data-ttu-id="d2074-133">Verrà aperta la pagina **Distinta effetti forn. emessa**.</span><span class="sxs-lookup"><span data-stu-id="d2074-133">The **Vendor Bill List Sent Card** page opens.</span></span>  
16. <span data-ttu-id="d2074-134">Per esportare le informazioni sui pagamenti, scegliere l'azione **Esporta distinta effetti su file**.</span><span class="sxs-lookup"><span data-stu-id="d2074-134">To export the payment information, choose the **Export Bill List to File** action.</span></span> <span data-ttu-id="d2074-135">È possibile visualizzare il file XML inviato.</span><span class="sxs-lookup"><span data-stu-id="d2074-135">You can review the xml file that was sent.</span></span>  

    1.  <span data-ttu-id="d2074-136">Esportare nel file (per file in formato SEPA standard)</span><span class="sxs-lookup"><span data-stu-id="d2074-136">Export to File (for standard SEPA format files)</span></span>  
    2.  <span data-ttu-id="d2074-137">Esporta distinta effetti su file</span><span class="sxs-lookup"><span data-stu-id="d2074-137">Export Bill List to File</span></span>  

<span data-ttu-id="d2074-138">È possibile visualizzare il file XML prima di inviarlo.</span><span class="sxs-lookup"><span data-stu-id="d2074-138">You can review the .xml file before sending it.</span></span> <span data-ttu-id="d2074-139">Per esaminare e correggere gli errori, è possibile fare riferimento al riquadro Dettaglio informazioni **Errori esportazione file**.</span><span class="sxs-lookup"><span data-stu-id="d2074-139">To review and fix errors, you can refer to the **File Export Errors** FactBox.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2074-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2074-140">See Also</span></span>  
[<span data-ttu-id="d2074-141">Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca</span><span class="sxs-lookup"><span data-stu-id="d2074-141">Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>](../../finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)

