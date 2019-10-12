---
title: 'Procedura: Correggere i report di transazioni IVA'
description: È possibile correggere e inviare nuovamente i report di transazioni IVA.
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
ms.openlocfilehash: feea7c992e87690bbe70ea860021ab33415811c2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300169"
---
# <a name="correct-vat-transactions-reports"></a><span data-ttu-id="1c03b-103">Correggere i report di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="1c03b-103">Correct VAT Transactions Reports</span></span>

1.  <span data-ttu-id="1c03b-104">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Report IVA** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1c03b-104">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Reports**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1c03b-105">Creare un nuovo report.</span><span class="sxs-lookup"><span data-stu-id="1c03b-105">Create a new report.</span></span> <span data-ttu-id="1c03b-106">Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).</span><span class="sxs-lookup"><span data-stu-id="1c03b-106">For more information, see [Create Electronic VAT Transactions Reports](how-to-create-electronic-vat-transactions-reports.md).</span></span>  
3.  <span data-ttu-id="1c03b-107">Nel nuovo report, impostare il campo **Tipo report IVA** su **Correttiva** o **Annullamento**.</span><span class="sxs-lookup"><span data-stu-id="1c03b-107">In the new report, change the **VAT Report Type** field to **Corrective** or **Cancellation**.</span></span> <span data-ttu-id="1c03b-108">Nel campo **Nr. report originale**</span><span class="sxs-lookup"><span data-stu-id="1c03b-108">In the **Original Report No.**</span></span> <span data-ttu-id="1c03b-109">selezionare il report che si desidera correggere dalla lista dei report disponibili.</span><span class="sxs-lookup"><span data-stu-id="1c03b-109">field, select the report that you want to correct from the list of available reports.</span></span> <span data-ttu-id="1c03b-110">I campi **Data di fine** e **Data di inizio** vengono copiati dal report originale.</span><span class="sxs-lookup"><span data-stu-id="1c03b-110">The **Start Date** and **End Date** fields are copied from the original report.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1c03b-111">È possibile selezionare soltanto i report IVA che risultano contrassegnati come inviati, in quanto è necessario che il report originale abbia un **Nr. ricevuta ufficio fiscale**</span><span class="sxs-lookup"><span data-stu-id="1c03b-111">You can only select VAT reports that are marked as Submitted, as it is required that the original report has a **Tax Auth. Receipt No.**</span></span>  
    >   
    >  <span data-ttu-id="1c03b-112">Se si tratta di un report correttivo, nella scheda **Pagina iniziale**, nel gruppo **Processo**, scegliere **Suggerisci righe** per ottenere i movimenti IVA corrispondenti per il periodo.</span><span class="sxs-lookup"><span data-stu-id="1c03b-112">If it is a corrective report, on the **Home** tab, in the **Process** group, choose **Suggest Lines** to get the relevant VAT entries for the period.</span></span> <span data-ttu-id="1c03b-113">In un report di annullamento non sono incluse righe.</span><span class="sxs-lookup"><span data-stu-id="1c03b-113">A cancellation report does not contain any lines.</span></span>  
    >   
    >  <span data-ttu-id="1c03b-114">Le righe suggerite sono basate sui movimenti IVA all'interno del periodo specificato e sul setup corrente della soglia.</span><span class="sxs-lookup"><span data-stu-id="1c03b-114">The suggested lines are based on the VAT entries within the specified period and the current threshold setup.</span></span> <span data-ttu-id="1c03b-115">Non è correlato alle informazioni del report originale.</span><span class="sxs-lookup"><span data-stu-id="1c03b-115">It is not correlated with the information from the original report.</span></span>  

4.  <span data-ttu-id="1c03b-116">Esaminare i dettagli della transazione.</span><span class="sxs-lookup"><span data-stu-id="1c03b-116">Review the transaction details.</span></span> <span data-ttu-id="1c03b-117">Per evitare che una riga venga dichiarata all'autorità fiscale, nella riga, deselezionare la casella di controllo **Elementi inclusi in report**.</span><span class="sxs-lookup"><span data-stu-id="1c03b-117">To exclude a line from being reported to the tax authority, on the line, clear the **Incl. in Report** check box.</span></span>  

    <span data-ttu-id="1c03b-118">Scegliere l'azione **Esporta**.</span><span class="sxs-lookup"><span data-stu-id="1c03b-118">Choose the **Export** action.</span></span> <span data-ttu-id="1c03b-119">Il processo batch **Esporta transazioni IVA** viene aperto.</span><span class="sxs-lookup"><span data-stu-id="1c03b-119">The **Export VAT Transactions** batch job opens.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1c03b-120">Scegliendo **Esporta** per un report con lo stato Aperto, verrà convalidato automaticamente e lo stato verrà modificato in Rilasciato.</span><span class="sxs-lookup"><span data-stu-id="1c03b-120">When you choose **Export** for a report with the status Open, it will be automatically validated and the status will be changed to Released.</span></span> <span data-ttu-id="1c03b-121">A questo punto, è possibile riaprire il report per apportare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1c03b-121">At this point, you can reopen the report to make changes.</span></span>  

5.  <span data-ttu-id="1c03b-122">Inviare il file all'autorità competente.</span><span class="sxs-lookup"><span data-stu-id="1c03b-122">Submit the file to the authority.</span></span> <span data-ttu-id="1c03b-123">Utilizzare le indicazioni fornite dall'autorità.</span><span class="sxs-lookup"><span data-stu-id="1c03b-123">Use the guidelines provided by the authority.</span></span> <span data-ttu-id="1c03b-124">Per ulteriori informazioni, vedere l'[agenzia delle entrate italiana](https://go.microsoft.com/fwlink/?LinkID=206524).</span><span class="sxs-lookup"><span data-stu-id="1c03b-124">For more information, see the [Italian Revenue Agency](https://go.microsoft.com/fwlink/?LinkID=206524).</span></span>  

    <span data-ttu-id="1c03b-125">Una volta ricevuta una risposta dalle autorità fiscali, è necessario aggiornare il report IVA.</span><span class="sxs-lookup"><span data-stu-id="1c03b-125">After you receive a response from the tax authorities, you must update the VAT report.</span></span>  

6.  <span data-ttu-id="1c03b-126">Nella Scheda dettaglio **Generale** nel campo **Nr. ricevuta ufficio fiscale**</span><span class="sxs-lookup"><span data-stu-id="1c03b-126">On the **General** FastTab, in the **Tax Auth. Receipt No.**</span></span> <span data-ttu-id="1c03b-127">specificare il numero di carico ricevuto dalle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="1c03b-127">field, specify the receipt number that you received from the tax authorities.</span></span>  
7.  <span data-ttu-id="1c03b-128">Scegliere l'azione **Contrassegna come inviato** per completare il report.</span><span class="sxs-lookup"><span data-stu-id="1c03b-128">Choose the **Mark as Submitted** action to finalize the report.</span></span> <span data-ttu-id="1c03b-129">Il valore del campo **Stato** diventa Inviato.</span><span class="sxs-lookup"><span data-stu-id="1c03b-129">The **Status** field is updated to Submitted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1c03b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c03b-130">See Also</span></span>  
 [<span data-ttu-id="1c03b-131">Esportare i report di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="1c03b-131">Export VAT Transactions Reports</span></span>](how-to-export-vat-transactions-reports.md)
