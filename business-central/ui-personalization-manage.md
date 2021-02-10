---
title: Personalizzare pagine per ruoli | Microsoft Docs
description: Informazioni su come personalizzare l'interfaccia utente per un profilo (ruolo) di modo che tutti gli utenti assegnati a quel ruolo vedano un'area di lavoro personalizzata.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cf7f261f945828b78db55cde0dda70d12b158127
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760344"
---
# <a name="customize-pages-for-profiles"></a>Personalizzare pagine per profili
Gli utenti possono personalizzare le pagine della propria area di lavoro per adattarle alle proprie preferenze. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

Gli amministratori possono personalizzare le pagine per un profilo, in base al ruolo aziendale o al reparto correlato, ad esempio, in modo che tutti gli utenti a cui è assegnato il profilo visualizzino il layout di pagina personalizzato. L'amministratore personalizza le pagine utilizzando le stesse funzionalità utilizzate dagli utenti quando personalizzano le pagine.

> [!NOTE]
> L'uso aziendale tipico di un profilo è un ruolo. Un profilo viene quindi denominato *Profilo (ruolo)* nell'interfaccia utente.

La personalizzazione delle pagine inizia dalla pagina **Profili (ruoli)**, ovvero il punto di partenza dell'amministratore per la gestione dei profili degli utenti in singole schede profilo. Oltre a personalizzare il layout delle pagine, si controllano varie altre impostazioni per i profili nella pagina **Profilo (ruolo)** di ogni profilo. Per ulteriori informazioni, vedere [Gestire i profili](admin-users-profiles-roles.md).

## <a name="to-customize-pages-for-a-profile"></a>Per personalizzare pagine per un profilo
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Profili (Ruoli)** e quindi scegliere il collegamento correlato.
2. Selezionare la riga per il profilo per cui si desidera personalizzare le pagine, quindi scegliere l'azione **Modifica**.
3. Scegliere l'azione **Personalizza pagine**.

    [!INCLUDE[prod_short](includes/prod_short.md)] viene aperto in una nuova scheda del browser per il profilo selezionato con il banner **Personalizzazione** attivato. Il banner **Personalizzazione** offre le stesse funzionalità del banner **Personalizzazione** disponibile per gli utenti.

4. Personalizzare le pagine in base alle esigenze del ruolo o del reparto in questione, proprio come farebbe un utente durante la personalizzazione. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

    > [!NOTE]
    > Per navigare durante la personalizzazione, utilizzare CTRL+clic su un'azione se è evidenziata dalla freccia.

5. Al termine della modifica del layout in una o più pagine, selezionare il pulsante **Fatto** nel banner **Personalizzazione**.
6. Chiudere la scheda del browser.

La personalizzazione delle pagine è ora registrata per il profilo.

## <a name="to-view-all-customized-pages-for-a-profile"></a>Per visualizzare tutte le pagine personalizzate per un profilo

È possibile ottenere una panoramica di quali pagine sono personalizzate per un profilo, ad esempio per pianificare quali personalizzare ulteriormente o eliminare.

- Nella pagina **Profilo (ruolo)**, scegliere l'azione **Gestisci pagine personalizzate**.

Nella pagina **Pagine personalizzate** è possibile eliminare le personalizzazioni e risolvere i problemi analizzando i potenziali problemi.  

## <a name="to-delete-all-customizations-for-a-profile"></a>Per eliminare tutte le personalizzazioni per un profilo
È possibile annullare tutte le personalizzazioni apportate per un profilo. Le personalizzazioni introdotte con un'estensione e le personalizzazioni eseguite da un utente non verranno eliminate. È possibile eliminare tutte le personalizzazioni con un'altra azione. Per ulteriori informazioni, vedere [Per eliminare tutte le personalizzazioni eseguite da un utente](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Nella pagina **Profilo (ruolo)** per un profilo personalizzato, selezionare l'azione **Cancella pagine personalizzate**.

Il layout delle pagine per il profilo viene ripristinato al layout predefinito.  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a>Per eliminare la personalizzazione di specifiche pagine per un profilo
È possibile eliminare personalizzazioni di singole pagine eseguite per un profilo. Le personalizzazioni introdotte con un'estensione e le personalizzazioni eseguite da un utente non verranno eliminate. È possibile eliminare personalizzazioni di specifiche pagine con un'altra azione. Per ulteriori informazioni, vedere [Per eliminare le personalizzazioni per pagine specifiche](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Nella pagina **Profilo (ruolo)**, scegliere l'azione **Gestisci pagine personalizzate**.
2. Nella pagina **Pagine personalizzate** selezionare una o più righe per le personalizzazioni che si desidera eliminare, quindi selezionare l'azione **Elimina**.

Il layout delle pagine selezionate viene adattato alle modifiche apportate.

## <a name="see-also"></a>Vedere anche

[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
