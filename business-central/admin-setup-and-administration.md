---
title: Attività di amministrazione in Business Central
description: 'Alcuni task in Business Central richiedono un setup e un''amministrazione centrale. In questa sezione, viene fornita una descrizione di tali task e informazioni su come utilizzarli.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# <a name="administration-tasks"></a>Attività di amministrazione

I task di amministrazione centrale vengono generalmente eseguiti da un solo ruolo nella società. L'ambito di tali task può dipendere dalle dimensioni dell'azienda e dalle responsabilità previste dalla mansione dell'amministratore. Questi task possono includere la gestione della sincronizzazione con il database di code di processi ed e-mail, l'impostazione di utenti e la personalizzazione dell'interfaccia utente.  

Per la riuscita di qualsiasi nuovo software aziendale, è importante immettere i valori di setup appropriati dall'inizio. [!INCLUDE[prod_short](includes/prod_short.md)] include varie guide di setup per la configurazione dei dati principali. Per ulteriori informazioni, vedere [Impostazione di Business Central](setup.md).

> [!NOTE]
> È possibile utilizzare gli strumenti di migrazione dei dati per eseguire la migrazione dei dati esistenti [!INCLUDE [prod_short](includes/prod_short.md)] online In alternativa, puoi impostare una nuova società in [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando i pacchetti di configurazione, uno strumento progettato per accelerare i tempi di distribuzione, migliorare la qualità dell'implementazione, introdurre un approccio ripetibile alle implementazioni e migliorare la produttività mediante l'automazione e la semplificazione di task ricorrenti. Per ulteriori informazioni, vedi [Migrazione dei dati locali in Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Puoi supportare le decisioni di setup con alcuni consigli generali per i campi di configurazione selezionati che potrebbero provocare la mancata efficacia della soluzione se definiti in modo errato.  

Un utente o amministratore avanzato può impostare il framework di scambio di dati per consentire agli utenti di esportare e importare i dati nei file bancari e di ruolo paga, ad esempio per i diversi processi di gestione bancaria. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.  

|**Per**|**Vedere**|  
|------------|-------------|
|Definire chi può accedere a [!INCLUDE[prod_short](includes/prod_short.md)] creando utenti nell'interfaccia di amministrazione di Microsoft 365 in base alle licenze del prodotto.|[Creare utenti in base alle licenze](ui-how-users-permissions.md)|
|Assegnare le autorizzazioni agli utenti, modificare i set di autorizzazioni e raggruppare gli utenti per una gestione semplificata delle autorizzazioni.|[Assegnare autorizzazioni a utenti e gruppi](ui-how-users-permissions.md)|
|Aggiungere utenti, gestire i permessi e l'accesso ai dati, assegnare ruoli.|[Gestire profili](admin-users-profiles-roles.md)|
|Gestire le impostazioni dell'utente, come azienda, ruolo, lingua, area geografica e fuso orario.|[Impostazioni utente](admin-manage-user-settings-preferences.md)|
|Configurare le stampanti e specificare quali report stampare su quali stampanti.|[Configurare le stampanti](ui-specify-printer-selection-reports.md)|
|Classificare i dati riservati per campi in modo da rispondere alle richieste da oggetti dati correlate ai relativi dati personali.|[Classificare i dati riservati](admin-classifying-data-sensitivity.md)|
|Rispondere a richieste da oggetti dati riguardanti i relativi dati personali.|[Rispondere a richieste relative a dati personali](admin-responding-to-requests-about-personal-data.md)|
|Impostare una nuova business unit utilizzando modelli|[Creare nuove società](about-new-company.md)|
|Tenere traccia di tutte le modifiche dirette apportate dagli utenti ai dati nel database per identificare l'origine di eventuali errori e delle modifiche ai dati.|[Registrazione di modifiche](across-log-changes.md)|  
|Immettere richieste singole o ricorrenti per eseguire report o codeunit.|[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)|  
|Gestire, eliminare o comprimere documenti|[Eliminare documenti](admin-manage-documents.md)|  
|Esporre le pagine, le codeunit e le query come servizi Web.|[Pubblicare un servizio Web](across-how-publish-web-service.md)|
|Come parte della creazione di app Connect tra [!INCLUDE[prod_short](includes/prod_short.md)] e soluzioni di terze parti tramite API REST, definire modelli che vengono utilizzati per popolare proprietà vuote in un'entità quando si crea un'azione POST attraverso un'API.|[Configurare i modelli di API](admin-configuring-api-template.md)|
|Crittografare i dati in [!INCLUDE[prod_short](includes/prod_short.md)] Server generando nuove chiavi di crittografia o importando quelle esistenti che vengono abilitate nel server.|[Gestire crittografia dati](admin-manage-data-encryption.md)|
|Connettere Dynamics 365 Sales a [!INCLUDE[prod_short](includes/prod_short.md)] per ottenere un'integrazione ottimale tra le relazioni con il cliente e l'elaborazione degli ordini nel processo dai lead agli incassi.|[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Modificare i campi e le azioni visualizzati nell'interfaccia utente per adattarli ai processi aziendali della società e estendere la soluzione con le app.|[Personalizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Amministrazione nell'interfaccia di amministrazione

Gli amministratori interni e delegati hanno accesso all'interfaccia di amministrazione [!INCLUDE [prod_short](includes/prod_short.md)] da cui possono configurare, monitorare e risolvere i problemi degli ambienti [!INCLUDE [prod_short](includes/prod_short.md)]. Nella tabella seguente sono descritte alcune delle attività principali, con collegamenti agli articoli che li descrivono.  

|**Per**|**Vedere**|  
|------------|-------------|
|Informazioni sugli strumenti disponibili per la risoluzione dei problemi.|[Supporto tecnico](/dynamics365/business-central/dev-itpro/technical-support)|
|Monitorare l'utilizzo e risolvere i problemi delle sessioni|[Telemetria dell'ambiente nell'interfaccia di amministrazione di Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Gestire le sessioni utente, inclusa l'annullamento di una sessione se l'utente è bloccato.|[Gestire sessioni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Configurare il tenant per inviare i dati di telemetria ad Azure Application Insights per una migliore analisi e risoluzione dei problemi.|[Abilitare l'invio della telemetria ad Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Vedi anche

[Funzionalità aziendale](across-business-functionality.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
