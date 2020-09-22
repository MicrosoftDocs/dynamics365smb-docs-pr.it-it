---
title: Aggiungere righe ulteriori per definire descrizioni estese
description: È possibile aggiungere righe supplementari per estendere il testo standard che descrive un articolo, un conto C/G e altri dati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782320"
---
# <a name="add-extended-text"></a><span data-ttu-id="bca55-103">Aggiungere testo esteso</span><span class="sxs-lookup"><span data-stu-id="bca55-103">Add Extended Text</span></span>

<span data-ttu-id="bca55-104">È possibile estendere la descrizione di articoli, unità di stockkeeping, conti di contabilità generale e risorse aggiungendo righe extra come testo esteso.</span><span class="sxs-lookup"><span data-stu-id="bca55-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="bca55-105">È inoltre possibile impostare le condizioni per l'uso delle righe extra.</span><span class="sxs-lookup"><span data-stu-id="bca55-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="bca55-106">La sezione seguente descrive come aggiungere testo esteso a una descrizione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="bca55-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="bca55-107">Gli stessi passaggi si applicano alle unità di stockkeeping, ai conti di contabilità generale e alle risorse.</span><span class="sxs-lookup"><span data-stu-id="bca55-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="bca55-108">Per definire il testo esteso per una descrizione</span><span class="sxs-lookup"><span data-stu-id="bca55-108">To define extended text for an description</span></span>

1. <span data-ttu-id="bca55-109">Aprire la scheda di un articolo al quale si desidera aggiungere il testo esteso, quindi scegliere l'azione **Testo esteso**.</span><span class="sxs-lookup"><span data-stu-id="bca55-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="bca55-110">Compilare i campi **Codice** e **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="bca55-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="bca55-111">Scegliere **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="bca55-111">Choose the **New**.</span></span>
4. <span data-ttu-id="bca55-112">Compilare il campo **Cod. lingua** o selezionare la casella di controllo **Tutti cod. lingua** se si utilizzano i codici lingua.</span><span class="sxs-lookup"><span data-stu-id="bca55-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="bca55-113">Compilare i campi **Data inizio** e **Data fine** se si desidera limitare il periodo in cui il testo esteso verrà utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bca55-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="bca55-114">Nel campo **Testo** immettere il testo esteso.</span><span class="sxs-lookup"><span data-stu-id="bca55-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="bca55-115">Selezionare le relative caselle di controllo per i tipi di documento su cui si desidera stampare il testo esteso.</span><span class="sxs-lookup"><span data-stu-id="bca55-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="bca55-116">Chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="bca55-116">Close the page.</span></span>

<span data-ttu-id="bca55-117">È ora possibile aggiungere questo testo esteso ai documenti.</span><span class="sxs-lookup"><span data-stu-id="bca55-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="bca55-118">La seguente procedura spiega come aggiungere testo esteso a un ordine cliente, ma gli stessi passaggi si applicano a qualsiasi altro documento specificato per il testo esteso.</span><span class="sxs-lookup"><span data-stu-id="bca55-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="bca55-119">Per aggiungere testo esteso di articoli in una riga di un ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="bca55-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="bca55-120">Aprire un ordine di vendita con una riga di vendita per un articolo che ha testo esteso definito.</span><span class="sxs-lookup"><span data-stu-id="bca55-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="bca55-121">Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="bca55-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="bca55-122">Selezionare la riga in questione e scegliere l'azione **Inserisci testo esteso**.</span><span class="sxs-lookup"><span data-stu-id="bca55-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="bca55-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bca55-123">See Also</span></span>

[<span data-ttu-id="bca55-124">Impostazione del magazzino</span><span class="sxs-lookup"><span data-stu-id="bca55-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="bca55-125">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bca55-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
