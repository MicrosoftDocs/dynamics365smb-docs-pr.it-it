---
title: Personalizzare le pagine per i ruoli
description: Informazioni su come personalizzare l'interfaccia utente per un profilo (ruolo) di modo che tutti gli utenti assegnati a quel ruolo vedano un'area di lavoro personalizzata.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# <a name="customize-pages-for-profiles"></a>Personalizzazione delle pagine per profili

Business Central fornisce sia la [personalizzazione](ui-personalization-user.md) per gli utenti sia la personalizzazione per gli amministratori. La personalizzazione consente agli utenti di personalizzare la proprio area di lavoro regolando i layout di pagina in base alle proprie preferenze. Gli amministratori possono personalizzare i layout di pagina per un profilo specifico, in base ai ruoli aziendale o ai reparti, di modo che tutti gli utenti visualizzino la stessa pagina personalizzata. Sebbene la personalizzazione consenta agli utenti di mostrare, nascondere e spostare campi e azioni in una pagina, la personalizzazione offre funzionalità aggiuntive. Ad esempio, la personalizzazione ti consente di mostrare i campi che si trovano nella tabella di origine della pagina o nelle tabelle di estensione ma non sono definiti nell'oggetto pagina. Questa non è una possibile personalizzazione.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> L'uso aziendale tipico di un profilo è un ruolo. Un profilo viene quindi denominato *Profilo (ruolo)* nell'interfaccia utente.

La personalizzazione delle pagine inizia dalla pagina **Profili (ruoli)**, ovvero il punto di partenza dell'amministratore per la gestione dei profili degli utenti in singole schede profilo. Oltre a personalizzare il layout delle pagine, si controllano varie altre impostazioni per i profili nella pagina **Profilo (ruolo)** di ogni profilo. Per ulteriori informazioni, vedere [Gestire i profili](admin-users-profiles-roles.md).

## <a name="prerequisites"></a>Prerequisiti

- L'account Business Central deve disporre del set di autorizzazioni **Gestione profilo D365** o autorizzazioni equivalenti. 

   Il set di autorizzazioni **Gestione profilo D365** include l'autorizzazione di esecuzione sull'oggetto di sistema **9026 Aggiungi campo a tabella**. Se non disponi di questa autorizzazione, non puoi aggiungere campi alla pagina a meno che non siano definiti nell'oggetto pagina. 

## <a name="customize-pages-for-a-profile"></a>Personalizzare pagine per un profilo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Profili (ruoli)**, quindi scegli il collegamento correlato.
2. Selezionare la riga per il profilo per cui si desidera personalizzare le pagine, quindi scegliere l'azione **Modifica**.
3. Scegliere l'azione **Personalizza pagine**.

    [!INCLUDE[prod_short](includes/prod_short.md)] viene aperto in una nuova scheda del browser per il profilo selezionato con il banner **Personalizzazione** attivato. Il banner **Personalizzazione** offre le stesse funzionalità del banner **Personalizzazione** disponibile per gli utenti.

4. Personalizzare le pagine in base alle esigenze del ruolo o del reparto in questione, proprio come farebbe un utente durante la personalizzazione. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

    > [!NOTE]
    > Per navigare durante la personalizzazione, utilizza <kbd>CTRL</kbd>+<kbd>+clic</kbd> su un'azione se è evidenziata dalla freccia.

5. Al termine della modifica del layout in una o più pagine, selezionare il pulsante **Fatto** nel banner **Personalizzazione**.
6. Chiudere la scheda del browser.

La personalizzazione delle pagine è ora registrata per il profilo.

## <a name="view-all-customized-pages-for-a-profile"></a>Visualizzare tutte le pagine personalizzate per un profilo

Puoi ottenere una panoramica di quali pagine sono personalizzate per un profilo, ad esempio per pianificare quali pagine personalizzare ulteriormente o eliminare.

- Nella pagina **Profilo (ruolo)**, scegliere l'azione **Gestisci pagine personalizzate**.

Nella pagina **Pagine personalizzate** è possibile eliminare le personalizzazioni e risolvere i problemi analizzando i potenziali problemi.  

## <a name="delete-all-customizations-for-a-profile"></a>Eliminare tutte le personalizzazioni per un profilo

È possibile annullare tutte le personalizzazioni apportate per un profilo. Le personalizzazioni introdotte con un'estensione e le personalizzazioni eseguite da un utente non vengono eliminate. È possibile eliminare tutte le personalizzazioni con un'altra azione. Per ulteriori informazioni, vedere [Per eliminare tutte le personalizzazioni eseguite da un utente](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Nella pagina **Profilo (ruolo)** per un profilo personalizzato, selezionare l'azione **Cancella pagine personalizzate**.

Il layout delle pagine per il profilo viene ripristinato al layout predefinito.  

## <a name="delete-customization-for-specific-pages-for-a-profile"></a>Eliminare la personalizzazione di specifiche pagine per un profilo

È possibile eliminare personalizzazioni di singole pagine eseguite per un profilo. Le personalizzazioni introdotte con un'estensione e le personalizzazioni eseguite da un utente non vengono eliminate. È possibile eliminare personalizzazioni di specifiche pagine con un'altra azione. Per ulteriori informazioni, vedere [Per eliminare le personalizzazioni per pagine specifiche](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Nella pagina **Profilo (ruolo)**, scegliere l'azione **Gestisci pagine personalizzate**.
2. Nella pagina **Pagine personalizzate** selezionare una o più righe per le personalizzazioni che si desidera eliminare, quindi selezionare l'azione **Elimina**.

Il layout delle pagine selezionate viene adattato alle modifiche apportate.

## <a name="add-a-field"></a>Aggiungere un campo

L'aggiunta di campi alla pagina viene eseguita dal riquadro **Aggiungi campo a pagina**, che si apre selezionando l'azione **+ Campo** quando è attivata la modalità di personalizzazione. È importante capire che il riquadro **Aggiungi campo a pagina** viene utilizzato per mostrare i campi già esistenti, nella pagina e nelle relative tabelle di origine, ma che sono attualmente non visibili. Non è possibile creare nuovi campi.

I riquadro **Aggiungi campo a pagina** presenta tutti i campi che possono essere visualizzati nella pagina. I campi sono suddivisi nelle seguenti categorie, come determinato dal design sottostante della pagina stessa, dalla relativa tabella di origine e dalle estensioni:

|Categoria|Descrizione|
|-|-|
|Campi tabella non presenti nell'oggetto pagina|Include i campi definiti nella tabella di base o nelle tabelle di estensione, ma non definiti nella pagina. La descrizione comando per questi campi include l'etichetta **Definito dalla tabella**.<br><br>|
|Campi pagina associati a una tabella|Include i campi definiti nella tabella di base o nelle estensioni della tabella e definiti anche nella pagina come visualizzati o nascosti. La descrizione comando per questi campi include l'etichetta **Definito dalla pagina**.|
|Campi pagina non associati a una tabella| I campi definiti non nella tabella di base o nelle tabelle di estensione, ma solo nella pagina. Questi campi sono generalmente utilizzati per variabili o calcoli. La descrizione comando per questi campi include l'etichetta **Definito dalla pagina**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Utilizza il pulsante filtro sopra l'elenco per modificare la categoria di campi visualizzata nel riquadro **Aggiungi campo a pagina**.  

:::image type="content" source="media/customization-filter.svg" alt-text="Pulsante filtro nel riquadro Aggiungi campo a pagina in modalità di personalizzazione.":::
 
### <a name="add-table-field-thats-not-on-the-page-object"></a>Aggiungere un campo tabella non presente nell'oggetto pagina

Se desideri rendere disponibile agli utenti un campo di sola tabella in una pagina, devi prima aggiungerlo alla pagina. Una volta aggiunto il campo, gli utenti possono scegliere di mostrare o nascondere il campo come preferiscono utilizzando la personalizzazione. Esistono due modi per aggiungere un campo.

- Un modo consiste nel trascinarlo dal riquadro **Aggiungi campo a pagina** nella posizione desiderata.
- Un altro modo consiste nel selezionare il campo nel riquadro per visualizzare la posizione consigliata nella pagina. Quindi vai alla posizione del campo nelle pagine, seleziona la freccia e seleziona **Aggiungi**. 

Una volta aggiunto il campo, la descrizione comando per il campo nel riquadro **Aggiungi campo a pagina** diventa **Definito dalla pagina**. La modifica del campo aggiunto è bloccata e non può essere sbloccata.

## <a name="remove-a-field"></a>Rimuovere un campo

Se hai aggiunto un campo tabella che originariamente non era nell'oggetto pagina, puoi rimuoverlo nuovamente. La rimozione di un campo è differente dal nasconderlo. Quando nascondi un campo, gli utenti possono comunque visualizzarlo nella propria area di lavoro tramite la personalizzazione. Se invece rimuovi un campo, il campo non potrà più essere mostrato o nascosto agli utenti. Se il campo è attualmente visualizzato nell'area di lavoro di un utente, scompare da tale area di lavoro quando lo rimuovi. 

Per rimuovere un campo, seleziona la freccia sul campo nella pagina e quindi seleziona **Rimuovi**. Se non riesci a trovare il campo, selezionalo nel riquadro **Aggiungi campo a pagina** per indicarne la posizione nascosta. 

> [!IMPORTANT]
> La rimozione di un campo non elimina i dati archiviati nel campo o nelle relative tabelle di origine. Rimuove semplicemente il campo dalla visualizzazione. 

## <a name="lock-and-unlock-editing"></a>Bloccare e sbloccare la modifica

La personalizzazione consente di bloccare (consentire) o sbloccare (impedire) la modifica della maggior parte dei campi in una pagina. Per bloccare o sbloccare la modifica, seleziona il campo nella pagina, seleziona la freccia, quindi seleziona **Blocca modifica** o **Sblocca modifica**. È importante tenere presente alcune regole per bloccare e sbloccare i campi:

- I campi che originariamente non erano nell'oggetto pagina ma che sono stati aggiunti alla pagina mediante personalizzazione sono sempre bloccati e non possono essere sbloccati utilizzando la personalizzazione.
- La struttura del campo può anche impedirne la modifica. Se lo sviluppatore AL imposta la [proprietà modificabile](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) su `false`, il campo sarà sempre bloccato e non potrà essere sbloccato.
- È importante notare che la funzionalità di modifica del blocco ha lo scopo di favorire l'accuratezza, la coerenza e l'affidabilità dei dati. Non è destinato a garantire l'integrità dei dati.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## <a name="important-information-and-tips"></a>Informazioni e suggerimenti importanti

- Non tutti i campi tabella possono essere disponibili per la personalizzazione dal riquadro **Aggiungi campo a pagina**. Lo sviluppatore di una tabella può scegliere di impedire che un campo venga visualizzato nella personalizzazione impostando la proprietà [AllowInCustomization](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) del campo su `false`.
- Non puoi personalizzare una pagina che è in [modalità analisi](analysis-mode.md). L'interruttore **Analizza** è disattivato. Se passi alla modalità di personalizzazione mentre la pagina è in modalità di analisi, la modalità di analisi viene automaticamente disattivata. 
- Alcune pagine hanno più campi pagina associati alla stessa tabella di origine. Il riquadro **Aggiungi campo a pagina** mostra tutti questi campi pagina in modo indipendente. Puoi mostrare, nascondere o spostare questi campi in modo indipendente senza influenzare gli altri.
- Se una parte o un gruppo è nascosto, puoi comunque identificare i campi nascosti nella parte o nel gruppo, ma non puoi aggiungere, spostare o mostrare i campi nella parte o nel gruppo finché non vengono resi visibili. 
## <a name="see-also"></a>Vedere anche

[Personalizza l'area di lavoro](ui-personalization-user.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
