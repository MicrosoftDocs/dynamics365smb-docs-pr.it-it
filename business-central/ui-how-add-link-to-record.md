---
title: Aggiungere allegati, collegamenti e note nei record | Microsoft Docs
description: Aggiungere un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6aa7018a43db8c663c209894e118518c3de2f7cf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393887"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="edc03-103">Gestire allegati, collegamenti e note in schede e documenti</span><span class="sxs-lookup"><span data-stu-id="edc03-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="edc03-104">Nel riquadro Dettaglio informazioni della maggior parte di schede e documenti, è possibile allegare file, aggiungere collegamenti e scrivere note.</span><span class="sxs-lookup"><span data-stu-id="edc03-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="edc03-105">Per collegamenti e note, è anche possibile eseguire queste operazioni nella pagina elenco selezionando dapprima la riga correlata.</span><span class="sxs-lookup"><span data-stu-id="edc03-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="edc03-106">Per visualizzare o modificare uno di questi tipi di informazioni allegate, è necessario dapprima aprire la scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="edc03-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="edc03-107">Il numero dietro il titolo della scheda indica quanti file, collegamenti o note allegati esistono per la scheda o il documento.</span><span class="sxs-lookup"><span data-stu-id="edc03-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="edc03-108">Allegati, collegamenti e note rimangono allegati durante il passaggio ad altri stati della scheda o del documento, ad esempio da un ordine di vendita in corso a una fattura di vendita registrata.</span><span class="sxs-lookup"><span data-stu-id="edc03-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="edc03-109">Tuttavia, nessuno dei tipi di allegato viene generato dal sistema, ad esempio durante la stampa o il salvataggio in un file.</span><span class="sxs-lookup"><span data-stu-id="edc03-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="edc03-110">Quando si spedisce e si fattura parzialmente un ordine di vendita o un ordine di acquisto, l'allegato verrà collegato solo alla fattura finale di quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="edc03-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="edc03-111">Allo stesso modo, quando si fattura utilizzando la funzione Differimenti, l'allegato viene collegato solo ai movimenti C/G per il documento, ma non per i movimenti di differimento.</span><span class="sxs-lookup"><span data-stu-id="edc03-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="edc03-112">Per allegare un file a una fattura acquisto</span><span class="sxs-lookup"><span data-stu-id="edc03-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="edc03-113">È possibile allegare un qualsiasi tipo di file, contenente testo, immagini o video, a una scheda o a un documento.</span><span class="sxs-lookup"><span data-stu-id="edc03-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="edc03-114">Ciò è utile, ad esempio, quando si desidera archiviare la fattura di un fornitore come file PDF nella relativa fattura acquisto in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="edc03-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="edc03-115">I file allegati con la funzione Documenti in entrata non sono inclusi nella scheda **Allegati**. Per ulteriori informazioni, vedere [Documenti in entrata](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="edc03-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="edc03-116">La seguente procedura è basata su una fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="edc03-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="edc03-117">I passaggi sono simili per tutti gli altri documenti e schede supportati.</span><span class="sxs-lookup"><span data-stu-id="edc03-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="edc03-118">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="edc03-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="edc03-119">Aprire l'ordine di vendita a cui desidera allegare un file.</span><span class="sxs-lookup"><span data-stu-id="edc03-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="edc03-120">Nel riquadro Dettaglio informazioni, aprire la scheda **Allegati**.</span><span class="sxs-lookup"><span data-stu-id="edc03-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="edc03-121">Scegliere il valore dietro il campo **Documenti**, ad esempio "0".</span><span class="sxs-lookup"><span data-stu-id="edc03-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="edc03-122">Nella pagina **Documenti allegati**, nel campo **Allegato**, scegliere l'azione **Seleziona file**.</span><span class="sxs-lookup"><span data-stu-id="edc03-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="edc03-123">Selezionare un file in qualsiasi posizione, quindi scegliere il pulsante **Apri**.</span><span class="sxs-lookup"><span data-stu-id="edc03-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="edc03-124">Il file è ora allegato alla fattura acquisto.</span><span class="sxs-lookup"><span data-stu-id="edc03-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="edc03-125">Per visualizzare il file allegato</span><span class="sxs-lookup"><span data-stu-id="edc03-125">To view an attached file</span></span>
1. <span data-ttu-id="edc03-126">Nel riquadro Dettaglio informazioni, aprire la scheda **Allegati**.</span><span class="sxs-lookup"><span data-stu-id="edc03-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="edc03-127">Scegliere il valore dietro il campo **Documenti**, ad esempio "1".</span><span class="sxs-lookup"><span data-stu-id="edc03-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="edc03-128">Nella pagina **Documenti allegati** scegliere l'azione **Anteprima**.</span><span class="sxs-lookup"><span data-stu-id="edc03-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="edc03-129">Aprire il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="edc03-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="edc03-130">Per salvare un documento come allegato PDF</span><span class="sxs-lookup"><span data-stu-id="edc03-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="edc03-131">Ogni volta che è necessario salvare un documento come file, è possibile utilizzare l'azione **Allega come PDF** per acquisire il contenuto del documento corrente come file PDF allegato al riquadro Dettaglio informazioni del documento.</span><span class="sxs-lookup"><span data-stu-id="edc03-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="edc03-132">Ciò è utile, ad esempio, quando i documenti seguono più passaggi in un processo, come un processo di vendita o un flusso di lavoro di approvazione, e si desidera fare riferimento a una stampa del passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="edc03-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="edc03-133">La seguente procedura è basata su un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="edc03-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="edc03-134">I passaggi sono simili per tutti i documenti supportati.</span><span class="sxs-lookup"><span data-stu-id="edc03-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="edc03-135">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="edc03-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="edc03-136">Selezionare un ordine di vendita programmato quindi scegliere l'azione **Allega come PDF**.</span><span class="sxs-lookup"><span data-stu-id="edc03-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="edc03-137">Un file PDF con il contenuto corrente dell'ordine cliente viene aggiunto alla scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="edc03-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="edc03-138">Per aggiungere un collegamento da una scheda articolo</span><span class="sxs-lookup"><span data-stu-id="edc03-138">To add a link from an item card</span></span>
<span data-ttu-id="edc03-139">È possibile aggiungere un collegamento da una scheda o documento a qualsiasi URL o percorso.</span><span class="sxs-lookup"><span data-stu-id="edc03-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="edc03-140">Ciò è utile, ad esempio, quando si desidera collegare una scheda articolo al catalogo articoli del fornitore.</span><span class="sxs-lookup"><span data-stu-id="edc03-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="edc03-141">La procedura seguente è basata su una scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="edc03-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="edc03-142">I passaggi sono simili per tutti gli altri documenti e schede supportati.</span><span class="sxs-lookup"><span data-stu-id="edc03-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="edc03-143">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="edc03-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="edc03-144">Selezionare l'articolo da cui si desidera aggiungere un collegamento, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="edc03-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="edc03-145">In **Collegamenti**, scegliere l'icona **+**.</span><span class="sxs-lookup"><span data-stu-id="edc03-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="edc03-146">Nel campo **Indirizzo collegamento**, immettere il collegamento.</span><span class="sxs-lookup"><span data-stu-id="edc03-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="edc03-147">Il collegamento deve essere un URL Internet o Intranet.</span><span class="sxs-lookup"><span data-stu-id="edc03-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="edc03-148">Nel campo **Descrizione** immettere le informazioni relative al collegamento.</span><span class="sxs-lookup"><span data-stu-id="edc03-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="edc03-149">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="edc03-149">Choose the **OK** button.</span></span>

<span data-ttu-id="edc03-150">Il collegamento è ora allegato alla scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="edc03-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="edc03-151">Per scrivere una nota in un ordine cliente</span><span class="sxs-lookup"><span data-stu-id="edc03-151">To write a note on a sales order</span></span>
<span data-ttu-id="edc03-152">È possibile scrivere una nota in un documento o una scheda, ad esempio, per comunicare istruzioni speciali ad altri utenti del documento o della scheda.</span><span class="sxs-lookup"><span data-stu-id="edc03-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="edc03-153">È possibile includere URL e collegamenti a file nelle note.</span><span class="sxs-lookup"><span data-stu-id="edc03-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="edc03-154">Le note nella scheda **Allegati** non sono correlate alla funzionalità Note interne, utilizzata principalmente per la comunicazione tra utenti del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="edc03-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="edc03-155">Per ulteriori informazioni, vedere [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="edc03-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="edc03-156">La seguente procedura è basata su un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="edc03-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="edc03-157">I passaggi sono simili per tutti gli altri documenti e schede supportati.</span><span class="sxs-lookup"><span data-stu-id="edc03-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="edc03-158">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="edc03-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="edc03-159">Selezionare l'ordine di vendita in cui si desidera scrivere una nota, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.</span><span class="sxs-lookup"><span data-stu-id="edc03-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="edc03-160">Nella sezione **Note**, scegliere l'icona **+**.</span><span class="sxs-lookup"><span data-stu-id="edc03-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="edc03-161">Nel campo **Nota**, scrivere un testo qualsiasi, ad esempio "Questo è un ordine urgente".</span><span class="sxs-lookup"><span data-stu-id="edc03-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="edc03-162">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="edc03-162">Choose the **OK** button.</span></span>

<span data-ttu-id="edc03-163">La nota è ora allegata all'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="edc03-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="edc03-164">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="edc03-164">See Also</span></span>  
<span data-ttu-id="edc03-165">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edc03-165">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="edc03-166">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="edc03-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="edc03-167">Impostazione delle notifiche del workflow</span><span class="sxs-lookup"><span data-stu-id="edc03-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]