---
title: Assegnare o modificare autorizzazioni utente | Documenti di Microsoft
description: Descrive come aggiungere utenti di Office 365 a Business Central e quindi assegnare le autorizzazioni, i diritti di accesso e le impostazioni di protezione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7509b60a72ee520d7adcd739034e23326882daf1
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195533"
---
# <a name="create-users-according-to-licenses"></a>Creare utenti in base alle licenze
Questo argomento descrive in che modo gli amministratori possono creare utenti e definire chi può accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] e quali autorizzazioni vengono concesse ai diversi i tipi di utenti in base alle licenze.

Quando si creano utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], puoi assegnare loro autorizzazioni specifiche tramite set di autorizzazioni e organizzare gli utenti in gruppi di utenti. I gruppi di utenti semplificano la gestione delle autorizzazioni per più utenti contemporaneamente. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

> [!NOTE]
> Il processo di gestione degli utenti e delle licenze varia a seconda che la soluzione [!INCLUDE[d365fin](includes/d365fin_md.md)] sia distribuita online o in locale. Ad esempio, nelle distribuzioni online, è possibile gestire gli utenti solo dopo che sono stati aggiunti a [!INCLUDE[d365fin](includes/d365fin_md.md)] da Office 365. Nelle distribuzioni locali è possibile creare, modificare ed eliminare utenti direttamente.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gestione di utenti e licenze nelle distribuzioni online
Nelle versioni online di [!INCLUDE[d365fin](includes/d365fin_md.md)] il numero di utenti è definito dalla sottoscrizione e viene aggiunto al proprio tenant nel Centro per i partner Microsoft, in genere dal partner Microsoft. Per ulteriori informazioni, vedere [Aggiungere un nuovo cliente](https://docs.microsoft.com/partner-center/add-a-new-customer) e [Creare, sospendere o annullare le sottoscrizioni dei clienti](https://docs.microsoft.com/partner-center/create-a-new-subscription) nella guida del Centro per i partner Microsoft.

Per definire chi può accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)], devi assegnare le licenze del prodotto agli utenti in base ai ruoli di cui dispongono in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ecco i modi in cui può essere eseguito:
- L'amministratore di Office 365 della società può eseguire questa operazione nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com). Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Office 365](https://aka.ms/CreateOffice365Users).  
- Un partner Microsoft può assegnare licenze nell'interfaccia di amministrazione di Microsoft 365 o nel Centro per i partner di Microsoft. Per ulteriori informazioni, vedere [Attività di gestione degli utenti per gli account dei clienti](https://docs.microsoft.com/partner-center/assign-licenses-to-users) nella guida del Centro per i partner Microsoft.

Per ulteriori informazioni, vedere [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) nella guida per sviluppatori e IT-Pro.

Quando agli utenti viene assegnata una licenza [!INCLUDE[d365fin](includes/d365fin_md.md)] in Office 365, puoi importarli nella pagina **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando l'azione **Ottieni nuovi utenti da Office 365**.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Per aggiungere un utente o aggiornare le informazioni dell'utente in Business Central
Utilizza funzioni di importazione dedicate per aggiungere nuovi utenti o aggiornare le informazioni dell'utente in [!INCLUDE[d365fin](includes/d365fin_md.md)] dall'Interfaccia di amministrazione di Microsoft 365.  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. A seconda di cosa si desidera fare, scegliere l'azione **Ottieni nuovi utenti da Office 365** o **Aggiorna utenti da Office 365**.

I nuovi utenti e le informazioni dell'utente nel tuo abbonamento Office 365 verranno aggiunti nella pagina **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per altre informazioni sulla sincronizzazione delle informazioni utente con Office 365, vedi [Sincronizzazione con Office 365](ui-how-users-permissions.md#synchronization-with-office-365).

> [!NOTE]
> Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a Business Central in modo che possa utilizzare i dati fiscali dell'azienda. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Per rimuovere l'accesso di un utente al sistema
Nelle distribuzioni online, è possibile rimuovere l'accesso di un utente a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tutti i riferimenti all'utente vengono conservati, ma l'utente non può accedere e le sessioni attive per l'utente vengono interrotte.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Aprire la pagina **Scheda utente** per l'utente pertinente, quindi nel campo **Stato** selezionare **Disabilitato**.
3. Per consentire nuovamente l'accesso all'utente, impostare il campo **Stato** su **Abilitato**.

Puoi anche rimuovere la licenza da un utente nell'interfaccia di amministrazione di Microsoft 365. L'utente non può quindi eseguire l'accesso. Per ulteriori informazioni, vedere [Rimuovere le licenze agli utenti](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Per modificare la licenza assegnata per un utente
In alcuni casi, potrebbe essere necessario modificare la licenza assegnata a un utente. Se si decide ad esempio di utilizzare il modulo Gestione assistenza e quindi è necessario aggiornare tutte le licenze Essential a Premium. Oppure se la responsabilità di un utente è cambiata ed è necessario sostituire una licenza per Team Member a Essential.

1. Modificare la licenza nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Office 365](https://aka.ms/CreateOffice365Users).
2. Accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] come amministratore.
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
4. Nella pagina **Utenti** scegliere l'azione **Ripristina gruppi di utenti di default dell'utente**.

Gli utenti verranno spostati in un gruppo di utenti appropriato e i set di autorizzazioni verranno aggiornati. Per ulteriori informazioni, vedere [Per gestire le autorizzazioni tramite gruppo di utenti](ui-define-granular-permissions.md).

> [!NOTE]
> A tutti gli utenti deve essere assegnata la stessa licenza: Essential o Premium. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/).

### <a name="synchronization-with-office-365"></a>Sincronizzazione con Office 365
Quando assegni una licenza a un utente per [!INCLUDE[d365fin](includes/d365fin_md.md)] in Office 365, vi sono due modi per creare l'utente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

* L'amministratore può aggiungere l'utente selezionando l'azione **Aggiorna utenti da Office 365** nella pagina **Utenti**.
* Le informazioni sulla licenza si aggiorneranno automaticamente quando l'utente accede per la prima volta.

In entrambi i casi, vengono automaticamente eseguite alcune impostazioni. Queste sono elencate nella seconda e terza colonna nella tabella seguente.

Se si modificano le informazioni dell'utente in Office 365, puoi aggiornare [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo da riflettere la modifica. A seconda di ciò che si desidera aggiornare, utilizzare una delle azioni della pagina **Utenti**. Le azioni sono descritte nelle ultime tre colonne nella tabella seguente.

|Cosa succede quando:|Primo utente, primo accesso|Ottieni utenti da Office 365|Aggiorna utenti da Office 365|Ripristina gruppi di utenti di default dell'utente|Aggiorna i gruppi di utenti|
|-|-|-|-|-|-|
|Ambito:|Utente corrente|Nuovi utenti in Office 365|Più utenti selezionati|Singolo utente selezionato (tranne quello corrente)|Più utenti selezionati|
|Creare il nuovo utente e assegnare il set di autorizzazioni SUPER.<br /><br /><!--Platform-->|**X**|| | | |
|Aggiornare il record utente in base alle informazioni effettive in Office 365: Stato, Nome completo, Email contatto, Indirizzo e-mail di autenticazione.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Sincronizzare piani utente (licenze) con licenze e ruoli assegnati in Office 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Aggiungere l'utente a gruppi di utenti in base ai piani utente correnti. Rimuovere il set di autorizzazioni SUPER per tutti gli utenti diversi dal primo utente che accede e gli [amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Almeno un'autorizzazione SUPER è obbligatoria.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Rimuove le autorizzazioni e i gruppi di utenti assegnati manualmente.|**X**<br /><br />Aggiorna le assegnazioni di gruppi di utenti.|

## <a name="the-device-license"></a>Licenza per dispositivo
La licenza del dispositivo Dynamics 365 Business Central consente a più utenti di utilizzare contemporaneamente un dispositivo coperto dalla licenza. Ad esempio, potrebbe trattarsi di un dispositivo per un punto vendita, un'officina o un magazzino. Dopo aver acquistato un numero certo numero di licenze per dispositivo, fino al tale numero di utenti assegnati al Utenti del dispositivo Dynamics 365 Business Central possono accedere contemporaneamente. Per ulteriori informazioni, vedere Guida alle licenze di Microsoft Dynamics 365 Business Central. La guida è disponibile per il download sul sito Web di [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/).

Il partner Microsoft o l'amministratore Office 365 della tua società possono creare il gruppo Utenti del dispositivo Dynamics 365 Business Central e aggiungere gli utenti del dispositivo come membri nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com/) o sul [portale di Azure](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Limitazioni dell'utente del dispositivo
Gli utenti con licenza per dispositivo non possono eseguire le seguenti attività in [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Impostare i processi da eseguire come attività pianificate nella coda processi. Gli utenti del dispositivo sono utenti simultanei e, pertanto, non è possibile garantire che l'utente interessato sia presente nel sistema quando viene eseguita un'attività richiesta.

- L'utente del dispositivo non può essere il primo utente ad effettuare l'accesso. Un utente di tipo Amministratore, Utente completo o Contabile esterno deve essere il primo utente ad accedere per poter impostare [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Per creare un gruppo di utenti del dispositivo Dynamics 365 Business Central
1. Nell'interfaccia di amministrazione di Microsoft 365, andare alla pagina **Gruppi**.
2. Scegliere l'azione **Aggiungi un gruppo**.
3. Nella pagina **Scegli un tipo di gruppo**, scegliere l'azione **Sicurezza** quindi scegliere l'azione **Aggiungi**.
4. Nella pagina **Nozioni di base**, immetti **Utenti del dispositivo Dynamics 365 Business Central** come nome del gruppo.
  
   >[!Note]
   >Il nome del gruppo deve essere scritto in inglese esattamente come mostrato nel passaggio 4, anche se si utilizza un'altra lingua.
5. Selezionare il pulsante **Chiudi**.

> [!NOTE]
> È anche possibile creare un gruppo di tipo Office 365. Per ulteriori informazioni, vedere [Confrontare i gruppi](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Per aggiungere i membri al gruppo
1. Nell'interfaccia di amministrazione di Microsoft 365, aggiornare la pagina **Gruppi** in modo che venga visualizzato il nuovo gruppo.
2. Selezionare il gruppo **Dynamics 365 Business Central Device Users**, quindi scegliere l'azione **Visualizza tutto e gestisci i membri**.
3. Scegliere l'azione **Aggiungi membri**.
4. Scegliere gli utenti che si intendono aggiungere, quindi scegliere il pulsante **Salva**.
5. Scegliere il pulsante **Chiudi** tre volte.

È possibile aggiungere tutti gli utenti necessari al gruppo Dynamics 365 Business Central Device Users. Tuttavia, il numero di dispositivi a cui gli utenti possono accedere contemporaneamente è definito dal numero di licenze per dispositivo acquistate.

> [!NOTE]
> Non è necessario assegnare una licenza [!INCLUDE[d365fin](includes/d365fin_md.md)] agli utenti membri del gruppo Dynamics 365 Business Central Device Users.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gestione di utenti e licenze nelle distribuzioni locali
Per le distribuzioni locali, nel file di licenza (.flf) è specificato il numero di licenze utente. Quando un amministratore o il partner Microsoft carica il file di licenza, l'amministratore può specificare quali utenti possono accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per le distribuzioni locali, l'amministratore crea, modifica ed elimina gli utenti direttamente dalla pagina **Utenti**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Per modificare o eliminare un utente in una distribuzione locale
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Scegliere l'utente che si intende modificare, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda utente** modificare le informazioni come necessario.    
4. Per eliminare un utente, selezionarlo, quindi scegliere l'azione **Elimina**.

> [!NOTE]
> Per le distribuzioni locali, un amministratore può specificare come autenticare le credenziali dell'utente nell'istanza [!INCLUDE[server](includes/server.md)]. Quando si crea un utente, si fornisce il tipo di credenziale che si sta utilizzando.<br /><br />
> Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella sezione Amministrazione del contenuto per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Vedere anche
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users)  
[Sicurezza e protezione in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) nella Guida per sviluppatori e professionisti IT
