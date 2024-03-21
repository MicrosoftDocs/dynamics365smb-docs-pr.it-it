---
title: Creare interazioni per contatti e segmenti
description: Scopri come creare interazioni in Business Central per comunicazioni intercorse con contatti e segmenti.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.reviewer: ivkoleti
ms.date: 12/13/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
ms.service: dynamics-365-business-central
---
# Creare interazioni per contatti e segmenti

Puoi creare interazioni per tenere traccia delle comunicazioni che hai con un singolo contatto o con più contatti nei segmenti. Per semplificare la creazione di interazioni, [!INCLUDE [prod_short](includes/prod_short.md)] fornisce la guida al setup assistito **Crea interazione**. La guida ti aiuta ad acquisire dettagli importanti sull'interazione.

Prima di creare interazioni, tuttavia, devi impostare modelli interazione. Per ulteriori informazioni su modelli interazione, vedi [Impostare modelli interazione](marketing-interactions.md).

## Per creare un'interazione con un contatto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contatti**, **Venditore** o **Mov. log interazione**, quindi scegli il collegamento correlato.
2. Selezionare l'azione **Crea interazione**.
3. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Se devi interrompere prima di aver chiuso l'interazione, puoi scegliere **Annulla** e quindi specifica se desideri salvare le impostazioni per poter continuare in seguito. Per ulteriori informazioni su interazioni posticipate, vedi [Per completare la configurazione di un'interazione posticipata](#to-finish-setting-up-a-postponed-interaction).

## Per creare un'interazione in un segmento

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Segmenti**, quindi scegli il collegamento correlato.
2. Selezionare l'azione **Crea interazione**.
3. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Dopo aver assegnato un'interazione a un segmento, puoi eseguire diverse altre azioni nella pagina  **Segmento**:
>
> * Personalizza l'interazione per ogni singolo contatto nel segmento, ad esempio selezionando un altro modello interazione nelle righe.  
>* Registra il segmento e le interazioni scegliendo l'azione **Log** per aprire la pagina **Log segmento**.
> * Crea un nuovo segmento contenente gli stessi contatti scegliendo la casella di controllo **Crea segmento di follow-up**. Questa impostazione richiede che sia specificata una serie di numeri per i segmenti nella pagina  **Setup marketing**.

Un'interazione viene registrata per ogni contatto all'interno del segmento nella tabella **Mov. log interazione** e il segmento viene registrato. I segmenti registrati sono disponibili nella pagina **Segmento registrato**.

## Per completare la configurazione di un'interazione posticipata

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Interazioni posticipate**, quindi scegli il collegamento correlato.
2. Scegli l'interazione che vuoi chiudere e quindi scegli **Riprendi**.

## Vedere anche

[Registrazione di interazioni](marketing-interactions.md)  
[Gestione dei contatti](marketing-contacts.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzare Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]