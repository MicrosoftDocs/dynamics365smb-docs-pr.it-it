---
title: Impostazione del piano dei conti| Documenti Microsoft
description: "È possibile modificare i conti predefiniti nel piano dei conti ed è possibile aggiungere nuovi conti."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ceb01999525139cabc7c31e2304f738dcc9267f8
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="29ba7-103">Impostazione o modifica del piano dei conti</span><span class="sxs-lookup"><span data-stu-id="29ba7-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="29ba7-104">Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari.</span><span class="sxs-lookup"><span data-stu-id="29ba7-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]<span data-ttu-id="29ba7-105"> include un piano dei conti standard pronto per supportare l'azienda.</span><span class="sxs-lookup"><span data-stu-id="29ba7-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="29ba7-106">Tuttavia, è possibile modificare i conti predefiniti ed è possibile aggiungere nuovi conti.</span><span class="sxs-lookup"><span data-stu-id="29ba7-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="29ba7-107">Aggiungere o modificare i conti</span><span class="sxs-lookup"><span data-stu-id="29ba7-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="29ba7-108">Nel piano dei conti, è possibile aprire ogni conto C/G e aggiungere o modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="29ba7-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="29ba7-109">È possibile eliminare un conto di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="29ba7-109">You can delete a general ledger account.</span></span> <span data-ttu-id="29ba7-110">Tuttavia, prima che venga eliminato, è necessario soddisfare le seguenti condizioni:</span><span class="sxs-lookup"><span data-stu-id="29ba7-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="29ba7-111">Il saldo nel conto deve essere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="29ba7-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="29ba7-112">Nel campo **Consenti Eliminaz. Conti C/G Anteriori a** della finestra **Setup Contabilità Generale** deve essere impostata una data ed è necessario che il conto non includa movimenti contabili in tale data o dopo tale data.</span><span class="sxs-lookup"><span data-stu-id="29ba7-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="29ba7-113">Se il campo **Verifica Uso Conti C/G** della finestra **Setup Contabilità Generale** è selezionato, il conto non deve essere utilizzato in tutte le categorie di registrazione o impostazioni delle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="29ba7-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="29ba7-114"> impedirà di eliminare un conto di contabilità generale che memorizza i dati necessari per il piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="29ba7-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="29ba7-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29ba7-115">See Also</span></span>
[<span data-ttu-id="29ba7-116">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="29ba7-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="29ba7-117">Gestione di conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="29ba7-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="29ba7-118">Utilizzo delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="29ba7-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="29ba7-119">Importazione dei dati da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="29ba7-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="29ba7-120">Procedura: Utilizzare i codici GIFI in Canada</span><span class="sxs-lookup"><span data-stu-id="29ba7-120">How to: Work With GIFI Codes in Canada</span></span>](ca-finance-work-gifi-codes.md)  
<span data-ttu-id="29ba7-121">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="29ba7-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
