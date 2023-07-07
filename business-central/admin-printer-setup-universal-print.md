---
title: Impostare le stampanti di Stampa universale
description: Scopri come utilizzare Stampa universale per fornire la stampa cloud in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# <a name="set-up-universal-print-printers"></a>Impostare le stampanti di Stampa universale

Stampa universale è un servizio basato su abbonamento a Microsoft 365 che funziona interamente su Microsoft Azure. Offre una gestione centralizzata della stampante tramite il portale Stampa universale. [!INCLUDE[prod_short](includes/prod_short.md)] rende disponibili agli utenti client le stampanti configurate in Stampa universale tramite l'estensione **Integrazione di stampa universale**.

![Configurazione della stampa universale.](media/Universal-Print-arch.png)

La configurazione completa richiede che tu lavori in Microsoft Azure, usando il [portale di Azure](https://portal.azure.com) e in [!INCLUDE[prod_short](includes/prod_short.md)]. La configurazione è suddivisa in due attività principali, come descritto in questo articolo:

1. In Microsoft Azure, configura Stampa universale e aggiungi le stampanti che vuoi utilizzare in Business Central a una condivisione di stampa. Vai in [questa sezione](#set-up-universal-print-and-printers-in-microsoft-azure).
2. In [!INCLUDE[prod_short](includes/prod_short.md)], aggiungi le stampanti dalle condivisioni di stampa in Stampa universale. Vai in [questa sezione](#add-printers-in-business-central-online) per online o [qui](#add-printers-in-business-central-on-premises) per locale.

## <a name="prerequisites"></a>Prerequisiti

- Stampanti supportate

  [!INCLUDE[prod_short](includes/prod_short.md)] supporta le stesse stampanti di Stampa universale, che possono essere stampanti compatibili con Stampa universale o non compatibili. Le stampanti non compatibili non possono comunicare direttamente con Stampa universale, quindi richiedono un software per un connettore aggiuntivo, fornito da Stampa universale. Alcune stampanti meno recenti potrebbero non essere supportate. 

- Stampa universale:

  - Un abbonamento o una licenza Stampa universale per la tua organizzazione.

    Per ulteriori informazioni, vedi [Licenza di Stampa universale](/universal-print/fundamentals/universal-print-license).

  - Possiedi i ruoli **Amministratore stampante** (o responsabile stampante) e **Amministratore globale** in Azure.

    Per gestire Stampa universale, il tuo account deve disporre dei ruoli **Amministratore stampante** (o responsabile stampante) e **Amministratore globale** in Azure AD. Questi ruoli sono necessari solo per la gestione di Stampa universale. Non sono richiesti dagli utenti che configurano le stampanti da [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] online e locale:

  - [!INCLUDE[prod_short](includes/prod_short.md)] 2021 primo ciclo di rilascio o successivi.
  - L'estensione **Integrazione di stampa universale** è installata.

    Questa estensione è pubblicata e installata per impostazione predefinita come parte di [!INCLUDE[prod_short](includes/prod_short.md)] online e in locale. Puoi verificare se è installata nella pagina **Gestione delle estensioni**. Per ulteriori informazioni, vedi [Installare e disinstallare le estensioni in Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] solo locale:
  - L'autenticazione Azure Active Directory o NavUserPassword è configurata.
    > [!NOTE]
    >  L'estensione Stampa universale non supporta l'autenticazione da servizio a servizio (S2S). Richiede a un utente che ha effettuato l'accesso di inviare processi di stampa al servizio di stampa universale tramite l'API Graph.
  - Un'applicazione per Business Central è registrata nel tuo tenant Azure AD e [!INCLUDE[prod_short](includes/prod_short.md)].

    Come altri servizi di Azure che funzionano con [!INCLUDE[prod_short](includes/prod_short.md)], Stampa universale richiede la registrazione di un'app per [!INCLUDE[prod_short](includes/prod_short.md)] in Azure AD. La registrazione dell'app fornisce servizi di autenticazione e autorizzazione tra [!INCLUDE[prod_short](includes/prod_short.md)] e Stampa universale.

    La tua distribuzione potrebbe già usare una registrazione dell'app per altri servizi di Azure, come Power BI. In tal caso, utilizza anche la registrazione dell'app esistente per Stampa universale, invece di aggiungerne una nuova. L'unica cosa che dovrai fare, in questo caso, è modificare la registrazione dell'app per includere le autorizzazioni di stampa pertinenti per l'API Microsoft Graph: **PrinterShare.ReadBasic.All**, **PrintJob.Create**, e **PrintJob.ReadBasic.** 

    Per registrare un'app e impostare le autorizzazioni appropriate, segui i passaggi descritti in [Registra un'applicazione in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## <a name="set-up-universal-print-and-printers-in-microsoft-azure"></a>Configurazione di Stampa universale e delle stampanti in Microsoft Azure

Prima di poter iniziare a gestire le stampanti Stampa universale in Business Central, sono necessarie diverse attività per attivare Stampa universale in Azure con le stampanti che desideri utilizzare.

Per istruzioni dettagliate su come eseguire la configurazione, vedi [Inizia: configurazione di Stampa universale](/universal-print/fundamentals/universal-print-getting-started) nella documentazione di Stampa universale. Ecco una panoramica dei passaggi che dovrai completare. La maggior parte di questi passaggi viene eseguita nel portale di Azure.

1. Assegna le licenze Stampa universale a te stesso e ad altri utenti.

    La modalità di assegnazione della licenza dipende dall'integrazione con Business Central Online o in locale.

    - Con [!INCLUDE[prod_short](includes/prod_short.md)] Online, assegni le licenze utilizzando l'interfaccia di amministrazione di Microsoft 365.

      Per ulteriori informazioni, vedi [Guida in linea di Microsoft Admin Center: assegna licenze agli utenti](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Con [!INCLUDE[prod_short](includes/prod_short.md)] in locale, assegni le licenze nel tenant di Azure tramite il portale di Azure.

      Per ulteriori informazioni, vedi [Directory di Azure: assegna o rimuovi licenze nel portale Azure Active Directory](/azure/active-directory/fundamentals/license-users-groups).

2. Installa il connettore Stampa universale per registrare le stampanti che non possono comunicare direttamente con Stampa universale.

    La maggior parte delle stampanti sul mercato non può comunicare direttamente con Stampa universale, quindi dovrai installare il connettore Stampa universale. Per ulteriori informazioni, vedi [Installazione del connettore Stampa universale](/universal-print/fundamentals/universal-print-connector-installation).

3. Registra le tue stampanti in Stampa universale.

    La registrazione di una stampante fa sì che Stampa universale sia a conoscenza della stampante.

    - Per le stampanti in grado di comunicare direttamente con Stampa universale, segui i passaggi forniti dal produttore della stampante.

    - Per altre stampanti, registra le stampanti utilizzando il connettore Stampa universale. 

      Per ulteriori informazioni, vedi [Registrazione della stampante](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Modifica delle proprietà della stampante (opzionale)

    Dopo aver registrato una stampante, puoi visualizzarne e modificarne le proprietà, ad esempio le preferenze predefinite.

    Per ulteriori informazioni, vedi [Gestione delle impostazioni della stampante tramite il portale Stampa universale](/universal-print/portal/configure-printer-settings).

5. Condividi le stampanti con gli utenti.

    Qualsiasi stampante che desideri utilizzare in [!INCLUDE[prod_short](includes/prod_short.md)] deve essere aggiunta a una *condivisione stampante* in Stampa universale. Qualsiasi utente che necessita dell'accesso alla stampante deve essere aggiunto come membro della condivisione stampante. Per ulteriori informazioni, vedi [Condividere una stampante](/universal-print/portal/share-printers).

    > [!TIP]
    > Puoi sempre aggiungere o rimuovere gli utenti in un secondo momento. Per ulteriori informazioni, vedi [Autorizzazioni della stampante](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Abilita la conversione dei documenti.

    Stampa universale esegue il rendering del contenuto per la stampa in formato XPS. Alcune stampanti legacy non supportano il rendering dei contenuti XPS&mdash;in molti casi, solo in formato PDF. La stampa su queste stampanti non riuscirà a meno che legacy non sia impostata per convertire i documenti nel formato supportato dalla stampante.

    Per ulteriori informazioni, vedi [Panoramica sulla conversione dei documenti](/universal-print/portal/document-conversion).

Ora sei pronto per aggiungere le stampanti a [!INCLUDE[prod_short](includes/prod_short.md)], configurare le stampanti predefinite per i report e stampare.  

## <a name="add-printers-in-business-central-online"></a>Aggiungere le stampanti in Business Central online

Dopo che le stampanti sono state configurate e condivise in Stampa universale, puoi aggiungerle per utilizzarle in [!INCLUDE[prod_short](includes/prod_short.md)]. Esistono due modi per aggiungere stampanti Stampa universale. Puoi aggiungere le stampanti tutte in una volta o singolarmente, una alla volta.

L'aggiunta di stampanti singole consente di configurare la stessa stampante Stampa universale in [!INCLUDE[prod_short](includes/prod_short.md)] più di una volta. Quindi, per ogni stampante aggiunta, puoi modificare le impostazioni di stampa, come il vassoio della carta, le dimensioni e l'orientamento. In questo modo, puoi impostare stampanti per diversi report e documenti con requisiti di output speciali.

> [!NOTE]
> Stai utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] locale? In tal caso, vai alla [sezione successiva](#add-printers-in-business-central-on-premises), la configurazione iniziale è leggermente diversa.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione stampante**, quindi scegli il collegamento correlato.
2. Seleziona **Stampa universale**, quindi una delle seguenti opzioni:

   - **Aggiungi tutte le stampanti di Stampa universale** per aggiungere tutte le stampanti che non sono già state aggiunte. Puoi utilizzare questa opzione anche se sono già state aggiunte stampanti.
   - **Aggiungi una stampante di Stampa universale** per aggiungere una stampante specifica.  
3. Segui le istruzioni sullo schermo.

    - Se hai scelto **Aggiungi tutte le stampanti di Stampa universale** viene avviata la configurazione **Aggiungi stampanti di Stampa universale**. 

    - Se hai scelto **Aggiungi una stampante di Stampa universale** viene visualizzata la pagina **Impostazioni di Stampa universale**. Compila il campo **Nome** e seleziona **...** accanto al campo **Condivisione di stampa in Stampa universale** per selezionare la condivisione stampante contenente la stampante di Stampa universale. Compila i rimanenti campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Dopo che una stampante è stata aggiunta, puoi visualizzarne e modificarne le impostazioni dalla pagina **Gestione stampante**. Seleziona la stampante, quindi scegli **Modifica impostazioni stampante**.

## <a name="add-printers-in-business-central-on-premises"></a>Aggiungere le stampanti in Business Central locale

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Prima che un utente possa aggiungere o utilizzare le stampanti di Stampa universale in Business Central, deve autorizzare l'accesso ai servizi di Azure utilizzati da Stampa universale e concedere l'autorizzazione a dati e operazioni quali:

- Accesso e lettura del profilo utente
- Lettura delle informazioni di base sul processo di stampa
- Creazione dei processi di stampa

Questa operazione viene in genere eseguita la prima volta che si connettono all'app registrata di Azure usata per Stampa universale. In Business Central online, questo flusso di autorizzazione viene eseguito in modo fluido, senza alcuna interazione da parte dell'utente. Ma in Business Central locale funziona in modo diverso. Richiede che tu, o qualsiasi altro utente che desideri utilizzare le stampanti di Stampa universale, avvii il flusso di autenticazione, di solito una sola volta. Il modo più diretto è descritto nei seguenti passaggi. Un modo meno diretto consiste nel connettersi a un altro servizio integrato che usa la stessa app registrata in Azure, come Power BI o OneDrive. Ogni utente in genere deve eseguire questa attività solo una volta.

> [!NOTE]
> Se sei un amministratore, ti consigliamo di completare questa attività prima degli altri utenti. Successivamente, informa gli utenti che dovranno utilizzare le stampanti di Stampante universale e come farlo. Se l'app registrata in Azure per Stampa universale richiede il consenso dell'amministratore per le autorizzazioni API, è più semplice concedere il consenso per conto dell'organizzazione. Puoi concedere il consenso dell'amministratore dal portale di Azure o quando esegui i passaggi seguenti. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### <a name="connect-to-universal-print-for-the-first-time"></a>Connessione a Stampa universale per la prima volta

Completa questi passaggi per connettersi al servizio Stampa universale per la prima volta.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione stampante**, quindi scegli il collegamento correlato.
2. Seleziona **Stampa universale** > **Aggiungi tutte le stampanti di Stampa universale** per avviare la guida al setup assistito (procedura guidata) **Aggiungi stampanti di Stampa universale**.
3. Segui le istruzioni sullo schermo fino ad arrivare alla pagina AUTORIZZAZIONI DEL SERVIZIO AZURE ACTIVE DIRECTORY.

    <!--The AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Azure AD setup, checking your Universal Print license, and then adding the printers.-->

   ![Mostra la pagina AUTORIZZAZIONI DEL SERVIZIO AZURE ACTIVE DIRECTORY](media/azure-ad-services-permissions.png "Mostra la pagina AUTORIZZAZIONI DEL SERVIZIO AZURE ACTIVE DIRECTORY")

4. Seleziona il collegamento **Autorizza servizi di Azure**.

   1. Se viene visualizzata la pagina **Autorizzazione richiesta**, leggila attentamente e seleziona **Accetta** per accettare e continuare. Se sei un amministratore, puoi selezionare **Consenso per conto dell'organizzazione** se desideri dare il consenso per tutti gli utenti.

      ![Mostra la pagina delle autorizzazioni richieste di Azure](media/azure-ad-permissions-requested.png "Pagina delle autorizzazioni richieste di Azure").

   2. Se ti viene richiesto, accedi con il tuo nome e la tua password.

5. Quando l'autorizzazione viene completata, si torna alla pagina **Aggiungi stampanti di Stampa universale**. Seleziona **Avanti** > **Fine** per completare l'impostazione.

Dopo che una stampante è stata aggiunta, puoi visualizzarne e modificarne le impostazioni dalla pagina **Gestione stampante**. Seleziona la stampante, quindi scegli **Modifica impostazioni stampante**.

Dopo aver completato l'accesso iniziale, puoi utilizzare le stampanti di Stampa universale per stampare report e altri processi di stampa. Per ulteriori informazioni, vai a [Stampa di un report](ui-work-report.md#PrintReport). Se desideri aggiungere, rimuovere o modificare qualsiasi stampante, torna alla pagina **Gestione stampa** e seleziona **Stampa universale**.

## <a name="common-problems-and-resolutions"></a>Problemi comuni e soluzioni

In questa sezione verranno descritti i problemi comuni che gli utenti potrebbero riscontrare durante il tentativo di impostare o utilizzare le stampanti di Stampa universale.

### <a name="you-dont-have-access-to-the-printer-your-printer"></a>Non si dispone dell'accesso alla stampante \<your-printer\>.

Se un utente riceve questo messaggio quando tenta di stampare un documento su una stampante di Stampa universale, potrebbe essere causato da una delle seguenti condizioni:

- L'utente non ha una licenza Stampa universale assegnata al proprio account Microsoft 365 o Azure Active AD. 
- L'utente non è assegnato alla condivisione stampante in Stampa universale.
- (Locale) La registrazione dell'app di Azure usata per Stampa universale non funziona o è stata modificata di recente dall'ultimo accesso dell'utente.
- (Locale) L'utente non ha ancora effettuato l'accesso all'app registrata in Azure per l'app Stampa universale per acconsentire per la prima volta.

## <a name="there-was-an-error-fetching-printers-shared-to-you"></a>Errore durante il recupero delle stampanti condivise.

Se un utente riceve questo messaggio quando prova ad aggiungere una stampante di Stampa universale dalla pagina **Gestione stampanti**, in genere è perché non ha ancora effettuato l'accesso all'app registrata in Azure per Stampa universale né ha acconsentito per la prima volta. 
<!--
### <a name="troubleshooting"></a>Troubleshooting

#### <a name="you-dont-see-the-a-printer-in-the"></a>You don't see the a printer in the

The printer is not shared in Universal Print.

### <a name="you-get-an-error-when-tryong-to-add-all-or-a-single-printer"></a>You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## <a name="could-not-upload-the-document-to-print-job-50"></a>Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## <a name="next-steps"></a>Passaggi successivi
[Configurazione delle stampanti predefinite](ui-specify-printer-selection-reports.md).

## <a name="see-also"></a>Vedere anche

[Panoramica delle stampanti](admin-printer-setup-overview.md)  
[Configurazione delle stampanti e-mail](admin-printer-setup-email.md)
[Stampa di un report](ui-work-report.md#PrintReport)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eseguire i processi batch](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
