---
title: Utilizzo dei dati di Business Central in Microsoft Teams | Microsoft Docs
description: Informazioni su come utilizzare l'app Business Central per Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989425"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Utilizzo dei dati Business Central in Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] offre un'app che connette Microsoft Teams ai dati aziendali in [!INCLUDE [prodshort](includes/prodshort.md)], in modo da poter condividere rapidamente i dettagli tra i membri del team e rispondere più rapidamente alle richieste. In questo articolo viene descritto come utilizzare l'app per condividere i dati [!INCLUDE [prodshort](includes/prodshort.md)] con i colleghi in una conversazione di Teams.

## <a name="overview"></a>Sintesi

L'app [!INCLUDE [prodshort](includes/prodshort.md)] consente di:

- Copiare un collegamento a qualsiasi record di Business Central e incollarlo in una conversazione di Teams per condividerlo con i colleghi. Il collegamento viene aperto in una scheda interattiva compatta che visualizza le informazioni sul record.
- Una volta nella conversazione, l'utente e i colleghi possono visualizzare ulteriori dettagli sul record, modificare i dati e intraprendere azioni, senza uscire da Teams.

[![Integrazione di Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Prerequisiti

- Avere accesso a Microsoft Teams.
- Avere installato l'app [!INCLUDE [prodshort](includes/prodshort.md)] in Teams. Per ulteriori informazioni, vedere [Installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] per Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Tutti i partecipanti a una conversazione di Teams saranno in grado di visualizzare le schede per i record di Business Central inviati alla conversazione. Tuttavia per visualizzare maggiori dettagli sui record, utilizzando i pulsanti **Dettagli** o **Apri nuova finestra** in una scheda, sarà necessario accedere a [!INCLUDE [prodshort](includes/prodshort.md)]. Per ulteriori informazioni, vedere [Gestione dell'integrazione di Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Includere una scheda Business Central in una conversazione di Teams

1. Accedere a [!INCLUDE [prodshort](includes/prodshort.md)] utilizzando il browser.
2. Aprire il record che si desidera condividere.

    L'app è progettata per visualizzare le pagine di tipo scheda da [!INCLUDE [prodshort](includes/prodshort.md)]. Quindi aprire una pagina che visualizza un singolo record, come un articolo, un cliente o un ordine di vendita. Non è possibile utilizzarla per la Gestione ruolo utente o le pagine che visualizzano più record in un elenco.

3. Copiare l'intero URL dalla barra degli indirizzi del browser.

   ![Copiare l'URL di Business Central dal browser](media/teams-url.png)
4. Accedere a Teams e avviare una conversazione, che può essere una chat con una persona, un gruppo di persone o un canale del team.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Incollare l'URL nella casella in cui si aggiunge un messaggio.

   ![Incollare l'URL di Business Central in Teams](media/teams-paste-url.png)
6. La prima volta che si incolla un collegamento in una conversazione, verrà richiesto di accedere a [!INCLUDE [prodshort](includes/prodshort.md)] e fornire il consenso all'app per il recupero dei dati. Seguire le istruzioni sullo schermo.

    > [!NOTE]
    > È necessario eseguire questo passaggio solo una volta.

7. Attendere mentre viene generata una scheda nella casella del messaggio.

8. Quando viene visualizzata la scheda, esaminare attentamente il contenuto della scheda per eventuali informazioni sensibili prima di inviare il messaggio. Questo passaggio è importante perché una volta inviato il messaggio, tutti i partecipanti alla conversazione possono vedere la scheda.

9. Se la scheda ha l'aspetto desiderato, selezionare **Invia** per inviarla alla conversazione.

    > [!TIP]
    > Dopo che viene visualizzata la scheda e prima di selezionare **Invia** è possibile eliminare l'URL incollato, se desiderato.

10. Per visualizzare ulteriori dettagli o apportare modifiche al record, selezionare **Dettagli**.

    La pagina dei dettagli è simile a quella che viene visualizzata in [!INCLUDE [prodshort](includes/prodshort.md)]. Tuttavia è leggermente adattata per Teams. Al termine della visualizzazione e delle modifiche, chiudere la finestra per tornare alla conversazione di Teams.

    > [!NOTE]
    > Eventuali modifiche apportate non si rifletteranno nella scheda fino alla volta successiva che si incolla il collegamento in una conversazione.

## <a name="see-also"></a>Vedere anche

[Panoramica dell'integrazione di Business Central e Microsoft Teams](across-teams-overview.md)  
[Installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] per Microsoft Teams](across-install-app-for-teams.md)  
[Sviluppo per l'integrazione di Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Introduzione](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
