---
title: Come creare collegamenti a informazioni o programmi esterni nei record | Microsoft Docs
description: Aggiungere un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3ccedd0f5bede5dc692b1fec89d87e708047a622
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="4cdb8-103">Aggiunta di collegamenti a siti Web, documenti o programmi nei record</span><span class="sxs-lookup"><span data-stu-id="4cdb8-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="4cdb8-104">In un record specifico, ad esempio un cliente, un documento o un ordine di vendita, è possibile aggiungere un collegamento a un sito Web, programma o documento esterno.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="4cdb8-105">In alternativa, è possibile creare un collegamento che apre un nuovo messaggio e-mail vuoto a un cliente specifico quando lo si seleziona.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="4cdb8-106">La pagina schede di alcuni record, ad esempio schede clienti e fornitori, includono un campo **Home page** in cui è possibile immettere un indirizzo Internet (URL).</span><span class="sxs-lookup"><span data-stu-id="4cdb8-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="4cdb8-107">Per includere altri collegamenti, è possibile utilizzare il metodo descritto in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="4cdb8-108">Un altro esempio potrebbe essere quando si ricevono fatture stampate dai fornitori.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="4cdb8-109">È possibile digitalizzarle e salvarle come file .pdf in un sito SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="4cdb8-110">È quindi possibile creare un collegamento da una fattura di acquisto in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] alla fattura corrispondente in SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="4cdb8-111">In alternativa, è possibile creare un collegamento da una scheda articolo nella pagina corrispondente nel catalogo in linea del fornitore.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>
  
## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="4cdb8-112">Per aggiungere un collegamento in un record</span><span class="sxs-lookup"><span data-stu-id="4cdb8-112">To add a link on a record</span></span>   
  
1.  <span data-ttu-id="4cdb8-113">Aprire il record a cui si desidera associare il collegamento, ad esempio una scheda cliente o un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="4cdb8-114">Se si desidera associare il collegamento a una riga specifica, ad esempio una riga di registrazione, selezionare la riga.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  
  
2.  <span data-ttu-id="4cdb8-115">Scegliere l'azione **Collegamenti** per aprire la finestra **Collegamenti** in cui vengono visualizzati tutti i collegamenti correnti aggiunti al record.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="4cdb8-116">Per aggiungere un nuovo collegamento, scegliere **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-116">To add a new link, choose **+new**.</span></span> 
  
4.  <span data-ttu-id="4cdb8-117">Nel campo **Indirizzo collegamento**, immettere</span><span class="sxs-lookup"><span data-stu-id="4cdb8-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="4cdb8-118">Per creare un collegamento a un file nel computer o in rete, immettere il percorso completo e il nome di file, ad esempio **C:Documenti\Fattura1.doc**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="4cdb8-119">Per creare un collegamento a un sito Web, immettere l'indirizzo Internet (URL), ad esempio **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span> 
    -   <span data-ttu-id="4cdb8-120">Per creare un collegamento a un sito Web, immettere l'indirizzo Internet (URL), ad esempio **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span> 
    -   <span data-ttu-id="4cdb8-121">Per creare un collegamento a un programma, immettere una stringa specifica per aprire il programma.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="4cdb8-122">Ad esempio, per aprire OneNote con una pagina specifica, immettere **onenote:///C:Documenti\test.one**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="4cdb8-123">Oppure per aprire Outlook con una nuova e-mail vuota a un alias specifico, immettere **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  
  
5.  <span data-ttu-id="4cdb8-124">Nel campo **Descrizione** inserire informazioni relative al collegamento.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-124">Fill in the **Description** field with information about the link.</span></span>  
  
6.  <span data-ttu-id="4cdb8-125">Fare clic sul pulsante **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-125">Choose the **Save** button.</span></span>  
  
## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="4cdb8-126">Per eliminare un collegamento da un record</span><span class="sxs-lookup"><span data-stu-id="4cdb8-126">To delete a link from a record</span></span>  
  
<span data-ttu-id="4cdb8-127">Per eliminare un collegamento, nella finestra **Collegamenti**, è possibile selezionare **…** e quindi **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="4cdb8-128">Se si elimina un unico record, ad esempio una riga dell'ordine di vendita, un ordine di vendita o una scheda cliente, tutti i collegamenti associati al record vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="4cdb8-129">Tuttavia, se si eliminano dei record utilizzando un processo batch, ad esempio **Elimina ord. vendita fatturati**, i collegamenti sono ancora archiviati nel database.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="4cdb8-130">Per eliminare i collegamenti dal database, eseguire la codeunit **Elimina collegamenti record orfani**.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="4cdb8-131">A questo proposito, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Elimina collegamenti record orfani**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4cdb8-131">To do this, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   
  
<!-- ### To run delete orphaned record links  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  
  
2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->
  
## <a name="see-also"></a><span data-ttu-id="4cdb8-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cdb8-132">See Also</span></span>  
<span data-ttu-id="4cdb8-133">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4cdb8-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
