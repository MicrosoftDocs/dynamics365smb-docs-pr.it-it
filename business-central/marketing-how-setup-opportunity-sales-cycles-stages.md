---
title: Impostare cicli e fasi di vendita dalle opportunità
description: 'Descrive come definire fasi di vendita, dal contatto iniziale alla chiusura, per creare un ciclo di vendita e assegnarlo alle opportunità in Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5122, 5121, 5120, 5175, 5119, 5098, 5096'
ms.date: 05/27/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Impostare cicli e fasi di vendita dalle opportunità

Prima di iniziare a utilizzare le opportunità di vendita, è necessario impostare cicli di vendita e fasi dei cicli di vendita. Un ciclo di vendita è composto da una serie di fasi che vanno dal contatto iniziale alla chiusura della vendita. Per ogni fase definisci i requisiti che devono essere soddisfatti, ad esempio richiesta di un'offerta di vendita, prima che un'opportunità possa passare alla fase successiva. È inoltre possibile specificare se una fase può essere ignorata. Puoi impostare un numero infinito di cicli di vendita. È possibile impostare tutte le fasi del ciclo di vendita necessarie all'interno di un ciclo di vendita.

Per utilizzare i cicli di vendita opportunità, devi impostare il ciclo di vendita, definire le diverse fasi del ciclo e quindi assegnare il ciclo alle opportunità. L'assegnazione di un'attività o dei task rilevanti all'opportunità può inoltre essere parte dell'impostazione del ciclo di vendita.

In questo articolo viene descritto anche come impostare i task e le attività e come assegnare i task alle attività. Per ulteriori informazioni, vedere [Per impostare attività con task](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Per impostare codici ciclo di vendita delle opportunità

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cicli di vendita**, quindi seleziona il collegamento correlato. La pagina **Cicli di vendita** si apre e viene visualizzato un elenco di tutti i cicli di vendita esistenti.
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Ripetere tali passaggi per impostare altri cicli di vendita. Dopo aver impostato i cicli delle opportunità di vendita, potrebbe essere necessario impostare le diverse fasi all'interno di ciascun ciclo.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Per definire le fasi ciclo di vendita delle opportunità

1. Nella pagina **Cicli di vendita** selezionare l'opportunità relativa al ciclo di vendita per la quale si desidera impostare le fasi, quindi fare clic sull'azione **Fasi**. Verrà aperta la pagina **Fasi ciclo di vendita**.
2. Scegliere l'azione **Nuovo** per inserire una nuova fase nel ciclo di vendita.

Ripetere tali passaggi per impostare altre fasi all'interno del ciclo di vendita.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Per assegnare cicli della fase alle opportunità

Una volta aggiunto il ciclo della fase delle opportunità, è possibile iniziare ad aggiungere le opportunità di vendita e quindi assegnare il ciclo della fase alle opportunità impostando il campo **Codice ciclo di vendita**. Per ulteriori informazioni, vedere [Creare opportunità di vendita](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Per impostare attività con task

È possibile combinare più task, ad esempio task che rappresentano un passaggio, nelle attività. I task delle attività sono in relazione tra essi in base a una formula di date. È possibile assegnare attività alle opportunità, agli agenti o ai contatti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Attività**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Nella Scheda dettaglio **Righe**, compilare tutte le righe necessarie i campi per definire una o più attività nel report.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Per assegnare task o attività di task a opportunità

Se si è impostato un task, è possibile assegnarlo a una opportunità di vendita e quindi assegnare l'attività di cui il task fa parte.

> [!NOTE]
> Non è possibile creare task di tipo *Riunione* in [!INCLUDE [prod_short](includes/prod_short.md)] online. La funzionalità richiede l'accesso a una distribuzione locale.

La seguente procedura descrive come assegnare i task dell'attività alle opportunità. I passaggi sono simili a quelli per l'assegnazione dei task ad agenti o contatti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Opportunità**, quindi scegli il collegamento correlato.
2. Selezionare un'opportunità, quindi scegliere l'azione **Task**.
3. Nella pagina **Lista task**, selezionare l'azione **Crea task**.
4. Nella pagina **Crea task** compilare i campi secondo le proprie necessità. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Come puoi vedere nel campo **Opportunità**, il task è assegnato automaticamente all'opportunità rilevante.
5. Scegli il pulsante **OK**.
6. Nella pagina **Lista task** selezionare il nuovo task e scegliere l'azione **Assegna attività**.
7. Nella pagina **Assegna attività** compilare i campi in base alle esigenze, quindi scegliere **OK**.

## <a name="see-also"></a>Vedere anche

[Elaborazione delle opportunità di vendita](marketing-processing-sales-opportunities.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
