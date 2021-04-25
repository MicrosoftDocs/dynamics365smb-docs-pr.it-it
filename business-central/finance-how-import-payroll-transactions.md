---
title: Importare transazioni retribuzioni| Documenti Microsoft
description: Per gestire lo stipendio, importare e registrare le transazioni finanziarie dal provider di retribuzioni nella contabilità generale, utilizzando un'estensione di retribuzione quale Ceridian o Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2bd2408152cac52be5e2b22e6568600ceeb96f6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781583"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="e1959-103">Importa transazioni retribuzioni</span><span class="sxs-lookup"><span data-stu-id="e1959-103">Import Payroll Transactions</span></span>
<span data-ttu-id="e1959-104">Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="e1959-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="e1959-105">A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella pagina **Contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="e1959-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="e1959-106">Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e1959-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="e1959-107">Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.</span><span class="sxs-lookup"><span data-stu-id="e1959-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e1959-108">Per utilizzare questa funzione, è necessario installare e abilitare un'estensione per l'importazione delle retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="e1959-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="e1959-109">Il Registro paga di Ceridian e le estensioni per l'importazione del file retribuzioni di Quickbooks sono preinstallati in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e1959-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e1959-110">Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e1959-110">For more information, see [Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="e1959-111">Per importare un file delle retribuzioni</span><span class="sxs-lookup"><span data-stu-id="e1959-111">To import a payroll file</span></span>
1. <span data-ttu-id="e1959-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e1959-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e1959-113">Nel batch registrazioni COGE appropriato scegliere l'azione **Importa transazioni retribuzioni**.</span><span class="sxs-lookup"><span data-stu-id="e1959-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="e1959-114">Si apre una guida al setup assistito.</span><span class="sxs-lookup"><span data-stu-id="e1959-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="e1959-115">Seguire i passaggi indicati nella pagina **Importa transazioni retribuzioni**.</span><span class="sxs-lookup"><span data-stu-id="e1959-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="e1959-116">Nel passaggio relativo alla mappatura dei record di retribuzione esterni ai conti C/G, i mapping eseguiti verranno ricordati che la successiva importazione degli stessi record.</span><span class="sxs-lookup"><span data-stu-id="e1959-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="e1959-117">In questo modo si risparmia tempo in quando non occorre compilare manualmente il campo **Nr. conto** nelle registrazioni COGE ogni volta che si importano transazioni retribuzioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="e1959-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="e1959-118">Se si sceglie il pulsante **OK** nella guida al setup assistito, la pagina **Contabilità generale** viene popolata con le righe che rappresentano le transazioni che contiene il file retribuzioni e con i conti appropriati già precompilati nei campi **Conto C/G** in base ai mapping effettuati nella guida.</span><span class="sxs-lookup"><span data-stu-id="e1959-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="e1959-119">Modificare o registrare le righe delle registrazioni relative a tutte le altre le transazioni della contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e1959-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="e1959-120">Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="e1959-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="e1959-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1959-121">See Also</span></span>
[<span data-ttu-id="e1959-122">Finanze</span><span class="sxs-lookup"><span data-stu-id="e1959-122">Finance</span></span>](finance.md)  
<span data-ttu-id="e1959-123">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e1959-123">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="e1959-124">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="e1959-124">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]