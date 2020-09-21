---
title: Creare una scheda cliente per registrare un nuovo cliente | Documenti Microsoft
description: Descrive come creare una scheda cliente per registrare informazioni su ogni nuovo cliente a cui sono rivolte le vendite.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: 3e25756cff974e0db835f5e3ed3247dff6d7624a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780886"
---
# <a name="register-new-customers"></a><span data-ttu-id="e1146-103">Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="e1146-103">Register New Customers</span></span>

<span data-ttu-id="e1146-104">I clienti sono l'origine del reddito.</span><span class="sxs-lookup"><span data-stu-id="e1146-104">Customers are the source of your income.</span></span> <span data-ttu-id="e1146-105">È necessario registrare ogni cliente, cui è stata effettuata una vendita, come una scheda cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="e1146-106">Le schede cliente contengono le informazioni richieste per la vendita dei prodotti al cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="e1146-107">Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="e1146-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="e1146-108">Prima di registrare nuovi clienti, è necessario impostare vari codici di vendita selezionabili durante la compilazione delle schede cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="e1146-109">Per ulteriori informazioni, vedere [Setup Vendite](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="e1146-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="e1146-110">Aggiunta di nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="e1146-110">Adding new customers</span></span>

<span data-ttu-id="e1146-111">Per registrare un nuovo cliente, è necessario compilare una scheda cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="e1146-112">È possibile stabilire modelli per profili di clienti diversi oppure aggiungere clienti senza modelli.</span><span class="sxs-lookup"><span data-stu-id="e1146-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="e1146-113">Se esistono i modelli cliente per diversi tipi di cliente, quando si crea una nuova scheda cliente, verrà visualizzata una pagina automaticamente da cui sarà possibile selezionare un modello appropriato.</span><span class="sxs-lookup"><span data-stu-id="e1146-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="e1146-114">Se esiste solo un modello cliente, allora le nuove schede cliente utilizzeranno sempre tale modello.</span><span class="sxs-lookup"><span data-stu-id="e1146-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="e1146-115">Per creare una nuova scheda cliente</span><span class="sxs-lookup"><span data-stu-id="e1146-115">To create a new customer card</span></span>

1. <span data-ttu-id="e1146-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e1146-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1146-117">Nella pagina **Clienti** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="e1146-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="e1146-118">Se esiste solo un modello cliente, allora verrà visualizzata una nuova scheda cliente con alcuni campi compilati con le informazioni derivanti dal modello.</span><span class="sxs-lookup"><span data-stu-id="e1146-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="e1146-119">Se esistono più modelli cliente, verrà aperta una pagina nella quale sarà possibile selezionare un modello cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="e1146-120">In questo caso, seguire i due passaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="e1146-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="e1146-121">Nella pagina **Selezionare un modello per un nuovo cliente** scegliere il modello da utilizzare per la nuova scheda cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="e1146-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1146-122">Choose the **OK** button.</span></span> <span data-ttu-id="e1146-123">Una nuova scheda cliente verrà visualizzata con alcuni campi compilati con le informazioni del modello.</span><span class="sxs-lookup"><span data-stu-id="e1146-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="e1146-124">Continuare a compilare o a modificare i campi della scheda cliente in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="e1146-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="e1146-125">Nella Scheda dettaglio **Prezzi vendita** è possibile visualizzare gli sconti o i prezzi speciali che si concedono al cliente se vengono soddisfatti determinati criteri come un articolo, la quantità minima di ordine o la data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="e1146-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="e1146-126">Ogni riga rappresenta un prezzo speciale o uno sconto riga.</span><span class="sxs-lookup"><span data-stu-id="e1146-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="e1146-127">Ogni colonna rappresenta un criterio da applicare per garantire il prezzo speciale immesso nel campo **Prezzo unitario** o lo sconto riga immesso nel campo **Sconto riga**.</span><span class="sxs-lookup"><span data-stu-id="e1146-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="e1146-128">Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="e1146-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="e1146-129">Il cliente è ora registrato e la scheda cliente è pronta per essere utilizzata nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="e1146-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="e1146-130">Se si desidera utilizzare questa scheda cliente come modello quando si creano nuove schede cliente, è possibile salvarla come modello.</span><span class="sxs-lookup"><span data-stu-id="e1146-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="e1146-131">Per ulteriori informazioni, vedere la seguente sezione:</span><span class="sxs-lookup"><span data-stu-id="e1146-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="e1146-132">Per salvare la scheda cliente come modello</span><span class="sxs-lookup"><span data-stu-id="e1146-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="e1146-133">Nella pagina **Scheda cliente** scegliere l'azione **Salva come modello**.</span><span class="sxs-lookup"><span data-stu-id="e1146-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="e1146-134">Nella pagina **Modello cliente** verrà visualizzata la scheda cliente come modello.</span><span class="sxs-lookup"><span data-stu-id="e1146-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="e1146-135">Compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="e1146-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e1146-136">Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**.</span><span class="sxs-lookup"><span data-stu-id="e1146-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="e1146-137">Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per il cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="e1146-138">Modificare o immettere i codici di dimensione da collegare alle nuove schede cliente create utilizzando la definizione.</span><span class="sxs-lookup"><span data-stu-id="e1146-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="e1146-139">Una volta completato il nuovo modello cliente, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1146-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="e1146-140">Il modello cliente viene aggiunto all'elenco dei modelli cliente, in modo che sia possibile utilizzarlo per creare nuove schede cliente.</span><span class="sxs-lookup"><span data-stu-id="e1146-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="e1146-141">Eliminazione di schede cliente</span><span class="sxs-lookup"><span data-stu-id="e1146-141">Deleting customer cards</span></span>

<span data-ttu-id="e1146-142">Se è stata registrata una transazione per un cliente, non è possibile eliminare la scheda perché i movimenti contabili potrebbero essere necessari per il controllo.</span><span class="sxs-lookup"><span data-stu-id="e1146-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="e1146-143">Per eliminare le schede cliente con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.</span><span class="sxs-lookup"><span data-stu-id="e1146-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1146-144">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e1146-144">See Also</span></span>

[<span data-ttu-id="e1146-145">Definizione dei metodi di pagamento</span><span class="sxs-lookup"><span data-stu-id="e1146-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="e1146-146">Unire record duplicati</span><span class="sxs-lookup"><span data-stu-id="e1146-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="e1146-147">Creazione di numerazioni</span><span class="sxs-lookup"><span data-stu-id="e1146-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="e1146-148">Vendite</span><span class="sxs-lookup"><span data-stu-id="e1146-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="e1146-149">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="e1146-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="e1146-150">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e1146-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
