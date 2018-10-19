---
title: Come trasferire movimenti C/G ai movimenti di costi | Microsoft Docs
description: I movimenti C/G possono essere trasferiti ai movimenti di costi.
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="e7a28-103">Trasferire movimenti C/G a movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="e7a28-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="e7a28-104">I movimenti C/G possono essere trasferiti ai movimenti di costi.</span><span class="sxs-lookup"><span data-stu-id="e7a28-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="e7a28-105">Prima di eseguire il processo per il trasferimento dei movimenti C/G ai movimenti di costi, è necessario preparare il trasferimento per evitare la registrazione manuale della correzione.</span><span class="sxs-lookup"><span data-stu-id="e7a28-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="e7a28-106">Per preparare il trasferimento</span><span class="sxs-lookup"><span data-stu-id="e7a28-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="e7a28-107">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità industriale** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e7a28-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e7a28-108">Nella finestra **Setup contabilità industriale** controllare che il campo **Data inizio per trasferimento C/G** sia impostato sul valore corretto.</span><span class="sxs-lookup"><span data-stu-id="e7a28-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="e7a28-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei tipi di costo** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e7a28-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="e7a28-110">Nella finestra **Scheda tipo costo** verificare che il campo **Intervallo conti C/G** sia collegato correttamente per ogni tipo di costo per prelevare i movimenti dalla contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e7a28-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="e7a28-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e7a28-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="e7a28-112">Per ogni conto di contabilità generale pertinente, nella finestra **Scheda conto C/G** verificare che il campo **Nr. tipo di costo**</span><span class="sxs-lookup"><span data-stu-id="e7a28-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="e7a28-113">sia collegato correttamente a un tipo di costo.</span><span class="sxs-lookup"><span data-stu-id="e7a28-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="e7a28-114">Per ulteriori informazioni, vedere [Definizione della relazione tra i tipi di costo e i conti di contabilità generale](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="e7a28-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="e7a28-115">Verificare che a tutti i relativi movimenti C/G siano associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo.</span><span class="sxs-lookup"><span data-stu-id="e7a28-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="e7a28-116">Per trasferire movimenti C/G a movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="e7a28-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="e7a28-117">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Trasferisci movimenti C/G a CA** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e7a28-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e7a28-118">Scegliere **Sì** per avviare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="e7a28-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="e7a28-119">Con il processo vengono trasferiti tutti i movimenti C/G che non sono già stati trasferiti.</span><span class="sxs-lookup"><span data-stu-id="e7a28-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="e7a28-120">Durante il trasferimento, con il processo vengono creati collegamenti nei movimenti nella tabella **Movimento di costo** e nella tabella **Registro costi**.</span><span class="sxs-lookup"><span data-stu-id="e7a28-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="e7a28-121">In questo modo è possibile analizzare l'origine dei movimenti di costi.</span><span class="sxs-lookup"><span data-stu-id="e7a28-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e7a28-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7a28-122">See Also</span></span>  
 <span data-ttu-id="e7a28-123">[Criteri per trasferire movimenti C/G ai movimenti di costi](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="e7a28-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="e7a28-124">[Trasferimento automatico e movimenti combinati](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="e7a28-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="e7a28-125">[Risultati del trasferimento](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="e7a28-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="e7a28-126">[Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="e7a28-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="e7a28-127">Definizione della relazione tra i tipi di costo e i conti di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="e7a28-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

