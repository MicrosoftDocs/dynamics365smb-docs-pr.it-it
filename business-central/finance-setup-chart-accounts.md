---
title: Impostazione di un piano dei conti
description: È possibile modificare i conti predefiniti nel piano dei conti ed è possibile aggiungere nuovi conti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8c75a214691b7d9886958866517afbb1d68b6f60
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242447"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="d9e9e-103">Impostazione o modifica del piano dei conti</span><span class="sxs-lookup"><span data-stu-id="d9e9e-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="d9e9e-104">Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d9e9e-105">include un piano dei conti standard pronto per supportare l'azienda.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="d9e9e-106">Tuttavia, è possibile modificare i conti predefiniti ed è possibile aggiungere nuovi conti.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="d9e9e-107">Aggiungere o modificare i conti</span><span class="sxs-lookup"><span data-stu-id="d9e9e-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="d9e9e-108">Nel piano dei conti, è possibile aprire ogni conto C/G e aggiungere o modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d9e9e-109">È possibile eliminare un conto di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-109">You can delete a general ledger account.</span></span> <span data-ttu-id="d9e9e-110">Tuttavia, prima che venga eliminato, è necessario soddisfare le seguenti condizioni:</span><span class="sxs-lookup"><span data-stu-id="d9e9e-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="d9e9e-111">Il saldo nel conto deve essere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="d9e9e-112">Nel campo **Consenti Eliminaz. Conti C/G Anteriori a** della pagina **Setup Contabilità Generale** deve essere impostata una data ed è necessario che il conto non includa movimenti contabili in tale data o dopo tale data.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="d9e9e-113">Se il campo **Verifica Uso Conti C/G** della pagina **Setup Contabilità Generale** è selezionato, il conto non deve essere utilizzato in tutte le categorie di registrazione o impostazioni delle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d9e9e-114">impedirà di eliminare un conto di contabilità generale che memorizza i dati necessari per il piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="d9e9e-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d9e9e-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9e9e-115">See Also</span></span>
[<span data-ttu-id="d9e9e-116">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="d9e9e-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="d9e9e-117">Gestione di conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="d9e9e-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="d9e9e-118">Utilizzo delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="d9e9e-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="d9e9e-119">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="d9e9e-119">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="d9e9e-120">Utilizzare le situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="d9e9e-120">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="d9e9e-121">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9e9e-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
