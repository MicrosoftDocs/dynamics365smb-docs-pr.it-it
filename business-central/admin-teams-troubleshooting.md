---
title: Risoluzione dei problemi relativi all'integrazione di Microsoft Teams
description: Scopri cosa puoi fare in veste di amministratore per controllare l'integrazione di Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 7a98b53a34ddf403cf6507da7740b97924d4c81c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385201"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Risoluzione dei problemi relativi all'integrazione di Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Questo articolo fornisce informazioni su come identificare e risolvere i problemi che potrebbero verificarsi durante l'utilizzo di Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)], come amministratore o utente tipico.

## <a name="none-of-my-links-expand-into-a-card"></a>Nessuno dei miei collegamenti si espande in una scheda 

Se stai riscontrando questo problema, procedi come segue:

1. Innanzitutto, assicurati che l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams sia installata.

    A questo proposito, accedi all'app desktop Teams o a Teams nel browser. Quindi, sul lato sinistro, seleziona **App** e cerca **[!INCLUDE [prod_short](includes/prod_short.md)]**. Quando trovi l'app **[!INCLUDE [prod_short](includes/prod_short.md)]**, selezionala per aprire la pagina dei dettagli dell'app. Se viene visualizzato il pulsante **Aggiungi per l'utente corrente**, l'app [!INCLUDE [prod_short](includes/prod_short.md)] non è installata. Per ulteriori informazioni su come installare l'app, vedi [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gli utenti guest non possono installare immediatamente le app. Per ulteriori informazioni sugli utenti guest, vedi le nostre domande frequenti sulla collaborazione con gli utenti guest. 

2. Quindi, controlla di aver effettuato l'accesso con l'identità corretta.

    In Teams passa a qualsiasi chat e nella casella di composizione del messaggio scegli l'icona [!INCLUDE [prod_short](includes/prod_short.md)]. Quando viene visualizzata la finestra, verifica se il nome utente utilizzato per la connessione è lo stesso per la connessione a [!INCLUDE [prod_short](includes/prod_short.md)].

3. Assicurati che la codeunit 2718 **Provider di riepilogo pagine** è pubblicata come servizio Web.

    Teams si connette a [!INCLUDE [prod_short](includes/prod_short.md)] utilizzando un endpoint a questa codeunit nel servizio [!INCLUDE [prod_short](includes/prod_short.md)]. Per informazioni sulla pubblicazione di servizi Web, vedi [Pubblicare un servizio Web](across-how-publish-web-service.md).

4. L'organizzazione potrebbe anche impedirti di incollare i collegamenti che si espandono in schede. Contatta l'amministratore per comprendere i criteri di organizzazione Teams che potrebbero applicarsi.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Il mio collegamento a volte non si espande in una scheda 

Un collegamento non si espanderà in una scheda nei seguenti casi:

- Il collegamento è relativo a una pagina di un tipo che non rappresenta un record. Ad esempio, potrebbe essere un collegamento a Gestione ruolo utente di [!INCLUDE [prod_short](includes/prod_short.md)]. Puoi controllare il tipo di pagina utilizzando il riquadro Controllo pagina nel client Web in [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni sul controllo delle pagine, vedi [Controllo di pagine](across-inspect-page.md).
- Il collegamento è relativo a una pagina che (a livello tecnico) non è collegata a una tabella di origine in [!INCLUDE [prod_short](includes/prod_short.md)]. Puoi controllare se in una pagina è presente una tabella di origine utilizzando il riquadro Controllo pagina nel client Web in [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni sul controllo delle pagine, vedi [Controllo di pagine](across-inspect-page.md). 
- Teams non supporta le anteprime dei collegamenti in alcune funzionalità. Ad esempio, quando è in corso una chat, stai partecipando a una riunione o sei un utente guest di un'altra organizzazione.
- Teams abbandona silenziosamente il tentativo di visualizzare la scheda dopo 15 secondi, ad esempio, a causa di problemi di rete.
- Team può non espandere il collegamento se hai già incollato un collegamento nella stessa casella di composizione del messaggio e hai eliminato la scheda.

Il collegamento deve inoltre contenere tutte le informazioni necessarie per individuare il record e visualizzare la scheda corrispondente. Queste informazioni includono:

- Il nome dell'ambiente, incluso nel percorso dell'URL. Se non specifichi il nome dell'ambiente, Teams presume che tu stia tentando di raggiungere l'ambiente denominato "Produzione".
- Il nome della società, utilizzando il parametro *company=*
- L'identificatore di pagina, utilizzando il parametro *page=*
- Il segnalibro del record, utilizzando il parametro *bookmark=*

Ad esempio:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Per dettagli tecnici sugli URL di [!INCLUDE [prod_short](includes/prod_short.md)], vedi [URL del client Web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) nella Guida per sviluppatori e professionisti IT di [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>La scheda viene visualizzata nella casella di composizione del messaggio, ma la selezione del pulsante Dettagli non ha effetto 

Dopo che un collegamento viene espanso in una scheda nella casella di composizione del messaggio, devi inviare il messaggio alla chat prima di poter utilizzare il pulsante **Dettagli**.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>La finestra dei dettagli si apre, ma mostra un errore prima che vengano visualizzati i dettagli

Questo problema può essere causato dalla mancanza di autorizzazioni in [!INCLUDE [prod_short](includes/prod_short.md)] o dalle impostazioni del browser (quando si utilizza Teams nel browser).

1. Verifica le autorizzazioni in [!INCLUDE [prod_short](includes/prod_short.md)].

    Per visualizzare i dettagli di una scheda, [!INCLUDE [prod_short](includes/prod_short.md)] controlla la licenza e le autorizzazioni per visualizzare quel record e quella pagina nella società e nell'ambiente specifici. Se non disponi delle autorizzazioni, nella finestra dei dettagli vengono visualizzati messaggi di errore standard di [!INCLUDE [prod_short](includes/prod_short.md)] relativi alle autorizzazioni. 

    Per ulteriori informazioni sulle autorizzazioni, vedi [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)

2. Controlla le impostazioni del browser se usi Teams nel browser.

    - Il blocco dei popup del browser deve essere disattivato o impostato per autorizzare i popup dai domini *businesscentral.dynamics.com* o *bc.dynamics.com*. Per informazioni su come autorizzare i popup per [!INCLUDE [prod_short](includes/prod_short.md)], vedi [Impostazione del browser](across-browser-settings.md#popup).
    - Il tuo browser deve avere accesso alla memoria del browser locale per i cookie e le preferenze mentre lavori.
    - Evita di utilizzare la navigazione privata o come utente ospite a meno che non sia necessario, poiché elimina o blocca determinati contenuti in alcuni browser.

    Per ulteriori informazioni sui requisiti minimi del browser, vedi [Requisiti minimi per l'utilizzo[!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Ho problemi con la fotocamera o la posizione in Teams 

Quando nella finestra dei dettagli utilizzi funzionalità di [!INCLUDE [prod_short](includes/prod_short.md)] che richiedono l'accesso alla posizione o alla fotocamera del dispositivo, devi prima fornire il tuo consenso affinché Teams acceda a queste funzionalità del dispositivo.  

- Per Team nel browser, assicurati che le impostazioni del browser consentano l'accesso alla fotocamera e alla posizione per https://teams.microsoft.com. 

- Per Teams per iOS o Android, assicurati che le impostazioni del dispositivo consentano l'accesso alla fotocamera e alla posizione per l'app per dispositivi mobili Teams. 

Per informazioni sulla modifica di queste impostazioni, vedi [La fotocamera non funziona in Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us).

L'app [!INCLUDE [prod_short](includes/prod_short.md)] non supporta la posizione nell'app desktop Teams. Per ulteriori informazioni sulla posizione, vedi [Domande frequenti su Teams](teams-faq.md#location).

Alcuni browser, come il nuovo Microsoft Edge, consentono di scegliere quale fotocamera del dispositivo utilizzare quando il dispositivo supporta più fotocamere. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>In Teams le schede e i dettagli delle schede sono visualizzati in lingue differenti

Affinché le schede e i relativi dettagli siano visualizzati in modo coerente nella stessa lingua in Teams, la lingua del client Teams e la lingua utilizzata nel client Web [!INCLUDE [prod_short](includes/prod_short.md)] devono corrispondere.

- Per informazioni sulla modifica della lingua in Teams, vedi [Modificare le impostazioni in Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7). 

- Per informazioni su come cambiare la lingua in [!INCLUDE [prod_short](includes/prod_short.md)], vedi[ Modificare le impostazioni di base - Lingua](ui-change-basic-settings.md#language).

Per ulteriori informazioni sull'utilizzo delle lingue in Teams e [!INCLUDE [prod_short](includes/prod_short.md)], vedi [ Domande frequenti su Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ho modificato un campo nella finestra dei dettagli, ma la modifica non è stata salvata

Le modifiche apportate a un campo nelle finestre dei dettagli vengono salvate automaticamente quando si esce dal campo. Prima di chiudere la finestra dopo aver modificato un campo, assicurati di premere il tasto TAB o fai clic o tocca fuori dal campo.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Un nuovo riquadro è apparso nell'icona di avvio delle app. Come posso rimuoverlo?

Quando visualizzi le tue app nella Home Page di Office 365 (https://home.office.com) oppure nell'icona di avvio delle app, un nuovo riquadro denominato "Connettore del servizio di integrazione di Business Central in Teams" viene visualizzato dopo l'installazione dell'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams. Questo riquadro non fornisce alcun valore in sé e può essere nascosto in sicurezza.

In qualità di amministratore, con autorizzazioni di amministratore di Azure Active Directory, puoi nascondere il riquadro mediante i seguenti passaggi:

1. Accedi all'[interfaccia di amministrazione di Azure Active Directory](https://aad.portal.azure.com/).
2. Seleziona **App aziendali**, quindi seleziona **Connettore del servizio di integrazione di Business Central in Teams**.
3. Seleziona **Proprietà**, quindi imposta **Visibile agli utenti** su **No**.
4. Seleziona **Salva**.

> [!NOTE]
> Ci vorrà del tempo prima che questa modifica abbia effetto.


## <a name="see-also"></a>Vedere anche

[Panoramica dell'integrazione di [!INCLUDE [prod_short](includes/prod_short.md)] e Microsoft Teams](across-teams-overview.md)  
[Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Domande frequenti su Teams](teams-faq.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]