---
title: Creare interazioni per i contatti e i segmenti| Documenti Microsoft
description: Descrive come creare interazioni per comunicazioni intercorse con i contatti e i segmenti in Finance and Operations, Business edition, ad esempio messaggi di posta diretta.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 93d5bc9fd8189d5a8341faa252de9eac257901d2
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="create-interactions-on-contacts-and-segments"></a>Creare interazioni per i contatti e i segmenti
È possibile creare interazioni per registrare tutte le interazioni e le comunicazioni intercorse con i contatti e i segmenti, ad esempio messaggi di posta.

Prima di creare interazioni, è necessario impostare i modelli di interazione. Per ulteriori informazioni, vedere [Impostare modelli di interazione](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>Per creare un'interazione
1. Aprire il contatto, l'agente o il movimento log interazione.
2. Selezionare l'azione **Crea interazione**.
3. Compilare i campi e scegliere **OK**.

> [!NOTE]  
>   Se è necessario eseguire un'altra attività prima di terminare l'interazione, è possibile scegliere **Annulla**, quindi terminare l'interazione in un secondo momento. Ciò pospone l'interazione.

## <a name="to-finish-and-delete-postponed-interactions"></a>Per completare ed eliminare le interazioni differite
1. Aprire il contatto, l'agente o il movimento log interazione.
2. Scegliere **Interazioni differite**.
3. Selezionare l'interazione che si desidera chiudere e scegliere l'azione **Riprendi**.

## <a name="to-create-an-interaction-on-a-segment"></a>Per creare un'interazione in un segmento
1. Nella home page scegliere **Segmenti attivi** o scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Segmenti**, quindi scegliere il collegamento correlato.
2. Nella finestra **Segmento**, nella sezione **Interazione**, compilare i campi per specificare l'interazione che si desidera assegnare al segmento.

    Una volta assegnata un'interazione al segmento, è possibile personalizzare l'interazione per ogni singolo contatto all'interno del segmento, ad esempio selezionando un altro modello di interazione nelle righe della finestra **Segmento**.  
3. Per registrare il segmento e interazioni, selezionare l'azione **Log**. Verrà visualizzata la finestra **Log segmento**.
4. Se si desidera creare un nuovo segmento contenente gli stessi contatti, selezionare la casella di controllo **Crea segmento di follow-up**. Per creare un segmento di follow-up, è necessario specificare la numerazione dei segmenti nella finestra **Setup marketing**.

Un'interazione viene registrata per ogni contatto all'interno del segmento nella tabella **Mov. log interazione** e il segmento viene registrato. È possibile individuare i segmenti registrati nella finestra **Segmento registrato**.

Se è stata selezionata la casella di controllo **Crea segmento di follow-up**, verrà creato un nuovo segmento contenente gli stessi contatti del segmento appena registrato.

## <a name="see-also"></a>Vedi anche
[Registrazione di interazioni](marketing-interactions.md)  
[Gestione dei contatti](marketing-contacts.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Setup Relationship Management](marketing-setup-marketing.md)  
[Utilizzo di Finance and Operations, Business edition](ui-work-product.md)

