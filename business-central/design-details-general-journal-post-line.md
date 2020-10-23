---
title: 'Dettagli di progettazione: riga di registrazione di contabilità generale | Microsoft Docs'
description: Questo argomento fornisce informazioni dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità della riga di registrazione di contabilità generale in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: aaffac8fe7e10d0155649c960803f65a8136c46d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911082"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="f28cc-103">Dettagli di progettazione: riga di registrazione di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="f28cc-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="f28cc-104">Questa documentazione fornisce informazioni tecniche dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità della riga di registrazione di contabilità generale in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f28cc-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f28cc-105">La riprogettazione semplifica e rende più facile la manutenzione di codeunit 12.</span><span class="sxs-lookup"><span data-stu-id="f28cc-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="f28cc-106">Viene innanzitutto illustrata una panoramica dei concetti alla base della riprogettazione.</span><span class="sxs-lookup"><span data-stu-id="f28cc-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="f28cc-107">Viene quindi illustrata l'architettura tecnica per mostrare le modifiche conseguenti alla riprogettazione.</span><span class="sxs-lookup"><span data-stu-id="f28cc-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="f28cc-108">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="f28cc-108">In This Section</span></span>  
[<span data-ttu-id="f28cc-109">Sintesi della riga di registrazione di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="f28cc-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="f28cc-110">Dettagli di progettazione: Struttura dell'interfaccia di registrazione</span><span class="sxs-lookup"><span data-stu-id="f28cc-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="f28cc-111">Dettagli di progettazione: Struttura del motore di registrazione</span><span class="sxs-lookup"><span data-stu-id="f28cc-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="f28cc-112">Modifiche relative alla codeunit 12: variabili globali di mappatura per la riga di registrazione di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="f28cc-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="f28cc-113">Modifiche relative alla codeunit 12: modifiche nelle procedure di registrazione di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="f28cc-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="f28cc-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f28cc-114">See Also</span></span>  
[<span data-ttu-id="f28cc-115">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="f28cc-115">Working with General Journals</span></span>](ui-work-general-journals.md)
