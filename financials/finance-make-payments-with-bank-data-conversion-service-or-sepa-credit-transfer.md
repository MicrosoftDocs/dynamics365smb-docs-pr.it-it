---
title: Eseguire i pagamenti con il servizio di conversione dati bancari o bonifico SEPA | Microsoft Docs
description: Elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d9388a99585eea4e9e229a2f47982f9f690e3001
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="eee02-103">Effettuare i pagamenti con servizio di conversione dati bancari o bonifico SEPA</span><span class="sxs-lookup"><span data-stu-id="eee02-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="eee02-104">Nella finestra **Registraz. pagamenti** è possibile elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni.</span><span class="sxs-lookup"><span data-stu-id="eee02-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="eee02-105">È quindi possibile caricare il file sul sito elettronico della banca dove vengono elaborati i trasferimenti di denaro correlati.</span><span class="sxs-lookup"><span data-stu-id="eee02-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="eee02-106"> supporta il formato di bonifico SEPA, ma nel proprio paese potrebbero essere disponibili anche altri formati di pagamento elettronico.</span><span class="sxs-lookup"><span data-stu-id="eee02-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="eee02-107">Per abilitare i bonifici SEPA, è necessario innanzitutto impostare un conto corrente bancario, un fornitore e il batch registrazioni COGE su cui si basano le registrazioni pagamenti.</span><span class="sxs-lookup"><span data-stu-id="eee02-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="eee02-108">Successivamente si preparano i pagamenti dei fornitori compilando automaticamente la finestra **Registraz. pagamenti** con i pagamenti in scadenza insieme alle date di registrazione specificate.</span><span class="sxs-lookup"><span data-stu-id="eee02-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="eee02-109">Una volta verificato che i pagamenti sono stati elaborati correttamente dalla banca, è possibile passare alla registrazione delle righe di registrazione pagamenti.</span><span class="sxs-lookup"><span data-stu-id="eee02-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="eee02-110">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="eee02-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="eee02-111">**Per**</span><span class="sxs-lookup"><span data-stu-id="eee02-111">**To**</span></span>|<span data-ttu-id="eee02-112">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="eee02-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="eee02-113">Attivare la funzionalità In modo inverso, è possibile utilizzare la funzionalità Servizio di conversione di dati bancari per convertire tutti i file di rendiconto bancario in un formato che è possibile importare o per convertire i file di pagamento esportati nel formato richiesto dalla banca.</span><span class="sxs-lookup"><span data-stu-id="eee02-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="eee02-114">Impostare il servizio di conversione di dati bancari</span><span class="sxs-lookup"><span data-stu-id="eee02-114">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="eee02-115">Impostare un conto corrente bancario, un fornitore e le registrazioni pagamenti per bonifici SEPA.</span><span class="sxs-lookup"><span data-stu-id="eee02-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="eee02-116">Impostare un bonifico SEPA</span><span class="sxs-lookup"><span data-stu-id="eee02-116">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="eee02-117">Compilare le registrazioni di pagamento con le righe per i pagamenti dovuti ai fornitori, con l'opzione di inserire le date di registrazione in base alla data di scadenza dei reltivi documenti di acquisto.</span><span class="sxs-lookup"><span data-stu-id="eee02-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="eee02-118">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="eee02-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="eee02-119">Esportare le righe registrazione pagamenti in un file in formato di bonifico SEPA.</span><span class="sxs-lookup"><span data-stu-id="eee02-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="eee02-120">Esportare pagamenti in un file della banca</span><span class="sxs-lookup"><span data-stu-id="eee02-120">Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="eee02-121">Quando il pagamento elettronico viene elaborato correttamente dalla banca, registrare i pagamenti.</span><span class="sxs-lookup"><span data-stu-id="eee02-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="eee02-122">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="eee02-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="eee02-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eee02-123">See Also</span></span>  
[<span data-ttu-id="eee02-124">Impostare il servizio di conversione di dati bancari</span><span class="sxs-lookup"><span data-stu-id="eee02-124">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="eee02-125">Impostare un bonifico SEPA</span><span class="sxs-lookup"><span data-stu-id="eee02-125">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="eee02-126">[Gestione della contabilità fornitori](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="eee02-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="eee02-127">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="eee02-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="eee02-128">Riscuotere pagamenti con addebito diretto SEPA</span><span class="sxs-lookup"><span data-stu-id="eee02-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

