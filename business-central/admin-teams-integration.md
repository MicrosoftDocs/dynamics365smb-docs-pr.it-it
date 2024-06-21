---
title: Gestione dell'integrazione Microsoft Teams con Business Central | Microsoft Docs
description: Gestione dell'integrazione di Business Central con Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Gestione dell'integrazione di Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Questo articolo fornisce una panoramica di ciò che è possibile fare come amministratore per controllare l'integrazione di Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)].

## In Microsoft Teams

### Requisiti minimi

Questa sezione descrive i requisiti minimi per il funzionamento dell'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams.

- Licenze richieste

    L'app [!INCLUDE[prod_short](includes/prod_short.md)] richiede una licenza Teams tramite un abbonamento Microsoft 365 Business o Enterprise. Gli abbonamenti a Teams indipendenti come Microsoft Teams (gratuito) o Microsoft Teams Essentials non sono supportati.

    La maggior parte delle funzionalità dell'app [!INCLUDE[prod_short](includes/prod_short.md)] per Teams richiede anche una licenza [!INCLUDE [prod_short](includes/prod_short.md)], come mostrato nella tabella seguente.

    |Quale|Licenza di [!INCLUDE [prod_short](includes/prod_short.md)]|
    |----|---|
    |Ricerca di contatti di [!INCLUDE [prod_short](includes/prod_short.md)].|![segno di spunta](media/check.png "selezionato")|
    |Incollare un collegamento a un record [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione e inviarla come scheda.|![segno di spunta](media/check.png "selezionato")|
    |Condividi un link da una pagina in [!INCLUDE [prod_short](includes/prod_short.md)] alla conversazione di Teams.|![segno di spunta](media/check.png "selezionato")|
    |Visualizzare una scheda di un record [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione.||
    |Visualizzare altri dettagli di una scheda per un record [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione.|![segno di spunta](media/check.png "selezionato")|
    |Aprire un link di pagina in [!INCLUDE [prod_short](includes/prod_short.md)] da una conversazione.|![segno di spunta](media/check.png "selezionato")|

- Consentire le anteprime URL

    L'impostazione dei criteri **Consenti anteprime URL** deve essere attivata. In caso contrario, non è possibile generare una scheda per i collegamenti di [!INCLUDE [prod_short](includes/prod_short.md)] incollati in una conversazione di Teams. Per ulteriori informazioni su questa impostazione, vedere [Gestire i criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams).

### Gestione dell'app [!INCLUDE [prod_short](includes/prod_short.md)] (facoltativo)

In qualità di amministratore di Teams, è possibile gestire tutte le app per l'organizzazione, inclusa l'app [!INCLUDE [prod_short](includes/prod_short.md)]. È possibile approvare o installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per l'organizzazione, impedire all'utente di installare l'app e altro ancora.

Per ulteriori informazioni, vedere i seguenti articoli nella documentazione di Microsoft Teams:

- [Gestire le app nell'interfaccia di amministrazione di Microsoft Teams](/MicrosoftTeams/manage-apps)
- [Gestire i criteri di configurazione dell'app in Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## In [!INCLUDE [prod_short](includes/prod_short.md)]

### Requisiti minimi

- Versione di [!INCLUDE [prod_short](includes/prod_short.md)]:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2021 primo ciclo di rilascio o successivi. L'integrazione di Teams è supportata solo per [!INCLUDE [prod_short](includes/prod_short.md)] online, non in locale.

- La codeunit **2718 Provider di riepilogo pagine** è pubblicata come servizio Web:

    Questa codeunit viene pubblicata come servizio Web per impostazione predefinita. La codeunit fa parte dell'applicazione di sistema [!INCLUDE [prod_short](includes/prod_short.md)]. Viene utilizzata per ottenere i dati del campo per una pagina [!INCLUDE [prod_short](includes/prod_short.md)] aggiunta a una conversazione di Teams. Per informazioni sulla pubblicazione di servizi Web, vedi [Pubblicare un servizio Web](across-how-publish-web-service.md).

- <a name="permissions"></a>Autorizzazioni utente:

    Per la maggior parte, la ricerca dei contatti, le pagine e i dati che gli utenti possono visualizzare e modificare in una conversazione di Teams sono controllati dalle autorizzazioni in [!INCLUDE [prod_short](includes/prod_short.md)].

    - Per cercare contatti, gli utenti devono avere almeno l'autorizzazione di lettura per la tabella dei **Contatti**. 
    - Per incollare un collegamento [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione di Teams e farlo espandere in una scheda, gli utenti devono disporre almeno dell'autorizzazione di lettura sulla pagina e sui relativi dati.
    - Una volta che una scheda è stata inviata a una conversazione, qualsiasi utente in quella conversazione può visualizzare quella scheda senza autorizzazione per [!INCLUDE [prod_short](includes/prod_short.md)].
    - Per visualizzare ulteriori dettagli per una scheda o aprire il record in [!INCLUDE [prod_short](includes/prod_short.md)], gli utenti devono disporre dell'autorizzazione di lettura sulla pagina e sui suoi dati.
    - Per modificare i dati, l'utente deve disporre delle autorizzazioni per la modifica.
    
    Per informazioni sulle autorizzazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

## Installare l'applicazione Business Central utilizzando la distribuzione centralizzata

Il centro di amministrazione di Microsoft Teams è dove configuri le politiche di configurazione delle app Teams per l'organizzazione. Nel centro amministrativo di Teams, puoi usare la funzione di distribuzione centralizzata per installare automaticamente l'app Business Central in Teams per tutti gli utenti della tua organizzazione, per gruppi specifici o per singoli utenti.

> [!NOTE]
> Per impostare la distribuzione centralizzata, il tuo account Teams deve avere il ruolo di **amministratore di Teams Service**  o il ruolo di **amministratore globale** .

1. In Business Central, scegli la ![Lente d'ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserire **Teams App Centralized Deployment**e poi scegliere il link relativo. Oppure, seleziona [qui](https://businesscentral.dynamics.com/?page=1833) per aprire direttamente la pagina.
2. Leggi le informazioni su **Set up the Business Central app for Teams**, poi scegli **Avanti** quando sei pronto.
3. Aprire il [centro amministrativo di Teams](https://go.microsoft.com/fwlink/?linkid=2163970)e completare i seguenti passi.
    1. Vai a **Teams apps** > **Setup policies**.
    2. Crea un nuovo criterio o seleziona il criterio che vuoi utilizzare per installare l'app Business Central, quindi seleziona **Aggiungi applicazioni**.
    3. Nella pagina **Aggiungi applicazioni installate**, cerca e seleziona **Business Central**.
    4. Scegliere **Aggiungi**.

       Business Central dovrebbe ora apparire tra le **app installate** per la policy.
    5. Configura altre impostazioni secondo le necessità, poi scegli **Salva**.

    Per ulteriori informazioni sui criteri di configurazione in Teams, vedi [Gestire i criteri di configurazione delle app in Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) nella documentazione di Teams.
4. Torna a **Teams App Centralized Deployment** in Business Central e seleziona **Fatto**.

> [!IMPORTANT]
> Possono essere necessarie fino a 24 ore per applicare la politica di configurazione dell'app e distribuire l'app agli utenti.

## Gestione della privacy e della conformità 

Microsoft Teams fornisce controlli estesi per la conformità e la gestione di dati sensibili o di identificazione personale, compresi i dati aggiunti a chat e canali mediante l'app [!INCLUDE [prod_short](includes/prod_short.md)].

### Informazioni su dove vengono memorizzate le schede di [!INCLUDE [prod_short](includes/prod_short.md)]

Dopo che una scheda è stata inviata a una chat, la scheda e i campi visualizzati nella scheda vengono copiati in Teams. Queste informazioni sono soggette ai criteri di Teams per l'organizzazione, come i criteri di conservazione dei dati. Quando si visualizzano i dettagli della scheda, i dati nella finestra dei dettagli non sono memorizzati in Teams. I dati rimangono memorizzati in [!INCLUDE [prod_short](includes/prod_short.md)] e verranno recuperati da Teams solo quando l'utente sceglie di visualizzare i dettagli. 

- Per ulteriori informazioni sulla posizione in cui Teams memorizza tali dati, vedi [Posizione dei dati in Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Per altre informazioni sui criteri di conservazione in Teams, vedi [Criteri di conservazione in Microsoft Teams](/microsoftteams/retention-policies).

### Limitazione della condivisione delle schede 

Per impedire a utenti o gruppi specifici di inviare schede a chat o canali, devi impostare criteri di messaggistica che disattivano l'impostazione **Anteprime URL**. Per ulteriori informazioni su questa impostazione, vedi [Gestire i criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams). 

È inoltre possibile utilizzare barriere informative per impedire a individui o gruppi di comunicare tra loro. Per saperne di più, vedi [Barriere informative in Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Le funzionalità di prevenzione della perdita di dati nel Centro sicurezza e conformità di Microsoft 365 non possono essere applicate in modo specifico alle schede. Possono tuttavia essere applicate ai messaggi di chat che contengono le schede. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### Rispondere alle richieste di dati

Per consentire ai membri del team e ai proprietari del team di eliminare i messaggi che contengono schede sensibili devi impostare criteri di messaggistica, come: **I proprietari possono eliminare i messaggi inviati** e **Gli utenti possono eliminare i messaggi inviati**. Per ulteriori informazioni, vedi [Gestire criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams).

Le funzionalità di conformità eDiscovery e di ricerca di contenuto nel Centro sicurezza e conformità di Microsoft 365 non possono essere applicate anche alle schede.

Poiché i dati delle schede in Teams sono una copia dei dati in [!INCLUDE [prod_short](includes/prod_short.md)], puoi anche usare le funzionalità di [!INCLUDE [prod_short](includes/prod_short.md)] per esportare i dati di un cliente se richiesto. Per ulteriori informazioni sulla privacy in [!INCLUDE [prod_short](includes/prod_short.md)], vedi [Domande frequenti sulla privacy per i clienti di Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## Mostrare o nascondere i dati dei record sulle schede

Quando un record viene condiviso con altri in una chat o un canale di Teams, viene visualizzata una scheda con i campi che contengono dati sul record. Tutti i destinatari possono visualizzare questi dati (o il riepilogo dei record) per impostazione predefinita, indipendentemente dalla loro licenza o autorizzazione in Business Central. Se sei un amministratore, puoi utilizzare la Guida alla configurazione assistita **Impostazioni scheda** per nascondere il riepilogo del record in modo che non venga visualizzato nelle schede in Teams. Nascondendo il riepilogo del record vengono rimossi tutti i campi e le immagini, ma continua a mostrare il pulsante **Dettagli** e altre informazioni non relative al record sulla scheda.

|Riepilogo record attivato|Riepilogo record disattivato|
|-|-|
|![Immagine che mostra una scheda in Teams quando il riepilogo record è attivato.](media/card-settings-example-on.png)|![Immagine che mostra una scheda in Teams quando il riepilogo record è disattivato.](media/card-settings-example-off.png)|

Configura l'impostazione per ambiente. Quindi, quando attivi o disattivi il riepilogo del record, avrà effetto su tutte le società nell'ambiente.

1. In Business Central, apri l'ambiente che vuoi modificare.

   > [!TIP]
   > Per cambiare ambiente, seleziona <kbd>Ctrl</kbd>+<kbd>O</kbd>.
2. Scegli la ![Lente d'ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impostazioni scheda**, quindi scegli il collegamento correlato. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Leggi le informazioni sulle **Impostazioni carta**, quindi scegli **Avanti** quando sei pronto.
4. Nella pagina **Visibilità dati** attiva l'opzione **Mostra riepilogo record** per visualizzare i dati sulle schede o disattivala per nascondere i dati.
5. Seleziona **Avanti** e segui le istruzioni per completare la guida all'installazione.

## Vedere anche

[[!INCLUDE [prod_short](includes/prod_short.md)] e Panoramica sull’integrazione di Microsoft Teams](across-teams-overview.md)  
[Installare l'App [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Domande frequenti su Teams](teams-faq.md)  
[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  
[Sviluppare per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]