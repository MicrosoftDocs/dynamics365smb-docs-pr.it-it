---
title: 'Procedura: Chiusura di un anno fiscale'
description: Per valutare i profitti e le perdite, alla fine di ogni anno fiscale viene fornito un report di chiusura dell'anno fiscale.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 027a2d836fe791d2d13b7833d4e735b63f1e0689
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382909"
---
# <a name="close-a-fiscal-year"></a><span data-ttu-id="2389a-103">Chiusura di un anno fiscale</span><span class="sxs-lookup"><span data-stu-id="2389a-103">Close a Fiscal Year</span></span>
<span data-ttu-id="2389a-104">Per valutare i profitti e le perdite, alla fine di ogni anno fiscale viene fornito un report di chiusura dell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="2389a-104">To evaluate profit and loss, a fiscal year closing report is provided at the end of each fiscal year.</span></span>  

<span data-ttu-id="2389a-105">La chiusura dell'anno fiscale include i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="2389a-105">Fiscal year closing involves the following steps:</span></span>  

- <span data-ttu-id="2389a-106">Chiusura dell'anno fiscale utilizzando l'opzione **Periodo contabile**.</span><span class="sxs-lookup"><span data-stu-id="2389a-106">Closing the fiscal year using the **Accounting Period** option.</span></span>  
- <span data-ttu-id="2389a-107">Generazione di un movimento di chiusura di fine anno utilizzando l'opzione **Chiudi conto economico**.</span><span class="sxs-lookup"><span data-stu-id="2389a-107">Generating a year-end closing entry using the **Close Income Statement** option.</span></span>  
- <span data-ttu-id="2389a-108">Registrazione del movimento di chiusura di fine anno.</span><span class="sxs-lookup"><span data-stu-id="2389a-108">Posting the year-end closing entry.</span></span>  

## <a name="to-close-a-fiscal-year"></a><span data-ttu-id="2389a-109">Per chiudere un anno fiscale</span><span class="sxs-lookup"><span data-stu-id="2389a-109">To close a fiscal year</span></span>  

1.  <span data-ttu-id="2389a-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Periodi contabili** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="2389a-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2389a-111">Per chiudere un periodo contabile, selezionare il periodo contabile, quindi scegliere l'azione **Chiudi anno**.</span><span class="sxs-lookup"><span data-stu-id="2389a-111">To close an accounting period, select the accounting period, and then choose the **Close Year** action.</span></span>  
3.  <span data-ttu-id="2389a-112">Selezionare il pulsante **Sì** per confermare che si desidera chiudere l'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="2389a-112">To confirm that you want to close the fiscal year, choose the **Yes** button.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="2389a-113">Dopo la chiusura dell'anno fiscale, non sarà possibile riaprilo, né modificare il periodo nell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="2389a-113">After the fiscal year is closed it cannot be opened again, and the period in the fiscal year cannot be changed.</span></span>  

## <a name="to-generate-a-year-end-closing-entry-using-the-close-income-statement-option"></a><span data-ttu-id="2389a-114">Per generare un movimento di chiusura di fine anno utilizzando l'opzione Chiudi conto economico</span><span class="sxs-lookup"><span data-stu-id="2389a-114">To generate a year-end closing entry using the Close Income Statement option</span></span>  

1.  <span data-ttu-id="2389a-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Chiudi conto economico** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="2389a-115">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Close Income Statement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2389a-116">Compilare i campi nella scheda **Opzioni** come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="2389a-116">On the **Options** tab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2389a-117">Campo</span><span class="sxs-lookup"><span data-stu-id="2389a-117">Field</span></span>|<span data-ttu-id="2389a-118">Description</span><span class="sxs-lookup"><span data-stu-id="2389a-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2389a-119">**Data fine anno fiscale**</span><span class="sxs-lookup"><span data-stu-id="2389a-119">**Fiscal Year Ending Date**</span></span>|<span data-ttu-id="2389a-120">Data di fine dell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="2389a-120">The ending date for the fiscal year.</span></span>|  
    |<span data-ttu-id="2389a-121">**Def. Registrazioni Generali**</span><span class="sxs-lookup"><span data-stu-id="2389a-121">**Gen. Journal Template**</span></span>|<span data-ttu-id="2389a-122">Nome della definizione di registrazioni COGE in cui collocare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="2389a-122">The name of the general journal template in which to place the entries.</span></span>|  
    |<span data-ttu-id="2389a-123">**Batch Reg. Generali**</span><span class="sxs-lookup"><span data-stu-id="2389a-123">**Gen. Journal Batch**</span></span>|<span data-ttu-id="2389a-124">Nome del batch di registrazioni COGE in cui collocare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="2389a-124">The name of the general journal batch in which to place the entries.</span></span>|  
    |<span data-ttu-id="2389a-125">**Nr. conto profitti/perdite**</span><span class="sxs-lookup"><span data-stu-id="2389a-125">**Balancing Account No.**</span></span>|<span data-ttu-id="2389a-126">Selezionare il numero di conto pertinente.</span><span class="sxs-lookup"><span data-stu-id="2389a-126">Select the relevant account number.</span></span>|  
    |<span data-ttu-id="2389a-127">**Nr. Documento**</span><span class="sxs-lookup"><span data-stu-id="2389a-127">**Document No.**</span></span>|<span data-ttu-id="2389a-128">In questo campo viene inserito automaticamente il successivo numero disponibile nel batch di registrazioni, se si specifica un valore nei campi **Def. registrazioni COGE** e **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="2389a-128">The batch job automatically populates this field with the next available number for the journal batch if you fill in the **Gen. Journal Template** and **Gen. Journal Batch** fields.</span></span> <span data-ttu-id="2389a-129">È anche possibile immettere manualmente un numero in questo campo.</span><span class="sxs-lookup"><span data-stu-id="2389a-129">You can also enter a number into this field manually.</span></span>|  
    |<span data-ttu-id="2389a-130">**Nr. conto utili d'esercizio**</span><span class="sxs-lookup"><span data-stu-id="2389a-130">**Net Profit Account No.**</span></span>|<span data-ttu-id="2389a-131">Selezionare il numero univoco del conto utili d'esercizio.</span><span class="sxs-lookup"><span data-stu-id="2389a-131">Select the unique net profit account number.</span></span>|  
    |<span data-ttu-id="2389a-132">**Nr. conto perdite d'esercizio**</span><span class="sxs-lookup"><span data-stu-id="2389a-132">**Net Loss Account No.**</span></span>|<span data-ttu-id="2389a-133">Selezionare il numero univoco del conto perdite d'esercizio.</span><span class="sxs-lookup"><span data-stu-id="2389a-133">Select the unique net loss account number.</span></span>|  
    |<span data-ttu-id="2389a-134">**Descr. registrazione**</span><span class="sxs-lookup"><span data-stu-id="2389a-134">**Posting Description**</span></span>|<span data-ttu-id="2389a-135">Immettere una descrizione.</span><span class="sxs-lookup"><span data-stu-id="2389a-135">Enter a description.</span></span> <span data-ttu-id="2389a-136">Il testo predefinito è **Chiudi conto economico**.</span><span class="sxs-lookup"><span data-stu-id="2389a-136">The default text is **Close Income Statement**.</span></span>|  
    |<span data-ttu-id="2389a-137">**Cod. business unit**</span><span class="sxs-lookup"><span data-stu-id="2389a-137">**Business Unit Code**</span></span>|<span data-ttu-id="2389a-138">Selezionare questa caselle di controllo se è necessario un movimento per ogni codice di business unit.</span><span class="sxs-lookup"><span data-stu-id="2389a-138">Select this check box if you require an entry for each business unit code.</span></span>|  
    |<span data-ttu-id="2389a-139">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="2389a-139">**Dimensions**</span></span>|<span data-ttu-id="2389a-140">Facoltativamente selezionare il campo per scegliere i codici di dimensione se è necessario un movimento per ogni dimensione utilizzata nel conto C/G.</span><span class="sxs-lookup"><span data-stu-id="2389a-140">Optionally, select the field to select the dimension codes if you require an entry for each dimension used in the general ledger account.</span></span>|  
    |<span data-ttu-id="2389a-141">**Chiusura periodo magazzino**</span><span class="sxs-lookup"><span data-stu-id="2389a-141">**Inventory Period Closed**</span></span>|<span data-ttu-id="2389a-142">Questo campo indica che i periodi di magazzino con date di fine successive o corrispondenti all'ultima data del periodo contabile sono chiusi.</span><span class="sxs-lookup"><span data-stu-id="2389a-142">This field indicates that the inventory periods with ending dates greater than or equal to the last date of the accounting period are closed.</span></span>|  

3.  <span data-ttu-id="2389a-143">Scegliere il pulsante **OK** per creare le scritture contabili.</span><span class="sxs-lookup"><span data-stu-id="2389a-143">Choose the **OK**  button to create the journal entries.</span></span>  

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="2389a-144">Per registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="2389a-144">To post the year-end closing entry</span></span>  

1.  <span data-ttu-id="2389a-145">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="2389a-145">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2389a-146">Nel campo **Batch** specificare il batch contenente i movimenti di chiusura.</span><span class="sxs-lookup"><span data-stu-id="2389a-146">In the **Batch** field, specify the batch that contains the closing entries.</span></span>  
3.  <span data-ttu-id="2389a-147">Aggiungere i movimenti corrispondenti alle righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2389a-147">Add the relevant entries to the journal lines.</span></span>  
4.  <span data-ttu-id="2389a-148">Per contabilizzare le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="2389a-148">To post the journal, choose the **Post** action.</span></span>  

<span data-ttu-id="2389a-149">Viene registrato un movimento in ogni conto economico in modo che il saldo sia zero.</span><span class="sxs-lookup"><span data-stu-id="2389a-149">An entry is posted to each income statement account so that it has a zero balance.</span></span> <span data-ttu-id="2389a-150">Il risultato di fine anno viene trasferito nel conto patrimoniale.</span><span class="sxs-lookup"><span data-stu-id="2389a-150">The year-end result is transferred to the balance sheet.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2389a-151">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2389a-151">See Also</span></span>  
 <span data-ttu-id="2389a-152">[Chiusura di anni e periodi](../../year-close-years-periods.md) </span><span class="sxs-lookup"><span data-stu-id="2389a-152">[Closing Years and Periods](../../year-close-years-periods.md) </span></span>  
 [<span data-ttu-id="2389a-153">Funzionalità locale per l'Italia</span><span class="sxs-lookup"><span data-stu-id="2389a-153">Italy Local Functionality</span></span>](italy-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]