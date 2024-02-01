---
title: Configurare la posta elettronica in Business Central (video)
description: Descrizione di come connettere gli account di posta elettronica a Business Central in modo da poter inviare messaggi in uscita senza dover aprire un'altra app.
author: brentholtorf
ms.author: bholtorf
ms.topic: get-started
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 10/06/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="set-up-email"></a>Configurare la posta elettronica

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Le persone nelle aziende inviano ogni giorno informazioni e documenti, come ordini vendita e acquisto e fatture, tramite e-mail. Gli amministratori possono collegare uno o più account di posta elettronica a [!INCLUDE[prod_short](includes/prod_short.md)], quindi puoi inviare documenti senza dover aprire un'app di posta elettronica. Puoi comporre ogni messaggio individualmente con strumenti di formattazione di base, come caratteri, stili, colori e così via, e aggiungere allegati fino a 100 MB. Inoltre, i layout di report consentono agli amministratori di includere solo le informazioni chiave dei documenti. Ulteriori informazioni in [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Le funzionalità di posta elettronica in [!INCLUDE[prod_short](includes/prod_short.md)] sono solo per i messaggi in uscita. Non puoi ricevere risposte, ovvero non c'è una pagina di "Posta in arrivo".

> [!NOTE]
> Puoi utilizzare le funzionalità di posta elettronica di [!INCLUDE[prod_short](includes/prod_short.md)] online solo con Exchange Online. Non sono supportati gli scenari ibridi, come la connessione [!INCLUDE[prod_short](includes/prod_short.md)] online a una versione locale di Exchange.
>
> Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] in locale, prima di poter configurare la posta elettronica è necessario creare una registrazione dell'app per [!INCLUDE[prod_short](includes/prod_short.md)] nel portale di Azure. La registrazione dell'app abiliterà [!INCLUDE[prod_short](includes/prod_short.md)] per eseguire l'autorizzazione e l'autenticazione con il provider di posta elettronica. Per ulteriori informazioni, vedi [Configurazione della posta elettronica per Business Central locale](admin-how-setup-email.md#set-up-email-for-business-central-on-premises). In [!INCLUDE[prod_short](includes/prod_short.md)] online, la registrazione viene eseguita automaticamente.

## <a name="requirements"></a>Requisiti

Ci sono un paio di requisiti per l'impostazione e l'utilizzo delle funzionalità di posta elettronica.

* Per configurare la posta elettronica, è necessario disporre del set di autorizzazioni **SETUP EMAIL**. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).
* Tutti coloro che utilizzeranno le funzionalità di posta elettronica devono disporre di una licenza completa [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, gli amministratori delegati e gli utenti guest non possono usare l'account di posta elettronica del tenant.

## <a name="add-email-accounts"></a>Aggiungere account di posta elettronica

Puoi aggiungere account di posta elettronica tramite estensioni che consentono agli account di diversi provider di connettersi a [!INCLUDE[prod_short](includes/prod_short.md)]. Le estensioni standard ti consentono di utilizzare gli account da Microsoft Exchange Online. Tuttavia, potrebbero essere disponibili altre estensioni che ti consentono di collegare account di altri provider, come Gmail.

Puoi specificare scenari aziendali predefiniti in cui utilizzare l'account di posta elettronica per inviare messaggi di posta elettronica. Ad esempio, è possibile specificare che tutti gli utenti inviino documenti di vendita da un account e documenti di acquisto da un altro. Ulteriori informazioni in [Assegnare scenari di posta elettronica ad account di posta elettronica](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

La tabella seguente descrive le estensioni di posta elettronica disponibili per impostazione predefinita.

|Estensione  |Descrizione  |Esempi di quando utilizzare  |
|---------|---------|---------|
|**Connettore Microsoft 365**|Tutti inviano e-mail da una cassetta postale condivisa in Exchange Online.|Quando tutti i messaggi provengono dallo stesso reparto, ad esempio, l'organizzazione di vendita invia messaggi da un account sales@cronus.com. L'opzione richiede la configurazione di una cassetta postale condivisa nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Cassette postali condivise](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Connettore utente corrente**|Tutti inviano e-mail dall'account utilizzato per accedere a [!INCLUDE[prod_short](includes/prod_short.md)].|Consentire comunicazioni da singoli account.|
|**Connettore SMTP**|Usare il protocollo SMTP per inviare messaggi e-mail.|Consentire le comunicazioni tramite il server di posta SMTP. |

> [!NOTE]
> Le estensioni **Connettore Microsoft 365** e **Connettore utente corrente** utilizzano gli account configurati per gli utenti nell'interfaccia di amministrazione di Microsoft 365 per la sottoscrizione di Microsoft 365. Per inviare e-mail utilizzando le estensioni, gli utenti devono disporre di una licenza valida per Exchange Online. Inoltre, negli ambienti sandbox queste estensioni che includono l'estensione **Outlook REST API** richiedono che l'impostazione **Consenti richieste HttpClient** sia abilitata. Per verificare se è abilitata per queste estensioni, vai nella pagina **Gestione estensioni** scegli l'estensione, quindi scegli l'opzione **Configura**.

> Gli utenti esterni, come gli amministratori delegati e i contabili esterni, non possono utilizzare queste estensioni per inviare messaggi di posta elettronica da [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="use-smtp"></a>Usa SMTP

Se desideri utilizzare il protocollo SMTP per inviare e-mail da [!INCLUDE[prod_short](includes/prod_short.md)], puoi utilizzare l'estensione del connettore SMTP. Quando si configura un account che utilizza SMTP, il campo **tipo di mittente** è importante. Se scegli **Utente specifico**, le e-mail verranno inviate utilizzando il nome e altre informazioni dall'account che stai configurando. Tuttavia, se scegli **Utente corrente**, le e-mail verranno inviate dall'account e-mail specificato per l'account di ciascun utente. L'utente corrente è simile alla funzione Invia come. Per altre informazioni vedi [Utilizzare un indirizzo mittente sostitutivo nei messaggi di posta elettronica in uscita](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] locale, non è possibile utilizzare il protocollo di autenticazione OAuth 2.0. Per utilizzare OAuth per SMTP, tutti gli utenti devono trovarsi nello stesso Microsoft Entra Microsoft Entra. 
> 
> Devi creare una registrazione dell'applicazione nel portale di Azure, quindi eseguire la guida al setup assistito **Impostazione Microsoft Entra ID** in [!INCLUDE[prod_short](includes/prod_short.md)] per la connessione a Microsoft Entra ID. Per ulteriori informazioni, vedi [Crea una registrazione dell'app per Business Central nel portale di Azure](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online sta deprecando l'uso dell'autenticazione di base per SMTP. I tenant che attualmente usano SMTP AUTH non saranno interessati da questa modifica. Tuttavia, consigliamo vivamente di utilizzare l'ultima versione di [!INCLUDE [prod_short](includes/prod_short.md)] e di configurare l'autenticazione OAuth 2.0 per SMTP. Non aggiungeremo l'autenticazione basata su certificato per le versioni precedenti di [!INCLUDE [prod_short](includes/prod_short.md)], ad esempio la versione 14. Se non riesci a configurare l'autenticazione OAuth 2.0, ti invitiamo a esplorare alternative di terze parti se desideri utilizzare l'e-mail SMTP nelle versioni precedenti.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="use-the-set-up-email-assisted-setup-guide"></a>Usa la guida per la configurazione assistitia della posta elettronica

La guida al setup assistito **Configurare la posta elettronica** può consentirti di utilizzare rapidamente la posta elettronica.

> [!NOTE]
> Devi disporre di un account di posta elettronica predefinito, anche se aggiungi un solo account. L'account predefinito verrà utilizzato per tutti gli scenari di posta elettronica non assegnati a un account. Ulteriori informazioni in [Assegnare scenari di posta elettronica ad account di posta elettronica](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Imposta account di posta elettronica**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Assegnare scenari di posta elettronica ad account di posta elettronica

Gli scenari di posta elettronica sono processi che implicano l'invio di un documento. Ad esempio, un ordine di vendita o di acquisto o una notifica, come un invito a un contabile esterno. È possibile utilizzare account di posta elettronica specifici per scenari specifici. Ad esempio, è possibile specificare che tutti gli utenti inviino sempre documenti di vendita da un account, documenti di acquisto da un altro e documenti di magazzino o di produzione da un terzo account. Puoi assegnare, riassegnare e rimuovere scenari quando vuoi. Uno scenario può essere assegnato solo a un account e-mail alla volta. L'account e-mail predefinito verrà utilizzato per tutti gli scenari non assegnati a un account.

Sulla pagina **Assegnazione scenario e-mail** puoi scegliere l'azione **Imposta allegati predefiniti** per aggiungere allegati a scenari di posta elettronica. Gli allegati saranno sempre disponibili quando si compone un messaggio e-mail per un documento relativo allo scenario. Ogni scenario di posta elettronica può avere uno o più allegati predefiniti. Gli allegati predefiniti vengono aggiunti automaticamente ai messaggi e-mail per lo scenario e-mail. Ad esempio, quando invii un ordine cliente tramite e-mail, verrà aggiunto l'allegato predefinito specificato per lo scenario Ordine di vendita. Gli allegati predefiniti vengono visualizzati nella sezione **Allegati** in fondo alla pagina **Componi un messaggio e-mail**. Puoi aggiungere manualmente allegati non predefiniti al messaggio e-mail.

<!--
## <a name="to-set-up-email"></a>To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a>Impostare i criteri di visualizzazione

Puoi controllare i messaggi di posta elettronica che un utente può accedere alle pagine Posta in uscita e Posta elettronica inviata.

In **Criteri di visualizzazione dei messaggi e-mail utente**, scegli un utente, quindi scegli una delle seguenti opzioni nel campo **Criteri di visualizzazione e-mail**:

* **Visualizza messaggi e-mail personali** - L'utente può visualizzare solo i propri messaggi di posta elettronica.
* **Visualizza tutti i messaggi e-mail** - L'utente può visualizzare tutti i messaggi e-mail, comprese le e-mail inviate da altri utenti.
* **Visualizza se accedi a tutti i record correlati** - Questo criterio di visualizzazione viene utilizzato se non vengono specificati altri criteri. Un utente può visualizzare i messaggi di posta elettronica inviati da altri utenti se l'utente ha accesso al record inviato e a tutti i record correlati. Ad esempio, l'utente A ha inviato una fattura di vendita registrata a un cliente. L'utente B può vedere il messaggio di posta elettronica se ha accesso sia alla fattura che al cliente.
* **Visualizza se l'accesso ai record correlati** - L'utente può visualizzare i messaggi di posta elettronica inviati da altre persone se ha accesso ad almeno un record correlato al record inviato. Ad esempio, l'utente A ha inviato una fattura di vendita registrata a un cliente. L'utente B può vedere il messaggio di posta elettronica se ha accesso alla fattura o al cliente.

> [!NOTE]
> Se lasci il campo **ID utente** vuoto e quindi scegli l'azione **Criterio di visualizzazione e-mail**, il criterio di visualizzazione si applica a tutti gli utenti.

## <a name="specify-how-many-messages-an-account-can-send-per-minute"></a>Specificare quanti messaggi un account può inviare al minuto

Alcuni provider di posta elettronica (ISP) limitano il numero di messaggi di posta elettronica che un account di posta elettronica può inviare in una sola volta, entro un certo periodo di tempo o entrambi. Conosciuta come *limitazione della posta elettronica*, questa pratica aiuta gli ISP a controllare il traffico sui loro server e prevenire lo spam. Se un account e-mail supera il limite, l'ISP potrebbe bloccare i messaggi. Per assicurarti che il numero di messaggi che invii da [!INCLUDE [prod_short](includes/prod_short.md)] sia conforme al limite del tuo ISP, specifica il limite per ciascuno dei tuoi account di posta elettronica.

Il limite predefinito per i tipi di account Microsoft 365 e Utente corrente è 30, che corrisponde al limite impostato da Exchange Online.

Il limite può essere specificato in due modi:

* Quando utilizzi la guida al setup assistito Configurare la posta elettronica per creare un nuovo account, specifica il limite nel campo **Limite di velocità al minuto**.
* Per gli account e-mail esistenti, specifica il limite nel campo **Limite di velocità e-mail** dell'account.

## <a name="set-up-reusable-email-texts-and-layouts"></a>Impostare testi e-mail riutilizzabili e layout

È possibile utilizzare i report per includere informazioni chiave di documenti vendita, acquisto e assistenza nei testi per le e-mail. I layout di report definiscono lo stile e il contenuto del testo nell'e-mail. Ad esempio il contenuto potrebbe includere testi come un saluto o istruzioni che precedono le informazioni sul documento. Questa procedura descrive come configurare il report **Vendite - Fattura** per fatture vendita registrate, ma il processo è simile per altri report.

> [!NOTE]
> Per utilizzare il layout per creare contenuto per i messaggi di posta elettronica, è necessario utilizzare il tipo di file Word per il layout.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Selezioni report - Vendite**, quindi scegli il collegamento correlato.
2. Nella pagina **Selezione report - Vendite**, nel campo **Utilizzo**, selezionare **Fattura**.
3. In una nuova riga nel campo **ID report** selezionare ad esempio il report standard 1306.
4. Seleziona la casella di controllo **Utilizza per corpo e-mail**.
5. Scegli il campo **Descrizione layout corpo e-mail** e seleziona un layout dall'elenco.
6. Per visualizzare o modificare il layout su cui si basa il testo dell'e-mail, seleziona il layout nella pagina **Layout report personalizzati** e scegli l'azione **Aggiorna layout**. Se personalizzi il layout, utilizza l'azione **Importa layout** per caricare il nuovo layout.
    > [!NOTE]
    > Per personalizzare un layout di report standard, ad esempio 1.306, è necessario creare una copia del report. [!INCLUDE [prod_short](includes/prod_short.md)] ti aiuterà a creare una copia quando importi un layout personalizzato per un report standard. Il nome del nuovo layout del rapporto personalizzato sarà preceduto da "Copia di".
7. Se desideri consentire ai clienti di utilizzare un servizio di pagamento, come PayPal, dovrai configurare il servizio. Successivamente, le informazioni e il collegamento PayPal vengono inseriti nel testo dell'e-mail. Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md).
8. Scegliere il pulsante **OK**.

A questo punto, quando si sceglie ad esempio l'azione **Invia** nella pagina **Fattura vendita registrata**, il corpo e-mail conterrà le informazioni del report 1306 precedute dal testo standard creato in base al layout di report selezionato nel passaggio 5.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Utilizzare un indirizzo mittente sostitutivo nei messaggi di posta elettronica in uscita

Se si utilizzano l'estensione connettore SMTP precedenti puoi utilizzare le funzionalità **Invia come** o **Invio per conto di** dal server Microsoft Exchange per modificare l'indirizzo del mittente nei messaggi in uscita. [!INCLUDE[prod_short](includes/prod_short.md)] utilizzerà l'account SMTP per l'autenticazione su Exchange, ma sostituirà l'indirizzo del mittente con quello specificato o lo modificherà con "per conto di".

Quando configuri un account e vuoi utilizzare le funzionalità Invia come o Invia per conto di Exchange, nel campo **Tipo di mittente** scegli **Utente specifico**.

In alternativa, puoi scegliere **Utente corrente** per consentire alle persone di inviare messaggi tramite il connettore SMTP. Il messaggio sembrerà essere inviato dall'account e-mail specificato nel campo E-mail di contatto sulla scheda utente per l'utente con cui ha effettuato l'accesso. Tuttavia, funzionerà in modo simile alla funzione Invia come e verrà inviato dall'account specificato nella configurazione del connettore SMTP.

Di seguito vengono riportati esempi di utilizzo di Invia come e Invia per conto di in [!INCLUDE[prod_short](includes/prod_short.md)]:

* È possibile che gli ordini di acquisto o di vendita che invii a fornitori e clienti sembrino provenire da un indirizzo _noreply@yourcompanyname.com_.
* Quando il flusso di lavoro invia una richiesta di approvazione tramite e-mail utilizzando l'indirizzo e-mail del richiedente.

> [!Note]
> È possibile utilizzare un solo account per sostituire gli indirizzi del mittente. Cioè, non è possibile avere un indirizzo sostitutivo per i processi di acquisto e un altro per i processi di vendita.

<!--
### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a>Impostare profili di invio documenti

Puoi risparmiare tempo impostando un metodo preferito di invio dei documenti di vendita per ciascuno dei tuoi clienti. Non dovrai selezionare un'opzione di invio, ad esempio se inviare il documento tramite e-mail o come documento elettronico, ogni volta che invii un documento. Per ulteriori informazioni, vedere [Impostare i profili di invio dei documenti](sales-how-setup-document-send-profiles.md).

## <a name="optional-set-up-email-logging-in-exchange-online"></a>Facltativo: Impostare il log delle e-mail in Exchange Online

Ottieni di più dalle comunicazioni tra i venditori e i clienti esistenti o potenziali. Puoi tenere traccia degli scambi di e-mail e trasformarli in opportunità attuabili. Altre informazioni in [Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="optional-monitor-email-usage-and-troubleshoot-email-failures-with-telemetry"></a>Facoltativo: monitora l'utilizzo della posta elettronica e risolvi i problemi relativi alla posta elettronica con la telemetria

Gli amministratori possono attivare la funzione di telemetria in [!INCLUDE[prod_short](includes/prod_short.md)] per ottenere dati sull'utilizzo e sui guasti di diverse funzionalità nel sistema. Per la posta elettronica, registriamo le seguenti operazioni:

- E-mail inviata correttamente  
- Un tentativo di inviare un'e-mail non è riuscito   
- Autenticazione a un server SMTP riuscita/fallita  
- Connessione a un server SMTP riuscita/fallita  

È possibile utilizzare questi dati per monitorare l'utilizzo della posta elettronica e per risolvere i problemi relativi alla posta elettronica. Ulteriori informazioni su [Analisi della telemetria e-mail (contenuto amministrativo)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace).  

## <a name="set-up-email-for-business-central-on-premises"></a>Configurazione della posta elettronica per Business Central locale

[!INCLUDE[prod_short](includes/prod_short.md)] locale può integrarsi con i servizi basati su Microsoft Azure. Ad esempio, puoi usare Cortana Intelligence per previsioni di flusso di cassa più intelligenti, Power BI per visualizzare l'attività e Exchange Online per l'invio di e-mail. L'integrazione con questi servizi si basa su una registrazione dell'app in Microsoft Entra ID. La registrazione dell'app fornisce servizi di autenticazione e autorizzazione per le comunicazioni. Per utilizzare le funzionalità di posta elettronica in [!INCLUDE[prod_short](includes/prod_short.md)] locale, è necessario registrare [!INCLUDE[prod_short](includes/prod_short.md)] come app nel portale di Azure e quindi connettere [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione dell'app. Nelle sezioni successive viene descritto come effettuare tali operazioni.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Creare una registrazione dell'app per Business Central nel portale di Azure

I passaggi per registrare [!INCLUDE[prod_short](includes/prod_short.md)] nel portale di Azure sono descritti in [Registrare un'applicazione in Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Per usare le funzionalità di posta elettronica, la registrazione dell'app deve usare una configurazione multi-tenant.

Le impostazioni specifiche delle funzionalità di posta elettronica sono le autorizzazioni delegate concesse alla registrazione dell'app. La tabella seguente elenca le autorizzazioni minime.

|Nome API/autorizzazione  |Tipo  |Descrizione  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegato|Accedere e leggere il profilo utente.         |
|Microsoft Graph / Mail.ReadWrite |Delegato|Comporre messaggi e-mail.         |
|Microsoft Graph / Mail.Send|Delegato|Inviare messaggi e-mail.         |
|Microsoft Graph / offline_access|Delegato|Mantenere il consenso all'accesso ai dati.|

Se utilizzi un connettore SMTP e desideri utilizzare OAuth 2.0 per l'autenticazione, le autorizzazioni sono leggermente diverse. La tabella seguente elenca le autorizzazioni.

|Nome API/autorizzazione  |Tipo  |Descrizione  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Delegato|Mantenere il consenso all'accesso ai dati.|
|Microsoft Graph / openid|Delegato|Accesso utenti.|
|Microsoft Graph / User.Read |Delegato|Accedere e leggere il profilo utente.         |
|Microsoft Graph / SMTP.Send|Delegato|Invia e-mail dalle caselle di posta utilizzando SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Delegato|Accedi e leggi il profilo utente.         |

Quando si crea una registrazione dell'app, prendere nota delle seguenti informazioni. Saranno necessarie per connettere [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione dell'app.
 
* ID applicazione (client)
* URI di reindirizzamento (facoltativo)
* Segreto client

Per le linee guida generali per la registrazione di un'app, vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
In caso di problemi nell'utilizzo del protocollo SMTP per inviare e-mail dopo la connessione a [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione della tua app, potrebbe essere perché SMTP AUTH non è abilitato per il tuo tenant. Ti consigliamo di utilizzare invece i connettori di posta elettronica Microsoft 365 e Utente corrente, perché utilizzano le API di Microsoft Graph Mail. Tuttavia, se è necessario utilizzare il protocollo SMTP, puoi abilitare SMTP AUTH. Per ulteriori informazioni, vedi [Abilita o disabilita l'invio SMTP al client autenticato (SMTP AUTH) in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect--to-your-app-registration"></a>Connettere l'app [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione dell'app

Dopo aver registrato l'applicazione nel portale di Azure, in [!INCLUDE[prod_short](includes/prod_short.md)], utilizza la pagina **Registrazione Microsoft Entra ID dell'applicazione e-mail** per connettere [!INCLUDE[prod_short](includes/prod_short.md)] alla stessa.

1. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione Microsoft Entra ID dell'applicazione e-mail**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> In alternativa, se ci si connette per la prima volta, è possibile eseguire la guida al setup assistito **Configurare la posta elettronica**. In questo caso, la guida includerà anche la pagina Registrazione Microsoft Entra ID dell'applicazione e-mail per aggiungere le informazioni per la connessione alla registrazione dell'app. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Microsoft Entra ID, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant)** or **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Microsoft Entra ID, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-also"></a>Vedere anche

[Cassette postali condivise in Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Inviare documenti tramite e-mail](ui-how-send-documents-email.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] come Posta in arrivo aziendale in Outlook](admin-outlook.md)  
[Scarica [!INCLUDE[prod_short](includes/prod_short.md)] sul dispositivo mobile](install-mobile-app.md)   
[Scarica [!INCLUDE[prod_short](includes/prod_short.md)] sul dispositivo mobile](install-mobile-app.md)   
[Analisi della telemetria e-mail (contenuto amministrativo)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
