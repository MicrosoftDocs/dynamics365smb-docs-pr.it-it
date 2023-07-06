---
title: Personalizzazione di Business Central Online con le app
description: Scopri tutte le informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle app in questo articolo.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: edupont
---
# <a name="customizing-business-central-online-with-apps"></a><a name="customizing-business-central-online-with-apps"></a><a name="customizing-business-central-online-with-apps"></a>Personalizzazione di Business Central Online con le app

È possibile modificare [!INCLUDE[prod_short](includes/prod_short.md)] online installando app in grado ad esempio di aggiungere funzionalità, modificare il comportamento o consentire l'accesso a nuovi servizi online. Queste app sono anche chiamate *estensioni* perché *estendono* [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a><a name="manage-apps"></a><a name="manage-apps"></a>Gestire le app

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

La prima volta che si avvia [!INCLUDE[prod_short](includes/prod_short.md)], alcune app risultano già installate. Con il tempo verranno rese disponibili altre app e sarà possibile scegliere se installarle o meno.

Ad esempio, Microsoft fornisce un'app che consente l'integrazione con PayPal Payments Standard. Questa estensione è installata per impostazione di default. Se tuttavia diventa disponibile un'altra estensione che offre l'integrazione con un altro servizio di pagamento, è possibile installare la nuova estensione e scegliere quale dei due servizi utilizzare.  

Per utilizzare la funzionalità fornita da un'app, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'app.

Per installare o disinstallare le app da AppSource o aggiungere estensioni per tenant, devi avere le autorizzazioni appropriate. È necessario essere membri del gruppo utenti **Gestione estesa D365** oppure disporre del set di autorizzazioni **GESTIONE ESTESA - AMMINISTRATORE**. Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> Per [!INCLUDE [prod_short](includes/prod_short.md)] in locale, non è possibile caricare estensioni per tenant o installare app di AppSource tramite la pagina **Gestione estensioni**. Non è possibile installare le app AppSource locali, neanche nelle distribuzioni basate su Docker.

Le app vengono gestite nella pagina **Gestione estensioni**. È possibile accedere a questa pagina dalla home page. In alternativa, scegliere l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo superiore destro, immettere **Estensione**, quindi scegliere il collegamento correlato. Per ulteriori informazioni, vedi [Installare e disinstallare le app](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Se ritieni di dover accedere a un'app, ma non è possibile individuare la relativa funzionalità, controlla la pagina **Gestione estensioni**, se l'app non è elencata, è possibile installarla come descritto nella sezione seguente.  

> [!NOTE]  
> Accedere a [AppSource.microsoft.com](https://appsource.microsoft.com/) tramite l'account di posta elettronica utilizzato per [!INCLUDE[prod_short](includes/prod_short.md)] online. Utilizzare lo stesso account e-mail per altri prodotti e servizi per un'esperienza fluida.  

È inoltre possibile accedere al marketplace da [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Gestione estensioni** puoi vedere le app attualmente installate e aprire la pagina **Marketplace delle estensioni** che mostra le app per [!INCLUDE[prod_short](includes/prod_short.md)] al momento disponibili in AppSource. Se si sceglie il collegamento *Altre app*, si passa a [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Se scegli un'app, è possibile leggerne una descrizione e accedere alla Guida dell'app per ottenere ulteriori informazioni. Quando scegli di ottenere un'app, è necessario accettare le condizioni per l'utilizzo. Se ottieni l'app dal sito Web AppSource, verrà eseguito l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)] per completare l'installazione.  

Quando installi un'app, potrebbe essere necessario configurarla. Se ad esempio vuoi utilizzare l'estensione **PayPal Payments Standard per [!INCLUDE[prod_short](includes/prod_short.md)]** sarà necessario specificare un conto.
Altre app aggiungono semplicemente dei campi a una pagina esistente oppure aggiungono una nuova pagina.   

Se disinstalli un'app e successivamente cambi idea, è possibile installarla di nuovo. Quando disinstalli un'app che usi, i dati vengono mantenuti in modo da essere disponibili qualora la si reinstallasse. Alcune app sono obbligatorie. Non è possibile disinstallarle dalla pagina **Gestione estensioni**. Se si tenta di disinstallarle, viene visualizzato un messaggio di errore.  

Alcune app sono fornite da Microsoft, altre sono fornite da [altre società](ui-extensions-other.md). Tutte le app sono state sottoposte a testing prima di essere rese disponibili. Tuttavia si consiglia di accedere ai collegamenti forniti con ciascuna estensione per ottenere maggiori informazioni sull'app prima di scegliere di installarla.  

> [!NOTE]  
> È possibile controllare la disponibilità di nuove app di Microsoft e altri fornitori su [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a><a name="apps-and-data-transfer"></a><a name="apps-and-data-transfer"></a>App e trasferimento dati

Poiché le seguenti app comunicano con altri servizi, potrebbero trasferire dati al di fuori della geografia dell'ambiente [!INCLUDE[prod_short](includes/prod_short.md)] :

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
* Mappa online
* Reg. IVA UE No. Assistenza

## <a name="connect-your-business"></a><a name="connect-your-business"></a><a name="connect-your-business"></a>Collega l'azienda

A partire dal secondo ciclo di rilascio del 2022, gli ambienti online [!INCLUDE [prod_short](includes/prod_short.md)] possono elencare una o più app nelle pagine **App di connettività** e **App bancarie**. Queste app possono collegare l'azienda a servizi esterni per aumentare la produttività automatizzando i processi. Ad esempio, puoi connetterti alle tue banche e importare automaticamente le transazioni bancarie. Le app sono facili da installare e configurare direttamente da questa pagina. Scegli un'app per saperne di più su funzionalità e prezzi.  

Visualizza l'elenco delle app suggerite scegliendo l'azione **App di connettività** nella pagina **Gestione estensioni**.  

> [!NOTE]
> La prima persona che apre la pagina **App di connettività** deve consentire all'estensione di connettersi a un servizio esterno. Consenti la connessione una volta o sempre. Se scegli di bloccare la connessione, devi trovare le app pertinenti su AppSource.

Questo servizio esterno genererà un elenco di app pertinenti in base al tuo paese o area geografica

## <a name="recommended-apps"></a><a name="recommended-apps"></a><a name="recommended-apps"></a>App raccomandate

I partner e i rivenditori Microsoft possono creare un'app che possono utilizzare per compilare elenchi di applicazioni che spesso raccomandano ai loro clienti. Se lo fanno, e hanno distribuito l'app al tuo tenant, le app saranno disponibili nella pagina **App consigliate** . Lì puoi leggere di ogni app e decidere se installarla.

> [!NOTE]
> Se sei un partner o un rivenditore Microsoft e sei interessato a fornire un elenco di applicazioni raccomandate, vedi [Raccomandare le applicazioni da AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) nel contenuto di amministrazione.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/customize-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Installare e disinstallare app](ui-extensions-install-uninstall.md)  
[Personalizzare Business Central](ui-customizing-overview.md)  
[App per Business Central fornite da altri provider](ui-extensions-other.md)  
[Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Abilitare i pagamenti clienti tramite i servizi di pagamento](sales-how-enable-payment-service-extensions.md)  
[Migrare i dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostare l'estensione dei codici postali GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[App per [!INCLUDE[prod_short](includes/prod_short.md)] fornite da altri provider](ui-extensions-other.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
