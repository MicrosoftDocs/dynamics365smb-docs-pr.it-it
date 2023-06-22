---
author: edupont04
ms.topic: include
ms.date: 02/15/2022
ms.author: edupont
---

> [!NOTE]
> Le sezioni seguenti presuppongono che si dispone dell'accesso come amministratore per Exchange Online.

Prima di poter configurare la registrazione delle e-mail, è necessario preparare Office 365 con le [cartelle pubbliche](/exchange/collaboration-exo/public-folders/public-folders). È possibile farlo nell'[interfaccia di amministrazione di Exchange](/exchange/exchange-admin-center?preserve-view=true) oppure è possibile usare [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Se si desidera utilizzare [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true), è possibile trovare ispirazione su come impostare lo script in uno script di esempio pubblicato nel [repository BCTech](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Seguire i passaggi seguenti per configurare Exchange Online, con collegamenti a ulteriori risorse per ottenere maggiori informazioni.

### <a name="create-an-admin-role-group" />Creare un gruppo di ruoli amministratore

Creare un gruppo di ruoli amministratore per cartelle pubbliche in base alle informazioni nella seguente tabella:

|Proprietà        |Valore                     |
|----------------|--------------------------|
|Name            |Gestione delle cartelle pubbliche |
|Ruoli selezionati  |Cartelle pubbliche            |
|Utenti selezionati  |L'e-mail dell'account utente che Business Central utilizzerà per eseguire il processo di log delle e-mail|

Per ulteriori informazioni, vedi [Gestire i gruppi di ruoli in Exchange Online](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox" />Creare una nuova cassetta postale della cartella pubblica della cartella pubblica

Creare una nuova cassetta postale della cartella pubblica in base alle informazioni nella seguente tabella:

|Proprietà        |Valore                     |
|----------------|--------------------------|
|Name            |Cassetta postale pubblica            |

Per ulteriori informazioni, vedi [Creare una cassetta postale della cartella pubblica](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### <a name="create-new-public-folders" />Creare nuove cartelle pubbliche

1. Creare una nuova cartella pubblica con il nome **Log delle e-mail** nella radice in modo che il percorso completo della cartella diventi `\Email Logging\`.
2. Creare due sottocartelle in modo che il risultato sia il seguente percorso completo delle cartelle:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Per ulteriori informazioni, vedi [Creare una cartella pubblica](/exchange/collaboration-exo/public-folders/create-public-folder).

### <a name="set-public-folder-ownership" />Impostare la proprietà della cartella pubblica

Impostare l'utente del log delle e-mail come proprietario di entrambe le cartelle pubbliche,*Coda* e *Archiviazione*.

Per ulteriori informazioni, vedere [Assegnare le autorizzazioni per la cartella pubblica](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder" />Abilitare alla posta la cartella pubblica *Coda*

  Per ulteriori informazioni, vedi [Abilitare o disabilitare alla posta una cartella pubblica](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### <a name="mail-enable-sending-emails-to-the-queue-public-folder" />Abilitare alla posta per l'invio di e-mail alla cartella pubblica *Coda*

Abilitare alla posta per l'invio di e-mail alla cartella pubblica *Coda* utilizzando Outlook o la shell di gestione di Exchange.

Per ulteriori informazioni, vedere [Consentire agli utenti anonimi di inviare e-mail a una cartella pubblica abilitata alla posta](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### <a name="create-mail-flow-rules" />Creare regole di flusso di posta

Creare due regole di flusso di posta in base alle informazioni nella seguente tabella:

|Scopo  |Name |Applica questa regola se...             |Esegui le operazioni seguenti...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Regola per le e-mail in entrata |Registra messaggi e-mail inviati all'organizzazione|*Il mittente* si trova *all'esterno dell'organizzazione* e *il destinatario* si trova *all'interno dell'organizzazione*|BCC dell'account e-mail specificato per la cartella pubblica *Coda*|
|Regola per le e-mail in uscita | Registra messaggi e-mail inviati dall'organizzazione |*Il mittente* si trova *all'interno dell'organizzazione* e *il destinatario* si trova *all'esterno dell'organizzazione*|BCC dell'account e-mail specificato per la cartella pubblica *Coda*|

Per ulteriori informazioni, vedere [Gestire le regole del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) e [Azioni della regola del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Se si apportano modifiche nella shell di gestione di Exchange, le modifiche diventano visibili nell'interfaccia di amministrazione di Exchange dopo un certo tempo. Inoltre, le modifiche apportate in Exchange saranno disponibili in [!INCLUDE[prod_short](prod_short.md)] dopo un certo tempo. Potrebbe verificarsi un ritardo di diverse ore.
