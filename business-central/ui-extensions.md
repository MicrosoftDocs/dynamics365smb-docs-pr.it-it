---
title: Personalizzazione di Business Central Online per con le estensioni
description: Scopri tutte le informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle estensioni.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont
ms.openlocfilehash: 8ff68bbeb2d7603b1c4d1b612413279cca5eec86
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530460"
---
# <a name="customizing-business-central-online-using-extensions"></a>Personalizzazione di Business Central Online per con le estensioni

È possibile modificare [!INCLUDE[prod_short](includes/prod_short.md)] online installando estensioni in grado ad esempio di aggiungere funzionalità, modificare il comportamento o consentire l'accesso a nuovi servizi online.

> [!NOTE]
> Per installare o disinstallare le estensioni da AppSource o aggiungere estensioni per tenant, è necessario avere le autorizzazioni appropriate. È necessario essere membri del gruppo utenti **Gestione estesa D365** oppure disporre del set di autorizzazioni **GESTIONE ESTESA - AMMINISTRATORE**. Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).  
>
> Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

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

> [!NOTE]  
> È possibile controllare la disponibilità di nuove estensioni di Microsoft e altri fornitori su [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Estensioni e trasferimento dati

Poiché le seguenti estensioni comunicano con altri servizi, potrebbero trasferire dati al di fuori della geografia dell'ambiente [!INCLUDE[prod_short](includes/prod_short.md)] :

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

## <a name="recommended-apps"></a>Applicazioni raccomandate
I partner e i rivenditori Microsoft possono creare un'estensione che possono utilizzare per compilare elenchi di applicazioni che spesso raccomandano ai loro clienti. Se lo fanno, e hanno distribuito l'estensione al tuo tenant, le app saranno disponibili nella pagina **App consigliate** . Lì puoi leggere di ogni app e decidere se installarla.

> [!NOTE]
> Se sei un partner o un rivenditore Microsoft e sei interessato a fornire un elenco di applicazioni raccomandate, vedi [Raccomandare le applicazioni da AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/customize-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Installare e disinstallare estensioni](ui-extensions-install-uninstall.md)  
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
