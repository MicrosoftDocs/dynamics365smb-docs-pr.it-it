---
title: Eliminare le voci del budget dei costi
description: Utilizzare il processo batch Elimina mov. budget costi per annullare i movimenti di budget costi dal registro budget costi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1115
ms.date: 07/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="delete-cost-budget-entries"></a>Eliminare le voci del budget dei costi

Utilizzare il processo batch **Elimina mov. budget costi** per annullare i movimenti di budget costi dal registro budget costi.  

Per evitare lacune nelle voci del budget dei costi e nelle voci del registro dei costi, non è possibile eliminare una singola voce o un lotto di voci al centro dell'elenco delle voci del registro.  

## <a name="to-delete-a-cost-budget-entry"></a>Per eliminare un mov. budget costi

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Elimina mov. budget costi**, quindi seleziona il collegamento correlato.  

    Nel campo **A nr. registro** Il campo contiene l'ultimo numero di registrazione e non può essere modificato.  

    È possibile utilizzare il campo **Da nr. registro** per selezionare un numero di movimento del registro dal quale iniziare l'eliminazione.  
2. Scegliere il pulsante **OK** per eliminare i movimenti di bugdet costi selezionati.  

> [!NOTE]  
> Per evitare un'eliminazione accidentale dei movimenti di budget costi, è possibile chiudere i movimenti del registro contrassegnando le righe come **Chiuso** nel campo **Chiuso** della pagina **Registri budget costi**.  

## <a name="see-also"></a>Vedere anche

[Contabilizzazione dei costi](finance-manage-cost-accounting.md)    
[Creazione di budget dei costi](finance-create-cost-budgets.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
