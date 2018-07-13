---
title: Impostare i processi finanziari| Documenti Microsoft
description: "Informazioni sulle attività per impostare i dati finanziari nella propria attività per adattarli alle esigenze di contabilità, controllo e gestione dei libri contabili."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 025c00e6013e773204a12abc7d86c09b3dcef3dd
ms.contentlocale: it-it
ms.lasthandoff: 06/28/2018

---
# <a name="setting-up-finance"></a><span data-ttu-id="5ecb8-103">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="5ecb8-103">Setting Up Finance</span></span>
<span data-ttu-id="5ecb8-104">Per velocizzare l'inizio, [!INCLUDE[d365fin](includes/d365fin_md.md)] include le configurazioni di default della maggior parte dei processi finanziari.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-104">To help you get going quickly, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="5ecb8-105">Se è necessario apportare modifiche alle configurazioni per adattarle alla propria attività, procedere subito.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="5ecb8-106">Ad esempio, nella Gestione ruolo utente, è possibile utilizzare la guida al setup assistito per configurare l'aliquota in base all'ubicazione.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-106">For example, from the Role Center, you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="5ecb8-107">Tuttavia, esistono alcune opzioni che occorre impostare manualmente.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="5ecb8-108">Ad esempio, se si desidera utilizzare le dimensioni come base per la categoria di business intelligence.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="5ecb8-109">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="5ecb8-110">Per</span><span class="sxs-lookup"><span data-stu-id="5ecb8-110">To</span></span> | <span data-ttu-id="5ecb8-111">Vedere</span><span class="sxs-lookup"><span data-stu-id="5ecb8-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="5ecb8-112">Scegliere la modalità di pagamento dei fornitori.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="5ecb8-113">Definizione dei metodi di pagamento</span><span class="sxs-lookup"><span data-stu-id="5ecb8-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="5ecb8-114">Specificare le categorie di registrazione che associano entità come clienti, fornitori, articoli, risorse e documenti di vendita o di acquisto a conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="5ecb8-115">Impostazione delle categorie di registrazione</span><span class="sxs-lookup"><span data-stu-id="5ecb8-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="5ecb8-116">Creare le situazioni contabili e definire le categorie di conti per definire il contenuto dei grafici e dei report finanziari, ad esempio i report di conto patrimoniale e conto economico.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-116">Create account schedules and define account categories to define the contents of financial charts and reports, such as the Balance Sheet and Income Statement reports.</span></span>|[<span data-ttu-id="5ecb8-117">Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti</span><span class="sxs-lookup"><span data-stu-id="5ecb8-117">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>](bi-how-work-account-schedule.md)|
|<span data-ttu-id="5ecb8-118">Impostare una tolleranza da cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-118">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="5ecb8-119">Utilizzare le tolleranze pagamento e le tolleranze sconto pagamento</span><span class="sxs-lookup"><span data-stu-id="5ecb8-119">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="5ecb8-120">Impostare periodi fiscali.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-120">Set up fiscal periods.</span></span> |[<span data-ttu-id="5ecb8-121">Aprire un nuovo anno fiscale</span><span class="sxs-lookup"><span data-stu-id="5ecb8-121">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="5ecb8-122">Definire come dichiarare alle autorità fiscali gli importi dell'imposta sul valore aggiunto (IVA) raccolti per le vendite.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-122">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="5ecb8-123">Procedura: Dichiarare l'IVA all'autorità fiscale</span><span class="sxs-lookup"><span data-stu-id="5ecb8-123">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="5ecb8-124">Impostare le funzionalità Vendite e acquisti per gestire i pagamenti in valute estere.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-124">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="5ecb8-125">Abilitare il collegamento dei movimenti contabili fornitore in valute diverse</span><span class="sxs-lookup"><span data-stu-id="5ecb8-125">Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="5ecb8-126">Aggiungere nuovi conti a un piano dei conti esistente.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-126">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="5ecb8-127">Impostazione del piano dei conti</span><span class="sxs-lookup"><span data-stu-id="5ecb8-127">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="5ecb8-128">Impostare i grafici di business intelligence (BI) per analizzare il flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-128">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="5ecb8-129">Impostazione di un'analisi di un flusso di cassa</span><span class="sxs-lookup"><span data-stu-id="5ecb8-129">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="5ecb8-130">Abilitazione della fatturazione di un cliente che non è impostato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5ecb8-130">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="5ecb8-131">Impostare i clienti per vendite in contanti</span><span class="sxs-lookup"><span data-stu-id="5ecb8-131">Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="5ecb8-132">Impostare la creazione di report Intrastat e inviare il report a un'autorità</span><span class="sxs-lookup"><span data-stu-id="5ecb8-132">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="5ecb8-133">Impostare e registrare report Intrastat</span><span class="sxs-lookup"><span data-stu-id="5ecb8-133">Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="5ecb8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ecb8-134">See Also</span></span>
[<span data-ttu-id="5ecb8-135">Finanze</span><span class="sxs-lookup"><span data-stu-id="5ecb8-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="5ecb8-136">Gestione di conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="5ecb8-136">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="5ecb8-137">Utilizzo delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="5ecb8-137">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="5ecb8-138">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="5ecb8-138">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="5ecb8-139">Analizzare il flusso di cassa dell'azienda</span><span class="sxs-lookup"><span data-stu-id="5ecb8-139">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="5ecb8-140">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5ecb8-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

