---
title: "Elaborare le opportunità di vendita nei cicli di vendita| Documenti Microsoft"
description: "È possibile visualizzare, chiudere o eliminare le opportunità di vendita ed è anche possibile creare offerte e ordini di vendita per opportunità e spostare un'opportunità fra le fasi di un ciclo di vendita."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 5b57b47d4ceb08a3836140945387e38887553a99
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="process-sales-opportunities"></a>Elaborare le opportunità di vendita
Ogni volta che si crea un'opportunità, si possono utilizzare numerose funzionalità per gestire l'opportunità e procedere verso il completamento.

## <a name="to-view-opportunities"></a>Per visualizzare le opportunità
Le opportunità di vendita esistenti sono disponibili nella finestra **Lista opportunità**. Sono disponibili diversi metodi per accedere alla finestra per elaborare le opportunità di vendita:

| Per visualizzare le opportunità per | Quindi |
| --- | --- |
| Tutti gli agenti e contatti |Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Lista opportunità** e quindi scegliere il collegamento correlato. |
| Un agente specifico |Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Offerta di vendita** e quindi scegliere il collegamento correlato. Selezionare l'agente, scegliere l'azione **Opportunitià** e quindi l'azione **Lista**. |
| Un contatto specifico |Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato. Selezionare il contatto dalla lista, quindi scegliere l'azione **Opportunitià**. |

Ciascuna di queste attività apre la finestra **Lista opportunità**.

## <a name="to-close-opportunities"></a>Per chiudere le opportunità
È possibile chiudere le opportunità una volta concluse le negoziazioni. Quando si chiude un'opportunità, è possibile specificare se è stata vinta o persa e i motivi per chiuderla. Per specificare un motivo, è necessario impostare codici di chiusura opportunità.

1. Nella finestra **Lista opportunità** selezionare l'opportunità e scegliere l'azione **Chiudi**. Verrà visualizzata la finestra **Chiudi opportunità**.
2. Compilare i campi appropriati e fare clic sul pulsante **OK**.

   I campi **Codice opportunità chiuse** e **Data di chiusura** sono obbligatori e devono essere compilati prima di selezionare il pulsante **OK**.

   Nel campo **Codice opportunità chiuse**, è possibile scegliere tra i codici chiusura opportunità esistenti o aggiungere un nuovo codice. Per aggiungere un nuovo codice, dall'elenco a discesa, selezionare **Seleziona da elenco completo** quindi **Nuovo**. Nella nuova riga vuota, compilare i campi **Codice**, **Tipo** e **Descrizione** e quindi il pulsante **OK**.

## <a name="to-create-quotes-for-opportunities"></a>Per creare offerte per opportunità
È possibile creare offerte di vendita relative ai contatti che non sono registrati come clienti.

1. Nella finestra **Lista opportunità** selezionare l'opportunità e scegliere l'azione **Assegna offerta di vendita**. Verrà visualizzata la finestra **Offerta di vendita**.
2. Compilare i relativi campi.

## <a name="to-create-sales-orders-for-opportunities"></a>Per creare ordini di vendita per opportunità
È possibile creare ordini di vendita a partire dalle offerte di vendita create per le opportunità. Prima di creare ordini di vendita per i contatti, è necessario creare il contatto come cliente. Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Nella finestra **Lista opportunità** individuare l'opportunità per la quale è stata creata un'offerta di vendita.
2. Scegliere l'azione **Assegna offerta di vendita**. Verrà visualizzata la finestra **Offerta vendita** per visualizzare l'offerta di vendita assegnata all'opportunità.
3. Compilare i campi aggiuntivi, quindi scegliere l'azione **Crea ordine**.

Quando si gestiscono opportunità di vendita, potrebbe essere necessario creare un'offerta per il contatto al quale è collegata l'opportunità.

## <a name="to-delete-opportunities"></a>Per rimuovere opportunità
È possibile rimuovere opportunità, ad esempio dopo aver concluso un'operazione commerciale. Tuttavia, è possibile eliminare solo le opportunità chiuse. Esistono due modi per eliminare le opportunità chiuse. È possibile eliminare le opportunità chiuse dalla finestra **Lista opportunità** oppure è possibile eseguire il processo batch **Elimina opportunità chiuse** per eliminare più opportunità in base a criteri specifici.

Per eliminare le opportunità chiuse nella finestra **Lista opportunità**, selezionare l'opportunità quindi selezionare l'azione **Elimina**.

Per eliminare le opportunità chiuse utilizzando il processo batch **Elimina opportunità chiuse**, attenersi alla seguente procedura:

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Rimuovi opportunità** e quindi scegliere il collegamento correlato.
2. Nella sezione **Opportunità**, impostare i filtri che specificano le opportunità chiuse eliminare.
3. Scegliere il pulsante **OK**.

Una volta eliminata un'opportunità, verrà rimossa dalla finestra **Lista opportunità**.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Per spostare un'opportunità nelle fasi ciclo di vendita
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

