---
title: Connessione a Microsoft Dataverse | Microsoft Docs
description: È possibile integrare altre app con Business Central tramite Microsoft Dataverse.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/20/2020
ms.author: bholtorf
ms.openlocfilehash: 47a042f1825eca548ecbf08c6901e5af26cbeb43
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573403"
---
# <a name="connect-to-microsoft-dataverse"></a>Connettersi a Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Questo argomento descrive come impostare una connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. In genere, le aziende creano la connessione per integrare e sincronizzare i dati con un'altra app aziendale di Dynamics 365, ad esempio [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Operazioni preliminari

Prima di creare la connessione, è necessario disporre di alcune informazioni:  

* L'URL per l'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a cui vuoi connetterti. Se si utilizza la guida al setup assistito **Setup connessione a Dataverse** per creare la connessione individueremo i tuoi ambienti, ma puoi anche inserire l'URL di un altro ambiente nel tuo tenant.  
* Il nome utente e la password di un account che dispone di autorizzazioni di amministratore in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Se disponi del primo ciclo di rilascio del 2020 di [!INCLUDE[prod_short](includes/prod_short.md)] locale, versione 16.5, leggi l'articolo [Alcuni problemi noti](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Dovrai completare la soluzione alternativa descritta prima di poter creare la connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

> [!IMPORTANT]
> L'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non deve essere in modalità di amministrazione. La modalità di amministrazione causerà la mancata connessione perché l'account utente di integrazione per la connessione non dispone delle autorizzazioni di amministratore. Per ulteriori informazioni, vedere [Modalità di amministrazione](/power-platform/admin/admin-mode).

> [!Note]
> Tali passaggi descrivono la procedura per [!INCLUDE[prod_short](includes/prod_short.md)] online.
> Se stai utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] locale e non si sta utilizzando l'account Azure Active Directory per connettersi a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], devi inoltre specificare un nome utente e una password di un account utente per l'integrazione. Questo account viene definito account "utente integrazione". Se si sta usando un account Azure Active Directory l'account utente di integrazione non è richiesto o visualizzato. L'utente dell'integrazione verrà impostato automaticamente e non richiede una licenza.

## <a name="set-up-a-connection-to-cds_long_md"></a>Impostare una connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

Per tutti i tipi di autenticazione diversi dall'autenticazione di Microsoft 365, si imposta la connessione su [!INCLUDE[cds_long_md](includes/cds_long_md.md)] nella pagina **Setup connessione a Dataverse**. Per l'autenticazione di Microsoft 365, è consigliabile utilizzare la guida al setup assistito **Setup connessione a Dataverse**. La guida rende più semplice configurare la connessione e specificare le funzionalità avanzate, ad esempio il modello di proprietà e la sincronizzazione iniziale.  

> [!IMPORTANT]
> Durante il setup della connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], all'amministratore verrà chiesto di concedere le autorizzazioni seguenti per un'applicazione Azure registrata denominata [!INCLUDE[prod_short](includes/prod_short.md)] Integration a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * L'autorizzazione di **accesso a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] come utente corrente** è necessaria affinché [!INCLUDE[prod_short](includes/prod_short.md)] possa, per conto dell'amministratore, creare automaticamente un utente dell'applicazione di integrazione [!INCLUDE[prod_short](includes/prod_short.md)] senza licenza e non interattivo, assegnare ruoli di sicurezza a tale utente e distribuire la soluzione di integrazione [!INCLUDE[prod_short](includes/prod_short.md)] in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Questa autorizzazione viene utilizzata una sola volta durante il setup della connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * L'autorizzazione **Accesso completo a Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** è necessaria in modo che l'utente dell'applicazione [!INCLUDE[prod_short](includes/prod_short.md)] Integration creato automaticamente possa accedere ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] che verranno sincronizzati.  
> * L'autorizzazione **Accedi e leggi il profilo** è necessaria per verificare che l'accesso dell'utente abbia effettivamente assegnato il ruolo di sicurezza Amministratore di sistema in [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Fornendo il consenso per conto dell'organizzazione, l'amministratore autorizza l'applicazione Azure registrata chiamata [!INCLUDE[prod_short](includes/prod_short.md)] Integration per [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a sincronizzare i dati usando le credenziali dell'utente dell'applicazione [!INCLUDE[prod_short](includes/prod_short.md)] Integration creato automaticamente.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Utilizzare la guida al setup assistito Setup connessione a Dataverse
La guida Setup connessione a Dataverse può semplificare la connessione delle applicazioni e può persino aiutarti a eseguire una sincronizzazione iniziale. Se scegli di eseguire la sincronizzazione iniziale, [!INCLUDE[prod_short](includes/prod_short.md)] esaminerà i dati in entrambe le applicazioni e fornirà suggerimenti sulla sincronizzazione iniziale. Nella seguente tabella vengono illustrati i suggerimenti.

|Suggerimento  |Descrizione  |
|---------|---------|
|**Sincronizzazione completa**|I dati esistono solo in [!INCLUDE[prod_short](includes/prod_short.md)] o solo in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Il suggerimento è di sincronizzare tutti i dati dal servizio in cui si trovano all'altro servizio.|
|**Nessuna sincronizzazione**|I dati esistono in entrambe le applicazioni e l'esecuzione della sincronizzazione completa duplicherebbe i dati. Il suggerimento è di associare i record.|
|**Dipendenza non soddisfatta**|I dati esistono in entrambe le applicazioni, ma la riga o la tabella non possono essere sincronizzate perché dipende da una riga o da una tabella con il suggerimento Nessuna sincronizzazione. Ad esempio, se i clienti non possono essere sincronizzati, non è possibile sincronizzare neanche i dati per i contatti che dipendono dai dati del cliente.|

> [!IMPORTANT]
> In genere, utilizzi la sincronizzazione completa solo quando si integrano le applicazioni per la prima volta e solo un'applicazione contiene dati. La sincronizzazione completa può essere utile in un ambiente dimostrativo perché crea e associa automaticamente i record in ciascuna applicazione, il che rende più veloce iniziare a lavorare con i dati sincronizzati. Tuttavia, devi eseguire la sincronizzazione completa solo se desideri una riga in [!INCLUDE[prod_short](includes/prod_short.md)] per ogni riga in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] per i mapping di tabella. In caso contrario, il risultato può essere record duplicati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup assistito** e quindi scegliere il collegamento correlato.
2. Scegliere **Impostare una connessione a Microsoft Dataverse** per avviare la guida al setup assistito.
3. Compilare i campi in base alle esigenze.

> [!NOTE]
> Se non viene richiesto di accedere con il proprio account amministratore, è probabile che i popup siano bloccati. Per accedere, consentire i popup da `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Per creare o gestire la connessione manualmente

La procedura seguente illustra come configurare la connessione manualmente nella pagina **Setup connessione a Dataverse**. Questa è anche la pagina in cui si gestiscono le impostazioni per l'integrazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione Dataverse** e quindi scegliere il collegamento correlato.
2. Immettere le seguenti informazioni per la connessione da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Campo|Descrizione|
    |-----|-----|
    |**URL ambiente**|Se sei proprietario di ambienti in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], li troveremo per te quando esegui la guida al setup. Se desideri connetterti a un altro ambiente in un altro tenant, puoi immettere le credenziali di amministratore per l'ambiente e verranno individuate. |
    |**Abilitato**|Iniziare a utilizzare l'integrazione. Se non si abilita la connessione subito, le impostazioni di connessione verranno salvate, ma gli utenti non potranno accedere ai dati di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] da [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile tornare a questa pagina e abilitare la connessione in un secondo momento.  |

3. Nel campo **Modello proprietà**, scegli se vuoi che una tabella team in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sia proprietaria di nuovi record o uno o più utenti specifici. Se scegli **Persona**, devi specificare ciascun utente. Se scegli **Team**, la Business Unit predefinita verrà visualizzata nel campo **Business Unit associata**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

   <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|

4. Per verificare le impostazioni di connessione, scegli **Connessione**, quindi **Test connessione**.  

    > [!NOTE]  
    > Se la crittografia dei dati non è abilitata in [!INCLUDE[prod_short](includes/prod_short.md)], verrà richiesto se si desidera abilitarla. Per abilitare la crittografia dei dati, scegliere **Sì** e immettere le informazioni necessarie. In caso contrario, scegliere **No**. È possibile abilitare la crittografia dei dati in un secondo momento. Per ulteriori informazioni, vedere [Crittografia di dati in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) nella Guida per sviluppatori e amministratori.  

5. Se la sincronizzazione di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non è ancora impostata, verrà richiesto se si desidera utilizzare l'impostazione di sincronizzazione predefinita. A seconda se si desidera conservare o meno i record allineati in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)]  scegliere **Sì** o **No**.
<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="connecting-on-premises-versions"></a>Connessione alle versioni locali

Per connettere [!INCLUDE[prod_short](includes/prod_short.md)] on-premises a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], è necessario specificare alcune informazioni nella pagina **Setup connessione a Dataverse**.

Se si desidera connettersi utilizzando un account Azure Active Directory (Azure AD), è necessario registrare un'applicazione in Azure AD e fornire l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento da utilizzare. L'URL di reindirizzamento è precompilato e dovrebbe funzionare per la maggior parte delle installazioni. È necessario configurare l'installazione per utilizzare HTTPS. Per ulteriori informazioni, vedere [Configurazione di SSL per proteggere la connessione client Web di Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Se si sta configurando il server in modo da avere una home page diversa, è sempre possibile cambiare l'URL. Il segreto del client verrà salvato come stringa crittografata nel database.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Per registrare un'applicazione in Azure AD per la connessione da Business Central a Dataverse

I seguenti passaggi presuppongono che si stia utilizzando Azure AD per gestire identità e accesso. Per ulteriori informazioni sulla registrazione di un'applicazione in Azure AD vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). Se non si utilizza Azure AD vedere [Utilizzo di un altro servizio di gestione dell'identità e degli accessi](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Nel portale di Azure, in **Gestisci** nel riquadro di navigazione, selezionare **Autenticazione**.  
2. In **URL di reindirizzamento**, aggiungere l'URL di reindirizzamento suggerito nella pagina **Setup connessione a Dataverse** in [!INCLUDE[prod_short](includes/prod_short.md)].
3. In **Gestisci**, scegliere **Autorizzazioni API**.
4. In **Autorizzazioni configurate**, scegliere **Aggiungi un'autorizzazione** e quindi aggiungere le autorizzazioni delegate nella scheda **API Microsoft** come segue:
    * Per Business Central, aggiungere le autorizzazioni **Financials.ReadWrite.All**.
    * Per Dynamics CRM, aggiungere le autorizzazioni **user_impersonation**.  

    > [!NOTE]
    > Il nome dell'API Dynamics CRM potrebbe cambiare.

5. In **Gestisci**, scegliere **Certificati e segreti**, quindi creare un nuovo segreto per l'app. Il segreto viene utilizzato in [!INCLUDE[prod_short](includes/prod_short.md)], nel campo **Segreto client** della pagina **Setup connessione a Dataverse** o archiviato in un archivio sicuro e fornito in una sottoscrizione di eventi come descritto in precedenza in questo argomento.
6. Scegliere **Panoramica**, quindi trovare il valore **ID applicazione (client)**. Questo è l'ID client dell'applicazione. È necessario inserirlo nella pagina **Setup connessione a Dataverse** nel campo **ID client** o archiviarlo in un archivio sicuro e fornirlo in una sottoscrizione di eventi.
7. In [!INCLUDE[prod_short](includes/prod_short.md)], nella pagina **Setup connessione a Dataverse** nel campo **URL ambiente** inserire l'URL per l'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
8. Per abilitare la connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], attivare l'interruttore **Abilitato**.
9. Accedere con l'account amministratore per Azure Active Directory (questo account deve avere una licenza valida per [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ed essere un amministratore nell'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Dopo aver effettuato l'accesso, verrà richiesto di consentire all'applicazione registrata l'accesso a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] per conto dell'organizzazione. È necessario fornire il consenso per completare il setup.

   > [!NOTE]
   > Se non viene richiesto di accedere con il proprio account amministratore, è probabile che i popup siano bloccati. Per accedere, consentire i popup da `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Utilizzo di un altro servizio di gestione dell'identità e degli accessi

Se non si sta usando Azure Active Directory per gestire le identità e l'accesso, è necessario l'aiuto di uno sviluppatore. Se si preferisce archiviare l'ID app e il segreto in una posizione diversa, è possibile lasciare vuoti i campi ID client e Segreto client e scrivere un'estensione per recuperare l'ID e il segreto dalla posizione. È possibile fornire il segreto in fase di esecuzione sottoscrivendo gli eventi OnGetCDSConnectionClientId e OnGetCDSConnectionClientSecret nella codeunit 7201 "Implementazione dell'integrazione di CDS"

### <a name="to-disconnect-from-cds_long_md"></a>Per disconnettersi da [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione Dataverse** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup connessione a Dataverse**, disattiva l'opzione **Abilitato**.  

## <a name="see-also"></a>Vedere anche

[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]