---
title: Installare le estensioni per personalizzare Business Central | Documenti Microsoft
description: Informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle estensioni.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 11/27/2018
ms.author: edupont
ms.openlocfilehash: f093a9ce2a654d5ee693ee91f32e87f6546279d1
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "852449"
---
# <a name="customizing-business-central-using-extensions"></a>Personalizzazione di Business Central con le estensioni
È possibile modificare [!INCLUDE[d365fin](includes/d365fin_md.md)] installando estensioni che, ad esempio, aggiungano funzionalità, modifichino il comportamento o permettano di accedere a nuovi servizi online.
La prima volta che si avvia [!INCLUDE[d365fin](includes/d365fin_md.md)], alcune estensioni risultano già installate. Con il tempo verranno rese disponibili altre estensioni e sarà possibile scegliere se installarle o meno.

Ad esempio, Microsoft fornisce un'estensione che consente l'integrazione con PayPal Payments Standard. Questa estensione è installata per impostazione di default.
Se tuttavia diventa disponibile un'altra estensione che offre l'integrazione con un altro servizio di pagamento, è possibile installare la nuova estensione e scegliere quale dei due servizi utilizzare.  

Le estensioni vengono gestite nella pagina **Gestione estensioni**. È possibile accedere a questa pagina dalla home page. In alternativa, scegliere l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo superiore destro, immettere **Estensione**, quindi scegliere il collegamento correlato.  

> [!NOTE]  
>   Se si prevede di dover accedere a un'estensione, ma non è possibile individuare la relativa funzionalità, controllare la pagina **Gestione estensioni**, se l'estensione non è elencata, è possibile installarla come descritto nella sezione seguente.  

## <a name="installing-an-extension"></a>Installazione di un'estensione
È possibile ottenere le nuove estensioni dal marketplace in [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?src=dynamics365website&product=dynamics-365-business-central). È possibile vedere tutte le estensioni disponibili per [!INCLUDE[d365fin](includes/d365fin_md.md)] ed è possibile ottenere app, estensioni e pacchetti di contenuto per altri prodotti Microsoft. Impostare i filtri desiderati, leggere le informazioni relative a ciascuna estensione e ottenere un'estensione per [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Accedere a [AppSource.microsoft.com](https://appsource.microsoft.com/) utilizzando l'account e-mail che si usa per [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilizzare lo stesso account e-mail per altri prodotti e servizi per un'esperienza fluida.  

È inoltre possibile accedere al marketplace da [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nella pagina **Gestione estensioni** è possibile vedere le estensioni attualmente installate e aprire la pagina **Marketplace delle estensioni** che mostra le estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] al momento disponibili in AppSource. Se si sceglie il collegamento *Altre app*, si passa a [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Se si sceglie un'estensione, è possibile leggerne una descrizione e accedere alla Guida dell'estensione per ottenere ulteriori informazioni. Quando si sceglie di ottenere una interno, è necessario accettare le condizioni per l'utilizzo. Se si ottiene l'estensione dal sito Web AppSource, verrà eseguito l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] per completare l'installazione.  

Quando si installa un'estensione, potrebbe essere necessario configurarla. Se ad esempio si intende utilizzare l'estensione **PayPal Payments Standard per [!INCLUDE[d365fin](includes/d365fin_md.md)]** sarà necessario specificare un conto.
Altre estensioni aggiungono semplicemente dei campi a una pagina esistente oppure aggiungono una nuova pagina.   

Se si disinstalla un'estensione e successivamente si cambia idea, è possibile installarla di nuovo. Quando si disinstalla un'estensione che si sta utilizzando, i dati vengono mantenuti in modo da essere disponibili qualora la si reinstallasse.  

Alcune estensioni sono fornite da Microsoft, altre sono fornite da [altre società](ui-extensions-other.md). Tutte le estensioni sono state sottoposte a testing prima di essere rese disponibili. Tuttavia si consiglia di accedere ai collegamenti forniti con ciascuna estensione per ottenere maggiori informazioni sull'estensione prima di scegliere di installarla.  

Microsoft fornisce le seguenti estensioni:  

* [Migrazione dei dati Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
* [Feed bancari di Envestnet Yodlee](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [Migrazione dei dati QuickBooks](ui-extensions-quickbooks-data-migration.md)  
* [Previsione vendite e magazzino](ui-extensions-sales-forecast.md)  
* [Registro paga di Ceridian](ui-extensions-ceridian-payroll.md)  
* [Importazione del file retribuzioni di Quickbooks](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)  
* [Utilizzare codici postali di GetAddress.io per il Regno Unito](ui-extensions-getaddressio.md)  
* [Migrazione dei dati di QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md)  
* [Portale contabile](ui-extensions-accountant-portal.md)  
* [Analisi di immagini](ui-extensions-image-analyzer.md)  
* [Pagamenti e riconciliazioni (DK)](ui-extensions-payments-reconciliation-formats-dk.md)  
* [Migrazione dati C5](ui-extensions-c5-data-migration.md)  
* [Informazioni aziendali essenziali](ui-extensions-essential-business-insights.md)  
* [Previsioni pagamenti ritardati](ui-extensions-late-payment-prediction.md  )

> [!NOTE]  
>  Le nuove estensioni non saranno subito disponibili in AppSource dopo l'annuncio di un aggiornamento. Seguire gli aggiornamenti sulla disponibilità delle estensioni tramite il sito Web [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Vedi anche
[Estensione di Dynamics 365 Business Central](about-develop-extensions.md)  
[Estensioni per Business Central fornite da altri provider](ui-extensions-other.md)  
[Impostare il servizio di Feed bancario di Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  
[Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione dell'estensione dei codici postali GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] fornite da altri provider](ui-extensions-other.md)  
[Introduzione](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
