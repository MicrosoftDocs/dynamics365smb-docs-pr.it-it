---
title: Personalizzazione delle pagine | Documenti Microsoft
description: Informazioni su come personalizzare l'interfaccia utente in base alle esigenze professionali in Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253725"
---
# <a name="personalizing-your-workspace"></a>Personalizzazione dell'area di lavoro

È possibile *personalizzare* l'area di lavoro per adattarla alle esigenze professionali e alle preferenze modificando le pagine in modo da visualizzare solo le informazioni necessarie, quando necessario. Le modifiche di personalizzazione apportate influenzeranno solo ciò che vede l'utente che le ha effettuate, non quello che altri utenti vedono.

A seconda del tipo di pagina e del relativo contenuto, è possibile eseguire varie task, come spostare o nascondere campi, colonne e azioni, spostare e nascondere intere parti e altro ancora.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Oltre a ciò che gli utenti possono personalizzare, gli amministratori e i super utenti possono sostituire la personalizzazione degli utenti e definire quali funzionalità sono accessibili in tutte le società o alcune specifiche. Per ulteriori informazioni, vedere [Personalizzazione di Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Per personalizzare una pagina

1. Nell'angolo in alto a destra, selezionare l'icona ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente") e quindi scegliere **Personalizza**.

    Viene visualizzato il banner **Personalizzazione** in alto per indicare che è possibile iniziare ad apportare le modifiche.

    ![Modalità di personalizzazione](media/ui_personalize_mode_small.png "Modalità di personalizzazione")

2. Andare alla pagina da personalizzare.

    Se nel banner viene visualizzato ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") oppure ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata"), non è possibile personalizzare la pagina. Per ulteriori informazioni, vedere [Perché non è possibile personalizzare una pagina](ui-personalization-locked.md).

3. Specificare un'area che si desidera personalizzare, ad esempio un'intestazione di colonna o campo in un elenco. Tutti gli elementi che è possibile personalizzare vengono immediatamente evidenziati con una freccia o un bordo. Vedere [sezione successiva](#What) per dettagli su ciò che è possibile fare.

4. È possibile continuare a modificare la stessa pagina o aprire un'altra pagina. Le modifiche vengono salvate automaticamente mentre le si apporta. Al termine, nel banner **Personalizzazione**, scegliere **Chiudi**.

## <a name="What"></a>Elementi personalizzabili

|Operazione da eseguire|Procedura|Osservazioni|
|----|------------|-------|
|Spostare qualcosa, come un campo, una colonna dell'elenco, un riquadro, un'azione o una parte|Fare clic in un punto qualsiasi dell'elemento che si desidera spostare e trascinarlo nella nuova posizione. La posizione è indicata da una spessa linea orizzontale o verticale.<br /><br />![Icona Impossibile spostare qui](media/personalization-cannot-move-here.png "Modalità di personalizzazione - Icona Impossibile spostare qui") indica che non è possibile spostare l'elemento nella posizione selezionata.|Le parti sono suddivisioni o aree in una pagina che contengono elementi quali più campi, un'altra pagina, un grafico o dei riquadri.<br /><br />Per ulteriori dettagli sulla personalizzazione di azioni, vedere la [sezione successiva](ui-personalization-user.md#Actions). |
|Nascondere qualcosa, come un campo, una colonna dell'elenco o una parte.|Selezionare la freccia e scegliere <b>Nascondi</b>.|Se il campo che si nasconde è visualizzato anche nell'intestazione della Scheda dettaglio quando questa è compressa, il campo non verrà più visualizzato.|
|Aggiungere un campo o una colonna.|Nel banner <b>Personalizzazione</b> scegliere <b>Altro</b> quindi scegliere <b>Campo</b>.<br /></br>Si apre a destra il riquadro <b>Aggiungi campo a pagina</b>. Elenca i campi che possono essere aggiunti nella pagina.<br /><br />Per aggiungere un campo, trascinarlo dal riquadro alla posizione che si desidera. La posizione è indicata da una spessa linea orizzontale o verticale.|Ogni pagina include una serie di campi predefiniti che è possibile visualizzare. Utilizzare questa procedura per aggiungere campi o colonne che non sono state visualizzate precedentemente o per visualizzare campi che sono stati nascosti.|
|Visualizzare un campo nell'intestazione di un Scheda dettaglio quando questa è compressa.|Selezionare la freccia e scegliere <b>Mostra quando compresso</b>. <br /> <br />Se questa opzione non è visualizzata, è già impostata. In questo caso, per smettere di visualizzare il campo nell'intestazione della Scheda dettaglio, scegliere <b>Mostra sempre</b>.|*Scheda dettaglio* è il termine utilizzato per un gruppo di campi visualizzati sotto un'intestazione comune. Utilizzare l'opzione <b>Mostra quando compresso</b> per visualizzare i campi più importanti. Se si seleziona un campo nell'intestazione, la Scheda dettaglio verrà visualizzata e lo stato attivo sarà sul campo selezionato.<br /><br />Questa opzione è applicabile solo se una pagina ha più di una Scheda dettaglio. Se vi è una sola Scheda dettaglio, può non essere compressa, per cui l'opzione <b>Mostra quando compresso</b> non è disponibile.|
|Visualizzare un campo solo quando si seleziona **Mostra di più**.|Selezionare la freccia e scegliere <b>Visualizza in "Mostra più"</b>. <br /> <br />Se l'opzione <b>Visualizza in "Mostra più"</b> non è visualizzata, è già impostata. In tal caso, per visualizzare sempre un campo e non solo quando si seleziona **Mostra di più**, scegliere <b>Mostra sempre</b>.||
|Modificare il riquadro di blocco di un elenco in un'altra colonna. |Selezionare la freccia della colonna che si desidera come ultima colonna del riquadro di blocco, quindi scegliere <b>Imposta Blocca riquadro</b>.<br /><br/>Se si desidera impostare il riquadro di blocco di nuovo sulla posizione originale, selezionare la freccia per la colonna corrente del blocco e scegliere <b>Cancella Blocca riquadro</b>. Nota: non è possibile rimuovere il riquadro di blocco.|Il riquadro di blocco specifica le colonne che sono sempre visualizzate a sinistra, anche quando si scorre orizzontalmente.|  
|Modificare la larghezza di una colonna.|Nella riga dell'intestazione della tabella, trascinare il bordo destro della colonna. <br /><br />Per massimizzare la larghezza della colonna in base alla riga di testo più lunga nella colonna, fare doppio clic sul bordo destro.||
|Ignorare un campo quando si preme INVIO.|Selezionare la freccia accanto al campo, o l'intestazione di una colonna in un elenco, e scegliere **Escludi da Accesso rapido**. <br /><br /> Se questa opzione non è visualizzata, il campo è già impostato per essere ignorato. In tal caso, per smettere di ignorare il campo, scegliere **Includi in Accesso rapido**. |Vedere [Accelerazione dell'immissione di dati utilizzando Accesso rapido](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Personalizzazione delle azioni

È possibile personalizzare la barra delle azioni che si trova nella parte superiore della pagina, come indicato dall'area evidenziata nella seguente illustrazione.

![Personalizzare la barra delle azioni](media/personalize-action-bar.png "Personalizzare la barra delle azioni")

La personalizzazione consente di specificare quali azioni visualizzare nella barra delle azioni e dove. È possibile visualizzare, nascondere o spostare singole azioni o gruppi di azioni. La personalizzazione della barra delle azioni è praticamente uguale a quella degli altri elementi dell'area di lavoro. Tuttavia, ciò che è possibile eseguire esattamente con un'azione o un gruppo dipende dalla posizione dell'azione o del gruppo nella barra delle azioni. Il modo migliore per saperlo è di provare e di seguire le istruzioni visualizzate. Le sezioni successive forniscono informazioni sulle personalizzazione della barra delle azioni.

### <a name="action-bar-overview"></a>Panoramica sulla barra delle azioni

Per comprendere meglio la personalizzazione delle azioni, è necessario avere una certa familiarità con alcuni termini, ovvero *gruppo di azioni* e *categoria promossa*.  

Un *gruppo di azioni* è un elemento che si espande per visualizzare altre azioni o gruppi. Ad esempio, nell'illustrazione seguente, **Registrazione** è un gruppo di azioni.

Una *categoria promossa* è un gruppo di azioni visualizzato tra due righe verticali `|` nella barra delle azioni. Le categorie includono in genere le azioni più utilizzate, affinché sia possibile trovarle rapidamente. Ad esempio, nell'illustrazione seguente, **Rilascio**, **Registrazione**, **Fattura** e **Naviga** sono categorie promosse.

![Personalizzare un gruppo della barra di azioni](media/personalize-action-bar-group-clip.png "Personalizzare un gruppo della barra delle azioni")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Per eliminare, nascondere e visualizzare azioni e gruppi

Per visualizzare o nascondere un'azione o un gruppo di azioni, selezionarlo e quindi scegliere una delle seguenti opzioni:

|Opzione|Funzione|
|------|------------
|**Elimina**|Questa opzione viene visualizzata se l'azione selezionata è visibile anche altrove nella barra delle azioni. La scelta di questa opzione elimina l'azione dalla posizione selezionata di modo che non sia più visualizzata. L'azione o il gruppo di azioni sarà visibile in altre posizioni. |
|**Nascondi**|Questa opzione viene visualizzata se l'azione o il gruppo di azioni non si trova in altre parti della barra delle azioni. Come per **Elimina**, la scelta di questa opzione rimuoverà l'azione o il gruppo di azioni dalla barra delle azioni. Tuttavia, nella modalità di personalizzazione, l'azione o il gruppo di azioni sarà ancora visualizzato nella posizione corrente, ma sarà inattivo.|
|**Mostra**|Questa opzione viene visualizzata se l'azione o il gruppo di azioni è stato nascosto (inattivo). La scelta di questa opzione visualizzerà l'azione o il gruppo di azioni nella barra delle azioni.|

### <a name="to-move-actions-and-action-groups"></a>Per spostare azioni e gruppi di azioni

Per spostare un azione o un gruppo di azioni, trascinarlo nella posizione desiderata, esattamente come campi e colonne.

La posizione in cui è possibile spostare l'azione o i gruppi di azioni è indicata da una riga orizzontale tra le azioni o da un bordo intorno a un gruppo di azioni.

- È possibile spostare singole azioni nelle categorie promosse, ma non è possibile riorganizzare l'ordine delle azioni nella categoria.
- Non è possibile spostare un gruppo di azioni in una categoria promossa.
- Per spostare un'azione o un gruppo di azioni in un altro gruppo di azioni che è vuoto, trascinare l'azione o il gruppo di azioni sul nuovo gruppo e rilasciarlo nella casella **Rilasciare qui un'azione**.

## <a name="additional-points-of-interest"></a>Ulteriori punti di interesse

Per agevolare la comprensione della personalizzazione, di seguito sono elencati alcuni puntatori.

- Quando si apportano modifiche a una pagina schede avviata da un elenco, le modifiche diventeranno effettive in tutti i record a cui si accede dalla lista. Ad esempio, si apre un cliente specifico da una pagina elenco Clienti e quindi si personalizza la pagina aggiungendo un campo. Quando si aprono altri clienti dall'elenco, il campo aggiunto verrà visualizzato anche per questi clienti.
- Le modifiche effettuate diventeranno effettive in tutte le Gestioni ruolo utente. Ad esempio, se si effettua una modifica all'elenco Cliente quando la Gestione ruolo utente è impostata su Manager aziendale, le modifiche verranno visualizzate anche nell'elenco cliente quando Gestione ruolo utente è impostata su Gestore ordini vendite.
- Le modifiche a una pagina in un riquadro diventeranno effettive nella pagina ovunque viene visualizzata.  
- È possibile aggiungere solo i campi e le colonne da una lista predefinita, che è basata sulla pagina. Non è possibile creare nuovi campi.

## <a name="to-clear-personalization"></a>Per cancellare la personalizzazione

In alcuni casi, potrebbe essere necessario annullare alcune o tutte le modifiche di personalizzazione effettuate nel tempo in una pagina. A questo proposito, nel banner **Personalizzazione** scegliere **Altro**, **Cancella personalizzazione** e quindi scegliere una delle opzioni seguenti Tenere presente che la cancellazione di una personalizzazione non può essere annullata.

|Opzione|Funzione|
|------|------------
|Solo azioni|Cancella qualsiasi modifica di personalizzazione alla barra delle azioni nella pagina.|
|Tutto tranne le azioni|Cancella qualsiasi modifica di personalizzazione alla pagina salvo quelle nella barra delle azioni Sono incluse le modifiche a campi, colonne, parti e riquadri. |
|Tutto|Cancella tutte le modifiche di personalizzazione alla pagina per ripristinarne l'aspetto originale. Sono incluse le modifiche alla barra delle azioni, a campi, colonne, parti e riquadri.|

## <a name="see-also"></a>Vedere anche

[Gestione della personalizzazione](ui-personalization-manage.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
