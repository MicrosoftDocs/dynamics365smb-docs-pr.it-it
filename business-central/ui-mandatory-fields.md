---
title: Campi obbligatori per l'esecuzione dei processi | Documenti Microsoft
description: Informazioni sui campi contrassegnati con un asterisco rosso, che indica che sono obbligatori e devono essere compilati per eseguire i processi.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 8c631dcbb2c6afa6abec9ace86df0f0babb23b2d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385501"
---
# <a name="detecting-mandatory-fields"></a><span data-ttu-id="9e6ae-103">Rilevare campi obbligatori</span><span class="sxs-lookup"><span data-stu-id="9e6ae-103">Detecting Mandatory Fields</span></span>
<span data-ttu-id="9e6ae-104">Immettendo i dati nelle pagine in [!INCLUDE[prod_short](includes/prod_short.md)], alcuni campi sono contrassegnati con un asterisco rosso.</span><span class="sxs-lookup"><span data-stu-id="9e6ae-104">When you enter data on pages in [!INCLUDE[prod_short](includes/prod_short.md)], certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="9e6ae-105">L'asterisco rosso significa che il campo deve essere compilato per completare un determinato processo che utilizza il campo, ad esempio registrare una transazione che utilizza il valore nel campo.</span><span class="sxs-lookup"><span data-stu-id="9e6ae-105">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>

<span data-ttu-id="9e6ae-106">Anche se il campo contiene un asterisco rosso, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="9e6ae-106">Even though the field contains a red asterisk, you are not forced to fill in the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="9e6ae-107">L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.</span><span class="sxs-lookup"><span data-stu-id="9e6ae-107">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>

## <a name="examples"></a><span data-ttu-id="9e6ae-108">Esempi</span><span class="sxs-lookup"><span data-stu-id="9e6ae-108">Examples</span></span>
<span data-ttu-id="9e6ae-109">Nella pagina **Scheda cliente** l'asterisco rosso viene visualizzato nei campi **Nome** e **Cod. area imposte** e nei campi della categoria di registrazione per indicare che non è possibile registrare una transazione di vendita per il cliente senza compilare tali campi.</span><span class="sxs-lookup"><span data-stu-id="9e6ae-109">On the **Customer Card** page, the red asterisk appears in the **Name** field, in the **Tax Area Code** field, and in the posting group fields to indicate that you cannot post a sales transaction for the customer unless the fields are filled.</span></span>

<span data-ttu-id="9e6ae-110">Nella pagina **Scheda articolo**, l'asterisco rosso viene visualizzato nel campo **Descrizione** per indicare che non è possibile immettere l'articolo in una riga di un documento, ad esempio un ordine di vendita, senza compilare questo campo.</span><span class="sxs-lookup"><span data-stu-id="9e6ae-110">On the **Item Card** page, the red asterisk appears in the **Description** field to indicate that you cannot enter the item on a document line, such as a sales order, unless this field is filled.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e6ae-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e6ae-111">See Also</span></span>
<span data-ttu-id="9e6ae-112">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e6ae-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]