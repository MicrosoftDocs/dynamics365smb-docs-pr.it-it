---
title: "Impostare cicli e fasi di vendita dalle opportunità| Documenti Microsoft"
description: "Descrive come definire fasi di vendita, dal contatto iniziale alla chiusura, per creare un ciclo di vendita e assegnarlo alle opportunità in Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ecff2e9e0705055a514f1726b3223f8196300cb6
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Impostare cicli e fasi di vendita dalle opportunità
Prima di iniziare a utilizzare le opportunità di vendita, è necessario impostare cicli di vendita e fasi dei cicli di vendita. Un ciclo di vendita è composto da una serie di fasi che vanno dal contatto iniziale alla chiusura della vendita. Per ogni fase possono essere previsti determinati requisiti che devono essere soddisfatti, ad esempio richiesta di un'offerta di vendita, prima che un'opportunità possa passare alla fase successiva. È inoltre possibile specificare se una fase può essere ignorata. È possibile impostare il numero desiderato di cicli di vendita e di fasi all'interno di un ciclo.

L'implementazione dei cicli di vendita delle opportunità consiste nell'impostare il ciclo di vendita, definire le varie fasi del ciclo e quindi assegnare il ciclo alle opportunità. L'assegnazione di un'attività o dei task rilevanti all'opportunità può inoltre essere parte dell'impostazione del ciclo di vendita.

In questo argomento viene descritto anche come impostare i task e le attività e come assegnare i task alle attività. Per ulteriori informazioni, vedere la sezione Per impostare attività con task.

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Per impostare codici ciclo di vendita delle opportunità
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cicli di vendita**, quindi scegliere il collegamento correlato. La finestra **Cicli di vendita** si apre e viene visualizzato un elenco di tutti i cicli di vendita esistenti.
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Ripetere tali passaggi per impostare altri cicli di vendita. Dopo aver impostato i cicli delle opportunità di vendita, potrebbe essere necessario impostare le diverse fasi all'interno di ciascun ciclo.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Per definire le fasi ciclo di vendita delle opportunità
1. Nella finestra **Cicli di vendita** selezionare l'opportunità relativa al ciclo di vendita per la quale si desidera impostare le fasi, quindi fare clic sull'azione **Fasi**. Verrà aperta la finestra **Fasi ciclo di vendita**.
2. Scegliere l'azione **Nuovo** per inserire una nuova fase nel ciclo di vendita.

Ripetere tali passaggi per impostare altre fasi all'interno del ciclo di vendita.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Per assegnare cicli della fase alle opportunità
Una volta aggiunto il ciclo della fase delle opportunità, è possibile iniziare ad aggiungere le opportunità di vendita e quindi assegnare il ciclo della fase alle opportunità impostando il campo **Codice ciclo di vendita**. Per ulteriori informazioni, vedere [Creare opportunità di vendita](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Per impostare attività con task
È possibile combinare più task, ad esempio task che rappresentano un passaggio, nelle attività. I task delle attività sono in relazione tra essi in base a una formula di date. È possibile assegnare attività alle opportunità, agli agenti o ai contatti.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Attività**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** e compilare i campi necessari.
3. Nella Scheda dettaglio **Righe**, compilare tutte le righe necessarie i campi per definire una o più attività nel report.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Per assegnare task o attività di task a opportunità
Se si è impostato un task, è possibile assegnarlo a una opportunità di vendita e quindi assegnare l'attività di cui il task fa parte.

> [!NOTE]  
>   Questa procedura descrive come assegnare i task dell'attività alle opportunità. i passaggi sono simili a quelli per l'assegnazione dei task ad agenti o contatti.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Opportunità**, quindi scegliere il collegamento correlato.
2. Selezionare un'opportunità, quindi scegliere l'azione **Task**.
3. Nella finestra **Lista task**, selezionare l'azione **Crea task**.
4.  Nella finestra **Crea task** compilare i campi secondo le proprie necessità.

    Si noti il campo **Opportunità**, che è assegnato automaticamente all'opportunità in questione.
5. Scegliere il pulsante **OK**.
6. Nella finestra **Lista task** selezionare il nuovo task e scegliere l'azione **Assegna attività**.
7. Nella finestra **Assegna attività** compilare i campi in base alle esigenze, quindi scegliere **OK**.

## <a name="see-also"></a>Vedi anche
[Elaborazione delle opportunità di vendita](marketing-processing-sales-opportunities.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

