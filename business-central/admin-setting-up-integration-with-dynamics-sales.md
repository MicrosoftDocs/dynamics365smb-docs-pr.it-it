---
title: Impostazione di account utente per l'integrazione con Microsoft Dataverse | Microsoft Docs
description: Ottenere informazioni su come impostare account utente che le app utilizzano per scambiare dati e che le persone utilizzano per accedere ai dati nelle app e per sincronizzarli.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Impostazione di account utente per l'integrazione con Microsoft Dataverse

In questo articolo viene fornita una panoramica su come impostare account utente necessari per integrare [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)].

## Impostare l'account utente amministratore

Per configurare la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)], è necessario accedere a [!INCLUDE[prod_short](includes/prod_short.md)] con un account utente assegnato alla licenza [!INCLUDE[prod_short](includes/prod_short.md)] Essential o [!INCLUDE[prod_short](includes/prod_short.md)] Premium. Utilizzeremo questo account una volta per installare e configurare alcuni componenti richiesti.

> [!IMPORTANT]
> Durante l'installazione, ti verrà chiesto di fornire le credenziali per l'ambiente [!INCLUDE[prod_short](includes/cds_long_md.md)]. Fornisci le credenziali di un account che è un utente con licenza a cui è assegnato il ruolo di sicurezza di **Amministratore di sistema** nell'ambiente [!INCLUDE[prod_short](includes/cds_long_md.md)] e amministratore globale nel tenant a cui appartiene l'ambiente. Questo account non ha bisogno di una licenza per [!INCLUDE[prod_short](includes/prod_short.md)], in quanto verrà utilizzato solo per eseguire attività di configurazione nell'ambiente [!INCLUDE[prod_short](includes/cds_long_md.md)].
>
> Al termine della configurazione della connessione, questo utente [!INCLUDE[prod_short](includes/cds_long_md.md)] può essere rimosso. L'integrazione continuerà a utilizzare l'account utente automaticamente creato specificatamente per l'integrazione.

## Autorizzazioni e ruoli di sicurezza per gli account utente in [!INCLUDE[prod_short](includes/cds_long_md.md)]

La soluzione di integrazione di base crea i seguenti ruoli in [!INCLUDE[cds_long](includes/cds_long_md.md)] per l'integrazione:

* **Amministratore di integrazione**: Consente agli utenti di gestire la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[cds_long](includes/cds_long_md.md)]. Assegnato in genere solo all'account utente automaticamente creato per la sincronizzazione.
* **Utente di integrazione**: Consente agli utenti di accedere ai dati sincronizzati. Assegnato in genere all'account utente automaticamente creato per la sincronizzazione e altri utenti che devono visualizzare o accedere ai dati sincronizzati.

> [!NOTE]
>
> I ruoli **Amministratore di integrazione** e **Utente di integrazione** devono essere utilizzati solo dall'utente dell'applicazione che esegue l'integrazione. L'utente dell'applicazione non ha bisogno della licenza [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[cds_long](includes/cds_long_md.md)] assegnata.

Quando installi la soluzione di integrazione di base, vengono configurate le autorizzazioni per l'account utente di integrazione. Se tali autorizzazioni vengono modificate manualmente, è possibile ripristinarle. Scegli **Ridistribuzione soluzione di integrazione** nella pagina **Setup connessione a Dataverse** per reinstallare la soluzione di integrazione di base. Questo passaggio distribuisce il ruolo di sicurezza Integrazione Business Central.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## Vedere anche

[Integrazione con Microsoft Dataverse](admin-common-data-service.md)  
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
