---
title: Creare utenti in base alle licenze
description: Descrive come aggiungere utenti a Business Central Online o in locale in base alle licenze.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173
ms.date: 03/23/2022
ms.author: edupont
ms.openlocfilehash: 52d8c0fb735bb0667f2219f5ed73e914e236014a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512154"
---
# <a name="create-users-according-to-licenses"></a>Creare utenti in base alle licenze

Questo articolo descrive come gli amministratori creano utenti e definiscono chi può accedere a [!INCLUDE[prod_short](includes/prod_short.md)]. Questo articolo illustra anche come assegnare autorizzazioni a diversi tipi di utenti in base alle licenze del prodotto.

Quando crei gli utenti in [!INCLUDE[prod_short](includes/prod_short.md)], puoi assegnare loro le autorizzazioni tramite set di autorizzazioni e organizzare gli utenti in gruppi di utenti. I gruppi di utenti semplificano la gestione delle autorizzazioni per più utenti contemporaneamente. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

Per ulteriori informazioni sui diversi tipi di licenze e sul funzionamento delle licenze in [!INCLUDE[prod_short](includes/prod_short.md)], [scarica la guida alle licenze di Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Il processo di gestione degli utenti e delle licenze varia a seconda che la soluzione [!INCLUDE[prod_short](includes/prod_short.md)] sia distribuita online o in locale. Per [!INCLUDE [prod_short](includes/prod_short.md)] online, è necessario aggiungere utenti da Microsoft 365. Nelle distribuzioni locali è possibile creare, modificare ed eliminare utenti direttamente.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Gestire utenti e licenze nei tenant online

Nella versione online di [!INCLUDE[prod_short](includes/prod_short.md)], il tuo abbonamento definisce il numero di utenti che sono consentiti. Gli utenti vengono aggiunti al tenant nel Centro per i partner Microsoft, in genere dal partner Microsoft. Per ulteriori informazioni, vedere [Aggiungere un nuovo cliente](/partner-center/add-a-new-customer) e [Creare, sospendere o annullare le sottoscrizioni dei clienti](/partner-center/create-a-new-subscription) nella guida del Centro per i partner Microsoft.

Per definire chi può accedere a [!INCLUDE[prod_short](includes/prod_short.md)], devi assegnare le licenze del prodotto agli utenti in base al lavoro che svolgono in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile assegnare le licenze in diversi modi:

- L'amministratore di Microsoft 365 della società può eseguire questa operazione nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com). Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un partner Microsoft può assegnare licenze nell'interfaccia di amministrazione di Microsoft 365 o nel Centro per i partner di Microsoft. Per ulteriori informazioni, vedere [Attività di gestione degli utenti per gli account dei clienti](/partner-center/assign-licenses-to-users) nella Guida del Centro per i partner Microsoft.

Per ulteriori informazioni, vedere [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) nella Guida per amministratori.

> [!NOTE]
> Dopo aver aggiunto gli utenti nell'interfaccia di amministrazione di Microsoft 365, ti consigliamo di aggiornare le informazioni sull'utente in [!INCLUDE[prod_short](includes/prod_short.md)] il prima possibile. Mantenere aggiornate le informazioni sugli utenti è facile e aiuta a garantire che le persone possano sempre accedere. Per altre informazioni vedi [Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central](#adduser).<br>
> 
> L'aggiornamento delle informazioni sull'utente è particolarmente importante se hai personalizzato i set di autorizzazioni per la licenza. Se un nuovo utente tenta di accedere a [!INCLUDE[prod_short](includes/prod_short.md)] prima che tu lo abbia aggiunto, potrebbe non essere in grado di farlo. Per ulteriori informazioni, vedi [Configurare le autorizzazioni in base alle licenze](#licensespermissions). 
> 
> Tuttavia, gli utenti che riscontrano questo problema non vengono effettivamente bloccati. Possono utilizzare l'azione **Torna alla home** o semplicemente accedere di nuovo per risolvere il problema.

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Configurare le autorizzazioni in base alle licenze

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Gli amministratori possono configurare set di autorizzazioni e gruppi di utenti in base ai diversi tipi di licenza.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Ad esempio, la licenza di uso comune, *Membro del team Dynamics 365 Business Central*, è impostata per impostazione predefinita per avere i gruppi di utenti *D365 Membro del team* e *Azione esportazione Excel* più i seguenti set di autorizzazioni:

- D365 LETTURA
- D365 MEMBRO DEL TEAM
- MODIFICA IN EXCEL - VISUALIZZA
- ESPORTA REPORT EXCEL
- LOCALE

Se questa non è la configurazione corretta per un determinato tenant, l'amministratore può modificarla. Tuttavia, le autorizzazioni personalizzate influiranno solo sui nuovi utenti a cui è stata assegnata quella licenza. Le autorizzazioni per gli utenti esistenti a cui è stata assegnata la licenza non saranno interessate.  

1. Accedere a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando come account amministratore.  
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Configurazione licenza**, quindi scegli il collegamento correlato.  

    In alternativa, se sei già nella pagina **Utenti** puoi eseguire la guida **Aggiorna utenti da Microsoft 365**, quindi, nella prima pagina della guida, scegli il collegamento **Configura le autorizzazioni per licenza**.  
3. Nella pagina **Configurazione della licenza** scegli la licenza che desideri personalizzare, quindi scegli l'azione **Configura**.  
4. Scegli il campo **Personalizza autorizzazioni** per attivare la personalizzazione e apportare le modifiche pertinenti.  

    Nel nostro esempio, l'amministratore desidera rimuovere l'autorizzazione di modifica in Excel, quindi rimuove il gruppo di utenti *Azione esportazione Excel* dalla licenza Membro del team. D'ora in poi, i nuovi utenti a cui è stata assegnata la licenza di membro del team non avranno la possibilità di esportare i dati in Excel. Se l'organizzazione cambia idea, può semplicemente tornare alla pagina **Configurazione della licenza** e disattivare la personalizzazione per quel tipo di licenza.  

> [!IMPORTANT]
> Questa personalizzazione delle autorizzazioni ha effetto solo per i nuovi utenti a cui si assegna la licenza pertinente. Gli utenti esistenti non vengono aggiornati. Ti consigliamo di personalizzare le autorizzazioni prima di iniziare ad assegnare le licenze agli utenti nell'interfaccia di amministrazione di Microsoft 365.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central
Dopo aver aggiunto utenti o modificato le informazioni utente nell'interfaccia di amministrazione di Microsoft 365, è possibile importare rapidamente le informazioni utente in [!INCLUDE[prod_short](includes/prod_short.md)]. L'importazione include le assegnazioni della licenza. 

1. Accedere a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando come account amministratore.
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Utenti**, quindi scegli il collegamento correlato.  
3. Scegliere **Aggiorna utenti da Microsoft 365**.

Quando si aggiungono nuovi utenti, il passaggio successivo consiste nell'assegnare gruppi di utenti e autorizzazioni. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md). Se stai aggiornando le informazioni utente e l'aggiornamento include una modifica della licenza, gli utenti verranno assegnati al gruppo di utenti appropriato e i relativi set di autorizzazioni verranno aggiornati. Per ulteriori informazioni, vedere [Per gestire le autorizzazioni tramite gruppo di utenti](ui-define-granular-permissions.md).  

> [!NOTE]
> A tutti gli utenti di un ambiente deve essere assegnata la stessa licenza: Essential o Premium. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Per altre informazioni sulla sincronizzazione delle informazioni utente con Microsoft 365, vedere la sezione [Sincronizzazione con Microsoft 365](#m365).

> [!NOTE]
> Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a Business Central in modo che possa utilizzare i dati fiscali dell'azienda. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Per rimuovere l'accesso di un utente al sistema

Nelle distribuzioni online, è possibile rimuovere l'accesso di un utente a [!INCLUDE[prod_short](includes/prod_short.md)]. Tutti i riferimenti all'utente vengono mantenuti. Tuttavia, l'utente non può accedere e le sessioni attive per l'utente vengono interrotte.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Apri la pagina **Scheda utente** per l'utente pertinente, quindi nel campo **Stato** seleziona **Disabilitato**.
3. Per consentire nuovamente l'accesso all'utente, imposta il campo **Stato** su **Abilitato**.

Puoi anche rimuovere la licenza da un utente nell'interfaccia di amministrazione di Microsoft 365. L'utente non può quindi eseguire l'accesso. Per ulteriori informazioni, vedi [Rimuovere le licenze agli utenti](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Sincronizzazione con Microsoft 365

Quando assegni una licenza per [!INCLUDE[prod_short](includes/prod_short.md)] a un utente in Microsoft 365, vi sono due modi per creare l'utente in [!INCLUDE[prod_short](includes/prod_short.md)].  

- L'amministratore può aggiungere l'utente scegliendo l'azione **Aggiorna utenti da Microsoft 365** nella pagina **Utenti** come descritto nella sezione [Per aggiungere un utente o aggiornare le informazioni sull'utente in Business Central](#adduser).
- Le informazioni sulla licenza si aggiorneranno automaticamente quando l'utente accede per la prima volta.

In entrambi i casi, vengono automaticamente eseguite diverse impostazioni. Queste impostazioni sono elencate nella seconda e terza colonna nella tabella seguente.

Se si modificano le informazioni dell'utente in Microsoft 365, puoi aggiornare [!INCLUDE[prod_short](includes/prod_short.md)] in modo da riflettere la modifica. A seconda di ciò che si desidera aggiornare, utilizzare una delle azioni della pagina **Utenti**. Le azioni sono descritte nelle ultime tre colonne nella tabella seguente.

> [!NOTE]
> Le azioni descritte nella tabella seguente sono accurate, tuttavia l'unica necessaria è **Aggiorna utenti da Microsoft 365**, che è stata aggiunta per semplificare il processo. Le altre azioni verranno rimosse in una versione futura di [!INCLUDE[prod_short](includes/prod_short.md)].

|Cosa succede quando:|Primo utente, primo accesso|Ottieni utenti da Microsoft 365|Aggiorna utenti da Microsoft 365|Ripristina gruppi di utenti di default dell'utente|Aggiorna i gruppi di utenti|Aggiorna le informazioni utente da Microsoft 365|
|-|-|-|-|-|-|-|
|Ambito:|Utente corrente|Nuovi utenti in Microsoft 365|Più utenti selezionati|Singolo utente selezionato (tranne quello corrente)|Più utenti selezionati|Più utenti selezionati|
|Creare il nuovo utente e assegnare il set di autorizzazioni SUPER.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Aggiorna l'utente in base alle informazioni in Microsoft 365: Stato, Nome completo, E-mail contatto, Indirizzo e-mail di autenticazione.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Sincronizzare piani utente (licenze) con licenze e ruoli assegnati in Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Aggiungere l'utente a gruppi di utenti in base ai piani utente correnti. Rimuovere il set di autorizzazioni SUPER per tutti gli utenti diversi dal primo utente che accede e gli [amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Almeno un'autorizzazione SUPER è obbligatoria.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Rimuove le autorizzazioni e i gruppi di utenti assegnati manualmente.|**X**<br /><br />Aggiorna le assegnazioni di gruppi di utenti.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Gestire utenti e licenze nelle distribuzioni locali

Per le distribuzioni locali, nel file di licenza (.flf) è specificato il numero di licenze utente. Quando un amministratore o il partner Microsoft carica il file di licenza, può specificare quali utenti possono accedere a [!INCLUDE[prod_short](includes/prod_short.md)].

Per le distribuzioni locali, l'amministratore crea, modifica ed elimina gli utenti direttamente dalla pagina **Utenti**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Per modificare o eliminare un utente in una distribuzione locale

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Scegliere l'utente che si intende modificare, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda utente** modificare le informazioni come necessario.  
4. Per eliminare un utente, selezionarlo, quindi scegliere l'azione **Elimina**.

> [!NOTE]
> Per le distribuzioni locali, un amministratore può specificare come autenticare le credenziali dell'utente nell'istanza [!INCLUDE[server](includes/server.md)]. Quando si crea un utente, si fornisce il tipo di credenziale che si sta utilizzando.
>
> Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella Guida per amministratori di [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Vedere anche

[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Licenze in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Aggiungere utenti a Microsoft 365 per le aziende](/microsoft-365/admin/add-users/add-users)  
[Sicurezza e protezione in Business Central (contenuto per amministratori)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Assegnare un ID telemetria agli utenti](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]