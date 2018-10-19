---
title: Gestire utenti e ruoli | Microsoft Docs
description: Informazioni su come gestire utenti e Gestioni ruolo utente in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Informazioni su utenti, profili e Gestioni ruolo utente

In [!INCLUDE[d365fin](includes/d365fin_md.md)], gli utenti vengono aggiunti da un amministratore che concede anche l'accesso per gli utenti alle aree di [!INCLUDE[d365fin](includes/d365fin_md.md)] necessarie per il loro lavoro.  

L'accesso alle funzionalità è gestito tramite *gruppi utente* e *profili*. In qualità di amministratore, è possibile rimuovere utenti nell'ambito della sottoscrizione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e assegnare le autorizzazioni utente nei gruppi utente.  

## <a name="adding-users"></a>Aggiunta di utenti

Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users).

Quindi, l'amministratore può assegnare le autorizzazioni a ciascun utente e ai gruppi utente. Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Utenti di distribuzioni locali

Per le distribuzioni locali di [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore può scegliere tra diversi meccanismi di autorizzazione delle credenziali per gli utenti. Pertanto, quando si crea un utente, fornire informazioni diverse a seconda del tipo di credenziali che si stanno utilizzando nell'istanza specifica di [!INCLUDE[server](includes/server.md)]. Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella sezione Amministrazione del contenuto per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profili

A tutte le persone nella società che hanno accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] viene assegnato un *profilo* che consente l'utilizzo di una *Gestione ruolo utente*.

I profili sono raccolte di utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] che condividono la stessa Gestione ruolo utente. Gestione ruolo utente è il punto di ingresso e la home page per [!INCLUDE[d365fin](includes/d365fin_md.md)] che offre rapido accesso alle attività più importanti e visualizza diverse informazioni approfondite e indicatori di prestazioni chiave (KPI) sul proprio lavoro.  

> [!NOTE]  
>  Nella versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] online, non è possibile aggiungere, modificare o eliminare profili.  

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

