---
title: Personalizzare Dynamics 365 Business Central | Documenti Microsoft
description: Sviluppare, mostrare e promuovere le proprie app ed estensioni per Business Central.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 04/12/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: a86d58c81bdee20ffd33273ca069d9fae640df96
ms.contentlocale: it-it
ms.lasthandoff: 04/16/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a>Estensione di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] è una soluzione di gestione aziendale che aiuta le aziende a connettere dati finanziari, dati di vendite, servizi e operazioni per snellire i processi aziendali, migliorare le interazioni con i clienti e prendere decisioni migliori. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] è disponibile nel cloud e per gli utenti su vari tipi di dispositivi, sempre aggiornato. Questa moderna piattaforma aziendale consente di personalizzare, ampliare e creare applicazioni in modo semplice e rapido per rispondere a esigenze specifiche, con sviluppo di codice minimo o praticamente nullo.  

L'utilizzo di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] come piattaforma per sviluppatori di app offre numerosi vantaggi, tra cui:

* Inizio in sicurezza grazie a un'esperienza di onboarding ottimizzata 
* Utilizzo dei servizi Go-To-Market di Microsoft
* Personalizzazzione della pagina di presentazione delle app 
* Connessione diretta con i responsabili delle decisioni e interazioni con più clienti
* Miglioramento del valore aziendale e aumento del volume delle operazioni commerciali con i clienti esistenti e nuovi
* Ottenere maggiori risultati con una piattaforma che una offre scalabilità ed esperienze moderne  
* Accesso a informazioni utili sulle prestazioni delle inserzioni tramite il portale dei partner cloud o il processo di pubblicazione delle app di Office
* Possibilità di offrire bundle con app aziendali intelligenti come PowerApps, Flow, Power BI, Cortana Intelligence e molte altre  

È possibile presentare i servizi [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] in Microsoft AppSource come: 

**Singole app**: per offrire sul mercato la propria esperienza del settore.  
**Pacchetti di servizi di consulenza**: per offrire sul mercato pacchetti di servizi predefiniti.

I nuovi strumenti di sviluppo consentono di creare estensioni per utenti di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. Se si desidera acquisire familiarità con i nuovi strumenti oppure ottenere informazioni sulle estensioni 2.0, vedere [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).  

Maggiori informazioni su quali app e servizi di consulenza sono attualmente disponibili su [Microsoft AppSource](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1).

Per aiutare gli utenti business a iniziare rapidamente, Microsoft ha aggiunto un catalogo di servizi di consulenza per soluzioni basate su [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], Power BI e PowerApps in AppSource. Ulteriori informazioni sui [Servizi di consulenza](/dynamics-nav/developer/readiness/readiness-consulting).

## <a name="choosing-which-services-to-offer-with-included365finlongincludesd365finlongmdmd"></a>Scelta dei servizi da offrire con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] 

### <a name="integrate-a-3rd-party-solution"></a>Integrare una soluzione di terze parti
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] espone molte API pronte all'uso per le [app Connect](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-connect-apps) per un'integrazione perfetta tra il servizio e [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. È possibile creare un pacchetto di servizi con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] e offrire ai clienti un'esperienza completa. Ulteriori informazioni sull'[integrazione di una soluzione di terze parti](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-thirdparty-solution).

### <a name="development-of-a-vertical-solution"></a>Sviluppo di una soluzione verticale
È possibile creare un'app specializzata per un settore specifico. Con l'app [Incorpora](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-embed-apps), si può estendere e personalizzare l'applicazione [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] esistente e migliorare l'esperienza dell'utente finale con una funzionalità specifica del settore utilizzando i nuovi e moderni strumenti di sviluppo e le estensioni della versione 2.0. Ulteriori informazioni sullo [sviluppo di una soluzione verticale](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-vertical).

### <a name="development-of-a-horizontal-solution"></a>Sviluppo di una soluzione orizzontale
Si possono estendere l'esperienza e le capacità di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] creando un'[app aggiuntiva](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-add-on-apps) che si integra nell'esperienza utente di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. Creare un'interfaccia basata sull'aspetto che si desidera abbia il flusso di dati tra [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] e i propri servizi. Ulteriori informazioni sullo [sviluppo di una soluzione orizzontale](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-horizontal). 

### <a name="development-of-a-localization-solution"></a>Sviluppo di una soluzione di localizzazione
Si può garantire la conformità alle normative locali sviluppando app per [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] con aree funzionali adattate ai requisiti del mercato locale con il [servizio di traduzione di Dynamics 365](/dynamics365/unified-operations/dev-itpro/lifecycle-services/translation-service-overview). Allineare le funzionalità principali dei requisiti legislativi locali ed estendere le funzionalità esistenti per competere con successo nel mercato locale. Ulteriori informazioni sullo [sviluppo di una soluzione localizzata](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization).

### <a name="reseller-solution"></a>Soluzione per rivenditori
Poiché ogni azienda è unica, la [personalizzazione dei tenant](/dynamics-nav/developer/readiness/readiness-customizing-tenants) consente di abbinare il modo in cui si lavora con i processi ottimizzati, la terminologia e il modo in cui i dipendenti o i reparti si connettono e collaborano. Inoltre, è possibile scegliere di rivendere e adattare [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] alle singole esigenze dei propri clienti fornendo [servizi di consulenza](/dynamics-nav/developer/readiness/readiness-consulting). In alternativa, si può utilizzare Microsoft Flow, Power Apps e Power BI per creare [flussi personalizzati](/dynamics-nav/developer/readiness/readiness-no-code), oltre ad app e report con business insight senza dover scrivere alcun codice. Ulteriori informazioni sui [rivenditori di Dynamics 365 (VAR)](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-reseller). 

## <a name="where-do-i-learn-more"></a>Dove si trovano altre informazioni?
Per ulteriori informazioni sulle offerte di servizi di consulenza Microsoft AppSource, selezionare i seguenti collegamenti: 

[Offerte AppSource Consulting](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1)  
[Idoneità dei partner](https://smp-cdn-prod.azureedge.net/documents/Microsoft%20AppSource%20Partner%20Listing%20Guidelines.pdf)  
[Modulo di presentazione per i partner](https://appsource.microsoft.com/en-us/partners/list-consulting-service)  

## <a name="the-ready-to-go-program"></a>Programma Ready to Go
Il programma Ready to Go è progettato per supportare i partner nell'inserimento delle offerte per Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] in Microsoft Appsource. Il programma offre: 

- [Formazione online](http://aka.ms/ReadyToGoOnlineLearning)
- [Training e workshop](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go#the-ready-to-go-coaching)
- [Piattaforma di collaborazione Microsoft](http://aka.ms/Collaborate)

Per ulteriori informazioni su come sviluppare un'offerta [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], consultare i dettagli del [programma Ready to Go](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go). Per domande o feedback sul programma **Ready to Go**, [contattatare Microsoft](mailto:dyn365bep@microsoft.com). 

## <a name="see-also"></a>Vedi anche
[Introduzione](product-get-started.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

