---
title: Connessione a Microsoft Dataverse (video)
description: Imposta una connessione tra Business Central e Dataverse. In genere le aziende creano la connessione per integrare i dati con un'altra app aziendale di Dynamics 365.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 7200, 7201
ms.date: 09/30/2021
ms.author: bholtorf
ms.openlocfilehash: bbe27c46562fa7550619283cb85cd1d7dcc76a3c
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059546"
---
# <a name="connect-to-microsoft-dataverse"></a>Connettersi a Microsoft Dataverse



Questo argomento descrive come impostare una connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. In genere, le aziende creano la connessione per integrare e sincronizzare i dati con un'altra app aziendale di Dynamics 365, ad esempio [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Operazioni preliminari

Prima di creare la connessione, è necessario disporre di alcune informazioni:  

* L'URL per l'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a cui vuoi connetterti. Se si utilizza la guida al setup assistito **Setup connessione a Dataverse** per creare la connessione individueremo i tuoi ambienti, ma puoi anche inserire l'URL di un altro ambiente nel tuo tenant.  
* Il nome utente e la password di un account che dispone di autorizzazioni di amministratore in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Se disponi del primo ciclo di rilascio del 2020 di [!INCLUDE[prod_short](includes/prod_short.md)] locale, versione 16.5, leggi l'articolo [Alcuni problemi noti](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Dovrai completare la soluzione alternativa descritta prima di poter creare la connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* La valuta locale della società in [!INCLUDE[prod_short](includes/prod_short.md)] deve essere la stessa della valuta della transazione di base in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Dopo aver impostato una transazione di base in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non è possibile cambiarla. Per ulteriori informazioni, vedere [Entità della valuta (valuta) di transazione](/powerapps/developer/data-platform/transaction-currency-currency-entity). Ciò significa che tutte le società [!INCLUDE[prod_short](includes/prod_short.md)] che colleghi a un'organizzazione [!INCLUDE[cds_long_md](includes/cds_long_md.md)] devono utilizzare la stessa valuta.

> [!IMPORTANT]
> L'ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non deve essere in modalità di amministrazione. La modalità di amministrazione causerà la mancata connessione perché l'account utente di integrazione per la connessione non dispone delle autorizzazioni di amministratore. Per ulteriori informazioni, vedere [Modalità di amministrazione](/power-platform/admin/admin-mode).

> [!Note]
> Tali passaggi descrivono la procedura per [!INCLUDE[prod_short](includes/prod_short.md)] online.
> Se stai utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] locale e non si sta utilizzando l'account Azure Active Directory per connettersi a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], devi inoltre specificare un nome utente e una password di un account utente per l'integrazione. Questo account viene definito account "utente integrazione". Se si sta usando un account Azure Active Directory l'account utente di integrazione non è richiesto o visualizzato. L'utente dell'integrazione verrà impostato automaticamente e non richiede una licenza.

## <a name="set-up-a-connection-to-cds_long_md"></a>Impostare una connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

Per tutti i tipi di autenticazione diversi dall'autenticazione di Microsoft 365, imposti la connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] nella pagina **Setup connessione a Dataverse**. Per l'autenticazione di Microsoft 365, è consigliabile utilizzare la guida del setup assistito **Setup connessione a Dataverse**. La guida rende più semplice configurare la connessione e specificare le funzionalità avanzate, ad esempio il modello di proprietà e la sincronizzazione iniziale.  

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

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup assistito**, quindi scegli il collegamento correlato.
2. Scegliere **Impostare una connessione a Microsoft Dataverse** per avviare la guida al setup assistito.
3. Compilare i campi in base alle esigenze.

> [!NOTE]
> Se non viene richiesto di accedere con il proprio account amministratore, è probabile che i popup siano bloccati. Per accedere, consentire i popup da `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Per creare o gestire la connessione manualmente

La procedura seguente illustra come configurare la connessione manualmente nella pagina **Setup connessione a Dataverse**. Questa è anche la pagina in cui si gestiscono le impostazioni per l'integrazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup connessione a Dataverse**, quindi scegli il collegamento correlato.
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
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Per verificare le impostazioni di connessione, scegli **Connessione**, quindi **Test connessione**.  

    > [!NOTE]  
    > Se la crittografia dei dati non è abilitata in [!INCLUDE[prod_short](includes/prod_short.md)], verrà richiesto se si desidera abilitarla. Per abilitare la crittografia dei dati, scegliere **Sì** e immettere le informazioni necessarie. In caso contrario, scegliere **No**. È possibile abilitare la crittografia dei dati in un secondo momento. Per ulteriori informazioni, vedere [Crittografia di dati in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) nella Guida per sviluppatori e amministratori.  
5. Se la sincronizzazione di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non è ancora impostata, verrà richiesto se si desidera utilizzare l'impostazione di sincronizzazione predefinita. A seconda se si desidera conservare o meno i record allineati in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)]  scegliere **Sì** o **No**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Personalizzare l'accoppiamento basato sulla corrispondenza

A partire dalla release 2021 wave 2, è possibile accoppiare i record in [!INCLUDE [prod_short](includes/prod_short.md)] e [!INCLUDE [cds_long_md](includes/cds_long_md.md)] in base a criteri di corrispondenza definiti dall'amministratore.  

L'algoritmo per la corrispondenza dei record può essere avviato dai seguenti punti in [!INCLUDE [prod_short](includes/prod_short.md)]:

* Elenca le pagine che mostrano i record sincronizzati con [!INCLUDE [cds_long_md](includes/cds_long_md.md)], come le pagine Clienti e Articoli.  

    Seleziona più record, quindi scegli l'azione **Correlato**, scegli **Dataverse**, scegli **Accoppiamento** e poi scegli **Accoppiamento basato sulla corrispondenza**.

    Quando il processo di accoppiamento basato sulla corrispondenza è avviato da un elenco di dati master, un lavoro di accoppiamento sarà programmato subito dopo aver selezionato i criteri di accoppiamento.  
* Il **Dataverse Full Synch. Pagina direvisione** .  

    Quando il processo di sincronizzazione completa rileva che hai disaccoppiato i record sia in [!INCLUDE [prod_short](includes/prod_short.md)] che in [!INCLUDE [cds_long_md](includes/cds_long_md.md)], appare un link **Seleziona criteri di accoppiamento** per la relativa tabella di integrazione.  

    È possibile avviare il processo **Eseguire la sincronizzazione completa** dalle pagine **Dataverse Configurazione connessione** e **Configurazione connessione Dynamics 365**, e può essere avviato come un passo nella guida **Configura una configurazione assistita Dataverse** quando si sceglie di completare la configurazione ed eseguire la sincronizzazione completa alla fine.  

    Quando il processo di accoppiamento basato sulla corrispondenza viene avviato dalla pagina **Dataverse Revisione sinc completa**, un lavoro di accoppiamento sarà programmato subito dopo aver completato la configurazione.  
* L'elenco delle **mappature delle tabelle di integrazione** .  

    Seleziona una mappatura, scegli l'azione **Coupling** e poi scegli **Accoppiamento basato su corrispondenza**.

    Quando il processo di accoppiamento basato sulla corrispondenza viene avviato da una mappatura della tabella di integrazione, un lavoro di accoppiamento verrà eseguito per tutti i record non accoppiati in quella mappatura. Se è stato eseguito per un insieme di record selezionati dalla lista, verrà eseguito solo per i record non accoppiati selezionati.

In tutti e tre i casi, la pagina **Select Coupling Criteria** si apre in modo da poter definire i criteri di accoppiamento pertinenti. In questa pagina, personalizza l'accoppiamento con i seguenti compiti:

* Scegliere quali campi per abbinare i record di [!INCLUDE [prod_short](includes/prod_short.md)] e le entità di [!INCLUDE [cds_long_md](includes/cds_long_md.md)], e anche scegliere se l'abbinamento su quel campo sarà case-sensitive o no.  

* Specifica se eseguire una sincronizzazione dopo l'accoppiamento dei record e, se il record usa la mappatura bidirezionale, scegli anche cosa succede se i conflitti sono elencati nella pagina **Risolvere i conflitti di aggiornamento** .  

* Dare priorità all'ordine di ricerca dei record specificando una *priorità di corrispondenza* per i campi di mappatura pertinenti. Le priorità di corrispondenza fanno sì che l'algoritmo cerchi una corrispondenza in un numero di iterazioni definito dai valori del campo **Priorità accoppiamento** in ordine crescente. Un valore vuoto nel campo **Priorità accoppiamento** viene interpretato come priorità 0, quindi i campi con questo valore vengono considerati per primi.  

* Specifica se creare una nuova istanza di entità in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] nel caso in cui non sia possibile trovare una corrispondenza unica non accoppiata utilizzando i criteri di corrispondenza. Per attivare questa capacità, scegli l'azione **Crea nuovo se non si trova accoppiamento** .  

### <a name="view-the-results-of-the-coupling-job"></a>Visualizza i risultati del lavoro di accoppiamento

Per visualizzare i risultati del lavoro di accoppiamento, aprire la pagina **Mappatura tabella integrazione**, selezionare la mappatura pertinente, scegliere l'azione **Accoppiamento** e poi scegliere l'azione **Registro lavoro accoppiamento integrazione** .  

Se ci sono dei record che non sono stati accoppiati, puoi approfondire il valore nella colonna Failed, che aprirà una lista di errori che specifica perché i record non sono riusciti ad accoppiarsi.  

L'accoppiamento fallito si verifica spesso nei seguenti casi:

* Non è stato definito alcun criterio di corrispondenza

    In questo caso, eseguite di nuovo l'accoppiamento basato sulla corrispondenza, ma ricordatevi di definire i criteri di accoppiamento.

* Nessuna corrispondenza è stata trovata per un certo numero di record, in base ai campi di corrispondenza scelti

    In questo caso, ripetete l'accoppiamento con qualche altro campo corrispondente.

* Sono state trovate corrispondenze multiple per un certo numero di record, in base ai campi di corrispondenza scelti  

    In questo caso, ripetete l'accoppiamento con qualche altro campo corrispondente.

* È stata trovata una singola corrispondenza, ma il record corrispondente è già accoppiato a un altro record in [!INCLUDE [prod_short](includes/prod_short.md)]  

    In questo caso, ripetete l'accoppiamento con qualche altro campo corrispondente, o indagate perché quell'entità [!INCLUDE [cds_long_md](includes/cds_long_md.md)] è accoppiata a quell'altro record in [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Per aiutarti ad avere una panoramica sul progresso dell'accoppiamento, il campo **Coupled to Dataverse** mostra se un record specifico è accoppiato a un'entità [!INCLUDE [cds_long_md](includes/cds_long_md.md)] oppure no. Puoi filtrare la lista dei record che vengono sincronizzati con [!INCLUDE [cds_long_md](includes/cds_long_md.md)] da questo campo.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Aggiornare le connessioni da Business Central Online per utilizzare l'autenticazione basata su certificato
> [!NOTE]
> Questa sezione è rilevante solo per i locatari online [!INCLUDE[prod_short](includes/prod_short.md)] che sono ospitati da Microsoft. I tenant online ospitati dagli ISV e le installazioni locali non sono interessati.

Ad aprile 2022, [!INCLUDE[cds_long_md](includes/cds_long_md.md)] depreca il tipo di autenticazione di Office365 (nome utente/password). Per ulteriori informazioni, vedi [Deprecazione del tipo di autenticazione Office365](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Inoltre, nel marzo 2022, [!INCLUDE[prod_short](includes/prod_short.md)] depreca l'uso dell'autenticazione da servizio a servizio basata su segreto client per i tenant online e richiede l'uso dell'autenticazione da servizio a servizio basata su certificato per le connessioni a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. I tenant [!INCLUDE[prod_short](includes/prod_short.md)] online ospitati da ISV e le installazioni locali possono continuare a utilizzare l'autenticazione del segreto client per connettersi a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

Per evitare di interrompere le integrazioni, _devi aggiornare_ la connessione per utilizzare l'autenticazione basata su certificato. Sebbene la modifica sia prevista per marzo 2022, ti consigliamo vivamente di eseguire l'upgrade il prima possibile. I passaggi seguenti descrivono come eseguire l'aggiornamento all'autenticazione basata su certificato. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Per aggiornare la connessione di Business Central online per utilizzare l'autenticazione basata su certificato

> [!NOTE]
> L'autenticazione basata su certificato è disponibile nel primo ciclo di rilascio di Business Central 2021 e versioni successive. Se usi una versione precedente, devi pianificare un aggiornamento al primo ciclo di rilascio di Business Central 2021 prima di marzo 2022. Per ulteriori informazioni, vedi [Programmazione degli aggiornamenti](/dynamics365/business-central/dev-itpro/administration/update-rollout-timeline#scheduling-updates). Se riscontri problemi, contatta il tuo partner o l'assistenza.

1. Nell'[interfaccia di amministrazione di Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center), verifica di utilizzare il primo ciclo di rilascio di Business Central 2021 o un ciclo successivo (versione 18 o successiva).
2. A seconda dell'integrazione o meno con Dynamics 365 Sales, esegui una delle seguenti operazioni:
   * Se integri, apri la pagina **Setup connessione a Microsoft Dynamics 365**.
   * In caso contrario, apri la pagina **Setup connessione a Dataverse**.
3. Scegli **Connessione**, poi **Usa autenticazione certificato** per aggiornare la connessione e utilizzare l'autenticazione basata su certificato.
4. Accedi con le credenziali di amministratore per Dataverse. L'accesso dovrebbe richiedere meno di un minuto.

> [!NOTE]
> Devi ripetere questi passaggi in ciascun ambiente [!INCLUDE[prod_short](includes/prod_short.md)], compresi gli ambienti di produzione e sandbox, e in ogni azienda per cui hai una connessione a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Connessione alle versioni locali

Per connettere [!INCLUDE[prod_short](includes/prod_short.md)] on-premises a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], è necessario specificare alcune informazioni nella pagina **Setup connessione a Dataverse**.

Se si desidera connettersi utilizzando un account Azure Active Directory (Azure AD), è necessario registrare un'applicazione in Azure AD e fornire l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento da utilizzare. L'URL di reindirizzamento è precompilato e dovrebbe funzionare per la maggior parte delle installazioni. È necessario configurare l'installazione per utilizzare HTTPS. Per ulteriori informazioni, vedere [Configurazione di SSL per proteggere la connessione client Web di Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Se si sta configurando il server in modo da avere una home page diversa, è sempre possibile cambiare l'URL. Il segreto del client verrà salvato come stringa crittografata nel database. 

### <a name="prerequisites"></a>Prerequisiti

Dataverse deve utilizzare uno dei seguenti tipi di autenticazione:

* Office365 (legacy)

  > [!IMPORTANT]
  > A partire da aprile 2022, Office365 (legacy) non sarà più supportato. Per ulteriori informazioni, vedi [Importanti modifiche (deprecazioni) in arrivo per Power Apps, Power Automate e app per il coinvolgimento dei clienti](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).
* Office365 (moderno, basato su client secret OAuth2)
* OAuth

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Per registrare un'applicazione in Azure AD per la connessione da Business Central a Dataverse

I seguenti passaggi presuppongono che si stia utilizzando Azure AD per gestire identità e accesso. Per ulteriori informazioni sulla registrazione di un'applicazione in Azure AD vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). 

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

### <a name="to-disconnect-from-cds_long_md"></a>Per disconnettersi da [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup connessione a Dataverse**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup connessione a Dataverse**, disattiva l'opzione **Abilitato**.  

## <a name="see-also"></a>Vedere anche

[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
