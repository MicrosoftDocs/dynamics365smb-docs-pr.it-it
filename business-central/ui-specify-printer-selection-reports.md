---
title: Configurazione delle stampanti
description: Informazioni sulla configurazione delle stampanti per report e documenti e sulle diverse funzionalità di stampa disponibili in Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 2650, 2750, 2752, 2753, 2754, 8900,
ms.date: 09/22/2022
ms.author: jswymer
ms.openlocfilehash: 07cda9c796a08436dc48d623f64fcc1252305a14
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607744"
---
# <a name="set-up-printers"></a>Configurare le stampanti

La stampa di documenti e report da [!INCLUDE[prod_short](includes/prod_short.md)] è un compito importante per gli utenti aziendali. Gli utenti vogliono in genere inviare i lavori di stampa direttamente a una delle stampanti della tua organizzazione&mdash;indipendentemente dal [!INCLUDE[prod_short](includes/prod_short.md)] client o dall'app che stanno utilizzando. Poiché [!INCLUDE[prod_short](includes/prod_short.md)] online è un servizio cloud, non può raggiungere direttamente le stampanti locali collegate ai dispositivi degli utenti, ma puoi connetterlo a stampanti abilitate per il cloud.

Per supportare le tue esigenze di stampa, [!INCLUDE[prod_short](includes/prod_short.md)] offre le seguenti caratteristiche:

|Funzionalità|Descrizione|Client Web| App per dispositivi mobili|App per Teams|
|-------|-----------|----------|-----------|--------------|
|Stampa universale|Stampa universale è una soluzione di gestione della stampante disponibile come servizio cloud di Microsoft. Con questa funzione, puoi configurare le tue stampanti in Stampa universale, quindi registrarle per l'uso in [!INCLUDE[prod_short](includes/prod_short.md)]. Questa funzione richiede un abbonamento a Stampa universale e l'estensione **Integrazione di Stampa universale**|![disponibile online.](media/check.png)|![disponibile online.](media/check.png)|![funziona online](media/check.png)|
|Stampa con indirizzo e-mail|Questa funzione consente di configurare stampanti abilitate per la posta elettronica. [!INCLUDE[prod_short](includes/prod_short.md)] quindi invia i lavori di stampa a una stampante utilizzando l'indirizzo e-mail della stampante. Questa funzione richiede stampanti abilitate per la posta elettronica e l'estensione **Invia a stampante e-mail**.|![disponibile online.](media/check.png)|![funziona online](media/check.png)|![funziona online](media/check.png)|
|Stampa tramite browser|I lavori di stampa sono gestiti dalla funzionalità di stampa del browser dell'utente. Se una stampante cloud non è installata e configurata, o se una stampante installata non funziona, la stampa imposterà automaticamente le opzioni di stampa per il browser. Il campo **Stampante** verrà visualizzato nella pagina di richiesta del report *(Gestita dal browser)*.|![funziona online](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] supporta altre estensioni stampante personalizzate che aggiungono ancora più funzioni di stampa. Pertanto, se sono installate estensioni della stampante personalizzate, la tua applicazione potrebbe includere funzionalità di stampa non descritte in questo articolo. 

## <a name="set-up-universal-print"></a>Configurazione della stampa universale

Stampa universale è un servizio basato su abbonamento a Microsoft 365 che funziona interamente su Microsoft Azure. Offre una gestione centralizzata della stampante tramite il portale Stampa universale. [!INCLUDE[prod_short](includes/prod_short.md)] rende disponibili agli utenti client le stampanti configurate in Stampa universale tramite l'estensione **Integrazione di stampa universale**.

![Configurazione della stampa universale.](media/Universal-Print-arch.png)

La configurazione completa richiede che tu lavori in Microsoft Azure, usando il [portale di Azure](https://portal.azure.com) e in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Stampanti supportate

[!INCLUDE[prod_short](includes/prod_short.md)] supporta le stesse stampanti di Stampa universale, che possono essere stampanti compatibili con Stampa universale o non compatibili. Le stampanti non compatibili non possono comunicare direttamente con Stampa universale, quindi richiedono un software per un connettore aggiuntivo, fornito da Stampa universale. Alcune stampanti meno recenti potrebbero non essere supportate. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Prerequisiti

**Per [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 primo ciclo di rilascio o successivi.
- L'estensione **Integrazione di stampa universale** è installata.

    Questa estensione è pubblicata e installata per impostazione predefinita come parte di [!INCLUDE[prod_short](includes/prod_short.md)] online e in locale. Puoi verificare se è installata nella pagina **Gestione delle estensioni**. Per ulteriori informazioni, vedi [Installare e disinstallare le estensioni in Business Central](ui-extensions-install-uninstall.md).

- [!INCLUDE[prod_short](includes/prod_short.md)] in locale:
  - L'autenticazione Azure Active Directory o NavUserPassword è configurata.
  - Un'applicazione per Business Central è registrata nel tuo tenant Azure AD e [!INCLUDE[prod_short](includes/prod_short.md)].

      Come altri servizi di Azure che funzionano con [!INCLUDE[prod_short](includes/prod_short.md)], Stampa universale richiede la registrazione di un'app per [!INCLUDE[prod_short](includes/prod_short.md)] in Azure AD. La registrazione dell'app fornisce servizi di autenticazione e autorizzazione tra [!INCLUDE[prod_short](includes/prod_short.md)] e Stampa universale.

      La tua distribuzione potrebbe già usare una registrazione dell'app per altri servizi di Azure, come Power BI. In tal caso, utilizza anche la registrazione dell'app esistente per Stampa universale, invece di aggiungerne una nuova. L'unica cosa che dovrai fare, in questo caso, è modificare la registrazione dell'app per includere le autorizzazioni di stampa pertinenti per l'API Microsoft Graph.

      Per registrare un'app e impostare le autorizzazioni appropriate, segui i passaggi descritti in [Registra un'applicazione in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Per Stampa universale**

- Un abbonamento o una licenza Stampa universale per la tua organizzazione.

    Per ulteriori informazioni, vedi [Licenza di Stampa universale](/universal-print/fundamentals/universal-print-license).

- Possiedi i ruoli **Gestione stampante** e **Amministratore globale** in Azure.

    Per gestire Stampa universale, il tuo account deve disporre dei ruoli **Gestione stampante** e **Amministratore globale** in Azure AD. Questi ruoli sono necessari solo per la gestione di Stampa universale. Non sono richiesti dagli utenti che utilizzano le stampanti da [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Configurazione di Stampa universale e aggiunta di stampanti in Microsoft Azure

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

5. Condividi le stampanti.

    Qualsiasi stampante che desideri utilizzare in [!INCLUDE[prod_short](includes/prod_short.md)] deve essere condivisa in Stampa universale.

    <!--Learn more at [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Per ulteriori informazioni, vedi [Condividere una stampante](/universal-print/portal/share-printers).

6. Autorizza gli utenti per le stampanti condivise.

    <!--Learn more at [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Per ulteriori informazioni, vedi [Autorizzazioni della stampante](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Abilita la conversione dei documenti.

    Stampa universale esegue il rendering del contenuto per la stampa in formato XPS. Alcune stampanti legacy non supportano il rendering dei contenuti XPS&mdash;in molti casi, solo in formato PDF. La stampa su queste stampanti non riuscirà a meno che legacy non sia impostata per convertire i documenti nel formato supportato dalla stampante.

    Per ulteriori informazioni, vedi [Panoramica sulla conversione dei documenti](/universal-print/portal/document-conversion).

Ora sei pronto per aggiungere le stampanti a [!INCLUDE[prod_short](includes/prod_short.md)], configurare le stampanti predefinite per i report e stampare.  

### <a name="add-universal-print-printers-to-business-central"></a>Aggiungere le stampanti Stampa universale a Business Central

Dopo che le stampanti sono state configurate e condivise in Stampa universale, sei pronto per utilizzarle in Business Central. Esistono due modi per aggiungere stampanti Stampa universale. Puoi aggiungere le stampanti tutte in una volta o singolarmente, una alla volta.

L'aggiunta di stampanti singole consente di configurare la stessa stampante Stampa universale in Business Central più di una volta. Quindi, per ogni stampante aggiunta, puoi modificare le impostazioni di stampa, come il vassoio della carta, le dimensioni e l'orientamento. In questo modo, puoi impostare stampanti per diversi report e documenti con requisiti di output speciali.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gestione stampante**, quindi scegli il collegamento correlato.
2. Seleziona **Stampa universale**, quindi una delle seguenti opzioni:

    - **Aggiungi tutte le stampanti di Stampa universale** per aggiungere tutte le stampanti che non sono già state aggiunte. Puoi utilizzare questa opzione anche se sono già state aggiunte stampanti. 

    - **Aggiungi una stampante di Stampa universale** per aggiungere una stampante specifica.  
3. Segui le istruzioni sullo schermo.

    - Se hai scelto **Aggiungi tutte le stampanti di Stampa universale** viene avviata la configurazione **Aggiungi stampanti di Stampa universale**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Se hai scelto **Aggiungi una stampante di Stampa universale** viene visualizzata la pagina **Impostazioni di Stampa universale**. Compila il campo **Nome** e seleziona **...** accanto al campo **Condivisione di stampa in Stampa universale** per selezionare la stampante di Stampa universale. Compila i rimanenti campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Queste azioni verificano la tua configurazione Azure AD (in locale), controlla di possedere la licenza di Stampa universale, infine aggiungi le stampanti.

    > [!NOTE]
    > Per i servizi locali, se è la prima volta che ti connetti a Stampa universale, viene visualizzata la pagina AUTORIZZAZIONI DI SERVIZIO AZURE ACTIVE DIRECTORY e ti verrà richiesto di dare il consenso ai servizi di Azure. Devi solo dare il consenso una volta.

Dopo che una stampante è stata aggiunta, puoi visualizzarne e modificarne le impostazioni dalla pagina **Gestione stampante**. Seleziona la stampante, quindi scegli **Modifica impostazioni stampante**. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned an UP license
- You have not been given access to the printer in UP.
- (On-premises) The app registration has been broken.
-->
## <a name="set-up-email-print"></a>Configurazione della stampa e-mail

### <a name="prerequisites"></a>Prerequisiti

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 primo ciclo di rilascio o successivi
- L'estensione **Invia a stampante e-mail** è installata

    Questa estensione è installata per impostazione di default. Per informazioni sull'installazione delle estensioni, vedi<!--see what?--> 
- La funzionalità e-mail è impostata.

   Per ulteriori informazioni, vedi [Configurazione e-mail](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Aggiungi una stampante e-mail

La pagina **Gestione stampante** mostra le stampanti attualmente configurate. La pagina ti dà anche accesso alla pagina **Impostazioni** per ciascuna stampante per modificare una configurazione esistente o configurare una nuova stampante.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gestione stampante**, quindi scegli il collegamento correlato.
2. Seleziona **Stampa e-mail**, quindi scegli **Aggiungi una stampante e-mail**.
3. Compila i campi nella pagina **Impostazioni stampante e-mail** in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > È necessario selezionare manualmente il formato carta appropriato per una stampante poiché non è possibile memorizzare alcuna stampante locale o impostazioni dell'utente.
    >
    > Assicurati che l'estensione Stampante e-mail non sia impostata sul formato carta **A4** per impostazione predefinita, che non è adatto in Nord America, ad esempio.

### <a name="privacy-notice"></a>Informativa sulla privacy

Se usi l'estensione Stampante e-mail, tutti o alcuni lavori di stampa vengono inviati all'indirizzo e-mail configurato per la stampante. Si consiglia vivamente di associare un ID e-mail univoco a un dispositivo stampante utilizzando solo i servizi ufficiali forniti dal produttore dell'hardware, come HP ePrint, KonicaMinolta EveryonePrint o Epson Email Print.

Prendi tutte le precauzioni sulla privacy necessarie, assicurati che la soluzione di stampa e-mail abbia le autorizzazioni, le impostazioni sulla privacy e i criteri di conservazione configurati correttamente. È responsabilità dell'utente fornire un indirizzo e-mail corretto, verificato e operativo. Per ulteriori informazioni, vedi [Informativa sulla privacy di Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="set-up-default-printers"></a><a name="default"></a>Configurazione delle stampanti predefinite

Esistono due modi per configurare le stampanti che vengono utilizzate per impostazione predefinita per i lavori di stampa. Una stampante predefinita è utile se si lavora con report diversi che richiedono stampanti diverse a causa del loro posizionamento nell'azienda o delle loro capacità di output.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Imposta una stampante come stampante predefinita per tutti i lavori di stampa

La pagina **Gestione stampante** ti consente di impostare una stampante come stampante predefinita per tutti i lavori di stampa. Puoi specificare la stampante come predefinita solo per te o per tutti gli utenti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gestione stampante**, quindi scegli il collegamento correlato.

    > [!TIP]
    > Puoi anche aprire la pagina **Gestione stampante** dalla pagina **Selezioni della stampante** scegliendo **Gestione stampante**.  
2. Nella pagina **Gestione stampante**, seleziona una stampante dall'elenco, scegli **Gestisci**, quindi scegli **Imposta come stampante di default personale** o **Imposta come stampante predefinita per tutti gli utenti**.

> [!NOTE]
> L'impostazione di una stampante predefinita da **Gestione stampante** aggiunge una voce in **Selezioni della stampante**.

### <a name="set-a-default-printer-for-specific-reports"></a>Imposta una stampante predefinita per report specifici

La pagina **Selezioni della stampante** ti consente di specificare la stampante che un report utilizza per impostazione predefinita. Le stampanti predefinite vengono impostate in base all'account utente. Puoi impostare una stampante predefinita solo per te stesso, per un altro utente o per tutti gli utenti.

> [!IMPORTANT]
> Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, la pagina **Selezioni della stampante** può essere utilizzata solo per le stampanti cloud definite dalle estensioni della stampante, come le stampanti Stampa e-mail e Stampa universale. Non può essere utilizzata per le stampanti locali.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Selezioni della stampante**, quindi scegli il collegamento correlato. In alternativa, seleziona una stampante dalla pagina **Gestione stampante**, quindi scegli l'azione **Selezioni stampante**.
2. Scegli l'azione **Nuovo** per aggiungere una selezione di stampanti per un report specifico.
3. Compilare i campi in base alle esigenze.

Il report specificato è ora impostato per la stampa sulla stampante selezionata per impostazione predefinita.

> [!NOTE]
> Quando si stampa il report in questione, puoi selezionarne uno diverso utilizzando il campo **Stampa** nella pagina della richiesta report.

> [!NOTE]
> Se non si imposta un report per una stampante specifica sulla pagina **Selezioni stampante**, la stampa viene effettuata sulla stampante predefinita della società, come definito nella pagina **Gestione stampante**.

Tu o l'amministratore potete anche usare la pagina **Selezioni stampante** per definire altre varianti di stampa per utenti e report. Nella seguente tabella viene descritta la combinazione dei valori per specificare diverse configurazioni di stampa per un report.

|A                                                 |Impostare i seguenti valori                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Stampare un report su una stampante specifica per tutti gli utenti |Specificare i valori nei campi **Nome stampante** e **ID report** e lasciare vuoto il campo **ID utente**.|
|Stampare tutti i report su una stampante specifica per un utente specifico|Specificare i valori nei campi **ID utente** e **Nome stampante** e lasciare vuoto il campo **ID utente**. Questa voce ha la stessa funzione di **Imposta come stampante di default personale** nella pagina **Gestione della stampa**.|
|Impostare la stampante di default per tutti gli utenti|Specificare un valore nel campo **Nome stampante** e lasciare vuoti i campi **ID utente** e **ID report**. Questa voce ha la stessa funzione di **Imposta come stampante predefinita per tutti gli utenti** nella pagina **Gestione della stampa**.|
|Stampare un report specifico sulla stampante di default dell'utente|Specificare un valore nel campo **ID report** e lasciare vuoti i campi **Nome stampante** e **ID utente**.|
|Stampare un report specifico su una stampante specifica per un utente specifico|Specificare i valori in tutti e tre i campi.|

> [!NOTE]
> Altre selezioni stampante specifiche hanno la precedenza su una selezione stampante generale. Ad esempio, una selezione di stampante che ha valori nei campi **ID utente**, **ID report** e **Nome stampante** ha la precedenza su una selezione di stampante che ha voci vuote nei campi **ID utente** o **ID report**.

### <a name="choosing-the-printer-when-running-a-report"></a>Scelta della stampante durante l'esecuzione di un report

Invece di utilizzare la stampante predefinita durante l'esecuzione di un report, è possibile ignorare questa impostazione dalla pagina della richiesta. Basta scegliere la stampante che vuoi utilizzare per questa generazione del report nel menu a discesa **Stampante**.

### <a name="sizing-print-jobs"></a>Ridimensionamento dei lavori di stampa

La stampa cloud è progettata per documenti di dimensioni ragionevoli. La maggior parte dei servizi cloud, inclusi PrintNode e HP ePrint, ha un limite di 10 MB per processo. Se è necessario stampare report più grandi, potrebbe essere necessario dividerli in più stampe.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/change-documents-dynamics-365-business-central/).

## <a name="see-also"></a>Vedere anche

[Stampa di un report](ui-work-report.md#PrintReport)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eseguire i processi batch](ui-how-run-batch-jobs.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
