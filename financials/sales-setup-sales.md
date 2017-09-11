---
title: Panoramica dei task per la configurazione dei processi di vendita | Documenti Microsoft
description: Descrive i task per impostare le regole e i valori per definire i criteri e processi di vendita.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75ed584feda066a6c412f861bd624646c4c31085
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-sales"></a><span data-ttu-id="d65ab-103">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="d65ab-103">Setting Up Sales</span></span>
<span data-ttu-id="d65ab-104">Prima di poter dare inizio alla gestione dei processi di vendita, è necessario configurare le regole e i valori che definiscono i criteri di vendita dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="d65ab-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="d65ab-105">È necessario definire la configurazione generale, ad esempio i documenti di vendita richiesti e le modalità di registrazione dei rispettivi valori.</span><span class="sxs-lookup"><span data-stu-id="d65ab-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="d65ab-106">Queste impostazioni generali vengono in genere eseguite una volta durante l'implementazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="d65ab-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="d65ab-107">Una serie di attività specifiche correlate alla registrazione di nuovi clienti è quella di prendere nota di tutti gli accordi riguardanti sconti o prezzi speciali in essere con ogni cliente.</span><span class="sxs-lookup"><span data-stu-id="d65ab-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="d65ab-108">L'impostazione delle vendite correlata all'aspetto contabile, come i metodi di pagamento e le valute, è descritta nella sezione Impostazione degli aspetti finanziari.</span><span class="sxs-lookup"><span data-stu-id="d65ab-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="d65ab-109">Per ulteriori informazioni, vedere [Impostazione di dati finanziari](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="d65ab-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="d65ab-110">Per</span><span class="sxs-lookup"><span data-stu-id="d65ab-110">To</span></span> | <span data-ttu-id="d65ab-111">Vedere</span><span class="sxs-lookup"><span data-stu-id="d65ab-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="d65ab-112">Creare una scheda cliente per ogni cliente a cui si effettua una vendita.</span><span class="sxs-lookup"><span data-stu-id="d65ab-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="d65ab-113">Procedura: Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="d65ab-113">How to: Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="d65ab-114">Consentire ai clienti di pagare tramite PayPal selezionando il logo di PayPal nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="d65ab-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="d65ab-115">Procedura: Abilitare i pagamenti clienti attraverso PayPal</span><span class="sxs-lookup"><span data-stu-id="d65ab-115">How to: Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="d65ab-116">Immettere sconti diversi e prezzi speciali che vengono concessi ai clienti a seconda dell'articolo, delle quantità e/o della data.</span><span class="sxs-lookup"><span data-stu-id="d65ab-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="d65ab-117">Procedura: Registrare accordi riguardanti prezzi, sconti e pagamenti applicati alle vendite</span><span class="sxs-lookup"><span data-stu-id="d65ab-117">How to: Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="d65ab-118">Impostare gli agenti in modo da poterli assegnare ai contatti clienti o misurarne le prestazioni per calcolare la provvigione sulle vendite o il premio.</span><span class="sxs-lookup"><span data-stu-id="d65ab-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="d65ab-119">Procedura: Impostare gli agenti</span><span class="sxs-lookup"><span data-stu-id="d65ab-119">How to: Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="d65ab-120">Specificare per i singoli clienti o per tutti il modo in cui i documenti di vendita vengono inviati per impostazione predefinita quando si sceglie l'azione **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="d65ab-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="d65ab-121">Procedura: Impostare profili di invio documenti</span><span class="sxs-lookup"><span data-stu-id="d65ab-121">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="d65ab-122">Impostare l'e-mail in modo che includa un riepilogo delle informazioni nel documento di vendita che viene inviato.</span><span class="sxs-lookup"><span data-stu-id="d65ab-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="d65ab-123">[Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="d65ab-123">[How to: Send Documents by Email](ui-how-send-documents-email.md).</span></span> |

## <a name="see-also"></a><span data-ttu-id="d65ab-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d65ab-124">See Also</span></span>
[<span data-ttu-id="d65ab-125">Vendite</span><span class="sxs-lookup"><span data-stu-id="d65ab-125">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d65ab-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d65ab-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

