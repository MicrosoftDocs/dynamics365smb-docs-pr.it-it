---
title: Suggerimenti e trucchi - RapidStart Services | Documenti Microsoft
description: "Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e43859a6095f0087c12d0f9c071c0504d3781ad2
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="b1744-103">Suggerimenti e trucchi: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="b1744-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="b1744-104">Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b1744-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="b1744-105">Sfruttare i modelli di configurazione</span><span class="sxs-lookup"><span data-stu-id="b1744-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="b1744-106">I modelli di configurazione consentono di migliorare il processo dell'implementazione rapida.</span><span class="sxs-lookup"><span data-stu-id="b1744-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="b1744-107">Utilizzando tali modelli, è possibile includere clienti simili in segmenti e quindi elaborare un protocollo di implementazione che gestisca tutti i clienti in un segmento in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="b1744-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="b1744-108">In tal modo, è possibile collegare un livello di preconfigurazione a ciascun segmento e procedere a un'implementazione rapida.</span><span class="sxs-lookup"><span data-stu-id="b1744-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="b1744-109">Questionari di configurazione</span><span class="sxs-lookup"><span data-stu-id="b1744-109">Configuration questionnaires</span></span>  
<span data-ttu-id="b1744-110">Per migliorare il processo di compilazione di un questionario di configurazione, valutare di definire risposte di default per indicare le procedure ottimali.</span><span class="sxs-lookup"><span data-stu-id="b1744-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="b1744-111">Creazione batch delle righe di registrazione</span><span class="sxs-lookup"><span data-stu-id="b1744-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="b1744-112">È consigliabile utilizzare gli strumenti di migrazione dati forniti per eseguire la migrazione dei movimenti delle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="b1744-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="b1744-113">In caso contrario, se si utilizza un processo batch per creare le righe delle registrazioni, con un ambito di tempo limitato e vengono generati solo i campi precedenti al default nelle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="b1744-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="b1744-114">Il resto delle registrazioni quindi deve essere completato manualmente.</span><span class="sxs-lookup"><span data-stu-id="b1744-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="b1744-115">Migrazione delle transazioni</span><span class="sxs-lookup"><span data-stu-id="b1744-115">Migrating transactions</span></span>  
<span data-ttu-id="b1744-116">È consigliabile eseguire la migrazione dei bilanci di apertura nel seguente ordine.</span><span class="sxs-lookup"><span data-stu-id="b1744-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="b1744-117">Eseguire la migrazione dei bilanci di apertura di contabilità generale senza utilizzare i registri secondari del conto di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="b1744-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="b1744-118">Utilizzare i conti di compensazione specifici del bilancio di apertura, un setup per ogni registro secondario.</span><span class="sxs-lookup"><span data-stu-id="b1744-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="b1744-119">Impostare i conti di compensazione per abilitare le registrazioni dirette.</span><span class="sxs-lookup"><span data-stu-id="b1744-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="b1744-120">Eseguire la migrazione dei movimenti contabili clienti aperti.</span><span class="sxs-lookup"><span data-stu-id="b1744-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="b1744-121">Eseguire la migrazione dei movimenti contabili articoli aperti.</span><span class="sxs-lookup"><span data-stu-id="b1744-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="b1744-122">Eseguire la migrazione dei movimenti di cespiti aperti.</span><span class="sxs-lookup"><span data-stu-id="b1744-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1744-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1744-123">See Also</span></span>  
[<span data-ttu-id="b1744-124">Impostare una società con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="b1744-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="b1744-125">Amministrazione</span><span class="sxs-lookup"><span data-stu-id="b1744-125">Administration</span></span>](admin-setup-and-administration.md)

