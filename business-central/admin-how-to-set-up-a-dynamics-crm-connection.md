---
title: Connessione a Common Data Service | Microsoft Docs
description: È possibile integrare altre app con Business Central tramite Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/24/2020
ms.author: bholtorf
ms.openlocfilehash: 10a257b60aedfb22066148fd48145779cd6d4a62
ms.sourcegitcommit: ac492bff0c87bf2a23fa93113e7571da9d5094c7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "3701994"
---
# <a name="connect-to-common-data-service"></a>Connettersi a Common Data Service

Questo argomento descrive come impostare una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. In genere, le aziende creano la connessione per integrare e sincronizzare i dati con un'altra app aziendale di Dynamics 365, ad esempio [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Operazioni preliminari

Prima di creare la connessione, è necessario disporre di alcune informazioni:  

* L'URL per l'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a cui vuoi connetterti. Se si utilizza la guida di setup assistito **Setup connessione a CDS** per creare la connessione individueremo i tuoi ambienti, ma puoi anche inserire l'URL di un altro ambiente nel tuo tenant.  
* Il nome utente e la password di un account che dispone di autorizzazioni di amministratore in [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

> [!Note]
> Tali passaggi descrivono la procedura per la versione online di [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Se si sta utilizzando Business Central on-premises e non si sta utilizzando l'account Azure Active Directory per connettersi a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], è inoltre necessario specificare un nome utente e una password di un account utente per l'integrazione. Questo account viene definito account "utente integrazione". Se si sta usando un account Azure Active Directory l'account utente di integrazione non è richiesto o visualizzato. L'utente dell'integrazione verrà impostato automaticamente e non richiede una licenza.

## <a name="set-up-a-connection-to-cds_long_md"></a>Impostare una connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

Per tutti i tipi di autenticazione diversi dall'autenticazione di Office 365, si imposta la connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] nella pagina **Setup connessione a CDS**. Per l'autenticazione di Office 365, è consigliabile utilizzare la guida del setup assistito **Setup connessione a Common Data Service**. La guida rende più semplice configurare la connessione e specificare le funzionalità avanzate, ad esempio il modello di proprietà e la sincronizzazione iniziale.  

> [!IMPORTANT]
> Durante il setup della connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], all'amministratore verrà chiesto di concedere le autorizzazioni seguenti per l'applicazione Azure registrata denominata [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * L'autorizzazione **Accesso [!INCLUDE[cds_long_md](includes/cds_long_md.md)] come utente corrente** è necessaria in modo che [!INCLUDE[d365fin](includes/d365fin_md.md)] possa per conto dell'amministratore, creare automaticamente un utente dell'applicazione [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration senza licenza non interattivo, assegnare ruoli di sicurezza a questo utente e distribuire la soluzione di integrazione CDS di base [!INCLUDE[d365fin](includes/d365fin_md.md)] in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Questa autorizzazione viene utilizzata una sola volta durante il setup della connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * L'autorizzazione **Accesso completo a Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** è necessaria in modo che l'utente dell'applicazione [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration creato automaticamente possa accedere ai dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] che verranno sincronizzati.  
> * L'autorizzazione **Accedi e leggi il profilo** è necessaria per verificare che l'accesso dell'utente abbia effettivamente assegnato il ruolo di sicurezza Amministratore di sistema in [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Fornendo il consenso per conto dell'organizzazione, l'amministratore autorizza l'applicazione Azure registrata chiamata [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration per [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a sincronizzare i dati usando le credenziali dell'utente dell'applicazione [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration creato automaticamente.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Per utilizzare la guida al setup assistito Setup connessione a Common Data Service

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup assistito** e quindi scegliere il collegamento correlato.
2. Scegliere **Setup connessione a Common Data Service** per avviare la guida al setup assistito.
3. Compilare i campi in base alle esigenze.

### <a name="to-create-or-maintain-the-connection-manually"></a>Per creare o gestire la connessione manualmente

La procedura seguente illustra come configurare la connessione manualmente nella pagina **Setup connessione a CDS**. Questa è anche la pagina in cui si gestiscono le impostazioni per l'integrazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione a CDS** e quindi scegliere il collegamento correlato.
2. Immettere le seguenti informazioni per la connessione da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Campo|Descrizione|
    |-----|-----|
    |**URL ambiente**|Se sei proprietario di ambienti in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], li troveremo per te quando esegui la guida al setup. Se desideri connetterti a un altro ambiente in un altro tenant, puoi immettere le credenziali di amministratore per l'ambiente e verranno individuate. |
    |**Abilitato**|Iniziare a utilizzare l'integrazione. Se non si abilita la connessione subito, le impostazioni di connessione verranno salvate, ma gli utenti non potranno accedere ai dati di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] da [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile tornare a questa pagina e abilitare la connessione in un secondo momento.  |

3. Nel campo **Modello proprietà**, scegli se vuoi che un'entità team in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sia proprietaria di nuovi record o uno o più utenti specifici. Se scegli **Persona**, devi specificare ciascun utente. Se scegli **Team**, la Business Unit predefinita BCI_Company verrà visualizzata nel campo **Business Unit associata**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Immettere le impostazioni avanzate seguenti.

    |Campo|Descrizione|
    |-----|-----|
    |**Gli utenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] devono essere mappati a quelli di CDS**|Se si sta utilizzando il modello di proprietà Persona, specificare se gli account utente [!INCLUDE[d365fin](includes/d365fin_md.md)] devono avere un account utente corrispondente in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. L'**indirizzo e-mail di autenticazione di Office 365** dell'utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] deve essere uguale all'**indirizzo e-mail principale** dell'utente di [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Se si imposta il valore **Sì**, gli utenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] che non hanno un account utente corrispondente in [!INCLUDE[crm_md](includes/crm_md.md)] non disporranno della funzionalità di integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] nell'interfaccia utente. L'accesso ai dati di [!INCLUDE[crm_md](includes/crm_md.md)] direttamente da [!INCLUDE[d365fin](includes/d365fin_md.md)] viene eseguito per conto dell'account utente di [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Se si imposta il valore **No**, tutti gli utenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] disporranno della funzionalità di integrazione di [!INCLUDE[crm_md](includes/crm_md.md)] nell'interfaccia utente. L'accesso ai dati di [!INCLUDE[crm_md](includes/crm_md.md)] viene eseguito per conto dell'utente di connessione (integrazione) [!INCLUDE[crm_md](includes/crm_md.md)].|
    |**Agente di Business Central corrente mappato a un utente**|Indica se l'account utente utilizzato viene mappato a account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field-->|

4. Per verificare le impostazioni di connessione, scegli **Connessione**, quindi **Test connessione**.  

    > [!NOTE]  
    > Se la crittografia dei dati non è abilitata in [!INCLUDE[d365fin](includes/d365fin_md.md)], verrà richiesto se si desidera abilitarla. Per abilitare la crittografia dei dati, scegliere **Sì** e immettere le informazioni necessarie. In caso contrario, scegliere **No**. È possibile abilitare la crittografia dei dati in un secondo momento. Per ulteriori informazioni, vedere [Crittografia di dati in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) nella Guida per sviluppatori e amministratori.  

5. Se la sincronizzazione di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non è ancora impostata, verrà richiesto se si desidera utilizzare l'impostazione di sincronizzazione predefinita. A seconda se si desidera conservare o meno i record allineati in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)]  scegliere **Sì** o **No**.

## <a name="show-me-the-process"></a>Mostrare il processo

Il video seguente mostra i passaggi per la connessione a [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Connessione alle versioni locali

Per connettere [!INCLUDE[d365fin](includes/d365fin_md.md)] on-premises a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], è necessario specificare alcune informazioni nella pagina **Setup connessione a Common Data Service**.

Se si desidera connettersi utilizzando un account Azure Active Directory (Azure AD), è necessario registrare un'applicazione in Azure AD e fornire l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento da utilizzare. L'URL di reindirizzamento è precompilato e dovrebbe funzionare per la maggior parte delle installazioni. È necessario configurare l'installazione per utilizzare HTTPS. Per ulteriori informazioni, vedere [Configurazione di SSL per proteggere la connessione client Web di Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Se si sta configurando il server in modo da avere una home page diversa, è sempre possibile cambiare l'URL. Il segreto del client verrà salvato come stringa crittografata nel database.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Per registrare un'applicazione in Azure AD per la connessione da Business Central a Common Data Service

I seguenti passaggi presuppongono che si stia utilizzando Azure AD per gestire identità e accesso. Per ulteriori informazioni sulla registrazione di un'applicazione in Azure AD vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). Se non si utilizza Azure AD vedere [Utilizzo di un altro servizio di gestione dell'identità e degli accessi](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Nel portale di Azure, in **Gestisci** nel riquadro di navigazione, selezionare **Autenticazione**.  
2. In **URL di reindirizzamento**, aggiungere l'URL di reindirizzamento suggerito nella pagina **Setup connessione a Common Data Service** in [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. In **Gestisci**, scegliere **Autorizzazioni API**.
4. In **Autorizzazioni configurate**, scegliere **Aggiungi un'autorizzazione** e quindi aggiungere le autorizzazioni delegate nella scheda **API Microsoft** come segue:
    * Per Business Central, aggiungere le autorizzazioni **Financials.ReadWrite.All**.
    * Per Dynamics CRM, aggiungere le autorizzazioni **user_impersonation**.  

    > [!NOTE]
    > Il nome dell'API Dynamics CRM potrebbe cambiare.

5. In **Gestisci**, scegliere **Certificati e segreti**, quindi creare un nuovo segreto per l'app. Il segreto viene utilizzato in [!INCLUDE[d365fin](includes/d365fin_md.md)], nel campo **Segreto client** della pagina **Setup connessione a Common Data Service** o archiviato in un archivio sicuro e fornito in una sottoscrizione di eventi come descritto in precedenza in questo argomento.
6. Scegliere **Panoramica**, quindi trovare il valore **ID applicazione (client)**. Questo è l'ID client dell'applicazione. È necessario inserirlo nella pagina **Setup connessione a Common Data Service** nel campo **ID client** o archiviarlo in un archivio sicuro e fornirlo in una sottoscrizione di eventi.
7. In [!INCLUDE[d365fin](includes/d365fin_md.md)], nella pagina **Setup connessione a Common Data Service** nel campo **URL ambiente** inserire l'URL per l'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
8. Per abilitare la connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], attivare l'interruttore **Abilitato**.
9. Accedere con l'account amministratore per Azure Active Directory (questo account deve avere una licenza valida per [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ed essere un amministratore nell'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Dopo aver effettuato l'accesso, verrà richiesto di consentire all'applicazione registrata l'accesso a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] per conto dell'organizzazione. È necessario fornire il consenso per completare il setup.

   > [!NOTE]
   > Se non viene richiesto di accedere con il proprio account amministratore, è probabile che i popup siano bloccati. Per accedere, consentire i popup da `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Utilizzo di un altro servizio di gestione dell'identità e degli accessi

Se non si sta usando Azure Active Directory per gestire le identità e l'accesso, è necessario l'aiuto di uno sviluppatore. Se si preferisce archiviare l'ID app e il segreto in una posizione diversa, è possibile lasciare vuoti i campi ID client e Segreto client e scrivere un'estensione per recuperare l'ID e il segreto dalla posizione. È possibile fornire il segreto in fase di esecuzione sottoscrivendo gli eventi OnGetCDSConnectionClientId e OnGetCDSConnectionClientSecret nella codeunit 7201 "Implementazione dell'integrazione di CDS"

### <a name="to-disconnect-from-cds_long_md"></a>Per disconnettersi da [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione a CDS** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup connessione a CDS**, disattiva l'opzione **Abilitato**.  

## <a name="see-also"></a>Vedere anche

[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  
