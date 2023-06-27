---
title: Creare utenti in base alle licenze
description: Descrive come aggiungere utenti a Business Central Online o in locale in base alle licenze.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="create-users-according-to-licenses" />Creare utenti in base alle licenze

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Questo articolo descrive come gli amministratori creano utenti e definiscono chi può accedere a [!INCLUDE[prod_short](includes/prod_short.md)]. Scoprirai come assegnare autorizzazioni a diversi utenti in base alle licenze del prodotto.

Quando crei utenti in [!INCLUDE[prod_short](includes/prod_short.md)], concedi loro le autorizzazioni tramite set di autorizzazioni. Puoi anche organizzare gli utenti in gruppi di utenti. I gruppi di utenti semplificano la gestione delle autorizzazioni e altre impostazioni per più utenti contemporaneamente. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

Per ulteriori informazioni sui diversi tipi di licenze e sul funzionamento delle licenze in [!INCLUDE[prod_short](includes/prod_short.md)], [scarica la guida alle licenze di Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Il processo di gestione degli utenti e delle licenze varia a seconda che la soluzione [!INCLUDE[prod_short](includes/prod_short.md)] sia distribuita online o in locale. Per [!INCLUDE [prod_short](includes/prod_short.md)] online, è necessario aggiungere utenti da Microsoft 365. Nelle distribuzioni locali è possibile creare, modificare ed eliminare utenti direttamente.  

## <a name="manage-users-and-licenses-in-online-tenants" />Gestire utenti e licenze nei tenant online

Gli account utente in [!INCLUDE[prod_short](includes/prod_short.md)] devono essere prima creati nell'interfaccia di amministrazione Microsoft 365. Questi account utente non sono esclusivi di Business Central. Se ti abboni ad altri piani, possono essere utilizzati per accedere ad altre applicazioni, come Power BI. Per informazioni sulla creazione di utenti nell'interfaccia di amministrazione Microsoft 365, vai a [Aggiungi utenti nell'interfaccia di amministrazione Microsoft](/microsoft-365/admin/add-users/add-users).

Il tuo abbonamento a [!INCLUDE[prod_short](includes/prod_short.md)] online definisce il numero di licenze utente [!INCLUDE[prod_short](includes/prod_short.md)] consentite. Gli utenti vengono aggiunti al tenant nel Centro per i partner Microsoft, in genere dal partner Microsoft. Per ulteriori informazioni, vedere [Amministraziojne di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Assegna le licenze agli utenti in base al lavoro che ciascun utente eseguirà [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile assegnare le licenze in diversi modi:

- L'amministratore di Microsoft 365 della società può eseguire questa operazione nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com). Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un partner Microsoft può assegnare licenze nell'interfaccia di amministrazione di Microsoft 365 o nel Centro per i partner di Microsoft. Per ulteriori informazioni, vedere [Attività di gestione degli utenti per gli account dei clienti](/partner-center/assign-licenses-to-users) nella Guida del Centro per i partner Microsoft.

Per ulteriori informazioni, vedere [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) nella Guida per amministratori.

Dopo aver creato gli account utente nell'interfaccia di amministrazione Microsoft 365, esistono due modi per importarli in Business Central:

- Un account utente viene importato automaticamente quando l'utente accede a [!INCLUDE [prod_short](includes/prod_short.md)] per la prima volta.

- L'amministratore può importare gli utenti selezionando l'azione  **Aggiorna utenti da Microsoft 365** nella pagina **Utenti* .

Entrambi gli approcci hanno i loro vantaggi e puoi usarli contemporaneamente. Ogni approccio consente agli amministratori di configurare in modo proattivo [!INCLUDE [prod_short](includes/prod_short.md)] per assegnare le autorizzazioni iniziali, i gruppi di utenti e i profili utente. L'utilizzo dell'azione **Aggiorna utenti da Microsoft 365** offre agli amministratori un maggiore controllo per modificare autorizzazioni, gruppi di utenti e profili. È un approccio ideale quando si configura [!INCLUDE [prod_short](includes/prod_short.md)] per la prima volta, prima che qualsiasi utente acceda o quando si aggiunge un nuovo team di utenti.

> [!NOTE]
> Dopo aver aggiunto gli utenti nell'interfaccia di amministrazione di Microsoft 365, ti consigliamo di aggiornare le informazioni sull'utente in [!INCLUDE[prod_short](includes/prod_short.md)] il prima possibile. Mantenere aggiornate le informazioni sugli utenti è facile e aiuta a garantire che le persone possano sempre accedere. Per altre informazioni vedi [Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central](#adduser).<br>
>
> L'aggiornamento delle informazioni sull'utente è particolarmente importante se hai personalizzato i set di autorizzazioni per la licenza. Se un nuovo utente tenta di accedere a [!INCLUDE[prod_short](includes/prod_short.md)] prima che tu lo abbia aggiunto, potrebbe non essere in grado di farlo. Per ulteriori informazioni, vedi [Configurare le autorizzazioni in base alle licenze](#licensespermissions).
>
> Tuttavia, gli utenti che riscontrano questo problema non vengono effettivamente bloccati. Possono usare l'azione **Torna alla home** o semplicemente accedere di nuovo per risolvere il problema.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Per ulteriori informazioni, vedi [Accesso dell'amministratore con delega a Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="configure-permissions-based-on-licenses" /><a name="licensespermissions"></a>Configurare le autorizzazioni in base alle licenze

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Gli amministratori possono configurare set di autorizzazioni e gruppi di utenti per ciascuna licenza.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Ad esempio, la licenza comunemente utilizzata, *Membro del team Dynamics 365 Business Central*, ha i seguenti set di autorizzazioni per impostazione predefinita:

- D365 LETTURA
- D365 MEMBRO DEL TEAM
- MODIFICA IN EXCEL - VISUALIZZA
- ESPORTA REPORT EXCEL
- LOCALE

Altri set di autorizzazioni vengono aggiunti automaticamente in base ai gruppi di utenti assegnati alla licenza. Quando si crea un nuovo utente basato su questa licenza, [!INCLUDE[prod_short](includes/prod_short.md)] assegna i set di autorizzazioni originati dai gruppi di utenti e i set di autorizzazioni dalla licenza. Le stesse autorizzazioni iniziali vengono assegnate all'utente se il suo account utente è stato creato automaticamente in [!INCLUDE[prod_short](includes/prod_short.md)] o se l'amministratore ha utilizzato l'azione **Aggiorna utenti da Microsoft 365** nella pagina **Utenti**.

Se questa non è la configurazione corretta per un determinato ambiente, l'amministratore può modificarla. Tuttavia, le autorizzazioni personalizzate influiranno solo sui nuovi utenti a cui è stata assegnata quella licenza. Le autorizzazioni per gli utenti esistenti a cui è stata assegnata la licenza non saranno interessate.  

1. Accedere a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando come account amministratore.  
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Configurazione licenza**, quindi scegli il collegamento correlato.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Nella pagina **Configurazione della licenza** scegli la licenza che desideri personalizzare, quindi scegli l'azione **Configura**.  
4. Scegli il campo **Personalizza autorizzazioni** per attivare la personalizzazione e apportare le modifiche pertinenti.  

    Nel nostro esempio, l'amministratore desidera rimuovere l'autorizzazione di modifica in Excel, quindi rimuove il gruppo di utenti *Azione esportazione Excel* dalla licenza Membro del team. D'ora in poi, i nuovi utenti a cui è stata assegnata la licenza di membro del team non avranno la possibilità di esportare i dati in Excel. Se l'organizzazione cambia idea, può semplicemente tornare alla pagina **Configurazione della licenza** e disattivare la personalizzazione per quel tipo di licenza.  

> [!IMPORTANT]
> Questa personalizzazione delle autorizzazioni ha effetto solo per i nuovi utenti a cui si assegna la licenza pertinente. Gli utenti esistenti non vengono aggiornati. Ti consigliamo di personalizzare le autorizzazioni prima di iniziare ad assegnare le licenze agli utenti nell'interfaccia di amministrazione di Microsoft 365.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central" /><a name="adduser"></a>Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central

Dopo aver aggiunto utenti o modificato le informazioni utente nell'interfaccia di amministrazione di Microsoft 365, è possibile importare rapidamente le informazioni utente in [!INCLUDE[prod_short](includes/prod_short.md)]. L'importazione include le assegnazioni della licenza.  

1. Accedere a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando come account amministratore.
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Utenti**, quindi scegli il collegamento correlato.  
3. Scegliere **Aggiorna utenti da Microsoft 365**.

> [!IMPORTANT]  
> L'esecuzione della sincronizzazione degli utenti da Microsoft 365 utilizzando la guida **Aggiornare gli utenti da Microsoft 365** richiede il set di autorizzazioni SUPER.

> [!NOTE]
> La guida **Aggiornare gli utenti da Microsoft 365** non aggiorna gli utenti a cui non è assegnata una licenza, ad esempio qualcuno che è amministratore globale e amministratore di Dynamics 365. Tali utenti verranno aggiornati la prossima volta che accedono all'ambiente.

Per i nuovi utenti, il passaggio successivo consiste nell'assegnare gruppi di utenti e autorizzazioni. Vai ad [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md) per ulteriori informazioni. Se stai aggiornando un utente e l'aggiornamento include una modifica della licenza, gli utenti verranno assegnati al gruppo di utenti appropriato e i relativi set di autorizzazioni verranno aggiornati. Per ulteriori informazioni, vedere [Per gestire le autorizzazioni tramite gruppo di utenti](ui-define-granular-permissions.md).  

> [!NOTE]
> A tutti gli utenti di un ambiente deve essere assegnata la stessa licenza: Essentials o Premium. Per ulteriori informazioni sulle licenze, visita il sito Web [Business Central](https://dynamics.microsoft.com/business-central/overview/) .

Per altre informazioni sulla sincronizzazione delle informazioni utente con Microsoft 365, vedi la sezione [Sincronizzazione con Microsoft 365](#m365).

> [!NOTE]
> Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a [!INCLUDE[prod_short](includes/prod_short.md)] in modo che possa utilizzare i dati fiscali dell'azienda. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system" />Per rimuovere l'accesso di un utente al sistema

Puoi rimuovere l'accesso di un utente a [!INCLUDE[prod_short](includes/prod_short.md)] online. Tutti i riferimenti all'utente vengono mantenuti. Tuttavia, l'utente non può accedere e le sessioni attive per l'utente vengono interrotte.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Apri la pagina **Scheda utente** per l'utente pertinente, quindi nel campo **Stato** seleziona **Disabilitato**.
3. Per consentire nuovamente l'accesso all'utente, imposta il campo **Stato** su **Abilitato**.

Puoi anche rimuovere la licenza da un utente nell'interfaccia di amministrazione di Microsoft 365. L'utente non può quindi eseguire l'accesso. Per ulteriori informazioni, vedi [Rimuovere le licenze agli utenti](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365" /><a name="m365"></a>Sincronizzazione con Microsoft 365

Quando assegni una licenza per [!INCLUDE[prod_short](includes/prod_short.md)] a un utente in Microsoft 365, vi sono due modi per creare l'utente in [!INCLUDE[prod_short](includes/prod_short.md)].  

- L'amministratore può aggiungere l'utente scegliendo l'azione **Aggiorna utenti da Microsoft 365** nella pagina **Utenti** come descritto nella sezione [Per aggiungere un utente o aggiornare le informazioni sull'utente in Business Central](#adduser).
- Le informazioni sulla licenza si aggiorneranno automaticamente quando l'utente accede per la prima volta.

In entrambi i casi, vengono automaticamente applicate diverse impostazioni. Queste impostazioni sono elencate nella seconda e terza colonna nella tabella seguente.

Se si modificano le informazioni dell'utente in Microsoft 365, puoi aggiornare [!INCLUDE[prod_short](includes/prod_short.md)] in modo da riflettere la modifica. A seconda di ciò che si desidera aggiornare, usare una delle azioni della pagina **Utenti**. Le azioni sono descritte nelle ultime due colonne nella tabella seguente.

|Cosa succede quando:|Primo utente, primo accesso|Aggiorna utenti da Microsoft 365|Ripristina gruppi di utenti di default dell'utente|
|-|-|-|-|
|Ambito:|Utente corrente|Più utenti selezionati|Singolo utente selezionato (tranne quello corrente)|
|Creare il nuovo utente e assegnare il set di autorizzazioni SUPER.<br /><br /><!--Platform-->|**X**|**X** | | 
|Aggiorna l'utente in base alle informazioni in Microsoft 365: Stato, Nome completo, E-mail contatto, Indirizzo e-mail di autenticazione.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Sincronizzare piani utente (licenze) con licenze e ruoli assegnati in Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Aggiungere l'utente a gruppi di utenti in base ai piani utente correnti. Rimuovere il set di autorizzazioni SUPER per tutti gli utenti diversi dal primo utente che accede e gli [amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Almeno un'autorizzazione SUPER è obbligatoria.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Rimuove le autorizzazioni e i gruppi di utenti assegnati manualmente.|

Gli utenti possono accedere ai record di [!INCLUDE[prod_short](includes/prod_short.md)] in Teams utilizzando solo la licenza Microsoft 365. Quando l'accesso è abilitato per un ambiente, la sincronizzazione tramite l'azione **Aggiorna utenti da Microsoft 365** non includerà gli utenti che dispongono solo di una licenza Microsoft 365. Per includere questi utenti nella sincronizzazione, devi prima aggiornare le impostazioni dell'ambiente assegnando un gruppo di sicurezza che contenga utenti con una licenza [!INCLUDE[prod_short](includes/prod_short.md)] e utenti con solo una licenza Microsoft 365.

Scopri come proteggere l'accesso agli ambienti utilizzando i gruppi di sicurezza in [Gestire gli accessi utilizzando gruppi di Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Ottieni una panoramica degli accessi a [!INCLUDE[prod_short](includes/prod_short.md)] in Teams con licenze Microsoft 365 in [admin-access-with-m365-license](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments" />Gestire utenti e licenze nelle distribuzioni locali

Per le distribuzioni locali, nel file di licenza (.bclicense o .flf). è specificato il numero di licenze utente. Quando un amministratore o il partner Microsoft carica il file di licenza, può specificare quali utenti possono accedere a [!INCLUDE[prod_short](includes/prod_short.md)].

Per le distribuzioni locali, l'amministratore crea, modifica ed elimina gli utenti direttamente dalla pagina **Utenti**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment" />Per modificare o eliminare un utente in una distribuzione locale

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti**, quindi scegli il collegamento correlato.
2. Scegliere l'utente che si intende modificare, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda utente** modificare le informazioni come necessario.  
4. Per eliminare un utente, selezionarlo, quindi scegliere l'azione **Elimina**.

> [!NOTE]
> Per le distribuzioni locali, un amministratore può specificare come autenticare le credenziali dell'utente nell'istanza [!INCLUDE[server](includes/server.md)]. Quando si crea un utente, si fornisce il tipo di credenziale che si sta utilizzando.
>
> Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella Guida per amministratori di [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also" />Vedere anche

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
