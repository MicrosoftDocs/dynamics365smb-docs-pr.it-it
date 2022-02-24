---
title: Analizzare e registrare il movimento di chiusura di fine anno | Documenti Microsoft
description: Descrive come aprire le registrazioni specificate nel processo batch Chiudi conto economico, quindi analizzare e registrare il movimento di chiusura di fine anno.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191739"
---
# <a name="post-the-year-end-closing-entry"></a>Registrare il movimento di chiusura di fine anno
Dopo avere utilizzato il processo batch **Chiudi conto economico** per generare il movimento o i movimenti di chiusura di fine anno, è necessario aprire le registrazioni specificate nel processo batch, quindi analizzare e registrare i movimenti.

## <a name="to-post-the-year-end-closing-entry"></a>Per registrare il movimento di chiusura di fine anno
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.
2. Nella pagina **Registrazione COGE**, nel campo **Nome batch**, selezionare il batch contenente i movimenti di chiusura.
3. Analizzare i movimenti.
4. Per contabilizzare le registrazioni, scegliere l'azione **Registra**.

> [!NOTE]  
>   Se viene rilevato un errore, viene visualizzato un messaggio di errore. Se la registrazione avviene correttamente, i movimenti registrati vengono rimossi dalle registrazioni. Dopo il completamento della registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero, e il risultato dell'anno viene trasferito al conto patrimoniale.

## <a name="see-also"></a>Vedi anche
[Chiudere periodi contabili](year-close-account-periods.md)  
[Chiusura registri](year-close-books.md)  
[Chiudi conto economico](year-close-income-statement.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
