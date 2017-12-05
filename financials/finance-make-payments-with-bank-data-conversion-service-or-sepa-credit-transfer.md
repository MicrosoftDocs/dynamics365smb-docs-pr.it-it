---
title: Scegliere il metodo di pagamento elettronico | Microsoft Docs
description: Elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: it-it
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="d8459-103">Eseguire i pagamenti con servizio di conversione di dati bancari o bonifico SEPA</span><span class="sxs-lookup"><span data-stu-id="d8459-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="d8459-104">Nella finestra **Registraz. pagamenti** è possibile elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni.</span><span class="sxs-lookup"><span data-stu-id="d8459-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="d8459-105">È quindi possibile caricare il file sul sito elettronico della banca dove vengono elaborati i trasferimenti di denaro correlati.</span><span class="sxs-lookup"><span data-stu-id="d8459-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d8459-106"> supporta il formato di bonifico SEPA, ma nel proprio paese potrebbero essere disponibili anche altri formati di pagamento elettronico.</span><span class="sxs-lookup"><span data-stu-id="d8459-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="d8459-107">Per abilitare i bonifici SEPA, è necessario innanzitutto impostare un conto corrente bancario, un fornitore e il batch registrazioni COGE su cui si basano le registrazioni pagamenti.</span><span class="sxs-lookup"><span data-stu-id="d8459-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="d8459-108">Successivamente si preparano i pagamenti dei fornitori compilando automaticamente la finestra **Registraz. pagamenti** con i pagamenti in scadenza insieme alle date di registrazione specificate.</span><span class="sxs-lookup"><span data-stu-id="d8459-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d8459-109">Una volta verificato che i pagamenti sono stati elaborati correttamente dalla banca, è possibile passare alla registrazione delle righe di registrazione pagamenti.</span><span class="sxs-lookup"><span data-stu-id="d8459-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="d8459-110">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="d8459-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="d8459-111">**Per**</span><span class="sxs-lookup"><span data-stu-id="d8459-111">**To**</span></span>|<span data-ttu-id="d8459-112">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="d8459-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="d8459-113">Attivare la funzionalità In modo inverso, è possibile utilizzare la funzionalità Servizio di conversione di dati bancari per convertire tutti i file di rendiconto bancario in un formato che è possibile importare o per convertire i file di pagamento esportati nel formato richiesto dalla banca.</span><span class="sxs-lookup"><span data-stu-id="d8459-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="d8459-114">Procedura: Impostare il servizio di conversione di dati bancari</span><span class="sxs-lookup"><span data-stu-id="d8459-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="d8459-115">Impostare un conto corrente bancario, un fornitore e le registrazioni pagamenti per bonifici SEPA.</span><span class="sxs-lookup"><span data-stu-id="d8459-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="d8459-116">Procedura: Impostare il bonifico SEPA</span><span class="sxs-lookup"><span data-stu-id="d8459-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="d8459-117">Compilare le registrazioni di pagamento con le righe per i pagamenti dovuti ai fornitori, con l'opzione di inserire le date di registrazione in base alla data di scadenza dei reltivi documenti di acquisto.</span><span class="sxs-lookup"><span data-stu-id="d8459-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="d8459-118">Gestire la contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="d8459-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="d8459-119">Esportare le righe registrazione pagamenti in un file in formato di bonifico SEPA.</span><span class="sxs-lookup"><span data-stu-id="d8459-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="d8459-120">Procedura: esportare pagamenti in un file della banca</span><span class="sxs-lookup"><span data-stu-id="d8459-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="d8459-121">Analizzare quali pagamenti sono stati esportati e in quali file.</span><span class="sxs-lookup"><span data-stu-id="d8459-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="d8459-122">Registri di bonifici</span><span class="sxs-lookup"><span data-stu-id="d8459-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="d8459-123">Quando il pagamento elettronico viene elaborato correttamente dalla banca, registrare i pagamenti.</span><span class="sxs-lookup"><span data-stu-id="d8459-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="d8459-124">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="d8459-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="d8459-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8459-125">See Also</span></span>  
[<span data-ttu-id="d8459-126">Procedura: Impostare il servizio di conversione di dati bancari</span><span class="sxs-lookup"><span data-stu-id="d8459-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="d8459-127">Procedura: Impostare il bonifico SEPA</span><span class="sxs-lookup"><span data-stu-id="d8459-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="d8459-128">[Gestire la contabilità fornitori](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="d8459-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="d8459-129">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="d8459-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="d8459-130">Riscuotere pagamenti con addebito diretto SEPA</span><span class="sxs-lookup"><span data-stu-id="d8459-130">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

