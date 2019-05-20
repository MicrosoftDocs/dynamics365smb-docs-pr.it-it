---
title: Assegnare un livello di priorità a un fornitore | Documenti Microsoft
description: È possibile assegnare dei numeri ai fornitori per assegnare loro una priorità e semplificare i suggerimenti di pagamento in Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c709539b24aa1f94c86dee26dd63adead39c892b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252365"
---
# <a name="prioritize-vendors"></a>Attribuire un ordine di priorità ai fornitori
[!INCLUDE[d365fin](includes/d365fin_md.md)] può fornire suggerimenti di pagamento ai fornitori, ad esempio pagamenti con scadenza a breve termine oppure pagamenti che prevedono uno sconto. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).

Innanzitutto, è necessario assegnare una priorità ai fornitori assegnando loro dei numeri.

## <a name="to-prioritize-vendors"></a>Per attribuire un ordine di priorità ai fornitori
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.
2. Selezionare il fornitore appropriato e scegliere **Modifica**.
3. Nel campo **Priorità** immettere un numero.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] il numero più basso, escluso lo 0, ha la massima priorità. Così, ad esempio, se si usano 1, 2 e 3, 1 avrà la massima priorità.

Se non si desidera dare la priorità a un fornitore, lasciare vuoto il campo **Priorità**. Quindi, se si usa la funzione di suggerimento di pagamento, il fornitore si troverà dopo tutti i fornitori che hanno un numero di priorità. Si possono immettere tutti i livelli di priorità necessari.

## <a name="see-also"></a>Vedi anche
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
