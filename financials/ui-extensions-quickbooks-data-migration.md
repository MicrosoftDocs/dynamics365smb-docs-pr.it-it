---
title: Utilizzo dell'estensione per la migrazione QuickBooks | Documenti Microsoft
description: Descrive come utilizzare l'estensione per importare clienti, fornitori, articoli e conti da QuickBooks Desktop in Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 14e0aea700bbb46a612d8e462ace22b10faac7e2
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="the-quickbooks-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="814fc-103">Estensione di migrazione dati per QuickBooks for Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="814fc-103">The QuickBooks Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="814fc-104">Questa estensione consente di eseguire la migrazione di clienti, fornitori, articoli e conti da QuickBooks [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="814fc-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="814fc-105">Se l'azienda al momento utilizza QuickBooks, è possibile esportare le informazioni rilevanti e aprire una guida al setup assistito per caricare i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="814fc-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="814fc-106">Per ulteriori informazioni, vedere [Importazione dei dati aziendali da altri sistemi contabili](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="814fc-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="814fc-107">Esportazione di dati da QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="814fc-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="814fc-108">È necessario aver esportato alcuni o tutti i clienti, i fornitori, gli articoli di magazzino e i conti esistenti in un file IIF (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="814fc-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="814fc-109">L'estensione per la migrazione dei dati QuickBooks include una mappatura predefinita dei dati QuickBooks affinché i dati esistenti possano essere utilizzati per testare la nuova azienda con [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="814fc-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="814fc-110">La mappatura predefinita sarà sufficiente nella maggior parte dei casi, ma è possibile modificare la mappatura nella guida al setup assistito.</span><span class="sxs-lookup"><span data-stu-id="814fc-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="814fc-111">Nel menu File di QuickBooks è presente un'utilità per l'esportazione di elenchi.</span><span class="sxs-lookup"><span data-stu-id="814fc-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="814fc-112">Ai fini di [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile esportare i seguenti elenchi:</span><span class="sxs-lookup"><span data-stu-id="814fc-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="814fc-113">Lista clienti</span><span class="sxs-lookup"><span data-stu-id="814fc-113">Customer List</span></span>  
* <span data-ttu-id="814fc-114">Lista fornitori</span><span class="sxs-lookup"><span data-stu-id="814fc-114">Vendor List</span></span>  
* <span data-ttu-id="814fc-115">Elenco articoli</span><span class="sxs-lookup"><span data-stu-id="814fc-115">Item List</span></span>  
* <span data-ttu-id="814fc-116">Lista conti</span><span class="sxs-lookup"><span data-stu-id="814fc-116">Account List</span></span>  

<span data-ttu-id="814fc-117">I dati esportati vengono salvati come file IIF, che può essere successivamente caricato in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="814fc-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="814fc-118">Utilizzo dell'estensione per la migrazione dei dati QuickBooks</span><span class="sxs-lookup"><span data-stu-id="814fc-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="814fc-119">L'estensione per la migrazione dei dati QuickBooks si trova nella Guida setup assistito Migrazione dati ed è pronta all'uso.</span><span class="sxs-lookup"><span data-stu-id="814fc-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="814fc-120">Per utilizzare l'estensione dopo aver esportato i dati da QuickBooks, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup assistito**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="814fc-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="814fc-121">Scegliere **Migra dati aziendali**, quindi seguire i passaggi nella guida.</span><span class="sxs-lookup"><span data-stu-id="814fc-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="814fc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="814fc-122">See Also</span></span>
[<span data-ttu-id="814fc-123">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="814fc-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="814fc-124">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="814fc-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

