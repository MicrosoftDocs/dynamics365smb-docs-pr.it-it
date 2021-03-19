---
title: Creare utenti in base alle licenze | Microsoft Docs
description: Descrive come aggiungere utenti a Business Central Online o in locale in base alle licenze.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cc6a32653d443d45a8cb037be275ff84e449ca02
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573353"
---
# <a name="create-users-according-to-licenses"></a>Creare utenti in base alle licenze

Questo articolo descrive in che modo gli amministratori possono creare utenti e definire chi può accedere a [!INCLUDE[prod_short](includes/prod_short.md)] e quali autorizzazioni vengono concesse ai diversi i tipi di utenti in base alle licenze.

Quando si creano utenti in [!INCLUDE[prod_short](includes/prod_short.md)], puoi assegnare loro autorizzazioni specifiche tramite set di autorizzazioni e organizzare gli utenti in gruppi di utenti. I gruppi di utenti semplificano la gestione delle autorizzazioni per più utenti contemporaneamente. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md). 

Per ulteriori informazioni sui diversi tipi di licenze e sul funzionamento delle licenze in [!INCLUDE[prod_short](includes/prod_short.md)], consultare la Guida alle licenze di Dynamics 365, scaricabile da [https://go.microsoft.com/fwlink/?LinkId=866544](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Il processo di gestione degli utenti e delle licenze varia a seconda che la soluzione [!INCLUDE[prod_short](includes/prod_short.md)] sia distribuita online o in locale. Per [!INCLUDE [prod_short](includes/prod_short.md)] Online, è necessario aggiungere utenti da Microsoft 365. Nelle distribuzioni locali è possibile creare, modificare ed eliminare utenti direttamente.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gestione di utenti e licenze nelle distribuzioni online

Nelle versioni online di [!INCLUDE[prod_short](includes/prod_short.md)] il numero di utenti è definito dalla sottoscrizione e viene aggiunto al proprio tenant nel Centro per i partner Microsoft, in genere dal partner Microsoft. Per ulteriori informazioni, vedere [Aggiungere un nuovo cliente](/partner-center/add-a-new-customer) e [Creare, sospendere o annullare le sottoscrizioni dei clienti](/partner-center/create-a-new-subscription) nella guida del Centro per i partner Microsoft.

Per definire chi può accedere a [!INCLUDE[prod_short](includes/prod_short.md)], devi assegnare le licenze del prodotto agli utenti in base ai ruoli di cui dispongono in [!INCLUDE[prod_short](includes/prod_short.md)]. Ecco i modi in cui può essere eseguito:

- L'amministratore di Microsoft 365 della società può eseguire questa operazione nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com). Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Microsoft 365](https://aka.ms/CreateOffice365Users).  
- Un partner Microsoft può assegnare licenze nell'interfaccia di amministrazione di Microsoft 365 o nel Centro per i partner di Microsoft. Per ulteriori informazioni, vedere [Attività di gestione degli utenti per gli account dei clienti](/partner-center/assign-licenses-to-users) nella Guida del Centro per i partner Microsoft.

Per ulteriori informazioni, vedere [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) nella Guida per amministratori.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central
Dopo aver aggiunto utenti o modificato le informazioni utente nell'interfaccia di amministrazione di Microsoft 365, è possibile importare rapidamente le informazioni utente in [!INCLUDE[prod_short](includes/prod_short.md)]. Ciò include le assegnazioni della licenza. 

1. Accedere a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando come account amministratore.
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.  
3. Scegliere **Aggiorna utenti da Office 365**.

Se si aggiungono nuovi utenti, il passaggio successivo consiste nell'assegnare gruppi di utenti e autorizzazioni. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md). Se si stanno aggiornando le informazioni utente e l'aggiornamento include una modifica della licenza, gli utenti verranno assegnati al gruppo di utenti appropriato e i relativi set di autorizzazioni verranno aggiornati. Per ulteriori informazioni, vedere [Per gestire le autorizzazioni tramite gruppo di utenti](ui-define-granular-permissions.md).  

> [!NOTE]
> A tutti gli utenti deve essere assegnata la stessa licenza: Essential o Premium. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Per altre informazioni sulla sincronizzazione delle informazioni utente con Microsoft 365, vedere la sezione [Sincronizzazione con Microsoft 365](#m365).

> [!NOTE]
> Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a Business Central in modo che possa utilizzare i dati fiscali dell'azienda. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Per rimuovere l'accesso di un utente al sistema

Nelle distribuzioni online, è possibile rimuovere l'accesso di un utente a [!INCLUDE[prod_short](includes/prod_short.md)]. Tutti i riferimenti all'utente vengono conservati, ma l'utente non può accedere e le sessioni attive per l'utente vengono interrotte.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Aprire la pagina **Scheda utente** per l'utente pertinente, quindi nel campo **Stato** selezionare **Disabilitato**.
3. Per consentire nuovamente l'accesso all'utente, impostare il campo **Stato** su **Abilitato**.

Puoi anche rimuovere la licenza da un utente nell'interfaccia di amministrazione di Microsoft 365. L'utente non può quindi eseguire l'accesso. Per ulteriori informazioni, vedere [Rimuovere le licenze agli utenti](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Sincronizzazione con Microsoft 365

Quando si assegna una licenza a un utente per [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft 365, vi sono due modi per creare l'utente in [!INCLUDE[prod_short](includes/prod_short.md)].  

- L'amministratore può aggiungere l'utente scegliendo l'azione **Aggiorna utenti da Office 365** nella pagina **Utenti** come descritto nella sezione [Per aggiungere un utente o aggiornare le informazioni sull'utente in Business Central](#adduser).
- Le informazioni sulla licenza si aggiorneranno automaticamente quando l'utente accede per la prima volta.

In entrambi i casi, vengono automaticamente eseguite alcune impostazioni. Queste sono elencate nella seconda e terza colonna nella tabella seguente.

Se si modificano le informazioni dell'utente in Microsoft 365, è possibile aggiornare [!INCLUDE[prod_short](includes/prod_short.md)] in modo da riflettere la modifica. A seconda di ciò che si desidera aggiornare, utilizzare una delle azioni della pagina **Utenti**. Le azioni sono descritte nelle ultime tre colonne nella tabella seguente.

> [!NOTE]
> Le azioni descritte nella tabella seguente sono accurate, tuttavia l'unica necessaria è **Aggiorna utenti da Office 365**, che è stata aggiunta per semplificare il processo. Le altre azioni verranno rimosse in una versione futura di [!INCLUDE[prod_short](includes/prod_short.md)].

|Cosa succede quando:|Primo utente, primo accesso|Ottieni utenti da Microsoft 365|Aggiorna utenti da Microsoft 365|Ripristina gruppi di utenti di default dell'utente|Aggiorna i gruppi di utenti|Aggiorna informazioni utente da Microsoft 365|
|-|-|-|-|-|-|-|
|Ambito:|Utente corrente|Nuovi utenti in Microsoft 365|Più utenti selezionati|Singolo utente selezionato (tranne quello corrente)|Più utenti selezionati|Più utenti selezionati|
|Creare il nuovo utente e assegnare il set di autorizzazioni SUPER.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Aggiornare l'utente in base alle informazioni in Microsoft 365: Stato, Nome completo, Email contatto, Indirizzo e-mail di autenticazione.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Sincronizzare piani utente (licenze) con licenze e ruoli assegnati in Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Aggiungere l'utente a gruppi di utenti in base ai piani utente correnti. Rimuovere il set di autorizzazioni SUPER per tutti gli utenti diversi dal primo utente che accede e gli [amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Almeno un'autorizzazione SUPER è obbligatoria.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Rimuove le autorizzazioni e i gruppi di utenti assegnati manualmente.|**X**<br /><br />Aggiorna le assegnazioni di gruppi di utenti.| |

## <a name="the-device-license"></a>Licenza per dispositivo

La licenza del dispositivo Dynamics 365 Business Central consente a più utenti di utilizzare contemporaneamente un dispositivo coperto dalla licenza. Ad esempio, potrebbe trattarsi di un dispositivo per un punto vendita, un'officina o un magazzino. Dopo aver acquistato un numero certo numero di licenze per dispositivo, fino al tale numero di utenti assegnati al Utenti del dispositivo Dynamics 365 Business Central possono accedere contemporaneamente. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Il partner Microsoft o l'amministratore Microsoft 365 della società può creare il gruppo Utenti del dispositivo Dynamics 365 Business Central e aggiungere gli utenti del dispositivo come membri nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com/) o sul [portale di Azure](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Limitazioni dell'utente del dispositivo

Gli utenti con licenza per dispositivo non possono eseguire le seguenti attività in [!INCLUDE[prod_short](includes/prod_short.md)]:

- Impostare i processi da eseguire come attività pianificate nella coda processi. Gli utenti del dispositivo sono utenti simultanei e, pertanto, non è possibile garantire che l'utente interessato sia presente nel sistema quando viene eseguita un'attività richiesta.

- L'utente del dispositivo non può essere il primo utente ad effettuare l'accesso. Un utente di tipo Amministratore, Utente completo o Contabile esterno deve essere il primo utente ad accedere per poter impostare [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) nella Guida per amministratori.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Per creare un gruppo di utenti del dispositivo Dynamics 365 Business Central

1. Nell'interfaccia di amministrazione di Microsoft 365, andare alla pagina **Gruppi**.
2. Scegliere l'azione **Aggiungi un gruppo**.
3. Nella pagina **Scegli un tipo di gruppo** scegliere l'opzione **Sicurezza** quindi scegliere l'azione **Aggiungi**.
4. Nella pagina **Nozioni di base**, immetti **Utenti del dispositivo Dynamics 365 Business Central** come nome del gruppo.
  
   >[!NOTE]
   >Il nome del gruppo deve essere scritto in inglese esattamente come mostrato nel passaggio 4, anche se si utilizza un'altra lingua.
5. Selezionare il pulsante **Chiudi**.

> [!NOTE]
> È anche possibile creare un gruppo di tipo Microsoft 365. Per ulteriori informazioni, vedere [Confrontare i gruppi](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Per aggiungere i membri al gruppo

1. Nell'interfaccia di amministrazione di Microsoft 365, aggiornare la pagina **Gruppi** in modo che venga visualizzato il nuovo gruppo.
2. Selezionare il gruppo **Dynamics 365 Business Central Device Users**, quindi scegliere l'azione **Visualizza tutto e gestisci i membri**.
3. Scegliere l'azione **Aggiungi membri**.
4. Scegliere gli utenti che si intendono aggiungere, quindi scegliere il pulsante **Salva**.
5. Scegliere il pulsante **Chiudi** tre volte.

È possibile aggiungere tutti gli utenti necessari al gruppo Dynamics 365 Business Central Device Users. Tuttavia, il numero di dispositivi a cui gli utenti possono accedere contemporaneamente è definito dal numero di licenze per dispositivo acquistate.

> [!NOTE]
> Non è necessario assegnare una licenza [!INCLUDE[prod_short](includes/prod_short.md)] agli utenti membri del gruppo Dynamics 365 Business Central Device Users.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gestione di utenti e licenze nelle distribuzioni locali

Per le distribuzioni locali, nel file di licenza (.flf) è specificato il numero di licenze utente. Quando un amministratore o il partner Microsoft carica il file di licenza, l'amministratore può specificare quali utenti possono accedere a [!INCLUDE[prod_short](includes/prod_short.md)].

Per le distribuzioni locali, l'amministratore crea, modifica ed elimina gli utenti direttamente dalla pagina **Utenti**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Per modificare o eliminare un utente in una distribuzione locale

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
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
[Preparazione al business](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Aggiungere utenti a Microsoft 365 per le aziende](https://aka.ms/CreateOffice365Users)  
[Sicurezza e protezione in Business Central (contenuto per amministratori)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]