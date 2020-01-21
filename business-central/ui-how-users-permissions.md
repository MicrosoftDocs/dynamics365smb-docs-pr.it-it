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
ms.date: 01/06/2020
ms.author: sgroespe
ms.openlocfilehash: b9fbf0b2793c6239f3a1a416230d4afb17bdb5c6
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943235"
---
# <a name="create-users-according-to-licenses"></a>Creare utenti in base alle licenze
Di seguito viene descritto in che modo gli amministratori possono creare utenti e definire chi può accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] e vengono indicati i diritti fondamentali di cui dispongono diversi i tipi di utenti in base alle licenze.

Quando gli utenti vengono creati in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile continuare ad assegnare autorizzazioni specifiche agli utenti tramite set di autorizzazioni e organizzare gli utenti in gruppi di utenti per una facile gestione delle autorizzazioni. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

> [!NOTE]
> Il processo di gestione degli utenti e delle licenze a seconda che la soluzione sia distribuita online o locale. Nelle distribuzioni online è ad esempio possibile disabilitare e abilitare un utente solo una volta aggiunto a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nelle distribuzioni locali è possibile creare, modificare ed eliminare utenti.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gestione di utenti e licenze nelle distribuzioni online
In [!INCLUDE[d365fin](includes/d365fin_md.md)] online il numero di utenti è definito dalla sottoscrizione e viene aggiunto al proprio tenant nel Centro per i partner Microsoft, in genere dal partner Microsoft. Per ulteriori informazioni, vedere [Aggiungere un nuovo cliente](https://docs.microsoft.com/partner-center/add-a-new-customer) e [Creare, sospendere o annullare le sottoscrizioni dei clienti](https://docs.microsoft.com/partner-center/create-a-new-subscription) nella guida del Centro per i partner Microsoft.

Per definire chi può accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)], le licenze del prodotto devono essere assegnate agli utenti in base ai ruoli di cui dispongono in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ecco i modi in cui può essere eseguito:
- L'amministratore di Office 365 della società può eseguire questa operazione nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com). Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Office 365](https://aka.ms/CreateOffice365Users).  
- Un partner Microsoft può assegnare licenze nell'interfaccia di amministrazione di Microsoft 365 o nel Centro per i partner di Microsoft. Per ulteriori informazioni, vedere [Attività di gestione degli utenti per gli account dei clienti](https://docs.microsoft.com/partner-center/assign-licenses-to-users) nella guida del Centro per i partner Microsoft.

Per ulteriori informazioni, vedere [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) nella guida per sviluppatori e ITPro.

Quando gli utenti con una licenza [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono creati in Office 365, è possibile importarli nella pagina **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando l'azione **Ottieni nuovi utenti da Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Per aggiungere un utente in Business Central
Per aggiungere utenti dall'Interfaccia di amministrazione di Microsoft 365 a [!INCLUDE[d365fin](includes/d365fin_md.md)] online, si utilizza una funzione di importazione dedicata.  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Ottieni nuovi utenti da Office 365**.

Ogni nuovo utente che è stato creato per la sottoscrizione a Office 365 verrà aggiunto nella pagina **Utenti**. Agli utenti vengono assegnati set di autorizzazioni in base alla licenza assegnata all'utente in Office 365. È quindi possibile procedere con l'assegnazione agli utenti di autorizzazioni più dettagliate e con la relativa organizzazione in gruppi di utenti per una facile gestione delle autorizzazioni. Per ulteriori informazioni, vedere [Per assegnare set di autorizzazioni agli utenti](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Se viene utilizzato un contabile esterno per gestire i libri contabili e i rendiconti finanziari, è possibile invitarlo a Business Central in modo che possa utilizzare i dati fiscali dell'azienda. Per ulteriori informazioni, vedere [Invitare il contabile esterno in Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Per rimuovere l'accesso di un utente al sistema
Nelle distribuzioni online è possibile rimuovere l'accesso di un utente al sistema impostando il campo **Stato** su **Disabilitato**. Tutti i riferimenti all'utente verranno mantenuti, ma l'utente non potrà più accedere al sistema e le sessioni attive per l'utente verranno interrotte.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Aprire la pagina **Scheda utente** per l'utente pertinente, quindi nel campo **Stato** selezionare **Disabilitato**.
3. Per consentire nuovamente l'accesso all'utente, impostare il campo **Stato** su **Abilitato**.

Oltre a disabilitare un utente, è possibile annullare l'assegnazione della licenza da un utente nell'interfaccia di amministrazione di Microsoft 365. L'utente non può quindi eseguire l'accesso. Per ulteriori informazioni, vedere [Annullare l'assegnazione delle licenze agli utenti](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Per modificare la licenza assegnata per un utente
In alcuni casi, potrebbe essere necessario modificare la licenza assegnata a un utente. Se si decide ad esempio di utilizzare il modulo Gestione assistenza e quindi è necessario aggiornare tutte le licenze Essential a Premium. Oppure se la responsabilità di un utente è cambiata ed è necessario sostituire una licenza per Team Member a Essential.

1. Modificare la licenza nell'interfaccia di amministrazione di Microsoft 365. Per ulteriori informazioni, vedere [Aggiungere gli utenti singolarmente o in blocco a Office 365](https://aka.ms/CreateOffice365Users).
2. Accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] come amministratore.
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
4. In alternativa, nella pagina **Utenti** scegliere l'azione **Aggiorna tutti i gruppi di utenti**.

Gli utenti verranno spostati in un gruppo di utenti appropriato e i set di autorizzazioni verranno aggiornati. Per ulteriori informazioni, vedere [Per gestire le autorizzazioni tramite gruppo di utenti](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> A tutti gli utenti regolari in una soluzione deve essere assegnata la stessa licenza: Essential o Premium.
> Per informazioni sulle licenze, vedere [Guida alle licenze di Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Sincronizzazione con Office 365
Quando una licenza viene assegnata a un utente in Office 365, vi sono due modi per creare l'utente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il sistema lo farà automaticamente quando l'utente accede per la prima volta, oppure l'amministratore può aggiungere l'utente scegliendo l'azione **Ottieni utenti da Office 365** nella pagina **Utenti**.

In entrambi i casi, vengono automaticamente eseguite alcune impostazioni aggiuntive. Queste sono elencate nella seconda e terza colonna nella tabella seguente.

Se si cambia l'utente in Office 365 successivamente ed è necessario sincronizzare le modifiche a [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile utilizzare diverse azioni nella pagina **Utenti** a seconda di cosa si desidera sincronizzare esattamente. Queste azioni sono elencate nelle ultime tre colonne nella tabella seguente.

|Cosa succede quando:|Primo accesso|Ottieni utenti da Office 365|Aggiorna utenti da Office 365|Ripristina gruppi di utenti di default dell'utente|Aggiorna i gruppi di utenti|
|-|-|-|-|-|-|
|Ambito:|Utente corrente|Nuovi utenti in Office 365|Più utenti selezionati|Singolo utente selezionato (tranne quello corrente)|Più utenti selezionati|
|Creare il nuovo utente e assegnare il set di autorizzazioni SUPER.<br /><br />Piattaforma|**X**|**X**| | | |
|Aggiornare il record utente in base alle informazioni effettive in Office 365: Stato, Nome completo, Email contatto, Indirizzo e-mail di autenticazione.<br /><br />Codeunit "Utente Azure AD Graph".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Sincronizzare piani utente (licenze) con licenze e ruoli assegnati in Office 365.<br /><br />Codeunit "Utente Azure AD Graph".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Aggiungere l'utente a gruppi di utenti in base ai piani utente correnti. Revocare il set di autorizzazioni SUPER (è necessario almeno un SUPER; non revocare da [amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration)).<br /><br />Codeunit "Gestione autorizzazioni". AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Sovrascrivi: rimuovere l'utente da altri gruppi. Rimuovere i set di autorizzazioni assegnati manualmente.|**X**<br /><br />Additivo: mantenere intatti l'iscrizione corrente al gruppo di utenti e i set di autorizzazioni assegnati. Aggiungere l'utente solo ai gruppi se necessario.|

## <a name="the-device-license"></a>Licenza per dispositivo
Con la licenza per dispositivo Dynamics 365 Business Central, più utenti possono utilizzare un dispositivo concesso in licenza per gestire un dispositivo per punto vendita, un dispositivo per officina o un dispositivo per magazzino. Per ulteriori informazioni, vedere [Guida alle licenze di Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

La licenza per dispositivo è implementata come modello per utenti simultanei. Dopo aver acquistato il numero X di licenze per dispositivo, fino al numero X di utenti dal gruppo designato chiamato Utenti del dispositivo Dynamics 365 Business Central* possono accedere contemporaneamente.

L'amministratore Office 365 della società o il partner Microsoft deve creare il gruppo di dispositivi designato e aggiungere gli utenti del dispositivo come membri del gruppo. Possono farlo nell'[interfaccia di amministrazione di Microsoft 365](https://admin.microsoft.com/) o nel [Portale di Azure](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Limitazioni dell'utente del dispositivo
Gli utenti con licenza per dispositivo non possono eseguire le seguenti attività in [!INCLUDE[d365fin](includes/d365fin_md.md)]:

-   Impostare i processi da eseguire come attività pianificate nella coda processi. Gli utenti del dispositivo sono utenti simultanei e, pertanto, non è possibile garantire che l'utente interessato sia presente nel sistema quando viene eseguita un'attività richiesta.

-   L'utente del dispositivo non può essere il primo utente a connettersi. Un utente di tipo Amministratore, Utente completo o Contabile esterno deve essere il primo utente ad accedere per poter impostare [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Amministratori](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Per creare un gruppo di utenti del dispositivo Dynamics 365 Business Central
1.  Nell'interfaccia di amministrazione di Microsoft 365, andare alla pagina **Gruppi**.
2.  Scegliere l'azione **Aggiungi un gruppo**.
3.  Nella pagina **Scegli un tipo di gruppo**, scegliere l'azione **Sicurezza** quindi scegliere l'azione **Aggiungi**.
4.  Nella pagina **Nozioni di base**, digitare *Dynamics 365 Business Central Device Users* come nome del gruppo.

    > [!Note]
    > Il nome del gruppo deve essere scritto esattamente come sopra, anche in una configurazione non inglese.
5. Selezionare il pulsante **Chiudi**.

> [!NOTE]
> È anche possibile creare un gruppo di tipo Office 365. Per ulteriori informazioni, vedere [Confrontare i gruppi](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Per aggiungere i membri al gruppo
1.  Nell'interfaccia di amministrazione di Microsoft 365, aggiornare la pagina **Gruppi** in modo che venga visualizzato il nuovo gruppo.
2.  Selezionare il gruppo **Dynamics 365 Business Central Device Users**, quindi scegliere l'azione **Visualizza tutto e gestisci i membri**.
3.  Scegliere l'azione **Aggiungi membri**.
4.  Scegliere gli utenti che si intendono aggiungere, quindi scegliere il pulsante **Salva**.
5.  Scegliere il pulsante **Chiudi** tre volte.

È possibile aggiungere tutti gli utenti necessari al gruppo Dynamics 365 Business Central Device Users. Il numero di dispositivi a cui gli utenti possono accedere contemporaneamente è definito dal numero di licenze per dispositivo acquistate.

> [!NOTE]
> Non è necessario assegnare una licenza [!INCLUDE[d365fin](includes/d365fin_md.md)] agli utenti membri del gruppo Dynamics 365 Business Central Device Users.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gestione di utenti e licenze nelle distribuzioni locali
Per le distribuzioni locali, nel file di licenza (.flf) è specificato un numero di utenti con licenza. Quando l'amministratore o il partner Microsoft carica il file di licenza, l'amministratore può specificare quali utenti possono accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per le distribuzioni locali, l'amministratore crea, modifica ed elimina gli utenti direttamente dalla pagina **Utenti**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Per modificare o eliminare un utente locale
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
2. Scegliere l'utente che si intende modificare, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda utente** modificare le informazioni come necessario.    
4. Per eliminare un utente, selezionarlo, quindi scegliere l'azione **Elimina**.

> [!NOTE]
> Per le distribuzioni locali di [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore può scegliere tra diversi meccanismi di autorizzazione delle credenziali per gli utenti. Pertanto, quando si crea un utente, fornire informazioni diverse a seconda del tipo di credenziali che si stanno utilizzando nell'istanza specifica di [!INCLUDE[server](includes/server.md)].<br /><br />
> Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella sezione Amministrazione del contenuto per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Vedere anche
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users)  
[Guida alle licenze di Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)  
[Sicurezza e protezione in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) nella Guida per sviluppatori e professionisti IT
