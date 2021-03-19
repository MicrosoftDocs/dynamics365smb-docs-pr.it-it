---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: d58d8d628577f163d36199b8fc5785982aac830a
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493002"
---
Prima di poter configurare il log delle e-mail, è necessario preparare Exchange Online con le [cartelle pubbliche](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). È possibile farlo nell'[interfaccia di amministrazione di Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) oppure è possibile usare la [shell di gestione di Exchange](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Se si desidera utilizzare la [shell di gestione di Exchange](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), è possibile trovare ispirazione su come impostare lo script in uno script di esempio pubblicato nel [repository BCTech](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Il seguente elenco descrive i passaggi principali con i collegamenti per ulteriori informazioni.  

- Creare un ruolo di amministratore per le cartelle pubbliche in base alle informazioni nella seguente tabella:

  |Proprietà        |Valore                     |
  |----------------|--------------------------|
  |Name            |Gestione delle cartelle pubbliche |
  |Ruoli selezionati  |Cartelle pubbliche            |
  |Membri selezionati|L'e-mail dell'account utente che Business Central utilizzerà per eseguire il processo di log delle e-mail|

  Per ulteriori informazioni, vedere [Gestire i gruppi di ruoli](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Creare una nuova cassetta postale della cartella pubblica in base alle informazioni nella seguente tabella:

  |Proprietà        |Valore                     |
  |----------------|--------------------------|
  |Name            |Cassetta postale pubblica            |

  Per ulteriori informazioni, vedere la pagina sulle [Creare una cassetta postale delle cartelle pubbliche in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Creare nuove cartelle pubbliche

  - Creare una nuova cartella pubblica con il nome *Log delle e-mail* nella radice in modo che il percorso completo della cartella diventi ```\Email Logging\```
  - Creare due sottocartelle in modo che il risultato sia il seguente percorso completo delle cartelle:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Per ulteriori informazioni, vedere [Creare una cartella pubblica](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Abilitare alla posta la cartella pubblica *Coda*

  Per ulteriori informazioni, vedere [Abilitare o disabilitare alla posta una cartella pubblica](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Abilitare alla posta per l'invio di e-mail alla cartella pubblica *Coda* utilizzando Outlook o la shell di gestione di Exchange

  Per ulteriori informazioni, vedere [Consentire agli utenti anonimi di inviare e-mail a una cartella pubblica abilitata alla posta](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Impostare l'utente del log delle e-mail come proprietario di entrambe le cartelle pubbliche, *Coda* e *Archiviazione* utilizzando Outlook o la shell di gestione di Exchange in base alle informazioni nella tabella seguente:

  |Proprietà        |Valore                     |
  |----------------|--------------------------|
  |Utente            |L'e-mail dell'account utente che Business Central utilizzerà per eseguire il processo di log delle e-mail|
  |Livello di autorizzazione|Proprietario                     |

  Per ulteriori informazioni, vedere [Assegnare le autorizzazioni per la cartella pubblica](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Creare due regole di flusso di posta in base alle informazioni nella seguente tabella

  |Scopo  |Name |Condizioni                        |Azione                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Regola per le e-mail in entrata |Registra messaggi e-mail inviati all'organizzazione|*Il mittente* si trova *all'esterno dell'organizzazione* e *il destinatario* si trova *all'interno dell'organizzazione*|BCC dell'account e-mail specificato per la cartella pubblica *Coda*|
  |Regola per le e-mail in uscita | Registra messaggi e-mail inviati dall'organizzazione |*Il mittente* si trova *all'interno dell'organizzazione* e *il destinatario* si trova *all'esterno dell'organizzazione*|BCC dell'account e-mail specificato per la cartella pubblica *Coda*|
  
  Per ulteriori informazioni, vedere [Gestire le regole del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) e [Azioni della regola del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Se si apportano modifiche nella shell di gestione di Exchange, le modifiche diventano visibili nell'interfaccia di amministrazione di Exchange dopo un certo tempo. Inoltre, le modifiche apportate in Exchange saranno disponibili in [!INCLUDE[prod_short](prod_short.md)] dopo un certo tempo. Potrebbe verificarsi un ritardo di diverse ore.
