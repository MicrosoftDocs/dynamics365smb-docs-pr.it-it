---
title: Personalizzazione delle pagine (video)
description: Informazioni su come personalizzare l'interfaccia utente e l'area di lavoro in base alle tue esigenze e preferenze professionali in Business Central.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 09/14/2023
ms.author: jswymer
---
# Personalizza l'area di lavoro

Puoi personalizzare l'area di lavoro per adattarla alle tue preferenze di lavoro. Modifica le pagine in modo che mostrino solo le informazioni di cui hai bisogno e dove ne hai bisogno. La personalizzazione riguarda solo la tua area di lavoro. Non cambia il modo in cui lavorano gli altri. Puoi personalizzare tutti i tipi di pagine, inclusa la pagina [Gestione ruolo utente](ui-change-basic-settings.md#role-center). 

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Puoi eseguire varie modifiche, come spostare o nascondere campi, colonne, azioni e intere parti e aggiungere nuovi campi. La maggior parte della personalizzazione deve essere eseguita attivando prima il banner **Personalizzazione**. Puoi apportare semplici rettifiche, come la larghezza della colonna, immediatamente su qualsiasi elenco.

> [!NOTE]
> Gli amministratori possono eseguire le stesse modifiche al layout degli utenti personalizzando un profilo (ruolo) a cui sono assegnati più utenti. Per saperne di più sulle pagine per i ruoli, vai a [Personalizzare le pagine per i ruoli](ui-personalization-manage.md)<br /><br />
Gli amministratori possono anche sostituire o disabilitare la personalizzazione degli utenti e definire quali funzionalità sono visualizzabili in tutte o alcune società. Per ulteriori informazioni, vedere [Personalizzazione di Business Central](ui-customizing-overview.md).

## Video

Il video seguente mostra alcuni dei modi per personalizzare il Centro gestione ruoli.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## Modificare la larghezza di una colonna

Puoi facilmente ridimensionare le colonne di qualsiasi elenco. Basta che trascini il bordo tra due colonne verso destra o sinistra.  

1. Nell'intestazione di un elenco, selezionare e trascinare il bordo tra 2 colonne.
2. In alternativa, fai doppio clic sul bordo tra due colonne per adattare automaticamente la larghezza della colonna. La larghezza si regola sulla dimensione ottimale per la migliore leggibilità.

Come per altre personalizzazioni, le modifiche apportate alla larghezza della colonna vengono archiviate nel proprio account e sono visibili indipendentemente dal dispositivo utilizzato.

## Iniziare a personalizzare utilizzando la modalità di personalizzazione

1. Aprire qualsiasi pagina da personalizzare.
1. Nell'angolo in alto a destra seleziona l'icona ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") e poi scegli l'azione **Personalizza**.

    Viene visualizzato il banner **Personalizzazione** in alto per indicare che è possibile iniziare ad apportare le modifiche.

    > [!NOTE]
    > Per navigare durante la personalizzazione, utilizza <kbd>CTRL</kbd>+<kbd>+clic<kbd> su un'azione se è evidenziata dalla freccia.

    Se nel banner viene visualizzato ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") oppure ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata"), non è possibile personalizzare la pagina. Per ulteriori informazioni, vedi [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).

1. Per modificare un elemento dell'interfaccia utente, puntare all'elemento, ad esempio un'azione, un campo o una parte. L'elemento viene immediatamente evidenziato con una freccia o un bordo. Scegliere l'elemento, quindi scegliere **Sposta**, **Rimuovi**, **Nascondi**, **Mostra**, **Visualizza in "Mostra più"**, **Mostra quando compresso**, **Mostra sempre**, **Imposta/Cancella Blocco riquadro** o **Includi/Escludi da Accesso rapido**, a seconda del tipo e dello stato dell'elemento dell'interfaccia utente.
1. Per aggiungere un campo, scegliere l'azione **+ Filtro**. Dal riquadro **Aggiungi campo a pagina**, trascinare e rilasciare un campo nella posizione desiderata nella pagina.
1. Al termine della modifica del layout in una o più pagine, selezionare il pulsante **Fatto** nel banner **Personalizzazione**.

Per ulteriori informazioni, vedere [Elementi personalizzabili](#What).

## <a name="What"></a>Elementi personalizzabili

|Operazione da eseguire|Procedura|Osservazioni|
|----|------------|-------|
|Spostare qualcosa, come un campo, una colonna dell'elenco, un riquadro, un'azione o una parte in un'altra posizione nella pagina|Fai clic in un punto qualsiasi dell'elemento che desideri spostare e trascinalo nella nuova posizione. Una spessa linea orizzontale o verticale indica la posizione.<br /><br />![L'icona Impossibile spostare qui](media/personalization-cannot-move-here.png "Modalità di personalizzazione - Impossibile spostare l'icona qui") indica che non è possibile spostare l'elemento nella posizione selezionata.|Le parti sono suddivisioni o aree in una pagina che contengono elementi quali più campi, un'altra pagina, un grafico o dei riquadri.<br /><br />[Ulteriori informazioni sulla personalizzazione delle azioni](#Actions)<br>[Ulteriori informazioni sulla personalizzazione delle parti](#Parts)|
|Nascondere un elemento attualmente visualizzato, come un campo, una colonna nell'elenco, un riquadro, un'azione o una parte.|Seleziona l'elemento, seleziona la freccia, quindi seleziona <b>Nascondi</b>.|Nella modalità di personalizzazione, le azioni nascoste sono visualizzate in grigio con testo in corsivo e le parti nascoste sono ombreggiate da linee diagonali. I campi e le colonne nascosti non sono indicati nella pagina. <!--The element is grayed when you are in personalizing mode.--> Quando esci dalla modalità di personalizzazione, tutti gli elementi scompaiono. Se il campo che nascondi è visualizzato anche nell'intestazione della Scheda dettaglio quando questa è compressa, il campo non è più visualizzato.|
|Mostrare un'azione o una parte attualmente nascosta|Per un elemento in grigio (nascosto), seleziona la freccia, quindi scegli <b>Mostra</b>.|L'elemento nascosto è di nuovo visibile.|
|Mostrare un campo attualmente nascosto|Nel banner <b>Personalizzazione</b>, scegli l'azione <b>+ Campo</b>.<br /></br>Si apre a il riquadro <b>Aggiungi campo a pagina</b> sul lato destro della pagina. Se selezioni un campo nel riquadro, la posizione nascosta dello stesso viene visualizzata nella pagina.<br /><br />Per mostrare un campo, trascinalo dal riquadro o dalla relativa posizione nascosta nella posizione desiderata. La posizione è indicata da una spessa linea orizzontale o verticale.<br><br> Un altro modo è selezionare la freccia nella posizione nascosta del campo e selezionare **Mostra**. |Ogni pagina include una serie di campi predefiniti che puoi scegliere di visualizzare.<br /><br />[Ulteriori informazioni sull'utilizzo di campi](#fields) |
|Visualizzare un campo nell'intestazione di un Scheda dettaglio quando questa è compressa.|Scegli la freccia e quindi <b>Mostra quando compresso</b>. <br /> <br />Se questa opzione non è visibile, è già impostata. In questo caso, per smettere di visualizzare il campo nell'intestazione della Scheda dettaglio, scegli <b>Mostra sempre</b>.|*Scheda dettaglio* è il termine utilizzato per un gruppo di campi visualizzati sotto un'intestazione comune. Utilizza l'opzione <b>Mostra quando compresso</b> per visualizzare i campi più importanti. Se selezioni un campo nell'intestazione, si apre la Scheda dettaglio e lo stato attivo è sul campo selezionato.<br /><br />Questa opzione è applicabile solo se una pagina ha più di una Scheda dettaglio. Se vi è una sola Scheda dettaglio, può non essere compressa, per cui l'opzione <b>Mostra quando compresso</b> non è disponibile.|
|Visualizzare un campo solo quando si seleziona **Mostra di più**.|Seleziona la freccia e quindi <b>Visualizza in "Mostra più"</b>.|Se l'opzione <b>Visualizza in "Mostra più"</b> non è visibile, il campo è già impostato. In tal caso, per visualizzare sempre un campo e non solo quando si seleziona **Mostra di più**, scegli <b>Mostra sempre</b>.|
|Stabilire se un campo può essere modificato o meno.|Seleziona il campo, seleziona la freccia nel campo, quindi seleziona <b>Blocca modifica</b> per impedire la modifica del valore del campo o <b>Sblocca modifica</b> per consentire la modifica del valore del campo.|Puoi sbloccare solo i campi che hai bloccato in precedenza. Alcuni campi sono bloccati per impostazione predefinita, in base al design o da un amministratore del profilo che ha [personalizzato la pagina](ui-personalization-manage.md). Questi campi non possono essere sbloccati.|
|Modificare il riquadro di blocco di un elenco in un'altra colonna. |Seleziona la freccia della colonna che desideri come ultima colonna del riquadro di blocco, quindi scegli <b>Imposta Blocca riquadro</b>.<br /><br/>Se vuoi impostare il riquadro di blocco di nuovo sulla posizione originale, seleziona la freccia per la colonna corrente del blocco e scegli <b>Cancella Blocca riquadro</b>. Nota: non puoi rimuovere il riquadro di blocco.|Il riquadro di blocco specifica le colonne che sono sempre visualizzate sul lato sinistro dell'elenco, anche quando si scorre orizzontalmente.|  
|Ignorare un campo quando si preme INVIO.|Seleziona la freccia accanto al campo, o l'intestazione di una colonna in un elenco, e scegli **Escludi da Immissione rapida**.  | Se **Escludi da Immisione rapida** non è visibile, il campo è già ignorato. In tal caso, per smettere di ignorare il campo, scegli **Includi in Immissione rapida**.<br><br>[Ulteriori informazioni su Immissione rapida](ui-enter-data.md#QuickEntry)|
|Riordinare e rimuovere visualizzazioni che rappresentano elenchi filtrati.|Scegli la freccia accanto a una visualizzazione, quindi scegli **Sposta**, **Rimuovi** o **Nascondi**.|[Ulteriori informazioni sul salvataggio e sulla personalizzazione di visualizzazioni elenco](ui-views.md)|  
|Aggiungere una nuova azione a una pagina o un report in Gestione ruolo utente.|Dalla pagina di destinazione, dalla pagina della richiesta di report o dalla finestra della funzionalità delle informazioni, seleziona l'icona del segnalibro.|[Ulteriori informazioni sull'aggiunta di un segnalibro a pagine e report](ui-bookmarks.md)|
|Avviare sempre un elenco come espanso o compresso|Scegli il pulsante **Espandi tutto** o **Comprimi tutto** nell'angolo in alto a sinistra dell'elenco. In alternativa, scegli l'azione **Espandi tutto** o **Comprimi tutto** nel menu della prima colonna. |Si applica agli elenchi di gerarchie comprimibili.|

## <a name="Actions"></a>Personalizzare la barra delle azioni e i menu

La personalizzazione consente di specificare quali azioni visualizzare nelle barre di spostamento e azione e in Gestione ruolo utente e dove. È possibile visualizzare, nascondere o spostare singole azioni o gruppi di azioni.

Il video seguente mostra come personalizzare le azioni sulle pagine e su Gestione ruolo utente.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

La personalizzazione delle barre di spostamento e azione è praticamente uguale a quella degli altri elementi dell'interfaccia di lavoro. Tuttavia, ciò che è possibile eseguire con un'azione o un gruppo dipende dalla posizione dell'azione o del gruppo. Il modo migliore per saperlo è di attivare la modalità di personalizzazione e di seguire le istruzioni visualizzate.

Per comprendere meglio la personalizzazione delle azioni, è necessario avere una certa familiarità con alcuni termini, ovvero *gruppo di azioni* e *categoria promossa*.  

Un *gruppo di azioni* è un elemento che si espande per visualizzare altre azioni o gruppi. Ad esempio, nella pagina **Ordini vendita**, l'azione **Funzioni** che viene visualizzata quando scegli l'azione **Azioni** è un gruppo di azioni.

Una *categoria promossa* è un gruppo di azioni visualizzato prima della riga verticale `|` nella barra delle azioni. Le categorie includono in genere le azioni più utilizzate, affinché sia possibile trovarle rapidamente. Ad esempio, nella pagina **Ordini vendita**, le azioni **Ordine**, **Rilascia** e **Registrazione**, le azioni sono categorie promosse.

> [!NOTE]  
> Per cancellare la personalizzazione, seleziona la freccia del menu progettazione della parte, quindi scegli **Cancella personalizzazione**.

### Rimuovere, nascondere e visualizzare azioni e gruppi di azioni

Quando si desidera mostrare o nascondere un'azione, le opzioni sotto la freccia definiscono le operazioni consentite in base allo stato dell'azione. 

1. Scegliere la punta per un'azione o per un gruppo di azioni.
2. Selezionare una delle seguenti opzioni:

|Opzione|Funzione|
|------|------------
|**Elimina**|Questa opzione viene visualizzata se l'azione selezionata è visibile anche altrove nella barra di spostamento o azione. La scelta di questa opzione elimina l'azione dalla posizione selezionata di modo che non sia più visualizzata. L'azione o il gruppo di azioni rimane visibile in altre posizioni. |
|**Nascondi**|Questa opzione viene visualizzata se l'azione o il gruppo di azioni non si trova altrove nella barra di spostamento o delle azioni. Come per **Elimina**, la scelta di questa opzione rimuove l'azione o il gruppo di azioni dalla barra di spostamento o delle azioni. Tuttavia, in modalità di personalizzazione, l'azione o il gruppo di azioni è ancora visualizzato nella posizione corrente, ma è inattivo.|
|**Mostra**|Questa opzione viene visualizzata se l'azione o il gruppo di azioni è stato nascosto (inattivo). La scelta di questa opzione visualizza l'azione o il gruppo di azioni nella barra di spostamento o delle azioni.|

### Spostare azioni e gruppi di azioni

La posizione in cui è possibile spostare l'azione o i gruppi di azioni è indicata da una riga orizzontale tra le due azioni o da un bordo intorno a un gruppo di azioni. Sono presenti le seguenti limitazioni:

- Puoi spostare singole azioni nelle categorie promosse, ma non è possibile riorganizzare l'ordine delle azioni nella categoria.
- Non è possibile spostare un gruppo di azioni in una categoria promossa.

1. Per spostare un azione o un gruppo di azioni, trascinarlo nella posizione desiderata, esattamente come per campi e colonne.
2. Per spostare un'azione o un gruppo di azioni in un altro gruppo di azioni che è vuoto, trascinare l'azione o il gruppo di azioni sul nuovo gruppo e rilasciarlo nella casella **Rilasciare qui un'azione**.

### Informazioni sul menu Automatizza

- Non puoi nascondere o spostare il menu **Automatizza** o il sottomenu **Power Automate** e le relative azioni.
- Puoi spostare i flussi inclusi sotto l'elemento **Automatizza**, ma non puoi nasconderli usando la personalizzazione. Lo spostamento del flusso crea una copia del flusso nella destinazione, non lo rimuove dall'elemento **Automatizza**.

> [!TIP]
> In qualità di amministratore, puoi nascondere l'elemento **Automatizza** per gli utenti. Ulteriori informazioni in [Configurare l'integrazione di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="Parts"></a>Personalizzare le parti

Punta a o selezione <kbd>ALT</kbd>+<kbd>Freccia SU</kbd> Le parti sono aree di una pagina in genere composte da più campi, grafici o altro contenuto. Una parte mostra un bordo colorato quando viene attivata. Ad esempio, una schermata iniziale di Gestione ruolo utente ha più parti. A causa del contorno ben definito, puoi personalizzare l'intera parte e il suo contenuto.

- Per spostare una parte, trascinala e rilasciala nella posizione desiderata. Una linea colorata indica posizioni valide sullo schermo. Ad esempio, i riquadri Dettaglio informazioni possono essere spostati solo accanto ad altri riquadri Dettaglio informazioni nel riquadro Dettaglio informazioni.
- Puoi nascondere una parte scegliendo l'opzione **Nascondi** sotto la freccia.
- Quando inizi a personalizzare o vai a una nuova pagina, tutte le parti che sono attualmente nascoste appaiono nella pagina con elementi visivi distintivi per indicare che sono nascoste. Puoi visualizzare la parte scegliendo l'opzione **Mostra** sotto la freccia.

Puoi cancellare tutte le modifiche di personalizzazione che hai apportato all'interno di una singola parte scegliendo l'opzione **Cancella personalizzazione** sotto la freccia della parte. L'annullamento della personalizzazione di una parte influisce solo sulle modifiche ai contenuti della parte, non sul posizionamento o sulla visibilità della parte nella pagina.  

## <a name="fields"></a> Utilizzare campi e colonne

Quando personalizzi una pagina, utilizza il riquadro **Aggiungi campo a pagina** per mostrare i campi attualmente nascosti nella pagina. Per aprire questo riquadro, seleziona l'azione **+ Campo** nella parte superiore della pagina. A differenza di altri elementi, i campi nascosti non sono indicati nella pagina stessa in modalità di personalizzazione. Tuttavia, puoi identificare i campi nascosti utilizzando il riquadro **Aggiungi campo a pagina**.

Per semplificare l'utilizzo dei campi, ecco alcune linee guida generali da seguire quando si utilizza il riquadro **Aggiungi campo a pagina**:

- Per impostazione predefinita, il riquadro elenca tutti i campi nascosti, contrassegnati dall'icona [icona Mostra campo nascosto](media/hidden-icon.png "Icona Mostra campo nascosto").
- Puoi filtrare l'elenco per mostrare altri campi, come quelli attualmente visualizzati nella pagina, selezionando il pulsante **Campi consigliati** sopra l'elenco e scegliendo un'opzione di filtro. Il nome del pulsante cambia in base all'opzione di filtro scelta.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Pulsante filtro nel riquadro Aggiungi campo a pagina in modalità di personalizzazione.":::
- La selezione di un campo nell'elenco ne evidenzia la posizione nella pagina. Se il campo è attualmente nascosto, la relativa posizione progettata è visualizzata in uno stato ombreggiato. 
- Per ottenere maggiori dettagli su un campo nell'elenco, punta allo stesso o seleziona <kbd>ALT</kbd>+<kbd> Freccia SU</kbd> per visualizzare una descrizione comando.
- I campi disponibili nel riquadro Aggiungi campo a pagina sono determinati dallo sviluppatore della pagina e della relativa tabella di origine o da un amministratore del profilo che ha [personalizzato la pagina](ui-personalization-manage.md). Non è possibile creare nuovi campi.
- Alcune pagine hanno più campi pagina associati alla stessa tabella di origine. Il riquadro mostrerà entrambi/tutti i campi pagina in modo indipendente. Anche mostrare/nascondere/spostare questi campi sono operazioni indipendenti che non hanno effetto l'una sull'altra.


### Rendere visibile un campo nascosto

Esistono due modi per mostrare un campo attualmente nascosto nella pagina:

- Trascinare il campo nella posizione desiderata. Una spessa linea orizzontale o verticale indica la posizione di destinazione.
- Selezionare il campo nell'elenco, quindi andare al campo ombreggiato nella pagina e selezionare l'opzione **Mostra**.

## Cancella individualizzazione

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

## Suggerimenti e altri punti di interesse

Per agevolare la comprensione della personalizzazione, di seguito sono elencati alcuni puntatori.

- Quando apporti modifiche a una pagina scheda che apri da un elenco, le modifiche diventano effettive in tutti i record a cui accedi dall'elenco. Ad esempio, si apre un cliente specifico da una pagina elenco Clienti e quindi si personalizza la pagina aggiungendo un campo. Quando apri altri clienti dall'elenco, il campo aggiunto viene visualizzato anche per questi clienti.
- Le modifiche che effettui riguardano tutte le Gestioni ruolo utente. Ad esempio, se effettui una modifica all'elenco Cliente quando la Gestione ruolo utente è impostata su Manager aziendale, le modifiche vengono visualizzate anche nella pagina **Clienti** quando Gestione ruolo utente è impostato su Gestore ordini vendite.
- Le modifiche a una pagina in un riquadro diventano effettive nella pagina ovunque viene visualizzata.  
- Non puoi personalizzare una pagina che è in [modalità analisi](analysis-mode.md). L'interruttore **Analizza** è disattivato. Se passi alla modalità di personalizzazione mentre la pagina è in modalità di analisi, la modalità di analisi viene automaticamente disattivata. 
- Alcune pagine hanno più campi pagina associati alla stessa tabella di origine. Il riquadro mostrerà entrambi/tutti i campi pagina in modo indipendente. Anche mostrare/nascondere/spostare questi campi sono operazioni indipendenti che non hanno effetto l'una sull'altra.
- Se una parte o un gruppo è nascosto, i campi fantasma saranno comunque visibili all'interno della parte o del gruppo, ma non potrai trascinare o aggiungere/mostrare quel campo finché non rendi visibile il gruppo o la parte.

## Vedi il relativo [training Microsoft](/training/modules/personalize-ui-dynamics-365-business-central/index)

## Vedi anche
[Personalizzare le pagine per profili](ui-personalization-manage.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
