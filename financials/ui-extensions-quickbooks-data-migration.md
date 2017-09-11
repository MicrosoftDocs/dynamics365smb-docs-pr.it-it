---
title: Utilizzo dell'estensione per la migrazione QuickBooks | Documenti Microsoft
description: Descrive come utilizzare l'estensione per importare clienti, fornitori, articoli e conti dal desktop di QuickBooks a Dynamics 365 for Financials.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="7da67-103">Estensione per la migrazione dei dati QuickBooks per Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="7da67-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="7da67-104">Questa estensione consente di eseguire la migrazione di clienti, fornitori, articoli e conti da QuickBooks [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7da67-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7da67-105">Se l'azienda al momento utilizza QuickBooks, è possibile esportare le informazioni rilevanti e aprire una guida al setup assistito per caricare i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7da67-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="7da67-106">Per ulteriori informazioni, vedere [Importazione dei dati aziendali da altri sistemi contabili](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="7da67-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="7da67-107">Esportazione dei dati da QuickBooks</span><span class="sxs-lookup"><span data-stu-id="7da67-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="7da67-108">È necessario aver esportato alcuni o tutti i clienti, i fornitori, gli articoli di magazzino e i conti esistenti in un file IIF (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="7da67-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="7da67-109">L'estensione per la migrazione dei dati QuickBooks include una mappatura predefinita dei dati QuickBooks affinché i dati esistenti possano essere utilizzati per testare la nuova azienda con [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7da67-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="7da67-110">La mappatura predefinita sarà sufficiente nella maggior parte dei casi, ma è possibile modificare la mappatura nella guida al setup assistito.</span><span class="sxs-lookup"><span data-stu-id="7da67-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="7da67-111">Nel menu File di QuickBooks è presente un'utilità per l'esportazione di elenchi.</span><span class="sxs-lookup"><span data-stu-id="7da67-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="7da67-112">Ai fini di [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile esportare i seguenti elenchi:</span><span class="sxs-lookup"><span data-stu-id="7da67-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="7da67-113">Lista clienti</span><span class="sxs-lookup"><span data-stu-id="7da67-113">Customer List</span></span>  
* <span data-ttu-id="7da67-114">Lista fornitori</span><span class="sxs-lookup"><span data-stu-id="7da67-114">Vendor List</span></span>  
* <span data-ttu-id="7da67-115">Elenco articoli</span><span class="sxs-lookup"><span data-stu-id="7da67-115">Item List</span></span>  
* <span data-ttu-id="7da67-116">Lista conti</span><span class="sxs-lookup"><span data-stu-id="7da67-116">Account List</span></span>  

<span data-ttu-id="7da67-117">I dati esportati vengono salvati come file IIF, che può essere successivamente caricato in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7da67-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="7da67-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7da67-118">See Also</span></span>
[<span data-ttu-id="7da67-119">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="7da67-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="7da67-120">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="7da67-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

