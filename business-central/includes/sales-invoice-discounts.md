---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778649"
---
<span data-ttu-id="392e6-101">Una volta immessi tutti gli articoli nelle righe, sarà possibile calcolare lo sconto fattura per l'intero documento di vendita scegliendo l'azione **Calcola sconto fattura**.</span><span class="sxs-lookup"><span data-stu-id="392e6-101">When all the items have been entered as lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="392e6-102">Lo sconto viene calcolato in base a tutte le righe nel documento di vendita per gli articoli per cui il campo **Consenti sconto fattura** della riga dell'ordine di vendita contenga il valore **Sì**.</span><span class="sxs-lookup"><span data-stu-id="392e6-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="392e6-103">Questa è l'impostazione di default per gli articoli.</span><span class="sxs-lookup"><span data-stu-id="392e6-103">This is the default setting for items.</span></span> <span data-ttu-id="392e6-104">Le righe con addebiti articolo non vengono ad esempio incluse nel calcolo dello sconto fattura.</span><span class="sxs-lookup"><span data-stu-id="392e6-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="392e6-105">Se si desidera applicare uno sconto a tali righe, è necessario impostare il campo **% sconto riga** nelle righe pertinenti.</span><span class="sxs-lookup"><span data-stu-id="392e6-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="392e6-106">Se il campo **Calcola sconto fatt.** è selezionato nella pagina **Setup contabilità clienti**, lo sconto fattura viene calcolato automaticamente quando su un documento di vendita si effettua una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="392e6-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="392e6-107">Visualizzare statistiche</span><span class="sxs-lookup"><span data-stu-id="392e6-107">View statistics</span></span>
> * <span data-ttu-id="392e6-108">Visualizzare un report di test</span><span class="sxs-lookup"><span data-stu-id="392e6-108">View a test report</span></span>
> * <span data-ttu-id="392e6-109">Stampa</span><span class="sxs-lookup"><span data-stu-id="392e6-109">Print</span></span>
> * <span data-ttu-id="392e6-110">Spedizioni postali</span><span class="sxs-lookup"><span data-stu-id="392e6-110">Post</span></span>

<span data-ttu-id="392e6-111">Le condizioni di sconto fattura per un cliente vengono definite nella pagina **Sconti fattura clienti** per il cliente.</span><span class="sxs-lookup"><span data-stu-id="392e6-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="392e6-112">Il codice valuta nel documento di vendita viene utilizzato per identificate le condizioni dello sconto in fattura nella valuta corrispondente.</span><span class="sxs-lookup"><span data-stu-id="392e6-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="392e6-113">Se gli sconti fattura non sono stati definiti in valuta estera, per calcolarli vengono usate automaticamente le condizioni di sconto fattura in valuta locale definite nella pagina **Sconti fattura clienti** e il tasso di cambio alla data di registrazione del documento di vendita.</span><span class="sxs-lookup"><span data-stu-id="392e6-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
