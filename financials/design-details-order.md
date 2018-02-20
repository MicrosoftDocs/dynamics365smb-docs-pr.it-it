---
title: 'Dettagli di progettazione: Ordine | Microsoft Docs'
description: Questo argomento fornisce informazioni a collegamenti ordine-a-ordine in un ambiente di produzione su ordine.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 24f5c56e9e148128d83593757d820fa62686403e
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-order"></a><span data-ttu-id="f5acf-103">Dettagli di progettazione: Ordine</span><span class="sxs-lookup"><span data-stu-id="f5acf-103">Design Details: Order</span></span>
<span data-ttu-id="f5acf-104">In un ambiente di produzione su ordine, un articolo viene acquistato o prodotto esclusivamente per coprire una domanda specifica.</span><span class="sxs-lookup"><span data-stu-id="f5acf-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="f5acf-105">In genere si riferisce ad articoli A e le motivazioni per scegliere il metodo di riordino Ordine può essere quello di una domanda poco frequente, un lead time insignificante o la variazione degli attributi necessari.</span><span class="sxs-lookup"><span data-stu-id="f5acf-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  
  
<span data-ttu-id="f5acf-106">Il programma crea un collegamento ordine su ordine, che funge da connessione preliminare tra l'approvvigionamento, un ordine di approvvigionamento o il magazzino e la domanda che deve soddisfare.</span><span class="sxs-lookup"><span data-stu-id="f5acf-106">The program creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  
  
<span data-ttu-id="f5acf-107">Oltre all'utilizzo del metodo Ordine, il collegamento ordine-a-ordine può essere applicato durante la pianificazione nei seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="f5acf-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  
  
* <span data-ttu-id="f5acf-108">Se si utilizza la politica di produzione Produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti necessari nello stesso ordine di produzione).</span><span class="sxs-lookup"><span data-stu-id="f5acf-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="f5acf-109">Se si utilizza la funzionalità Pianifica ordine vendita per creare un ordine di produzione da un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="f5acf-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  
  
<span data-ttu-id="f5acf-110">Anche se un'azienda manifatturiera si considera come ambiente di produzione su ordine, potrebbe essere meglio utilizzare un metodo di riordino lotto-per-lotto se gli articoli sono standard puro senza variazione negli attributi.</span><span class="sxs-lookup"><span data-stu-id="f5acf-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="f5acf-111">Di conseguenza, verrà utilizzato il magazzino non pianificato e si accumuleranno solo ordini di vendita con la stessa data di spedizione o all'interno di un intervallo di tempo definito.</span><span class="sxs-lookup"><span data-stu-id="f5acf-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  
  
## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="f5acf-112">Collegamenti ordine su ordine e date di scadenza arretrate</span><span class="sxs-lookup"><span data-stu-id="f5acf-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="f5acf-113">A differenza della maggior parte dei set di approvvigionamento-domanda, gli ordini collegati con date di scadenza precedenti alla data di inizio della pianificazione sono completamente pianificati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f5acf-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="f5acf-114">Il motivo economico di questa eccezione è che la domanda e l'approvvigionamento specifici devono essere sincronizzati attraverso l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f5acf-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="f5acf-115">Per ulteriori informazioni sulla zona bloccata che si applica alla maggior parte dei tipi di domanda-approvvigionamento, vedere [Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="f5acf-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5acf-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5acf-116">See Also</span></span>  
<span data-ttu-id="f5acf-117">[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="f5acf-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="f5acf-118">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="f5acf-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="f5acf-119">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="f5acf-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="f5acf-120">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="f5acf-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
