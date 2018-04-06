---
title: Utilizzo dell'estensione di migrazione dati C5 | Documenti Microsoft
description: "Utilizzare questa estensione per migrare clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f2b7f66de1caa63edaeb240b35501fb62645c469
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="660e0-103">Estensione di migrazione dati C5 per Business Central</span><span class="sxs-lookup"><span data-stu-id="660e0-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="660e0-104">Questa estensione consente di migrare facilmente clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="660e0-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="660e0-105">È inoltre possibile migrare lo storico dei movimenti per i conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="660e0-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="660e0-106">La società in [!INCLUDE[d365fin](includes/d365fin_md.md)] non deve contenere alcun dato.</span><span class="sxs-lookup"><span data-stu-id="660e0-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="660e0-107">Inoltre, una volta avviata una migrazione, non creare clienti, fornitori, articoli o conti fino al termine della migrazione.</span><span class="sxs-lookup"><span data-stu-id="660e0-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="660e0-108">Quali dati vengono migrati?</span><span class="sxs-lookup"><span data-stu-id="660e0-108">What Data is Migrated?</span></span>
<span data-ttu-id="660e0-109">I seguenti dati vengono migrati per ogni entità:</span><span class="sxs-lookup"><span data-stu-id="660e0-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="660e0-110">**Clienti**</span><span class="sxs-lookup"><span data-stu-id="660e0-110">**Customers**</span></span>
* <span data-ttu-id="660e0-111">Località</span><span class="sxs-lookup"><span data-stu-id="660e0-111">Location</span></span>
* <span data-ttu-id="660e0-112">Paese</span><span class="sxs-lookup"><span data-stu-id="660e0-112">Country</span></span>
* <span data-ttu-id="660e0-113">Dimensioni clienti (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="660e0-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="660e0-114">Metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="660e0-114">Shipment method</span></span>
* <span data-ttu-id="660e0-115">Venditore</span><span class="sxs-lookup"><span data-stu-id="660e0-115">Sales Person</span></span>
* <span data-ttu-id="660e0-116">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="660e0-116">Payment terms</span></span>
* <span data-ttu-id="660e0-117">Metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="660e0-117">Payment method</span></span>
* <span data-ttu-id="660e0-118">Gruppo prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="660e0-118">Customer price group</span></span>
* <span data-ttu-id="660e0-119">Sconto fattura cliente</span><span class="sxs-lookup"><span data-stu-id="660e0-119">Customer invoice discount</span></span>

<span data-ttu-id="660e0-120">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="660e0-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="660e0-121">Setup registrazione cliente</span><span class="sxs-lookup"><span data-stu-id="660e0-121">Customer posting setup</span></span>
* <span data-ttu-id="660e0-122">Batch registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="660e0-122">General journal batch</span></span>
* <span data-ttu-id="660e0-123">Transazioni aperte(movimenti contabili clienti)</span><span class="sxs-lookup"><span data-stu-id="660e0-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="660e0-124">**Fornitori**</span><span class="sxs-lookup"><span data-stu-id="660e0-124">**Vendors**</span></span>
* <span data-ttu-id="660e0-125">Località</span><span class="sxs-lookup"><span data-stu-id="660e0-125">Location</span></span>
* <span data-ttu-id="660e0-126">Paese</span><span class="sxs-lookup"><span data-stu-id="660e0-126">Country</span></span>
* <span data-ttu-id="660e0-127">Dimensioni fornitori (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="660e0-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="660e0-128">Sconto fattura</span><span class="sxs-lookup"><span data-stu-id="660e0-128">Invoice discount</span></span>
* <span data-ttu-id="660e0-129">Metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="660e0-129">Shipment method</span></span>
* <span data-ttu-id="660e0-130">Add. acquisti</span><span class="sxs-lookup"><span data-stu-id="660e0-130">Purchaser</span></span>
* <span data-ttu-id="660e0-131">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="660e0-131">Payment terms</span></span>
* <span data-ttu-id="660e0-132">Metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="660e0-132">Payment method</span></span>
* <span data-ttu-id="660e0-133">Sconto fattura fornitore</span><span class="sxs-lookup"><span data-stu-id="660e0-133">Vendor invoice discount</span></span>

<span data-ttu-id="660e0-134">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="660e0-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="660e0-135">Setup registrazione fornitori</span><span class="sxs-lookup"><span data-stu-id="660e0-135">Vendor posting setup</span></span>
* <span data-ttu-id="660e0-136">Batch registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="660e0-136">General journal batch</span></span>
* <span data-ttu-id="660e0-137">Transazioni aperte(movimenti contabili fornitori)</span><span class="sxs-lookup"><span data-stu-id="660e0-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="660e0-138">**Articoli**</span><span class="sxs-lookup"><span data-stu-id="660e0-138">**Items**</span></span>
* <span data-ttu-id="660e0-139">Località</span><span class="sxs-lookup"><span data-stu-id="660e0-139">Location</span></span>
* <span data-ttu-id="660e0-140">Paese</span><span class="sxs-lookup"><span data-stu-id="660e0-140">Country</span></span>
* <span data-ttu-id="660e0-141">Dimensioni articoli (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="660e0-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="660e0-142">Sconti riga vendita</span><span class="sxs-lookup"><span data-stu-id="660e0-142">Sales line discounts</span></span>
* <span data-ttu-id="660e0-143">Categorie sconto clienti</span><span class="sxs-lookup"><span data-stu-id="660e0-143">Customer discount groups</span></span>
* <span data-ttu-id="660e0-144">Gruppi sconto articolo</span><span class="sxs-lookup"><span data-stu-id="660e0-144">Item discount groups</span></span>
* <span data-ttu-id="660e0-145">Prezzo vendita</span><span class="sxs-lookup"><span data-stu-id="660e0-145">Sales price</span></span>
* <span data-ttu-id="660e0-146">Nomenclatura combinata</span><span class="sxs-lookup"><span data-stu-id="660e0-146">Tariff number</span></span>
* <span data-ttu-id="660e0-147">Unità di misura</span><span class="sxs-lookup"><span data-stu-id="660e0-147">Units of measure</span></span>
* <span data-ttu-id="660e0-148">Codice tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="660e0-148">Item tracking code</span></span>
* <span data-ttu-id="660e0-149">Gruppo prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="660e0-149">Customer price group</span></span>

<span data-ttu-id="660e0-150">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="660e0-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="660e0-151">Setup registrazione magazzino</span><span class="sxs-lookup"><span data-stu-id="660e0-151">Inventory posting setup</span></span>
* <span data-ttu-id="660e0-152">Setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="660e0-152">General posting setup</span></span>
* <span data-ttu-id="660e0-153">Batch registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="660e0-153">Item journal batch</span></span>
* <span data-ttu-id="660e0-154">Transazioni aperte(movimenti contabili articoli)</span><span class="sxs-lookup"><span data-stu-id="660e0-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="660e0-155">Se esistono transazioni aperte che usano valute estere, vengono migrati anche i tassi di cambio per queste valute.</span><span class="sxs-lookup"><span data-stu-id="660e0-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="660e0-156">Altri tassi di cambio non sono migrati.</span><span class="sxs-lookup"><span data-stu-id="660e0-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="660e0-157">Per migrare i dati</span><span class="sxs-lookup"><span data-stu-id="660e0-157">To migrate data</span></span>
<span data-ttu-id="660e0-158">Sono necessari solo alcuni passaggi per esportare i dati da C5 e importarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="660e0-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="660e0-159">In C5, utilizzare la funzione **Esporta database** per esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="660e0-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="660e0-160">Quindi, inviare la cartella di esportazione a una cartella compressa (.zip).</span><span class="sxs-lookup"><span data-stu-id="660e0-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="660e0-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") e immettere **Migrazione dati**, quindi scegliere **Migrazione dati**.</span><span class="sxs-lookup"><span data-stu-id="660e0-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="660e0-162">Completare i passaggi nella guida di setup assistito.</span><span class="sxs-lookup"><span data-stu-id="660e0-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="660e0-163">Assicurarsi di scegliere **Importa da Microsoft Dynamcis C5 2012** come origine dati.</span><span class="sxs-lookup"><span data-stu-id="660e0-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="660e0-164">Le aziende spesso aggiungono campi per personalizzare C5 per il proprio settore specifico.</span><span class="sxs-lookup"><span data-stu-id="660e0-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="660e0-165"> non migra i dati dai campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="660e0-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="660e0-166">Inoltre, la migrazione non avrà esito positivo se sono presenti più di 10 campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="660e0-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="660e0-167">Visualizzazione dello stato della migrazione</span><span class="sxs-lookup"><span data-stu-id="660e0-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="660e0-168">Utilizzare la pagina **Sintesi migrazione dati** per monitorare il successo della migrazione.</span><span class="sxs-lookup"><span data-stu-id="660e0-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="660e0-169">La pagina mostra informazioni quali il numero di entità che la migrazione includerà, lo stato della migrazione e il numero di articoli che sono stati migrati e se la migrazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="660e0-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="660e0-170">Mostra inoltre il numero di errori, consente di analizzare gli errori riscontrati e, se possibile, consente di passare facilmente all'entità per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="660e0-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="660e0-171">Per ulteriori informazioni, vedere la sezione successiva in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="660e0-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="660e0-172">Mentre si attendono i risultati della migrazione, è necessario aggiornare la pagina per visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="660e0-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="660e0-173">Correzione degli errori</span><span class="sxs-lookup"><span data-stu-id="660e0-173">Correcting Errors</span></span>
<span data-ttu-id="660e0-174">Se si verifica un errore, il campo **Stato** mostrerà **Completato con errori**, quindi il campo **Numero di errori** mostrerà il numero degli errori.</span><span class="sxs-lookup"><span data-stu-id="660e0-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="660e0-175">Per visualizzare un elenco degli errori, è possibile aprire la pagina **Errori di migrazione dati** scegliendo:</span><span class="sxs-lookup"><span data-stu-id="660e0-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="660e0-176">Il numero nel campo **Numero di errori** per l'entità.</span><span class="sxs-lookup"><span data-stu-id="660e0-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="660e0-177">L'entità, quindi l'azione **Mostra errori**.</span><span class="sxs-lookup"><span data-stu-id="660e0-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="660e0-178">Nella pagina **Errori di migrazione dati**, per correggere un errore è possibile scegliere un messaggio di errore, quindi **Modifica record** per aprire una pagina che mostra i dati migrati per l'entità.</span><span class="sxs-lookup"><span data-stu-id="660e0-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="660e0-179">Dopo aver corretto uno o più errori, è possibile scegliere **Esegui migrazione** per migrare solo le entità corrette, senza dover riavviare completamente la migrazione.</span><span class="sxs-lookup"><span data-stu-id="660e0-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="660e0-180">Se è stato corretto più di un errore, è possibile utilizzare la funzionalità **Seleziona più elementi** per selezionare più righe da migrare.</span><span class="sxs-lookup"><span data-stu-id="660e0-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="660e0-181">In alternativa, se esistono errori che non è importante correggere, è possibile selezionarli, quindi scegliere **Ignora selezione**.</span><span class="sxs-lookup"><span data-stu-id="660e0-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="660e0-182">Se si dispone di articoli che sono inclusi in una distinta base, potrebbe essere necessario effettuare la migrazione più di una volta se l'articolo originale non viene creato prima delle varianti a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="660e0-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="660e0-183">Se una variante articolo viene creata per prima, il riferimento all'articolo originale può causare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="660e0-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="660e0-184">Verifica dei dati dopo la migrazione</span><span class="sxs-lookup"><span data-stu-id="660e0-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="660e0-185">Un modo per verificare che i dati siano stati migrati correttamente consiste nell'esaminare le seguenti pagine in C5 e [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="660e0-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="660e0-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="660e0-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="660e0-187">Movimenti clienti</span><span class="sxs-lookup"><span data-stu-id="660e0-187">Customer Entries</span></span>| <span data-ttu-id="660e0-188">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="660e0-188">General Journals</span></span>|
|<span data-ttu-id="660e0-189">Movimenti fornitori</span><span class="sxs-lookup"><span data-stu-id="660e0-189">Vendor Entries</span></span>| <span data-ttu-id="660e0-190">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="660e0-190">General Journals</span></span>|
|<span data-ttu-id="660e0-191">Mov. Articoli</span><span class="sxs-lookup"><span data-stu-id="660e0-191">Item Entries</span></span>| <span data-ttu-id="660e0-192">Registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="660e0-192">Item Journals</span></span>|

<span data-ttu-id="660e0-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], il batch per i dati migrati è denominato **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="660e0-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="660e0-194">Interruzione della migrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="660e0-194">Stopping Data Migration</span></span>
<span data-ttu-id="660e0-195">È possibile interrompere la migrazione dei dati scegliendo **Interrompi tutte le migrazioni**.</span><span class="sxs-lookup"><span data-stu-id="660e0-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="660e0-196">In tal caso, tutte le migrazioni in sospeso vengono interrotte.</span><span class="sxs-lookup"><span data-stu-id="660e0-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="660e0-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="660e0-197">See Also</span></span>
<span data-ttu-id="660e0-198">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="660e0-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="660e0-199">[Benvenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="660e0-199">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

