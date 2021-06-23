---
title: Utilizzo di modelli Word per comunicazioni in blocco | Microsoft Docs
description: I modelli di Word possono semplificare la creazione di massa di documenti personalizzati per entità specifiche.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110956"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="8d0e6-103">Utilizzo di modelli Word per comunicazioni in blocco</span><span class="sxs-lookup"><span data-stu-id="8d0e6-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="8d0e6-104">I modelli di Microsoft Word possono semplificare le comunicazioni di massa con entità come clienti e fornitori.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="8d0e6-105">Ad esempio, è possibile creare brochure per avvisare i clienti di una campagna di vendita, lettere per informare i fornitori su una nuova politica di acquisto o inviti per attirare contatti a un evento imminente.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

> [!NOTE]
> <span data-ttu-id="8d0e6-106">Puoi utilizzare i modelli di Word solo su dispositivi con Microsoft Word 2019 e il sistema operativo Windows installati.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-106">You can use Word templates only on devices with Microsoft Word 2019 and the Windows operating system installed.</span></span>

<span data-ttu-id="8d0e6-107">Puoi usare entità in [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati per il modello e aggiungi campi unione per personalizzare i documenti per ciascuna entità.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-107">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="8d0e6-108">I campi di unione provengono dall'entità in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8d0e6-108">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8d0e6-109">Quando si applica un modello di Word a un'entità, i dati dei campi unione vengono inseriti nel documento.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-109">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="8d0e6-110">Nella pagina **Modelli di Word** è possibile utilizzare una guida alla configurazione assistita per scaricare un file ZIP contenente un file DataSource.txt e un file modello di Word per un'entità.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-110">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="8d0e6-111">Dopo aver impostato il modello e aggiunto i campi unione, utilizza la stessa guida per caricare il modello.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-111">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="8d0e6-112">Puoi utilizzare solo il modello di Word e i file di origine dati che scarichi da [!INCLUDE[prod_short](includes/prod_short.md)] ed è necessario archiviare i file nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-112">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="8d0e6-113">Quando scegli un'entità per cui creare un modello, l'elenco mostra tutte le entità in formato [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8d0e6-113">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8d0e6-114">Tuttavia, non è possibile creare modelli per tutte le entità.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-114">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="8d0e6-115">Se il nome di un'entità contiene caratteri speciali, come **/**, **.**, **_**, or **-**, non puoi creare un modello per esso.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-115">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="8d0e6-116">Il nome dell'entità è mostrato nella colonna **Didascalia oggetto**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-116">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="8d0e6-117">Quando si imposta il modello in Word, nella scheda **Corrispondenza** puoi aggiungere campi di unione scegliendo **Inserisci Campo Unione**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-117">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="8d0e6-118">Non è possibile utilizzare i campi unione se il nome del campo contiene 40 o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-118">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="8d0e6-119">Ad esempio, non è possibile utilizzare il campo Company__Information_Customs_Permit_Date perché contiene 40 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-119">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="8d0e6-120">Quando il tuo modello di Word è pronto, nella pagina **Modelli di Word** puoi scegliere **Applica** per generare i documenti.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-120">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="8d0e6-121">Puoi creare un documento che contiene sezioni per ogni entità o dividere l'operazione per creare un nuovo documento per ogni entità.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-121">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="8d0e6-122">Per creare un modello di Word</span><span class="sxs-lookup"><span data-stu-id="8d0e6-122">To create a Word template</span></span>
1. <span data-ttu-id="8d0e6-123">Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli di Word** e quindi scegli il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="8d0e6-124">Segui i passaggi nella guida di setup assistito.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-124">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="8d0e6-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8d0e6-125">See Also</span></span>
[<span data-ttu-id="8d0e6-126">Gestione dei layout di report e documenti</span><span class="sxs-lookup"><span data-stu-id="8d0e6-126">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
