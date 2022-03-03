---
title: Elimina mov. budget costi
description: Utilizzare il processo batch Elimina mov. budget costi per annullare i movimenti di budget costi dal registro budget costi.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 1115
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1d6d920e4259752a25dd73c4b10a84e09334f78e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138019"
---
# <a name="delete-cost-budget-entries"></a>Elimina mov. budget costi

Utilizzare il processo batch **Elimina mov. budget costi** per annullare i movimenti di budget costi dal registro budget costi.  

Per evitare qualsiasi gap nei movimenti di budget costi e nei movimenti del registro dei costi, non è possibile eliminare un unico movimento o un batch di movimenti a metà della lista dei movimenti del registro.  

## <a name="to-delete-a-cost-budget-entry"></a>Per eliminare un mov. budget costi  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Elimina mov. budget costi**, quindi seleziona il collegamento correlato.  

    Nel campo **A nr. registro** è incluso l'ultimo numero del movimento del registro e non può essere modificato.  

    È possibile utilizzare il campo **Da nr. registro** per selezionare un numero di movimento del registro dal quale iniziare l'eliminazione.  
2. Scegliere il pulsante **OK** per eliminare i movimenti di bugdet costi selezionati.  

> [!NOTE]  
> Per evitare un'eliminazione accidentale dei movimenti di budget costi, è possibile chiudere i movimenti del registro contrassegnando le righe come **Chiuso** nel campo **Chiuso** della pagina **Registri budget costi**.  

## <a name="see-also"></a>Vedere anche

[Contabilizzazione dei costi](finance-manage-cost-accounting.md)
[Creazione di budget di costi](finance-create-cost-budgets.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]