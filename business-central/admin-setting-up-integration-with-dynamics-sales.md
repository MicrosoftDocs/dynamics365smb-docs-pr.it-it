---
title: Impostazione di account utente per l'integrazione con Common Data Service | Microsoft Docs
description: Ottenere informazioni su come impostare account utente che le app utilizzano per scambiare dati e che le persone utilizzano per accedere ai dati nelle app e per sincronizzarli.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ad10aa53b4fe6a8b9b65ad798c206fa251e08a7a
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196497"
---
# <a name="setting-up-user-accounts-for-integrating-with-common-data-service"></a>Impostazione di account utente per l'integrazione con Common Data Service
In questo articolo viene fornita una panoramica su come impostare account utente necessari per integrare [!INCLUDE[d365fin](includes/cds_long_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="setting-up-the-administrator-user-account"></a>Impostazione dell'account utente amministratore
Devi aggiungere il tuo account utente amministratore per [!INCLUDE[d365fin](includes/d365fin_md.md)] come utente in [!INCLUDE[d365fin](includes/cds_long_md.md)]. Quando si imposta la connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)] useremo questo account una volta per installare e configurare alcuni componenti richiesti. <!--Verify this-->

## <a name="setting-up-the-user-account-for-the-integration"></a>Impostazione dell'account utente per l'integrazione
È necessario creare un account utente dedicato nella sottoscrizione di Office 365 che [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)] possono utilizzare per sincronizzare i dati. Questo account utente deve essere in grado di accedere a [!INCLUDE[d365fin](includes/cds_long_md.md)], a indicare che tale utente deve avere una licenza per [!INCLUDE[d365fin](includes/cds_long_md.md)] e almeno un ruolo di sicurezza ad esso assegnato in [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--not sure that this applies as described [here](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). For more information about how to create users in [!INCLUDE[d365fin](includes/cds_long_md.md)], see [Manage security, users, and teams](https://go.microsoft.com/fwlink/?LinkID=616518). --> Dopo che la connessione è impostata, [!INCLUDE[d365fin](includes/d365fin_md.md)] assegnerà all'account utente i ruoli di sicurezza di cui necessita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--![Assisted setup guide showing place to enter synchronization user credentials](media/sync-user-setup.png "Visualization assisted setup wizard page showing place to enter synchronization user credentials")-->

> [!IMPORTANT]  
> Non utilizzare l'account amministratore per [!INCLUDE[d365fin](includes/cds_long_md.md)] per la sincronizzazione. In caso contrario, la sincronizzazione verrà interrotta.

## <a name="permissions-and-security-roles-for-user-accounts-in-d365fin"></a>Autorizzazioni e ruoli di sicurezza per gli account utente in [!INCLUDE[d365fin](includes/cds_long_md.md)]
Quando si installa la soluzione di integrazione CDS di base, le autorizzazioni per l'account utente di integrazione sono configurate. Se tali autorizzazioni vengono modificate, potrebbe essere necessario ripristinarle. Puoi farlo reinstallando la soluzione di integrazione CDS di base scegliendo **Ridistribuisci soluzione di integrazione** nella pagina **Configurazione connessione Common Data Service**. Viene distribuito il ruolo di sicurezza Integrazione CDS Business Central.


<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)].

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

#### Integration User
The following table displays the minimum permissions on each tab for each security role that is required for the integration user.

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

## <a name="see-also"></a>Vedere anche  
[Integrazione con Common Data Service](admin-common-data-service.md)  
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
