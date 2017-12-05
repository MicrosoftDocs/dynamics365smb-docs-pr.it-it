---
title: Utilizzo dell'estensione di migrazione dati C5 | Documenti Microsoft
description: "Utilizzare questa estensione per migrare clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: it-it
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="08e40-103">Estensione di migrazione dati C5 per Dynamics 365 for Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="08e40-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="08e40-104">Questa estensione consente di migrare facilmente clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08e40-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="08e40-105">La società in [!INCLUDE[d365fin](includes/d365fin_md.md)] non deve contenere alcun dato.</span><span class="sxs-lookup"><span data-stu-id="08e40-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="08e40-106">Inoltre, una volta avviata una migrazione, non creare clienti, fornitori, articoli o conti fino al termine della migrazione.</span><span class="sxs-lookup"><span data-stu-id="08e40-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="08e40-107">Per migrare i dati</span><span class="sxs-lookup"><span data-stu-id="08e40-107">To migrate data</span></span>
<span data-ttu-id="08e40-108">Sono necessari solo alcuni passaggi per esportare i dati da C5 e importarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="08e40-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="08e40-109">In C5, utilizzare la funzione **Esporta database** per esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="08e40-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="08e40-110">Quindi, inviare la cartella di esportazione a una cartella compressa (.zip).</span><span class="sxs-lookup"><span data-stu-id="08e40-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="08e40-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") e immettere **Migrazione dati**, quindi scegliere **Migrazione dati**.</span><span class="sxs-lookup"><span data-stu-id="08e40-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="08e40-112">Completare i passaggi nella guida di setup assistito.</span><span class="sxs-lookup"><span data-stu-id="08e40-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="08e40-113">Assicurarsi di scegliere **Importa da Microsoft Dynamcis C5 2012** come origine dati.</span><span class="sxs-lookup"><span data-stu-id="08e40-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="08e40-114">Le aziende spesso aggiungono campi per personalizzare C5 per il proprio settore specifico.</span><span class="sxs-lookup"><span data-stu-id="08e40-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="08e40-115"> non migra i dati dai campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="08e40-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="08e40-116">Inoltre, la migrazione non avrà esito positivo se sono presenti più di 10 campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="08e40-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="08e40-117">Visualizzazione dello stato della migrazione</span><span class="sxs-lookup"><span data-stu-id="08e40-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="08e40-118">Utilizzare la pagina **Sintesi migrazione dati** per monitorare il successo della migrazione.</span><span class="sxs-lookup"><span data-stu-id="08e40-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="08e40-119">La pagina mostra informazioni quali il numero di entità che la migrazione includerà, lo stato della migrazione e il numero di articoli che sono stati migrati e se la migrazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="08e40-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="08e40-120">Mostra inoltre il numero di errori, consente di analizzare gli errori riscontrati e, se possibile, consente di passare facilmente all'entità per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="08e40-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="08e40-121">Per ulteriori informazioni, vedere la sezione successiva in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="08e40-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="08e40-122">Mentre si attendono i risultati della migrazione, è necessario aggiornare la pagina per visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="08e40-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="08e40-123">Correzione degli errori</span><span class="sxs-lookup"><span data-stu-id="08e40-123">Correcting Errors</span></span>
<span data-ttu-id="08e40-124">Se si verifica un errore, il campo **Stato** mostrerà **Completato con errori**, quindi il campo **Numero di errori** mostrerà il numero degli errori.</span><span class="sxs-lookup"><span data-stu-id="08e40-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="08e40-125">Per visualizzare un elenco degli errori, è possibile aprire la pagina **Errori di migrazione dati** scegliendo:</span><span class="sxs-lookup"><span data-stu-id="08e40-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="08e40-126">Il numero nel campo **Numero di errori** per l'entità.</span><span class="sxs-lookup"><span data-stu-id="08e40-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="08e40-127">L'entità, quindi l'azione **Mostra errori**.</span><span class="sxs-lookup"><span data-stu-id="08e40-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="08e40-128">Nella pagina **Errori di migrazione dati**, per correggere un errore è possibile scegliere un messaggio di errore, quindi **Modifica record** per aprire una pagina che mostra i dati migrati per l'entità.</span><span class="sxs-lookup"><span data-stu-id="08e40-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="08e40-129">Dopo aver corretto uno o più errori, è possibile scegliere **Esegui migrazione** per migrare solo le entità corrette, senza dover riavviare completamente la migrazione.</span><span class="sxs-lookup"><span data-stu-id="08e40-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="08e40-130">Se è stato corretto più di un errore, è possibile utilizzare la funzionalità **Seleziona più elementi** per selezionare più righe da migrare.</span><span class="sxs-lookup"><span data-stu-id="08e40-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="08e40-131">In alternativa, se esistono errori che non è importante correggere, è possibile selezionarli, quindi scegliere **Ignora selezione**.</span><span class="sxs-lookup"><span data-stu-id="08e40-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="08e40-132">Se si dispone di articoli che sono inclusi in una distinta base, potrebbe essere necessario effettuare la migrazione più di una volta se l'articolo originale non viene creato prima delle varianti a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="08e40-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="08e40-133">Se una variante articolo viene creata per prima, il riferimento all'articolo originale può causare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="08e40-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="08e40-134">Verifica dei dati dopo la migrazione</span><span class="sxs-lookup"><span data-stu-id="08e40-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="08e40-135">Se si desidera verificare che i dati siano stati migrati correttamente, è possibile esaminare le seguenti pagine in C5 e [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="08e40-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="08e40-136">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="08e40-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="08e40-137">Movimenti clienti</span><span class="sxs-lookup"><span data-stu-id="08e40-137">Customer Entries</span></span>| <span data-ttu-id="08e40-138">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="08e40-138">General Journals</span></span>|
|<span data-ttu-id="08e40-139">Movimenti fornitori</span><span class="sxs-lookup"><span data-stu-id="08e40-139">Vendor Entries</span></span>| <span data-ttu-id="08e40-140">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="08e40-140">General Journals</span></span>|
|<span data-ttu-id="08e40-141">Mov. Articoli</span><span class="sxs-lookup"><span data-stu-id="08e40-141">Item Entries</span></span>| <span data-ttu-id="08e40-142">Registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="08e40-142">Item Journals</span></span>|

<span data-ttu-id="08e40-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], il batch per i dati migrati è denominato **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="08e40-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="08e40-144">Interruzione della migrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="08e40-144">Stopping Data Migration</span></span>
<span data-ttu-id="08e40-145">È possibile interrompere la migrazione dei dati scegliendo **Interrompi tutte le migrazioni**.</span><span class="sxs-lookup"><span data-stu-id="08e40-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="08e40-146">In tal caso, tutte le migrazioni in sospeso vengono interrotte.</span><span class="sxs-lookup"><span data-stu-id="08e40-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="08e40-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08e40-147">See Also</span></span>
<span data-ttu-id="08e40-148">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="08e40-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="08e40-149">[Benvenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="08e40-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

