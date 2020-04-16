---
title: Creare oggetti XMLport basati su schemi XML | Microsoft Docs
description: Utilizzare gli schemi XML per impostare il framework del servizio di scambio documenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 60b1e7ad420e805e27ad27d8aa7c66fb1274e7b5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188003"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="d73bf-103">Utilizzare gli schemi XML per preparare le definizioni di scambio dati</span><span class="sxs-lookup"><span data-stu-id="d73bf-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="d73bf-104">Per abilitare l'importazione/esportazione di dati in file XML attraverso il framework di scambio dati in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile usare gli schemi XML per definire quali elementi di dati si desidera scambiare con [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d73bf-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d73bf-105">È possibile effettuare questa attività nella pagina **Visualizzatore schema XML** caricando il file di schema XML, selezionando gli elementi dati pertinenti e quindi inizializzando una definizione di scambio dati o un oggetto XMLport.</span><span class="sxs-lookup"><span data-stu-id="d73bf-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="d73bf-106">Dopo avere definito gli elementi dati da includere in base allo schema XML, è possibile utilizzare l'azione **Genera XMLport** per creare l'oggetto XMLport.</span><span class="sxs-lookup"><span data-stu-id="d73bf-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="d73bf-107">In alternativa, è possibile utilizzare l'azione **Genera definizione scambio dati** per inizializzare una definizione di scambio di dati in base agli elementi dati selezionati, che poi può essere completata nella struttura di scambio di dati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="d73bf-108">Viene creato un record nella pagina **Registrazione definizioni di scambio** dove si continua il processo definendo il mapping tra gli elementi del file e i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d73bf-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d73bf-109">Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="d73bf-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="d73bf-110">In questo argomento sono contenute le seguenti procedure:</span><span class="sxs-lookup"><span data-stu-id="d73bf-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="d73bf-111">Per caricare un file di schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="d73bf-112">Per selezionare o rimuovere i nodi in uno schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="d73bf-113">Per generare una definizione di scambio di dati basata su uno schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="d73bf-114">Per generare un oggetto XMLport per il file basato su uno schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="d73bf-115">Per importare un oggetto XMLport in Object Designer</span><span class="sxs-lookup"><span data-stu-id="d73bf-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="d73bf-116">Per caricare un file di schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="d73bf-117">Assicurarsi che il file schema XML pertinente sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="d73bf-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="d73bf-118">L'estensione del file è .xsd.</span><span class="sxs-lookup"><span data-stu-id="d73bf-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="d73bf-119">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="d73bf-120">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-120">Choose the **New** action.</span></span>  

4.  <span data-ttu-id="d73bf-121">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d73bf-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="d73bf-122">Campo</span><span class="sxs-lookup"><span data-stu-id="d73bf-122">Field</span></span>|<span data-ttu-id="d73bf-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d73bf-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d73bf-124">**Codice**</span><span class="sxs-lookup"><span data-stu-id="d73bf-124">**Code**</span></span>|<span data-ttu-id="d73bf-125">Specificare un codice per identificare lo Schema XML.</span><span class="sxs-lookup"><span data-stu-id="d73bf-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="d73bf-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="d73bf-126">**Description**</span></span>|<span data-ttu-id="d73bf-127">Specificare una descrizione dello Schema XML.</span><span class="sxs-lookup"><span data-stu-id="d73bf-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="d73bf-128">Il campo **Spazio dei nomi di destinazione** specifica lo spazio dei nomi nel file schema XML che è stato caricato dalla riga.</span><span class="sxs-lookup"><span data-stu-id="d73bf-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="d73bf-129">Scegliere l'azione **Carica schema**, quindi selezionare il file di schema XML.</span><span class="sxs-lookup"><span data-stu-id="d73bf-129">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="d73bf-130">Quando il file viene caricato, i campi rimanenti nella riga vengono compilati con informazioni provenienti dal file e viene selezionata la casella di controllo **Schema caricato**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d73bf-131">La struttura ad albero dello schema XML caricato è compressa per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d73bf-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="d73bf-132">Ogni nodo può essere espanso scegliendo il pulsante **+** accanto al nodo desiderato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="d73bf-133">Per espandere tutti i nodi, selezionare **Espandi tutto** nella barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d73bf-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="d73bf-134">Per selezionare o rimuovere i nodi in uno schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="d73bf-135">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Visualizzatore schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="d73bf-136">Compilare i campi nell'intestazione come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="d73bf-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="d73bf-137">Campo</span><span class="sxs-lookup"><span data-stu-id="d73bf-137">Field</span></span>|<span data-ttu-id="d73bf-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d73bf-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d73bf-139">**Codice schema XML**</span><span class="sxs-lookup"><span data-stu-id="d73bf-139">**XML Schema Code**</span></span>|<span data-ttu-id="d73bf-140">Specificare il file schema XML che è stato caricato nel passaggio 5 nella sezione "Per caricare un file schema XML".</span><span class="sxs-lookup"><span data-stu-id="d73bf-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="d73bf-141">**Nuovo nr. XMLport**</span><span class="sxs-lookup"><span data-stu-id="d73bf-141">**New XMLport No.**</span></span>|<span data-ttu-id="d73bf-142">Specificare il numero dell'oggetto XMLport che viene creato da questo schema XML quando si sceglie l'azione **Genera XMLport**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="d73bf-143">Le righe sono ora compilate con nodi che rappresentano tutti gli elementi nello Schema XML.</span><span class="sxs-lookup"><span data-stu-id="d73bf-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="d73bf-144">I nodi per gli elementi obbligatori secondo lo Schema XML vengono selezionati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d73bf-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="d73bf-145">Nella prima riga, nella colonna **Nome nodo**, espandere il nodo **Documento**, quindi espandere gradualmente i nodi sottostanti che si desidera esaminare.</span><span class="sxs-lookup"><span data-stu-id="d73bf-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="d73bf-146">In alternativa, fare clic con il pulsante destro del mouse su un nodo, quindi selezionare **Espandi tutto**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="d73bf-147">Scegliere una delle seguenti azioni per modificare quali nodi vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-147">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="d73bf-148">**Azione**</span><span class="sxs-lookup"><span data-stu-id="d73bf-148">**Action**</span></span>|<span data-ttu-id="d73bf-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d73bf-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="d73bf-150">**Mostra tutto**</span><span class="sxs-lookup"><span data-stu-id="d73bf-150">**Show All**</span></span>|<span data-ttu-id="d73bf-151">Tutti i nodi vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="d73bf-152">**Nascondi voci non obbligatorie**</span><span class="sxs-lookup"><span data-stu-id="d73bf-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="d73bf-153">Solo i nodi che rappresentano gli articoli richiesti in base allo schema XML vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="d73bf-154">Questi nodi sono in genere indicati da un **1** nel campo **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="d73bf-155">Selezionare **Mostra tutto** per stornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d73bf-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="d73bf-156">**Nascondi voci non selezionate**</span><span class="sxs-lookup"><span data-stu-id="d73bf-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="d73bf-157">Solo i nodi in cui la casella di controllo **Selezionato** è selezionata vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="d73bf-158">Selezionare **Mostra tutto** per stornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d73bf-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="d73bf-159">Scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-159">Choose the **Edit** action.</span></span>  

6.  <span data-ttu-id="d73bf-160">Con la casella di controllo **Selezionato** specificare per ciascun nodo se si desidera che l'elemento sia supportato nella definizione di scambio dati per il file della banca SEPA correlato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d73bf-161">Quando si seleziona un nodo figlio obbligatorio, vengono selezionati anche tutti i relativi nodi padre.</span><span class="sxs-lookup"><span data-stu-id="d73bf-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="d73bf-162">Selezionare l'azione **Seleziona tutti gli elementi obbligatori** per selezionare nuovamente tutti i nodi che rappresentano gli elementi che sono richiesti in base allo Schema XML.</span><span class="sxs-lookup"><span data-stu-id="d73bf-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="d73bf-163">Selezionare l'azione **Deseleziona tutto** per annullare eventuali selezionare.</span><span class="sxs-lookup"><span data-stu-id="d73bf-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="d73bf-164">Il campo **Scelta** specifica che il nodo dispone di due o più nodi di pari livello che fungono da opzioni.</span><span class="sxs-lookup"><span data-stu-id="d73bf-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="d73bf-165">Per generare una definizione di scambio di dati basata su uno schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="d73bf-166">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="d73bf-167">Selezionare lo schema XML rilevante e quindi scegliere l'azione **Apri visualizzatore schema XML**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-167">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="d73bf-168">Assicurarsi che i nodi pertinenti siano selezionati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="d73bf-169">Per ulteriori informazioni, vedere la sezione "Per selezionare o rimuovere i nodi in uno schema XML".</span><span class="sxs-lookup"><span data-stu-id="d73bf-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="d73bf-170">Nella pagina **Visualizzatore schema XML** scegliere l'azione **Genera definizione scambio dati**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-170">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="d73bf-171">Verrà creata una definizione di scambio dati nella pagina **Registrazione definizioni di scambio** che si potrà completare specificando gli elementi del file da mappare con i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d73bf-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d73bf-172">Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="d73bf-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d73bf-173">È inoltre possibile utilizzare la funzione **Ottieni struttura file** della pagina **Registrazione definizioni di scambio** che utilizza la funzionalità della finestra **Visualizzatore schema XML** per precompilare la Scheda dettaglio **Definizioni colonne**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="d73bf-174">Per generare un oggetto XMLport basato su uno schema XML</span><span class="sxs-lookup"><span data-stu-id="d73bf-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="d73bf-175">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="d73bf-176">Selezionare lo schema XML rilevante e quindi scegliere l'azione **Apri visualizzatore schema XML**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-176">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="d73bf-177">Nel campo **Nuovo nr. XMLport**</span><span class="sxs-lookup"><span data-stu-id="d73bf-177">In the **New XMLport No.**</span></span> <span data-ttu-id="d73bf-178">specificare il numero che il nuovo oggetto XMLport riceverà quando sarà generato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="d73bf-179">Assicurarsi che i nodi pertinenti siano selezionati.</span><span class="sxs-lookup"><span data-stu-id="d73bf-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="d73bf-180">Per ulteriori informazioni, vedere la sezione "Per selezionare o rimuovere i nodi in uno schema XML".</span><span class="sxs-lookup"><span data-stu-id="d73bf-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="d73bf-181">Scegliere l'azione **Genera XMLport**, quindi salvare l'oggetto come file con estensione TXT nel percorso appropriato.</span><span class="sxs-lookup"><span data-stu-id="d73bf-181">Choose the **Generate XMLport** action, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="d73bf-182">Importare il nuovo oggetto XMLport nell'ambiente di sviluppo di [!INCLUDE[d365fin](includes/d365fin_md.md)] e compilarlo.</span><span class="sxs-lookup"><span data-stu-id="d73bf-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="d73bf-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d73bf-183">See Also</span></span>  
<span data-ttu-id="d73bf-184">[Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="d73bf-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="d73bf-185">[Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file) </span><span class="sxs-lookup"><span data-stu-id="d73bf-185">[Export Payments to a Bank File](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file) </span></span>  
<span data-ttu-id="d73bf-186">[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="d73bf-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="d73bf-187">Informazioni sul framework di scambio dati</span><span class="sxs-lookup"><span data-stu-id="d73bf-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)
