---
title: Gestione dell'integrazione Microsoft Teams con Business Central | Microsoft Docs
description: Gestione dell'integrazione di Business Central con Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: ecb3f88bf14c74f026f10fd49efe28f189036589
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882207"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Gestione dell'integrazione di Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Questo articolo fornisce una panoramica di ciò che è possibile fare come amministratore per controllare l'integrazione di Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Requisiti minimi

Questa sezione descrive i requisiti minimi per il funzionamento dell'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams.

- Licenze richieste

    Questa tabella offre una panoramica delle licenze necessarie per il funzionamento dell'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams.

    |Quale|Licenza Teams|Licenza di [!INCLUDE [prod_short](includes/prod_short.md)]|
    |----|---|---|
    |Ricerca di contatti di [!INCLUDE [prod_short](includes/prod_short.md)].|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|
    |Incollare un collegamento a un record [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione e inviarla come scheda.|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|
    |Visualizzare una scheda di un record [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione.|![segno di spunta](media/check.png "selezionato")||
    |Visualizzare altri dettagli di una scheda per un record [!INCLUDE [prod_short](includes/prod_short.md)] in una conversazione.|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|

- Consentire le anteprime URL

    L'impostazione dei criteri **Consenti anteprime URL** deve essere attivata. In caso contrario, non è possibile generare una scheda per i collegamenti di [!INCLUDE [prod_short](includes/prod_short.md)] incollati in una conversazione di Teams. Per ulteriori informazioni su questa impostazione, vedere [Gestire i criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Gestione dell'app [!INCLUDE [prod_short](includes/prod_short.md)] (facoltativo)

In qualità di amministratore di Teams, è possibile gestire tutte le app per l'organizzazione, inclusa l'app [!INCLUDE [prod_short](includes/prod_short.md)]. È possibile approvare o installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per l'organizzazione, impedire all'utente di installare l'app e altro ancora.

Per ulteriori informazioni, vedere i seguenti articoli nella documentazione di Microsoft Teams:

- [Gestire le app nell'interfaccia di amministrazione di Microsoft Teams](/MicrosoftTeams/manage-apps)
- [Gestire i criteri di configurazione dell'app in Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>In [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Requisiti minimi

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

## <a name="managing-privacy-and-compliance"></a>Gestione della privacy e della conformità 

Microsoft Teams fornisce controlli estesi per la conformità e la gestione di dati sensibili o di identificazione personale, compresi i dati aggiunti a chat e canali mediante l'app [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="understanding-where-prod_short-cards-are-stored"></a>Informazioni su dove vengono memorizzate le schede di [!INCLUDE [prod_short](includes/prod_short.md)] 

Dopo che una scheda è stata inviata a una chat, la scheda e i campi visualizzati nella scheda vengono copiati in Teams. Queste informazioni sono soggette ai criteri di Teams per l'organizzazione, come i criteri di conservazione dei dati. Quando si visualizzano i dettagli della scheda, i dati nella finestra dei dettagli non sono memorizzati in Teams. I dati rimangono memorizzati in [!INCLUDE [prod_short](includes/prod_short.md)] e verranno recuperati da Teams solo quando l'utente sceglie di visualizzare i dettagli. 

- Per ulteriori informazioni sulla posizione in cui Teams memorizza tali dati, vedi [Posizione dei dati in Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Per altre informazioni sui criteri di conservazione in Teams, vedi [Criteri di conservazione in Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Limitazione della condivisione delle schede 

Per impedire a utenti o gruppi specifici di inviare schede a chat o canali, devi impostare criteri di messaggistica che disattivano l'impostazione **Anteprime URL**. Per ulteriori informazioni su questa impostazione, vedi [Gestire i criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams). 

È inoltre possibile utilizzare barriere informative per impedire a individui o gruppi di comunicare tra loro. Per saperne di più, vedi [Barriere informative in Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Le funzionalità di prevenzione della perdita di dati nel Centro sicurezza e conformità di Microsoft 365 non possono essere applicate in modo specifico alle schede. Possono tuttavia essere applicate ai messaggi di chat che contengono le schede. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Rispondere alle richieste di dati

Per consentire ai membri del team e ai proprietari del team di eliminare i messaggi che contengono schede sensibili devi impostare criteri di messaggistica, come: **I proprietari possono eliminare i messaggi inviati** e **Gli utenti possono eliminare i messaggi inviati**. Per ulteriori informazioni, vedi [Gestire criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams).

Le funzionalità di conformità eDiscovery e di ricerca di contenuto nel Centro sicurezza e conformità di Microsoft 365 non possono essere applicate anche alle schede.

Poiché i dati delle schede in Teams sono una copia dei dati in [!INCLUDE [prod_short](includes/prod_short.md)], puoi anche usare le funzionalità di [!INCLUDE [prod_short](includes/prod_short.md)] per esportare i dati di un cliente se richiesto. Per ulteriori informazioni sulla privacy in [!INCLUDE [prod_short](includes/prod_short.md)], vedi [Domande frequenti sulla privacy per i clienti di Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Vedere anche
[Panoramica dell'integrazione di [!INCLUDE [prod_short](includes/prod_short.md)] e Microsoft Teams](across-teams-overview.md)  
[Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Domande frequenti su Teams](teams-faq.md)  
[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]