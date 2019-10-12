---
title: 'Procedura: Chiusura di un anno fiscale'
description: Per valutare i profitti e le perdite, alla fine di ogni anno fiscale viene fornito un report di chiusura dell'anno fiscale.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9c5e616778d5fb2d036cabebf8fb5d1c7178d764
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301305"
---
# <a name="close-a-fiscal-year"></a><span data-ttu-id="9d826-103">Chiusura di un anno fiscale</span><span class="sxs-lookup"><span data-stu-id="9d826-103">Close a Fiscal Year</span></span>
<span data-ttu-id="9d826-104">Per valutare i profitti e le perdite, alla fine di ogni anno fiscale viene fornito un report di chiusura dell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="9d826-104">To evaluate profit and loss, a fiscal year closing report is provided at the end of each fiscal year.</span></span>  

<span data-ttu-id="9d826-105">La chiusura dell'anno fiscale include i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="9d826-105">Fiscal year closing involves the following steps:</span></span>  

- <span data-ttu-id="9d826-106">Chiusura dell'anno fiscale utilizzando l'opzione **Periodo contabile**.</span><span class="sxs-lookup"><span data-stu-id="9d826-106">Closing the fiscal year using the **Accounting Period** option.</span></span>  
- <span data-ttu-id="9d826-107">Generazione di un movimento di chiusura di fine anno utilizzando l'opzione **Chiudi conto economico**.</span><span class="sxs-lookup"><span data-stu-id="9d826-107">Generating a year-end closing entry using the **Close Income Statement** option.</span></span>  
- <span data-ttu-id="9d826-108">Registrazione del movimento di chiusura di fine anno.</span><span class="sxs-lookup"><span data-stu-id="9d826-108">Posting the year-end closing entry.</span></span>  

## <a name="to-close-a-fiscal-year"></a><span data-ttu-id="9d826-109">Per chiudere un anno fiscale</span><span class="sxs-lookup"><span data-stu-id="9d826-109">To close a fiscal year</span></span>  

1.  <span data-ttu-id="9d826-110">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Periodi contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9d826-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9d826-111">Per chiudere un periodo contabile, selezionare il periodo contabile, quindi scegliere l'azione **Chiudi anno**.</span><span class="sxs-lookup"><span data-stu-id="9d826-111">To close an accounting period, select the accounting period, and then choose the **Close Year** action.</span></span>  
3.  <span data-ttu-id="9d826-112">Selezionare il pulsante **Sì** per confermare che si desidera chiudere l'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="9d826-112">To confirm that you want to close the fiscal year, choose the **Yes** button.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="9d826-113">Dopo la chiusura dell'anno fiscale, non sarà possibile riaprilo, né modificare il periodo nell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="9d826-113">After the fiscal year is closed it cannot be opened again, and the period in the fiscal year cannot be changed.</span></span>  

## <a name="to-generate-a-year-end-closing-entry-using-the-close-income-statement-option"></a><span data-ttu-id="9d826-114">Per generare un movimento di chiusura di fine anno utilizzando l'opzione Chiudi conto economico</span><span class="sxs-lookup"><span data-stu-id="9d826-114">To generate a year-end closing entry using the Close Income Statement option</span></span>  

1.  <span data-ttu-id="9d826-115">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Chiudi conto economico**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9d826-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9d826-116">Compilare i campi nella scheda **Opzioni** come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="9d826-116">On the **Options** tab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9d826-117">Campo</span><span class="sxs-lookup"><span data-stu-id="9d826-117">Field</span></span>|<span data-ttu-id="9d826-118">Description</span><span class="sxs-lookup"><span data-stu-id="9d826-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9d826-119">**Data fine anno fiscale**</span><span class="sxs-lookup"><span data-stu-id="9d826-119">**Fiscal Year Ending Date**</span></span>|<span data-ttu-id="9d826-120">Data di fine dell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="9d826-120">The ending date for the fiscal year.</span></span>|  
    |<span data-ttu-id="9d826-121">**Def. Registrazioni Generali**</span><span class="sxs-lookup"><span data-stu-id="9d826-121">**Gen. Journal Template**</span></span>|<span data-ttu-id="9d826-122">Nome della definizione di registrazioni COGE in cui collocare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="9d826-122">The name of the general journal template in which to place the entries.</span></span>|  
    |<span data-ttu-id="9d826-123">**Batch Reg. Generali**</span><span class="sxs-lookup"><span data-stu-id="9d826-123">**Gen. Journal Batch**</span></span>|<span data-ttu-id="9d826-124">Nome del batch di registrazioni COGE in cui collocare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="9d826-124">The name of the general journal batch in which to place the entries.</span></span>|  
    |<span data-ttu-id="9d826-125">**Nr. conto profitti/perdite**</span><span class="sxs-lookup"><span data-stu-id="9d826-125">**Balancing Account No.**</span></span>|<span data-ttu-id="9d826-126">Selezionare il numero di conto pertinente.</span><span class="sxs-lookup"><span data-stu-id="9d826-126">Select the relevant account number.</span></span>|  
    |<span data-ttu-id="9d826-127">**Nr. Documento**</span><span class="sxs-lookup"><span data-stu-id="9d826-127">**Document No.**</span></span>|<span data-ttu-id="9d826-128">In questo campo viene inserito automaticamente il successivo numero disponibile nel batch di registrazioni, se si specifica un valore nei campi **Def. registrazioni COGE** e **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="9d826-128">The batch job automatically populates this field with the next available number for the journal batch if you fill in the **Gen. Journal Template** and **Gen. Journal Batch** fields.</span></span> <span data-ttu-id="9d826-129">È anche possibile immettere manualmente un numero in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9d826-129">You can also enter a number into this field manually.</span></span>|  
    |<span data-ttu-id="9d826-130">**Nr. conto utili d'esercizio**</span><span class="sxs-lookup"><span data-stu-id="9d826-130">**Net Profit Account No.**</span></span>|<span data-ttu-id="9d826-131">Selezionare il numero univoco del conto utili d'esercizio.</span><span class="sxs-lookup"><span data-stu-id="9d826-131">Select the unique net profit account number.</span></span>|  
    |<span data-ttu-id="9d826-132">**Nr. conto perdite d'esercizio**</span><span class="sxs-lookup"><span data-stu-id="9d826-132">**Net Loss Account No.**</span></span>|<span data-ttu-id="9d826-133">Selezionare il numero univoco del conto perdite d'esercizio.</span><span class="sxs-lookup"><span data-stu-id="9d826-133">Select the unique net loss account number.</span></span>|  
    |<span data-ttu-id="9d826-134">**Descr. registrazione**</span><span class="sxs-lookup"><span data-stu-id="9d826-134">**Posting Description**</span></span>|<span data-ttu-id="9d826-135">Immettere una descrizione.</span><span class="sxs-lookup"><span data-stu-id="9d826-135">Enter a description.</span></span> <span data-ttu-id="9d826-136">Il testo predefinito è **Chiudi conto economico**.</span><span class="sxs-lookup"><span data-stu-id="9d826-136">The default text is **Close Income Statement**.</span></span>|  
    |<span data-ttu-id="9d826-137">**Cod. business unit**</span><span class="sxs-lookup"><span data-stu-id="9d826-137">**Business Unit Code**</span></span>|<span data-ttu-id="9d826-138">Selezionare questa caselle di controllo se è necessario un movimento per ogni codice di business unit.</span><span class="sxs-lookup"><span data-stu-id="9d826-138">Select this check box if you require an entry for each business unit code.</span></span>|  
    |<span data-ttu-id="9d826-139">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="9d826-139">**Dimensions**</span></span>|<span data-ttu-id="9d826-140">Facoltativamente selezionare il campo per scegliere i codici di dimensione se è necessario un movimento per ogni dimensione utilizzata nel conto C/G.</span><span class="sxs-lookup"><span data-stu-id="9d826-140">Optionally, select the field to select the dimension codes if you require an entry for each dimension used in the general ledger account.</span></span>|  
    |<span data-ttu-id="9d826-141">**Chiusura periodo magazzino**</span><span class="sxs-lookup"><span data-stu-id="9d826-141">**Inventory Period Closed**</span></span>|<span data-ttu-id="9d826-142">Questo campo indica che i periodi di magazzino con date di fine successive o corrispondenti all'ultima data del periodo contabile sono chiusi.</span><span class="sxs-lookup"><span data-stu-id="9d826-142">This field indicates that the inventory periods with ending dates greater than or equal to the last date of the accounting period are closed.</span></span>|  

3.  <span data-ttu-id="9d826-143">Scegliere il pulsante **OK** per creare le scritture contabili.</span><span class="sxs-lookup"><span data-stu-id="9d826-143">Choose the **OK**  button to create the journal entries.</span></span>  

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="9d826-144">Per registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="9d826-144">To post the year-end closing entry</span></span>  

1.  <span data-ttu-id="9d826-145">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9d826-145">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9d826-146">Nel campo **Batch** specificare il batch contenente i movimenti di chiusura.</span><span class="sxs-lookup"><span data-stu-id="9d826-146">In the **Batch** field, specify the batch that contains the closing entries.</span></span>  
3.  <span data-ttu-id="9d826-147">Aggiungere i movimenti corrispondenti alle righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9d826-147">Add the relevant entries to the journal lines.</span></span>  
4.  <span data-ttu-id="9d826-148">Per contabilizzare le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="9d826-148">To post the journal, choose the **Post** action.</span></span>  

<span data-ttu-id="9d826-149">Viene registrato un movimento in ogni conto economico in modo che il saldo sia zero.</span><span class="sxs-lookup"><span data-stu-id="9d826-149">An entry is posted to each income statement account so that it has a zero balance.</span></span> <span data-ttu-id="9d826-150">Il risultato di fine anno viene trasferito nel conto patrimoniale.</span><span class="sxs-lookup"><span data-stu-id="9d826-150">The year-end result is transferred to the balance sheet.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d826-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d826-151">See Also</span></span>  
 <span data-ttu-id="9d826-152">[Chiusura di anni e periodi](../../year-close-years-periods.md) </span><span class="sxs-lookup"><span data-stu-id="9d826-152">[Closing Years and Periods](../../year-close-years-periods.md) </span></span>  
 [<span data-ttu-id="9d826-153">Funzionalità locale per l'Italia</span><span class="sxs-lookup"><span data-stu-id="9d826-153">Italy Local Functionality</span></span>](italy-local-functionality.md)
