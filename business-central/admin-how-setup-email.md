---
title: Configurare la posta elettronica in Business Central
description: Descrizione di come connettere gli account di posta elettronica a Business Central in modo da poter inviare messaggi in uscita senza dover aprire un'altra app.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 791033d9b4077ad6e3bf37ab04956113183b5f2b
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440500"
---
# <a name="set-up-email"></a>Configurare la posta elettronica
Le persone nelle aziende inviano ogni giorno informazioni e documenti, come ordini vendita e acquisto e fatture, tramite e-mail. Gli amministratori possono semplificare l'operazione collegando uno o più account di posta elettronica a [!INCLUDE[prod_short](includes/prod_short.md)], quindi puoi inviare documenti senza dover aprire un'app di posta elettronica. Puoi comporre ogni messaggio individualmente con strumenti di formattazione di base, come caratteri, stili, colori e così via, e aggiungere allegati fino a 100 MB. Gli amministratori possono anche impostare layout di report che includono solo le informazioni chiave dei documenti. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Le funzionalità di posta elettronica in [!INCLUDE[prod_short](includes/prod_short.md)] sono solo per i messaggi in uscita. Non puoi ricevere risposte, ovvero non c'è una pagina di posta in arrivo in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Puoi utilizzare le funzionalità di posta elettronica di [!INCLUDE[prod_short](includes/prod_short.md)] online solo con Exchange Online. Non sono supportati gli scenari ibridi, come la connessione [!INCLUDE[prod_short](includes/prod_short.md)] online a una versione locale di Exchange.
> 
> Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] in locale, prima di poter configurare la posta elettronica è necessario creare una registrazione dell'app per [!INCLUDE[prod_short](includes/prod_short.md)] nel portale di Azure. La registrazione dell'app abiliterà [!INCLUDE[prod_short](includes/prod_short.md)] per eseguire l'autorizzazione e l'autenticazione con il provider di posta elettronica. Per ulteriori informazioni, vedere [Impostazione della posta elettronica per Business Central locale](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). In [!INCLUDE[prod_short](includes/prod_short.md)] online, la registrazione viene eseguita automaticamente.

## <a name="required-permissions"></a>Autorizzazioni richieste
Per configurare la posta elettronica, è necessario disporre del set di autorizzazioni **SETUP EMAIL**. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Aggiunta di account di posta elettronica
Puoi aggiungere account di posta elettronica tramite estensioni che consentono agli account di diversi provider di connettersi a [!INCLUDE[prod_short](includes/prod_short.md)]. Le estensioni standard ti consentono di utilizzare account da Microsoft Exchange Online, ma potrebbero essere disponibili altre estensioni che consentono di collegare account di altri provider, come Gmail.

Dopo aver aggiunto un account di posta elettronica, è possibile specificare scenari aziendali predefiniti in cui utilizzare l'account per inviare messaggi di posta elettronica. Ad esempio, è possibile specificare che tutti gli utenti inviino documenti di vendita da un account e documenti di acquisto da un altro. Per ulteriori informazioni, vedere [Assegnare scenari di posta elettronica agli account di posta elettronica](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

La tabella seguente descrive le estensioni di posta elettronica disponibili per impostazione predefinita.

|Estensione  |Descrizione  |Esempi di quando utilizzare  |
|---------|---------|---------|
|**Microsoft 365**|Tutti inviano e-mail da una cassetta postale condivisa in Exchange Online.|Quando tutti i messaggi provengono dallo stesso reparto, ad esempio, l'organizzazione di vendita invia messaggi da un account sales@cronus.com. Ciò richiede la configurazione di una cassetta postale condivisa nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Cassette postali condivise](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Utente corrente**|Tutti inviano e-mail dall'account utilizzato per accedere a [!INCLUDE[prod_short](includes/prod_short.md)].|Consentire comunicazioni da singoli account.|
|**Altro (SMTP)**|Usare il protocollo SMTP per inviare messaggi e-mail.|Consentire le comunicazioni tramite il server di posta SMTP. |

> [!NOTE]
> Le estensioni **Microsoft 365** e **Utente corrente** utilizzano gli account configurati per gli utenti nell'interfaccia di amministrazione di Microsoft 365 per l'abbonamento a Microsoft 365. Per inviare e-mail utilizzando le estensioni, gli utenti devono disporre di una licenza valida per Exchange Online. 
>
> Inoltre, gli utenti esterni, come gli amministratori delegati e i contabili esterni, non possono utilizzare queste estensioni per inviare messaggi di posta elettronica da [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Impostazioni SMTP precedenti ed estensione Email - Connettore SMTP
Se stai già utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] e hai configurato la posta elettronica tramite la configurazione SMTP precedente, puoi continuare a utilizzare la configurazione in parallelo con l'estensione Email - Connettore SMTP. Quando aggiorniamo [!INCLUDE[prod_short](includes/prod_short.md)] alla versione di rilascio successiva, copiamo le impostazioni SMTP precedenti nell'estensione Email - Connettore SMTP. Quando è pronto, l'amministratore può attivare le funzionalità di posta elettronica avanzata e inizierai a utilizzare l'estensione Email - Connettore SMTP. Per ulteriori informazioni, vedere [Informazioni su Gestione funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management#about-feature-management). Tuttavia, non esiste alcuna sincronizzazione tra l'estensione del connettore SMTP e le impostazioni precedenti. Se modifichi le impostazioni SMTP nell'estensione, devi apportare le stesse modifiche nella configurazione SMTP precedente o viceversa.

> [!NOTE]
> Se disponi di personalizzazioni che si basano sulla configurazione di posta elettronica SMTP precedente, è possibile che si abbiano dei problemi con le personalizzazioni se inizi a utilizzare le estensioni di posta elettronica. Si consiglia di configurare e testare le estensioni prima di attivare l'opzione per le funzionalità di posta elettronica avanzate.

> [!IMPORTANT]
> Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] in locale, puoi utilizzare OAuth 2.0 per l'autenticazione, ma è necessario creare una registrazione dell'applicazione nel portale di Azure e quindi eseguire una guida al setup assistito **Imposta Azure Active Directory** in formato [!INCLUDE[prod_short](includes/prod_short.md)] per connettersi ad Azure AD. Per ulteriori informazioni, vedi [Crea una registrazione dell'app per Business Central nel portale di Azure](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>Aggiungere account di posta elettronica
La guida al setup assistito **Configurare la posta elettronica** può consentirti di utilizzare rapidamente la posta elettronica.

> [!NOTE]
> Devi disporre di un account di posta elettronica predefinito, anche se aggiungi un solo account. L'account predefinito verrà utilizzato per tutti gli scenari di posta elettronica non assegnati a un account. Per ulteriori informazioni, vedere [Assegnare scenari di posta elettronica agli account di posta elettronica](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Imposta account di posta elettronica**, quindi scegli il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Assegnare scenari di posta elettronica ad account di posta elettronica
Gli scenari di posta elettronica sono processi che comportano l'invio di un documento, ad esempio un ordine vendita o acquisto, o una notifica, ad esempio un invito a un contabile esterno. È possibile utilizzare account di posta elettronica specifici per scenari specifici. Ad esempio, è possibile specificare che tutti gli utenti inviino sempre documenti di vendita da un account, documenti di acquisto da un altro e documenti di magazzino o di produzione da un terzo account. Puoi assegnare, riassegnare e rimuovere scenari quando vuoi, ma puoi assegnare uno scenario a un solo account di posta elettronica alla volta. L'account di posta elettronica predefinito verrà utilizzato per tutti gli scenari di posta elettronica non assegnati a un account.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto
È possibile utilizzare i report per includere informazioni chiave di documenti vendita e acquisto nei testi per le e-mail. Questa procedura descrive come configurare il report **Vendite - Fattura** per fatture vendita registrate, ma il processo è simile per altri report.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Selezioni report Vendite**, quindi scegli il collegamento correlato.
2. Nella pagina **Selezione report - Vendite**, nel campo **Utilizzo**, selezionare **Fattura**.
3. In una nuova riga nel campo **ID report** selezionare ad esempio il report standard 1306.
4. Selezionare la casella di controllo **Utilizza per corpo e-mail**.
5. Scegli il campo **Descrizione layout corpo e-mail** e seleziona un layout dall'elenco.

    I layout di report definiscono lo stile e il contenuto del testo dell'e-mail, incluso testo come saluti o istruzioni che precedono le informazioni del documento. Se la tua organizzazione dispone di diversi layout, puoi visualizzare tutti i layout dei report disponibili se scegli **Seleziona da elenco completo**.
6. Per visualizzare o modificare il layout su cui si basa il testo dell'e-mail, seleziona il layout nella pagina **Layout report personalizzati** e scegli l'azione **Aggiorna layout**.
7. Se si desidera offrire ai clienti la possibilità di pagare elettronicamente gli articoli acquistati, è possibile configurare il servizio di pagamento correlato, come PayPal, e quindi inserire informazioni su PayPal e il collegamento ipertestuale nel testo dell'e-mail. Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md).
8. Scegliere il pulsante **OK**.

A questo punto, quando si sceglie ad esempio l'azione **Invia** nella pagina **Fattura vendita registrata**, il corpo e-mail conterrà le informazioni del report 1306 precedute dal testo standard creato in base al layout di report selezionato nel passaggio 5.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Utilizzo di un indirizzo mittente sostitutivo nei messaggi di posta elettronica in uscita
Se si utilizzano le impostazioni SMTP precedenti puoi utilizzare le funzionalità **Invia come** o **Invio per conto di** dal server Microsoft Exchange per modificare l'indirizzo del mittente nei messaggi in uscita. [!INCLUDE[prod_short](includes/prod_short.md)] utilizzerà l'account SMTP per l'autenticazione su Exchange, ma sostituirà l'indirizzo del mittente con quello specificato o lo modificherà con "per conto di".

Di seguito vengono riportati esempi di utilizzo di Invia come e Invia per conto di in [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Quando si inviano documenti come ordini di acquisto o di vendita a fornitori e clienti, è possibile che debbano essere visualizzati da un indirizzo _noreply@yourcompanyname.com_.
 * Quando il flusso di lavoro invia una richiesta di approvazione tramite e-mail utilizzando l'indirizzo e-mail del richiedente.

> [!Note]
> È possibile utilizzare un solo account per sostituire gli indirizzi del mittente. Cioè, non è possibile avere un indirizzo sostitutivo per i processi di acquisto e un altro per i processi di vendita.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Per impostare l'indirizzo mittente sostitutivo per i messaggi di posta elettronica in uscita
1. Nell'**Interfaccia di amministrazione di Exchange** per l'account Microsoft 365, trovare la casella di posta da utilizzare come indirizzo sostitutivo, quindi copiare o annotare l'indirizzo. Se è necessario un nuovo indirizzo, andare all'interfaccia di amministrazione di Microsoft 365 per creare un nuovo utente e configurare la relativa casella di posta.
2. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup e-mail SMTP**, quindi scegli il collegamento correlato.
3. Nel campo **Invia come**, immettere l'indirizzo sostitutivo.
4. Copiare o prendere nota dell'indirizzo nel campo **ID utente**.
5. Nell'**Interfaccia di amministrazione di Exchange**, trovare la casella di posta da utilizzare come indirizzo sostitutivo, quindi immettere l'indirizzo nel campo **ID utente** nel campo **Invia come**. Per ulteriori informazioni, vedi [Utilizzare EAC per assegnare autorizzazioni alle singole cassette postali](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Per utilizzare l'indirizzo sostitutivo nei workflow di approvazione
1. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup e-mail SMTP**, quindi scegli il collegamento correlato.
2. Copiare o prendere nota dell'indirizzo nel campo **ID utente**.
3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup utente approvazione**, quindi scegli il collegamento correlato.
4. Nell'**Interfaccia di amministrazione di Exchange**, trovare le caselle di posta per ogni utente elencato nella pagina **Setup utente approvazione** e nel campo **Invia come** immettere l'indirizzo dal campo **ID utente** della pagina **Setup e-mail SMTP** pagina in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Gestire autorizzazioni per destinatari](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup e-mail SMTP**, quindi scegli il collegamento correlato.
6. Per abilitare la sostituzione, attivare l'interruttore **Consenti sostituzione mittente**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] determinerà quale indirizzo visualizzare nel seguente ordine: <br><br> 1. L'indirizzo specificato nel campo **Posta elettronica** della pagina **Setup utente approvazione** per i messaggi in un workflow. <br> 2. L'indirizzo specificato nel campo **Invia come** della pagina **Setup e-mail SMTP**. <br> 3. L'indirizzo specificato nel campo **ID utente** della pagina **Setup e-mail SMTP**.

## <a name="set-up-document-sending-profiles"></a>Impostare profili di invio documenti
È possibile impostare un metodo di invio di documenti vendita preferito per ogni cliente, in modo da non dover selezionare un'opzione di invio, come se inviare il documento tramite posta elettronica o come documento elettronico ogni volta che si invia un documento. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Impostare le cartelle pubbliche e le regole per il log delle e-mail in Exchange Online
Ottenere di più dalle comunicazioni tra i venditori e i tuoi clienti esistenti o potenziali monitorando gli scambi di e-mail e trasformandoli in opportunità fruibili. Per ulteriori informazioni, vedere [Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Quindi, connettersi a [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online. Per ulteriori informazioni, vedere [Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Configurazione della posta elettronica per Business Central locale 
[!INCLUDE[prod_short](includes/prod_short.md)] locale può integrarsi con i servizi basati su Microsoft Azure. Ad esempio, puoi usare Cortana Intelligence per previsioni di flusso di cassa più intelligenti, Power BI per visualizzare l'attività e Exchange Online per l'invio di e-mail. L'integrazione con questi servizi si basa su una registrazione dell'app in Azure Active Directory. La registrazione dell'app fornisce servizi di autenticazione e autorizzazione per le comunicazioni. Per utilizzare le funzionalità di posta elettronica in [!INCLUDE[prod_short](includes/prod_short.md)] locale, è necessario registrare [!INCLUDE[prod_short](includes/prod_short.md)] come app nel portale di Azure e quindi connettere [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione dell'app. Nelle sezioni successive viene descritto come effettuare tali operazioni.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Crea una registrazione dell'app per Business Central nel portale di Azure
I passaggi per registrare [!INCLUDE[prod_short](includes/prod_short.md)] nel portale di Azure sono descritti in [Registrare un'applicazione in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Le impostazioni specifiche delle funzionalità di posta elettronica sono le autorizzazioni delegate concesse alla registrazione dell'app. La tabella seguente elenca le autorizzazioni minime.

|Nome API/autorizzazione  |Tipo  |Descrizione  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegato|Accedere e leggere il profilo utente.         |
|Microsoft Graph / Mail.ReadWrite |Delegato|Comporre messaggi e-mail.         |
|Microsoft Graph / Mail.Send|Delegato|Inviare messaggi e-mail.         |
|Microsoft Graph / offline_access|Delegato|Mantenere il consenso all'accesso ai dati.|

Se utilizzi una configurazione SMTP precedente o il connettore SMTP e desideri utilizzare OAuth per l'autenticazione, le autorizzazioni sono leggermente diverse. La tabella seguente elenca le autorizzazioni.

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
In caso di problemi nell'utilizzo della configurazione SMTP precedente per inviare e-mail dopo la connessione a [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione della tua app, potrebbe essere perché SMTP AUTH non è abilitato per il tuo tenant. Ti consigliamo di utilizzare invece i connettori di posta elettronica Microsoft 365 e Utente corrente, perché utilizzano le API di Microsoft Graph Mail. Tuttavia, se è necessario utilizzare la configurazione SMTP, è possibile abilitare SMTP AUTH. Per ulteriori informazioni, vedi [Abilita o disabilita l'invio SMTP al client autenticato (SMTP AUTH) in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>Connettere l'app [!INCLUDE[prod_short](includes/prod_short.md)] alla registrazione dell'app
Dopo aver registrato l'applicazione nel portale di Azure, in [!INCLUDE[prod_short](includes/prod_short.md)], utilizzare la guida al setup assistito **Registrazione AAD dell'applicazione e-mail** per connettere [!INCLUDE[prod_short](includes/prod_short.md)] alla stessa.

1. In [!INCLUDE[prod_short](includes/prod_short.md)], scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione AAD dell'applicazione e-mail**, quindi scegli il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> In alternativa, se ci si connette per la prima volta, è possibile eseguire la guida al setup assistito **Configurare la posta elettronica**. La guida richiederà le informazioni per la connessione alla registrazione dell'app. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Vedere anche

[Cassette postali condivise in Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)] come Posta in arrivo aziendale in Outlook](admin-outlook.md)  
[Scarica [!INCLUDE[prod_short](includes/prod_short.md)] sul mio dispositivo mobile](install-mobile-app.md)
[Scarica [!INCLUDE[prod_short](includes/prod_short.md)] sul mio dispositivo mobile](install-mobile-app.md)
[Analisi della telemetria e-mail (contenuto amministrativo)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
