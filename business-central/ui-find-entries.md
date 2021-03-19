---
title: Ricerca di movimenti | Microsoft Docs
description: In questo articolo viene descritto la correlazione tra documenti e movimenti
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 437e0c076b664ad35d5819783e98d9e91abee982
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393976"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="17f63-103">Ricerca di movimenti correlati per documenti registrati</span><span class="sxs-lookup"><span data-stu-id="17f63-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="17f63-104">In questo articolo viene illustrato come trovare documenti e movimenti correlati tra loro in base a informazioni comuni, come:</span><span class="sxs-lookup"><span data-stu-id="17f63-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="17f63-105">Numero del documento o data di registrazione</span><span class="sxs-lookup"><span data-stu-id="17f63-105">Document number or posting date</span></span>
- <span data-ttu-id="17f63-106">Tipo di contatto commerciale, numero o numero di documento esterno</span><span class="sxs-lookup"><span data-stu-id="17f63-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="17f63-107">Numero di serie dell'articolo o numero di lotto</span><span class="sxs-lookup"><span data-stu-id="17f63-107">Item serial number or lot number</span></span>

<span data-ttu-id="17f63-108">Questa funzione risulta utile per cercare i movimenti contabili ottenuti da determinate transazioni.</span><span class="sxs-lookup"><span data-stu-id="17f63-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="17f63-109">Durante la ricerca per numero di documento, è possibile stampare il riepilogo dal report Movimenti documento.</span><span class="sxs-lookup"><span data-stu-id="17f63-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="17f63-110">Inizia</span><span class="sxs-lookup"><span data-stu-id="17f63-110">Get started</span></span>

<span data-ttu-id="17f63-111">La funzione Trova movimenti è immediatamente disponibile sulla maggior parte delle pagine che visualizzano documenti registrati o movimenti di documenti registrati, sia per elenchi che per schede.</span><span class="sxs-lookup"><span data-stu-id="17f63-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="17f63-112">Quindi il primo passo è aprire una di queste pagine.</span><span class="sxs-lookup"><span data-stu-id="17f63-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="17f63-113">Quindi, scegliere l'azione **Trova movimenti** o premere i tasti Alt + G.</span><span class="sxs-lookup"><span data-stu-id="17f63-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="17f63-114">La pagina **Trova movimenti** include tutti i documenti e i movimenti correlati basati sul numero di documento e sulla data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="17f63-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="17f63-115">La pagina è divisa in tre sezioni:</span><span class="sxs-lookup"><span data-stu-id="17f63-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="17f63-116">La sezione superiore mostra i campi e le azioni che si utilizzano per filtrare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="17f63-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="17f63-117">La sezione centrale mostra i documenti correlati in base alla ricerca.</span><span class="sxs-lookup"><span data-stu-id="17f63-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="17f63-118">La sezione inferiore mostra le informazioni sul documento di origine trovato durante la ricerca.</span><span class="sxs-lookup"><span data-stu-id="17f63-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="17f63-119">Ricerca di movimenti</span><span class="sxs-lookup"><span data-stu-id="17f63-119">Search for entries</span></span>

<span data-ttu-id="17f63-120">È possibile cercare movimenti in base alle informazioni sul documento, al contatto commerciale o al riferimento articolo.</span><span class="sxs-lookup"><span data-stu-id="17f63-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="17f63-121">Per modificare la ricerca, selezionare **Azioni**, **Trova per**, quindi una delle seguenti azioni:</span><span class="sxs-lookup"><span data-stu-id="17f63-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="17f63-122">Azione</span><span class="sxs-lookup"><span data-stu-id="17f63-122">Action</span></span>|<span data-ttu-id="17f63-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17f63-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="17f63-124">Trova per documento</span><span class="sxs-lookup"><span data-stu-id="17f63-124">Find by Document</span></span>|<span data-ttu-id="17f63-125">Visualizzare i movimenti in base a un numero di documento o una data di registrazione specifici.</span><span class="sxs-lookup"><span data-stu-id="17f63-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="17f63-126">Contatto business</span><span class="sxs-lookup"><span data-stu-id="17f63-126">Business Contact</span></span> |<span data-ttu-id="17f63-127">Visualizzare i movimenti in base a un tipo di contatto specifico, numero di contatto e/o numero di documento esterno.</span><span class="sxs-lookup"><span data-stu-id="17f63-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="17f63-128">È possibile immettere le informazioni sul documento assegnato da un fornitore o un cliente.</span><span class="sxs-lookup"><span data-stu-id="17f63-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="17f63-129">Utilizzare i campi disponibili per ricercare i documenti del fornitore utilizzando i numeri da lui assegnati ai documenti.</span><span class="sxs-lookup"><span data-stu-id="17f63-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="17f63-130">Riferimento articolo</span><span class="sxs-lookup"><span data-stu-id="17f63-130">Item reference</span></span>|<span data-ttu-id="17f63-131">Visualizzare i movimenti in base a un numero di serie o un numero di lotto.</span><span class="sxs-lookup"><span data-stu-id="17f63-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="17f63-132">È possibile immettere il numero seriale o di lotto oppure un filtro sui numeri seriali o di lotto di cui si desidera eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="17f63-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="17f63-133">Questa azione risulta utile per visualizzare elementi in cui è stato utilizzato un numero di tracciabilità articolo specifico, individuarne il fornitore di origine o il cliente a cui è stata effettuata la vendita.</span><span class="sxs-lookup"><span data-stu-id="17f63-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="17f63-134">Dopo aver effettuato una selezione, inserire le informazioni di ricerca pertinenti nei campi in alto.</span><span class="sxs-lookup"><span data-stu-id="17f63-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="17f63-135">Usare i suggerimenti dei campi come aiuto.</span><span class="sxs-lookup"><span data-stu-id="17f63-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="17f63-136">Al termine, scegliere **Trova** per avviare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="17f63-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="17f63-137">Se si modifica qualsiasi filtro, è necessario scegliere nuovamente **Trova**.</span><span class="sxs-lookup"><span data-stu-id="17f63-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="17f63-138">Per un paio di esempi sull'utilizzo di **Trova movimenti**, vedere [Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md) e [Procedura dettagliata: Tracciabilità dei numeri seriali/lotto](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="17f63-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="17f63-139">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="17f63-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="17f63-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="17f63-140">See Also</span></span>

[<span data-ttu-id="17f63-141">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="17f63-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="17f63-142">Aggiungere un'azione di pagina a Gestione ruolo utente</span><span class="sxs-lookup"><span data-stu-id="17f63-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="17f63-143">Tracciare gli articoli tracciati</span><span class="sxs-lookup"><span data-stu-id="17f63-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]