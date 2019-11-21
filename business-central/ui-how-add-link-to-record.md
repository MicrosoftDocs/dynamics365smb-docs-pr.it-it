---
title: Aggiungere allegati, collegamenti e note nei record | Microsoft Docs
description: Aggiungere un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649790"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="cad84-103">Gestire allegati, collegamenti e note in schede e documenti</span><span class="sxs-lookup"><span data-stu-id="cad84-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="cad84-104">Nel riquadro Dettaglio informazioni della maggior parte di schede e documenti, è possibile allegare file, aggiungere collegamenti e scrivere note.</span><span class="sxs-lookup"><span data-stu-id="cad84-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="cad84-105">Per collegamenti e note, è anche possibile eseguire queste operazioni nella pagina elenco selezionando dapprima la riga correlata.</span><span class="sxs-lookup"><span data-stu-id="cad84-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="cad84-106">Per visualizzare o modificare uno di questi tipi di informazioni allegate, è necessario dapprima aprire la scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="cad84-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="cad84-107">Il numero dietro il titolo della scheda indica quanti file, collegamenti o note allegati esistono per la scheda o il documento.</span><span class="sxs-lookup"><span data-stu-id="cad84-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="cad84-108">Allegati, collegamenti e note rimangono allegati durante il passaggio ad altri stati della scheda o del documento, ad esempio da un ordine di vendita in corso a una fattura di vendita registrata.</span><span class="sxs-lookup"><span data-stu-id="cad84-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="cad84-109">Si noti, tuttavia, che nessuno dei tipi di allegato viene generato dal sistema, ad esempio durante la stampa o il salvataggio in un file.</span><span class="sxs-lookup"><span data-stu-id="cad84-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="cad84-110">Per allegare un file a una fattura acquisto</span><span class="sxs-lookup"><span data-stu-id="cad84-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="cad84-111">È possibile allegare un qualsiasi tipo di file, contenente testo, immagini o video, a una scheda o a un documento.</span><span class="sxs-lookup"><span data-stu-id="cad84-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="cad84-112">Ciò è utile, ad esempio, quando si desidera archiviare la fattura di un fornitore come file PDF nella relativa fattura acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cad84-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="cad84-113">I file allegati con la funzione Documenti in entrata non sono inclusi nella scheda **Allegati**. Per ulteriori informazioni, vedere [Documenti in entrata](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="cad84-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="cad84-114">La seguente procedura è basata su ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="cad84-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="cad84-115">I passaggi sono simili per tutti gli altri documenti e schede supportati.</span><span class="sxs-lookup"><span data-stu-id="cad84-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="cad84-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="cad84-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="cad84-117">Aprire l'ordine di vendita a cui desidera allegare un file.</span><span class="sxs-lookup"><span data-stu-id="cad84-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="cad84-118">Nel riquadro Dettaglio informazioni, aprire la scheda **Allegati**.</span><span class="sxs-lookup"><span data-stu-id="cad84-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="cad84-119">Scegliere il valore dietro il campo **Documenti**, ad esempio "0".</span><span class="sxs-lookup"><span data-stu-id="cad84-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="cad84-120">Nella pagina **Documenti allegati**, nel campo **Allegato**, scegliere il pulsante **Seleziona file**.</span><span class="sxs-lookup"><span data-stu-id="cad84-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="cad84-121">Selezionare un file in qualsiasi posizione, quindi scegliere il pulsante **Apri**.</span><span class="sxs-lookup"><span data-stu-id="cad84-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="cad84-122">Il file è ora allegato alla fattura acquisto.</span><span class="sxs-lookup"><span data-stu-id="cad84-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="cad84-123">Per aggiungere un collegamento da una scheda articolo</span><span class="sxs-lookup"><span data-stu-id="cad84-123">To add a link from an item card</span></span>
<span data-ttu-id="cad84-124">È possibile aggiungere un collegamento da una scheda o documento a qualsiasi URL o percorso.</span><span class="sxs-lookup"><span data-stu-id="cad84-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="cad84-125">Ciò è utile, ad esempio, quando si desidera collegare una scheda articolo al catalogo articoli del fornitore.</span><span class="sxs-lookup"><span data-stu-id="cad84-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="cad84-126">La procedura seguente è basata su una scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="cad84-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="cad84-127">I passaggi sono simili per tutti gli altri documenti e schede supportati.</span><span class="sxs-lookup"><span data-stu-id="cad84-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="cad84-128">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="cad84-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="cad84-129">Selezionare l'articolo da cui si desidera aggiungere un collegamento, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="cad84-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="cad84-130">In **Collegamenti**, scegliere l'icona **+**.</span><span class="sxs-lookup"><span data-stu-id="cad84-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="cad84-131">Nel campo **Indirizzo collegamento**, immettere il collegamento.</span><span class="sxs-lookup"><span data-stu-id="cad84-131">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="cad84-132">Il collegamento deve essere un URL Internet o Intranet.</span><span class="sxs-lookup"><span data-stu-id="cad84-132">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="cad84-133">Nel campo **Descrizione** immettere le informazioni relative al collegamento.</span><span class="sxs-lookup"><span data-stu-id="cad84-133">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="cad84-134">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="cad84-134">Choose the **OK** button.</span></span>

<span data-ttu-id="cad84-135">Il collegamento è ora allegato alla scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="cad84-135">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="cad84-136">Per scrivere una nota in un ordine cliente</span><span class="sxs-lookup"><span data-stu-id="cad84-136">To write a note on a sales order</span></span>
<span data-ttu-id="cad84-137">È possibile scrivere una nota in un documento o una scheda, ad esempio, per comunicare istruzioni speciali ad altri utenti del documento o della scheda.</span><span class="sxs-lookup"><span data-stu-id="cad84-137">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="cad84-138">È possibile includere URL e collegamenti a file nelle note.</span><span class="sxs-lookup"><span data-stu-id="cad84-138">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="cad84-139">Le note nella scheda **Allegati** non sono correlate alla funzionalità Note interne, utilizzata principalmente per la comunicazione tra utenti del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cad84-139">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="cad84-140">Per ulteriori informazioni, vedere [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="cad84-140">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="cad84-141">La seguente procedura è basata su un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="cad84-141">The following procedure is based on a sales order.</span></span> <span data-ttu-id="cad84-142">I passaggi sono simili per tutti gli altri documenti e schede supportati.</span><span class="sxs-lookup"><span data-stu-id="cad84-142">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="cad84-143">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="cad84-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="cad84-144">Selezionare l'ordine di vendita in cui si desidera scrivere una nota, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="cad84-144">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="cad84-145">Nella sezione **Note**, scegliere l'icona **+**.</span><span class="sxs-lookup"><span data-stu-id="cad84-145">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="cad84-146">Nel campo **Nota**, scrivere un testo qualsiasi, ad esempio "Questo è un ordine urgente".</span><span class="sxs-lookup"><span data-stu-id="cad84-146">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="cad84-147">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="cad84-147">Choose the **OK** button.</span></span>

<span data-ttu-id="cad84-148">La nota è ora allegata all'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="cad84-148">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="cad84-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cad84-149">See Also</span></span>  
<span data-ttu-id="cad84-150">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cad84-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cad84-151">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="cad84-151">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="cad84-152">Impostazione delle notifiche del workflow</span><span class="sxs-lookup"><span data-stu-id="cad84-152">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
