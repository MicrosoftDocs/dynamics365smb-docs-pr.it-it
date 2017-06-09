---
title: "Procedura: Impostare cicli e fasi di vendita dalle opportunità | Documenti Microsoft"
description: "Viene descritto come impostare cicli e fasi di vendita dalle opportunità in Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Procedura: Impostare cicli e fasi di vendita dalle opportunità
Prima di iniziare a utilizzare le opportunità di vendita, è necessario impostare cicli di vendita e fasi dei cicli di vendita. Un ciclo di vendita è composto da una serie di fasi che vanno dal contatto iniziale alla chiusura della vendita. Per ogni fase possono essere previsti determinati requisiti che devono essere soddisfatti, ad esempio richiesta di un'offerta di vendita, prima che un'opportunità possa passare alla fase successiva. È inoltre possibile specificare se una fase può essere ignorata. È possibile impostare il numero desiderato di cicli di vendita e di fasi all'interno di un ciclo.

Implementare i cicli di vendita delle opportunità consiste nell'impostare il codice ciclo di vendita, definire le varie fasi del ciclo e quindi assegnare il ciclo alle opportunità.

## <a name="to-set-up-an-opportunity-sales-cycle-code"></a>Per impostare un codice ciclo di vendita delle opportunità
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Cicli di vendita**, quindi scegliere il collegamento correlato. La finestra **Cicli di vendita** si apre e viene visualizzato un elenco di tutti i cicli di vendita esistenti.
2. Scegliere l'azione **Nuovo** e compilare i campi.

Ripetere tali passaggi per impostare altri cicli di vendita. Dopo aver impostato i cicli delle opportunità di vendita, potrebbe essere necessario impostare le diverse fasi all'interno di ciascun ciclo.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Per definire le fasi ciclo di vendita delle opportunità
1. Nella finestra **Cicli di vendita** selezionare l'opportunità relativa al ciclo di vendita per la quale si desidera impostare le fasi, quindi fare clic sull'azione **Fasi**. Verrà aperta la finestra **Fasi ciclo di vendita**.
2. Scegliere l'azione **Nuovo** per inserire una nuova fase nel ciclo di vendita.

Ripetere tali passaggi per impostare altre fasi all'interno del ciclo di vendita.

## <a name="to-assign-stage-cycle-to-an-opportunity"></a>Per assegnare il ciclo della fase a un'opportunità
Una volta aggiunto il ciclo della fase delle opportunità, è possibile iniziare ad aggiungere le opportunità di vendita e quindi assegnare il ciclo della fase alle opportunità impostando il campo **Codice ciclo di vendita**. Per ulteriori informazioni, vedere [Procedura: Creare opportunità di vendita](marketing-how-create-opportunities.md).

## <a name="see-also"></a>Vedi anche
[Elaborazione delle opportunità di vendita](marketing-processing-sales-opportunities.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

