---
title: Gestione della personalizzazione come amministratore in Business Central | Documenti Microsoft
description: Informazioni su come personalizzare l'interfaccia utente in base alle esigenze professionali.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 4914c0b7c269d5f725f33c839eb677455293cea0
ms.contentlocale: it-it
ms.lasthandoff: 06/01/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Gestione della personalizzazione come amministratore
<!--NAV in the Web client-->
Gli utenti possono personalizzare l'area di lavoro per adattarla alle proprie preferenze. In qualità di amministratore, è possibile controllare e gestire la personalizzazione disabilitando la possibilità per gli utenti di personalizzare le pagine e cancellando le personalizzazioni di pagina che gli utenti hanno effettuato.

## <a name="disable-personalization-for-a-profile"></a>Disabilitare la personalizzazione per un profilo
È possibile impedire a tutti gli utenti che appartengono a un profilo specifico di personalizzare le proprie pagine.
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Profili**, quindi scegliere il collegamento correlato.
2.  Selezionare dall'elenco il profilo che si desidera modificare.
3. Selezionare la casella di controllo **Disabilita personalizzazione** e quindi fare clic sul pulsante **OK**.

## <a name="clear-user-personalizations"></a>Cancellare le personalizzazioni dell'utente

La cancellazione delle modifiche di personalizzazione della pagina ripristina la pagina al layout originale prima che fosse apportata qualsiasi personalizzazione. Ci sono due modi per eliminare le personalizzazioni che gli utenti hanno apportato alle pagine: utilizzando la pagina **Elimina personalizzazione utente** o la pagina **Scheda personalizzazione utente**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Eliminare le personalizzazioni dell'utente tramite la pagina Elimina personalizzazione utente

La pagina **Elimina personalizzazione utente** consente di eliminare la personalizzazione in base alla pagina e all'utente.

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Elimina personalizzazione utente**, quindi scegliere il collegamento correlato.

    Nella pagina vengono elencate tutte le pagine che sono state personalizzate e l'utente a cui appartengono.

    >[!NOTE]
    > Un segno di spunta nelle colonne **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che gestiva la personalizzazione in modo diverso rispetto ad adesso. Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina. Per ulteriori informazioni, vedere [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).

2. Selezionare la voce che si desidera eliminare, quindi scegliere l'azione **Elimina**.

    L'utente visualizzerà le modifiche dopo l'accesso successivo.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Eliminare le personalizzazioni dell'utente tramite la pagina Scheda personalizzazione utente

La pagina **Scheda personalizzazione utente** consente di eliminare la personalizzazione in tutte le pagine per un utente specifico. Questa operazione richiede l'autorizzazione di scrittura per la tabella **Profilo** 2000000072.

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Personalizzazione utente**, quindi scegliere il collegamento correlato.

    Nella pagina **Personalizzazione utente** vengono elencati tutti gli utenti che potenzialmente dispongono di pagine personalizzate. Se non è presente un utente nell'elenco, significa che non dispone di pagine personalizzate.

2. Selezionare l'utente dalla lista, quindi scegliere l'azione **Modifica**.

3.  Nella scheda **Azioni**, scegliere **Cancella pagine personalizzate**.

    L'utente visualizzerà le modifiche dopo l'accesso successivo.

## <a name="see-also"></a>Vedi anche
[Personalizzazione dell'area di lavoro](ui-personalization-user.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  

