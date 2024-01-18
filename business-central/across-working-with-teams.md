---
title: Condivisione dei record di Business Central in Microsoft Teams
description: Informazioni su come utilizzare l'app Business Central per Microsoft Teams.
author: jswymer
ms.topic: how-to
ms.service: dynamics365-business-central
ms.reviewer: jswymer
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 12/12/2023
ms.author: jswymer
ms.custom: bap-template
---

# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams"></a>Condivisione di record e link di pagine di Business Central in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] offre un paio di modi per condividere i dati da Business Central direttamente in una conversazione Microsoft Teams:

<!-- 
## <a name="overview"></a>Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Con l'app [!INCLUDE [prod_short](includes/prod_short.md)] installata in Teams, puoi includere una scheda interattiva del record di Business Central in una conversazione di Teams.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Con o senza l'app [!INCLUDE [prod_short](includes/prod_short.md)] installata, puoi condividere un link dalle pagine di Business Central a una conversazione di Teams.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

Le sezioni seguenti descrivono i diversi modi in dettaglio.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation"></a>Includere e visualizzare una scheda Business Central in una conversazione Teams

Con l'applicazione Business Central per Teams, puoi copiare un link da qualsiasi record di Business Central, come un cliente o un ordine di vendita, e incollare il link in una conversazione di Teams. L'app collega Microsoft Teams ai dati aziendali in [!INCLUDE [prod_short](includes/prod_short.md)]\. Poi espande il link in una scheda compatta e interattiva che visualizza le informazioni sul record. Una volta nella conversazione, l'utente e i colleghi possono visualizzare ulteriori dettagli sul record, modificare i dati e intraprendere azioni, senza uscire da Teams.

[![Integrazione di Teams con Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites"></a>Prerequisiti

- Avere accesso a Microsoft Teams.
- Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams. Per ulteriori informazioni, vedere [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Tutti i partecipanti a una conversazione di Teams saranno in grado di visualizzare le schede per i record di Business Central inviati alla conversazione. Tuttavia per visualizzare maggiori dettagli sui record, utilizzando i pulsanti **Dettagli** o **Apri nuova finestra** in una scheda, sarà necessario accedere a [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Gestione dell'integrazione di Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation"></a>Includere una scheda Business Central in una conversazione di Teams

1. Accedere a [!INCLUDE [prod_short](includes/prod_short.md)] utilizzando il browser.
2. Aprire il record che si desidera condividere.

    L'app è progettata per visualizzare una scheda per pressoché ogni tipo di pagina [!INCLUDE [prod_short](includes/prod_short.md)]. Ma offre la migliore esperienza quando viene utilizzato per le pagine che visualizzano un singolo record, come un articolo, un cliente o un ordine cliente.
3. Copia il collegamento alla pagina.

    Il collegamento può essere copiato in due modi: Il modo più semplice e preferito è selezionare **Condividi** ![Icona Condividi in Business Central](media/share-icon.png) > **Copia collegamento**. L'altro modo è copiare l'URL completo dalla barra degli indirizzi del browser.

    [![Copia l'URL di Business Central dal browser.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Accedere a Teams e avviare una conversazione, che può essere una chat con una persona, un gruppo di persone o un canale del team.
5. Incolla il collegamento (URL) nella casella del messaggio in cui componi un messaggio.

    ![Incolla l'URL di Business Central in Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Se ricevi un messaggio del tipo: *Business Central vuole mostrare un'anteprima di questo collegamento*, significa che non hai installato l'app Business Central per Teams. Per installare l'app, seleziona **Mostra anteprima** e segui le istruzioni.

    > [!NOTE]
    > A seconda della versione di Business Central, la prima volta che si incolla un collegamento in una conversazione, verrà richiesto di accedere a [!INCLUDE [prod_short](includes/prod_short.md)] e fornire il consenso di recuperare i dati all'app. Segui semplicemente le istruzioni sullo schermo. Dovrai eseguire questo passaggio solo una volta.
6. Attendere mentre viene generata una scheda nella casella del messaggio.
7. Quando viene visualizzata la scheda, esaminare attentamente il contenuto della scheda per eventuali informazioni sensibili prima di inviare il messaggio. Questo passaggio è importante perché una volta inviato il messaggio, tutti i partecipanti alla conversazione possono vedere la scheda.
8. Se la scheda ha l'aspetto desiderato, selezionare **Invia** per inviarla alla conversazione.

    > [!TIP]
    > Dopo che viene visualizzata la scheda e prima di selezionare **Invia** è possibile eliminare l'URL incollato, se desiderato.
9. Per visualizzare ulteriori dettagli o apportare modifiche al record visualizzato nella scheda, selezionare **Dettagli**. Per ulteriori informazioni, vedere la sezione seguente.

### <a name="view-card-details"></a>Visualizzare i dettagli della scheda

Una volta che una scheda è stata inviata a una conversazione, tutti i partecipanti con le [autorizzazioni adeguate](admin-teams-integration.md#permissions) possono selezionare **Dettagli** per aprire una finestra che visualizza ulteriori informazioni sul record ed eventualmente apportare modifiche al record. Non importa se sei tu a inviare la scheda o a riceverla. La funzionalità **Dettagli** è particolarmente utile per i destinatari, perché fornisce loro rapidamente informazioni concise e mirate sul record.

La finestra dei dettagli è simile a quella di [!INCLUDE [prod_short](includes/prod_short.md)], ma è focalizzata sulla pagina o sul record a cui si riferisce la scheda. Al termine della visualizzazione e delle modifiche, chiudere la finestra per tornare alla conversazione di Teams.

Ecco un paio di cose da tenere a mente quando si utilizzano i dettagli della scheda:

- Per aprire i dettagli della carta, gli utenti devono avere il permesso sulla pagina e i suoi dati in [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Le schede nelle chat di Teams non vengono aggiornate automaticamente alle modifiche. Qualsiasi modifica salvata su un record nella finestra dei dettagli viene salvata in [!INCLUDE [prod_short](includes/prod_short.md)]\. Ma la scheda in Teams non mostrerà le modifiche nella conversione, finché non incollerai nuovamente il collegamento.

Per ulteriori informazioni sull'utilizzo delle schede e sui dettagli delle schede, vedi [Domande frequenti su Teams](teams-faq.md).

## <a name="share-a-link-to-page-from-business-central-to-teams"></a><a name="share-link"></a>Condividi un link alla pagina da Business Central a Teams

Direttamente dalla maggior parte delle pagine di raccolta, come la pagina degli **articoli**, e dalle pagine dei dettagli, come la scheda degli **articoli**, puoi inviare un link alla pagina a destinatari specifici in una conversazione di Team. Per esempio, puoi condividere un link a una vista filtrata dei tuoi record. I destinatari possono quindi selezionare il link per aprire la pagina in [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![Il menu Condividi visualizzato su una scheda.](media/teams-share-link-v2.png "Il menu Condividi visualizzato su una scheda.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites-1"></a>Prerequisiti

- Avere accesso a Microsoft Teams.
- (Facoltativo) Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams. 

  Con l'app installata, i messaggi che invii con il collegamento includeranno anche una scheda compatta per la pagina. Per ulteriori informazioni su come installare l'app, vedi [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link"></a>Condividi un link

1. In [!INCLUDE [prod_short](includes/prod_short.md)]\, apri la pagina che vuoi condividere.
2. Nella parte superiore della pagina, scegli l'azione ![!Condividi con altre app sulle pagine.](media/share-icon.png) e poi **Condividi in Teams**.
3. Se ti viene chiesto, accedi a Teams con il tuo nome utente e la tua password.
4. Nella pagina **Condividi in Teams**, digita il nome di una persona, gruppo o canale a cui vuoi inviare il messaggio.
5. La casella del messaggio include un link alla pagina. Se l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams è installata, nella finestra del messaggio apparirà anche una scheda per il record o la pagina collegati.

   Aggiungi altre informazioni se vuoi, poi scegli **Condividi**.
6. Il link è stato condiviso. Se vuoi andare alla conversazione, scegli **Vai a Teams**.

## <a name="see-also"></a>Vedere anche

[Panoramica dell'integrazione di Business Central e Microsoft Teams](across-teams-overview.md)  
[Installare l'App [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Domande frequenti su Teams](teams-faq.md)  
[Ricerca di clienti, fornitori e altri contatti da Microsoft Teams](across-search-contacts-teams.md)  
[Cambiare le impostazioni aziendali e di altro tipo in Teams](across-teams-settings.md)  
[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  
[Sviluppare per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
