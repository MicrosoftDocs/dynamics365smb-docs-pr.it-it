---
title: Gestire utenti e ruoli | Microsoft Docs
description: Informazioni su come gestire utenti e Gestioni ruolo utente in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245811"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Informazioni su utenti, profili e Gestioni ruolo utente

In [!INCLUDE[d365fin](includes/d365fin_md.md)], gli utenti vengono aggiunti da un amministratore che concede anche l'accesso per gli utenti alle aree di [!INCLUDE[d365fin](includes/d365fin_md.md)] necessarie per il loro lavoro.  

L'accesso alle funzionalità è gestito tramite *gruppi utente* e *profili*. In qualità di amministratore, è possibile rimuovere utenti nell'ambito della sottoscrizione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e assegnare le autorizzazioni utente nei gruppi utente.  

## <a name="adding-users"></a>Aggiunta di utenti

Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users).

Quindi, l'amministratore può assegnare le autorizzazioni a ciascun utente e ai gruppi utente. Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).  

Le autorizzazioni più efficaci che un utente può avere è il set di autorizzazioni SUPER. Ogni società deve avere almeno un utente con tale set di autorizzazioni, ma la procedura ottimale consiste nell'assegnare a ogni utente soltanto le autorizzazioni necessarie alle loro esigenze lavorative in [!INCLUDE[prodshort](includes/prodshort.md)]. Ad esempio, ciò consente di accertare che gli utenti hanno accesso solo ai dati pertinenti al loro lavoro.  

> [!TIP]
> È una procedura ottimale assicurare che anche l'amministratore Office 365 disponga del set di autorizzazioni SUPER in [!INCLUDE[prodshort](includes/prodshort.md)] in quanto ciò semplifica molte attività amministrative, inclusa la configurazione dell'integrazione con altre app.

### <a name="users-of-on-premises-deployments"></a>Utenti di distribuzioni locali

Per le distribuzioni locali di [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore può scegliere tra diversi meccanismi di autorizzazione delle credenziali per gli utenti. Pertanto, quando si crea un utente, fornire informazioni diverse a seconda del tipo di credenziali che si stanno utilizzando nell'istanza specifica di [!INCLUDE[server](includes/server.md)]. Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella sezione Amministrazione del contenuto per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profili

A tutte le persone nella società che hanno accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] viene assegnato un *profilo* che consente l'utilizzo di una *Gestione ruolo utente*.

I profili sono raccolte di utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] che condividono la stessa Gestione ruolo utente. Gestione ruolo utente è il punto di ingresso e la home page per [!INCLUDE[d365fin](includes/d365fin_md.md)] che offre rapido accesso alle attività più importanti e visualizza diverse informazioni approfondite e indicatori di prestazioni chiave (KPI) sul proprio lavoro.  

> [!NOTE]  
>  Nella versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] online, non è possibile aggiungere, modificare o eliminare profili.  

### <a name="CreateProfile"></a>Creare un profilo

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Lista profili**, quindi scegliere il collegamento correlato.  

2.  Nella pagina **Lista profili**, scegliere l'azione **Nuovo** per aprire la pagina **Scheda Nuovo profilo**.  

3.  Nel campo **ID profilo** immettere un nome che descriva il ruolo previsto degli utenti.  

4.  Nel campo **Descrizione** immettere una descrizione dell'ID profilo, ad esempio **Gestore ordini**.  

5.  Impostare il campo **ID Gestione ruolo utente** nella Gestione ruolo utente che si intende assegnare al profilo.  

La procedura per modificare un profilo esistente è identica, tranne che si seleziona un profilo esistente nella pagina **Lista profili** invece di scegliere l'azione **Nuovo**.  


### <a name="copy-a-profile"></a>Copia di un profilo
La copia di un profilo consente di risparmiare tempo se si desidera utilizzare impostazioni simili in un profilo e si desidera soltanto modificare poche impostazioni.

1.  Aprire il profilo che si desidera copiare, quindi scegliere l'azione **Copia profilo**.

2.  Nel campo **Nuovo ID profilo** immettere un nome per il profilo che si desidera copiare.

3.  Impostare il campo **Nuovo ambito profilo** su una delle seguenti opzioni:

    - **Sistema** per rendere il nuovo profilo disponibile a tutti i database del tenant che utilizzano l'applicazione.
    - **Tenant** per rendere il nuovo profilo disponibile solo al database del tenant corrente.
4. Al termine, scegliere il pulsante **OK**.

### <a name="ExportImportProfile"></a>Importazione ed esportazione di profili

È possibile esportare e importare i profili come file XML a e da un database [!INCLUDE[d365fin](includes/d365fin_md.md)]. L'esportazione e l'importazione di un profilo consentono di risparmiare tempo quando si configura l'interfaccia utente perché si riutilizza una configurazione di profilo esistente anziché dover configurare un profilo da zero. Se si dispone di un profilo configurato in un database [!INCLUDE[d365fin](includes/d365fin_md.md)] e si desidera riutilizzare tutte o alcune delle stesse configurazioni del profilo in un database diverso, è possibile esportare il profilo in un file XML. Quindi, è possibile importare il file XML del profilo nel secondo database.

-   Per esportare un profilo, è possibile scegliere l'azione **Esporta profili** nella pagina **Lista profili** o **Scheda profilo** oppure cercare e aprire la pagina **Esporta profili**. Salvare il file XML in un'ubicazione sul computer o sulla rete.

-   Per importare un profilo, è possibile scegliere l'azione **Importa profilo** nella pagina **Lista profili** oppure cercare e aprire la pagina **Importa profili**. 

    > [!NOTE]  
    >  Non è possibile importare un profilo già esistente nel database, anche se il file XML è denominato in modo diverso o ha un contenuto diverso. È necessario eliminare il profilo esistente prima di importare quello nuovo.


## <a name="configuration-and-personalization"></a>Configurazione e personalizzazione
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Gli utenti possono personalizzare l'interfaccia utente della versione personale personalizzando l'interfaccia utente con le proprie credenziali di accesso. Questa personalizzazione può essere eliminata dall'amministratore. Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).  

## <a name="see-also"></a>Vedi anche  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)  
[Gestione della personalizzazione come amministratore](ui-personalization-manage.md)  
[Personalizzazione dell'area di lavoro](ui-personalization-user.md)  
