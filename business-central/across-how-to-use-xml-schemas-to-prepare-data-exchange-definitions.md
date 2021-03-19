---
title: Utilizzare gli schemi XML per preparare le definizioni di scambio dati
description: Utilizzare gli schemi XML per impostare il framework del servizio di scambio documenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 25073b552644c9ca013a2eae90a0d013ab57e556
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379425"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="dbaed-103">Utilizzare gli schemi XML per preparare le definizioni di scambio dati</span><span class="sxs-lookup"><span data-stu-id="dbaed-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="dbaed-104">Per abilitare l'importazione/esportazione di dati in file XML attraverso il framework di scambio dati in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile usare gli schemi XML per definire quali elementi di dati si desidera scambiare con [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dbaed-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="dbaed-105">È possibile effettuare questa attività nella pagina **Visualizzatore schema XML** caricando il file di schema XML, selezionando gli elementi dati pertinenti e quindi inizializzando una definizione di scambio dati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="dbaed-106">Dopo avere definito gli elementi dati da includere in base allo schema XML, è possibile utilizzare l'azione **Genera definizione scambio dati** per inizializzare una definizione di scambio di dati in base agli elementi dati selezionati, che poi può essere completata nella struttura di scambio di dati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="dbaed-107">Viene creato un record nella pagina **Registrazione definizioni di scambio** dove si continua il processo definendo il mapping tra gli elementi del file e i campi in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dbaed-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="dbaed-108">Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="dbaed-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="dbaed-109">In questo argomento sono contenute le seguenti procedure:</span><span class="sxs-lookup"><span data-stu-id="dbaed-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="dbaed-110">Per caricare un file di schema XML</span><span class="sxs-lookup"><span data-stu-id="dbaed-110">To load an XML schema file</span></span>  

- <span data-ttu-id="dbaed-111">Per selezionare o rimuovere i nodi in uno schema XML</span><span class="sxs-lookup"><span data-stu-id="dbaed-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="dbaed-112">Per generare una definizione di scambio di dati basata su uno schema XML</span><span class="sxs-lookup"><span data-stu-id="dbaed-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="dbaed-113">Per caricare un file di schema XML</span><span class="sxs-lookup"><span data-stu-id="dbaed-113">To load an XML schema file</span></span>

1. <span data-ttu-id="dbaed-114">Assicurarsi che il file schema XML pertinente sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="dbaed-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="dbaed-115">L'estensione del file è .xsd.</span><span class="sxs-lookup"><span data-stu-id="dbaed-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="dbaed-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="dbaed-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="dbaed-117">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="dbaed-118">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dbaed-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="dbaed-119">Campo</span><span class="sxs-lookup"><span data-stu-id="dbaed-119">Field</span></span>|<span data-ttu-id="dbaed-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbaed-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="dbaed-121">**Codice**</span><span class="sxs-lookup"><span data-stu-id="dbaed-121">**Code**</span></span>|<span data-ttu-id="dbaed-122">Specificare un codice per identificare lo Schema XML.</span><span class="sxs-lookup"><span data-stu-id="dbaed-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="dbaed-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="dbaed-123">**Description**</span></span>|<span data-ttu-id="dbaed-124">Specificare una descrizione dello Schema XML.</span><span class="sxs-lookup"><span data-stu-id="dbaed-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="dbaed-125">Il campo **Spazio dei nomi di destinazione** specifica lo spazio dei nomi nel file schema XML che è stato caricato dalla riga.</span><span class="sxs-lookup"><span data-stu-id="dbaed-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="dbaed-126">Scegliere l'azione **Carica schema**, quindi selezionare il file di schema XML.</span><span class="sxs-lookup"><span data-stu-id="dbaed-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="dbaed-127">Quando il file viene caricato, i campi rimanenti nella riga vengono compilati con informazioni provenienti dal file e viene selezionata la casella di controllo **Schema caricato**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="dbaed-128">La struttura ad albero dello schema XML caricato è compressa per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dbaed-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="dbaed-129">Ogni nodo può essere espanso scegliendo il pulsante **+** accanto al nodo desiderato.</span><span class="sxs-lookup"><span data-stu-id="dbaed-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="dbaed-130">Per espandere tutti i nodi, selezionare **Espandi tutto** nella barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="dbaed-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="dbaed-131">Per selezionare o rimuovere i nodi in uno schema XML</span><span class="sxs-lookup"><span data-stu-id="dbaed-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="dbaed-132">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Visualizzatore schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="dbaed-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="dbaed-133">Compilare i campi nell'intestazione come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="dbaed-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="dbaed-134">Campo</span><span class="sxs-lookup"><span data-stu-id="dbaed-134">Field</span></span>|<span data-ttu-id="dbaed-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbaed-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="dbaed-136">**Codice schema XML**</span><span class="sxs-lookup"><span data-stu-id="dbaed-136">**XML Schema Code**</span></span>|<span data-ttu-id="dbaed-137">Specificare il file schema XML che è stato caricato nel passaggio 5 nella sezione "Per caricare un file schema XML".</span><span class="sxs-lookup"><span data-stu-id="dbaed-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="dbaed-138">**Nuovo nr. XMLport**</span><span class="sxs-lookup"><span data-stu-id="dbaed-138">**New XMLport No.**</span></span>|<span data-ttu-id="dbaed-139">Specificare il numero dell'oggetto XMLport che viene creato da questo schema XML quando si sceglie l'azione **Genera XMLport**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="dbaed-140">Le righe sono ora compilate con nodi che rappresentano tutti gli elementi nello Schema XML.</span><span class="sxs-lookup"><span data-stu-id="dbaed-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="dbaed-141">I nodi per gli elementi obbligatori secondo lo Schema XML vengono selezionati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dbaed-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="dbaed-142">Nella prima riga, nella colonna **Nome nodo**, espandere il nodo **Documento**, quindi espandere gradualmente i nodi sottostanti che si desidera esaminare.</span><span class="sxs-lookup"><span data-stu-id="dbaed-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="dbaed-143">In alternativa, fare clic con il pulsante destro del mouse su un nodo, quindi selezionare **Espandi tutto**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="dbaed-144">Scegliere una delle seguenti azioni per modificare quali nodi vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="dbaed-145">**Azione**</span><span class="sxs-lookup"><span data-stu-id="dbaed-145">**Action**</span></span>|<span data-ttu-id="dbaed-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbaed-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="dbaed-147">**Mostra tutto**</span><span class="sxs-lookup"><span data-stu-id="dbaed-147">**Show All**</span></span>|<span data-ttu-id="dbaed-148">Tutti i nodi vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="dbaed-149">**Nascondi voci non obbligatorie**</span><span class="sxs-lookup"><span data-stu-id="dbaed-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="dbaed-150">Solo i nodi che rappresentano gli articoli richiesti in base allo schema XML vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="dbaed-151">Questi nodi sono in genere indicati da un **1** nel campo **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="dbaed-152">Selezionare **Mostra tutto** per stornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dbaed-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="dbaed-153">**Nascondi voci non selezionate**</span><span class="sxs-lookup"><span data-stu-id="dbaed-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="dbaed-154">Solo i nodi in cui la casella di controllo **Selezionato** è selezionata vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="dbaed-155">Selezionare **Mostra tutto** per stornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dbaed-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="dbaed-156">Scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="dbaed-157">Con la casella di controllo **Selezionato** specificare per ciascun nodo se si desidera che l'elemento sia supportato nella definizione di scambio dati per il file della banca SEPA correlato.</span><span class="sxs-lookup"><span data-stu-id="dbaed-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="dbaed-158">Quando si seleziona un nodo figlio obbligatorio, vengono selezionati anche tutti i relativi nodi padre.</span><span class="sxs-lookup"><span data-stu-id="dbaed-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="dbaed-159">Selezionare l'azione **Seleziona tutti gli elementi obbligatori** per selezionare nuovamente tutti i nodi che rappresentano gli elementi che sono richiesti in base allo Schema XML.</span><span class="sxs-lookup"><span data-stu-id="dbaed-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="dbaed-160">Selezionare l'azione **Deseleziona tutto** per annullare eventuali selezionare.</span><span class="sxs-lookup"><span data-stu-id="dbaed-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="dbaed-161">Il campo **Scelta** specifica che il nodo dispone di due o più nodi di pari livello che fungono da opzioni.</span><span class="sxs-lookup"><span data-stu-id="dbaed-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="dbaed-162">Per generare una definizione di scambio di dati basata su uno schema XML</span><span class="sxs-lookup"><span data-stu-id="dbaed-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="dbaed-163">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="dbaed-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="dbaed-164">Selezionare lo schema XML rilevante e quindi scegliere l'azione **Apri visualizzatore schema XML**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="dbaed-165">Assicurarsi che i nodi pertinenti siano selezionati.</span><span class="sxs-lookup"><span data-stu-id="dbaed-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="dbaed-166">Per ulteriori informazioni, vedere la sezione "Per selezionare o rimuovere i nodi in uno schema XML".</span><span class="sxs-lookup"><span data-stu-id="dbaed-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="dbaed-167">Nella pagina **Visualizzatore schema XML** scegliere l'azione **Genera definizione scambio dati**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="dbaed-168">Verrà creata una definizione di scambio dati nella pagina **Registrazione definizioni di scambio** che si potrà completare specificando gli elementi del file da mappare con i campi in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dbaed-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="dbaed-169">Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="dbaed-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="dbaed-170">È inoltre possibile utilizzare la funzione **Ottieni struttura file** della pagina **Registrazione definizioni di scambio** che utilizza la funzionalità della finestra **Visualizzatore schema XML** per precompilare la Scheda dettaglio **Definizioni colonne**.</span><span class="sxs-lookup"><span data-stu-id="dbaed-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="dbaed-171">Nella prima ondata di rilascio del 2019 e nelle versioni precedenti, è possibile generare un XMLport basato sullo schema e poi importalo nella soluzione.</span><span class="sxs-lookup"><span data-stu-id="dbaed-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="dbaed-172">Questa funzionalità non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="dbaed-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbaed-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dbaed-173">See Also</span></span>

[<span data-ttu-id="dbaed-174">Impostare le definizioni di scambio dati</span><span class="sxs-lookup"><span data-stu-id="dbaed-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="dbaed-175">Esportare pagamenti in un file della banca</span><span class="sxs-lookup"><span data-stu-id="dbaed-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="dbaed-176">Riscuotere pagamenti con addebito diretto SEPA</span><span class="sxs-lookup"><span data-stu-id="dbaed-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="dbaed-177">Informazioni sul framework di scambio dati</span><span class="sxs-lookup"><span data-stu-id="dbaed-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]