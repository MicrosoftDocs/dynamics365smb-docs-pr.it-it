---
title: Come creare collegamenti a informazioni o programmi esterni nei record | Microsoft Docs
description: Aggiungere un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 602d520043c5192109ccc4e2605ae0e231dafc1e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250344"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="1aafb-103">Aggiunta di collegamenti a siti Web, documenti o programmi nei record</span><span class="sxs-lookup"><span data-stu-id="1aafb-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="1aafb-104">In un record specifico, ad esempio un cliente, un documento o un ordine di vendita, è possibile aggiungere un collegamento a un sito Web, programma o documento esterno.</span><span class="sxs-lookup"><span data-stu-id="1aafb-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="1aafb-105">In alternativa, è possibile creare un collegamento che apre un nuovo messaggio e-mail vuoto a un cliente specifico quando lo si seleziona.</span><span class="sxs-lookup"><span data-stu-id="1aafb-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="1aafb-106">La pagina schede di alcuni record, ad esempio schede clienti e fornitori, includono un campo **Home page** in cui è possibile immettere un indirizzo Internet (URL).</span><span class="sxs-lookup"><span data-stu-id="1aafb-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="1aafb-107">Per includere altri collegamenti, è possibile utilizzare il metodo descritto in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="1aafb-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1aafb-108">Attualmente, questa funzionalità è disponibile solo in distribuzioni [!INCLUDE [prodshort](includes/prodshort.md)] in locale con il client Windows di Dynamics NAV legacy.</span><span class="sxs-lookup"><span data-stu-id="1aafb-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="1aafb-109">Un altro esempio potrebbe essere quando si ricevono fatture stampate dai fornitori.</span><span class="sxs-lookup"><span data-stu-id="1aafb-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="1aafb-110">È possibile digitalizzarle e salvarle come file .pdf in un sito SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1aafb-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="1aafb-111">È quindi possibile creare un collegamento da una fattura di acquisto in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] alla fattura corrispondente in SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1aafb-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="1aafb-112">In alternativa, è possibile creare un collegamento da una scheda articolo nella pagina corrispondente nel catalogo in linea del fornitore.</span><span class="sxs-lookup"><span data-stu-id="1aafb-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="1aafb-113">Per aggiungere un collegamento in un record</span><span class="sxs-lookup"><span data-stu-id="1aafb-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="1aafb-114">Aprire il record a cui si desidera associare il collegamento, ad esempio una scheda cliente o un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="1aafb-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="1aafb-115">Se si desidera associare il collegamento a una riga specifica, ad esempio una riga di registrazione, selezionare la riga.</span><span class="sxs-lookup"><span data-stu-id="1aafb-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="1aafb-116">Scegliere l'azione **Collegamenti** per aprire la pagina **Collegamenti** in cui vengono visualizzati tutti i collegamenti correnti aggiunti al record.</span><span class="sxs-lookup"><span data-stu-id="1aafb-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="1aafb-117">Per aggiungere un nuovo collegamento, scegliere **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="1aafb-118">Nel campo **Indirizzo collegamento**, immettere</span><span class="sxs-lookup"><span data-stu-id="1aafb-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="1aafb-119">Per creare un collegamento a un file nel computer o in rete, immettere il percorso completo e il nome di file, ad esempio **C:Documenti\Fattura1.doc**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="1aafb-120">Per creare un collegamento a un sito Web, immettere l'indirizzo Internet (URL), ad esempio **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="1aafb-121">Per creare un collegamento a un sito Web, immettere l'indirizzo Internet (URL), ad esempio **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-121">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="1aafb-122">Per creare un collegamento a un programma, immettere una stringa specifica per aprire il programma.</span><span class="sxs-lookup"><span data-stu-id="1aafb-122">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="1aafb-123">Ad esempio, per aprire OneNote con una pagina specifica, immettere **onenote:///C:Documenti\test.one**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-123">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="1aafb-124">Oppure per aprire Outlook con una nuova e-mail vuota a un alias specifico, immettere **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-124">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="1aafb-125">Nel campo **Descrizione** inserire informazioni relative al collegamento.</span><span class="sxs-lookup"><span data-stu-id="1aafb-125">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="1aafb-126">Fare clic sul pulsante **Salva**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-126">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="1aafb-127">Per eliminare un collegamento da un record</span><span class="sxs-lookup"><span data-stu-id="1aafb-127">To delete a link from a record</span></span>  

<span data-ttu-id="1aafb-128">Per eliminare un collegamento, nella pagina **Collegamenti**, è possibile selezionare **…** e quindi **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-128">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="1aafb-129">Se si elimina un unico record, ad esempio una riga dell'ordine di vendita, un ordine di vendita o una scheda cliente, tutti i collegamenti associati al record vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="1aafb-129">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="1aafb-130">Tuttavia, se si eliminano dei record utilizzando un processo batch, ad esempio **Elimina ord. vendita fatturati**, i collegamenti sono ancora archiviati nel database.</span><span class="sxs-lookup"><span data-stu-id="1aafb-130">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="1aafb-131">Per eliminare i collegamenti dal database, eseguire la codeunit **Elimina collegamenti record orfani**.</span><span class="sxs-lookup"><span data-stu-id="1aafb-131">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="1aafb-132">A tale scopo, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina collegamenti record orfani** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1aafb-132">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="1aafb-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1aafb-133">See Also</span></span>  
<span data-ttu-id="1aafb-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1aafb-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
