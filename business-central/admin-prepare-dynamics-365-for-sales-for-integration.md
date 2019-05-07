---
title: Integrazione con Dynamics 365 for Sales| Microsoft Docs
description: Ottenere informazioni per prepararsi all'integrazione di Dynamics 365 Business Central con Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 991d8432c24b1963da019e3c8b665f9ad009d077
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "940227"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Integrazione con Dynamics 365 for Sales
Il ruolo di agente è spesso considerato come rivolto verso l'esterno in un'azienda. Tuttavia, può essere utile per gli agenti essere in grado di guardare dentro l'azienda e di osservare ciò che avviene nel back end. L'integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] fornire agli agenti tale possibilità consentendo agli stessi di visualizzare informazioni in [!INCLUDE[d365fin](includes/d365fin_md.md)] mentre lavorano in [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, durante la preparazione di un'offerta di vendita può essere utile sapere se si dispone di giacenza sufficiente per soddisfare l'ordine. Per ulteriori informazioni, vedere [Utilizzo di Dynamics 365 for Sales da Business Central](marketing-integrate-dynamicscrm.md).

> [!Note]
> Questi passaggi descrivono il processo Integrazione online delle versioni di [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Panoramica del processo di integrazione
I passaggi seguenti forniscono una panoramica delle operazioni per l'integrazione di [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)]integrare.

> [!Note]  
> Queste task richiedono il ruolo di sicurezza **Amministratore di sistema** in [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Nell'interfaccia di amministrazione di Office 365, impostare un account utente per il collegamento e la sincronizzazione dei dati con [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Impostazione dell'integrazione con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Assegnare licenze per [!INCLUDE[crm_md](includes/crm_md.md)] agli utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] che utilizzeranno le app integrate.

3. Impostare una connessione a [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Impostare una connessione a Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Facoltativo: associare i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md).

5. Sincronizzazione i dati tra le app. Per ulteriori informazioni, vedere [Sincronizzazione di Business Central e Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Informazioni sulla soluzione di integrazione di Business Central
La soluzione consente al personale di visualizzare informazioni in [!INCLUDE[d365fin](includes/d365fin_md.md)] mentre lavorano in [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, può fornire una panoramica delle statistiche dei clienti, consentendo agli utenti di associare e visualizzare record in [!INCLUDE[crm_md](includes/crm_md.md)] da [!INCLUDE[d365fin](includes/d365fin_md.md)] e consente di determinare quali prodotti sono disponibili in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per impostazione predefinita, la guida al setup assistito Impostazione della connessione di Dynamics 365 for Sales importerà la soluzione di integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]. A questo proposito, la guida al setup utilizza un account utente amministratore. Questo account deve inoltre essere un utente valido in [!INCLUDE[crm_md](includes/crm_md.md)] con i ruoli di sicurezza seguenti:

* Amministratore di sistema  
* Addetto alla personalizzazione della soluzione  

Per ulteriori informazioni, vedere, [Impostazione di account utente per l'integrazione con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md) e [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).  

Questo account viene utilizzato solamente una volta durante il setup. Dopo che la soluzione viene importata in [!INCLUDE[d365fin](includes/d365fin_md.md)]l'account non è più necessario. L'integrazione continuerà a utilizzare l'account utente creato specificatamente per integrazione.

Oltre alla personalizzazione di [!INCLUDE[crm_md](includes/crm_md.md)], la soluzione di integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] crea anche i seguenti ruoli in [!INCLUDE[crm_md](includes/crm_md.md)] per l'integrazione:

* **Amministratore di integrazione** - Consente agli utenti di gestire la connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)]. Assegnato in genere solo all'account utente per la sincronizzazione.  
* **Utente integrazione** - Consente agli utenti di accedere ai dati sincronizzati. Assegnato in genere all'account utente per la sincronizzazione e qualsiasi altro utente che deve visualizzare o accedere ai dati sincronizzati.
* **Utente disponibilità prodotto** - Consente agli utenti di richiedere la disponibilità dei prodotti in [!INCLUDE[d365fin](includes/d365fin_md.md)] da [!INCLUDE[crm_md](includes/crm_md.md)].

Alla fine della guida al setup, [!INCLUDE[d365fin](includes/d365fin_md.md)] richiede di associare gli agenti agli utenti in [!INCLUDE[crm_md](includes/crm_md.md)]. I record in [!INCLUDE[crm_md](includes/crm_md.md)] in genere hanno un proprietario (utente) a cui sono assegnati e se l'associazione tra l'utente in [!INCLUDE[crm_md](includes/crm_md.md)] e l'agente in [!INCLUDE[d365fin](includes/d365fin_md.md)] non esiste, la sincronizzazione non riuscirà. Questa operazione può anche essere eseguita in seguito utilizzando l'azione **Associa agenti** nella pagina **Setup connessione Microsoft Dynamics 365**.

## <a name="see-also"></a>Vedere anche  
[Impostazione di account utente per l'integrazione con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Impostare una connessione a Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)
[Sincronizzazione di Business Central e Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)
