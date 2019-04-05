---
title: Aggiornare i tassi di cambio delle valute| Documenti Microsoft
description: Per utilizzare più valute nell'attività commerciale, è possibile impostare un codice per ogni valuta e utilizzare un servizio di conversione esterno.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 03/19/2019
ms.author: sgroespe
ms.openlocfilehash: 81db512103c36f77b9d31e01fe05214045e74705
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "853188"
---
# <a name="update-currency-exchange-rates"></a>Aggiornare i tassi di cambio valuta
Con l'espandersi delle attività delle società in un numero sempre maggiore di paesi, diventa importante poter vendere e riportare i dati finanziari in più di una valuta. È necessario impostare un codice per ogni valuta utilizzata se si compra o si vende in valute diverse dalla valuta locale, se si hanno debiti o crediti in altre valute o si registrano transazioni C/G in diverse valute.

La contabilità generale è impostata per utilizzare la valuta locale (VL) ma è anche possibile impostarla per l'uso di un'altra valuta con un tasso di cambio corrente assegnato. Se si imposta una seconda valuta come valuta contabile addizionale, in [!INCLUDE[d365fin](includes/d365fin_md.md)] gli importi in ogni movimento C/G e in tutti gli altri movimenti, ad esempio i movimenti IVA, vengono registrati automaticamente sia nella valuta locale che nella valuta addizionale. Per ulteriori informazioni, vedere [Impostare una valuta contabile addizionale](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Rettifica di tassi di cambio
Poiché i tassi di cambio oscillano costantemente, gli equivalenti in valuta addizionale nel sistema devono essere rettificati periodicamente. Se queste rettifiche non vengono apportate, gli importi che sono stati convertiti da valute estere (o addizionali) e registrati nella contabilità generale in valuta locale possono essere fuorvianti. Inoltre, i movimenti quotidiani registrati prima dell'immissione di un tasso di cambio quotidiano nel programma devono essere aggiornati dopo l'immissione delle informazioni su tale tasso di cambio.

Il processo batch **Rettifica tassi di cambio** viene utilizzato manualmente per rettificare i tassi di cambio dei movimenti cliente, fornitore e conti C/C bancari registrati. Consente inoltre di aggiornare gli importi nella valuta contabile addizionale nei movimenti C/G. I tassi di cambio possono essere rettificati automaticamente utilizzando un servizio. Per ulteriori informazioni, vedere [Per impostare un servizio dei tassi di cambio delle valute](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Effetto su clienti e fornitori
Per i conti di clienti e fornitori, la valuta viene rettificata in base al tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per singoli saldi in valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili non-realizzati** o nel campo **Conto Perdite Non-Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nel conto crediti/debiti della contabilità generale.

Il processo batch consente di elaborare tutti i movimenti registro clienti e i movimenti fornitori aperti. Se per un movimento vi è una differenza di tasso di cambio, il processo batch crea un nuovo registro fornitori o un nuovo registro clienti dettagliato, che riflette l'importo rettificato nel registro fornitori o clienti.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioni nei movimenti clienti e fornitori
Ai movimenti di rettifica vengono assegnate le dimensioni dei movimenti del registro clienti/fornitori e le rettifiche vengono registrate per combinazione di valori di dimensione.

### <a name="effect-on-bank-accounts"></a>Effetto su conti correnti bancari
Per i conti correnti bancari, la valuta viene rettificata utilizzando il tasso di cambio valido alla data di registrazione specificata nel processo batch. Durante il processo batch vengono calcolate le differenze per ogni conto corrente bancario che ha un codice di valuta, quindi gli importi vengono registrati nel conto C/G specificato nel campo **Conto utili realizzati** o nel campo **Conto Perdite Realizzate** della pagina **Valuta**. I movimenti rettificativi vengono automaticamente registrati nei conti correnti bancari CoGe specificati nelle categorie di registrazione dei conti correnti bancari. Viene calcolato un solo movimento per valuta per categoria di registrazione.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioni nei movimenti di conti correnti bancari
Ai movimenti di rettifica per il conto CoGe del conto corrente bancario e per il conto profitti/perdite vengono assegnate le dimensioni di default del conto corrente bancario.

### <a name="effect-on-gl-accounts"></a>Effetto su conti C/G
Se si effettua una registrazione in una valuta contabile addizionale, è possibile impostare il processo batch per creare nuovi movimenti di contabilità generale per rettifiche valutarie comprese tra VL e la valuta contabile addizionale. Verranno calcolate le differenze per ogni movimento C/G e inserite delle rettifiche a seconda del contenuto del campo **Rettifica tasso di cambio** di ogni conto C/G.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensioni nei movimenti del conto C/G
Ai movimenti di rettifica vengono assegnate le dimensioni di default dei conti in cui vengono registrati.

> [!Important]
> Prima di eseguire il processo batch, è necessario immettere i tassi di cambio di rettifica necessari alla rettifica dei saldi in valuta estera. Questa operazione viene eseguita nella pagina **Tassi di cambio valuta**.

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
