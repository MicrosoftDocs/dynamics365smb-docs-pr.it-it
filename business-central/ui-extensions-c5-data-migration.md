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
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5c89d841cdf0e92af4a3dc497cb9c807798e3924
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="4d384-103">Estensione di migrazione dati C5</span><span class="sxs-lookup"><span data-stu-id="4d384-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="4d384-104">Questa estensione consente di migrare facilmente clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4d384-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4d384-105">È inoltre possibile migrare lo storico dei movimenti per i conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4d384-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="4d384-106">La società in [!INCLUDE[d365fin](includes/d365fin_md.md)] non deve contenere alcun dato.</span><span class="sxs-lookup"><span data-stu-id="4d384-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="4d384-107">Inoltre, una volta avviata una migrazione, non creare clienti, fornitori, articoli o conti fino al termine della migrazione.</span><span class="sxs-lookup"><span data-stu-id="4d384-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="4d384-108">Quali dati vengono migrati?</span><span class="sxs-lookup"><span data-stu-id="4d384-108">What Data is Migrated?</span></span>
<span data-ttu-id="4d384-109">I seguenti dati vengono migrati per ogni entità:</span><span class="sxs-lookup"><span data-stu-id="4d384-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="4d384-110">**Clienti**</span><span class="sxs-lookup"><span data-stu-id="4d384-110">**Customers**</span></span>
* <span data-ttu-id="4d384-111">Contatti</span><span class="sxs-lookup"><span data-stu-id="4d384-111">Contacts</span></span>  
* <span data-ttu-id="4d384-112">Località</span><span class="sxs-lookup"><span data-stu-id="4d384-112">Location</span></span>
* <span data-ttu-id="4d384-113">Paese</span><span class="sxs-lookup"><span data-stu-id="4d384-113">Country</span></span>
* <span data-ttu-id="4d384-114">Dimensioni clienti (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="4d384-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="4d384-115">Metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="4d384-115">Shipment method</span></span>
* <span data-ttu-id="4d384-116">Venditore</span><span class="sxs-lookup"><span data-stu-id="4d384-116">Sales Person</span></span>
* <span data-ttu-id="4d384-117">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="4d384-117">Payment terms</span></span>
* <span data-ttu-id="4d384-118">Metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="4d384-118">Payment method</span></span>
* <span data-ttu-id="4d384-119">Gruppo prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="4d384-119">Customer price group</span></span>
* <span data-ttu-id="4d384-120">Sconto fattura cliente</span><span class="sxs-lookup"><span data-stu-id="4d384-120">Customer invoice discount</span></span>

<span data-ttu-id="4d384-121">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="4d384-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="4d384-122">Setup registrazione cliente</span><span class="sxs-lookup"><span data-stu-id="4d384-122">Customer posting setup</span></span>
* <span data-ttu-id="4d384-123">Batch registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d384-123">General journal batch</span></span>
* <span data-ttu-id="4d384-124">Transazioni aperte(movimenti contabili clienti)</span><span class="sxs-lookup"><span data-stu-id="4d384-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="4d384-125">**Fornitori**</span><span class="sxs-lookup"><span data-stu-id="4d384-125">**Vendors**</span></span>
* <span data-ttu-id="4d384-126">Contatti</span><span class="sxs-lookup"><span data-stu-id="4d384-126">Contacts</span></span>
* <span data-ttu-id="4d384-127">Località</span><span class="sxs-lookup"><span data-stu-id="4d384-127">Location</span></span>
* <span data-ttu-id="4d384-128">Paese</span><span class="sxs-lookup"><span data-stu-id="4d384-128">Country</span></span>
* <span data-ttu-id="4d384-129">Dimensioni fornitori (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="4d384-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="4d384-130">Sconto fattura</span><span class="sxs-lookup"><span data-stu-id="4d384-130">Invoice discount</span></span>
* <span data-ttu-id="4d384-131">Metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="4d384-131">Shipment method</span></span>
* <span data-ttu-id="4d384-132">Add. acquisti</span><span class="sxs-lookup"><span data-stu-id="4d384-132">Purchaser</span></span>
* <span data-ttu-id="4d384-133">Condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="4d384-133">Payment terms</span></span>
* <span data-ttu-id="4d384-134">Metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="4d384-134">Payment method</span></span>
* <span data-ttu-id="4d384-135">Sconto fattura fornitore</span><span class="sxs-lookup"><span data-stu-id="4d384-135">Vendor invoice discount</span></span>

<span data-ttu-id="4d384-136">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="4d384-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="4d384-137">Setup registrazione fornitori</span><span class="sxs-lookup"><span data-stu-id="4d384-137">Vendor posting setup</span></span>
* <span data-ttu-id="4d384-138">Batch registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d384-138">General journal batch</span></span>
* <span data-ttu-id="4d384-139">Transazioni aperte(movimenti contabili fornitori)</span><span class="sxs-lookup"><span data-stu-id="4d384-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="4d384-140">**Articoli**</span><span class="sxs-lookup"><span data-stu-id="4d384-140">**Items**</span></span>
* <span data-ttu-id="4d384-141">Località</span><span class="sxs-lookup"><span data-stu-id="4d384-141">Location</span></span>
* <span data-ttu-id="4d384-142">Paese</span><span class="sxs-lookup"><span data-stu-id="4d384-142">Country</span></span>
* <span data-ttu-id="4d384-143">Dimensioni articoli (reparto, centro, scopo)</span><span class="sxs-lookup"><span data-stu-id="4d384-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="4d384-144">Sconti riga vendita</span><span class="sxs-lookup"><span data-stu-id="4d384-144">Sales line discounts</span></span>
* <span data-ttu-id="4d384-145">Categorie sconto clienti</span><span class="sxs-lookup"><span data-stu-id="4d384-145">Customer discount groups</span></span>
* <span data-ttu-id="4d384-146">Gruppi sconto articolo</span><span class="sxs-lookup"><span data-stu-id="4d384-146">Item discount groups</span></span>
* <span data-ttu-id="4d384-147">Prezzo vendita</span><span class="sxs-lookup"><span data-stu-id="4d384-147">Sales price</span></span>
* <span data-ttu-id="4d384-148">Nomenclatura combinata</span><span class="sxs-lookup"><span data-stu-id="4d384-148">Tariff number</span></span>
* <span data-ttu-id="4d384-149">Unità di misura</span><span class="sxs-lookup"><span data-stu-id="4d384-149">Units of measure</span></span>
* <span data-ttu-id="4d384-150">Codice tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="4d384-150">Item tracking code</span></span>
* <span data-ttu-id="4d384-151">Gruppo prezzi cliente</span><span class="sxs-lookup"><span data-stu-id="4d384-151">Customer price group</span></span>
* <span data-ttu-id="4d384-152">DB assemblaggio</span><span class="sxs-lookup"><span data-stu-id="4d384-152">Assembly BOMs</span></span>

<span data-ttu-id="4d384-153">Se si migrano i conti, anche i seguenti dati vengono migrati:</span><span class="sxs-lookup"><span data-stu-id="4d384-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="4d384-154">Setup registrazione magazzino</span><span class="sxs-lookup"><span data-stu-id="4d384-154">Inventory posting setup</span></span>
* <span data-ttu-id="4d384-155">Setup registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d384-155">General posting setup</span></span>
* <span data-ttu-id="4d384-156">Batch registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="4d384-156">Item journal batch</span></span>
* <span data-ttu-id="4d384-157">Transazioni aperte(movimenti contabili articoli)</span><span class="sxs-lookup"><span data-stu-id="4d384-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="4d384-158">Se esistono transazioni aperte che usano valute estere, vengono migrati anche i tassi di cambio per queste valute.</span><span class="sxs-lookup"><span data-stu-id="4d384-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="4d384-159">Altri tassi di cambio non sono migrati.</span><span class="sxs-lookup"><span data-stu-id="4d384-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="4d384-160">**Piano dei conti**</span><span class="sxs-lookup"><span data-stu-id="4d384-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="4d384-161">Dimensioni standard: reparto, scopo e centro di costo</span><span class="sxs-lookup"><span data-stu-id="4d384-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="4d384-162">Transazioni storiche C/G</span><span class="sxs-lookup"><span data-stu-id="4d384-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="4d384-163">Le transazioni storiche C/G vengono trattate in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="4d384-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="4d384-164">Quando si migrano i dati si imposta un parametro **Periodo corrente**.</span><span class="sxs-lookup"><span data-stu-id="4d384-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="4d384-165">Questo parametro consente di elaborare le transazioni C/G.</span><span class="sxs-lookup"><span data-stu-id="4d384-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="4d384-166">Le transazioni dopo questa data vengono migrate singolarmente.</span><span class="sxs-lookup"><span data-stu-id="4d384-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="4d384-167">Le operazioni precedenti alla data vengono aggregate per conto e migrate come importo singolo.</span><span class="sxs-lookup"><span data-stu-id="4d384-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="4d384-168">Ad esempio, sono presenti transazioni nel 2015, 2016, 2017, 2018 e si specifica il 1° gennaio 2017 nel campo Periodo corrente.</span><span class="sxs-lookup"><span data-stu-id="4d384-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="4d384-169">Per ogni conto, gli importi per le transazioni il 31 dicembre 2106 o in data precedente verranno aggregate in un'unica riga del giornale di registrazione generale per ciascun conto C/G.</span><span class="sxs-lookup"><span data-stu-id="4d384-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="4d384-170">Tutte le transazioni dopo questa data verranno migrate singolarmente.</span><span class="sxs-lookup"><span data-stu-id="4d384-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="4d384-171">Per migrare i dati</span><span class="sxs-lookup"><span data-stu-id="4d384-171">To migrate data</span></span>
<span data-ttu-id="4d384-172">Sono necessari solo alcuni passaggi per esportare i dati da C5 e importarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="4d384-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="4d384-173">In C5, utilizzare la funzione **Esporta database** per esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="4d384-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="4d384-174">Quindi, inviare la cartella di esportazione a una cartella compressa (.zip).</span><span class="sxs-lookup"><span data-stu-id="4d384-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="4d384-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Migrazione dati** e quindi scegliere **Migrazione dati**.</span><span class="sxs-lookup"><span data-stu-id="4d384-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="4d384-176">Completare i passaggi nella guida di setup assistito.</span><span class="sxs-lookup"><span data-stu-id="4d384-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="4d384-177">Assicurarsi di scegliere **Importa da Microsoft Dynamcis C5 2012** come origine dati.</span><span class="sxs-lookup"><span data-stu-id="4d384-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="4d384-178">Visualizzazione dello stato della migrazione</span><span class="sxs-lookup"><span data-stu-id="4d384-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="4d384-179">Utilizzare la pagina **Sintesi migrazione dati** per monitorare il successo della migrazione.</span><span class="sxs-lookup"><span data-stu-id="4d384-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="4d384-180">La pagina mostra informazioni quali il numero di entità che la migrazione includerà, lo stato della migrazione e il numero di articoli che sono stati migrati e se la migrazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4d384-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="4d384-181">Mostra inoltre il numero di errori, consente di analizzare gli errori riscontrati e, se possibile, consente di passare facilmente all'entità per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="4d384-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="4d384-182">Per ulteriori informazioni, vedere la sezione successiva in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="4d384-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="4d384-183">Mentre si attendono i risultati della migrazione, è necessario aggiornare la pagina per visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="4d384-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="4d384-184">Come evitare la doppia registrazione</span><span class="sxs-lookup"><span data-stu-id="4d384-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="4d384-185">Per evitare la doppia registrazione in contabilità generale, vengono utilizzati i seguenti conti di contropartita per le transazioni aperte:</span><span class="sxs-lookup"><span data-stu-id="4d384-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="4d384-186">Per i fornitori, si usa il conto v/fornitori della categoria di registrazione fornitori.</span><span class="sxs-lookup"><span data-stu-id="4d384-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="4d384-187">Per i clienti, si usa il conto v/clienti della categoria di registrazione clienti.</span><span class="sxs-lookup"><span data-stu-id="4d384-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="4d384-188">Per gli articoli, si crea una registrazione COGE dove il conto di rettifica è il conto specificato come conto relativo al magazzino nel setup della registrazione magazzino.</span><span class="sxs-lookup"><span data-stu-id="4d384-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="4d384-189">Correzione degli errori</span><span class="sxs-lookup"><span data-stu-id="4d384-189">Correcting Errors</span></span>
<span data-ttu-id="4d384-190">Se si verifica un errore, il campo **Stato** mostrerà **Completato con errori**, quindi il campo **Numero di errori** mostrerà il numero degli errori.</span><span class="sxs-lookup"><span data-stu-id="4d384-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="4d384-191">Per visualizzare un elenco degli errori, è possibile aprire la pagina **Errori di migrazione dati** scegliendo:</span><span class="sxs-lookup"><span data-stu-id="4d384-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="4d384-192">Il numero nel campo **Numero di errori** per l'entità.</span><span class="sxs-lookup"><span data-stu-id="4d384-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="4d384-193">L'entità, quindi l'azione **Mostra errori**.</span><span class="sxs-lookup"><span data-stu-id="4d384-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="4d384-194">Nella pagina **Errori di migrazione dati**, per correggere un errore è possibile scegliere un messaggio di errore e **Modifica record** per visualizzare i dati migrati per l'entità.</span><span class="sxs-lookup"><span data-stu-id="4d384-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="4d384-195">Se sono presenti più errori da correggere, è possibile scegliere **Correzione in blocco errori** per modificare le entità in un elenco.</span><span class="sxs-lookup"><span data-stu-id="4d384-195">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="4d384-196">È comunque necessario aprire i singoli record se l'errore è stato causato da una voce correlata.</span><span class="sxs-lookup"><span data-stu-id="4d384-196">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="4d384-197">Ad esempio, un fornitore non verrà migrato se un indirizzo e-mail di uno dei suoi contatti ha un formato non valido.</span><span class="sxs-lookup"><span data-stu-id="4d384-197">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="4d384-198">Dopo aver corretto uno o più errori, è possibile scegliere **Esegui migrazione** per migrare solo le entità corrette, senza dover riavviare completamente la migrazione.</span><span class="sxs-lookup"><span data-stu-id="4d384-198">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="4d384-199">Se è stato corretto più di un errore, è possibile utilizzare la funzionalità **Seleziona più elementi** per selezionare più righe da migrare.</span><span class="sxs-lookup"><span data-stu-id="4d384-199">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="4d384-200">In alternativa, se esistono errori che non è importante correggere, è possibile selezionarli, quindi scegliere **Ignora selezione**.</span><span class="sxs-lookup"><span data-stu-id="4d384-200">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="4d384-201">Se si dispone di articoli che sono inclusi in una distinta base, potrebbe essere necessario effettuare la migrazione più di una volta se l'articolo originale non viene creato prima delle varianti a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="4d384-201">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="4d384-202">Se una variante articolo viene creata per prima, il riferimento all'articolo originale può causare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="4d384-202">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="4d384-203">Verifica dei dati dopo la migrazione</span><span class="sxs-lookup"><span data-stu-id="4d384-203">Verifying Data After Migrating</span></span>
<span data-ttu-id="4d384-204">Un modo per verificare che i dati siano stati migrati correttamente consiste nell'esaminare le seguenti pagine in C5 e [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4d384-204">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="4d384-205">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="4d384-205">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="4d384-206">Processo batch da usare</span><span class="sxs-lookup"><span data-stu-id="4d384-206">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="4d384-207">Movimenti clienti</span><span class="sxs-lookup"><span data-stu-id="4d384-207">Customer Entries</span></span>| <span data-ttu-id="4d384-208">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d384-208">General Journals</span></span>| <span data-ttu-id="4d384-209">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="4d384-209">CUSTMIGR</span></span> |
|<span data-ttu-id="4d384-210">Movimenti fornitori</span><span class="sxs-lookup"><span data-stu-id="4d384-210">Vendor Entries</span></span>| <span data-ttu-id="4d384-211">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d384-211">General Journals</span></span>| <span data-ttu-id="4d384-212">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="4d384-212">VENDMIGR</span></span>|
|<span data-ttu-id="4d384-213">Mov. Articoli</span><span class="sxs-lookup"><span data-stu-id="4d384-213">Item Entries</span></span>| <span data-ttu-id="4d384-214">Registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="4d384-214">Item Journals</span></span>| <span data-ttu-id="4d384-215">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="4d384-215">ITEMMIGR</span></span> |
|<span data-ttu-id="4d384-216">Movimenti C/G</span><span class="sxs-lookup"><span data-stu-id="4d384-216">G/L Entries</span></span>| <span data-ttu-id="4d384-217">Registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d384-217">General Journals</span></span>| <span data-ttu-id="4d384-218">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="4d384-218">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="4d384-219">Interruzione della migrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="4d384-219">Stopping Data Migration</span></span>
<span data-ttu-id="4d384-220">È possibile interrompere la migrazione dei dati scegliendo **Interrompi tutte le migrazioni**.</span><span class="sxs-lookup"><span data-stu-id="4d384-220">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="4d384-221">In tal caso, tutte le migrazioni in sospeso vengono interrotte.</span><span class="sxs-lookup"><span data-stu-id="4d384-221">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d384-222">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d384-222">See Also</span></span>
<span data-ttu-id="4d384-223">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4d384-223">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="4d384-224">Introduzione</span><span class="sxs-lookup"><span data-stu-id="4d384-224">Getting Started</span></span>](product-get-started.md)

