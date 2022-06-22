---
title: Installare e disinstallare estensioni
description: Informazioni su come installare e disinstallare le estensioni in Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 05/24/2022
ms.author: solsen
ms.openlocfilehash: a70ea442ffb9d6e5f131e4d720da57f033474e16
ms.sourcegitcommit: 6eeac924d8e211080316ce5068e3d4fb5a2d5ed9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804658"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Installare e disinstallare le estensioni in Business Central

È possibile modificare [!INCLUDE[prod_short](includes/prod_short.md)] installando estensioni che, ad esempio aggiungano funzionalità, modifichino il comportamento o permettano di accedere a nuovi servizi online. Per ulteriori informazioni, vedere [Personalizzazione di Business Central usando le estensioni](ui-extensions.md).

> [!NOTE]
> Per installare o disinstallare le estensioni da AppSource o aggiungere estensioni per tenant, è necessario avere le autorizzazioni appropriate. Devi essere un membro di EXTEND. MGT. - Gruppo utenti ADMIN o è necessario disporre dell'estensione EXTEND. MGT. - set di autorizzazione ADMIN. Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda.
>
> Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.

> [!NOTE]  
> Il set di autorizzazioni **EXTEND. MGT. - ADMIN** è stato introdotto nella versione Business Central 2021 primo ciclo di rilascio come sostituzione per il set di autorizzazioni **D365 EXTENSION MGT** nelle versioni precedenti.

## <a name="install-an-extension"></a><a name="install"></a>Installare un'estensione

Le estensioni vengono gestite nella pagina **Gestione estensioni**. È possibile accedere a questa pagina dalla home page. In alternativa scegli l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo in alto a destra, inserisci **Estensione**, quindi scegli il collegamento correlato.  

È possibile ottenere le nuove estensioni dal marketplace in [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). È possibile vedere tutte le estensioni disponibili per [!INCLUDE[prod_short](includes/prod_short.md)] ed è possibile ottenere app, estensioni e pacchetti di contenuto per altri prodotti Microsoft. Impostare i filtri desiderati, leggere le informazioni relative a ciascuna estensione e ottenere un'estensione per [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Accedere a [AppSource.microsoft.com](https://appsource.microsoft.com/) utilizzando l'account e-mail che si usa per [!INCLUDE[prod_short](includes/prod_short.md)]. Utilizzare lo stesso account e-mail per altri prodotti e servizi per un'esperienza fluida.  

È inoltre possibile accedere al marketplace da [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Gestione estensioni** è possibile vedere le estensioni attualmente installate e aprire la pagina **Marketplace delle estensioni** che mostra le estensioni per [!INCLUDE[prod_short](includes/prod_short.md)] al momento disponibili in AppSource. Se scegli il collegamento *Altre app*, passi ad [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Se si sceglie un'estensione, è possibile leggerne una descrizione e accedere alla Guida dell'estensione per ottenere ulteriori informazioni. Quando si sceglie di ottenere una interno, è necessario accettare le condizioni per l'utilizzo. Se ottieni l'estensione dal sito Web AppSource, verrà eseguito l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)] per completare l'installazione.  

Quando si installa un'estensione, potrebbe essere necessario configurarla. Se ad esempio si intende utilizzare l'estensione **PayPal Payments Standard per [!INCLUDE[prod_short](includes/prod_short.md)]** sarà necessario specificare un conto.
Altre estensioni aggiungono semplicemente dei campi a una pagina esistente oppure aggiungono una nuova pagina.

Se si disinstalla un'estensione e successivamente si cambia idea, è possibile installarla di nuovo. Quando si disinstalla un'estensione che si sta utilizzando, i dati vengono mantenuti in modo da essere disponibili qualora la si reinstallasse. Alcune estensioni sono obbligatorie. Non è possibile disinstallare le estensioni dalla pagina **Gestione estensioni**. Se si tenta di disinstallarle, viene visualizzato un messaggio di errore.

Alcune estensioni sono fornite da Microsoft, altre sono fornite da [altre società](ui-extensions-other.md). Tutte le estensioni sono state sottoposte a testing prima di essere rese disponibili. Tuttavia si consiglia di accedere ai collegamenti forniti con ciascuna estensione per ottenere maggiori informazioni sull'estensione prima di scegliere di installarla.

Microsoft fornisce le seguenti estensioni:

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
* [Importazione del file retribuzioni di Quickbooks](ui-extensions-quickbooks-payroll.md)
* [Previsione vendite e magazzino](ui-extensions-sales-forecast.md)
* [Gruppo IVA](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK - Migrazione dati C5](ui-extensions-c5-data-migration.md)
* [DK - Pagamenti e riconciliazioni](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK - Formati di file .tax](ui-extensions-tax-file-formats-dk.md)
* [Estensione dei codici postali di GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Invia avviso di rimessa](ui-extensions-send-remittance-advice.md)

## <a name="upload-a-per-tenant-extension-pte"></a>Caricare un'estensione per tenant (PTE)

Si carica un PTE usando la pagina di **gestione delle estensioni** . Nella pagina di **gestione delle estensioni**, vai su **Gestisci**, poi scegli **Carica estensioni**. Nella pagina **Caricare e distribuire l'estensione**, specifica il file .app da caricare. Per procedere, scegli il pulsante **Accetta** e poi il pulsante **Distribuisci**, questo inizierà il processo di distribuzione del PTE.

Se il PTE contiene modifiche allo schema di suddivisione, è possibile *forzarne* il caricamento. Per farlo, nella **modalità Schema Sync** scegli l'opzione **Forza** . Viene visualizzata una finestra di dialogo di conferma da accettare prima di procedere.  

## <a name="uninstall-an-extension"></a>Disinstallare un'estensione

Si disinstalla un'estensione utilizzando la pagina **Gestione delle estensioni** . Per disinstallare un'estensione, selezionala nella pagina, quindi seleziona l'azione **Disinstalla**. Se si disinstalla un'estensione e successivamente si cambia idea, è possibile installare di nuovo l'estensione.

Quando disinstalli un'estensione che stai utilizzando, i dati vengono mantenuti per impostazione predefinita qualora la volessi reinstallare. È possibile scegliere di eliminare i dati con l'estensione. Questa operazione è controllata dall'interruttore **Elimina dati dell'estensione**. Per impostazione predefinita, questo interruttore è **disattivato**. Quando provi ad attivare l'interruttore **Elimina dati dell'estensione** per l'estensione, otterrai una finestra di dialogo di conferma e devi scegliere **sì** per attivarlo. Dopo aver attivato l'interruttore **Elimina dati dell'estensione** puoi disinstallare l'estensione e ti verrà chiesto di riconfermare che desideri disinstallare l'estensione ed eliminare i dati.

> [!IMPORTANT]  
> - Potrebbero esserci altre estensioni che richiedono o dipendono dall'estensione che vuoi disinstallare per eseguire l'operazione. Queste altre estensioni sono denominate *dipendenti*. Non è possibile disinstallare un'estensione a meno che non vengano disinstallate anche le estensioni dipendenti.
> - Quando scegli di disinstallare un'estensione che ha una o più dipendenti, verrà visualizzata una finestra di dialogo di conferma che elenca le estensioni dipendenti e chiede se desideri disinstallare l'estensione e tutte le estensioni dipendenti. Dovrai selezionare **sì** per continuare.
> - Se attivi l'interruttore **Elimina dati dell'estensione**, la disinstallazione dell'estensione cancellerà tutti i dati per l'estensione **e** i dati di tutte le estensioni dipendenti. Questa azione non può essere annullata.
> - Alcune estensioni sono obbligatorie. Non è possibile disinstallarle dalla pagina **Gestione estensioni**. Se si tenta di disinstallarle, viene visualizzato un messaggio di errore.  

## <a name="see-also"></a>Vedere anche

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