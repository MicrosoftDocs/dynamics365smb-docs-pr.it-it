---
title: Come eliminare i movimenti di budget costi | Microsoft Docs
description: Utilizzare il processo batch Elimina mov. budget costi per annullare i movimenti di budget costi dal registro budget costi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 54df71ec903cc23930a88b0a5b20a17ecfb3d561
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183382"
---
# <a name="delete-cost-budget-entries"></a>Elimina mov. budget costi
Utilizzare il processo batch **Elimina mov. budget costi** per annullare i movimenti di budget costi dal registro budget costi.  

Per evitare qualsiasi gap nei movimenti di budget costi e nei movimenti del registro dei costi, non è possibile eliminare un unico movimento o un batch di movimenti a metà della lista dei movimenti del registro.  

### <a name="to-delete-a-cost-budget-entry"></a>Per eliminare un mov. budget costi  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina mov. budget costi** e quindi scegliere il collegamento correlato.  

    Nel campo **A nr. registro** è incluso l'ultimo numero del movimento del registro e non può essere modificato.  

    È possibile utilizzare il campo **Da nr. registro** per selezionare un numero di movimento del registro dal quale iniziare l'eliminazione.  
2.  Scegliere il pulsante **OK** per eliminare i movimenti di bugdet costi selezionati.  

> [!NOTE]  
>  Per evitare un'eliminazione accidentale dei movimenti di budget costi, è possibile chiudere i movimenti del registro contrassegnando le righe come **Chiuso** nel campo **Chiuso** della pagina **Registri budget costi**.  

## <a name="see-also"></a>Vedere anche  
[Contabilizzazione dei costi](finance-manage-cost-accounting.md)
[Creazione di budget di costi](finance-create-cost-budgets.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
