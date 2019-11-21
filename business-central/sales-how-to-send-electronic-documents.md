---
title: Inviare documenti elettronici | Documenti Microsoft
description: Informazioni su come inviare le fatture elettronicamente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 26b2e5bf479f3343f66bd852078b337ad87e852a
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554817"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="37ac1-103">Inviare documenti elettronici</span><span class="sxs-lookup"><span data-stu-id="37ac1-103">Send Electronic Documents</span></span>
<span data-ttu-id="37ac1-104">La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta l'invio delle fatture e delle note di credito elettroniche nel formato PEPPOL, che è supportato dai principali provider di servizi di scambio documenti.</span><span class="sxs-lookup"><span data-stu-id="37ac1-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="37ac1-105">Un provider di servizi di Exchange per documenti invia i documenti elettronici tra i partner commerciali.</span><span class="sxs-lookup"><span data-stu-id="37ac1-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="37ac1-106">Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.</span><span class="sxs-lookup"><span data-stu-id="37ac1-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="37ac1-107">Nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)], un servizio di scambio documenti è preconfigurato e pronto per l'installazione nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="37ac1-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="37ac1-108">Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="37ac1-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="37ac1-109">Per inviare una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia** in cui è anche possibile impostare il profilo di invio documenti predefinito del cliente.</span><span class="sxs-lookup"><span data-stu-id="37ac1-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="37ac1-110">Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura.</span><span class="sxs-lookup"><span data-stu-id="37ac1-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="37ac1-111">Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi in [Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="37ac1-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="37ac1-112">Per inviare una fattura di vendita elettronica</span><span class="sxs-lookup"><span data-stu-id="37ac1-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="37ac1-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="37ac1-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="37ac1-114">Creare una nuova fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="37ac1-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="37ac1-115">Una volta che la fattura di vendita è pronta per essere fatturata, scegliere l'azione **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-115">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="37ac1-116">Se il profilo di invio predefinito del cliente è **Documento elettronico**, sarà mostrato nella finestra di dialogo **Conferma registrazione e invio** e basterà scegliere il pulsante **Sì** per registrare e inviare elettronicamente la fattura nel formato selezionato.</span><span class="sxs-lookup"><span data-stu-id="37ac1-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="37ac1-117">Nella finestra di dialogo **Conferma registrazione e invio** scegliere il pulsante AssistEdit a destra del campo **Invia documento a**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="37ac1-118">Nella finestra di dialogo **Invia documento a**, nel campo **Documento elettronico**, scegliere **Tramite il servizio di Exchange per documenti**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="37ac1-119">Nel campo **Formato** scegliere **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="37ac1-120">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-120">Choose the **OK** button.</span></span> <span data-ttu-id="37ac1-121">Viene visualizzata la finestra di dialogo **Conferma registrazione e invio**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="37ac1-122">Nel campo **Invia documento a** viene aggiunto **Documento elettronico (PEPPOL)**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="37ac1-123">Scegliere il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="37ac1-124">La fattura di vendita viene registrata e inviata al cliente come documento elettronico in formato PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="37ac1-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="37ac1-125">È inoltre possibile inviare una fattura di vendita registrata come documento elettronico.</span><span class="sxs-lookup"><span data-stu-id="37ac1-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="37ac1-126">La procedura è uguale a quella descritta in questo argomento per i documenti di vendita non registrati.</span><span class="sxs-lookup"><span data-stu-id="37ac1-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="37ac1-127">Nella pagina **Fatt. di vend. reg.** scegliere l'azione **Log attività** per visualizzare lo stato del documento elettronico.</span><span class="sxs-lookup"><span data-stu-id="37ac1-127">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span> <span data-ttu-id="37ac1-128">Per ulteriori informazioni, vedere **Log attività**.</span><span class="sxs-lookup"><span data-stu-id="37ac1-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="37ac1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37ac1-129">See Also</span></span>  
[<span data-ttu-id="37ac1-130">Fatturare le vendite</span><span class="sxs-lookup"><span data-stu-id="37ac1-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="37ac1-131">Impostare profili di invio documenti</span><span class="sxs-lookup"><span data-stu-id="37ac1-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="37ac1-132">Impostare l'invio e la ricezione di documenti elettronici</span><span class="sxs-lookup"><span data-stu-id="37ac1-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="37ac1-133">Impostare un servizio di scambio documenti</span><span class="sxs-lookup"><span data-stu-id="37ac1-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="37ac1-134">Impostare le definizioni di scambio dati</span><span class="sxs-lookup"><span data-stu-id="37ac1-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="37ac1-135">Scambio di dati in modalità elettronica</span><span class="sxs-lookup"><span data-stu-id="37ac1-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="37ac1-136">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="37ac1-136">General Business Functionality</span></span>](ui-across-business-areas.md)  
