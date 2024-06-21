---
title: Perché non è possibile personalizzare una pagina
description: È possibile che la personalizzazione di una pagina sia bloccata. Leggi qui cosa puoi fare per sbloccarla in modo da poterla personalizzare.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Perché non è possibile personalizzare una pagina

Vi sono due condizioni che impediscono la personalizzazione di una pagina. La pagina è protetta (come indicato dall'icona ![Blocco della personalizzazione.](media/personalization-lock-icon.png "Blocco della personalizzazione")) oppure è bloccata (come indicato dall'icona ![Personalizzazione bloccata.](media/personalization-blocked-icon.png "Personalizzazione bloccata")) .

## Protetta dalla personalizzazione

Se c'è un'icona ![Personalizza blocco.](media/personalization-lock-icon.png "Blocco della personalizzazione") nel banner **Personalizzazione** quando viene aperta una pagina, indica che attualmente non sono consentite ulteriori modifiche di personalizzazione nella pagina.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

I motivi possono essere due:

1. La pagina è stata personalizzata in precedenza, ma utilizzando una versione antecedente del prodotto. Il modo in cui la personalizzazione funziona in background è stato modificato dall'ultima volta che è stata personalizzata la pagina. Purtroppo, il vecchio e il nuovo modo non funzionano insieme.

2. Finora, è stato utilizzato solo [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] ora deprecato per personalizzare la pagina.

### Sblocco della pagina

Se si desidera sbloccare una pagina e continuare a personalizzarla, scegliere l'icona ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") e quindi scegliere **Sblocca**.  

> [!CAUTION]
> La personalizzazione corrente della pagina verrà eliminata. Per la pagina verrà utilizzato il layout originale e sarà necessario cominciare da zero.  

## Bloccata per la personalizzazione

Se esiste un'icona ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata") nel banner **Personalizzazione**, ciò significa che qualsiasi personalizzazione della pagina è bloccata.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Ciò è dovuto al fatto che Gestione ruolo utente o il ruolo attualmente associato al proprio account utente modifica questa pagina specificatamente per il ruolo. Contattare l'amministratore per l'assistenza. In alternativa, provare a passare a un Centro ruoli che include l'adattamento dei ruoli per questa pagina. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).

## Vedere anche

[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Personalizzare pagine per profili](ui-personalization-manage.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
