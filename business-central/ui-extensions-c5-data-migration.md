---
title: Utilizzo dell'estensione di migrazione dati C5 | Documenti Microsoft
description: "Utilizzare questa estensione per migrare clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: it-it
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="c8465-103">Estensione di migrazione dati C5 per Business Central</span><span class="sxs-lookup"><span data-stu-id="c8465-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="c8465-104">Questa estensione consente di migrare facilmente clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c8465-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c8465-105">È inoltre possibile migrare lo storico dei movimenti per i conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="c8465-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="c8465-106">La società in [!INCLUDE[d365fin](includes/d365fin_md.md)] non deve contenere alcun dato.</span><span class="sxs-lookup"><span data-stu-id="c8465-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="c8465-107">Inoltre, una volta avviata una migrazione, non creare clienti, fornitori, articoli o conti fino al termine della migrazione.</span><span class="sxs-lookup"><span data-stu-id="c8465-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="c8465-108">Quali dati vengono migrati?</span><span class="sxs-lookup"><span data-stu-id="c8465-108">What Data is Migrated?</span></span>
<span data-ttu-id="c8465-109">I seguenti dati vengono migrati per ogni entità:</span><span class="sxs-lookup"><span data-stu-id="c8465-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="c8465-110">**Clienti**</span><span class="sxs-lookup"><span data-stu-id="c8465-110">**Customers**</span></span>
* <span data-ttu-id="c8465-111">Località</span><span class="sxs-lookup"><span data-stu-id="c8465-111">Location</span></span>
* <span data-ttu-id="c8465-112">Paese</span><span class="sxs-lookup"><span data-stu-id="c8465-112">Country</span></span>
* <span data-ttu-id="c8465-113">Dimensioni clienti (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="c8465-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c8465-114">Metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="c8465-114">Shipment method</span></span>
* <span data-ttu-id="c8465-115">Venditore</span><span class="sxs-lookup"><span data-stu-id="c8465-115">Sales Person</span></span>
* <span data-ttu-id="c8465-116">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="c8465-116">Payment terms</span></span>
* <span data-ttu-id="c8465-117">Metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="c8465-117">Payment method</span></span>
* <span data-ttu-id="c8465-118">Gruppo prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="c8465-118">Customer price group</span></span>
* <span data-ttu-id="c8465-119">Sconto fattura cliente</span><span class="sxs-lookup"><span data-stu-id="c8465-119">Customer invoice discount</span></span>

<span data-ttu-id="c8465-120">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="c8465-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c8465-121">Setup registrazione cliente</span><span class="sxs-lookup"><span data-stu-id="c8465-121">Customer posting setup</span></span>
* <span data-ttu-id="c8465-122">Batch registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="c8465-122">General journal batch</span></span>
* <span data-ttu-id="c8465-123">Transazioni aperte(movimenti contabili clienti)</span><span class="sxs-lookup"><span data-stu-id="c8465-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="c8465-124">**Fornitori**</span><span class="sxs-lookup"><span data-stu-id="c8465-124">**Vendors**</span></span>
* <span data-ttu-id="c8465-125">Località</span><span class="sxs-lookup"><span data-stu-id="c8465-125">Location</span></span>
* <span data-ttu-id="c8465-126">Paese</span><span class="sxs-lookup"><span data-stu-id="c8465-126">Country</span></span>
* <span data-ttu-id="c8465-127">Dimensioni fornitori (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="c8465-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c8465-128">Sconto fattura</span><span class="sxs-lookup"><span data-stu-id="c8465-128">Invoice discount</span></span>
* <span data-ttu-id="c8465-129">Metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="c8465-129">Shipment method</span></span>
* <span data-ttu-id="c8465-130">Add. acquisti</span><span class="sxs-lookup"><span data-stu-id="c8465-130">Purchaser</span></span>
* <span data-ttu-id="c8465-131">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="c8465-131">Payment terms</span></span>
* <span data-ttu-id="c8465-132">Metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="c8465-132">Payment method</span></span>
* <span data-ttu-id="c8465-133">Sconto fattura fornitore</span><span class="sxs-lookup"><span data-stu-id="c8465-133">Vendor invoice discount</span></span>

<span data-ttu-id="c8465-134">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="c8465-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c8465-135">Setup registrazione fornitori</span><span class="sxs-lookup"><span data-stu-id="c8465-135">Vendor posting setup</span></span>
* <span data-ttu-id="c8465-136">Batch registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="c8465-136">General journal batch</span></span>
* <span data-ttu-id="c8465-137">Transazioni aperte(movimenti contabili fornitori)</span><span class="sxs-lookup"><span data-stu-id="c8465-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="c8465-138">**Articoli**</span><span class="sxs-lookup"><span data-stu-id="c8465-138">**Items**</span></span>
* <span data-ttu-id="c8465-139">Località</span><span class="sxs-lookup"><span data-stu-id="c8465-139">Location</span></span>
* <span data-ttu-id="c8465-140">Paese</span><span class="sxs-lookup"><span data-stu-id="c8465-140">Country</span></span>
* <span data-ttu-id="c8465-141">Dimensioni articoli (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="c8465-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c8465-142">Sconti riga vendita</span><span class="sxs-lookup"><span data-stu-id="c8465-142">Sales line discounts</span></span>
* <span data-ttu-id="c8465-143">Categorie sconto clienti</span><span class="sxs-lookup"><span data-stu-id="c8465-143">Customer discount groups</span></span>
* <span data-ttu-id="c8465-144">Gruppi sconto articolo</span><span class="sxs-lookup"><span data-stu-id="c8465-144">Item discount groups</span></span>
* <span data-ttu-id="c8465-145">Prezzo vendita</span><span class="sxs-lookup"><span data-stu-id="c8465-145">Sales price</span></span>
* <span data-ttu-id="c8465-146">Nomenclatura combinata</span><span class="sxs-lookup"><span data-stu-id="c8465-146">Tariff number</span></span>
* <span data-ttu-id="c8465-147">Unità di misura</span><span class="sxs-lookup"><span data-stu-id="c8465-147">Units of measure</span></span>
* <span data-ttu-id="c8465-148">Codice tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="c8465-148">Item tracking code</span></span>
* <span data-ttu-id="c8465-149">Gruppo prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="c8465-149">Customer price group</span></span>

<span data-ttu-id="c8465-150">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="c8465-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c8465-151">Setup registrazione magazzino</span><span class="sxs-lookup"><span data-stu-id="c8465-151">Inventory posting setup</span></span>
* <span data-ttu-id="c8465-152">Setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="c8465-152">General posting setup</span></span>
* <span data-ttu-id="c8465-153">Batch registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="c8465-153">Item journal batch</span></span>
* <span data-ttu-id="c8465-154">Transazioni aperte(movimenti contabili articoli)</span><span class="sxs-lookup"><span data-stu-id="c8465-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="c8465-155">Se esistono transazioni aperte che usano valute estere, vengono migrati anche i tassi di cambio per queste valute.</span><span class="sxs-lookup"><span data-stu-id="c8465-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="c8465-156">Altri tassi di cambio non sono migrati.</span><span class="sxs-lookup"><span data-stu-id="c8465-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="c8465-157">**Piano dei conti**</span><span class="sxs-lookup"><span data-stu-id="c8465-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="c8465-158">Dimensioni standard: reparto, scopo e centro di costo</span><span class="sxs-lookup"><span data-stu-id="c8465-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="c8465-159">Transazioni storiche C/G</span><span class="sxs-lookup"><span data-stu-id="c8465-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="c8465-160">Le transazioni storiche C/G vengono trattate in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="c8465-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="c8465-161">Quando si migrano i dati si imposta un parametro **Periodo corrente**.</span><span class="sxs-lookup"><span data-stu-id="c8465-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="c8465-162">Questo parametro consente di elaborare le transazioni C/G.</span><span class="sxs-lookup"><span data-stu-id="c8465-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="c8465-163">Le transazioni dopo questa data vengono migrate singolarmente.</span><span class="sxs-lookup"><span data-stu-id="c8465-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="c8465-164">Le operazioni precedenti alla data vengono aggregate per conto e migrate come importo singolo.</span><span class="sxs-lookup"><span data-stu-id="c8465-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="c8465-165">Ad esempio, sono presenti transazioni nel 2015, 2016, 2017, 2018 e si specifica il 1° gennaio 2017 nel campo Periodo corrente.</span><span class="sxs-lookup"><span data-stu-id="c8465-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="c8465-166">Per ogni conto, gli importi per le transazioni il 31 dicembre 2106 o in data precedente verranno aggregate in un'unica riga del giornale di registrazione generale per ciascun conto C/G.</span><span class="sxs-lookup"><span data-stu-id="c8465-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="c8465-167">Tutte le transazioni dopo questa data verranno migrate singolarmente.</span><span class="sxs-lookup"><span data-stu-id="c8465-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="c8465-168">Per migrare i dati</span><span class="sxs-lookup"><span data-stu-id="c8465-168">To migrate data</span></span>
<span data-ttu-id="c8465-169">Sono necessari solo alcuni passaggi per esportare i dati da C5 e importarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="c8465-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="c8465-170">In C5, utilizzare la funzione **Esporta database** per esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="c8465-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="c8465-171">Quindi, inviare la cartella di esportazione a una cartella compressa (.zip).</span><span class="sxs-lookup"><span data-stu-id="c8465-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="c8465-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") e immettere **Migrazione dati**, quindi scegliere **Migrazione dati**.</span><span class="sxs-lookup"><span data-stu-id="c8465-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="c8465-173">Completare i passaggi nella guida di setup assistito.</span><span class="sxs-lookup"><span data-stu-id="c8465-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="c8465-174">Assicurarsi di scegliere **Importa da Microsoft Dynamcis C5 2012** come origine dati.</span><span class="sxs-lookup"><span data-stu-id="c8465-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="c8465-175">Le aziende spesso aggiungono campi per personalizzare C5 per il proprio settore specifico.</span><span class="sxs-lookup"><span data-stu-id="c8465-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="c8465-176"> non migra i dati dai campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c8465-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="c8465-177">Inoltre, la migrazione non avrà esito positivo se sono presenti più di 10 campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c8465-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="c8465-178">Visualizzazione dello stato della migrazione</span><span class="sxs-lookup"><span data-stu-id="c8465-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="c8465-179">Utilizzare la pagina **Sintesi migrazione dati** per monitorare il successo della migrazione.</span><span class="sxs-lookup"><span data-stu-id="c8465-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="c8465-180">La pagina mostra informazioni quali il numero di entità che la migrazione includerà, lo stato della migrazione e il numero di articoli che sono stati migrati e se la migrazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c8465-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="c8465-181">Mostra inoltre il numero di errori, consente di analizzare gli errori riscontrati e, se possibile, consente di passare facilmente all'entità per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="c8465-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="c8465-182">Per ulteriori informazioni, vedere la sezione successiva in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c8465-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="c8465-183">Mentre si attendono i risultati della migrazione, è necessario aggiornare la pagina per visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="c8465-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="c8465-184">Come evitare la doppia registrazione</span><span class="sxs-lookup"><span data-stu-id="c8465-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="c8465-185">Per evitare la doppia registrazione in contabilità generale, vengono utilizzati i seguenti conti di contropartita per le transazioni aperte:</span><span class="sxs-lookup"><span data-stu-id="c8465-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="c8465-186">Per i fornitori, si usa il conto v/fornitori della categoria di registrazione fornitori.</span><span class="sxs-lookup"><span data-stu-id="c8465-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="c8465-187">Per i clienti, si usa il conto v/clienti della categoria di registrazione clienti.</span><span class="sxs-lookup"><span data-stu-id="c8465-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="c8465-188">Per gli articoli, si crea una registrazione COGE dove il conto di rettifica è il conto specificato come conto relativo al magazzino nel setup della registrazione magazzino.</span><span class="sxs-lookup"><span data-stu-id="c8465-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="c8465-189">Correzione degli errori</span><span class="sxs-lookup"><span data-stu-id="c8465-189">Correcting Errors</span></span>
<span data-ttu-id="c8465-190">Se si verifica un errore, il campo **Stato** mostrerà **Completato con errori**, quindi il campo **Numero di errori** mostrerà il numero degli errori.</span><span class="sxs-lookup"><span data-stu-id="c8465-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="c8465-191">Per visualizzare un elenco degli errori, è possibile aprire la pagina **Errori di migrazione dati** scegliendo:</span><span class="sxs-lookup"><span data-stu-id="c8465-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="c8465-192">Il numero nel campo **Numero di errori** per l'entità.</span><span class="sxs-lookup"><span data-stu-id="c8465-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="c8465-193">L'entità, quindi l'azione **Mostra errori**.</span><span class="sxs-lookup"><span data-stu-id="c8465-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="c8465-194">Nella pagina **Errori di migrazione dati**, per correggere un errore è possibile scegliere un messaggio di errore, quindi **Modifica record** per aprire una pagina che mostra i dati migrati per l'entità.</span><span class="sxs-lookup"><span data-stu-id="c8465-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="c8465-195">Dopo aver corretto uno o più errori, è possibile scegliere **Esegui migrazione** per migrare solo le entità corrette, senza dover riavviare completamente la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c8465-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="c8465-196">Se è stato corretto più di un errore, è possibile utilizzare la funzionalità **Seleziona più elementi** per selezionare più righe da migrare.</span><span class="sxs-lookup"><span data-stu-id="c8465-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="c8465-197">In alternativa, se esistono errori che non è importante correggere, è possibile selezionarli, quindi scegliere **Ignora selezione**.</span><span class="sxs-lookup"><span data-stu-id="c8465-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="c8465-198">Se si dispone di articoli che sono inclusi in una distinta base, potrebbe essere necessario effettuare la migrazione più di una volta se l'articolo originale non viene creato prima delle varianti a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="c8465-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="c8465-199">Se una variante articolo viene creata per prima, il riferimento all'articolo originale può causare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="c8465-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="c8465-200">Verifica dei dati dopo la migrazione</span><span class="sxs-lookup"><span data-stu-id="c8465-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="c8465-201">Un modo per verificare che i dati siano stati migrati correttamente consiste nell'esaminare le seguenti pagine in C5 e [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c8465-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="c8465-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="c8465-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="c8465-203">Processo batch da usare</span><span class="sxs-lookup"><span data-stu-id="c8465-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="c8465-204">Movimenti clienti</span><span class="sxs-lookup"><span data-stu-id="c8465-204">Customer Entries</span></span>| <span data-ttu-id="c8465-205">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="c8465-205">General Journals</span></span>| <span data-ttu-id="c8465-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="c8465-206">CUSTMIGR</span></span> |
|<span data-ttu-id="c8465-207">Movimenti fornitori</span><span class="sxs-lookup"><span data-stu-id="c8465-207">Vendor Entries</span></span>| <span data-ttu-id="c8465-208">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="c8465-208">General Journals</span></span>| <span data-ttu-id="c8465-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="c8465-209">VENDMIGR</span></span>|
|<span data-ttu-id="c8465-210">Mov. Articoli</span><span class="sxs-lookup"><span data-stu-id="c8465-210">Item Entries</span></span>| <span data-ttu-id="c8465-211">Registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="c8465-211">Item Journals</span></span>| <span data-ttu-id="c8465-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="c8465-212">ITEMMIGR</span></span> |
|<span data-ttu-id="c8465-213">Movimenti C/G</span><span class="sxs-lookup"><span data-stu-id="c8465-213">G/L Entries</span></span>| <span data-ttu-id="c8465-214">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="c8465-214">General Journals</span></span>| <span data-ttu-id="c8465-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="c8465-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="c8465-216">Interruzione della migrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="c8465-216">Stopping Data Migration</span></span>
<span data-ttu-id="c8465-217">È possibile interrompere la migrazione dei dati scegliendo **Interrompi tutte le migrazioni**.</span><span class="sxs-lookup"><span data-stu-id="c8465-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="c8465-218">In tal caso, tutte le migrazioni in sospeso vengono interrotte.</span><span class="sxs-lookup"><span data-stu-id="c8465-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8465-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8465-219">See Also</span></span>
<span data-ttu-id="c8465-220">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c8465-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="c8465-221">Introduzione</span><span class="sxs-lookup"><span data-stu-id="c8465-221">Getting Started</span></span>](product-get-started.md) 

