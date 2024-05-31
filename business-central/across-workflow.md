---
title: Workflow in Dynamics 365 Business Central
description: Usa le funzionalità di flusso di lavoro integrate per impostare flussi di lavoro di approvazione per integrare i flussi di lavoro automatizzati basati su Power Automate. È possibile impostare passaggi per assegnare attività a persone diverse nell'ambito delle diverse attività dei processi aziendali.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflow in Dynamics 365 Business Central

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. Le attività di sistema, come la pubblicazione automatica, possono essere incluse come passaggi in flussi di lavoro. Le attività di sistema possono essere precedute o seguite da attività utente. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.

La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] supporta questi tipi di workflow:
  
* Flussi di Power Automate

  * I flussi automatizzati che sono attivati da eventi quali la creazione, la modifica o l'eliminazione di record o documenti in [!INCLUDE[prod_short](includes/prod_short.md)]. Sono inclusi anche i flussi di approvazione creati in Power Automate che si attivano quando viene richiesta un'approvazione in [!INCLUDE[prod_short](includes/prod_short.md)].
  * Flussi istantanei che vengono attivati manualmente dal menu dell'azione **Automatizza** in elenchi, schede e pagine di documenti.

    Creare e attivare manualmente un flusso di Power Automate su un record [!INCLUDE[prod_short](includes/prod_short.md)], come un cliente, un articolo o un ordine di vendita, con opzioni per manipolare le informazioni sia internamente che esternamente (utilizzando strumenti integrati).

* Flussi di lavoro di approvazione basati su modelli di flusso di lavoro integrati

  Nella pagina **Modelli di flusso di lavoro**, puoi vedere tutti i flussi di lavoro disponibili. La versione di valutazione di [!INCLUDE[prod_short](includes/prod_short.md)] include molti workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per crearne di nuovi. Quando apri un modello dalla pagina **Modelli di flusso di lavoro** e il nome del flusso di lavoro inizia con *MS-*, il modello viene aggiunto da Microsoft.

## <a name="power-automate-flows"></a>Flussi di Power Automate

Con [!INCLUDE [prod_short](includes/prod_short.md)] online, puoi iscriverti a Power Automate per creare potenti flussi di lavoro automatizzati. Esegui quei flussi di lavoro da dentro [!INCLUDE [prod_short](includes/prod_short.md)]. I flussi possono connettere origini dati interne ed esterne e strumenti, senza conoscenze di codifica.

|**Task** |**Vedere**|
|-------|-------|
|Introduzione a Power Automate, alla creazione di flussi e all'esecuzione di flussi istantanei|[Utilizzare i flussi Power Automate in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Scopri i dettagli su come creare, modificare e gestire i flussi|[Imposta flussi automatizzati](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) e [Imposta flussi istantanei](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Imposta l'integrazione di Power Automate con [!INCLUDE[prod_short](includes/prod_short.md)] per gli utenti in qualità di amministratore|[Configurare l'integrazione di Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## <a name="approval-workflows"></a>Workflow di approvazione

Crea un workflow di approvazione definendo cosa avvia il workflow e cosa accade dopo, come segue:

* Un evento del workflow, moderato dalle condizioni dell'evento.
* Una risposta del flusso di lavoro, moderata dalle opzioni di risposta.

Per definire i passaggi del workflow compila i campi delle righe del workflow in base a valori di evento e di risposta che rappresentano gli scenari supportati.

Esempi di eventi di workflow di approvazione includono la creazione di ordini/preventivi/fatture di vendita o acquisto, modifiche dei prezzi e modifiche del fornitore o del cliente.

[!INCLUDE[workflow](includes/workflow.md)]

| **Per** | **Vedere** |
|--|--|
| Imposta gli utenti del workflow di approvazione, specifica la modalità di notifica per gli utenti e crea nuovi flussi di lavoro. Per creare i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione. | [Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md) |
| Abilita i workflow di approvazione, intervieni sulle relative notifiche, incluse le richieste e le approvazioni di una fase del workflow. Archiviare ed eliminare i flussi di lavoro. | [Usare workflow di approvazione](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione di progetti](projects-manage-projects.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Risolvere i problemi dei flussi di lavoro automatizzati di [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
