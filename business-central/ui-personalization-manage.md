---
title: Gestione della personalizzazione come amministratore in Business Central | Documenti Microsoft
description: Informazioni su come personalizzare l'interfaccia utente in base alle esigenze professionali.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 08/16/2019
ms.author: jswymer
ms.openlocfilehash: 268d61e05f84643abe8eeeb283bd035e0247fe1c
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887739"
---
# <a name="managing-personalization-as-an-administrator"></a>Gestione della personalizzazione come amministratore

 Gli utenti possono personalizzare l'area di lavoro per adattarla alle proprie preferenze. In veste di amministratore, si controlla e si gestisce la personalizzazione:

-   Abilitando o disabilitando la funzionalità di personalizzazione per l'intera applicazione (solo installazione locale).
-   Abilitando o disabilitando la funzionalità di personalizzazione per gli utenti di un profilo specifico.
-   Annullando qualsiasi personalizzazione di pagina che gli utenti hanno effettuato.

## <a name="EnablePersonalization"></a>Per abilitare o disabilitare la personalizzazione (solo locale)

Per impostazione predefinita, la personalizzazione non è abilitata nel client. La personalizzazione viene abilitata o disabilitata modificando il file di configurazione (navsettings.json) dell'istanza del server Web Business Central che serve i client.

1. Per abilitare la personalizzazione, aggiungere la seguente riga nel file navsettings.json:

    ```
    "PersonalizationEnabled": "true"
    ```

    Per disabilitare la personalizzazione, rimuovere questa riga o modificarla in:

    ```
    "PersonalizationEnabled": "false"
    ```

    Per ulteriori informazioni su come modificare il file navsettings.json, vedere [Modificare direttamente il file navsettings.json](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Generare e scaricare i simboli dell'applicazione.

    Questo passaggio è facoltativo e non necessario per abilitare la personalizzazione. Tuttavia, garantisce la possibilità di personalizzare le nuove pagine create dagli sviluppatori.

    1. Innanzitutto, generare i simboli eseguendo finsql.exe con il comando `generatesymbolreference`. Il file finsql.exe si trova nella cartella di installazione per [!INCLUDE[server](includes/server.md)] e Dynamics NAV Development Environment (CSIDE). Per generare i simboli, aprire un prompt dei comandi, accedere ala directory in cui si trova il file ed eseguire il comando seguente:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Ad esempio:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Per ulteriori informazioni, vedere [Eseguire C/SIDE e AL contemporaneamente](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Configurare l'istanza di [!INCLUDE[nav_server_md](includes/nav_server_md.md)] per **Abilitare il collegamento dei riferimenti dei simboli dell'applicazione all'avvio del server** (EnableSymbolLoadingAtServerStartup). Per ulteriori informazioni, vedere [Configurazione di Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Per disabilitare la personalizzazione per un profilo

È possibile impedire a tutti gli utenti che appartengono a un profilo specifico di personalizzare le proprie pagine.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Profili** e scegliere il collegamento correlato.
2. Selezionare dall'elenco il profilo che si desidera modificare.
3. Selezionare la casella di controllo **Disabilita personalizzazione** e quindi fare clic sul pulsante **OK**.

> [!NOTE]  
> In Business Central online, è possibile disabilitare la personalizzazione solo per un profilo tenant e non per i profili di sistema. 

## <a name="to-clear-user-personalizations"></a>Per eliminare personalizzazioni dell'utente

La cancellazione delle modifiche di personalizzazione della pagina ripristina la pagina al layout originale prima che fosse apportata qualsiasi personalizzazione. Ci sono due modi per eliminare le personalizzazioni che gli utenti hanno apportato alle pagine: utilizzando la pagina **Elimina personalizzazione utente** o la pagina **Scheda personalizzazione utente**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Per eliminare le personalizzazioni dell'utente tramite la pagina Elimina personalizzazione utente

La pagina **Elimina personalizzazione utente** consente di eliminare la personalizzazione in base alla pagina e all'utente.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina personalizzazione utente** e quindi scegliere il collegamento correlato.

    Nella pagina vengono elencate tutte le pagine che sono state personalizzate e l'utente a cui appartengono.

    >[!NOTE]
    > Un segno di spunta nelle colonne **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che gestiva la personalizzazione in modo diverso rispetto ad adesso. Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina. Per ulteriori informazioni, vedere [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).

2. Selezionare la voce che si desidera eliminare, quindi scegliere l'azione **Elimina**.

    L'utente visualizzerà le modifiche dopo l'accesso successivo.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Per eliminare le personalizzazioni dell'utente tramite la pagina Scheda personalizzazione utente

La pagina **Scheda personalizzazione utente** consente di eliminare la personalizzazione in tutte le pagine per un utente specifico. Questa operazione richiede l'autorizzazione di scrittura per la tabella **Profilo** 2000000072.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Personalizzazione utente** e quindi scegliere il collegamento correlato.

    Nella pagina **Personalizzazione utente** vengono elencati tutti gli utenti che potenzialmente dispongono di pagine personalizzate. Se non è presente un utente nell'elenco, significa che non dispone di pagine personalizzate.

2. Selezionare l'utente dalla lista, quindi scegliere l'azione **Modifica**.

3. Nella scheda **Azioni**, scegliere **Cancella pagine personalizzate**.

    L'utente visualizzerà le modifiche dopo l'accesso successivo.

## <a name="see-also"></a>Vedi anche
[Personalizzazione dell'area di lavoro](ui-personalization-user.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
