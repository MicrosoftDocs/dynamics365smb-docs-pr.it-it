---
title: Selezione report in Business Central
description: Informazioni su come impostare i report utilizzati per stampare vari tipi di documenti in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: 9d282ea35f7b4bdf317e818504f061d4145404bd
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379000"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="32437-103">Selezione report in Business Central</span><span class="sxs-lookup"><span data-stu-id="32437-103">Report Selection in Business Central</span></span>

<span data-ttu-id="32437-104">È possibile impostare report predefiniti che saranno utilizzati diversi documenti acquisto e vendite (ordini, offerte, fatture, note di credito e così via).</span><span class="sxs-lookup"><span data-stu-id="32437-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="32437-105">Ad esempio, se si dispone di un layout specifico per le fatture vendita, è possibile specificare tale report nella pagina **Selezioni report - Vendite** di modo che venga utilizzato per inviare o stampare fatture vendita.</span><span class="sxs-lookup"><span data-stu-id="32437-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="32437-106">Le pagine **Selezioni report** specificano quale report verrà stampato nelle diverse situazioni.</span><span class="sxs-lookup"><span data-stu-id="32437-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="32437-107">[!INCLUDE [prod_short](includes/prod_short.md)] include configurazioni predefinite, ma ovviamente puoi modificare queste impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="32437-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="32437-108">È inoltre possibile aggiungere report alle pagine **Selezione report**, ad esempio per stampare più di un report per tipo di documento.</span><span class="sxs-lookup"><span data-stu-id="32437-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="32437-109">Selezioni report disponibili</span><span class="sxs-lookup"><span data-stu-id="32437-109">Available report selections</span></span>

<span data-ttu-id="32437-110">[!INCLUDE [prod_short](includes/prod_short.md)] include pagine **Selezione report** differenti per aree diverse.</span><span class="sxs-lookup"><span data-stu-id="32437-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="32437-111">Le tabelle seguenti descrivono dove è possibile trovare informazioni sulle diverse pagine.</span><span class="sxs-lookup"><span data-stu-id="32437-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="32437-112">Area o attività</span><span class="sxs-lookup"><span data-stu-id="32437-112">Area or task</span></span>  |<span data-ttu-id="32437-113">Ulteriori informazioni</span><span class="sxs-lookup"><span data-stu-id="32437-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="32437-114">Esempio di funzionamento della selezione report (vendite)</span><span class="sxs-lookup"><span data-stu-id="32437-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="32437-115">Selezione report per documenti di vendita</span><span class="sxs-lookup"><span data-stu-id="32437-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="32437-116">Layout predefinito per e-mail con documenti vendita e acquisto</span><span class="sxs-lookup"><span data-stu-id="32437-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="32437-117">Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto</span><span class="sxs-lookup"><span data-stu-id="32437-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="32437-118">Definire layout di assegni</span><span class="sxs-lookup"><span data-stu-id="32437-118">Define check layouts</span></span>     |[<span data-ttu-id="32437-119">Selezionare un layout degli assegni</span><span class="sxs-lookup"><span data-stu-id="32437-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="32437-120">Definire report per report IVA (Germania)</span><span class="sxs-lookup"><span data-stu-id="32437-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="32437-121">Impostare report per l'IVA e l'Intrastat</span><span class="sxs-lookup"><span data-stu-id="32437-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="32437-122">[!INCLUDE [prod_short](includes/prod_short.md)] può includere ulteriori pagine **Selezione report**, a seconda della posizione e del settore, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="32437-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="32437-123">Puoi sempre controllare la configurazione scegliendo l'icona a forma di ![Lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettendo **Selezioni report**, quindi scegli il collegamento pertinente.</span><span class="sxs-lookup"><span data-stu-id="32437-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="32437-124">La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] include le pagine **Sezione report** seguenti:</span><span class="sxs-lookup"><span data-stu-id="32437-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="32437-125">**Selezione report - Vendite**</span><span class="sxs-lookup"><span data-stu-id="32437-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="32437-126">**Selezione report - Acquisto**</span><span class="sxs-lookup"><span data-stu-id="32437-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="32437-127">**Selezione report - Magazzino**</span><span class="sxs-lookup"><span data-stu-id="32437-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="32437-128">**Selezione report - Flusso di cassa**</span><span class="sxs-lookup"><span data-stu-id="32437-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="32437-129">**Selezione report - Warehouse**</span><span class="sxs-lookup"><span data-stu-id="32437-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="32437-130">**Selezione report - Conto bancario**</span><span class="sxs-lookup"><span data-stu-id="32437-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="32437-131">**Selezioni report - Sollecito/Addebito interessi**</span><span class="sxs-lookup"><span data-stu-id="32437-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="32437-132">Esempio: Selezione report per documenti vendita</span><span class="sxs-lookup"><span data-stu-id="32437-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="32437-133">La pagina **Selezione report - Vendite** definisce i report predefiniti da utilizzare in diversi scenari per ogni tipo di documento correlato.</span><span class="sxs-lookup"><span data-stu-id="32437-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="32437-134">Scegli un tipo di documento nel campo **Utilizzo**, quindi aggiungi o esamina la selezione report.</span><span class="sxs-lookup"><span data-stu-id="32437-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="32437-135">Puoi impostare più di un report e l'ordine di sequenza in cui i rapporti devono essere inviati o stampati.</span><span class="sxs-lookup"><span data-stu-id="32437-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="32437-136">Alcuni tipi di documento possono essere inviati come allegati di posta elettronica e altri no.</span><span class="sxs-lookup"><span data-stu-id="32437-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="32437-137">Ogni pagina **Selezione report** mostra altri campi se il tipo supporta la posta elettronica per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32437-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="32437-138">Ad esempio, nelle pagine **Selezione report - Vendite** e **Selezione report - Acquisto**, i seguenti campi consentono di configurare la posta elettronica:</span><span class="sxs-lookup"><span data-stu-id="32437-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="32437-139">Nome campo</span><span class="sxs-lookup"><span data-stu-id="32437-139">Field name</span></span> |<span data-ttu-id="32437-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32437-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="32437-141">**Utilizza per corpo e-mail**</span><span class="sxs-lookup"><span data-stu-id="32437-141">**Use for Email Body**</span></span>| <span data-ttu-id="32437-142">Specifica le informazioni riepilogative, come il numero di fattura, la data di scadenza e il collegamento del servizio di pagamento, che verranno aggiunte al testo del messaggio e-mail inviato.</span><span class="sxs-lookup"><span data-stu-id="32437-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="32437-143">**Utilizza per allegato e-mail**</span><span class="sxs-lookup"><span data-stu-id="32437-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="32437-144">Specifica che il documento correlato verrà allegato al messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="32437-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="32437-145">**Descrizione layout corpo e-mail**</span><span class="sxs-lookup"><span data-stu-id="32437-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="32437-146">Specifica il layout del corpo del messaggio di posta elettronica utilizzato, in genere un layout di report personalizzato.</span><span class="sxs-lookup"><span data-stu-id="32437-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="32437-147">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="32437-147">See also</span></span>

[<span data-ttu-id="32437-148">Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto</span><span class="sxs-lookup"><span data-stu-id="32437-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="32437-149">Selezionare un layout degli assegni</span><span class="sxs-lookup"><span data-stu-id="32437-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="32437-150">Impostare report per l'IVA e l'Intrastat (Germania)</span><span class="sxs-lookup"><span data-stu-id="32437-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="32437-151">Gestione dei layout di report e documenti</span><span class="sxs-lookup"><span data-stu-id="32437-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="32437-152">Definire layout di documenti per clienti e fornitori</span><span class="sxs-lookup"><span data-stu-id="32437-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="32437-153">Configurare le stampanti</span><span class="sxs-lookup"><span data-stu-id="32437-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]