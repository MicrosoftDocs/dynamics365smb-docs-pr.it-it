---
title: 'Procedura: Aggiornare i dati delle transazioni IVA'
description: "Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti eseguendo il report **Aggiorna data transazione IVA**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8f52cc875dda2171d8347fe6aaafa454db43e172
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="update-vat-transactions-data"></a><span data-ttu-id="50b8b-103">Aggiornare i dati delle transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="50b8b-103">Update VAT Transactions Data</span></span>
<span data-ttu-id="50b8b-104">Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti eseguendo il report **Aggiorna data transazione IVA**.</span><span class="sxs-lookup"><span data-stu-id="50b8b-104">Before you create the first VAT transaction report, you should prepare the existing data by running the **Update VAT Transaction Data** report.</span></span> <span data-ttu-id="50b8b-105">È inoltre necessario eseguire questo report se sono state apportate modifiche al setup in base ai nuovi requisiti delle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="50b8b-105">You should also run this report if you have made changes to the setup based on new requirements from the tax authorities.</span></span>  

<span data-ttu-id="50b8b-106">È possibile eseguire il report **Aggiorna data transazione IVA** come test prima di modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-106">You can run the **Update VAT Transaction Data** report as a test before you change any data.</span></span> <span data-ttu-id="50b8b-107">Dopo avere verificato che i filtri soddisfano le previsioni e le richieste delle autorità fiscali, eseguire nuovamente il report per apportare le modifiche appropriate ai dati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-107">When you have verified that the filters meet your expectations and the requirements of the tax authorities, you should run the report again to make the appropriate changes to data.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="50b8b-108">Prima di eseguire il report **Aggiorna data transazione IVA**, è necessario attivare il log delle modifiche nella finestra **Setup log modifiche**.</span><span class="sxs-lookup"><span data-stu-id="50b8b-108">Before you run the **Update VAT Transaction Data** report, you should activate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="50b8b-109">Inoltre, è necessario attivare la registrazione delle modifiche nel campo **Includi in report transazioni IVA** nella tabella **Movimenti IVA**.</span><span class="sxs-lookup"><span data-stu-id="50b8b-109">Also, you should enable logging for modifications to the **Include in VAT Transac. Report** field on the **VAT Entry** table.</span></span>  

## <a name="to-update-vat-transaction-data"></a><span data-ttu-id="50b8b-110">Per aggiornare i dati delle transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="50b8b-110">To update VAT transaction data</span></span>  

1.  <span data-ttu-id="50b8b-111">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Aggiorna data transazione IVA**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="50b8b-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Update VAT Transaction Data**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="50b8b-112">Facoltativamente, nella Scheda dettaglio **Movimenti IVA** impostare i filtri appropriati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-112">Optionally, on the **VAT Entry** FastTab, set the appropriate filters.</span></span>  
3.  <span data-ttu-id="50b8b-113">Nella Scheda dettaglio **Opzioni** compilare i campi come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="50b8b-113">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="50b8b-114">Campo</span><span class="sxs-lookup"><span data-stu-id="50b8b-114">Field</span></span>|<span data-ttu-id="50b8b-115">Description</span><span class="sxs-lookup"><span data-stu-id="50b8b-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="50b8b-116">**Confronta con soglia**</span><span class="sxs-lookup"><span data-stu-id="50b8b-116">**Compare against Threshold**</span></span>|<span data-ttu-id="50b8b-117">Selezionare per confrontare i movimenti IVA rispetto agli importi di soglia specificati nel setup registrazioni IVA.</span><span class="sxs-lookup"><span data-stu-id="50b8b-117">Select to compare VAT entries against the threshold amounts that are specified in the VAT posting setup.</span></span>|  
    |<span data-ttu-id="50b8b-118">**Mostra solo elenco**</span><span class="sxs-lookup"><span data-stu-id="50b8b-118">**Show List Only**</span></span>|<span data-ttu-id="50b8b-119">Selezionare se non si desidera aggiornare i dati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-119">Select if you do not want to update data.</span></span><br /><br /> <span data-ttu-id="50b8b-120">Se si seleziona questo campo, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] stampa un report in modo da poter verificare le modifiche prima che i dati vengano modificati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-120">If you select this field, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] prints a report so that you can verify the changes before data is modified.</span></span> <span data-ttu-id="50b8b-121">Il report contiene una riga per ogni documento in cui l'imponibile IVA sia uguale o maggiore degli importi di soglia.</span><span class="sxs-lookup"><span data-stu-id="50b8b-121">The report contains a line for each document where the VAT base is equal to or greater than the threshold amounts.</span></span> <span data-ttu-id="50b8b-122">**Avviso:** Non selezionare questo campo e il campo **Imposta Includi in report transazioni IVA**.</span><span class="sxs-lookup"><span data-stu-id="50b8b-122">**Warning:**  Do not select both this field and the **Set Include in VAT Transaction Report** field.</span></span>|  
    |<span data-ttu-id="50b8b-123">**Imposta Includi in report transazioni IVA**</span><span class="sxs-lookup"><span data-stu-id="50b8b-123">**Set Include in VAT Transaction Report**</span></span>|<span data-ttu-id="50b8b-124">Selezionare per impostare **Imposta Includi in report transazioni IVA** su **Sì** in tutti i movimenti IVA in cui gli importi soddisfano gli importi di soglia specificati nel setup registrazioni IVA.</span><span class="sxs-lookup"><span data-stu-id="50b8b-124">Select to set the **Include in VAT Trans. Report** to **Yes** on all VAT entries where the amounts meet the threshold amounts that are specified in the VAT posting setup.</span></span> <span data-ttu-id="50b8b-125">**Avviso:** Se si seleziona questo campo, i dati vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-125">**Warning:**  If you select this field, your data is updated.</span></span> <span data-ttu-id="50b8b-126">È consigliabile eseguire il report come test prima di eseguirlo per modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-126">You should run the report as a test before you run it to change data.</span></span>|  

4.  <span data-ttu-id="50b8b-127">Scegliere il pulsante **Stampa** per aggiornare i dati delle transazioni IVA oppure scegliere il pulsante **Anteprima** per visualizzare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="50b8b-127">Choose the **Print** button to update VAT transaction data, or choose the **Preview** button to view the changes.</span></span>  

<span data-ttu-id="50b8b-128">Quando si esegue il report, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] elabora i movimenti IVA in base ai filtri impostati.</span><span class="sxs-lookup"><span data-stu-id="50b8b-128">When you run the report, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] processes VAT entries based on the filters that you set.</span></span> <span data-ttu-id="50b8b-129">Le seguenti regole sono applicabili:</span><span class="sxs-lookup"><span data-stu-id="50b8b-129">The following rules are also applied:</span></span>  

- <span data-ttu-id="50b8b-130">Il campo **In blacklist** per il movimento IVA deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="50b8b-130">The **Blacklisted** field for the VAT entry must be blank.</span></span>  
- <span data-ttu-id="50b8b-131">Il campo **Tipo** del movimento IVA non deve essere **Liquidazione**.</span><span class="sxs-lookup"><span data-stu-id="50b8b-131">The **Type** field for the VAT entry must not be **Settlement**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="50b8b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50b8b-132">See Also</span></span>  
[<span data-ttu-id="50b8b-133">Impostare l'IVA</span><span class="sxs-lookup"><span data-stu-id="50b8b-133">Set Up VAT</span></span>](../../finance-setup-vat.md)  
 <span data-ttu-id="50b8b-134">[Preparare i report di transazioni IVA](how-to-prepare-for-vat-transactions-reports.md) </span><span class="sxs-lookup"><span data-stu-id="50b8b-134">[Prepare for VAT Transactions Reports](how-to-prepare-for-vat-transactions-reports.md) </span></span>  
 [<span data-ttu-id="50b8b-135">IVA italiana</span><span class="sxs-lookup"><span data-stu-id="50b8b-135">Italian VAT</span></span>](italian-vat.md)   

