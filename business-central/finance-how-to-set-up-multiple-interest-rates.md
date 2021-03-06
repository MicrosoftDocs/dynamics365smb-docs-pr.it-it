---
title: Come impostare più tassi d'interesse
description: È possibile calcolare gli addebiti di interessi con più tassi di interesse per un periodo specifico. Il calcolo degli interessi è simile per tutti gli addebiti di interessi, con la sola variazione del tasso di interesse in un periodo specifico.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a38e286dab02dcb23acaba39a0d61b0b939bb20
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775427"
---
# <a name="set-up-multiple-interest-rates"></a>Impostare più tassi d'interesse
Più tassi di interesse sono utilizzati in periodi differenti per pagamenti in ritardo nelle transazioni commerciali. Ad esempio, un governo specifica il tasso di interesse massimo da imporre ai consumatori. Questo tasso di interesse può essere modificato due volte all'anno, il 1° gennaio e il 1° luglio. Il tasso di interesse tra le aziende (B2B) è concordato tra le parti e non è soggetto ad alcun limite. Il tasso annunciato è in genere superiore del quattro per cento all'interesse bancario normale.

Quando si creano le condizioni di addebito degli interessi e i termini di sollecito, per la penalità di pagamento ritardato, è possibile specificare più tassi di interesse in modo che la penalità sia calcolata in base a tassi di interesse differenti in diversi periodi. Per ulteriori informazioni, vedere [Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Per impostare più tassi d'interesse  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Condiz. interessi finanziari** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Condiz. interessi finanziari**, selezionare le condizioni di addebito, quindi scegliere l'azione **Tassi di interesse**.  
3.  Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Scegliere il pulsante **OK**.  
5.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Termini di sollecito** e quindi scegliere il collegamento correlato.  
6.  Nella pagina **Termini di sollecito**, selezionare i termini di sollecito, quindi scegliere l'azione **Livelli**.  
7.  Nella pagina **Livelli di sollecito**, selezionare il campo **Interessi calcolati**.  

Quando si emette una nota di addebito interessi, la nota mostra gli addebiti di interessi con più tassi di interesse per un periodo di tempo specifico. La nota contiene anche dettagli relativi a contatti del cliente, società che ha emesso la nota, importo addizionale e importo totale. Il movimento di apertura nella nota è visualizzato in grassetto. Gli addebiti di interessi sono calcolati con più tassi di interesse per un periodo di tempo specifico e vengono stampati dopo il movimento di apertura della nota.  

## <a name="see-also"></a>Vedere anche  
[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]