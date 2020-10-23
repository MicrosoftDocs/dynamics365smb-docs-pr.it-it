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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989360"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Gestione dell'integrazione di Microsoft Teams con Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Questo articolo fornisce una panoramica di ciò che è possibile fare come amministratore per controllare l'integrazione di Microsoft Teams con [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Requisiti minimi

Questa sezione descrive i requisiti minimi per il funzionamento dell'app [!INCLUDE [prodshort](includes/prodshort.md)] in Teams.

- Licenze richieste

    Questa tabella offre una panoramica delle licenze necessarie per il funzionamento dell'app [!INCLUDE [prodshort](includes/prodshort.md)] in Teams.

    |Quale|Licenza Teams|Licenza Business Central|
    |----|---|---|
    |Incollare un collegamento a un record [!INCLUDE [prodshort](includes/prodshort.md)] in una conversazione e inviarla come scheda.|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|
    |Visualizzare una scheda di un record [!INCLUDE [prodshort](includes/prodshort.md)] in una conversazione.|![segno di spunta](media/check.png "selezionato")||
    |Visualizzare altri dettagli di una scheda per un record [!INCLUDE [prodshort](includes/prodshort.md)] in una conversazione.|![segno di spunta](media/check.png "selezionato")|![segno di spunta](media/check.png "selezionato")|

- Consentire le anteprime URL

    L'impostazione dei criteri **Consenti anteprime URL** deve essere attivata. In caso contrario, non è possibile generare una scheda per i collegamenti di Business Central incollati in una conversazione di Teams. Per ulteriori informazioni su questa impostazione, vedere [Gestire i criteri di messaggistica in Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Gestione dell'app Business Central (opzionale)

In qualità di amministratore di Teams, è possibile gestire tutte le app per l'organizzazione, inclusa l'app [!INCLUDE [prodshort](includes/prodshort.md)]. È possibile approvare o installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] per l'organizzazione, impedire all'utente di installare l'app e altro ancora.

Per ulteriori informazioni, vedere i seguenti articoli nella documentazione di Microsoft Teams:

- [Gestire le app nell'interfaccia di amministrazione di Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Gestire i criteri di configurazione dell'app in Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>In [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Requisiti minimi

- Versione di [!INCLUDE [prodshort](includes/prodshort.md)]:

    Secondo ciclo di rilascio del 2020 (versione 17) di [!INCLUDE [prodshort](includes/prodshort.md)] o successiva. L'integrazione di Teams è supportata solo per [!INCLUDE [prodshort](includes/prodshort.md)] online, non in locale.

- La codeunit **2718 Provider di riepilogo pagine** è pubblicata come servizio Web:

    Questa codeunit viene pubblicata come servizio Web per impostazione predefinita. La codeunit fa parte dell'applicazione di sistema [!INCLUDE [prodshort](includes/prodshort.md)]. Viene utilizzata per ottenere i dati del campo per una pagina [!INCLUDE [prodshort](includes/prodshort.md)] aggiunta a una conversazione di Teams. 

- Autorizzazioni utente:

    Per la maggior parte, le pagine e i dati che gli utenti possono visualizzare e modificare in una conversazione di Teams sono controllati dalle autorizzazioni in [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Per incollare un collegamento [!INCLUDE [prodshort](includes/prodshort.md)] in una conversazione di Teams e farlo espandere in una scheda, gli utenti devono disporre almeno dell'autorizzazione di lettura sulla pagina e sui relativi dati.
    - Una volta che una scheda è stata inviata a una conversazione, qualsiasi utente in quella conversazione può visualizzare quella scheda senza autorizzazione per Business Central.
    - Per visualizzare ulteriori dettagli per una scheda o aprire il record in [!INCLUDE [prodshort](includes/prodshort.md)], gli utenti devono disporre dell'autorizzazione di lettura sulla pagina e sui suoi dati.
    - Per modificare i dati, l'utente deve disporre delle autorizzazioni per la modifica.
    
    Per informazioni sulle autorizzazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

## <a name="see-also"></a>Vedere anche
[Panoramica dell'integrazione di Business Central e Microsoft Teams](across-teams-overview.md)  
[Installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Introduzione](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
