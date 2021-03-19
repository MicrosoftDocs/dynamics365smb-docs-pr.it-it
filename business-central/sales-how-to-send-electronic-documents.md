---
title: Inviare documenti elettronici
description: Informazioni su come inviare le fatture elettronicamente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383002"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="bb190-103">Inviare documenti elettronici</span><span class="sxs-lookup"><span data-stu-id="bb190-103">Send Electronic Documents</span></span>

<span data-ttu-id="bb190-104">La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] supporta l'invio delle fatture e delle note di credito elettroniche nel formato PEPPOL, supportato dai principali provider di servizi di scambio documenti.</span><span class="sxs-lookup"><span data-stu-id="bb190-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="bb190-105">Un provider di servizi di Exchange per documenti invia i documenti elettronici tra i partner commerciali.</span><span class="sxs-lookup"><span data-stu-id="bb190-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="bb190-106">Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.</span><span class="sxs-lookup"><span data-stu-id="bb190-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="bb190-107">Nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)], un servizio di scambio documenti è preconfigurato e pronto per l'installazione nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="bb190-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="bb190-108">Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="bb190-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="bb190-109">Tuttavia, in alcuni casi, è necessario installare un'app.</span><span class="sxs-lookup"><span data-stu-id="bb190-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="bb190-110">Per ulteriori informazioni, vedere [Domande frequenti sulla fatturazione elettronica](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="bb190-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="bb190-111">Per inviare una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="bb190-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="bb190-112">Nella finestra di dialogo è inoltre possibile impostare il profilo di invio documenti predefinito del cliente.</span><span class="sxs-lookup"><span data-stu-id="bb190-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="bb190-113">Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura.</span><span class="sxs-lookup"><span data-stu-id="bb190-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="bb190-114">Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi in [Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="bb190-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="bb190-115">Per inviare una fattura di vendita elettronica</span><span class="sxs-lookup"><span data-stu-id="bb190-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="bb190-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture vendite** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bb190-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="bb190-117">Creare una nuova fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="bb190-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="bb190-118">Una volta che la fattura di vendita è pronta per essere fatturata, scegliere l'azione **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="bb190-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="bb190-119">Se il profilo di invio predefinito del cliente è **Documento elettronico**, verrà visualizzato nella finestra di dialogo **Conferma registrazione e invio**.</span><span class="sxs-lookup"><span data-stu-id="bb190-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="bb190-120">In questo modo, è necessario soltanto scegliere il pulsante **Sì** per registrare e inviare la fattura in formato elettronico nel formato selezionato.</span><span class="sxs-lookup"><span data-stu-id="bb190-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="bb190-121">Nella finestra di dialogo **Conferma registrazione e invio** scegliere il pulsante AssistEdit a destra del campo **Invia documento a**.</span><span class="sxs-lookup"><span data-stu-id="bb190-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="bb190-122">Nella finestra di dialogo **Invia documento a**, nel campo **Documento elettronico**, scegliere **Tramite il servizio di Exchange per documenti**.</span><span class="sxs-lookup"><span data-stu-id="bb190-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="bb190-123">Nel campo **Formato** scegliere **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="bb190-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="bb190-124">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb190-124">Choose the **OK** button.</span></span> <span data-ttu-id="bb190-125">Viene visualizzata la finestra di dialogo **Conferma registrazione e invio**.</span><span class="sxs-lookup"><span data-stu-id="bb190-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="bb190-126">Nel campo **Invia documento a** viene aggiunto **Documento elettronico (PEPPOL)**.</span><span class="sxs-lookup"><span data-stu-id="bb190-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="bb190-127">Scegliere il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="bb190-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="bb190-128">La fattura di vendita viene registrata e inviata al cliente in formato PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="bb190-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="bb190-129">È inoltre possibile inviare una fattura di vendita registrata come documento elettronico.</span><span class="sxs-lookup"><span data-stu-id="bb190-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="bb190-130">La procedura è uguale a quella descritta in questo argomento per i documenti di vendita non registrati.</span><span class="sxs-lookup"><span data-stu-id="bb190-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="bb190-131">Nella pagina **Fatt. di vend. reg.** scegliere l'azione **Log attività** per visualizzare lo stato del documento elettronico.</span><span class="sxs-lookup"><span data-stu-id="bb190-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="bb190-132">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="bb190-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="bb190-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bb190-133">See Also</span></span>

[<span data-ttu-id="bb190-134">Fatturare le vendite</span><span class="sxs-lookup"><span data-stu-id="bb190-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="bb190-135">Impostare profili di invio documenti</span><span class="sxs-lookup"><span data-stu-id="bb190-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="bb190-136">Impostare l'invio e la ricezione di documenti elettronici</span><span class="sxs-lookup"><span data-stu-id="bb190-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="bb190-137">Impostare un servizio di scambio documenti</span><span class="sxs-lookup"><span data-stu-id="bb190-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="bb190-138">Impostare le definizioni di scambio dati</span><span class="sxs-lookup"><span data-stu-id="bb190-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="bb190-139">Scambio di dati in modalità elettronica</span><span class="sxs-lookup"><span data-stu-id="bb190-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="bb190-140">Domande frequenti sulla fatturazione elettronica</span><span class="sxs-lookup"><span data-stu-id="bb190-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="bb190-141">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="bb190-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]