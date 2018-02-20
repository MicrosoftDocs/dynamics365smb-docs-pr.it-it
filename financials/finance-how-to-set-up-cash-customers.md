---
title: Come impostare un cliente per vendite in contanti | Microsoft Docs
description: Questo argomento descrive la procedura per impostare i clienti che pagano in contanti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a72e6ff0a710f2d555c805e4fa28896683a819e9
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="223fe-103">Impostare i clienti per vendite in contanti</span><span class="sxs-lookup"><span data-stu-id="223fe-103">Set Up Cash Customers</span></span>
<span data-ttu-id="223fe-104">Non è possibile creare una fattura senza un numero di cliente.</span><span class="sxs-lookup"><span data-stu-id="223fe-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="223fe-105">Ciò si applica anche nel caso di una vendita in contanti, quando non ci sarebbe niente da registrare in un conto cliente.</span><span class="sxs-lookup"><span data-stu-id="223fe-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="223fe-106">Per impostare un cliente per vendite in contanti</span><span class="sxs-lookup"><span data-stu-id="223fe-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="223fe-107">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cliente**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="223fe-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="223fe-108">Creare una nuova scheda **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="223fe-108">Create a new **Customer** card.</span></span> <span data-ttu-id="223fe-109">Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="223fe-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="223fe-110">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="223fe-110">In the **No.**</span></span> <span data-ttu-id="223fe-111">immettere ad esempio **Incassi**.</span><span class="sxs-lookup"><span data-stu-id="223fe-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="223fe-112">Nel campo **Nome** immettere ad esempio **Vendita in Contante**.</span><span class="sxs-lookup"><span data-stu-id="223fe-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="223fe-113">Nella Scheda dettaglio **Fatturazione** compilare i campi **Cat. reg. cliente** e **Cat. reg. business**.</span><span class="sxs-lookup"><span data-stu-id="223fe-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="223fe-114">È stato così impostato un nuovo cliente con informazioni sufficienti per la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="223fe-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="223fe-115">Può essere stata scelta una categoria di registrazione che viene utilizzata anche per le vendite a credito interne.</span><span class="sxs-lookup"><span data-stu-id="223fe-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="223fe-116">Se si desidera mantenere separati i dati sulle vendite in contanti, ad esempio con un conto speciale di vendita o incassi, è possibile impostare per questo scopo una nuova categoria di registrazione.</span><span class="sxs-lookup"><span data-stu-id="223fe-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="223fe-117">È necessario immettere un numero di conto incassi per la categoria di registrazione, anche se il saldo di questo conto dopo la registrazione di una fattura corrisponderà sempre a 0.</span><span class="sxs-lookup"><span data-stu-id="223fe-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="223fe-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="223fe-118">See Also</span></span>
[<span data-ttu-id="223fe-119">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="223fe-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="223fe-120">[Registrare nuovi clienti](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="223fe-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="223fe-121">Finanze</span><span class="sxs-lookup"><span data-stu-id="223fe-121">Finance</span></span>](finance.md)  


