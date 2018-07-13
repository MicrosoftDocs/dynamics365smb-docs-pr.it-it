---
title: Risoluzione dei problemi di integrazione con Microsoft Flow | Documenti Microsoft
description: Risolvere i problemi per rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato.
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 80bc35f6ea8c4264c2cd8960be3370e5966b88e3
ms.contentlocale: it-it
ms.lasthandoff: 06/01/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="5e635-103">Risoluzione dei problemi di integrazione con Microsoft Flow - Richiesta di URL troppo lungo</span><span class="sxs-lookup"><span data-stu-id="5e635-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="5e635-104">È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="5e635-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="5e635-105">È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.</span><span class="sxs-lookup"><span data-stu-id="5e635-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="5e635-106">Se si sta creando un Microsoft Flow utilizzando il connettore [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile ricevere un messaggio di errore indicante che l'URL richiesto è troppo lungo dopo la creazione del flusso, ad esempio: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="5e635-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="5e635-107">Causa</span><span class="sxs-lookup"><span data-stu-id="5e635-107">Cause</span></span>
<span data-ttu-id="5e635-108">Quando si attiva un flusso viene eseguita la ricerca delle modifiche ai dati.</span><span class="sxs-lookup"><span data-stu-id="5e635-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="5e635-109">Nel determinare se i dati sono stati modificati, i connettori confrontano i dati memorizzati nella cache con i nuovi dati richiesti dall'origine.</span><span class="sxs-lookup"><span data-stu-id="5e635-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="5e635-110">Quando la richiesta dei dati crea un URL troppo lungo l'esito è negativo.</span><span class="sxs-lookup"><span data-stu-id="5e635-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="5e635-111">Le cause comuni possono includere:</span><span class="sxs-lookup"><span data-stu-id="5e635-111">Common causes may include:</span></span>
- <span data-ttu-id="5e635-112">Generalmente, qualsiasi tabella di origine con più di 250 righe</span><span class="sxs-lookup"><span data-stu-id="5e635-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="5e635-113">Tabelle di origine che contengono diverse migliaia di record</span><span class="sxs-lookup"><span data-stu-id="5e635-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="5e635-114">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="5e635-114">Workaround</span></span>
<span data-ttu-id="5e635-115">Utilizzare questa procedura come soluzione alternativa.</span><span class="sxs-lookup"><span data-stu-id="5e635-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="5e635-116">Scegliere di modificare il flusso che ha restituito l'esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5e635-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="5e635-117">Espandere **Mostra opzioni avanzate** nel trigger del flusso.</span><span class="sxs-lookup"><span data-stu-id="5e635-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="5e635-118">Nel campo **Ignora numero** immettere il numero dei record da ignorare.</span><span class="sxs-lookup"><span data-stu-id="5e635-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="5e635-119">Ad esempio, se la tabella utilizzata come origine dati contiene 4.000 record, immettere 4.000 come numero di record da ignorare.</span><span class="sxs-lookup"><span data-stu-id="5e635-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="5e635-120">Aggiornare il flusso.</span><span class="sxs-lookup"><span data-stu-id="5e635-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="5e635-121">Il connettore è attualmente in Beta.</span><span class="sxs-lookup"><span data-stu-id="5e635-121">The connector is currently in Beta.</span></span> <span data-ttu-id="5e635-122">Gli aggiornamenti alla modalità di modifica dei dati vengono inclusi in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="5e635-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="5e635-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e635-123">See Also</span></span>
<span data-ttu-id="5e635-124">[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="5e635-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="5e635-125">Introduzione</span><span class="sxs-lookup"><span data-stu-id="5e635-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="5e635-126">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="5e635-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="5e635-127">[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="5e635-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="5e635-128">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="5e635-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="5e635-129">Finanze</span><span class="sxs-lookup"><span data-stu-id="5e635-129">Finance</span></span>](finance.md)  

