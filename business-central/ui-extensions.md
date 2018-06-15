---
title: Installare le estensioni per personalizzare Business Central | Documenti Microsoft
description: "Informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle estensioni."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 07/07/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 55de1952941f6f8d01d76c657fcf8c48d7ada6b1
ms.contentlocale: it-it
ms.lasthandoff: 05/17/2018

---
# <a name="customizing-business-central-using-extensions"></a>Personalizzazione di Business Central con le estensioni
È possibile modificare [!INCLUDE[d365fin](includes/d365fin_md.md)] installando estensioni che, ad esempio, aggiungano funzionalità, modifichino il comportamento o permettano di accedere a nuovi servizi online.
La prima volta che si avvia [!INCLUDE[d365fin](includes/d365fin_md.md)], alcune estensioni risultano già installate. Con il tempo verranno rese disponibili altre estensioni e sarà possibile scegliere se installarle o meno.

Ad esempio, Microsoft fornisce un'estensione che consente l'integrazione con PayPal Payments Standard. Questa estensione è installata per impostazione di default.
Se tuttavia diventa disponibile un'altra estensione che offre l'integrazione con un altro servizio di pagamento, è possibile installare la nuova estensione e scegliere quale dei due servizi utilizzare.  

Le estensioni vengono gestite nella finestra **Gestione estensioni**. È possibile accedere a questa finestra dalla home page. In alternativa, scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report") nell'angolo superiore destro, inserire **Estensione**, quindi scegliere il collegamento correlato.  

> [!NOTE]  
>   Se si prevede di dover accedere a un'estensione, ma non è possibile individuare la relativa funzionalità, controllare la finestra **Gestione estensioni**, se l'estensione non è elencata, è possibile installarla come descritto nella sezione seguente.  

## <a name="installing-an-extension"></a>Installazione di un'estensione
È possibile ottenere le nuove estensioni dal marketplace all'indirizzo [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1) dove sono disponibili tutte le estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] e le app, le estensioni e i pacchetti di contenuti per altri prodotti Microsoft. Impostare i filtri desiderati, leggere le informazioni relative a ciascuna estensione e ottenere un'estensione per [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Accedere ad [AppSource.microsoft.com](https://appsource.microsoft.com/) utilizzando l'account e-mail che si usa per [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilizzare lo stesso account e-mail per altri prodotti e servizi per un'esperienza fluida.  

È inoltre possibile accedere al marketplace da [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nella finestra **Gestione estensioni** è possibile vedere le estensioni attualmente installate e aprire la pagina **Marketplace delle estensioni** che mostra le estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] al momento disponibili in AppSource. Se si sceglie il collegamento *Altre app*, si passa a [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Se si sceglie un'estensione, è possibile leggerne una descrizione e accedere alla Guida dell'estensione per ottenere ulteriori informazioni. Quando si sceglie di ottenere una interno, è necessario accettare le condizioni per l'utilizzo. Se si ottiene l'estensione dal sito Web AppSource, verrà eseguito l'accesso in [!INCLUDE[d365fin](includes/d365fin_md.md)] per completare l'installazione.  

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
* [Migrazione dei dati online QuickBooks](ui-extensions-quickbooks-online-data-migration.md)  
* [Portale contabile](ui-extensions-accountant-portal.md)  
* [Analisi di immagini](ui-extensions-image-analyzer.md)  
* [Pagamenti e riconciliazioni (DK)](ui-extensions-payments-reconciliation-formats-dk.md)  
* [Migrazione dati C5](ui-extensions-c5-data-migration.md)  
* [Informazioni aziendali essenziali](ui-extensions-essential-business-insights.md)  

> [!NOTE]  
>  Le nuove estensioni non saranno subito disponibili in AppSource dopo l'annuncio di un aggiornamento. Seguire gli aggiornamenti sulla disponibilità delle estensioni tramite il sito Web [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Vedi anche
[Impostare il servizio di Feed bancario di Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  
[Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione dell'estensione dei codici postali GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] fornite da altri provider](ui-extensions-other.md)  
[Introduzione](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

