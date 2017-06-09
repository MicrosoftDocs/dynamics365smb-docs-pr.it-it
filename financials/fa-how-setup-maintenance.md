---
title: 'Procedura: Impostare la manutenzione cespiti | Documenti Microsoft'
description: Viene descritto come impostare il sistema per la manutenzione dei cespiti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e97f3cec67fa8b0ef270d406a0efe804da82d99f
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-maintenance"></a>Procedura: Impostare la manutenzione cespiti
Per gestire la manutenzione dei cespiti, è prima necessario impostare alcune informazioni generali di manutenzione, un conto analitico per i costi di manutenzione e i codici di manutenzione per i tipi di lavoro, ad esempio assistenza di routine o riparazione.

## <a name="to-set-up-general-maintenance-information"></a>Per impostare le informazioni generali di manutenzione
Se vengono impostati campi per la manutenzione è possibile registrare le spese di manutenzione dalla registrazione cespiti.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Cespiti**, quindi scegliere il collegamento correlato.
2. Selezionare il cespite per cui si desidera definire la copertura assicurativa, quindi scegliere l'azione **Modifica**.
3. Compilare i campi appropriati nella Scheda dettaglio **Manutenzione**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Per impostare i codici di manutenzione
Quando si registrano dei costi di manutenzione dalle registrazioni COGE, si compila il campo **Cod. manutenzione** per registrare il tipo di manutenzione eseguita, ad esempio assistenza di routine o riparazione.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Manutenzione**, quindi scegliere il collegamento correlato.
2. Nella finestra **Manutenzione**, impostare i codici per i diversi tipi di lavoro di manutenzione.

## <a name="to-set-up-maintenance-expense-accounts"></a>Per impostare i conti spesa manutenzione
Per registrare i costi di manutenzione occorre prima immettere un numero di conto nella finestra **Cat. Reg. Cespite**.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Cat. reg. cespiti**, quindi scegliere il collegamento correlato.
2. Compilare il campo **Conto Spesa Manutenzione** per ogni categoria di registrazione.

**Nota:** per definire che i costi di manutenzione vengano allocati ai reparti o ai progetti, impostare le chiavi di allocazione. Per ulteriori informazioni, vedere [Procedura: Impostare le funzionalità generali per i cespiti](fa-how-setup-general.md).

## <a name="see-also"></a>Vedi anche
[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Finanza](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

