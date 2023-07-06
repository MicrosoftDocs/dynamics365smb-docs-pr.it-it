---
title: Installare e disinstallare app
description: Informazioni su come installare e disinstallare le app e le estensioni in Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 20350'
ms.date: 09/22/2022
ms.author: solsen
---

# <a name="install-and-uninstall-extensions-apps-in-business-central"></a><a name="install-and-uninstall-extensions-apps-in-business-central"></a><a name="install-and-uninstall-extensions-apps-in-business-central"></a>Installare e disinstallare le estensioni (app) in Business Central

È possibile modificare [!INCLUDE[prod_short](includes/prod_short.md)] installando app che, ad esempio aggiungano funzionalità, modifichino il comportamento o permettano di accedere a nuovi servizi online. Per ulteriori informazioni, vedere [Personalizzazione di Business Central usando le estensioni](ui-extensions.md).

> [!NOTE]
> Per installare o disinstallare le app da AppSource o aggiungere app per tenant, devi avere le autorizzazioni appropriate. Devi essere un membro di EXTEND. MGT. - Gruppo utenti ADMIN o è necessario disporre dell'estensione EXTEND. MGT. - set di autorizzazione ADMIN. Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda.
>
> Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.

Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.

## <a name="install-an-extension"></a><a name="install-an-extension"></a><a name="install-an-extension"></a><a name="install"></a>Installare un'estensione

Le app e le estensioni vengono gestite nella pagina **Gestione estensioni**. È possibile accedere a questa pagina dalla home page. In alternativa scegli l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo in alto a destra, inserisci **Estensione**, quindi scegli il collegamento correlato.  

È possibile ottenere le nuove app dal marketplace in [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Il mercato offre tutte le app disponibili per [!INCLUDE[prod_short](includes/prod_short.md)], oltre ad app e pacchetti di contenuti per altri prodotti Microsoft. Impostare i filtri desiderati, leggere le informazioni relative a ciascuna estensione e ottenere un'estensione per [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Accedere a [AppSource.microsoft.com](https://appsource.microsoft.com/) utilizzando l'account e-mail che si usa per [!INCLUDE[prod_short](includes/prod_short.md)]. Utilizzare lo stesso account e-mail per altri prodotti e servizi per un'esperienza fluida.  

Puoi accedere ad AppSource anche da [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Gestione estensioni** puoi vedere le app attualmente installate e aprire la pagina **Marketplace delle estensioni** che mostra le app per [!INCLUDE[prod_short](includes/prod_short.md)] al momento disponibili in AppSource. Se scegli il collegamento *Altre app*, passi ad [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Se scegli un'app, è possibile leggerne una descrizione e accedere alla Guida dell'app per ottenere ulteriori informazioni. Quando scegli di ottenere un'app, è necessario accettare le condizioni per l'utilizzo. Se ottieni l'app dal sito Web AppSource, verrà eseguito l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)] per completare l'installazione.  

Dopo aver installato un'app, potrebbe essere necessario configurarla. Alcune app richiedono che tu fornisca alcune informazioni prima di poterle utilizzare. Ad esempio, dopo aver installato l'app **PayPal Payments Standard**, devi specificare l'indirizzo e-mail o l'ID conto commerciante per il tuo conto PayPal. Per configurare un'app, o per scoprire di quali informazioni hai bisogno, nella pagina **Estensioni installate** scegli l'azione **Imposta**.  

Altre app aggiungono semplicemente dei campi a una pagina esistente oppure aggiungono una nuova pagina.

Se disinstalli un'app e successivamente cambi idea, è possibile installarla di nuovo. Quando disinstalli un'app che usi, i dati vengono mantenuti in modo da essere disponibili qualora la si reinstallasse. Alcune app sono obbligatorie. Non è possibile disinstallare le app dalla pagina **Gestione estensioni**. Se si tenta di disinstallarle, viene visualizzato un messaggio di errore.

Alcune app sono fornite da Microsoft, altre sono fornite da [altre società](ui-extensions-other.md). Tutte le app sono state sottoposte a testing prima di essere rese disponibili. Tuttavia si consiglia di accedere ai collegamenti forniti con ciascuna app per ottenere maggiori informazioni sull'app prima di scegliere di installarla.

Microsoft fornisce le seguenti app:

* [Estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
* [Registro paga di Ceridian](ui-extensions-ceridian-payroll.md)
* [Hub aziendale](ui-extensions-company-hub.md)  
* [Migrazione dei dati Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Informazioni aziendali essenziali](ui-extensions-essential-business-insights.md)
* [Analisi di immagini](ui-extensions-image-analyzer.md)
* [Cloud intelligente](ui-extensions-data-replication.md)
* [Cloud intelligente base](ui-extensions-intelligent-cloud.md)  
* [Previsioni pagamenti ritardati](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [Migrazione dei dati QuickBooks](ui-extensions-quickbooks-data-migration.md)
* [Migrazione dei dati di QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md)
* [Importazione del file retribuzioni di QuickBooks](ui-extensions-quickbooks-payroll.md)
* [Previsione vendite e magazzino](ui-extensions-sales-forecast.md)
* [Gruppo IVA](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK - Migrazione dati C5](ui-extensions-c5-data-migration.md)
* [DK - Pagamenti e riconciliazioni](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK - Formati di file .tax](ui-extensions-tax-file-formats-dk.md)
* [Estensione dei codici postali di GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Invia avviso di rimessa](ui-extensions-send-remittance-advice.md)

## <a name="set-up-an-app"></a><a name="set-up-an-app"></a><a name="set-up-an-app"></a>Impostare un'estensione
Dopo aver installato un'app, potrebbe essere necessario configurarla. Ad esempio, per l'app **PayPal Payments Standard per [!INCLUDE[prod_short](includes/prod_short.md)]** è necessario specificare il conto PayPal da utilizzare. In tal caso, al termine dell'installazione, [!INCLUDE[prod_short](includes/prod_short.md)] ti chiederà se desideri configurare l'app immediatamente. Le impostazioni possono essere obbligatorie per il funzionamento dell'app o facoltative.

Se scegli di configurare subito la tua app e ha una configurazione obbligatoria, [!INCLUDE[prod_short](includes/prod_short.md)] aprirà la configurazione obbligatoria. La configurazione può essere una pagina in cui inserire le informazioni o una guida al setup assistito che ti aiuta durante i passaggi. Se non completi l'impostazione in una volta, puoi utilizzare la pagina **Setup per _nome dell'app_**, che elenca tutte le impostazioni per l'app. Impostazioni obbligatorie indicate da **lettere in grassetto**.

## <a name="upload-a-per-tenant-extension-pte"></a><a name="upload-a-per-tenant-extension-pte"></a><a name="upload-a-per-tenant-extension-pte"></a>Caricare un'estensione per tenant (PTE)

Si carica un PTE usando la pagina di **gestione delle estensioni** . Nella pagina di **gestione delle estensioni**, vai su **Gestisci**, poi scegli **Carica estensioni**. Nella pagina **Caricare e distribuire l'estensione**, specifica il file .app da caricare. Per procedere, scegli il pulsante **Accetta** e poi il pulsante **Distribuisci**, questo inizierà il processo di distribuzione del PTE.

Se il PTE contiene modifiche allo schema di suddivisione, è possibile *forzarne* il caricamento. Per farlo, nella **modalità Schema Sync** scegli l'opzione **Forza** . Viene visualizzata una finestra di dialogo di conferma da accettare prima di procedere.  

## <a name="uninstall-an-app"></a><a name="uninstall-an-app"></a><a name="uninstall-an-app"></a>Disinstallare un'app

Si disinstalla un'app utilizzando la pagina **Gestione delle estensioni** . Per disinstallare un'app, selezionala nella pagina, quindi seleziona l'azione **Disinstalla**. Se si disinstalla un'app e successivamente si cambia idea, è possibile installare di nuovo l'app.

Quando disinstalli un'app che stai utilizzando, i dati vengono mantenuti per impostazione predefinita qualora la volessi reinstallare. È possibile scegliere di eliminare i dati con l'app. Questa operazione è controllata dall'interruttore **Elimina dati dell'estensione**. Per impostazione predefinita, questo interruttore è **disattivato**. Quando provi ad attivare l'interruttore **Elimina dati dell'estensione** per l'app, otterrai una finestra di dialogo di conferma e devi scegliere **sì** per attivarlo. Dopo aver attivato l'interruttore **Elimina dati dell'estensione** puoi disinstallare l'app e ti verrà chiesto di riconfermare che desideri disinstallare l'app ed eliminare i dati.

> [!IMPORTANT]  
> - Potrebbero esserci altre app che richiedono o dipendono dall'app che vuoi disinstallare per eseguire l'operazione. Queste altre app sono denominate *dipendenti*. Non è possibile disinstallare un'app a meno che non vengano disinstallate anche le app dipendenti.
> - Quando scegli di disinstallare un'app che ha una o più dipendenti, verrà visualizzata una finestra di dialogo di conferma che elenca le app dipendenti e chiede se desideri disinstallare l'app e tutte le app dipendenti. Dovrai selezionare **sì** per continuare.
> - Se attivi l'interruttore **Elimina dati dell'estensione**, la disinstallazione dell'app cancellerà tutti i dati per l'app **e** i dati di tutte le app dipendenti. Questa azione non può essere annullata.
> - Alcune app sono obbligatorie. Non è possibile disinstallarle dalla pagina **Gestione estensioni**. Se si tenta di disinstallarle, viene visualizzato un messaggio di errore.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Personalizzare Business Central](ui-customizing-overview.md)  
[Estensioni per Business Central fornite da altri provider](ui-extensions-other.md)  
[Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione dell'estensione dei codici postali GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Estensioni per [!INCLUDE[prod_short](includes/prod_short.md)] fornite da altri provider](ui-extensions-other.md)  
[Preparazione al business](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
