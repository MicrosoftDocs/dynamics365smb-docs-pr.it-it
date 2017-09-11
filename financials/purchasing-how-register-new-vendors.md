---
title: Creare una scheda fornitore per registrare un nuovo fornitore | Documenti Microsoft
description: Informazioni su come creare una scheda fornitore per registrare un nuovo fornitore.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-register-new-vendors"></a><span data-ttu-id="5b95e-103">Procedura: Registrare nuovi fornitori</span><span class="sxs-lookup"><span data-stu-id="5b95e-103">How to: Register New Vendors</span></span>
<span data-ttu-id="5b95e-104">I fornitori forniscono i prodotti venduti.</span><span class="sxs-lookup"><span data-stu-id="5b95e-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="5b95e-105">Ogni fornitore da cui si acquista deve essere registrato come una scheda fornitore.</span><span class="sxs-lookup"><span data-stu-id="5b95e-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="5b95e-106">Prima di registrare nuovi fornitori, è necessario impostare vari codici di acquisto che sarà possibile selezionare durante la compilazione delle schede fornitore.</span><span class="sxs-lookup"><span data-stu-id="5b95e-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="5b95e-107">Dopo la creazione di tutta l'anagrafica necessaria, è possibile eseguire ulteriori operazioni di configurazione del fornitore, ad esempio impostare il fornitore come prioritario per i pagamenti ed elencare gli articoli che tale fornitore e altri fornitori possono mettere a disposizione.</span><span class="sxs-lookup"><span data-stu-id="5b95e-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="5b95e-108">Un altro gruppo di attività di impostazione dei fornitori è costituito dalla registrazione degli accordi relativi a sconti, prezzi e metodi di pagamento.</span><span class="sxs-lookup"><span data-stu-id="5b95e-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="5b95e-109">Per ulteriori informazioni, vedere [Impostazioni acquisti](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="5b95e-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="5b95e-110">Le schede fornitore conservano le informazioni richieste per acquistare i prodotti presso i fornitori.</span><span class="sxs-lookup"><span data-stu-id="5b95e-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="5b95e-111">Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md) e [Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="5b95e-111">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md) and [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="5b95e-112">Se esistono modelli fornitore per diversi tipi di fornitore, durante la creazione di una nuova scheda fornitore, verrà visualizzata una finestra nella quale sarà possibile selezionare un modello appropriato.</span><span class="sxs-lookup"><span data-stu-id="5b95e-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="5b95e-113">Se esiste solo un modello fornitore, allora le nuove schede fornitore utilizzeranno sempre tale modello.</span><span class="sxs-lookup"><span data-stu-id="5b95e-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="5b95e-114">Per creare una nuova scheda fornitore</span><span class="sxs-lookup"><span data-stu-id="5b95e-114">To create a new vendor card</span></span>
1. <span data-ttu-id="5b95e-115">Nella home page scegliere **Fornitori** per aprire l'elenco di fornitori esistenti.</span><span class="sxs-lookup"><span data-stu-id="5b95e-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="5b95e-116">Nella finestra **Fornitori** scegliere **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="5b95e-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="5b95e-117">Se esistono più modelli fornitore, verrà aperta una finestra nella quale sarà possibile selezionare un modello.</span><span class="sxs-lookup"><span data-stu-id="5b95e-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="5b95e-118">In questo caso, seguire i due passaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="5b95e-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="5b95e-119">Nella finestra **Selezionare un modello per un nuovo fornitore** scegliere il modello da utilizzare per la nuova scheda fornitore.</span><span class="sxs-lookup"><span data-stu-id="5b95e-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="5b95e-120">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b95e-120">Choose the **OK** button.</span></span> <span data-ttu-id="5b95e-121">Verrà visualizzata una nuova scheda fornitore con alcuni campi compilati con le informazioni del modello.</span><span class="sxs-lookup"><span data-stu-id="5b95e-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="5b95e-122">Continuare a compilare o a modificare i campi della scheda fornitore in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="5b95e-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="5b95e-123">Il fornitore è ora registrato e la scheda fornitore è pronta per essere utilizzata nei documenti di acquisto.</span><span class="sxs-lookup"><span data-stu-id="5b95e-123">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="5b95e-124">Se si desidera utilizzare questa scheda fornitore come modello quando si creano nuove schede fornitore, è possibile salvarla come modello fornitore.</span><span class="sxs-lookup"><span data-stu-id="5b95e-124">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="5b95e-125">Per ulteriori informazioni, vedere la seguente sezione:</span><span class="sxs-lookup"><span data-stu-id="5b95e-125">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="5b95e-126">Per salvare la scheda fornitore come modello</span><span class="sxs-lookup"><span data-stu-id="5b95e-126">To save the vendor card as a template</span></span>
1. <span data-ttu-id="5b95e-127">Nella finestra **Scheda fornitore** scegliere l'azione **Salva come modello**.</span><span class="sxs-lookup"><span data-stu-id="5b95e-127">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="5b95e-128">Nella finestra **Modello fornitore** verrà visualizzata la scheda fornitore come modello.</span><span class="sxs-lookup"><span data-stu-id="5b95e-128">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="5b95e-129">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="5b95e-129">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="5b95e-130">Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**.</span><span class="sxs-lookup"><span data-stu-id="5b95e-130">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="5b95e-131">Verrà visualizzata la finestra **Modelli dimensioni** nella quale saranno indicati tutti i codici per le dimensioni che sono impostati per il fornitore.</span><span class="sxs-lookup"><span data-stu-id="5b95e-131">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="5b95e-132">Modificare o immettere i codici di dimensione da collegare alle nuove schede fornitore create utilizzando la definizione.</span><span class="sxs-lookup"><span data-stu-id="5b95e-132">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="5b95e-133">Una volta completato il nuovo modello fornitore, scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b95e-133">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="5b95e-134">Il modello fornitore viene aggiunto all'elenco dei modelli fornitore, in modo che sia possibile utilizzarlo per creare nuove schede fornitore.</span><span class="sxs-lookup"><span data-stu-id="5b95e-134">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b95e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b95e-135">See Also</span></span>
[<span data-ttu-id="5b95e-136">Acquisti</span><span class="sxs-lookup"><span data-stu-id="5b95e-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5b95e-137">[Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="5b95e-137">[How to: Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="5b95e-138">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5b95e-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

