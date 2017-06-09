---
title: 'Procedura: Aggiornare i tassi di cambio delle valute | Documenti Microsoft'
description: Utilizzo delle valute multiple
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Procedura: Aggiornare i tassi di cambio
È necessario impostare un codice per ogni valuta utilizzata se si compra o si vende in valute diverse dalla valuta locale, se si hanno debiti o crediti in altre valute o si registrano transazioni C/G in diverse valute.  

**Nota**: questa funzionalità richiede che l'esperienza sia impostata su ***** Suite *****. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

È possibile utilizzare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute. Il servizio Tassi di cambio della valuta di Yahoo è preinstallato e pronto per essere abilitato.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Per impostare un servizio dei tassi di cambio delle valute
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Servizi tasso di cambio valuta**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella finestra **Servizi tasso di cambio valuta** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere la casella controllo **Abilitato** per abilitare il servizio.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Per aggiornare i tassi di cambio delle valute mediante un servizio
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Valute**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Aggiorna tassi di cambio**.

Il valore nel campo **Tasso di cambio** della finestra **Valute** viene aggiornato con il tasso di cambio delle valute più recente.

## <a name="see-also"></a>Vedi anche
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

