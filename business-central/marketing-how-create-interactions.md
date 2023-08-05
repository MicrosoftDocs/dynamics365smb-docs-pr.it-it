---
title: Creare interazioni per i contatti e i segmenti
description: 'Descrive come creare interazioni per comunicazioni intercorse con i contatti e i segmenti in Business Central, ad esempio messaggi di posta diretta.'
documentationcenter: ''
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
ms.date: 04/01/2021
ms.author: jswymer
---
# Creare interazioni per i contatti e i segmenti
È possibile creare interazioni per registrare tutte le interazioni e le comunicazioni intercorse con i contatti e i segmenti, ad esempio messaggi di posta.

Prima di creare interazioni, è necessario impostare i modelli di interazione. Per ulteriori informazioni, vedere [Impostare modelli di interazione](marketing-interactions.md).

## Per creare un'interazione
1. Aprire il contatto, l'agente o il movimento log interazione.
2. Selezionare l'azione **Crea interazione**.
3. Compilare i campi e scegliere **OK**.

> [!NOTE]  
>   Se è necessario eseguire un'altra attività prima di terminare l'interazione, è possibile scegliere **Annulla**, quindi terminare l'interazione in un secondo momento. Ciò pospone l'interazione.

## Per completare ed eliminare le interazioni differite
1. Aprire il contatto, l'agente o il movimento log interazione.
2. Scegliere **Interazioni differite**.
3. Selezionare l'interazione che si desidera chiudere e scegliere l'azione **Riprendi**.

## Per creare un'interazione in un segmento
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Segmenti**, quindi scegli il collegamento correlato.
2. Nella pagina **Segmento**, nella sezione **Interazione**, compilare i campi per specificare l'interazione che si desidera assegnare al segmento.

    Una volta assegnata un'interazione al segmento, è possibile personalizzare l'interazione per ogni singolo contatto all'interno del segmento, ad esempio selezionando un altro modello di interazione nelle righe della pagina **Segmento**.  
3. Per registrare il segmento e interazioni, selezionare l'azione **Log**. Verrà visualizzata la pagina **Log segmento**.
4. Se si desidera creare un nuovo segmento contenente gli stessi contatti, selezionare la casella di controllo **Crea segmento di follow-up**. Per creare un segmento di follow-up, è necessario specificare la numerazione dei segmenti nella pagina **Setup marketing**.

Un'interazione viene registrata per ogni contatto all'interno del segmento nella tabella **Mov. log interazione** e il segmento viene registrato. È possibile individuare i segmenti registrati nella pagina **Segmento registrato**.

Se è stata selezionata la casella di controllo **Crea segmento di follow-up**, verrà creato un nuovo segmento contenente gli stessi contatti del segmento appena registrato.

## Vedi anche
[Registrazione di interazioni](marketing-interactions.md)  
[Gestione dei contatti](marketing-contacts.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzare Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]