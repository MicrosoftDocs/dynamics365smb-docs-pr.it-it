---
title: Aggiornare i tassi di cambio delle valute| Documenti Microsoft
description: "Per utilizzare più valute nell'attività commerciale, è possibile impostare un codice per ogni valuta e utilizzare un servizio di conversione esterno, ad esempio Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="9a941-103">Procedura: Aggiornare i tassi di cambio</span><span class="sxs-lookup"><span data-stu-id="9a941-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="9a941-104">È necessario impostare un codice per ogni valuta utilizzata se si compra o si vende in valute diverse dalla valuta locale, se si hanno debiti o crediti in altre valute o si registrano transazioni C/G in diverse valute.</span><span class="sxs-lookup"><span data-stu-id="9a941-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9a941-105">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="9a941-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="9a941-106">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="9a941-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="9a941-107">È possibile utilizzare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute.</span><span class="sxs-lookup"><span data-stu-id="9a941-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="9a941-108">Il servizio Tassi di cambio della valuta di Yahoo è preinstallato e pronto per essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="9a941-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="9a941-109">Per impostare un servizio dei tassi di cambio delle valute</span><span class="sxs-lookup"><span data-stu-id="9a941-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="9a941-110">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Servizi tasso di cambio valuta**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9a941-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="9a941-111">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="9a941-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="9a941-112">Nella finestra **Servizi tasso di cambio valuta** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="9a941-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="9a941-113">Scegliere la casella controllo **Abilitato** per abilitare il servizio.</span><span class="sxs-lookup"><span data-stu-id="9a941-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="9a941-114">Per aggiornare i tassi di cambio delle valute mediante un servizio</span><span class="sxs-lookup"><span data-stu-id="9a941-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="9a941-115">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Servizi tasso di cambio valuta**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9a941-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="9a941-116">Scegliere l'azione **Aggiorna tassi di cambio**.</span><span class="sxs-lookup"><span data-stu-id="9a941-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="9a941-117">Il valore nel campo **Tasso di cambio** della finestra **Valute** viene aggiornato con il tasso di cambio delle valute più recente.</span><span class="sxs-lookup"><span data-stu-id="9a941-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a941-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a941-118">See Also</span></span>
[<span data-ttu-id="9a941-119">Chiusura di anni e periodi</span><span class="sxs-lookup"><span data-stu-id="9a941-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="9a941-120">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a941-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

