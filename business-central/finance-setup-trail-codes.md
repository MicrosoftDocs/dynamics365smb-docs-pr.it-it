---
title: Impostare codici per audit trail | Microsoft Docs
description: Informazioni sulle attività per impostare i codici sorgente e le causali da utilizzare per tenere traccia degli audit trail.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 05/12/2020
ms.author: edupont
ms.openlocfilehash: eac9b5268cda8671a7189a429dedd9eb3cbfbc53
ms.sourcegitcommit: b9264b4ed650feca18776892ec23f2aa7ec43e20
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372689"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="f36a0-103">Impostazione di codici sorgente e causali per audit trail</span><span class="sxs-lookup"><span data-stu-id="f36a0-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="f36a0-104">A tutti i movimenti registrati viene automaticamente assegnato un codice origine, in modo da poter risalire all'origine delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="f36a0-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="f36a0-105">Se si desidera assegnare ai movimenti un codice origine aggiuntivo, è possibile utilizzare le causali.</span><span class="sxs-lookup"><span data-stu-id="f36a0-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="f36a0-106">Le causali indicano perché è stato creato un movimento.</span><span class="sxs-lookup"><span data-stu-id="f36a0-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="f36a0-107">Quando si impostano le causali, è possibile assegnarle alle definizioni delle registrazioni e ai batch di registrazione, nonché a singoli documenti e righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f36a0-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="f36a0-108">Sia per i codici sorgente sia per le causali, utilizzare codici facili da ricordare e descrittivi.</span><span class="sxs-lookup"><span data-stu-id="f36a0-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="f36a0-109">Il codice deve essere unico ed è possibile impostare un numero indefinito di codici.</span><span class="sxs-lookup"><span data-stu-id="f36a0-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="f36a0-110">Definire i codici origine</span><span class="sxs-lookup"><span data-stu-id="f36a0-110">Define source codes</span></span>

<span data-ttu-id="f36a0-111">A volte può essere necessario conoscere la provenienza di un determinato movimento, ovvero sapere, ad esempio, se è riconducibile alla contabilizzazione di una registrazione COGE o di una fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="f36a0-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="f36a0-112">Il codice origine indica dove è stato creato un movimento.</span><span class="sxs-lookup"><span data-stu-id="f36a0-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="f36a0-113">I movimenti vengono creati alla contabilizzazione di registrazioni e fatture e all'esecuzione di determinati processi batch.</span><span class="sxs-lookup"><span data-stu-id="f36a0-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="f36a0-114">Ogni tipo di registrazione dispone di un codice origine specifico, che viene assegnato alla creazione dei movimenti.</span><span class="sxs-lookup"><span data-stu-id="f36a0-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="f36a0-115">Quando si contabilizzano registrazioni, ordini, fatture, note credito o registrazioni e quando si eseguono alcuni processi batch, vengono generati dei movimenti nei rendiconti finanziari.</span><span class="sxs-lookup"><span data-stu-id="f36a0-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="f36a0-116">La pagina **Setup codice origine** contiene varie Schede dettaglio, una per ogni area di applicazione.</span><span class="sxs-lookup"><span data-stu-id="f36a0-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="f36a0-117">Ogni Scheda dettaglio contiene i codici origine applicabili a quell'area di applicazione.</span><span class="sxs-lookup"><span data-stu-id="f36a0-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="f36a0-118">Sia in fase di registrazione che di esecuzione di un processo batch, il codice origine corretto viene automaticamente allegato al movimento.</span><span class="sxs-lookup"><span data-stu-id="f36a0-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="f36a0-119">Nel caso si contabilizzino delle registrazioni COGE, ad esempio, al movimento viene allegato il codice *GENJNL*.</span><span class="sxs-lookup"><span data-stu-id="f36a0-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="f36a0-120">È quindi possibile filtrare la pagina **Movimenti C/G** pagina per mostrare quali movimenti sono stati pubblicati dalla registrazioni COGE o dai documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="f36a0-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="f36a0-121">Per definire i codici origine</span><span class="sxs-lookup"><span data-stu-id="f36a0-121">To define source codes</span></span>

1. <span data-ttu-id="f36a0-122">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Setup codice origine** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f36a0-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="f36a0-123">Nella finestra **Setup codice origine**, per ogni tipo di registrazione e processo batch, specificare il codice sorgente pertinente.</span><span class="sxs-lookup"><span data-stu-id="f36a0-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="f36a0-124">È possibile modificare il contenuto di un campo in un secondo momento e tale modifica avrà un impatto sulle registrazioni future.</span><span class="sxs-lookup"><span data-stu-id="f36a0-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="f36a0-125">Modificare i codici origine</span><span class="sxs-lookup"><span data-stu-id="f36a0-125">Change source codes</span></span>

<span data-ttu-id="f36a0-126">Potrebbe essere necessario modificare un codice origine.</span><span class="sxs-lookup"><span data-stu-id="f36a0-126">You may want to change a source code.</span></span> <span data-ttu-id="f36a0-127">Ad esempio, può essere necessario modificare il codice origine *GENJNL* in *GNJ*.</span><span class="sxs-lookup"><span data-stu-id="f36a0-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="f36a0-128">Per modificare i codici origine</span><span class="sxs-lookup"><span data-stu-id="f36a0-128">To change source codes</span></span>

1. <span data-ttu-id="f36a0-129">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Codice origine** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f36a0-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="f36a0-130">Nella riga che contiene il codice da modificare selezionare il codice nel campo **Codice**.</span><span class="sxs-lookup"><span data-stu-id="f36a0-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="f36a0-131">Immettere il nuovo codice, quindi fare clic sul pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="f36a0-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="f36a0-132">È possibile modificare anche il contenuto del campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="f36a0-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="f36a0-133">Tutti i nuovi movimenti contabilizzati dalle registrazioni COGE disporranno di nuovo codice origine.</span><span class="sxs-lookup"><span data-stu-id="f36a0-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="f36a0-134">Definire le causali</span><span class="sxs-lookup"><span data-stu-id="f36a0-134">Define reason codes</span></span>

<span data-ttu-id="f36a0-135">Le causali integrano i codici sorgente e vengono utilizzati per indicare il motivo per cui è stata creato un movimento.</span><span class="sxs-lookup"><span data-stu-id="f36a0-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="f36a0-136">È possibile assegnare causali a movimenti singoli e assegnare codici permanenti a definizioni e batch di registrazioni specifici.</span><span class="sxs-lookup"><span data-stu-id="f36a0-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="f36a0-137">Una volta collegate le causali a una riga di registrazioni oppure a una testata delle vendite o degli acquisti, tutti i movimenti verranno contrassegnati automaticamente da una causale al momento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="f36a0-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="f36a0-138">Per impostare le causali</span><span class="sxs-lookup"><span data-stu-id="f36a0-138">To set up reason codes</span></span>

1. <span data-ttu-id="f36a0-139">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Causali** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f36a0-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="f36a0-140">Nella finestra **Causali** immettere il primo codice nel campo **Codice**.</span><span class="sxs-lookup"><span data-stu-id="f36a0-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="f36a0-141">Nel campo **Descrizione** immettere un testo esplicativo.</span><span class="sxs-lookup"><span data-stu-id="f36a0-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="f36a0-142">Ripetere la procedura per ogni codice che si intende utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f36a0-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="f36a0-143">È possibile impostare quanti codici si ritengono necessari.</span><span class="sxs-lookup"><span data-stu-id="f36a0-143">You can set up any number of codes.</span></span>

<span data-ttu-id="f36a0-144">La seguente procedura descrive come aggiungere una causale a una definizione di registrazioni, ma passaggi simili si applicano all'aggiunta di una causale a una riga di registrazione o a un batch di registrazioni.</span><span class="sxs-lookup"><span data-stu-id="f36a0-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="f36a0-145">Per assegnare causali alle definizioni di registrazioni</span><span class="sxs-lookup"><span data-stu-id="f36a0-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="f36a0-146">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Definizione registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f36a0-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="f36a0-147">Sulla riga della definizione di registrazioni selezionata immettere il codice pertinente nel campo **Causale**.</span><span class="sxs-lookup"><span data-stu-id="f36a0-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="f36a0-148">Chiudere la definizione di registrazioni.</span><span class="sxs-lookup"><span data-stu-id="f36a0-148">Close the journal template.</span></span>

<span data-ttu-id="f36a0-149">La causale selezionata verrà copiata nei nuovi batch di registrazioni creati in questa definizione di registrazioni.</span><span class="sxs-lookup"><span data-stu-id="f36a0-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="f36a0-150">È possibile assegnare causali a definizioni di registrazioni in altre aree di applicazione utilizzando la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="f36a0-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="f36a0-151">Per utilizzare le causali sui documenti di acquisto e vendita</span><span class="sxs-lookup"><span data-stu-id="f36a0-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="f36a0-152">Aprire il documento di acquisto o vendita appropriato.</span><span class="sxs-lookup"><span data-stu-id="f36a0-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="f36a0-153">Nella testata degli acquisti o delle vendite immettere la causale nel campo **Causale**.</span><span class="sxs-lookup"><span data-stu-id="f36a0-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="f36a0-154">Quando la fattura viene registrata, la causale viene copiata in ogni movimento C/G, cliente e fornitore.</span><span class="sxs-lookup"><span data-stu-id="f36a0-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="f36a0-155">Non è possibile assegnare causali diverse a singole righe di acquisto e vendita, perché tutte le righe vengono registrate come un unico movimento.</span><span class="sxs-lookup"><span data-stu-id="f36a0-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f36a0-156">Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="f36a0-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="f36a0-157">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f36a0-157">See Also</span></span>

[<span data-ttu-id="f36a0-158">Finanze</span><span class="sxs-lookup"><span data-stu-id="f36a0-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="f36a0-159">Riconciliazione dei conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="f36a0-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="f36a0-160">Utilizzo delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="f36a0-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="f36a0-161">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="f36a0-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="f36a0-162">Analizzare il flusso di cassa dell'azienda</span><span class="sxs-lookup"><span data-stu-id="f36a0-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="f36a0-163">[Utilizzo di [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f36a0-163">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
