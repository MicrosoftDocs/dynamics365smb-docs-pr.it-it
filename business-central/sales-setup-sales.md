---
title: Panoramica dei task per la configurazione dei processi di vendita | Documenti Microsoft
description: Descrive i task per impostare le regole e i valori per definire i criteri e processi di vendita.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6903744c1be0492267c8dee307e4b012aed4ffa4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "935544"
---
# <a name="setting-up-sales"></a><span data-ttu-id="41823-103">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="41823-103">Setting Up Sales</span></span>
<span data-ttu-id="41823-104">Prima di poter dare inizio alla gestione dei processi di vendita, è necessario configurare le regole e i valori che definiscono i criteri di vendita dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="41823-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="41823-105">È necessario definire la configurazione generale, ad esempio i documenti di vendita richiesti e le modalità di registrazione dei rispettivi valori.</span><span class="sxs-lookup"><span data-stu-id="41823-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="41823-106">Queste impostazioni generali vengono in genere eseguite una volta durante l'implementazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="41823-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="41823-107">Una serie di attività specifiche correlate alla registrazione di nuovi clienti è quella di prendere nota di tutti gli accordi riguardanti sconti o prezzi speciali in essere con ogni cliente.</span><span class="sxs-lookup"><span data-stu-id="41823-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="41823-108">L'impostazione delle vendite correlata all'aspetto contabile, come i metodi di pagamento e le valute, è descritta nella sezione Impostazione degli aspetti finanziari.</span><span class="sxs-lookup"><span data-stu-id="41823-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="41823-109">Per ulteriori informazioni, vedere [Impostazione di dati finanziari](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="41823-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="41823-110">Per</span><span class="sxs-lookup"><span data-stu-id="41823-110">To</span></span> | <span data-ttu-id="41823-111">Vedere</span><span class="sxs-lookup"><span data-stu-id="41823-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="41823-112">Creare una scheda cliente per ogni cliente a cui si effettua una vendita.</span><span class="sxs-lookup"><span data-stu-id="41823-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="41823-113">Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="41823-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="41823-114">Consentire ai clienti di pagare tramite PayPal selezionando il logo di PayPal nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="41823-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="41823-115">Abilitare i pagamenti clienti attraverso PayPal</span><span class="sxs-lookup"><span data-stu-id="41823-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="41823-116">Immettere sconti diversi e prezzi speciali che vengono concessi ai clienti a seconda dell'articolo, delle quantità e/o della data.</span><span class="sxs-lookup"><span data-stu-id="41823-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="41823-117">Registrazione di prezzi, sconti e contratti di pagamento per le vendite</span><span class="sxs-lookup"><span data-stu-id="41823-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="41823-118">Impostare gli agenti in modo da poterli assegnare ai contatti clienti o misurarne le prestazioni per calcolare la provvigione sulle vendite o il premio.</span><span class="sxs-lookup"><span data-stu-id="41823-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="41823-119">Impostare gli agenti</span><span class="sxs-lookup"><span data-stu-id="41823-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="41823-120">Specificare per i singoli clienti o per tutti il modo in cui i documenti di vendita vengono inviati per impostazione predefinita quando si sceglie l'azione **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="41823-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="41823-121">Impostare profili di invio documenti</span><span class="sxs-lookup"><span data-stu-id="41823-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="41823-122">Impostare l'e-mail in modo che includa un riepilogo delle informazioni nel documento di vendita che viene inviato.</span><span class="sxs-lookup"><span data-stu-id="41823-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="41823-123">[Inviare documenti via e-mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="41823-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="41823-124">Utilizzare un servizio Web UE per verificare il numero di partita IVA del cliente.</span><span class="sxs-lookup"><span data-stu-id="41823-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="41823-125">Verificare i numeri di partita IVA</span><span class="sxs-lookup"><span data-stu-id="41823-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="41823-126">Immettere le informazioni sui diversi fornitori di servizi di trasporto utilizzati, incluso un collegamento al relativo servizio che consente di rintracciare il collo.</span><span class="sxs-lookup"><span data-stu-id="41823-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="41823-127">Impostare gli spedizionieri</span><span class="sxs-lookup"><span data-stu-id="41823-127">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="41823-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41823-128">See Also</span></span>
[<span data-ttu-id="41823-129">Vendite</span><span class="sxs-lookup"><span data-stu-id="41823-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="41823-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41823-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
