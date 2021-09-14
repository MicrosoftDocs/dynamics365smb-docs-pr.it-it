---
title: Installare le estensioni per personalizzare Business Central
description: Scopri tutte le informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle estensioni.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/25/2021
ms.author: edupont
ms.openlocfilehash: b408afe65f2063ab77dca4e4e87fcfc4715f1204
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440505"
---
# <a name="customizing-business-central-online-using-extensions"></a>Personalizzazione di Business Central Online per con le estensioni

È possibile modificare [!INCLUDE[prod_short](includes/prod_short.md)] online installando estensioni in grado ad esempio di aggiungere funzionalità, modificare il comportamento o consentire l'accesso a nuovi servizi online.

> [!NOTE]
> Per installare o disinstallare le estensioni da AppSource o aggiungere estensioni per tenant, è necessario avere le autorizzazioni appropriate. Devi essere un membro di EXTEND. MGT. - Gruppo utenti ADMIN o è necessario disporre dell'estensione EXTEND. MGT. - set di autorizzazione ADMIN. Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda.
>
> Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.

> [!NOTE]  
> Il set di autorizzazioni **EXTEND. MGT. - ADMIN** è stato introdotto nella versione Business Central 2021 primo ciclo di rilascio come sostituzione per il set di autorizzazioni **D365 EXTENSION MGT** nelle versioni precedenti.

> [!IMPORTANT]  
> Il caricamento di estensioni per tenant e l'installazione di estensioni AppSource non sono supportati tramite la pagina **Gestione delle estensioni** per installazioni locali. Non è possibile installare le estensioni AppSource locali, neanche nelle distribuzioni basate su Docker.

La prima volta che si avvia [!INCLUDE[prod_short](includes/prod_short.md)], alcune estensioni risultano già installate. Con il tempo verranno rese disponibili altre estensioni e sarà possibile scegliere se installarle o meno.

Ad esempio, Microsoft fornisce un'estensione che consente l'integrazione con PayPal Payments Standard. Questa estensione è installata per impostazione di default.
Se tuttavia diventa disponibile un'altra estensione che offre l'integrazione con un altro servizio di pagamento, è possibile installare la nuova estensione e scegliere quale dei due servizi utilizzare.  

Le estensioni vengono gestite nella pagina **Gestione estensioni**. È possibile accedere a questa pagina dalla home page. In alternativa, scegliere l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo superiore destro, immettere **Estensione**, quindi scegliere il collegamento correlato. Per ulteriori informazioni, vedere [Installazione e disinstallazione delle estensioni](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Se si prevede di dover accedere a un'estensione, ma non è possibile individuare la relativa funzionalità, controllare la pagina **Gestione estensioni**, se l'estensione non è elencata, è possibile installarla come descritto nella sezione seguente.  

> [!NOTE]  
> Accedere a [AppSource.microsoft.com](https://appsource.microsoft.com/) tramite l'account di posta elettronica utilizzato per [!INCLUDE[prod_short](includes/prod_short.md)] online. Utilizzare lo stesso account e-mail per altri prodotti e servizi per un'esperienza fluida.  

È inoltre possibile accedere al marketplace da [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Gestione estensioni** è possibile vedere le estensioni attualmente installate e aprire la pagina **Marketplace delle estensioni** che mostra le estensioni per [!INCLUDE[prod_short](includes/prod_short.md)] al momento disponibili in AppSource. Se si sceglie il collegamento *Altre app*, si passa a [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Se si sceglie un'estensione, è possibile leggerne una descrizione e accedere alla Guida dell'estensione per ottenere ulteriori informazioni. Quando si sceglie di ottenere una interno, è necessario accettare le condizioni per l'utilizzo. Se si ottiene l'estensione dal sito Web AppSource, verrà eseguito l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)] per completare l'installazione.  

Quando si installa un'estensione, potrebbe essere necessario configurarla. Se ad esempio si intende utilizzare l'estensione **PayPal Payments Standard per [!INCLUDE[prod_short](includes/prod_short.md)]** sarà necessario specificare un conto.
Altre estensioni aggiungono semplicemente dei campi a una pagina esistente oppure aggiungono una nuova pagina.   

Se si disinstalla un'estensione e successivamente si cambia idea, è possibile installarla di nuovo. Quando si disinstalla un'estensione che si sta utilizzando, i dati vengono mantenuti in modo da essere disponibili qualora la si reinstallasse. Alcune estensioni sono obbligatorie. Non è possibile disinstallarle dalla pagina **Gestione estensioni**. Se si tenta di disinstallarle, viene visualizzato un messaggio di errore.  

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

> [!NOTE]  
> È possibile controllare la disponibilità di nuove estensioni di Microsoft e altri fornitori su [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Estensioni e trasferimento dati

Poiché le seguenti estensioni stanno comunicando con altri servizi, potrebbero trasferire dati al di fuori dell'area geografica dell'ambiente [!INCLUDE[prod_short](includes/prod_short.md)]:

* Estensione AMC Banking 365 Fundamentals
* Analisi di immagini
* Previsione pagamento ritardato
* PayPal Payments Standard
* Previsione vendite e magazzino
* WorldPay Payments Standard

Questo vale anche per alcune funzionalità nell'applicazione di base, come le seguenti capacità:

* Previsione flusso di cassa
* Servizio di scambio documenti
* Connessioni Dataverse
* Servizio OCR
* Online Map
* Reg. IVA UE No. Assistenza

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
