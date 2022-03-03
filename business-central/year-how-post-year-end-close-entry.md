---
title: Registrare il movimento di chiusura di fine anno
description: Descrive come aprire le registrazioni specificate nel processo batch Chiudi conto economico, quindi analizzare e registrare il movimento di chiusura di fine anno.
author: edupont04
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.search.form: 100
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: d426dc74506a244746d8696dc12f80a0ada3a58e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142700"
---
# <a name="posting-the-year-end-closing-entry"></a>Registrazione del movimento di chiusura di fine anno

Dopo avere utilizzato il processo batch **Chiudi conto economico** per generare il movimento o i movimenti di chiusura di fine anno, è necessario aprire le registrazioni specificate nel processo batch, quindi analizzare e registrare i movimenti.  

> [!TIP]
> A seconda dei processi di lavoro delle organizzazioni, è possibile scegliere di chiudere o meno i periodi contabili e gli anni fiscali in [!INCLUDE [prod_short](includes/prod_short.md)]. La procedura seguente presuppone che sia stato chiuso l'anno fiscale utilizzando l'opzione *Periodi contabili*, che sia stato generato un movimento di chiusura di fine anno utilizzando il processo batch **Chiudi conto economico** e che si è ora pronti a registrare il movimento di chiusura di fine anno insieme alla compensazione dei movimenti conti patrimonio netto. L'organizzazione può scegliere di lavorare in modo diverso, ad esempio di registrare il movimento di chiusura di fine anno come parte della chiusura dell'anno fiscale.

## <a name="to-post-the-year-end-closing-entry"></a>Per registrare il movimento di chiusura di fine anno

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
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