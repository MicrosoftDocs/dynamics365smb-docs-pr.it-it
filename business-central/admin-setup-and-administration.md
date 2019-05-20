---
title: Task amministrativi in Business Central | Documenti di Microsoft
description: Alcuni task in Business Central richiedono un setup e un'amministrazione centrale. In questa sezione, viene fornita una descrizione di tali task e informazioni su come utilizzarli.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: c5b76a434403da0d472b1e1fa9430d40ff082220
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247188"
---
# <a name="administration"></a>Setup
I task di amministrazione centrale vengono generalmente eseguiti da un solo ruolo nella società. L'ambito di tali task può dipendere dalle dimensioni dell'azienda e dalle responsabilità previste dalla mansione dell'amministratore. Questi task possono includere la gestione della sincronizzazione con il database di code di processi ed e-mail, l'impostazione di utenti e la personalizzazione dell'interfaccia utente.  

Per la riuscita di qualsiasi nuovo software aziendale, è importante immettere i valori di setup appropriati dall'inizio. [!INCLUDE[d365fin](includes/d365fin_md.md)] include varie guide di setup per la configurazione dei dati principali. Per ulteriori informazioni, vedere [Impostazione di Business Central](setup.md).

Se si utilizza RapidStart Services per implementare i valori di setup o questi vengono immessi manualmente nella nuova società, è possibile supportare le decisioni di setup con alcuni consigli generali per i campi di setup selezionati che potrebbero provocare la mancata efficacia della soluzione se definiti in modo errato.  

Un utente o amministratore avanzato può impostare il framework di scambio di dati per consentire agli utenti di esportare e importare i dati nei file bancari e di ruolo paga, ad esempio per i diversi processi di gestione bancaria.

> [!NOTE]
> È possibile impostare una nuova società in [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando RapidStart Services, uno strumento progettato per accelerare i tempi di distribuzione, migliorare la qualità dell'implementazione, introdurre un approccio ripetibile alle implementazioni e migliorare la produttività mediante l'automazione e la semplificazione di task ricorrenti. Per ulteriori informazioni, vedere [Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Aggiungere utenti, gestire i permessi e l'accesso ai dati, assegnare ruoli.|[Informazioni su profili e Gestioni ruolo utente](admin-users-profiles-roles.md)|  
|Assegnare le autorizzazioni agli utenti, modificare i set di autorizzazioni e raggruppare gli utenti per autorizzazioni.|[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)|
|Classificare i dati riservati per campi in modo da rispondere alle richieste da oggetti dati correlate ai relativi dati personali.|[Classificazione di dati riservati](admin-classifying-data-sensitivity.md)|
|Rispondere a richieste da oggetti dati riguardanti i relativi dati personali.|[Rispondere a richieste relative a dati personali](admin-responding-to-requests-about-personal-data.md)|
|Impostare una nuova business unit utilizzando modelli|[Creazione di nuove società](about-new-company.md)|
|Tenere traccia di tutte le modifiche dirette apportate dagli utenti ai dati nel database per identificare l'origine di eventuali errori e delle modifiche ai dati.|[Registrazione di modifiche](across-log-changes.md)|  
|Immettere richieste singole o ricorrenti per eseguire report o codeunit.|[Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md)|  
|Gestire, eliminare o comprimere documenti|[Eliminazione di documenti](admin-manage-documents.md)|  
|Esporre le pagine, le codeunit e le query come servizi Web.|[Pubblicazione di un servizio Web](across-how-publish-web-service.md)|
|Come parte della creazione di app Connect tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e soluzioni di terze parti tramite REST API, definire modelli che vengono utilizzati per popolare proprietà vuote in un'entità quando si crea un'azione POST attraverso un'API.|[Configurazione di modelli di API](admin-configuring-api-template.md)|
|Crittografare i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)] Server generando nuove chiavi di crittografia o importando quelle esistenti che vengono abilitate nel server.|[Gestione crittografia dati](admin-manage-data-encryption.md)|
|Connettere Dynamics 365 for Sales a [!INCLUDE[d365fin](includes/d365fin_md.md)] per ottenere un'integrazione ottimale tra le relazioni con il cliente e l'elaborazione degli ordini nel processo dai lead agli incassi.|[Integrazione con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Modificare i campi e le azioni visualizzati nell'interfaccia utente per adattarli ai processi aziendali della società e estendere la soluzione con le app.|[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)|

## <a name="see-also"></a>Vedi anche
[Funzionalità aziendale](across-business-functionality.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Introduzione](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  