---
title: Come eliminare i movimenti di budget costi | Microsoft Docs
description: Utilizzare il processo batch **Elimina mov. budget costi** per annullare i movimenti di budget costi dal registro budget costi.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ad8ba706ba1b376b78449ba801ed0f4fc4cfe09
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="delete-cost-budget-entries"></a>Elimina mov. budget costi
Utilizzare il processo batch **Elimina mov. budget costi** per annullare i movimenti di budget costi dal registro budget costi.  

Per evitare qualsiasi gap nei movimenti di budget costi e nei movimenti del registro dei costi, non è possibile eliminare un unico movimento o un batch di movimenti a metà della lista dei movimenti del registro.  

### <a name="to-delete-a-cost-budget-entry"></a>Per eliminare un mov. budget costi  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Elimina mov. budget costi**, quindi scegliere il collegamento correlato.  

    Nel campo **A nr. registro** è incluso l'ultimo numero del movimento del registro e non può essere modificato.  

    È possibile utilizzare il campo **Da nr. registro** per selezionare un numero di movimento del registro dal quale iniziare l'eliminazione.  
2.  Scegliere il pulsante **OK** per eliminare i movimenti di bugdet costi selezionati.  

> [!NOTE]  
>  Per evitare un'eliminazione accidentale dei movimenti di budget costi, è possibile chiudere i movimenti del registro contrassegnando le righe come **Chiuso** nel campo **Chiuso** della finestra **Registri budget costi**.  

## <a name="see-also"></a>Vedi anche  
[Contabilizzazione dei costi](finance-manage-cost-accounting.md)
[Creazione di budget di costi](finance-create-cost-budgets.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

