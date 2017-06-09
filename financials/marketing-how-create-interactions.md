---
title: 'Procedura: Creare interazioni per i contatti e i segmenti | Documenti Microsoft'
description: Viene descritto come creare interazioni per i contatti e i segmenti in Financials
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
ms.openlocfilehash: b50d332441bee01158559616fff5d5f5ca381a90
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-interactions-on-contacts-and-segments"></a>Procedura: Creare interazioni per i contatti e i segmenti
È possibile creare interazioni per registrare tutte le interazioni e le comunicazioni intercorse con i contatti e i segmenti, ad esempio messaggi di posta.

Prima di creare interazioni, è necessario impostare i modelli di interazione. Per ulteriori informazioni, vedere [Impostare modelli di interazione](marketing-interactions.md#set-up-interaction-templates).

## <a name="to-create-an-interaction"></a>Per creare un'interazione
1. Aprire il contatto, l'agente o il movimento log interazione.
2. Selezionare l'azione **Crea interazione**.
3. Compilare i campi e fare clic sul pulsante **OK**.

**Nota**: se è necessario eseguire un'altra attività prima di terminare l'interazione, è possibile scegliere **Annulla**, chiudere la procedura guidata e scegliere di terminare l'interazione in un secondo momento. Ciò pospone l'interazione.

## <a name="to-finish-and-delete-postponed-interactions"></a>Per completare ed eliminare le interazioni differite
1. Aprire il contatto, l'agente o il movimento log interazione.
2. Scegliere **Interazioni differite**.
3. Selezionare l'interazione che si desidera chiudere e scegliere l'azione **Riprendi**.

## <a name="to-create-an-interaction-on-a-segment"></a>Per creare un'interazione in un segmento
1. Nella home page scegliere **Segmenti attivi**; in alternativa, nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Segmenti**, quindi scegliere il collegamento correlato.
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
[Utilizzo di dati finanziari](ui-work-product.md)

