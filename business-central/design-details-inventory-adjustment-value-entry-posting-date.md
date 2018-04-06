---
title: Data di registrazione dei movimenti di valorizzazione
description: Informazioni su come il processo batch Rettifica costo - Movimenti articoli identifica e assegna una data di registrazione ai movimenti di valorizzazione che il processo batch crea.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c95432ec1cf24aaaedf0fad5a2746ace9705e2e3
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="4daa5-103">Dettagli di progettazione: Data di registrazione del movimento di valorizzazione della rettifica</span><span class="sxs-lookup"><span data-stu-id="4daa5-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="4daa5-104">In questo articolo vengono fornite informazioni per gli utenti della funzionalità Magazzino e costing di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4daa5-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4daa5-105">L'articolo fornisce informazioni su come il processo batch **Rettifica costo - Movimenti articoli** identifica e assegna una data di registrazione ai movimenti di valorizzazione che il processo batch crea.</span><span class="sxs-lookup"><span data-stu-id="4daa5-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="4daa5-106">Innanzitutto viene esaminato il concetto del processo, il modo in cui il processo batch identifica e assegna la data di registrazione al movimento di valorizzazione da creare.</span><span class="sxs-lookup"><span data-stu-id="4daa5-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="4daa5-107">In seguito, vengono descritti alcuni scenari in cui il team di supporto si è a volte imbattuto e infine viene mostrato un riepilogo dei concetti utilizzati a partire dalla versione 3.0.</span><span class="sxs-lookup"><span data-stu-id="4daa5-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="4daa5-108">Concetto</span><span class="sxs-lookup"><span data-stu-id="4daa5-108">The Concept</span></span>  
<span data-ttu-id="4daa5-109">A partire dalla versione 5.0, il processo batch **Rettifica costo - Movimenti articoli** assegna una data di registrazione al movimento di valorizzazione da creare mediante la seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="4daa5-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="4daa5-110">Inizialmente la data di registrazione del movimento da creare è la stessa data del movimento che viene rettificato.</span><span class="sxs-lookup"><span data-stu-id="4daa5-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="4daa5-111">La data di registrazione viene convalidata in base ai periodi di magazzino e/o al setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="4daa5-112">Assegnazione della data di registrazione; se la data di registrazione iniziale non rientra nell'intervallo di date di registrazione consentite, il processo batch assegnerà una data di registrazione consentita in base al periodo di magazzino o al setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="4daa5-113">Se i periodi di magazzino e le date di registrazione consentite nel setup di contabilità generale sono definiti, la data più lontana delle due verrà assegnata al movimento di valorizzazione della rettifica.</span><span class="sxs-lookup"><span data-stu-id="4daa5-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="4daa5-114">Esaminiamo questo processo con un esempio pratico.</span><span class="sxs-lookup"><span data-stu-id="4daa5-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="4daa5-115">Supponiamo di avere un movimento contabile articolo di vendita.</span><span class="sxs-lookup"><span data-stu-id="4daa5-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="4daa5-116">L'articolo è stato spedito il 5 settembre 2013 ed è stato fatturato il giorno dopo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="4daa5-117">![Movimento contabile articolo: Formato data: AAAA MM GG](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span><span class="sxs-lookup"><span data-stu-id="4daa5-117">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span></span>  

<span data-ttu-id="4daa5-118">Nell'illustrazione seguente, il primo movimento di valorizzazione (379) indica la spedizione e ha la stessa data di registrazione del movimento contabile articolo padre.</span><span class="sxs-lookup"><span data-stu-id="4daa5-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="4daa5-119">Il secondo movimento di valorizzazione (381) rappresenta la fattura.</span><span class="sxs-lookup"><span data-stu-id="4daa5-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="4daa5-120">Il terzo movimento di valorizzazione (391) è una rettifica del movimento di valorizzazione di fatturazione (381).</span><span class="sxs-lookup"><span data-stu-id="4daa5-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="4daa5-121">![Movimento contabile articolo: Formato data: AAAA MM GG](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span><span class="sxs-lookup"><span data-stu-id="4daa5-121">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span></span>  

 <span data-ttu-id="4daa5-122">Passaggio 1: al movimento di valorizzazione della rettifica da creare è assegnata la stessa data di registrazione del movimento che viene rettificato, illustrato sopra dal movimento di valorizzazione 391.</span><span class="sxs-lookup"><span data-stu-id="4daa5-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="4daa5-123">Passaggio 2: convalida della data di registrazione assegnata iniziale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="4daa5-124">Il processo batch **Rettifica costo - Movimenti articoli** determina se la data di registrazione iniziale del movimento di valorizzazione della rettifica rientra nell'intervallo di date consentite basato sui periodi di magazzino e/o sul setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="4daa5-125">Esaminiamo la vendita menzionata in precedenza aggiungendo il setup dell'intervallo di date di registrazione consentite.</span><span class="sxs-lookup"><span data-stu-id="4daa5-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="4daa5-126">Periodi di magazzino:</span><span class="sxs-lookup"><span data-stu-id="4daa5-126">Inventory Periods:</span></span>  

<span data-ttu-id="4daa5-127">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span><span class="sxs-lookup"><span data-stu-id="4daa5-127">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span></span>

 <span data-ttu-id="4daa5-128">La prima data di registrazione consentita è il primo giorno del primo periodo aperto.</span><span class="sxs-lookup"><span data-stu-id="4daa5-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="4daa5-129">1° settembre 2013.</span><span class="sxs-lookup"><span data-stu-id="4daa5-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="4daa5-130">Setup contabilità generale:</span><span class="sxs-lookup"><span data-stu-id="4daa5-130">General Ledger Setup:</span></span>  

<span data-ttu-id="4daa5-131">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span><span class="sxs-lookup"><span data-stu-id="4daa5-131">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span></span>

 <span data-ttu-id="4daa5-132">La prima data di registrazione consentita è la data indicata nel campo Consenti registraz. da: 10 settembre 2013.</span><span class="sxs-lookup"><span data-stu-id="4daa5-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="4daa5-133">Se i periodi di magazzino e le date di registrazione consentite nel setup di contabilità generale sono definiti, la data più lontana delle due definirà l'intervallo di date di registrazione consentite.</span><span class="sxs-lookup"><span data-stu-id="4daa5-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="4daa5-134">Passaggio 3: assegnazione di una data di registrazione consentita;</span><span class="sxs-lookup"><span data-stu-id="4daa5-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="4daa5-135">La data di registrazione assegnata iniziale era il 6 settembre come illustrato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="4daa5-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="4daa5-136">Tuttavia, nel secondo passaggio il processo batch Rettifica costo - Movimenti articoli identifica che la data di registrazione consentita più vicina è il 10 settembre e pertanto assegna il 10 settembre al movimento di valorizzazione della rettifica, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4daa5-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="4daa5-137">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span><span class="sxs-lookup"><span data-stu-id="4daa5-137">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span></span>

 <span data-ttu-id="4daa5-138">Qui termina la descrizione del concetto per l'assegnazione di date di registrazione a movimenti di valorizzazione creati mediante il processo batch Rettifica costo - Movimenti articoli.</span><span class="sxs-lookup"><span data-stu-id="4daa5-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="4daa5-139">Esaminiamo ora alcuni scenari in cui il team di supporto si è a volte imbattuto riguardanti le date di registrazione assegnate nel processo batch Rettifica Costo – Movimenti articoli e i relativi setup .</span><span class="sxs-lookup"><span data-stu-id="4daa5-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="4daa5-140">Scenari</span><span class="sxs-lookup"><span data-stu-id="4daa5-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="4daa5-141">Scenario I: "la data di registrazione non è compresa nell'intervallo di date di registrazione consentite....".</span><span class="sxs-lookup"><span data-stu-id="4daa5-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="4daa5-142">Questo è uno scenario in cui un utente riceve il suddetto messaggio di errore durante il processo batch Rettifica costo - Movimenti articoli.</span><span class="sxs-lookup"><span data-stu-id="4daa5-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="4daa5-143">Nella descrizione del concetto di assegnazione di date di registrazione vista nella sezione precedente, lo scopo del processo batch Rettifica costo – Movimenti articoli è creare un movimento di valorizzazione con il 10 settembre come data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="4daa5-144">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span><span class="sxs-lookup"><span data-stu-id="4daa5-144">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span></span>

 <span data-ttu-id="4daa5-145">Continuiamo con il setup utente:</span><span class="sxs-lookup"><span data-stu-id="4daa5-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="4daa5-146">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span><span class="sxs-lookup"><span data-stu-id="4daa5-146">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span></span>

 <span data-ttu-id="4daa5-147">L'utente in questo caso ha un intervallo di date di registrazione consentite dall'11 settembre al 30 settembre e pertanto non gli è consentito registrare il movimento di valorizzazione della rettifica con il 10 settembre come data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="4daa5-148">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span><span class="sxs-lookup"><span data-stu-id="4daa5-148">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span></span>

 <span data-ttu-id="4daa5-149">L'articolo della Knowledge Base [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) esamina ulteriori scenari relativi al messaggio di errore citato.</span><span class="sxs-lookup"><span data-stu-id="4daa5-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="4daa5-150">Scenario II: la data di registrazione del movimento di valorizzazione della rettifica rispetto alla data di registrazione del movimento origina la rettifica come rivalutazione o addebito articolo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="4daa5-151">Scenario di rivalutazione:</span><span class="sxs-lookup"><span data-stu-id="4daa5-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="4daa5-152">Prerequisiti:</span><span class="sxs-lookup"><span data-stu-id="4daa5-152">Prerequisites:</span></span>  

 <span data-ttu-id="4daa5-153">Setup magazzino:</span><span class="sxs-lookup"><span data-stu-id="4daa5-153">Inventory setup:</span></span>  

-   <span data-ttu-id="4daa5-154">Reg. automatica costi = Sì</span><span class="sxs-lookup"><span data-stu-id="4daa5-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="4daa5-155">Rettifica costo automatica=Sempre</span><span class="sxs-lookup"><span data-stu-id="4daa5-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="4daa5-156">Tipo calcolo costo medio=articolo</span><span class="sxs-lookup"><span data-stu-id="4daa5-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="4daa5-157">Costo medio periodo=Giorno</span><span class="sxs-lookup"><span data-stu-id="4daa5-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="4daa5-158">Setup contabilità generale:</span><span class="sxs-lookup"><span data-stu-id="4daa5-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="4daa5-159">Consenti registraz. da = 1° gennaio 2014</span><span class="sxs-lookup"><span data-stu-id="4daa5-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="4daa5-160">Consenti registrazioni fino a = vuoto</span><span class="sxs-lookup"><span data-stu-id="4daa5-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="4daa5-161">Setup utente:</span><span class="sxs-lookup"><span data-stu-id="4daa5-161">User Setup:</span></span>  

-   <span data-ttu-id="4daa5-162">Consenti registraz. da = 1° dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="4daa5-163">Consenti registrazioni fino a = vuoto</span><span class="sxs-lookup"><span data-stu-id="4daa5-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="4daa5-164">Per verificare lo scenario:</span><span class="sxs-lookup"><span data-stu-id="4daa5-164">To test the scenario</span></span>  

1.  <span data-ttu-id="4daa5-165">Creare TEST articolo:</span><span class="sxs-lookup"><span data-stu-id="4daa5-165">Create item TEST:</span></span>  

     <span data-ttu-id="4daa5-166">Unità di misura base = PZ</span><span class="sxs-lookup"><span data-stu-id="4daa5-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="4daa5-167">Metodo di costing = Media</span><span class="sxs-lookup"><span data-stu-id="4daa5-167">Costing Method = Average</span></span>  

     <span data-ttu-id="4daa5-168">Selezionare categorie di registrazione facoltative.</span><span class="sxs-lookup"><span data-stu-id="4daa5-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="4daa5-169">Aprire le registrazioni magazzino, creare e registrare una riga come segue:</span><span class="sxs-lookup"><span data-stu-id="4daa5-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4daa5-170">Data di registrazione = 15 dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="4daa5-171">Articolo = TEST</span><span class="sxs-lookup"><span data-stu-id="4daa5-171">Item = TEST</span></span>  

     <span data-ttu-id="4daa5-172">Tipo movimento = Acquisto</span><span class="sxs-lookup"><span data-stu-id="4daa5-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="4daa5-173">Quantità = 100</span><span class="sxs-lookup"><span data-stu-id="4daa5-173">Quantity = 100</span></span>  

     <span data-ttu-id="4daa5-174">Importo unitario = 10</span><span class="sxs-lookup"><span data-stu-id="4daa5-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="4daa5-175">Aprire le registrazioni magazzino, creare e registrare una riga come segue:</span><span class="sxs-lookup"><span data-stu-id="4daa5-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4daa5-176">Data = 20 dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="4daa5-177">Articolo = TEST</span><span class="sxs-lookup"><span data-stu-id="4daa5-177">Item = TEST</span></span>  

     <span data-ttu-id="4daa5-178">Tipo movimento = Rettifica negativa</span><span class="sxs-lookup"><span data-stu-id="4daa5-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="4daa5-179">Quantità = 2</span><span class="sxs-lookup"><span data-stu-id="4daa5-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="4daa5-180">Aprire le registrazioni magazzino, creare e registrare una riga come segue:</span><span class="sxs-lookup"><span data-stu-id="4daa5-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4daa5-181">Data = 15 gennaio 2014</span><span class="sxs-lookup"><span data-stu-id="4daa5-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="4daa5-182">Articolo = TEST</span><span class="sxs-lookup"><span data-stu-id="4daa5-182">Item = TEST</span></span>  

     <span data-ttu-id="4daa5-183">Tipo movimento = Rettifica negativa</span><span class="sxs-lookup"><span data-stu-id="4daa5-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="4daa5-184">Quantità = 3</span><span class="sxs-lookup"><span data-stu-id="4daa5-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="4daa5-185">Aprire le registrazioni rivalutazioni, creare e registrare una riga come segue:</span><span class="sxs-lookup"><span data-stu-id="4daa5-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4daa5-186">Articolo = TEST</span><span class="sxs-lookup"><span data-stu-id="4daa5-186">Item = TEST</span></span>  

     <span data-ttu-id="4daa5-187">Collega-a movimento = selezionare il movimento di tipo Acquisto registrato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="4daa5-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="4daa5-188">La data di registrazione della rivalutazione sarà la stessa del movimento che rettifica.</span><span class="sxs-lookup"><span data-stu-id="4daa5-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="4daa5-189">Costo unitario (rivalutato) = 40</span><span class="sxs-lookup"><span data-stu-id="4daa5-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="4daa5-190">I seguenti movimenti contabili articoli e di valorizzazione sono stati registrati:</span><span class="sxs-lookup"><span data-stu-id="4daa5-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="4daa5-191">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span><span class="sxs-lookup"><span data-stu-id="4daa5-191">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span></span>

 <span data-ttu-id="4daa5-192">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span><span class="sxs-lookup"><span data-stu-id="4daa5-192">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span></span>

 <span data-ttu-id="4daa5-193">Il processo batch Rettifica costo - Movimenti articoli ha riconosciuto una variazione nel costo e rettificato le rettifiche negative.</span><span class="sxs-lookup"><span data-stu-id="4daa5-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="4daa5-194">**Analisi delle date di registrazione dei movimenti di valorizzazione delle rettifiche creati:** la data di registrazione consentita più vicina a cui il processo batch Rettifica costo - Movimenti articoli deve fare riferimento è il 1° gennaio 2014 come indicato nel setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="4daa5-195">**Rettifica negativa nel passaggio 3:** la data di registrazione assegnata è il 1° gennaio, fornita dal setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="4daa5-196">La data di registrazione del movimento di valorizzazione in relazione alla rettifica è il 20 dicembre 2013.</span><span class="sxs-lookup"><span data-stu-id="4daa5-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="4daa5-197">Secondo il setup di contabilità generale la data non rientra nell'intervallo di date di registrazione consentite.</span><span class="sxs-lookup"><span data-stu-id="4daa5-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="4daa5-198">Di conseguenza, la data di registrazione indicata nel campo Consenti registraz. da nel setup di contabilità generale è assegnata al movimento di valorizzazione della rettifica.</span><span class="sxs-lookup"><span data-stu-id="4daa5-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="4daa5-199">**Rettifica negativa nel passaggio 4:** la data di registrazione assegnata è il 15 gennaio.</span><span class="sxs-lookup"><span data-stu-id="4daa5-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="4daa5-200">La data di registrazione del movimento di valorizzazione in relazione alla rettifica è il 15 gennaio, che rientra nell'intervallo di date di registrazione consentite secondo il setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="4daa5-201">La rettifica apportata per la rettifica negativa nel passaggio 3 è oggetto di discussione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="4daa5-202">La data di registrazione favorevole del movimento di valorizzazione della rettifica sarebbe stata il 20 dicembre o almeno in dicembre in quanto la rivalutazione che causa la modifica in COGS è stata registrata in dicembre.</span><span class="sxs-lookup"><span data-stu-id="4daa5-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="4daa5-203">Per eseguire la rettifica negativa nel passaggio 3 in dicembre, la data indicata nel campo Consenti registraz. da del setup di contabilità generale deve essere in dicembre.</span><span class="sxs-lookup"><span data-stu-id="4daa5-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="4daa5-204">**Conclusione:**</span><span class="sxs-lookup"><span data-stu-id="4daa5-204">**Conclusion:**</span></span>  

 <span data-ttu-id="4daa5-205">Sulla base delle esperienze relative a questo scenario, considerando il setup più appropriato dell'intervallo di date di registrazione consentite per un'azienda, potrebbe essere utile considerare quanto segue: fino a che è consentito registrare le modifiche apportate al valore di magazzino in un periodo, dicembre in questo caso, il setup utilizzato dall'azienda per gli intervalli di date di registrazione consentite deve essere allineato a questa decisione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="4daa5-206">Il campo Consenti registraz. da nel setup di contabilità generale, indicante il 1° dicembre, permetterebbe il trasferimento della rivalutazione effettuata a dicembre ai movimenti in uscita interessati nello stesso periodo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="4daa5-207">Per i gruppi di utenti a cui non è consentito registrare in dicembre ma a gennaio, condizione probabilmente determinata dal setup di contabilità generale in questo scenario, si deve utilizzare il setup utente.</span><span class="sxs-lookup"><span data-stu-id="4daa5-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="4daa5-208">Scenario con addebito articolo:</span><span class="sxs-lookup"><span data-stu-id="4daa5-208">Item charge scenario:</span></span>  
 <span data-ttu-id="4daa5-209">Prerequisiti:</span><span class="sxs-lookup"><span data-stu-id="4daa5-209">Prerequisites:</span></span>  

 <span data-ttu-id="4daa5-210">Setup magazzino:</span><span class="sxs-lookup"><span data-stu-id="4daa5-210">Inventory setup:</span></span>  

-   <span data-ttu-id="4daa5-211">Reg. automatica costi = Sì</span><span class="sxs-lookup"><span data-stu-id="4daa5-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="4daa5-212">Rettifica costo automatica=Sempre</span><span class="sxs-lookup"><span data-stu-id="4daa5-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="4daa5-213">Tipo calcolo costo medio=articolo</span><span class="sxs-lookup"><span data-stu-id="4daa5-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="4daa5-214">Costo medio periodo=Giorno</span><span class="sxs-lookup"><span data-stu-id="4daa5-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="4daa5-215">Setup contabilità generale:</span><span class="sxs-lookup"><span data-stu-id="4daa5-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="4daa5-216">Consenti registraz. da = 1° dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="4daa5-217">Consenti registrazioni fino a = vuoto</span><span class="sxs-lookup"><span data-stu-id="4daa5-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="4daa5-218">Setup utente:</span><span class="sxs-lookup"><span data-stu-id="4daa5-218">User Setup:</span></span>  

-   <span data-ttu-id="4daa5-219">Consenti registraz. da = 1° dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="4daa5-220">Consenti registrazioni fino a = vuoto</span><span class="sxs-lookup"><span data-stu-id="4daa5-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="4daa5-221">Per verificare lo scenario:</span><span class="sxs-lookup"><span data-stu-id="4daa5-221">To test the scenario</span></span>  

1.  <span data-ttu-id="4daa5-222">Creare un addebito articolo:</span><span class="sxs-lookup"><span data-stu-id="4daa5-222">Create item charge:</span></span>  

     <span data-ttu-id="4daa5-223">Unità di misura base = PZ</span><span class="sxs-lookup"><span data-stu-id="4daa5-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="4daa5-224">Metodo di costing = Media</span><span class="sxs-lookup"><span data-stu-id="4daa5-224">Costing Method = Average</span></span>  

     <span data-ttu-id="4daa5-225">Selezionare categorie di registrazione facoltative.</span><span class="sxs-lookup"><span data-stu-id="4daa5-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="4daa5-226">Creare un nuovo ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="4daa5-226">Create new purchase order</span></span>  

     <span data-ttu-id="4daa5-227">Acquistare da - Nr. for.: 10000</span><span class="sxs-lookup"><span data-stu-id="4daa5-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="4daa5-228">Data di registrazione = 15 dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="4daa5-229">Nr. fattura fornitore: 1234</span><span class="sxs-lookup"><span data-stu-id="4daa5-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="4daa5-230">Nella riga ordine di acquisto:</span><span class="sxs-lookup"><span data-stu-id="4daa5-230">On the purchase order line:</span></span>  

     <span data-ttu-id="4daa5-231">Articolo = ADDEBITO</span><span class="sxs-lookup"><span data-stu-id="4daa5-231">Item = CHARGE</span></span>  

     <span data-ttu-id="4daa5-232">Quantità = 1</span><span class="sxs-lookup"><span data-stu-id="4daa5-232">Quantity = 1</span></span>  

     <span data-ttu-id="4daa5-233">Costo unitario diretto = 100</span><span class="sxs-lookup"><span data-stu-id="4daa5-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="4daa5-234">Registrare carico e fattura.</span><span class="sxs-lookup"><span data-stu-id="4daa5-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="4daa5-235">Creare un nuovo ordine di vendita:</span><span class="sxs-lookup"><span data-stu-id="4daa5-235">Create new sales order:</span></span>  

     <span data-ttu-id="4daa5-236">Vendere a - Nr. cliente: 10000</span><span class="sxs-lookup"><span data-stu-id="4daa5-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="4daa5-237">Data di registrazione = 16 dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="4daa5-238">Nella riga dell'ordine di vendita:</span><span class="sxs-lookup"><span data-stu-id="4daa5-238">On the sales order line:</span></span>  

     <span data-ttu-id="4daa5-239">Articolo = ADDEBITO</span><span class="sxs-lookup"><span data-stu-id="4daa5-239">Item = CHARGE</span></span>  

     <span data-ttu-id="4daa5-240">Quantità = 1</span><span class="sxs-lookup"><span data-stu-id="4daa5-240">Quantity = 1</span></span>  

     <span data-ttu-id="4daa5-241">Prezzo unitario = 135</span><span class="sxs-lookup"><span data-stu-id="4daa5-241">Unit Price = 135</span></span>  

     <span data-ttu-id="4daa5-242">Registrare spedizione e fattura.</span><span class="sxs-lookup"><span data-stu-id="4daa5-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="4daa5-243">Setup contabilità generale:</span><span class="sxs-lookup"><span data-stu-id="4daa5-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="4daa5-244">Consenti registraz. da = 1° gennaio 2014</span><span class="sxs-lookup"><span data-stu-id="4daa5-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="4daa5-245">Consenti registrazioni fino a = vuoto</span><span class="sxs-lookup"><span data-stu-id="4daa5-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="4daa5-246">Creare un nuovo ordine di acquisto:</span><span class="sxs-lookup"><span data-stu-id="4daa5-246">Create new purchase order:</span></span>  

     <span data-ttu-id="4daa5-247">Acquistare da - Nr. for.: 10000</span><span class="sxs-lookup"><span data-stu-id="4daa5-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="4daa5-248">Data di registrazione = 2 gennaio 2014</span><span class="sxs-lookup"><span data-stu-id="4daa5-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="4daa5-249">Nr. fattura fornitore: 2345</span><span class="sxs-lookup"><span data-stu-id="4daa5-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="4daa5-250">Nella riga ordine di acquisto:</span><span class="sxs-lookup"><span data-stu-id="4daa5-250">On the purchase order line:</span></span>  

     <span data-ttu-id="4daa5-251">Addebito articolo = COM-SPEDIZ</span><span class="sxs-lookup"><span data-stu-id="4daa5-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="4daa5-252">Quantità = 1</span><span class="sxs-lookup"><span data-stu-id="4daa5-252">Quantity = 1</span></span>  

     <span data-ttu-id="4daa5-253">Costo unitario diretto = 3</span><span class="sxs-lookup"><span data-stu-id="4daa5-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="4daa5-254">Assegnare l'addebito articolo al carico di acquisto del passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="4daa5-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="4daa5-255">Registrare carico e fattura.</span><span class="sxs-lookup"><span data-stu-id="4daa5-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="4daa5-256">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span><span class="sxs-lookup"><span data-stu-id="4daa5-256">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span></span>

6.  <span data-ttu-id="4daa5-257">In data 3 gennaio arriva una fattura di acquisto contenente un ulteriore addebito articolo per l'acquisto effettuato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="4daa5-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="4daa5-258">La data documento di questa fattura è il 30 dicembre e pertanto viene registrata con la data 30 dicembre 2013.</span><span class="sxs-lookup"><span data-stu-id="4daa5-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="4daa5-259">Creare un nuovo ordine di acquisto:</span><span class="sxs-lookup"><span data-stu-id="4daa5-259">Create new purchase order:</span></span>  

     <span data-ttu-id="4daa5-260">Acquistare da - Nr. for.: 10000</span><span class="sxs-lookup"><span data-stu-id="4daa5-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="4daa5-261">Data di registrazione = 30 dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="4daa5-262">Nr. fattura fornitore: 3456</span><span class="sxs-lookup"><span data-stu-id="4daa5-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="4daa5-263">Nella riga ordine di acquisto:</span><span class="sxs-lookup"><span data-stu-id="4daa5-263">On the purchase order line:</span></span>  

     <span data-ttu-id="4daa5-264">Addebito articolo = COM-SPEDIZ</span><span class="sxs-lookup"><span data-stu-id="4daa5-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="4daa5-265">Quantità = 1</span><span class="sxs-lookup"><span data-stu-id="4daa5-265">Quantity = 1</span></span>  

     <span data-ttu-id="4daa5-266">Costo unitario diretto = 2</span><span class="sxs-lookup"><span data-stu-id="4daa5-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="4daa5-267">Assegnare l'addebito articolo al carico di acquisto del passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="4daa5-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="4daa5-268">Registrare carico e fattura.</span><span class="sxs-lookup"><span data-stu-id="4daa5-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="4daa5-269">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span><span class="sxs-lookup"><span data-stu-id="4daa5-269">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span></span>

 <span data-ttu-id="4daa5-270">Il report Valutazione magazzino viene stampato in data 31 dicembre 2013</span><span class="sxs-lookup"><span data-stu-id="4daa5-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="4daa5-271">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span><span class="sxs-lookup"><span data-stu-id="4daa5-271">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span></span>

 <span data-ttu-id="4daa5-272">**Riepilogo dello scenario:**</span><span class="sxs-lookup"><span data-stu-id="4daa5-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="4daa5-273">Lo scenario descritto termina con un report Valutazione magazzino che indica Quantità = 0 quando Valore = 2.</span><span class="sxs-lookup"><span data-stu-id="4daa5-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="4daa5-274">L'addebito articolo registrato nel passaggio 11 fa parte del valore Aumento di magazzino di dicembre mentre la riduzione di magazzino dello stesso periodo non è influenzata.</span><span class="sxs-lookup"><span data-stu-id="4daa5-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="4daa5-275">La data 1° gennaio indicata nel campo Consenti registraz. da del setup di contabilità generale era ideale per il primo addebito articolo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="4daa5-276">I costi dell'aumento e della riduzione di magazzino sono stati registrati nello stesso periodo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="4daa5-277">Per il secondo addebito articolo tuttavia, il setup di contabilità generale posiziona la modifica in COGS nel periodo successivo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="4daa5-278">**Conclusione:**</span><span class="sxs-lookup"><span data-stu-id="4daa5-278">**Conclusion:**</span></span>  

 <span data-ttu-id="4daa5-279">È una sfida dimostrare nel report Valutazione magazzino che Quantità = 0 quando Valore <> 0.</span><span class="sxs-lookup"><span data-stu-id="4daa5-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="4daa5-280">In questo caso è anche più difficile indicare le impostazioni ottimali, in quanto le fatture di acquisto arrivano lo stesso giorno ma fanno riferimento a periodi o persino anni fiscali differenti.</span><span class="sxs-lookup"><span data-stu-id="4daa5-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="4daa5-281">Il passaggio a un nuovo anno fiscale richiede normalmente una pianificazione e in tale ambito le informazioni relative al processo Rettifica costo - Movimenti articoli, che riconosce COGS, devono essere prese in considerazione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="4daa5-282">Come alternativa in questo scenario si sarebbe potuto avere una data in dicembre di un paio di giorni in più nel campo Consenti registraz. da del setup di contabilità generale e differire la registrazione del primo addebito articolo per consentire il riconoscimento di tutti i costi relativi al periodo/anno fiscale per il periodo a cui appartengono inizialmente, quindi eseguire il processo batch Rettifica costo - Movimenti articoli e infine spostare la data di registrazione consentita al nuovo periodo\/anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="4daa5-283">Si sarebbe quindi potuto registrare il primo addebito con la data 2 gennaio.</span><span class="sxs-lookup"><span data-stu-id="4daa5-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="4daa5-284">Cronologia del processo batch Rettifica costo - Movimenti articoli</span><span class="sxs-lookup"><span data-stu-id="4daa5-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="4daa5-285">Di seguito è riportato un riepilogo del concetto che assegna date di registrazione ai movimenti di valorizzazione delle rettifiche mediante il processo batch Rettifica costo – Movimenti articoli versione 3.0.</span><span class="sxs-lookup"><span data-stu-id="4daa5-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="4daa5-286">A partire dalla versione 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="4daa5-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="4daa5-287">Nel form di richiesta del processo batch Rettifica costo - Movimenti articoli l'utente deve immettere una data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="4daa5-288">Il processo batch esamina tutte le modifiche necessarie e crea movimenti di valorizzazione con la data di registrazione immessa nel form di richiesta.</span><span class="sxs-lookup"><span data-stu-id="4daa5-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="4daa5-289">La data di registrazione suggerita da utilizzare è la data corrente.</span><span class="sxs-lookup"><span data-stu-id="4daa5-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="4daa5-290">Versione 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="4daa5-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="4daa5-291">Nel form di richiesta del processo batch Rettifica costo - Movimenti articoli l'utente deve immettere una data di registrazione movimento in periodo chiuso.</span><span class="sxs-lookup"><span data-stu-id="4daa5-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="4daa5-292">Il processo batch esamina tutte le modifiche necessarie e crea movimenti di valorizzazione con la data di registrazione del movimento contabile articolo padre (data di spedizione della vendita a cui si riferisce la rettifica).</span><span class="sxs-lookup"><span data-stu-id="4daa5-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="4daa5-293">Se la data di registrazione del movimento contabile articolo padre non rientra nell'intervallo di date di registrazione consentite, alla data di registrazione indicata come data di registrazione movimento in periodo chiuso verrà assegnato il movimento di valorizzazione della rettifiche.</span><span class="sxs-lookup"><span data-stu-id="4daa5-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="4daa5-294">Una data viene considerata in un periodo chiuso quando è antecedente alla data nel campo Consenti registraz. da del setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="4daa5-295">A partire dalla versione 5.0:</span><span class="sxs-lookup"><span data-stu-id="4daa5-295">From version 5.0:</span></span>  
 <span data-ttu-id="4daa5-296">Non è più necessario indicare una data di registrazione nel modulo di richiesta del processo batch Rettifica costo - Movimenti articoli.</span><span class="sxs-lookup"><span data-stu-id="4daa5-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="4daa5-297">Il processo batch esamina tutte le modifiche necessarie e crea movimenti di valorizzazione con la data di registrazione del movimento di valorizzazione che rettifica.</span><span class="sxs-lookup"><span data-stu-id="4daa5-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="4daa5-298">Se la data di registrazione non rientra nell'intervallo di date di registrazione consentito, viene utilizzata la data di registrazione nel campo Consenti registraz. da del setup di contabilità generale OPPURE, se vengono utilizzati i periodi di magazzino, la data più lontana tra le due.</span><span class="sxs-lookup"><span data-stu-id="4daa5-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="4daa5-299">Vedere il concetto descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4daa5-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="4daa5-300">Cronologia del processo batch Registra costo magazzino in C/G</span><span class="sxs-lookup"><span data-stu-id="4daa5-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="4daa5-301">Il processo batch Registra costo magazzino in C/G è strettamente associato al processo batch Rettifica Costo - Movimenti articoli ed è per questo motivo che la cronologia di questo processo batch è inclusa in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="4daa5-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="4daa5-302">A partire dalla versione 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="4daa5-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="4daa5-303">Nel form di richiesta del processo batch Registra costo magazzino in C/G l'utente deve inserire una data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="4daa5-304">Il processo batch esamina tutti i movimenti di valorizzazione nell'eventuale filtro e crea movimenti C/G con la data di registrazione immessa nel form di richiesta.</span><span class="sxs-lookup"><span data-stu-id="4daa5-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="4daa5-305">Versione 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="4daa5-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="4daa5-306">Nel form di richiesta del processo batch Registra costo magazzino in C/G è disponibile il campo relativo alla data di registrazione movimento in periodo chiuso.</span><span class="sxs-lookup"><span data-stu-id="4daa5-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="4daa5-307">Il programma utilizza la data in questo campo come data di registrazione per i movimenti di contabilità generale che crea per i movimenti di valorizzazione le cui date di registrazione sono in periodi contabili chiusi.</span><span class="sxs-lookup"><span data-stu-id="4daa5-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="4daa5-308">In caso contrario, i movimenti di contabilità generale avranno la stessa data di registrazione dei movimenti di valorizzazione originali.</span><span class="sxs-lookup"><span data-stu-id="4daa5-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="4daa5-309">Una data viene considerata in un periodo chiuso quando è antecedente alla data nel campo Consenti registraz. da del setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="4daa5-310">Se si esegue la registrazione in C\/G per gruppo registrazione, i movimenti di contabilità generale avranno la data di registrazione specificata nel campo Data di registrazione nel form di richiesta.</span><span class="sxs-lookup"><span data-stu-id="4daa5-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="4daa5-311">Nelle versioni 3 e 4 il processo esamina tutti i movimenti di valorizzazione per rilevare se esistono eventuali movimenti di valorizzazione in cui Importo costo (effettivo) differisce da Costo registrato in C/G.</span><span class="sxs-lookup"><span data-stu-id="4daa5-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="4daa5-312">In caso affermativo, la differenza verrà registrata in un movimento C/G.</span><span class="sxs-lookup"><span data-stu-id="4daa5-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="4daa5-313">Se viene utilizzata la registrazione dei costi previsti, i campi corrispondenti vengono elaborati nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="4daa5-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="4daa5-314">![Rettifica costo &#45;Dati movimenti articoli](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span><span class="sxs-lookup"><span data-stu-id="4daa5-314">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="4daa5-315">A partire dalla versione 5.0:</span><span class="sxs-lookup"><span data-stu-id="4daa5-315">From version 5.0:</span></span>  
 <span data-ttu-id="4daa5-316">Non è più necessario indicare una data di registrazione nel modulo di richiesta del processo batch Registra costo magazzino in C/G.</span><span class="sxs-lookup"><span data-stu-id="4daa5-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="4daa5-317">Il movimento C/G viene creato con la stessa data di registrazione del movimento di valorizzazione correlato.</span><span class="sxs-lookup"><span data-stu-id="4daa5-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="4daa5-318">Per completare il processo batch l'intervallo di date di registrazione consentite deve permettere la data di registrazione del movimento C/G creato.</span><span class="sxs-lookup"><span data-stu-id="4daa5-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="4daa5-319">In caso contrario, l'intervallo di date di registrazione consentite deve essere riaperto temporaneamente modificando o rimuovendo le date nei campi Consenti registraz. da e Consenti registrazioni fino a nel setup di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="4daa5-320">Per evitare problemi di riconciliazione la data di registrazione del movimento C/G deve corrispondere alla data di registrazione del movimento di valorizzazione.</span><span class="sxs-lookup"><span data-stu-id="4daa5-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="4daa5-321">Il processo batch esamina la Tabella 5811 - Registra mov. valorizzazione in C/G per identificare i movimenti di valorizzazione nell'ambito della registrazione nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4daa5-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="4daa5-322">Dopo una corretta esecuzione, la tabella viene svuotata.</span><span class="sxs-lookup"><span data-stu-id="4daa5-322">After successful run the table is emptied.</span></span>  

 <span data-ttu-id="4daa5-323">Eventuali suggerimenti su come questo processo e la relativa documentazione possono essere migliorati ulteriormente sono benaccetti.</span><span class="sxs-lookup"><span data-stu-id="4daa5-323">Any feedback to how this process and documentation can be further developed is very welcome.</span></span>  

 <span data-ttu-id="4daa5-324">Helene Holmin</span><span class="sxs-lookup"><span data-stu-id="4daa5-324">Helene Holmin</span></span>  

 <span data-ttu-id="4daa5-325">Ingegnere escalation Dynamics NAV</span><span class="sxs-lookup"><span data-stu-id="4daa5-325">Dynamics NAV Escalation Engineer</span></span>  

## <a name="see-also"></a><span data-ttu-id="4daa5-326">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4daa5-326">See Also</span></span>  
[<span data-ttu-id="4daa5-327">Dettagli di progettazione: Costing di magazzino</span><span class="sxs-lookup"><span data-stu-id="4daa5-327">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="4daa5-328">Dettagli di progettazione: Collegamento articoli</span><span class="sxs-lookup"><span data-stu-id="4daa5-328">Design Details: Item Application</span></span>](design-details-item-application.md)  

