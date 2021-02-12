---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035789"
---
<span data-ttu-id="4432a-101">Una volta immessi tutti gli articoli nelle righe ordine di vendita, sarà possibile calcolare lo sconto sulla fattura per l'intero documento di vendita scegliendo l'azione **Calcola sconto fattura**.</span><span class="sxs-lookup"><span data-stu-id="4432a-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="4432a-102">Se il campo **Calcola sconto fatt.** viene selezionato nella finestra **Setup contabilità clienti**, lo sconto fattura viene calcolato automaticamente quando sul documento di vendita si esegue una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="4432a-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="4432a-103">Visualizzare statistiche</span><span class="sxs-lookup"><span data-stu-id="4432a-103">View statistics</span></span>
* <span data-ttu-id="4432a-104">Visualizzare un report di test</span><span class="sxs-lookup"><span data-stu-id="4432a-104">View a test report</span></span>
* <span data-ttu-id="4432a-105">Stampa</span><span class="sxs-lookup"><span data-stu-id="4432a-105">Print</span></span>
* <span data-ttu-id="4432a-106">Spedizioni postali</span><span class="sxs-lookup"><span data-stu-id="4432a-106">Post</span></span>

<span data-ttu-id="4432a-107">Nei documenti di acquisto di articoli e risorse lo sconto viene distribuito su tutte le righe nel cui campo **Sconto Fattura** sia stato immesso **Sì**.</span><span class="sxs-lookup"><span data-stu-id="4432a-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="4432a-108">Questa è l'impostazione di default per gli articoli.</span><span class="sxs-lookup"><span data-stu-id="4432a-108">This is the default setting for items.</span></span>

<span data-ttu-id="4432a-109">Per calcolare lo sconto fattura, si definiscono le condizioni di sconto fattura definite nella pagina **Sconti fattura clienti**.</span><span class="sxs-lookup"><span data-stu-id="4432a-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="4432a-110">Il codice valuta nel documento di vendita viene utilizzato per identificate le condizioni dello sconto in fattura nella valuta corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4432a-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="4432a-111">Se gli sconti fattura non sono stati definiti in valuta estera, per calcolarli vengono usate automaticamente le condizioni di sconto fattura in valuta locale definite nella pagina **Sconti fattura clienti** e il tasso di cambio alla data di registrazione del documento di vendita.</span><span class="sxs-lookup"><span data-stu-id="4432a-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
