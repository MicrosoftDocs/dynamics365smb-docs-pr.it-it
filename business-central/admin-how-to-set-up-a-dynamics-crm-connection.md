---
title: Connettersi a Dynamics 365 Sales | Microsoft Docs
description: È possibile integrare altre app con Business Central tramite Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196641"
---
# <a name="connect-to-common-data-service"></a>Connettersi a Common Data Service
Questo argomento descrive come impostare una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)]. In genere, le aziende creano la connessione per integrare e sincronizzare i dati con un'altra app aziendale di Dynamics 365, ad esempio [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Operazioni preliminari
Prima di creare la connessione, è necessario disporre di alcune informazioni:  

* L'URL per l'ambiente [!INCLUDE[d365fin](includes/cds_long_md.md)] a cui vuoi connetterti. Se si utilizza la guida di setup assistito **Setup connessione a CDS** per creare la connessione individueremo i tuoi ambienti, ma puoi anche inserire l'URL di un altro ambiente nel tuo tenant.  
* Un nome utente e la password di un account utente utilizzato solo per l'integrazione. Questo account viene definito account "utente integrazione". 
* Il nome utente e la password di un account che dispone di autorizzazioni di amministratore in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Tali passaggi descrivono la procedura per la versione online di [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Impostare una connessione a [!INCLUDE[d365fin](includes/cds_long_md.md)].  
Per tutti i tipi di autenticazione diversi dall'autenticazione di Office 365, si imposta la connessione a [!INCLUDE[d365fin](includes/cds_long_md.md)] nella pagina **Setup connessione a CDS**. Per l'autenticazione di Office 365, è consigliabile utilizzare la guida del setup assistito **Setup connessione a CDS**. La guida rende più semplice configurare la connessione e specificare le funzionalità avanzate, ad esempio l'associazione tra record.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Per utilizzare la guida del setup assistito Setup connessione a CDS 
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup assistito** e quindi scegliere il collegamento correlato.
2. Scegli **Imposta connessione di integrazione di base CDS** per avviare la guida al setup assistito.
3. Compilare i campi in base alle esigenze.

> [!Note]
> La guida del setup assistito **Setup connessione a CDS** assegna automaticamente i ruoli di sicurezza **Amministratore integrazione** e **Utente integrazione** all'account utente utilizzato per l'integrazione e imposta la modalità di accesso per l'account su **non interattiva**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Per creare o gestire la connessione manualmente
La procedura seguente illustra come configurare la connessione manualmente nella pagina **Setup connessione a CDS**. Questa è anche la pagina in cui si gestiscono le impostazioni per l'integrazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione a CDS** e quindi scegliere il collegamento correlato.
2. Immettere le seguenti informazioni per la connessione da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Campo|Descrizione|
|-----|-----|
|**URL ambiente**|Se sei proprietario di ambienti in [!INCLUDE[d365fin](includes/cds_long_md.md)], li troveremo per te quando esegui la guida al setup. Se desideri connetterti a un altro ambiente in un altro tenant, puoi immettere le credenziali di amministratore per l'ambiente e verranno individuate. |
|**Nome utente** e **Password**|Le credenziali dell'account utente dedicato per l'integrazione. Per ulteriori informazioni, vedere [Impostazione di account utente per l'integrazione con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Abilitato**|Iniziare a utilizzare l'integrazione. Se non si abilita la connessione subito, le impostazioni di connessione verranno salvate, ma gli utenti non potranno accedere ai dati di [!INCLUDE[d365fin](includes/cds_long_md.md)] da [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile tornare a questa pagina e abilitare la connessione in un secondo momento.  |

3. Nel campo **Modello proprietà**, scegli se vuoi che un'entità team in [!INCLUDE[d365fin](includes/cds_long_md.md)] sia proprietaria di nuovi record o uno o più utenti specifici. Se scegli **Persona**, devi specificare ciascun utente. Se scegli **Team**, la Business Unit predefinita BCI_Company verrà visualizzata nel campo **Business Unit associata**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Per verificare le impostazioni di connessione, scegli **Connessione**, quindi **Test connessione**.  

    > [!NOTE]  
    >  Se la crittografia dei dati non è abilitata in [!INCLUDE[d365fin](includes/d365fin_md.md)], verrà richiesto se si desidera abilitarla. Per abilitare la crittografia dei dati, scegliere **Sì** e immettere le informazioni necessarie. In caso contrario, scegliere **No**. È possibile abilitare la crittografia dei dati in un secondo momento. Per ulteriori informazioni, vedere [Crittografia di dati in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) nella Guida per sviluppatori e professionisti IT.  

5. Se la sincronizzazione di [!INCLUDE[d365fin](includes/cds_long_md.md)] non è ancora impostata, verrà richiesto se si desidera utilizzare l'impostazione di sincronizzazione predefinita. A seconda se si desidera conservare o meno i record allineati in [!INCLUDE[d365fin](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)]  scegliere **Sì** o **No**.

> [!Note]
> La connessione a [!INCLUDE[d365fin](includes/cds_long_md.md)] mediante la pagina **Setup connessione a CDS** può richiedere l'assegnazione dei ruoli di sicurezza Amministratore di integrazione e Utente integrazione all'account utente utilizzato per l'integrazione in Dynamics 365 Sales. Per ulteriori informazioni, vedere [Assegnare un ruolo di sicurezza a un utente](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Per disconnettersi da [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione a CDS** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup connessione a CDS**, disattiva l'opzione **Abilitato**.  

## <a name="see-also"></a>Vedere anche  
[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  
