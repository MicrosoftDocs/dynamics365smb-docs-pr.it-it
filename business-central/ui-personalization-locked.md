---
title: Perché non è possibile personalizzare una pagina | Documenti Microsoft
description: Descrizione dei motivi per cui non è possibile personalizzare una pagina e delle azioni che è possibile intraprendere per sbloccare la pagina e personalizzarla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796764"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Perché non è possibile personalizzare una pagina

Vi sono due condizioni che impediscono la personalizzazione di una pagina. La pagina è protetta (come indicato da ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione")) oppure è bloccata (come indicato da ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata"))

## <a name="locked-from-personalizing"></a>Protetta dalla personalizzazione

Se è presente un'icona ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") nel banner **Personalizzazione** quando viene aperta una pagina (come mostrato), ciò indica che attualmente non sono consentite ulteriori modifiche di personalizzazione nella pagina.

![Blocco della personalizzazione](media/personalization-locked.png "Blocco della personalizzazione")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Ciò può avvenire per due motivi:

1. La pagina è stata personalizzata in precedenza, ma utilizzando una versione antecedente del prodotto. Il modo in cui la personalizzazione funziona in background è stato modificato dall'ultima volta che è stata personalizzata la pagina. Purtroppo, il vecchio e il nuovo modo non funzionano insieme.

2. Finora, è stato utilizzato solo [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] per personalizzare la pagina.

### <a name="unlocking-the-page"></a>Sblocco della pagina

Se si desidera sbloccare una pagina e continuare a personalizzarla, scegliere ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") e quindi **Sblocca**.  

Prima di sbloccare la pagina, considerare quanto segue:

- La personalizzazione corrente della pagina verrà eliminata. Per la pagina verrà utilizzato il layout originale e sarà necessario cominciare da zero.

- In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la pagina rimarrà così com'è e non verrà alterata dalle modifiche della nuova personalizzazione effettuate nel client Business Central. In seguito, la personalizzazione in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] e quella nel client Business Central verranno completate indipendentemente l'una dall'altra.

## <a name="blocked-from-personalizing"></a>Bloccata per la personalizzazione

Se esiste un'icona ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata") nel banner Personalizzazione, ciò significa che qualsiasi personalizzazione della pagina è bloccata.

![Blocco della personalizzazione](media/personalization-blocked.png "Blocco della personalizzazione")

Ciò è dovuto al fatto che Gestione ruolo utente o il ruolo attualmente associato al proprio account utente modifica questa pagina specificatamente per il ruolo. Contattare l'amministratore per assistenza oppure, se utile, cercare di passare a una Gestione ruolo utente (da [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "Passare direttamente alla pagina Impostazioni utente in Business Central")) che include l'adattamento al ruolo per questa pagina.

## <a name="see-also"></a>Vedere anche
[Personalizzazione dell'area di lavoro](ui-personalization-manage.md)  
[Gestione della personalizzazione](ui-personalization-manage.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
