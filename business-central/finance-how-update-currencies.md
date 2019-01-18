---
title: Aggiornare i tassi di cambio delle valute| Documenti Microsoft
description: "Per utilizzare più valute nell'attività commerciale, è possibile impostare un codice per ogni valuta e utilizzare un servizio di conversione esterno, ad esempio FloatRates."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 23940bd1e5fd29dc92e8285c08679135889701e9
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="update-currency-exchange-rates"></a>Aggiornare i tassi di cambio valuta
È necessario impostare un codice per ogni valuta utilizzata se si compra o si vende in valute diverse dalla valuta locale, se si hanno debiti o crediti in altre valute o si registrano transazioni C/G in diverse valute.  

Con l'espandersi delle attività delle società in un numero sempre maggiore di paesi, diventa importante poter rivedere o riportare i dati finanziari in più di una valuta. Il programma consente l'utilizzo di più valute. La contabilità generale viene impostata utilizzando la valuta locale (VL), ma è possibile impostare un'altra valuta come valuta addizionale, assegnando un tasso di cambio corrente.  

 Se si imposta una seconda valuta come valuta contabile addizionale, gli importi in ogni movimento CG e in tutti gli altri movimenti, ad esempio i movimenti IVA, vengono registrati automaticamente in [!INCLUDE[d365fin](includes/d365fin_md.md)] sia nella valuta locale che nella valuta addizionale. Quando vengono calcolati gli importi dei movimenti C/G in una valuta contabile addizionale, vengono utilizzate le informazioni della pagina **Tassi di cambio valuta** per individuare il tasso di cambio appropriato.  

> [!WARNING]  
>  La funzionalità Valuta addizionale NON deve essere utilizzata come base per la conversione del rendiconto finanziario. Questo strumento non consente di eseguire la conversione dei rendiconti finanziari delle filiali estere come parte del consolidamento di una società. La funzionalità della valuta contabile addizionale consente esclusivamente di creare report in un'altra valuta, come se tale valuta fosse quella locale della società.

## <a name="adjusting-exchange-rates"></a>Rettifica di tassi di cambio  
Poiché i tassi di cambio oscillano costantemente, gli equivalenti in valuta addizionale nel sistema devono essere rettificati periodicamente. Se queste rettifiche non vengono apportate, gli importi che sono stati convertiti da valute estere (o addizionali) e registrati nella contabilità generale in valuta locale possono essere fuorvianti. Inoltre, i movimenti quotidiani registrati prima dell'immissione di un tasso di cambio quotidiano nel programma devono essere aggiornati dopo l'immissione delle informazioni su tale tasso di cambio. Il processo batch Rettifica tassi di cambio viene utilizzato per rettificare i tassi di cambio dei movimenti cliente, fornitore e conti C/C bancari registrati. Consente inoltre di aggiornare gli importi nella valuta contabile addizionale nei movimenti C/G.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Visualizzazione di report e importi nella valuta addizionale  
L'utilizzo di una valuta addizionale può essere utile per il processo di creazione di report di una società nei seguenti casi:  

- Società di paesi non UE che effettuano numerose transazioni con società di paesi UE. In questo caso, la società non UE potrebbe desiderare di creare report in euro per semplificare l'utilizzo dei report finanziari da parte dei partner commerciali UE.  

- Società che desiderano visualizzare i report in una valuta maggiormente utilizzata a livello internazionale rispetto alla propria valuta locale.  

Numerosi report nell'area di applicazione della contabilità generale sono basati sui movimenti C/G. Per visualizzare i dati finanziari del report nella valuta contabile aggiuntiva, selezionare semplicemente il campo **Mostra in valuta di cambio addizionale** nella pagina di report CG pertinente.  

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
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

