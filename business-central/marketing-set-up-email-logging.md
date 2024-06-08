---
title: Imposta log delle e-mail
description: Informazioni su come trasformare le interazioni e-mail tra venditori e clienti in reali opportunità di vendita.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 09/18/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
ms.service: dynamics-365-business-central
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Ottieni di più dalle comunicazioni tra i venditori e i clienti facendo diventare gli scambi di e-mail in opportunità fruibili. [!INCLUDE[prod_short](includes/prod_short.md)] può utilizzare Exchange Online per tenere un log dei messaggi in entrata e in uscita. È possibile visualizzare e analizzare i contenuti di ciascun messaggio nella pagina **Movimenti log interazione**.

> [!IMPORTANT]
> Per [!INCLUDE[prod_short](includes/prod_short.md)] online, [!INCLUDE[prod_short](includes/prod_short.md)] e Exchange Online devono appartenere allo stesso tenant.

## <a name="to-set-up-email-logging"></a>Per impostare la registrazione e-mail

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Impostare le cartelle pubbliche e le regole per il log delle e-mail in Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Quindi, connettersi a [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online.

### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Impostare una casella di posta condivisa e regole condivise per la registrazione della posta elettronica in Exchange Online

> [!NOTE]
> Questi passaggi richiedono l'accesso come amministratore per Exchange Online.

Prepara una cassetta postale condivisa nell'interfaccia di amministrazione di Exchange. In alternativa, puoi anche usare Exchange Online PowerShell. Per ulteriori informazioni, vedi [Creare una casella di posta condivisa](/microsoft-365/admin/email/create-a-shared-mailbox) o [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Seusi Exchange Management PowerShell, le modifiche diventano disponibili nell'interfaccia di amministrazione di Exchange dopo un certo tempo. Potrebbe verificarsi un ritardo di diverse ore.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Aggiungere un account utente per i membri della cassetta postale condivisa

L'account che utilizzerai per la registrazione e-mail è un account Exchange Online. Il processo programmato utilizza l'account per connettersi alla cassetta postale ed elaborare le e-mail. Questo account non deve essere associato a una persona specifica. Aggiungi l'account e-mail ai membri per la casella di posta condivisa. Per ulteriori informazioni, vedi [Utilizzare l'interfaccia di amministrazione di Exchange per modificare la delega della cassetta postale condivisa](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a>Consentire ad altri utenti di vedere le e-mail registrate

È possibile consentire a un altro utente di aprire un messaggio di posta elettronica in Exchange correlato a una voce del registro di interazione da [!INCLUDE[prod_short](includes/prod_short.md)]. Per farlo, concedi all'utente l'autorizzazione ``Read`` per la cartella **Archivio** nella casella di posta condivisa. Per maggiori informazioni, vedi [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules"></a>Creare regole di flusso di posta

Le regole del flusso di posta cercano condizioni specifiche per i messaggi e agiscono. Crea due regole di flusso di posta in base alle informazioni nella seguente tabella. Per ulteriori informazioni, vedere [Gestire le regole del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) e [Azioni della regola del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Scopo  |Name  |Applica questa regola se...  |Esegui le operazioni seguenti...  |
|---------|---------|---------|---------|
|Regola per le e-mail in entrata     |Registra messaggi e-mail inviati all'organizzazione|Il mittente si trova all'esterno dell'organizzazione e il destinatario si trova all'interno dell'organizzazione|BCC dell'account e-mail è specificato per la cassetta postale condivisa.|
|Regola per le e-mail in uscita     |Registra messaggi e-mail inviati dall'organizzazione|Il mittente si trova all'interno dell'organizzazione e il destinatario si trova all'esterno dell'organizzazione.|BCC dell'account e-mail è specificato per la cassetta postale condivisa.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] elabora solo i messaggi nella cartella Posta in arrivo nella cassetta postale condivisa. Se una regola sposta i messaggi dalla Posta in arrivo a un'altra cartella, tali messaggi non verranno elaborati. Inoltre, vengono ignorati anche i messaggi nella cartella Posta indesiderata.

## <a name="set-up--to-log-email-messages"></a>Impostare [!INCLUDE[prod_short](includes/prod_short.md)] per registrare i messaggi e-mail

Iniziare la registrazione dei messaggi e-mail con due semplici passaggi:

1. Collegare [!INCLUDE[prod_short](includes/prod_short.md)]con Exchange Online per l'abbonamento a Microsoft 365. Exchange Online gestisce i messaggi di posta elettronica. Questo passaggio è stato semplificato con una guida di installazione assistita. Sono necessarie solo le credenziali di amministratore per l'account amministratore in Microsoft 365. Per iniziare la guida, andare alla pagina **Setup assistito** e quindi selezionare la guida **Configurare la registrazione e-mail**.  

2. Assicurati che gli indirizzi email dei tuoi venditori e contatti in [!INCLUDE[prod_short](includes/prod_short.md)] siano validi. Per fare ciò, per ogni cliente o venditore, aprire la scheda **Contatto** o **Venditore/Acquirente** e osservare il campo **E-mail**.

    > [!Tip]
    > Dopo aver completato i passaggi nella guida, è possibile verificare se la connessione ha avuto esito positivo. Cerca **Log delle e-mail**, scegli **Azioni**, quindi scegli **Convalida setup**.

## <a name="view-email-message-exchanges-in-the-interaction-log"></a>Visualizzazione degli scambi di messaggi e-mail nel log delle interazioni

[!INCLUDE[prod_short](includes/prod_short.md)] crea una voce nella pagina **Log delle interazioni** ogni volta che un venditore e un contatto scambiano un messaggio di posta elettronica. Per visualizzare il log delle interazioni, aprire la scheda **Contatto** per la persona, scegliere **Correlato**, quindi **Cronologia** e **Movimenti log interazione**. Ci sono alcune cose che si possono fare con ogni voce del log, ad esempio:

* Visualizzare il contenuto del messaggio di posta elettronica che è stato scambiato selezionando **Processo** e quindi **Mostra allegati**.
* Trasforma uno scambio di e-mail in un'opportunità di vendita. Se una voce sembra promettente, è possibile trasformarla in un'opportunità e gestirne i progressi verso una vendita. Per trasformare uno scambio di e-mail in un'opportunità, scegli la voce, quindi **Processo** e poi **Crea opportunità**. Per ulteriori informazioni, vedere [Gestire opportunità di vendita](marketing-manage-sales-opportunities.md).

## <a name="mailbox-and-folder-limits-in-exchange-online"></a>Limiti di cassette postali e cartelle in Exchange Online

Ci sono limiti di cassette postali e cartelle Exchange Online, come i limiti per le dimensioni delle cartelle e il numero di messaggi. Per altre informazioni, vedi [Limiti di Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) e [Limiti per le cartelle pubbliche in Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] archivia i messaggi e-mail registrati in una cartella in Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] archivia anche un collegamento a ciascun messaggio registrato. I collegamenti aprono i messaggi registrati in Exchange Online dalle pagine Movimenti log interazione, Scheda contatto e Scheda venditore in [!INCLUDE[prod_short](includes/prod_short.md)]. Se un messaggio registrato viene spostato in un'altra cartella, il collegamento verrà interrotto. Ad esempio, un messaggio potrebbe essere spostato manualmente o Exchange Online potrebbe avviare automaticamente la suddivisione automatica quando viene raggiunto un limite di archiviazione.

I passaggi seguenti possono aiutarti a evitare di interrompere i collegamenti ai messaggi in Exchange Online.

1. Non spostare i messaggi esistenti in un'altra cartella dopo aver modificato le impostazioni per la configurazione del log delle e-mail. La conservazione dei messaggi esistenti dove si trovano conserverà i collegamenti. I collegamenti ai messaggi nella nuova cartella saranno validi.
2. Evita di raggiungere i limiti di cassette postali e cartelle. Se stai per raggiungere un limite, procedi nel seguente modo:
    1. Imposta una nuova casella di posta condivisa in Exchange Online.
    2. Aggiorna le regole del flusso di posta elettronica in Exchange Online.
    3. Aggiorna di conseguenza la configurazione dei log delle e-mail in Business Central

## <a name="connect-on-premises-versions-to-microsoft-exchange"></a>Connettere le versioni locali a Microsoft Exchange

È possibile connettere [!INCLUDE[prod_short](includes/prod_short.md)] in locale a Exchange in locale o a Exchange Online per il log delle e-mail. Per entrambe le versioni di Exchange, le impostazioni per la connessione sono disponibili nella pagina **Setup marketing**. Per Exchange Online, è anche possibile utilizzare una guida alla al setup assistito.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## <a name="connect-to-exchange-on-premises"></a>Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## <a name="connect-to-exchange-online"></a>Connessione a Exchange Online

Per eseguire la connessione a Exchange Online devi registrare un'applicazione in Microsoft Entra ID. Fornisci l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento per la registrazione. L'URL di reindirizzamento è preimpostato e dovrebbe funzionare per la maggior parte delle installazioni. Per ulteriori informazioni, vedi [Per registrare un'applicazione in Microsoft Entra ID per la connessione da Business Central a Exchange Online](#to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-exchange-online). 

Devi anche usare **OAuth2** come **Tipo di autenticazione**. Devi anche registrare un'applicazione in Microsoft Entra ID. Fornisci l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento per la registrazione. L'URL di reindirizzamento è precompilato e dovrebbe funzionare per la maggior parte delle installazioni. Per ulteriori informazioni, vedere Per registrare un'applicazione in Microsoft Entra ID per la connessione da Business Central a Exchange Online di seguito.

È necessario configurare l'installazione per utilizzare HTTPS. Per ulteriori informazioni, vedi [Configurazione di SSL per proteggere la connessione client Web di Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Se stai configurando il server in modo da avere una home page diversa, puoi cambiare l'URL. Il segreto del client verrà salvato come stringa crittografata nel database.

### <a name="to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-exchange-online"></a>Per registrare un'applicazione in Microsoft Entra ID per la connessione da Business Central a Exchange Online

I seguenti passaggi presuppongono che si stia utilizzando Microsoft Entra ID per gestire identità e accesso. Per ulteriori informazioni, vedi [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. Nel portale di Azure, in **Gestisci** selezionare **Autenticazione**.
2. In **URL di reindirizzamento**, aggiungere l'URL di reindirizzamento suggerito nella pagina **Log delle e-mail** in [!INCLUDE[prod_short](includes/prod_short.md)]. Se il campo dell'URL di reindirizzamento nella pagina Log delle e-mail è vuoto, trova l'URL di reindirizzamento suggerito nella pagina **Setup assistito**. Per aprire la pagina, nella pagina **Log delle e-mail** scegli **Azioni**, quindi **Setup assistito**.

    > [!NOTE]
    > Se non si specifica l'URL di reindirizzamento, è possibile farlo in seguito scegliendo **Aggiungi una piattaforma** e quindi **Web** per aggiungere l'applicazione Web e l'URL di reindirizzamento.

3. Sotto **Gestisci**, scegli **Autorizzazioni API** e scegli **Microsoft Graph**, quindi scegli **Autorizzazioni delegate**.
4. Usa la casella di ricerca per trovare e selezionare **Posta**, quindi aggiungi l'autorizzazione **Mail.ReadWrite.Shared**. 
5. In **Gestisci**, scegli **Certificati e segreti**, quindi crea un nuovo segreto per l'app. Userai il segreto nel campo **Segreto client** della pagina **Log delle e-mail** in [!INCLUDE[prod_short](includes/prod_short.md)].
6. Scegli **Panoramica**, quindi trova il valore **ID applicazione (client)**. Questo è l'ID client dell'applicazione. Devi inserirlo nel campo **ID client** della pagina **Log delle e-mail**.
7. In [!INCLUDE[prod_short](includes/prod_short.md)], configura il log delle e-mail nella pagina **Log delle e-mail** o usa la guida **Setup assistito** per assistenza.

### <a name="use-another-identity-and-access-management-service"></a>Utilizzare un altro servizio di gestione dell'identità e degli accessi

Se non si sta usando Microsoft Entra ID per gestire le identità e l'accesso, è necessario l'aiuto di uno sviluppatore. Se si preferisce archiviare l'ID app e il segreto in una posizione diversa, è possibile lasciare vuoti i campi ID client e Segreto client e scrivere un'estensione per recuperare l'ID e il segreto dalla posizione. È possibile fornire il segreto in fase di esecuzione sottoscrivendo gli eventi OnGetCDSConnectionClientId e OnGetCDSConnectionClientSecret nella codeunit 1641 "Setup log delle e-mail".

## <a name="to-start-logging-email"></a>Per avviare il log delle e-mail

1. Per avviare il log delle e-mail, nella pagina **Log delle e-mail** attiva l'interruttore **Abilitato**.
2. Accedi con l'account Exchange Online utilizzato dal processo programmato per connettersi alla cassetta postale ed elaborare le e-mail.

    > [!NOTE]
    > Se non ti viene richiesto di accedere con l'account Exchange Online, è possibile che i popup siano bloccati da browser. Per accedere, consenti i popup da https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a>Per interrompere il log delle e-mail

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Log delle e-mail**, quindi scegli il collegamento correlato.
2. Disattiva l'interruttore **Abilitato**.

## <a name="to-change-the-user-account-used-for-email-logging"></a>Per modificare l'account utente utilizzato per il log delle e-mail

### <a name="-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Accedi a [!INCLUDE[prod_short](includes/prod_short.md)] con l'account utilizzato dal processo programmato per connettersi alla cassetta postale ed elaborare le e-mail. Questo account deve avere accesso a [!INCLUDE[prod_short](includes/prod_short.md)] ed Exchange Online.
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Log delle e-mail**, quindi scegli il collegamento correlato. 
3. Scegli **Correlato**, quindi **Movimento coda processi**.
4. Riavvia il processo **Log delle e-mail**.

### <a name="-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] locale

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Log delle e-mail**, quindi scegli il collegamento correlato.
2. Scegli **Azioni**, quindi **Rinnova token**.
3. Accedi con l'account Exchange Online utilizzato dal processo programmato per connettersi alla cassetta postale ed elaborare le e-mail.

## <a name="see-also"></a>Vedere anche
[Gestione delle relazioni](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
