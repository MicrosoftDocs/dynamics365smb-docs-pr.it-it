---
title: Importare transazioni retribuzioni| Documenti Microsoft
description: "Per gestire lo stipendio, importare e registrare le transazioni finanziarie dal provider di retribuzioni nella contabilità generale, utilizzando un'estensione di retribuzione quale Ceridian o Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45ac64abac2a604eb4f669dd3c246b59f05f4d31
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="import-payroll-transactions"></a><span data-ttu-id="e1acf-103">Importa transazioni retribuzioni</span><span class="sxs-lookup"><span data-stu-id="e1acf-103">Import Payroll Transactions</span></span>
<span data-ttu-id="e1acf-104">Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="e1acf-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="e1acf-105">A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella finestra **Contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="e1acf-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="e1acf-106">Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e1acf-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="e1acf-107">Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.</span><span class="sxs-lookup"><span data-stu-id="e1acf-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e1acf-108">Per utilizzare questa funzione, è necessario installare e abilitare un'estensione per l'importazione delle retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="e1acf-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="e1acf-109">Il Registro paga di Ceridian e le estensioni per l'importazione del file retribuzioni di Quickbooks sono preinstallati in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e1acf-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e1acf-110">Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e1acf-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="e1acf-111">Per importare un file delle retribuzioni</span><span class="sxs-lookup"><span data-stu-id="e1acf-111">To import a payroll file</span></span>
1. <span data-ttu-id="e1acf-112">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e1acf-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e1acf-113">Nel batch registrazioni COGE appropriato scegliere l'azione **Importa transazioni retribuzioni**.</span><span class="sxs-lookup"><span data-stu-id="e1acf-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="e1acf-114">Si apre una guida al setup assistito.</span><span class="sxs-lookup"><span data-stu-id="e1acf-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="e1acf-115">Seguire i passaggi indicati nella finestra **Importa transazioni retribuzioni**.</span><span class="sxs-lookup"><span data-stu-id="e1acf-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
>   <span data-ttu-id="e1acf-116">Nel passaggio relativo alla mappatura dei record di retribuzione esterni ai conti C/G, i mapping eseguiti verranno ricordati che la successiva importazione degli stessi record.</span><span class="sxs-lookup"><span data-stu-id="e1acf-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="e1acf-117">In questo modo si risparmia tempo in quando non occorre compilare manualmente il campo **Nr. conto** nelle registrazioni COGE ogni volta che si importano transazioni retribuzioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="e1acf-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="e1acf-118">Se si sceglie il pulsante **OK** nella guida al setup assistito, la finestra **Contabilità generale** viene popolata con le righe che rappresentano le transazioni che contiene il file retribuzioni e con i conti appropriati già precompilati nei campi **Conto C/G** in base ai mapping effettuati nella guida.</span><span class="sxs-lookup"><span data-stu-id="e1acf-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="e1acf-119">Modificare o registrare le righe delle registrazioni relative a tutte le altre le transazioni della contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e1acf-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="e1acf-120">Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="e1acf-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="e1acf-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1acf-121">See Also</span></span>
[<span data-ttu-id="e1acf-122">Finanze</span><span class="sxs-lookup"><span data-stu-id="e1acf-122">Finance</span></span>](finance.md)  
<span data-ttu-id="e1acf-123">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e1acf-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="e1acf-124">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="e1acf-124">Working with General Journals</span></span>](ui-work-general-journals.md)  

