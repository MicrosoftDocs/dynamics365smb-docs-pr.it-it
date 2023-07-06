---
title: Personalizzazione delle pagine (video)
description: Informazioni su come personalizzare l'interfaccia utente e l'area di lavoro in base alle tue esigenze e preferenze professionali in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 10/11/2022
ms.author: bholtorf
---
# <a name="personalize-your-workspace"></a><a name="personalize-your-workspace"></a><a name="personalize-your-workspace"></a>Personalizzare l'area di lavoro

Puoi personalizzare l'area di lavoro per adattarla alle tue preferenze di lavoro. Modifica le pagine in modo che mostrino solo le informazioni di cui hai bisogno e dove ne hai bisogno. La personalizzazione riguarda solo la tua area di lavoro. Non cambia il modo in cui lavorano gli altri.

È possibile personalizzare tutti i tipi di pagine, inclusa la pagina Gestione ruolo utente. Per ulteriori informazioni su Gestione ruolo utente, vai a [Gestione ruolo utente](ui-change-basic-settings.md#role-center).  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Puoi eseguire varie modifiche, come spostare o nascondere campi, colonne, azioni e intere parti e aggiungere nuovi campi. La maggior parte della personalizzazione deve essere eseguita attivando prima il banner **Personalizzazione**. Puoi apportare semplici rettifiche, come la larghezza della colonna, immediatamente su qualsiasi elenco.

> [!NOTE]
> Gli amministratori possono eseguire le stesse modifiche al layout degli utenti personalizzando l'area di lavoro per un profilo a cui sono assegnati più utenti. Per saperne di più sulle pagine per i ruoli, vai a [Personalizzare le pagine per i ruoli](ui-personalization-manage.md)<br /><br />
Gli amministratori possono anche sostituire o disabilitare la personalizzazione degli utenti e definire quali funzionalità sono visualizzabili in tutte o alcune società. Per ulteriori informazioni, vedere [Personalizzazione di Business Central](ui-customizing-overview.md).

## <a name="video"></a><a name="video"></a><a name="video"></a>Video

Il video seguente mostra alcuni dei modi per personalizzare il Centro gestione ruoli.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column"></a><a name="to-change-the-width-of-a-column"></a><a name="to-change-the-width-of-a-column"></a>Per modificare la larghezza di una colonna

Puoi facilmente ridimensionare le colonne di qualsiasi elenco. Basta che trascini il bordo tra due colonne verso destra o sinistra.  

1. Nell'intestazione di un elenco, selezionare e trascinare il bordo tra 2 colonne.
2. In alternativa, fare doppio clic sul bordo tra due colonne per adattare automaticamente la larghezza della colonna. La larghezza si regola sulla dimensione ottimale per la migliore leggibilità.

Come per altre personalizzazioni, le modifiche apportate alla larghezza della colonna vengono archiviate nel proprio account e sono visibili indipendentemente dal dispositivo utilizzato.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a><a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a><a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>Per avviare la personalizzazione di una pagina tramite il banner **Personalizzazione**

1. Aprire qualsiasi pagina da personalizzare.
2. Nell'angolo in alto a destra seleziona l'icona ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") e poi scegli l'azione **Personalizza**.

    Viene visualizzato il banner **Personalizzazione** in alto per indicare che è possibile iniziare ad apportare le modifiche.

    > [!NOTE]
    > Per navigare durante la personalizzazione, utilizzare CTRL+clic su un'azione se è evidenziata dalla freccia.

    Se nel banner viene visualizzato ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") oppure ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata"), non è possibile personalizzare la pagina. Per ulteriori informazioni, vedi [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).

3. Per aggiungere un campo, scegliere l'azione **+ Filtro**.
4. Dal riquadro **Aggiungi campo a pagina**, trascinare e rilasciare un campo nella posizione desiderata nella pagina.
5. Per modificare un elemento dell'interfaccia utente, puntare all'elemento, ad esempio un'azione, un campo o una parte. L'elemento viene immediatamente evidenziato con una freccia o un bordo.
6. Scegliere l'elemento, quindi scegliere **Sposta**, **Rimuovi**, **Nascondi**, **Mostra**, **Visualizza in "Mostra più"**, **Mostra quando compresso**, **Mostra sempre**, **Imposta/Cancella Blocco riquadro** o **Includi/Escludi da Accesso rapido**, a seconda del tipo e dello stato dell'elemento dell'interfaccia utente. Per ulteriori informazioni, vedere [Elementi personalizzabili](#What).
7. Al termine della modifica del layout in una o più pagine, selezionare il pulsante **Fatto** nel banner **Personalizzazione**.

## <a name="what-you-can-personalize"></a><a name="what-you-can-personalize"></a><a name="what-you-can-personalize"></a><a name="What"></a>Elementi personalizzabili

|Operazione da eseguire|Procedura|Osservazioni|
|----|------------|-------|
|Spostare qualcosa, come un campo, una colonna dell'elenco, un riquadro, un'azione o una parte|Fare clic in un punto qualsiasi dell'elemento che si desidera spostare e trascinarlo nella nuova posizione. La posizione è indicata da una spessa linea orizzontale o verticale.<br /><br />![L'icona Impossibile spostare qui](media/personalization-cannot-move-here.png "Modalità di personalizzazione - Impossibile spostare l'icona qui") indica che non è possibile spostare l'elemento nella posizione selezionata.|Le parti sono suddivisioni o aree in una pagina che contengono elementi quali più campi, un'altra pagina, un grafico o dei riquadri.<br /><br />Per ulteriori informazioni sulla personalizzazione di azioni, vedi [Personalizzazione delle azioni](ui-personalization-user.md#Actions). |
|Nascondere qualcosa, come un campo, una colonna in un elenco, un riquadro, un'azione o una parte.|Selezionare la freccia e quindi <b>Nascondi</b>.|L'elemento è grigio quando è attivata la modalità di personalizzazione. Se il campo che si nasconde è visualizzato anche nell'intestazione della Scheda dettaglio quando questa è compressa, il campo non verrà più visualizzato.|
|Mostrare azioni e parti nascosti.|Per un elemento in grigio (nascosto), selezionare la freccia, quindi scegliere <b>Mostra</b>.|L'elemento nascosto è di nuovo visibile.|
|Aggiungere un campo o una colonna.|Nel banner <b>Personalizzazione</b>, scegliere l'azione <b>+ Campo</b>.<br /></br>Si apre a destra il riquadro <b>Aggiungi campo a pagina</b>. Elenca i campi che possono essere aggiunti nella pagina.<br /><br />Per aggiungere un campo, trascinarlo dal riquadro alla posizione che si desidera. La posizione è indicata da una spessa linea orizzontale o verticale.|Ogni pagina include una serie di campi predefiniti che è possibile visualizzare. Utilizza questa procedura per aggiungere campi o colonne che non sono state visualizzate precedentemente o per visualizzare campi che sono stati nascosti.|
|Visualizza un campo nell'intestazione di un Scheda dettaglio quando questa è compressa.|Selezionare la freccia e quindi <b>Mostra quando compresso</b>. <br /> <br />Se questa opzione non è visibile, è già impostata. In questo caso, per smettere di visualizzare il campo nell'intestazione della Scheda dettaglio, scegliere <b>Mostra sempre</b>.|*Scheda dettaglio* è il termine utilizzato per un gruppo di campi visualizzati sotto un'intestazione comune. Utilizzare l'opzione <b>Mostra quando compresso</b> per visualizzare i campi più importanti. Se si seleziona un campo nell'intestazione, la Scheda dettaglio verrà visualizzata e lo stato attivo sarà sul campo selezionato.<br /><br />Questa opzione è applicabile solo se una pagina ha più di una Scheda dettaglio. Se vi è una sola Scheda dettaglio, può non essere compressa, per cui l'opzione <b>Mostra quando compresso</b> non è disponibile.|
|Visualizzare un campo solo quando si seleziona **Mostra di più**.|Selezionare la freccia e quindi <b>Visualizza in "Mostra più"</b>. <br /> <br />Se l'opzione <b>Visualizza in "Mostra più"</b> non è visibile, è già impostata. In tal caso, per visualizzare sempre un campo e non solo quando si seleziona **Mostra di più**, scegliere <b>Mostra sempre</b>.||
|Modificare il riquadro di blocco di un elenco in un'altra colonna. |Selezionare la freccia della colonna che si desidera come ultima colonna del riquadro di blocco, quindi scegliere <b>Imposta Blocca riquadro</b>.<br /><br/>Se si desidera impostare il riquadro di blocco di nuovo sulla posizione originale, selezionare la freccia per la colonna corrente del blocco e scegliere <b>Cancella Blocca riquadro</b>. Nota: non puoi rimuovere il riquadro di blocco.|Il riquadro di blocco specifica le colonne che sono sempre visualizzate a sinistra, anche quando si scorre orizzontalmente.|  
|Ignorare un campo quando si preme INVIO.|Selezionare la freccia accanto al campo, o l'intestazione di una colonna in un elenco, e scegliere **Escludi da Accesso rapido**. <br /><br /> Se questa opzione non è visibile, il campo è già impostato per essere ignorato. In tal caso, per smettere di ignorare il campo, scegliere **Includi in Accesso rapido**. |Vedere [Accelerazione dell'immissione di dati utilizzando Accesso rapido](ui-enter-data.md#QuickEntry)|
|Riordinare e rimuovere visualizzazioni che rappresentano elenchi filtrati.|Scegliere la freccia accanto a una visualizzazione, quindi scegliere **Sposta**, **Rimuovi** o **Nascondi**.|Vedere [Salvare e personalizzare visualizzazioni elenco](ui-views.md).|  
|Aggiungere una nuova azione a una pagina o un report in Gestione ruolo utente.|Dalla pagina di destinazione, dalla pagina della richiesta di report o dalla finestra della funzionalità delle informazioni, selezionare l'icona del segnalibro.|Vedere [Aggiungere un segnalibro a una pagina o un report in Gestione ruolo utente](ui-bookmarks.md)|
|Avvia sempre un elenco come espanso o compresso|Scegli il pulsante **Espandi tutto** o **Comprimi tutto** nell'angolo in alto a sinistra dell'elenco. In alternativa, scegli l'azione **Espandi tutto** o **Comprimi tutto** nel menu della prima colonna. |Si applica agli elenchi di gerarchie comprimibili.|

## <a name="personalizing-the-action-bar-and-menus"></a><a name="personalizing-the-action-bar-and-menus"></a><a name="personalizing-the-action-bar-and-menus"></a><a name="Actions"></a>Personalizzazione della barra delle azioni e dei menu

La personalizzazione consente di specificare quali azioni visualizzare nelle barre di spostamento e azione e in Gestione ruolo utente e dove. È possibile visualizzare, nascondere o spostare singole azioni o gruppi di azioni.

Il video seguente mostra come personalizzare le azioni sulle pagine e su Gestione ruolo utente.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

La personalizzazione delle barre di spostamento e azione è praticamente uguale a quella degli altri elementi dell'interfaccia di lavoro. Tuttavia, ciò che è possibile eseguire con un'azione o un gruppo dipende dalla posizione dell'azione o del gruppo. Il modo migliore per saperlo è di attivare la modalità di personalizzazione e di seguire le istruzioni visualizzate.

Per comprendere meglio la personalizzazione delle azioni, è necessario avere una certa familiarità con alcuni termini, ovvero *gruppo di azioni* e *categoria promossa*.  

Un *gruppo di azioni* è un elemento che si espande per visualizzare altre azioni o gruppi. Ad esempio, nella pagina **Ordini vendita**, l'azione **Funzioni** che viene visualizzata quando scegli l'azione **Azioni** è un gruppo di azioni.

Una *categoria promossa* è un gruppo di azioni visualizzato prima della riga verticale `|` nella barra delle azioni. Le categorie includono in genere le azioni più utilizzate, affinché sia possibile trovarle rapidamente. Ad esempio, nella pagina **Ordini vendita**, le azioni **Ordine**, **Rilascia** e **Registrazione**, le azioni sono categorie promosse.

> [!NOTE]  
> Per cancellare la personalizzazione, seleziona la freccia del menu progettazione della parte, quindi scegli **Cancella personalizzazione**.

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a><a name="to-remove-hide-and-show-actions-and-action-groups"></a><a name="to-remove-hide-and-show-actions-and-action-groups"></a>Per rimuovere, nascondere e visualizzare azioni e gruppi di azioni

Quando si desidera mostrare o nascondere un'azione, le opzioni sotto la freccia definiscono le operazioni consentite in base allo stato dell'azione. 

1. Scegliere la punta per un'azione o per un gruppo di azioni.
2. Selezionare una delle seguenti opzioni:

|Opzione|Funzione|
|------|------------
|**Elimina**|Questa opzione viene visualizzata se l'azione selezionata è visibile anche altrove nella barra di spostamento o azione. La scelta di questa opzione elimina l'azione dalla posizione selezionata di modo che non sia più visualizzata. L'azione o il gruppo di azioni sarà visibile in altre posizioni. |
|**Nascondi**|Questa opzione viene visualizzata se l'azione o il gruppo di azioni non si trova altrove nella barra di spostamento o delle azioni. Come per **Elimina**, la scelta di questa opzione rimuoverà l'azione o il gruppo di azioni dalla barra di spostamento o delle azioni. Tuttavia, in modalità di personalizzazione, l'azione o il gruppo di azioni sarà ancora visualizzato nella posizione corrente, ma sarà inattivo.|
|**Mostra**|Questa opzione viene visualizzata se l'azione o il gruppo di azioni è stato nascosto (inattivo). La scelta di questa opzione visualizzerà l'azione o il gruppo di azioni nella barra di spostamento o delle azioni.|

### <a name="to-move-actions-and-action-groups"></a><a name="to-move-actions-and-action-groups"></a><a name="to-move-actions-and-action-groups"></a>Per spostare azioni e gruppi di azioni

La posizione in cui è possibile spostare l'azione o i gruppi di azioni è indicata da una riga orizzontale tra le due azioni o da un bordo intorno a un gruppo di azioni. Sono presenti le seguenti limitazioni:

- Puoi spostare singole azioni nelle categorie promosse, ma non è possibile riorganizzare l'ordine delle azioni nella categoria.
- Non è possibile spostare un gruppo di azioni in una categoria promossa.

1. Per spostare un azione o un gruppo di azioni, trascinarlo nella posizione desiderata, esattamente come per campi e colonne.
2. Per spostare un'azione o un gruppo di azioni in un altro gruppo di azioni che è vuoto, trascinare l'azione o il gruppo di azioni sul nuovo gruppo e rilasciarlo nella casella **Rilasciare qui un'azione**.

## <a name="personalizing-parts"></a><a name="personalizing-parts"></a><a name="personalizing-parts"></a><a name="Parts"></a>Personalizzazione delle parti

Le parti sono aree di una pagina che in genere sono composte da più campi, grafici o altro contenuto. Una parte mostra un bordo colorato quando viene attivata. Ad esempio, una schermata iniziale di Gestione ruolo utente ha più parti. A causa del contorno ben definito, puoi personalizzare l'intera parte e il suo contenuto.

- Per spostare una parte, trascinala e rilasciala nella posizione desiderata. Una linea colorata indica posizioni valide sullo schermo. Ad esempio, i riquadri Dettaglio informazioni possono essere spostati solo accanto ad altri riquadri Dettaglio informazioni nel riquadro Dettaglio informazioni.
- Puoi nascondere una parte scegliendo l'opzione **Nascondi** sotto la freccia.
- Quando inizi a personalizzare o vai a una nuova pagina, tutte le parti che sono attualmente nascoste appariranno sulla pagina con elementi visivi distintivi per indicare che sono nascoste. Puoi visualizzare la parte scegliendo l'opzione **Mostra** sotto la freccia.

Puoi cancellare tutte le modifiche di personalizzazione che hai apportato all'interno di una singola parte scegliendo l'opzione **Cancella personalizzazione** sotto la freccia della parte. L'annullamento della personalizzazione di una parte influisce solo sulle modifiche ai contenuti della parte, non sul posizionamento o sulla visibilità della parte nella pagina.  

## <a name="to-clear-personalization"></a><a name="to-clear-personalization"></a><a name="to-clear-personalization"></a>Per cancellare la personalizzazione

In alcuni casi, potrebbe essere necessario annullare alcune o tutte le modifiche di personalizzazione effettuate nel tempo in una pagina.

1. Nel banner **Personalizzazione**, scegliere l'azione **Cancella personalizzazione**.
2. Selezionare una delle seguenti opzioni.  

> [!CAUTION]
> La cancellazione di una personalizzazione non può essere annullata.

|Opzione|Funzione|
|------|------------
|**Solo menu di navigazione**|Cancella tutte le modifiche di personalizzazione che apportate al menu di navigazione condiviso in Gestione ruolo utente e in altre pagine. Tali modifiche includono tutte le nuove azioni che sono state aggiunte come segnalibri e qualsiasi modifica ai collegamenti e ai gruppi nel menu.|  
|**Solo azioni**|Cancella qualsiasi modifica di personalizzazione alla barra di spostamento o delle azioni nella pagina.|
|**Solo campi e colonne**|Cancella qualsiasi modifica di personalizzazione alla pagina salvo quelle nella barra di spostamento o delle azioni. Sono incluse le modifiche a campi, colonne, parti e riquadri. |
|**Tutto**|Cancella tutte le modifiche di personalizzazione alla pagina per ripristinarne l'aspetto originale. Sono incluse le modifiche alla barra di spostamento o delle azioni, a campi, colonne, parti e riquadri.|

## <a name="other-points-of-interest"></a><a name="other-points-of-interest"></a><a name="other-points-of-interest"></a>Altri punti di interesse

Per agevolare la comprensione della personalizzazione, di seguito sono elencati alcuni puntatori.

- Quando si apportano modifiche a una pagina schede avviata da un elenco, le modifiche diventeranno effettive in tutti i record a cui si accede dalla lista. Ad esempio, si apre un cliente specifico da una pagina elenco Clienti e quindi si personalizza la pagina aggiungendo un campo. Quando si aprono altri clienti dall'elenco, il campo aggiunto verrà visualizzato anche per questi clienti.
- Le modifiche effettuate diventeranno effettive in tutte le Gestioni ruolo utente. Ad esempio, se si effettua una modifica all'elenco Cliente quando la Gestione ruolo utente è impostata su Manager aziendale, le modifiche verranno visualizzate anche nella pagina **Clienti** quando Gestione ruolo utente è impostato su Gestore ordini vendite.
- Le modifiche a una pagina in un riquadro diventeranno effettive nella pagina ovunque viene visualizzata.  
- È possibile aggiungere solo i campi e le colonne da una lista predefinita, che è basata sulla pagina. Non è possibile creare nuovi campi.
- La voce **Power Automate** nella barra delle azioni
  - Non puoi nascondere o spostare la voce **Automatizza** o la voce secondaria **Power Automate** e le relative azioni **Crea un flusso** e **Gestisci flussi**.
  - Puoi spostare i flussi inclusi sotto l'elemento **Automatizza**, ma non puoi nasconderli usando la personalizzazione. Lo spostamento del flusso crea una copia del flusso nella destinazione, non lo rimuoverà dall'elemento **Automatizza**.

   > [!TIP]
   > In qualità di amministratore, puoi nascondere l'elemento **Automatizza** per gli utenti. Ulteriori informazioni in [Configurare l'integrazione di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedi anche
[Personalizzare pagine per profili](ui-personalization-manage.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
