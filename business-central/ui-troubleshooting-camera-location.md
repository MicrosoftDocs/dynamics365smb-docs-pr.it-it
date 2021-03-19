---
title: 'Risoluzione dei problemi: accesso alla fotocamera e alla posizione'
description: In questo articolo viene descritto come risolvere i problemi relativi all'accesso alle informazioni sulla fotocamera e sulla posizione in Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.openlocfilehash: 68ec41a42898688cbebea341782f0e0bc265341a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393776"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Risoluzione dei problemi: accesso alla fotocamera e alla posizione

È possibile che si riscontrino problemi quando si prova ad accedere alla fotocamera e alle informazioni sulla posizione di un dispositivo da [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile trovare le possibili cause e risoluzioni di questi problemi di seguito.

## <a name="device-must-have-camera-and-location-capabilities"></a>Il dispositivo deve avere fotocamera e funzionalità di posizione

Per accedere alla fotocamera o alla posizione di un utente da un dispositivo, il dispositivo deve avere, rispettivamente, una fotocamera fisica o la capacità di recuperare le informazioni sulla posizione.

Se il dispositivo dispone di fotocamera e funzionalità di posizione, ma si riscontrano ancora problemi, è possibile che alcuni driver necessitino di aggiornamento o reinstallazione. Anche se non si è sicuri, si consiglia sempre di aggiornare il sistema operativo del dispositivo, i driver e il browser alla versione più recente per la migliore esperienza.

## <a name="access-permissions-not-enabled"></a>Autorizzazioni di accesso non abilitate

È necessario abilitare l'accesso generale alla fotocamera e alla posizione dalle impostazioni sulla privacy del dispositivo e concedere esplicitamente a [!INCLUDE[prod_short](includes/prod_short.md)] l'autorizzazione ad accedervi. Ad esempio, per vedere o modificare le autorizzazioni per un dispositivo in esecuzione su Windows, andare a **Impostazioni**, scegliere **Privacy** e quindi **Autorizzazioni dell'app**. 

Per i dispositivi mobili, è necessario concedere le autorizzazioni di accesso alla fotocamera e alla posizione all'app mobile [!INCLUDE[prod_short](includes/prod_short.md)]. Per farlo per un dispositivo iOS, andare a **Impostazioni**, scegliere **Privacy** e quindi **Fotocamera** o **Posizione**. Per i dispositivi Android, andare a **Impostazioni**, scegliere **App e notifiche**, **Avanzate**, **Gestione autorizzazioni** e quindi **Fotocamera** o **Posizione**.

Inoltre, se si sta utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] in un browser, è necessario concedere al sito [!INCLUDE[prod_short](includes/prod_short.md)] l'autorizzazione ad accedere alla fotocamera o alle informazioni sulla posizione. Per visualizzare o modificare le autorizzazioni di un sito nel browser Microsoft Edge, andare a **Impostazioni**, scegliere **Autorizzazioni sito** e quindi **Fotocamera** o **Posizione**. Da notare che questo potrebbe essere diverso per altri browser.

Per impostazione predefinita, il dispositivo o il browser visualizzerà una richiesta per accedere a queste funzionalità quando l'utente le attiva per la prima volta.

> [!NOTE]  
> Alcuni browser precedenti non consentono l'accesso alla fotocamera e alla posizione. Ad esempio, la fotocamera non è disponibile in Internet Explorer o nel browser Edge legacy.

## <a name="web-client-connection-not-secure"></a>Connessione client Web non protetta

La fotocamera e le funzionalità di posizione sono disponibili solo quando si accede al client Web tramite connessioni HTTP protette da SSL, utilizzando lo schema URI `https://`. 

L'unica eccezione è la connessione a `http://localhost`, utilizzato per scopi di sviluppo e test.


## <a name="working-with-virtualization-technologies"></a>Lavorare con le tecnologie di virtualizzazione

Quando ci si collega a [!INCLUDE[prod_short](includes/prod_short.md)] tramite Desktop remoto o un'altra virtualizzazione, l'accesso alla fotocamera o alla posizione potrebbe non essere disponibile. In tal caso, utilizzare invece il sistema fisico.

## <a name="antivirus-software"></a>Software antivirus
Alcuni programmi software antivirus bloccano l'accesso alla fotocamera e alla posizione per impostazione predefinita. Ricordare di controllare le impostazioni del software antivirus.

## <a name="see-also"></a>Vedere anche
[Implementazione della fotocamera in AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implementazione della posizione in AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]