---
title: Registrare il movimento di chiusura di fine anno
description: Descrive come aprire le registrazioni specificate nel processo batch Chiudi conto economico, quindi analizzare e registrare il movimento di chiusura di fine anno.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c822685ae5723bc6b13f9fedad45dbddefdb956
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776594"
---
# <a name="post-the-year-end-closing-entry"></a>Registrare il movimento di chiusura di fine anno

Dopo avere utilizzato il processo batch **Chiudi conto economico** per generare il movimento o i movimenti di chiusura di fine anno, è necessario aprire le registrazioni specificate nel processo batch, quindi analizzare e registrare i movimenti.  

> [!TIP]
> A seconda dei processi di lavoro delle organizzazioni, è possibile scegliere di chiudere o meno i periodi contabili e gli anni fiscali in [!INCLUDE [prod_short](includes/prod_short.md)]. La procedura seguente presuppone che sia stato chiuso l'anno fiscale utilizzando l'opzione *Periodi contabili*, che sia stato generato un movimento di chiusura di fine anno utilizzando il processo batch **Chiudi conto economico** e che si è ora pronti a registrare il movimento di chiusura di fine anno insieme alla compensazione dei movimenti conti patrimonio netto. L'organizzazione può scegliere di lavorare in modo diverso, ad esempio di registrare il movimento di chiusura di fine anno come parte della chiusura dell'anno fiscale.

## <a name="to-post-the-year-end-closing-entry"></a>Per registrare il movimento di chiusura di fine anno

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.
2. Nella pagina **Registrazione COGE**, nel campo **Nome batch**, selezionare il batch contenente i movimenti di chiusura.
3. Analizzare i movimenti.
4. Per contabilizzare le registrazioni, scegliere l'azione **Registra**.

> [!NOTE]  
> Se viene rilevato un errore, viene visualizzato un messaggio di errore. Se la registrazione avviene correttamente, i movimenti registrati vengono rimossi dalle registrazioni. Dopo il completamento della registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero, e il risultato dell'anno viene trasferito al conto patrimoniale.

## <a name="see-also"></a>Vedi anche

[Chiudere periodi contabili](year-close-account-periods.md)  
[Chiusura registri](year-close-books.md)  
[Chiudi conto economico](year-close-income-statement.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]