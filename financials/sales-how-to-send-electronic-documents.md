---
title: Inviare documenti elettronici | Documenti Microsoft
description: Informazioni su come inviare le fatture elettronicamente.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fae5e37b8f1fcca84a474b2eac2039f7fc6d8245
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="send-electronic-documents"></a><span data-ttu-id="faf1d-103">Inviare documenti elettronici</span><span class="sxs-lookup"><span data-stu-id="faf1d-103">Send Electronic Documents</span></span>
<span data-ttu-id="faf1d-104">La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta l'invio delle fatture e delle note di credito elettroniche nel formato PEPPOL, che è supportato dai principali provider di servizi di scambio documenti.</span><span class="sxs-lookup"><span data-stu-id="faf1d-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="faf1d-105">Un provider di servizi di Exchange per documenti invia i documenti elettronici tra i partner commerciali.</span><span class="sxs-lookup"><span data-stu-id="faf1d-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="faf1d-106">Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.</span><span class="sxs-lookup"><span data-stu-id="faf1d-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="faf1d-107">Nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)], un servizio di scambio documenti è preconfigurato e pronto per l'installazione nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="faf1d-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="faf1d-108">Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="faf1d-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="faf1d-109">Per inviare una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia** in cui è anche possibile impostare il profilo di invio documenti predefinito del cliente.</span><span class="sxs-lookup"><span data-stu-id="faf1d-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="faf1d-110">Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura.</span><span class="sxs-lookup"><span data-stu-id="faf1d-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="faf1d-111">Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi in [Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="faf1d-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="faf1d-112">Per inviare una fattura di vendita elettronica</span><span class="sxs-lookup"><span data-stu-id="faf1d-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="faf1d-113">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture vendite**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="faf1d-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="faf1d-114">Creare una nuova fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="faf1d-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="faf1d-115">Quando la fattura è pronta, nel gruppo **Registrazione** della scheda **Azioni** scegliere **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="faf1d-116">Se il profilo di invio predefinito del cliente è **Documento elettronico**, sarà mostrato nella finestra di dialogo **Conferma registrazione e invio** e basterà scegliere il pulsante **Sì** per registrare e inviare elettronicamente la fattura nel formato selezionato.</span><span class="sxs-lookup"><span data-stu-id="faf1d-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="faf1d-117">Nella finestra di dialogo **Conferma registrazione e invio** scegliere il pulsante AssistEdit a destra del campo **Invia documento a**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="faf1d-118">Nella finestra di dialogo **Invia documento a**, nel campo **Documento elettronico**, scegliere **Tramite il servizio di Exchange per documenti**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="faf1d-119">Nel campo **Formato** scegliere **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="faf1d-120">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-120">Choose the **OK** button.</span></span> <span data-ttu-id="faf1d-121">Viene visualizzata la finestra di dialogo **Conferma registrazione e invio**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="faf1d-122">Nel campo **Invia documento a** viene aggiunto **Documento elettronico (PEPPOL)**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="faf1d-123">Scegliere il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="faf1d-124">La fattura di vendita viene registrata e inviata al cliente come documento elettronico in formato PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="faf1d-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="faf1d-125">È inoltre possibile inviare una fattura di vendita registrata come documento elettronico.</span><span class="sxs-lookup"><span data-stu-id="faf1d-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="faf1d-126">La procedura è uguale a quella descritta in questo argomento per i documenti di vendita non registrati.</span><span class="sxs-lookup"><span data-stu-id="faf1d-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="faf1d-127">Nella finestra **Fatt. di vend. reg.** nella scheda **Azioni**, nel gruppo **Generale**, scegliere **Log attività** per visualizzare lo stato del documento elettronico.</span><span class="sxs-lookup"><span data-stu-id="faf1d-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="faf1d-128">Per ulteriori informazioni, vedere **Log attività**.</span><span class="sxs-lookup"><span data-stu-id="faf1d-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="faf1d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="faf1d-129">See Also</span></span>  
[<span data-ttu-id="faf1d-130">Fatturare le vendite</span><span class="sxs-lookup"><span data-stu-id="faf1d-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="faf1d-131">Impostare profili di invio documenti</span><span class="sxs-lookup"><span data-stu-id="faf1d-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="faf1d-132">Impostare l'invio e la ricezione di documenti elettronici</span><span class="sxs-lookup"><span data-stu-id="faf1d-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="faf1d-133">Impostare un servizio di scambio documenti</span><span class="sxs-lookup"><span data-stu-id="faf1d-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="faf1d-134">Impostare le definizioni di scambio dati</span><span class="sxs-lookup"><span data-stu-id="faf1d-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="faf1d-135">Scambio di dati in modalità elettronica</span><span class="sxs-lookup"><span data-stu-id="faf1d-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="faf1d-136">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="faf1d-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

