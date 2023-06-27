---
title: Aggiungere la scheda Business Central in Microsoft Teams
description: Scopri come aggiungere schede in Teams che visualizzano le pagine Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams" />Aggiungere la scheda Business Central in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

In Teams, le schede vengono visualizzate nella parte superiore dei canali e delle chat, offrendo ai partecipanti un rapido accesso alle informazioni pertinenti. Questo articolo spiega diversi modi per aggiungere una scheda che visualizzi i dati [!INCLUDE [prod_short](includes/prod_short.md)].

![Schede in Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs" />Informazioni sulle schede Business Central

Una scheda [!INCLUDE [prod_short](includes/prod_short.md)] fornisce una vista mirata degli elenchi e delle pagine delle schede di [!INCLUDE [prod_short](includes/prod_short.md)]. La scheda non mostra l'intero client Web [!INCLUDE [prod_short](includes/prod_short.md)]. Non c'è il bordo del browser, il banner di [!INCLUDE [prod_short](includes/prod_short.md)] (ad esempio con Dimmi, ricerca, guida) o menu di navigazione in alto, solo il contenuto della pagina e le sue azioni. Il contenuto è interattivo, il che significa che puoi selezionare azioni e collegamenti, modificare i dati e altro ancora. Sei limitato a ciò che vedi e puoi fare con le stesse autorizzazioni assegnate al tuo account in [!INCLUDE [prod_short](includes/prod_short.md)].

Per sapere chi può visualizzare il contenuto in una scheda [!INCLUDE [prod_short](includes/prod_short.md)], vedi [Chi può vedere il contenuto di una scheda?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Sei uno sviluppatore? Puoi anche aggiungere schede a livello di codice utilizzando l'API Microsoft Graph. Per ulteriori informazioni, vedi [Aggiungere schede Business Central in Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites" />Prerequisiti

Per aggiungere una scheda [!INCLUDE [prod_short](includes/prod_short.md)], devono essere soddisfatti i seguenti requisiti:

- Avere accesso a Microsoft Teams.
- Disponi di una licenza di [!INCLUDE [prod_short](includes/prod_short.md)].
- Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams. Per ulteriori informazioni, vedi [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md).

Per vedere la scheda [!INCLUDE [prod_short](includes/prod_short.md)] aggiunta da un altro partecipante al canale o alla chat, devono essere soddisfatti i seguenti requisiti:

- Avere accesso a Microsoft Teams.
- Disporre di una licenza [!INCLUDE [prod_short](includes/prod_short.md)] o avere accesso limitato a Business Central con una sola licenza Microsoft 365. Per ulteriori informazioni, vedi [Accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md).
- Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams.

## <a name="add-tab-using-recommended-content" />Aggiungere la scheda utilizzando il contenuto consigliato

Segui questi passaggi per aggiungere una scheda scegliendo cosa visualizzare da un elenco prontamente disponibile di contenuti consigliati basato sul tuo centro di ruolo, senza uscire da Teams. Per ulteriori informazioni sui contenuti tra cui è possibile scegliere, vedi [Da dove provengono i contenuti consigliati?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Nella parte superiore di un canale o di una chat in Teams, seleziona **+ Aggiungi una scheda**.
2. Nella casella **Ricerca**, digita *Business Central*, quindi seleziona l'icona **[!INCLUDE [prod_short](includes/prod_short.md)]** e attendi che venga visualizzata la scheda [!INCLUDE [prod_short](includes/prod_short.md)] di configurazione.

   ![Mostra la finestra di configurazione della scheda Business Central in Teams](media/teams-bc-tab-config-window.png)

3. L'opzione **Scegli tra i contenuti consigliati per** mostra l'azienda in [!INCLUDE [prod_short](includes/prod_short.md)] con cui stai lavorando. Se desideri mostrare i contenuti di un'altra azienda, seleziona l'azienda attuale, quindi utilizza le opzioni **Ambiente** e **Azienda** per specificare l'azienda con cui si desidera lavorare.
4. Seleziona la freccia giù nell'opzione **Contenuto della scheda** e scegli il contenuto che desideri visualizzare.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Alcune pagine possono includere visualizzazioni diverse, che sono varianti della pagina filtrata per mostrare dati specifici. Per modificare la visualizzazione del contenuto, seleziona la freccia giù per l'opzione **Vista preferita** e scegli la vista dall'elenco.

   Per ulteriori informazioni sulle viste, vedi [Salvare e personalizzare le visualizzazioni](ui-views.md).
6. Seleziona **Pubblica nel canale circa questa scheda** per pubblicare automaticamente un annuncio nel canale o nella chat di Teams per far sapere ai partecipanti che hai aggiunto questa scheda.
7. Seleziona **Salva**.

## <a name="add-tab-using-a-page-link" />Aggiungi scheda utilizzando un collegamento a una pagina

Un altro modo per aggiungere una scheda utilizzando un collegamento (URL) alla pagina che desideri mostrare. Questa modalità è utile quando si desidera visualizzare un record specifico di [!INCLUDE [prod_short](includes/prod_short.md)] o una pagina di elenco che non è stata inserita nei preferiti nel centro di ruolo.

1. Nella parte superiore di un canale o di una chat in Teams, seleziona **+ Aggiungi una scheda**.
2. Nella casella **Ricerca**, digita *business central* e seleziona l'icona **[!INCLUDE [prod_short](includes/prod_short.md)]**.
3. Attendi che venga visualizzata la la finestra di configurazione della scheda [!INCLUDE [prod_short](includes/prod_short.md)], quindi seleziona l'opzione **Incolla un collegamento [!INCLUDE [prod_short](includes/prod_short.md)]**.

   ![viene visualizzata la finestra di configurazione della scheda Business Central in Teams con l'opzione di collegamento evidenziata](media/teams-bc-tab-config-window-page-link.png)
4. Vai a [!INCLUDE [prod_short](includes/prod_short.md)] e apri la pagina che desideri visualizzare nella scheda.
5. Copia il collegamento alla pagina.

   Il collegamento può essere copiato in due modi: Il modo più semplice e preferito è selezionare **Condividi** ![Icona Condividi in Business Central](media/share-icon.png) > **Copia collegamento**. L'altro modo è copiare l'URL completo dalla barra degli indirizzi del browser. Per ulteriori informazioni su questo passaggio, vedi [Condivisione di record e link di pagine di Business Central](across-working-with-teams.md).

6. Torna a Teams e incolla il collegamento nella casella **URL**.
7. Nella casella **Nome scheda**, immetti un nome che verrà visualizzato nella scheda.
8. Seleziona **Pubblica nel canale circa questa scheda** per pubblicare automaticamente un annuncio nel canale o nella chat di Teams per far sapere ai partecipanti che hai aggiunto questa scheda.
9. Seleziona **Salva**.

## <a name="add-tab-by-pinning-card-details" />Aggiungi scheda inserendi i dettagli della scheda

Utilizzare questi passaggi per aggiungere una scheda per un record che è stato condiviso o incollato in un canale o in una chat di Teams. Per informazioni su come condividere record e collegamenti a pagine in Teams, vedi [Condividi record e collegamenti di pagina in Teams](across-working-with-teams.md).

1. In Teams, seleziona il pulsante **Dettagli** sulla scheda.
2. Nell'angolo in alto a destra dei dettagli della scheda, seleziona **Aggiungi nella parte superiore della chat** ![Icona Aggiungi per aggiungere la scheda Teams in Business Central](media/pin-teams.png).

## <a name="change-a-tab-and-its-content" />Modificare una scheda e il suo contenuto

Dopo aver aggiunto una scheda, puoi apportare determinate modifiche. Ad esempio, puoi rinominarla, spostarla e rimuoverla. Puoi trovare queste azioni nelle opzioni della scheda disponibili selezionando la freccia giù nella scheda.

![Viene visualizzata la finestra di configurazione della scheda Business Central in Teams e il menu delle opzioni relative alla scheda](media/teams-bc-tab-config-window-options.png)

Per quanto riguarda il contenuto di una scheda, puoi modificare i dati, se disponi delle autorizzazioni. Se modifichi i dati, gli altri non vedranno le modifiche finché non escono dalla scheda e tornano alla scheda. Lo stesso vale per te se altri utenti apportano modifiche ai dati. Non puoi modificare la pagina visualizzata nella scheda, quindi rimuovi semplicemente la scheda e aggiungine un'altra.

Puoi anche modificare la visualizzazione della pagina e dei suoi dati, ad esempio ordinare e cambiare il layout tra visualizzazione a elenco e a riquadri. Quando apporti questo tipo di modifiche, non influiranno su ciò che gli altri vedono. Vedranno ciò che hai pubblicato in origine, finché non apporteranno modifiche simili.

## <a name="see-also" />Vedere anche

[Panoramica dell'integrazione di Business Central e Microsoft Teams](across-teams-overview.md)  
[Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Condivisione di record e link di pagine di Business Central in Microsoft Teams](across-working-with-teams.md).
[Domande frequenti su Teams](teams-faq.md)  
[Ricerca di clienti, fornitori e altri contatti da Microsoft Teams](across-search-contacts-teams.md)  
[Modifica della società e di altre impostazioni in Teams](across-teams-settings.md)  
[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
