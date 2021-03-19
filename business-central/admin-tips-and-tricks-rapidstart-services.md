---
title: Suggerimenti e consigli - RapidStart Services | Microsoft Docs
description: Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d37c15320724412b757225b506fbee8e588164da
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385626"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="78fd1-103">Suggerimenti e consigli: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="78fd1-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="78fd1-104">Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="78fd1-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="78fd1-105">Sfruttare i modelli di configurazione</span><span class="sxs-lookup"><span data-stu-id="78fd1-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="78fd1-106">I modelli di configurazione consentono di migliorare il processo dell'implementazione rapida.</span><span class="sxs-lookup"><span data-stu-id="78fd1-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="78fd1-107">Utilizzando tali modelli, è possibile includere clienti simili in segmenti e quindi elaborare un protocollo di implementazione che gestisca tutti i clienti in un segmento in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="78fd1-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="78fd1-108">In tal modo, è possibile collegare un livello di preconfigurazione a ciascun segmento e procedere a un'implementazione rapida.</span><span class="sxs-lookup"><span data-stu-id="78fd1-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="78fd1-109">Questionari di configurazione</span><span class="sxs-lookup"><span data-stu-id="78fd1-109">Configuration questionnaires</span></span>

<span data-ttu-id="78fd1-110">Per migliorare il processo di compilazione di un questionario di configurazione, valutare di definire risposte di default per indicare le procedure ottimali.</span><span class="sxs-lookup"><span data-stu-id="78fd1-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="78fd1-111">Creazione batch delle righe di registrazione</span><span class="sxs-lookup"><span data-stu-id="78fd1-111">Batch creation of journal lines</span></span>

<span data-ttu-id="78fd1-112">È consigliabile utilizzare gli strumenti di migrazione dati forniti per eseguire la migrazione dei movimenti delle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="78fd1-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="78fd1-113">In caso contrario, se si utilizza un processo batch per creare le righe delle registrazioni, con un ambito di tempo limitato e vengono generati solo i campi precedenti al default nelle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="78fd1-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="78fd1-114">Il resto delle registrazioni quindi deve essere completato manualmente.</span><span class="sxs-lookup"><span data-stu-id="78fd1-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="78fd1-115">Migrazione delle transazioni</span><span class="sxs-lookup"><span data-stu-id="78fd1-115">Migrating transactions</span></span>

<span data-ttu-id="78fd1-116">È consigliabile eseguire la migrazione dei bilanci di apertura nel seguente ordine.</span><span class="sxs-lookup"><span data-stu-id="78fd1-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="78fd1-117">Eseguire il migrazione dei bilanci di apertura di contabilità generale senza utilizzare i registri secondari del conto di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="78fd1-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="78fd1-118">Utilizzare i conti di compensazione specifici del bilancio di apertura, un setup per ogni registro secondario.</span><span class="sxs-lookup"><span data-stu-id="78fd1-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="78fd1-119">Impostare i conti di compensazione per abilitare le registrazioni dirette.</span><span class="sxs-lookup"><span data-stu-id="78fd1-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="78fd1-120">Eseguire la migrazione dei movimenti contabili clienti aperti.</span><span class="sxs-lookup"><span data-stu-id="78fd1-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="78fd1-121">Eseguire la migrazione dei movimenti contabili articoli aperti.</span><span class="sxs-lookup"><span data-stu-id="78fd1-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="78fd1-122">Eseguire la migrazione i movimenti di cespiti aperti.</span><span class="sxs-lookup"><span data-stu-id="78fd1-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="78fd1-123">Rendere ogni pacchetto gestibile</span><span class="sxs-lookup"><span data-stu-id="78fd1-123">Make each package manageable</span></span>

<span data-ttu-id="78fd1-124">Quando si utilizzano pacchetti di configurazione per migrare i dati, separare i dati in pacchetti separati per una più facile portabilità.</span><span class="sxs-lookup"><span data-stu-id="78fd1-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="78fd1-125">Ad esempio, se si desidera migrare 20 anni di movimenti contabili, l'importazione potrebbe richiedere molte ore e giorni.</span><span class="sxs-lookup"><span data-stu-id="78fd1-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="78fd1-126">Dividere invece i dati in modo che ogni pacchetto diventi più gestibile.</span><span class="sxs-lookup"><span data-stu-id="78fd1-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="78fd1-127">Attualmente, non ci sono regole fisse per ciò che rende performante un pacchetto, ma se si riscontrano problemi durante l'importazione o l'esportazione di un pacchetto, provare a ridurne le dimensioni e vedere se questo aiuta.</span><span class="sxs-lookup"><span data-stu-id="78fd1-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="78fd1-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="78fd1-128">See Also</span></span>

[<span data-ttu-id="78fd1-129">Impostazione di una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="78fd1-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="78fd1-130">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="78fd1-130">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]