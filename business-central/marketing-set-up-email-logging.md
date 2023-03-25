---
title: Imposta log delle e-mail
description: Informazioni su come trasformare le interazioni e-mail tra venditori e clienti in reali opportunità di vendita.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.date: 03/22/2022
ms.search.form: '1680, 1811, 5076'
ms.author: bholtorf
---
# Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti
Ottieni di più dalle comunicazioni tra i venditori e i clienti facendo diventare gli scambi di e-mail in opportunità fruibili. [!INCLUDE[prod_short](includes/prod_short.md)] può utilizzare Exchange Online per tenere un log dei messaggi in entrata e in uscita. È possibile visualizzare e analizzare i contenuti di ciascun messaggio nella pagina **Movimenti log interazione**.

> [!NOTE]
> Nel primo ciclo di rilascio del 2022 abbiamo semplificato i processi per l'impostazione della registrazione della posta elettronica per aumentare la flessibilità e la sicurezza. I nuovi clienti che utilizzano questa versione, trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Registrazione delle e-mail tramite l'API Microsoft Graph** nella pagina **Gestione funzionalità**. Per ulteriori informazioni, vedi [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> Per [!INCLUDE[prod_short](includes/prod_short.md)] online, la nuova esperienza richiede che [!INCLUDE[prod_short](includes/prod_short.md)] ed Exchange Online siano nello stesso tenant.

## Per impostare la registrazione e-mail
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Registrazione delle e-mail tramite l'API Microsoft Graph**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda **Esperienza corrente**.

## [Esperienza corrente](#tab/current-experience)

### Impostare le cartelle pubbliche e le regole per il log delle e-mail in Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Quindi, connettersi a [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online.

## [Nuova esperienza](#tab/new-experience)
### Impostare una casella di posta condivisa e regole condivise per la registrazione della posta elettronica in Exchange Online

> [!NOTE]
> Questi passaggi richiedono l'accesso come amministratore per Exchange Online.

Prepara una cassetta postale condivisa nell'interfaccia di amministrazione di Exchange. In alternativa, puoi anche usare Exchange Online PowerShell. Per ulteriori informazioni, vedi [Creare una casella di posta condivisa](/microsoft-365/admin/email/create-a-shared-mailbox) o [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Seusi Exchange Management PowerShell, le modifiche diventano disponibili nell'interfaccia di amministrazione di Exchange dopo un certo tempo. Potrebbe verificarsi un ritardo di diverse ore.

### Aggiungere un account utente per i membri della cassetta postale condivisa
L'account che utilizzerai per la registrazione e-mail è un account Exchange Online. Il processo programmato utilizza l'account per connettersi alla cassetta postale ed elaborare le e-mail. Questo account non deve essere associato a una persona specifica. Aggiungi l'account e-mail ai membri per la casella di posta condivisa. Per ulteriori informazioni, vedi [Utilizzare l'interfaccia di amministrazione di Exchange per modificare la delega della cassetta postale condivisa](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Consentire ad altri utenti di vedere le e-mail registrate
È possibile consentire a un altro utente di aprire un messaggio di posta elettronica in Exchange correlato a una voce del registro di interazione da [!INCLUDE[prod_short](includes/prod_short.md)]. Per farlo, concedi all'utente l'autorizzazione ``Read`` per la cartella **Archivio** nella casella di posta condivisa. Per maggiori informazioni, vedi [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### Creare regole di flusso di posta
Le regole del flusso di posta cercano condizioni specifiche per i messaggi e agiscono. Crea due regole di flusso di posta in base alle informazioni nella seguente tabella. Per ulteriori informazioni, vedere [Gestire le regole del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) e [Azioni della regola del flusso di posta in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Scopo  |Name  |Applica questa regola se...  |Esegui le operazioni seguenti...  |
|---------|---------|---------|---------|
|Regola per le e-mail in entrata     |Registra messaggi e-mail inviati all'organizzazione|Il mittente si trova all'esterno dell'organizzazione e il destinatario si trova all'interno dell'organizzazione|BCC dell'account e-mail è specificato per la cassetta postale condivisa.|
|Regola per le e-mail in uscita     |Registra messaggi e-mail inviati dall'organizzazione|Il mittente si trova all'interno dell'organizzazione e il destinatario si trova all'esterno dell'organizzazione.|BCC dell'account e-mail è specificato per la cassetta postale condivisa.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] elabora solo i messaggi nella cartella Posta in arrivo nella cassetta postale condivisa. Se una regola sposta i messaggi dalla Posta in arrivo a un'altra cartella, tali messaggi non verranno elaborati. Inoltre, vengono ignorati anche i messaggi nella cartella Posta indesiderata. 

---

## Impostare [!INCLUDE[prod_short](includes/prod_short.md)] per registrare i messaggi e-mail
Questi passaggi sono gli stessi sia per le esperienze attuali che per quelle nuove.

Iniziare la registrazione dei messaggi e-mail con due semplici passaggi:

1. Collegare [!INCLUDE[prod_short](includes/prod_short.md)]con Exchange Online per l'abbonamento a Microsoft 365. Exchange Online gestisce i messaggi di posta elettronica. Questo passaggio è stato semplificato con una guida di installazione assistita. Sono necessarie solo le credenziali di amministratore per l'account amministratore in Microsoft 365. Per iniziare la guida, andare alla pagina **Setup assistito** e quindi selezionare la guida **Configurare la registrazione e-mail**.  

2. Assicurati che gli indirizzi email dei tuoi venditori e contatti in [!INCLUDE[prod_short](includes/prod_short.md)] siano validi. Per fare ciò, per ogni cliente o venditore, aprire la scheda **Contatto** o **Venditore/Acquirente** e osservare il campo **E-mail**.

> [!Tip]
> Dopo aver completato i passaggi nella guida, è possibile verificare se la connessione ha avuto esito positivo. A seconda che tu stia utilizzando l'esperienza attuale o nuova, esegui uno dei seguenti passaggi: 
>
> * **Esperienza corrente**: Cerca **Impostazione marketing** e scegli **Accesso**, **Funzioni**, e quindi **Convalida configurazione registrazione email**.
> * **Nuova esperienza**: Cerca **Log delle e-mail**, scegli **Azioni**, quindi scegli **Convalida setup**.

## Visualizzazione degli scambi di messaggi e-mail nel log delle interazioni

[!INCLUDE[prod_short](includes/prod_short.md)] crea una voce nella pagina **Log delle interazioni** ogni volta che un venditore e un contatto scambiano un messaggio di posta elettronica. Per visualizzare il log delle interazioni, aprire la scheda **Contatto** per la persona, scegliere **Correlato**, quindi **Cronologia** e **Movimenti log interazione**. Ci sono alcune cose che si possono fare con ogni voce del log, ad esempio:

- Visualizzare il contenuto del messaggio di posta elettronica che è stato scambiato selezionando **Processo** e quindi **Mostra allegati**.
- Trasforma uno scambio di e-mail in un'opportunità di vendita. Se una voce sembra promettente, è possibile trasformarla in un'opportunità e gestirne i progressi verso una vendita. Per trasformare uno scambio di e-mail in un'opportunità, scegli la voce, quindi **Processo** e poi **Crea opportunità**. Per ulteriori informazioni, vedere [Gestire opportunità di vendita](marketing-manage-sales-opportunities.md).

## Limiti di cassette postali e cartelle in Exchange Online
Ci sono limiti di cassette postali e cartelle Exchange Online, come i limiti per le dimensioni delle cartelle e il numero di messaggi. Per altre informazioni, vedi [Limiti di Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) e [Limiti per le cartelle pubbliche in Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019).

[!INCLUDE[prod_short](includes/prod_short.md)] archivia i messaggi e-mail registrati in una cartella in Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] archivia anche un collegamento a ciascun messaggio registrato. I collegamenti aprono i messaggi registrati in Exchange Online dalle pagine Movimenti log interazione, Scheda contatto e Scheda venditore in [!INCLUDE[prod_short](includes/prod_short.md)]. Se un messaggio registrato viene spostato in un'altra cartella, il collegamento verrà interrotto. Ad esempio, un messaggio potrebbe essere spostato manualmente o Exchange Online potrebbe avviare automaticamente la suddivisione automatica quando viene raggiunto un limite di archiviazione.

I passaggi seguenti possono aiutarti a evitare di interrompere i collegamenti ai messaggi in Exchange Online.

1. Non spostare i messaggi esistenti in un'altra cartella dopo aver modificato le impostazioni per la configurazione del log delle e-mail. La conservazione dei messaggi esistenti dove si trovano conserverà i collegamenti. I collegamenti ai messaggi nella nuova cartella saranno validi.
2. Evita di raggiungere i limiti di cassette postali e cartelle. Se stai per raggiungere un limite, procedi nel seguente modo:
    1. Configura una nuova casella di posta condivisa (nuova esperienza) o una nuova cartella condivisa (esperienza corrente) in Exchange Online.
    2. Aggiorna le regole del flusso di posta elettronica in Exchange Online.
    3. Aggiorna di conseguenza la configurazione dei log delle e-mail in Business Central

## Connettere le versioni locali a Microsoft Exchange

È possibile connettere [!INCLUDE[prod_short](includes/prod_short.md)] in locale a Exchange in locale o a Exchange Online per il log delle e-mail. Per entrambe le versioni di Exchange, le impostazioni per la connessione sono disponibili nella pagina **Setup marketing**. Per Exchange Online, è anche possibile utilizzare una guida alla al setup assistito.

> [!IMPORTANT]
> La nuova esperienza non supporta una connessione a Exchange locale. Se devi usare Exchange in locale, non abilitare l'aggiornamento della funzionalità per la nuova esperienza.

## Connettersi a Exchange in locale
## [Esperienza corrente](#tab/current-experience)
Per connettere [!INCLUDE[prod_short](includes/prod_short.md)] in locale a Exchange in locale, nella pagina **Setup marketing**, è possibile utilizzare **Di base** come **Tipo di autenticazione** e quindi immettere le credenziali per l'account utente per Exchange in locale. Quindi attivare l'interruttore **Abilitato** per avviare il log delle e-mail.

## [Nuova esperienza](#tab/new-experience)
La nuova esperienza non supporta le connessioni a Exchange locale.

---

## Connettersi a Exchange Online
Per connettersi a Exchange Online è necessario registrare un'applicazione in Azure Active Directory. Fornisci l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento per la registrazione. L'URL di reindirizzamento è preimpostato e dovrebbe funzionare per la maggior parte delle installazioni. Per ulteriori informazioni, vedere [Per registrare un'applicazione in Azure AD per la connessione da Business Central a Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Devi anche usare **OAuth2** come **Tipo di autenticazione**. Devi anche registrare un'applicazione in Azure Active Directory. Fornisci l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento per la registrazione. L'URL di reindirizzamento è precompilato e dovrebbe funzionare per la maggior parte delle installazioni. Per ulteriori informazioni, vedere Per registrare un'applicazione in Azure AD per la connessione da Business Central a Exchange Online di seguito.

È necessario configurare l'installazione per utilizzare HTTPS. Per ulteriori informazioni, vedi [Configurazione di SSL per proteggere la connessione client Web di Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Se stai configurando il server in modo da avere una home page diversa, puoi cambiare l'URL. Il segreto del client verrà salvato come stringa crittografata nel database.

### Per registrare un'applicazione in Azure AD per la connessione da Business Central a Exchange Online
I seguenti passaggi presuppongono che si stia utilizzando Azure Active Directory per gestire identità e accesso. Per ulteriori informazioni, vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). 

## [Esperienza corrente](#tab/current-experience) 
I seguenti passaggi presuppongono che si stia utilizzando Azure Active Directory per gestire identità e accesso. Per ulteriori informazioni, vedi [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). Se non usi Azure Active Directory vedi [Utilizzare un altro servizio di gestione dell'identità e degli accessi](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Nel portale di Azure, in **Gestisci** selezionare **Autenticazione**.
2. In **URL di reindirizzamento**, aggiungere l'URL di reindirizzamento suggerito nella pagina **Setup marketing** in [!INCLUDE[prod_short](includes/prod_short.md)]. Se l'URL di reindirizzamento nella pagina Setup marketing è vuoto, trovare l'URL di reindirizzamento suggerito nella pagina **Setup assistito log delle e-mail**.

    > [!NOTE]
    > Se non si specifica l'URL di reindirizzamento, è possibile farlo in seguito scegliendo **Aggiungi una piattaforma** e quindi **Web** per aggiungere l'applicazione Web e l'URL di reindirizzamento. 

3. In **Gestisci**, scegliere **Manifesto**.
4. Individuare la proprietà **requiredResourceAccess** nel manifest e aggiungere il codice seguente tra parentesi ([]) per aggiungere le autorizzazioni richieste. Per ulteriori informazioni, vedere [Registrare l'applicazione](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Selezionare **Salva**.
6. Sotto **Gestisci**, scegliere **Autorizzazioni API**, quindi verificare che siano elencate le seguenti autorizzazioni:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. In **Gestisci**, scegliere **Certificati e segreti**, quindi creare un nuovo segreto per l'app. Utilizzi il segreto in [!INCLUDE[prod_short](includes/prod_short.md)], nel campo **Segreto client** della pagina **Setup marketing** o lo archivi in un archivio sicuro per utilizzarlo in una sottoscrizione di eventi.
8. Scegli **Panoramica**, quindi trova il valore **ID applicazione (client)**. Il valore **ID applicazione (client)** è l'ID client della tua applicazione. Devi immettere l'ID client nella **pagina Setup connessione** nel campo **ID client** o archiviarlo in un archivio sicuro e fornirlo in una sottoscrizione di eventi.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], configurare il log delle e-mail nella pagina **Setup marketing** o usare la guida **Setup assistito log delle e-mail** per assistenza con il processo.
    * Fornire l'account di posta elettronica dell'utente per conto del quale il processo programmato si connetterà Exchange Online ed elaborerà le e-mail. L'utente deve disporre di una licenza valida per Exchange Online.
    * Fornire l'URL per Exchange Online. In genere, questo URL è il dominio specificato nell'indirizzo di posta elettronica dell'utente.
    * Specificare il **Percorso cartella coda** e il **Percorso cartella archiviazione**.
10. Per avviare il log delle e-mail, attivare l'interruttore **Abilitato**.
11. Accedere con l'account amministratore per Azure Active Directory (questo account deve avere una licenza valida per Exchange ed essere un amministratore in Exchange Online). Dopo aver effettuato l'accesso, devi permettere all'applicazione registrata l'accesso a Exchange Online per conto dell'organizzazione. È necessario fornire il consenso per completare il setup.

   > [!NOTE]
   > Se non viene richiesto di accedere con il proprio account amministratore, è possibile che i popup siano bloccati. Per accedere, consentire i popup da https://login.microsoftonline.com.

## [Nuova esperienza](#tab/new-experience)
1. Nel portale di Azure, in **Gestisci** selezionare **Autenticazione**.
2. In **URL di reindirizzamento**, aggiungere l'URL di reindirizzamento suggerito nella pagina **Log delle e-mail** in [!INCLUDE[prod_short](includes/prod_short.md)]. Se il campo dell'URL di reindirizzamento nella pagina Log delle e-mail è vuoto, trova l'URL di reindirizzamento suggerito nella pagina **Setup assistito**. Per aprire la pagina, nella pagina **Log delle e-mail** scegli **Azioni**, quindi **Setup assistito**.

    > [!NOTE]
    > Se non si specifica l'URL di reindirizzamento, è possibile farlo in seguito scegliendo **Aggiungi una piattaforma** e quindi **Web** per aggiungere l'applicazione Web e l'URL di reindirizzamento.

3. Sotto **Gestisci**, scegli **Autorizzazioni API** e scegli **Microsoft Graph**, quindi scegli **Autorizzazioni delegate**.
4. Usa la casella di ricerca per trovare e selezionare **Posta**, quindi aggiungi l'autorizzazione **Mail.ReadWrite.Shared**. 
5. In **Gestisci**, scegli **Certificati e segreti**, quindi crea un nuovo segreto per l'app. Userai il segreto nel campo **Segreto client** della pagina **Log delle e-mail** in [!INCLUDE[prod_short](includes/prod_short.md)].
6. Scegli **Panoramica**, quindi trova il valore **ID applicazione (client)**. Questo è l'ID client dell'applicazione. Devi inserirlo nel campo **ID client** della pagina **Log delle e-mail**.
7. In [!INCLUDE[prod_short](includes/prod_short.md)], configura il log delle e-mail nella pagina **Log delle e-mail** o usa la guida **Setup assistito** per assistenza.

### Utilizzare un altro servizio di gestione dell'identità e degli accessi
Se non si sta usando Azure Active Directory per gestire le identità e l'accesso, è necessario l'aiuto di uno sviluppatore. Se si preferisce archiviare l'ID app e il segreto in una posizione diversa, è possibile lasciare vuoti i campi ID client e Segreto client e scrivere un'estensione per recuperare l'ID e il segreto dalla posizione. È possibile fornire il segreto in fase di esecuzione sottoscrivendo gli eventi OnGetCDSConnectionClientId e OnGetCDSConnectionClientSecret nella codeunit 1641 "Setup log delle e-mail".

---

## Per avviare il log delle e-mail
1. Per avviare il log delle e-mail, nella pagina **Log delle e-mail** attiva l'interruttore **Abilitato**.
2. Accedi con l'account Exchange Online utilizzato dal processo programmato per connettersi alla cassetta postale ed elaborare le e-mail.

    > [!NOTE]
    > Se non ti viene richiesto di accedere con l'account Exchange Online, è possibile che i popup siano bloccati da browser. Per accedere, consenti i popup da https://login.microsoftonline.com.

## Per interrompere il log delle e-mail
## [Esperienza corrente](#tab/current-experience)
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup marketing**, quindi scegli il collegamento correlato.
1. Disattivare l'interruttore **Abilitato**.

## [Nuova esperienza](#tab/new-experience)
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Log delle e-mail**, quindi scegli il collegamento correlato.
2. Disattiva l'interruttore **Abilitato**.

---

## Per modificare l'account utente utilizzato per il log delle e-mail
Se stai utilizzando la nuova esperienza, puoi modificare l'account utente utilizzato per il log delle e-mail. L'esperienza corrente non supporta questa operazione.

## [Esperienza corrente](#tab/current-experience) 
Disabilita la configurazione corrente, cambia l'utente nella pagina **Log delle e-mail** e quindi riabilita il log delle e-mail. Puoi anche eseguire nuovamente la guida setup assistito.

## [Nuova esperienza](#tab/new-experience)
### [!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Accedi a [!INCLUDE[prod_short](includes/prod_short.md)] con l'account utilizzato dal processo programmato per connettersi alla cassetta postale ed elaborare le e-mail. Questo account deve avere accesso a [!INCLUDE[prod_short](includes/prod_short.md)] ed Exchange Online.
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Log delle e-mail**, quindi scegli il collegamento correlato. 
3. Scegli **Correlato**, quindi **Movimento coda processi**.
4. Riavvia il processo **Log delle e-mail**.

### [!INCLUDE[prod_short](includes/prod_short.md)] locale
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Log delle e-mail**, quindi scegli il collegamento correlato. 
2. Scegli **Azioni**, quindi **Rinnova token**.
3. Accedi con l'account Exchange Online utilizzato dal processo programmato per connettersi alla cassetta postale ed elaborare le e-mail.



## Vedere anche
[Gestione delle relazioni](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]