---
title: Task amministrativi in Dynamics 365 | Microsoft Docs
description: Alcuni task in Dynamics 365 richiedono un setup e un'amministrazione centrale. In questa sezione, viene fornita una descrizione di tali task e informazioni su come utilizzarli.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: c7e5efe85dddcc7db84b05879f0c71990167c775
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a>Setup e amministrazione in Dynamics 365 for Financials
I task di amministrazione centrale vengono generalmente eseguiti da un solo ruolo nella società. L'ambito di tali task può dipendere dalle dimensioni dell'azienda e dalle responsabilità previste dalla mansione dell'amministratore. Questi task possono includere la gestione della sincronizzazione con il database di code di processi ed e-mail, l'impostazione di utenti, la personalizzazione dell'interfaccia utente e la gestione delle chiavi di crittografia.  

Per la riuscita di qualsiasi nuovo software aziendale, è importante immettere i valori di setup appropriati dall'inizio. [!INCLUDE[d365fin](includes/d365fin_md.md)] include varie guide di setup per la configurazione dei dati principali. Per altre informazioni, vedere [Impostazione di Dynamics 365 for Financials](setup.md).

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

Un utente o amministratore avanzato può impostare il framework di scambio di dati per consentire agli utenti di esportare e importare i dati nei file bancari e di ruolo paga, ad esempio per i diversi processi di gestione bancaria.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Aggiungere utenti, gestire i permessi e l'accesso ai dati, assegnare ruoli.|[Utenti, profili e Gestioni ruolo utente in Dynamics 365 for Financials](admin-users-profiles-roles.md)|  
|Tenere traccia di tutte le modifiche dirette apportate dagli utenti ai dati nel database per identificare l'origine di eventuali errori e delle modifiche ai dati.|[Registrazione di modifiche in Dynamics 365 for Financials](across-log-changes.md)|  
|Supportare le decisioni di setup con alcuni consigli per i campi selezionati che potrebbero provocare la mancata efficacia della soluzione se definiti in modo errato|[Impostare aree di applicazione complesse utilizzando le procedure ottimali](set-up-complex-application-areas-using-best-practices.md)|  
|Esporre le pagine, le codeunit e le query come servizi Web.|[Procedura: Pubblicare un servizio Web](across-how-publish-web-service.md)|  
|Impostare un server SMTP per consentire la comunicazione e-mail in entrata e in uscita da Dynamics 365 for Financials.| [Procedura: Impostare la posta elettronica manualmente o tramite il setup assistito](madeira-how-setup-email.md)|  
|Immettere richieste singole o ricorrenti per eseguire report o codeunit.|[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)|  
|Gestire, eliminare o comprimere documenti|[Gestire i documenti](admin-manage-documents.md)|  
|Impostare una nuova business unit utilizzando modelli|[Creazione di nuove società in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)|  

## <a name="see-also"></a>Vedi anche
[Funzionalità aziendale](madeira-business-functionality.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Benvenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

