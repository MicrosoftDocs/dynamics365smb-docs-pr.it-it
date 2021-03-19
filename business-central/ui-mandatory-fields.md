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
# <a name="detecting-mandatory-fields"></a>Rilevare campi obbligatori
Immettendo i dati nelle pagine in [!INCLUDE[prod_short](includes/prod_short.md)], alcuni campi sono contrassegnati con un asterisco rosso. L'asterisco rosso significa che il campo deve essere compilato per completare un determinato processo che utilizza il campo, ad esempio registrare una transazione che utilizza il valore nel campo.

Anche se il campo contiene un asterisco rosso, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina. L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.

## <a name="examples"></a>Esempi
Nella pagina **Scheda cliente** l'asterisco rosso viene visualizzato nei campi **Nome** e **Cod. area imposte** e nei campi della categoria di registrazione per indicare che non è possibile registrare una transazione di vendita per il cliente senza compilare tali campi.

Nella pagina **Scheda articolo**, l'asterisco rosso viene visualizzato nel campo **Descrizione** per indicare che non è possibile immettere l'articolo in una riga di un documento, ad esempio un ordine di vendita, senza compilare questo campo.

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]