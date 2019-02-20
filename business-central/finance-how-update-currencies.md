---
title: Aggiornare i tassi di cambio delle valute| Documenti Microsoft
description: "Per utilizzare più valute nell'attività commerciale, è possibile impostare un codice per ogni valuta e utilizzare un servizio di conversione esterno."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: it-it
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a>Aggiornare i tassi di cambio valuta
Con l'espandersi delle attività delle società in un numero sempre maggiore di paesi, diventa importante poter vendere e riportare i dati finanziari in più di una valuta. È necessario impostare un codice per ogni valuta utilizzata se si compra o si vende in valute diverse dalla valuta locale, se si hanno debiti o crediti in altre valute o si registrano transazioni C/G in diverse valute.

La contabilità generale è impostata per utilizzare la valuta locale (VL) ma è anche possibile impostarla per l'uso di un'altra valuta con un tasso di cambio corrente assegnato. Se si imposta una seconda valuta come valuta contabile addizionale, in [!INCLUDE[d365fin](includes/d365fin_md.md)] gli importi in ogni movimento C/G e in tutti gli altri movimenti, ad esempio i movimenti IVA, vengono registrati automaticamente sia nella valuta locale che nella valuta addizionale. Per ulteriori informazioni, vedere [Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Rettifica di tassi di cambio
Poiché i tassi di cambio oscillano costantemente, gli equivalenti in valuta addizionale nel sistema devono essere rettificati periodicamente. Se queste rettifiche non vengono apportate, gli importi che sono stati convertiti da valute estere (o addizionali) e registrati nella contabilità generale in valuta locale possono essere fuorvianti. Inoltre, i movimenti quotidiani registrati prima dell'immissione di un tasso di cambio quotidiano nel programma devono essere aggiornati dopo l'immissione delle informazioni su tale tasso di cambio. Il processo batch Rettifica tassi di cambio viene utilizzato per rettificare i tassi di cambio dei movimenti cliente, fornitore e conti C/C bancari registrati. Consente inoltre di aggiornare gli importi nella valuta contabile addizionale nei movimenti C/G.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Per impostare un servizio dei tassi di cambio delle valute
È possibile utilizzare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute, ad esempio FloatRates.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Servizi tasso di cambio valuta** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Servizi tasso di cambio valuta** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere la casella controllo **Abilitato** per abilitare il servizio.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Per aggiornare i tassi di cambio delle valute mediante un servizio
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Valute** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Aggiorna tassi di cambio**.

Il valore nel campo **Tasso di cambio** della pagina **Valute** viene aggiornato con il tasso di cambio delle valute più recente.

## <a name="see-also"></a>Vedi anche
[Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

