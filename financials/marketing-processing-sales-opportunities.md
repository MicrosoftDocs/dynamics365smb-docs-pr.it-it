---
title: "Elaborazione delle opportunità di vendita | Documenti Microsoft"
description: "Viene descritta l&quot;elaborazione delle opportunità di vendita in Financials"
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
ms.openlocfilehash: 889ef028b34ddad52c978373a5dab4329d96c91f
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="processing-sales-opportunities"></a>Elaborazione delle opportunità di vendita
Ogni volta che si crea un'opportunità, si possono utilizzare numerose funzionalità per gestire l'opportunità e procedere verso il completamento.

## <a name="view-opportunities"></a>Visualizzare le opportunità
Le opportunità di vendita esistenti sono disponibili nella finestra **Lista opportunità**. Sono disponibili diversi metodi per accedere alla finestra per elaborare le opportunità di vendita:

| Per visualizzare le opportunità per | Passaggi |
| --- | --- |
| Tutti gli agenti e contatti |Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Lista opportunità**, quindi scegliere il collegamento correlato. |
| Un agente specifico |Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Agenti**, quindi scegliere il collegamento correlato. Selezionare l'agente, scegliere l'azione **Opportunitià** e quindi l'azione **Lista**. |
| Un contatto specifico |Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Contatti**, quindi scegliere il collegamento correlato. Selezionare il contatto dalla lista, quindi scegliere l'azione **Opportunitià**. |

Ciascuna di queste attività apre la finestra **Lista opportunità**.

## <a name="close-opportunities"></a>Chiudere le opportunità
È possibile chiudere le opportunità una volta concluse le negoziazioni. Quando si chiude un'opportunità, è possibile specificare se è stata vinta o persa e i motivi per chiuderla. Per specificare un motivo, è necessario impostare codici di chiusura opportunità.

1. Nella finestra **Lista opportunità** selezionare l'opportunità e scegliere l'azione **Chiudi**. Verrà visualizzata la finestra **Chiudi opportunità**.
2. Compilare i campi appropriati e fare clic sul pulsante **OK**.

   I campi **Codice opportunità chiuse** e **Data di chiusura** sono obbligatori e devono essere compilati prima di selezionare il pulsante **OK**.

   Nel campo **Codice opportunità chiuse**, è possibile scegliere tra i codici chiusura opportunità esistenti o aggiungere un nuovo codice. Per aggiungere un nuovo codice, dall'elenco a discesa, selezionare **Seleziona da elenco completo** quindi **Nuovo**. Nella nuova riga vuota, compilare i campi **Codice**, **Tipo** e **Descrizione** e quindi il pulsante **OK**.

## <a name="create-quotes-for-opportunities"></a>Per creare offerte per opportunità
È possibile creare offerte di vendita relative ai contatti che non sono registrati come clienti.

1. Nella finestra **Lista opportunità** selezionare l'opportunità e scegliere l'azione **Assegna offerta di vendita**. Verrà visualizzata la finestra **Offerta di vendita**.
2. Compilare i relativi campi.

## <a name="create-sales-orders-for-opportunities"></a>Per creare ordini di vendita per opportunità
È possibile creare ordini di vendita a partire dalle offerte di vendita create per le opportunità. Prima di creare ordini di vendita per i contatti, è necessario creare il contatto come cliente. Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Nella finestra **Lista opportunità** individuare l'opportunità per la quale è stata creata un'offerta di vendita.
2. Scegliere l'azione **Assegna offerta di vendita**. Verrà visualizzata la finestra **Offerta vendita** per visualizzare l'offerta di vendita assegnata all'opportunità.
3. Compilare i campi aggiuntivi, quindi scegliere l'azione **Crea ordine**.

Quando si gestiscono opportunità di vendita, potrebbe essere necessario creare un'offerta per il contatto al quale è collegata l'opportunità.

## <a name="delete-opportunities"></a>Rimuovere le opportunità
È possibile rimuovere opportunità, ad esempio dopo aver concluso un'operazione commerciale. Tuttavia, è possibile eliminare solo le opportunità chiuse. Esistono due modi per eliminare le opportunità chiuse. È possibile eliminare le opportunità chiuse dalla finestra **Lista opportunità** oppure è possibile eseguire il processo batch **Elimina opportunità chiuse** per eliminare più opportunità in base a criteri specifici.

Per eliminare le opportunità chiuse nella finestra **Lista opportunità**, selezionare l'opportunità quindi selezionare l'azione **Elimina**.

Per eliminare le opportunità chiuse utilizzando il processo batch **Elimina opportunità chiuse**, attenersi alla seguente procedura:

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Rimuovi opportunità**, quindi scegliere il collegamento correlato.
2. Nella sezione **Opportunità**, impostare i filtri che specificano le opportunità chiuse eliminare.
3. Scegliere il pulsante **OK**.

Una volta eliminata un'opportunità, verrà rimossa dalla finestra **Lista opportunità**.

## <a name="move-an-opportunity-through-sales-cycle-stages"></a>Spostare un'opportunità nelle fasi ciclo di vendita
Se un'opportunità segue un ciclo di vendita, è possibile spostarla in avanti o indietro nelle varie fasi, ad esempio verso la fase successiva o precedente e perfino saltare una fase.

1. Nella finestra **Lista opportunità**, selezionare l'azione **Aggiorna**. Verrà visualizzata la finestra **Aggiorna opportunità**.
2. Utilizzare il campo **Tipo azione** per spostare l'opportunità lungo le fasi ciclo di vendita.
   * Scegliendo **Successiva** l'opportunità verrà spostata in avanti di una fase.
   * **Ignora** sposta l'opportunità avanti di una o più fasi del ciclo di vendita specificato nel campo **Presentazione**. È possibile saltare solo le fasi che sono state impostate per consentire questa operazione.
   * Scegliendo **Precedente** l'opportunità verrà spostata indietro di una fase.
   * **Ignora** sposta l'opportunità indietro di una o più fasi del ciclo di vendita specificato nel campo **Presentazione**.
   * **Aggiorna** consente di modificare le informazioni, ad esempio modificare la valutazione delle possibilità di successo e i valori previsti, senza spostarsi in un'altra fase.
3. Compilare gli altri campi come appropriato e fare clic sul pulsante **OK**.

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Creazione e gestione di contatti](marketing-contacts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

