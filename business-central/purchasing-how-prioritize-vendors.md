---
title: Assegnare un livello di priorità a un fornitore (video) | Documenti Microsoft
description: È possibile assegnare dei numeri ai fornitori per assegnare loro una priorità e semplificare i suggerimenti di pagamento in Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7e68c56422f4f3de33006297ec396fdd34169e8d
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940053"
---
# <a name="prioritize-vendors"></a>Attribuire un ordine di priorità ai fornitori
[!INCLUDE[prod_short](includes/prod_short.md)] può fornire suggerimenti di pagamento ai fornitori, ad esempio pagamenti con scadenza a breve termine oppure pagamenti che prevedono uno sconto. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).

Innanzitutto, è necessario assegnare una priorità ai fornitori assegnando loro dei numeri.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Per attribuire un ordine di priorità ai fornitori
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Selezionare il fornitore appropriato e scegliere **Modifica**.
3. Nel campo **Priorità** immettere un numero.

In [!INCLUDE[prod_short](includes/prod_short.md)] il numero più basso, escluso lo 0, ha la massima priorità. Così, ad esempio, se si usano 1, 2 e 3, 1 avrà la massima priorità.

Se non si desidera dare la priorità a un fornitore, lasciare vuoto il campo **Priorità**. Quindi, se si usa la funzione di suggerimento di pagamento, il fornitore si troverà dopo tutti i fornitori che hanno un numero di priorità. Si possono immettere tutti i livelli di priorità necessari.

## <a name="see-also"></a>Vedere anche
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]