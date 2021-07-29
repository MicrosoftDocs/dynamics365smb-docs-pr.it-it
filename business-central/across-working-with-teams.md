---
title: Condivisione dei record di Business Central in Microsoft Teams
description: Informazioni su come utilizzare l'app Business Central per Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: fb134ce04cb6b53f2432f0f371d7ca82411f0cee
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444020"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a>Condivisione dei record di Business Central in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] offre un'app che connette Microsoft Teams ai dati aziendali in [!INCLUDE [prod_short](includes/prod_short.md)], in modo da poter condividere rapidamente i dettagli tra i membri del team e rispondere più rapidamente alle richieste. In questo articolo viene descritto come utilizzare l'app per condividere i record di [!INCLUDE [prod_short](includes/prod_short.md)], come un cliente, un ordine vendita o una fattura, con i colleghi in una conversazione di Teams.

## <a name="overview"></a>Sintesi

L'app [!INCLUDE [prod_short](includes/prod_short.md)] consente di:

- Copiare un collegamento a qualsiasi record di Business Central e incollarlo in una conversazione di Teams per condividerlo con i colleghi. L'app espanderà il collegamento in una scheda interattiva compatta che visualizza le informazioni sul record.
- Una volta nella conversazione, l'utente e i colleghi possono visualizzare ulteriori dettagli sul record, modificare i dati e intraprendere azioni, senza uscire da Teams.

[![Integrazione di Teams con Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Prerequisiti

- Avere accesso a Microsoft Teams.
- Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams. Per ulteriori informazioni, vedere [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Tutti i partecipanti a una conversazione di Teams saranno in grado di visualizzare le schede per i record di Business Central inviati alla conversazione. Tuttavia per visualizzare maggiori dettagli sui record, utilizzando i pulsanti **Dettagli** o **Apri nuova finestra** in una scheda, sarà necessario accedere a [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Gestione dell'integrazione di Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Includere una scheda Business Central in una conversazione di Teams

1. Accedere a [!INCLUDE [prod_short](includes/prod_short.md)] utilizzando il browser.
2. Aprire il record che si desidera condividere.

    L'app è progettata per visualizzare le pagine di tipo scheda da [!INCLUDE [prod_short](includes/prod_short.md)]. Quindi aprire una pagina che visualizza un singolo record, come un articolo, un cliente o un ordine di vendita. Non è possibile utilizzarla per la Gestione ruolo utente o le pagine che visualizzano più record in un elenco.

3. Copiare l'intero URL dalla barra degli indirizzi del browser.

   ![Copia l'URL di Business Central dal browser.](media/teams-url-v2.png)
4. Accedere a Teams e avviare una conversazione, che può essere una chat con una persona, un gruppo di persone o un canale del team.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Incollare l'URL nella casella del messaggio in cui si compone un messaggio.

   ![Incolla l'URL di Business Central in Teams.](media/teams-paste-url-v2.png)
6. La prima volta che si incolla un collegamento in una conversazione, verrà richiesto di accedere a [!INCLUDE [prod_short](includes/prod_short.md)] e fornire il consenso all'app per il recupero dei dati. Seguire le istruzioni sullo schermo.

    > [!NOTE]
    > È necessario eseguire questo passaggio solo una volta.

7. Attendere mentre viene generata una scheda nella casella del messaggio.

8. Quando viene visualizzata la scheda, esaminare attentamente il contenuto della scheda per eventuali informazioni sensibili prima di inviare il messaggio. Questo passaggio è importante perché una volta inviato il messaggio, tutti i partecipanti alla conversazione possono vedere la scheda.

9. Se la scheda ha l'aspetto desiderato, selezionare **Invia** per inviarla alla conversazione.

    > [!TIP]
    > Dopo che viene visualizzata la scheda e prima di selezionare **Invia** è possibile eliminare l'URL incollato, se desiderato.

10. Per visualizzare ulteriori dettagli o apportare modifiche al record visualizzato nella scheda, selezionare **Dettagli**. Per ulteriori informazioni, vedere la sezione seguente.

## <a name="view-card-details"></a>Visualizzare i dettagli della scheda

Una volta che una scheda è stata inviata a una conversazione, tutti i partecipanti con le [autorizzazioni adeguate](admin-teams-integration.md#permissions) possono selezionare **Dettagli** per aprire una finestra che visualizza ulteriori informazioni sul record ed eventualmente apportare modifiche al record. Non importa se sei tu a inviare la scheda o a riceverla. La funzionalità **Dettagli** è particolarmente utile per i destinatari, perché fornisce loro rapidamente informazioni concise e mirate sul record, anziché dover eseguire la scansione dell'intero record.

La finestra dei dettagli è simile a quella che viene visualizzata nel record di [!INCLUDE [prod_short](includes/prod_short.md)]. Tuttavia è leggermente adattata per Teams. Al termine della visualizzazione e delle modifiche, chiudere la finestra per tornare alla conversazione di Teams.

Ecco un paio di cose da tenere a mente quando si utilizzano i dettagli della scheda:

- Per visualizzare i dettagli della scheda, gli utenti devono disporre dell'autorizzazione per la pagina e i relativi dati in [!INCLUDE [prod_short](includes/prod_short.md)].
- Le schede nelle chat di Teams non vengono aggiornate automaticamente alle modifiche. Tutte le modifiche salvate in un record nella finestra dei dettagli vengono salvate in [!INCLUDE [prod_short](includes/prod_short.md)]. Ma la scheda in Teams non mostrerà le modifiche nella conversione, finché non incollerai nuovamente il collegamento.

Per ulteriori informazioni sull'utilizzo delle schede e sui dettagli delle schede, vedi [Domande frequenti su Teams](teams-faq.md).

## <a name="see-also"></a>Vedere anche

[Panoramica dell'integrazione di Business Central e Microsoft Teams](across-teams-overview.md)  
[Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Domande frequenti su Teams](teams-faq.md)  
[Ricerca di clienti, fornitori e altri contatti da Microsoft Teams](across-search-contacts-teams.md)  
[Modifica della società e di altre impostazioni in Teams](across-teams-settings.md)  
[Risoluzione dei problemi relativi a Teams](admin-teams-troubleshooting.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]