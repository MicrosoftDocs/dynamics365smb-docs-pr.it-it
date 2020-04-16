---
title: Utilizzo di Common Data Service
description: Introduzione a Common Data Service e i suoi componenti.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: bb21647b4cd07d4d4e2d37ae597551d9ca50d210
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196875"
---
# <a name="integrating-with-common-data-service"></a>Integrazione con Common Data Service
Le app aziendali utilizzano spesso dati provenienti da più di un'origine. [!INCLUDE[d365fin](includes/cds_long_md.md)] combina i dati in un unico set di logica che semplifica la connessione di altre applicazioni Dynamics 365, ad esempio [!INCLUDE[crm_md](includes/crm_md.md)] o la tua applicazione basata su [!INCLUDE[d365fin](includes/cds_long_md.md)], per [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Per altre informazioni su [!INCLUDE[d365fin](includes/cds_long_md.md)], vedi [Cos'è Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

I passaggi seguenti forniscono una panoramica delle operazioni per l'integrazione di [!INCLUDE[d365fin](includes/cds_long_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)]integrare.

> [!Note]  
> Queste task richiedono il ruolo di sicurezza **Amministratore di sistema** in [!INCLUDE[d365fin](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Nell'interfaccia di amministrazione di Microsoft 365, impostare un account utente per il collegamento e la sincronizzazione dei dati con [!INCLUDE[d365fin](includes/cds_long_md.md)]. Per ulteriori informazioni, vedere [Impostazione di account utente per l'integrazione con Common Data Service](admin-setting-up-integration-with-dynamics-sales.md).

2. Assegnare licenze per [!INCLUDE[d365fin](includes/cds_long_md.md)] agli utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] che utilizzeranno le app integrate.

3. Impostare una connessione a [!INCLUDE[d365fin](includes/cds_long_md.md)]. Per ulteriori informazioni, vedere [Connettersi a Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Sincronizzazione i dati tra le app. Per ulteriori informazioni, vedere [Sincronizzazione di Business Central e Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Introduzione a [!INCLUDE[d365fin](includes/cds_long_md.md)]
Per iniziare con [!INCLUDE[d365fin](includes/cds_long_md.md)] avrai bisogno di un account Microsoft Power Apps. Se non hai già un account Power Apps, puoi ottenerne uno gratuitamente visitando [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) e scegliendo il collegamento **Inizia gratis**. Per saperne di più su come iniziare con [!INCLUDE[d365fin](includes/cds_long_md.md)], vedi il modulo [Integrazione con Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) di Microsft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Sincronizzazione dei dati bidirezionale o unidirezionale
A seconda delle esigenze aziendali, puoi configurare l'integrazione per sincronizzare i dati da o verso un'app aziendale di Dynamics 365 a un'altra, o in entrambe le direzioni in tempo quasi reale tramite [!INCLUDE[d365fin](includes/cds_long_md.md)]. Ad esempio, se si integra [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] tramite [!INCLUDE[d365fin](includes/cds_long_md.md)], un venditore può creare un ordine cliente in [!INCLUDE[crm_md](includes/crm_md.md)] e l'ordine verrà sincronizzato con [!INCLUDE[d365fin](includes/d365fin_md.md)]. Al contrario, da [!INCLUDE[crm_md](includes/crm_md.md)], il venditore può visualizzare le informazioni da [!INCLUDE[d365fin](includes/d365fin_md.md)] sulla disponibilità dell'articolo nell'ordine. 

## <a name="standard-and-custom-entities"></a>Entità standard e personalizzate
[!INCLUDE[d365fin](includes/cds_long_md.md)] archivia in modo sicuro i dati in un set di entità, che sono insiemi di record simili a come una tabella archivia i dati all'interno di un database. [!INCLUDE[d365fin](includes/cds_long_md.md)] include un set di base di entità standard che coprono scenari tipici, ma puoi anche creare entità personalizzate specifiche per la tua organizzazione. In [!INCLUDE[d365fin](includes/d365fin_md.md)], puoi visualizzare le entità standard e personalizzate sincronizzate nella pagina Mapping tabella integrazione.

## <a name="about-the-base-cds-integration-solution"></a>Informazioni sulla soluzione di integrazione CDS di base
La soluzione di integrazione CDS di base è un componente chiave dell'integrazione. La soluzione aggiunge i ruoli obbligatori e i livelli di accesso agli account utente per l'integrazione e crea entità necessarie per mappare la società [!INCLUDE[d365fin](includes/d365fin_md.md)] a unità di business in [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Per impostazione predefinita, la guida al setup assistito **Configurare la connessione [!INCLUDE[d365fin](includes/cds_long_md.md)]** importerà la soluzione. A questo proposito, la guida al setup utilizza un account utente amministratore specificato. Questo account deve essere un utente valido in [!INCLUDE[d365fin](includes/cds_long_md.md)] con i ruoli di sicurezza seguenti:

* Amministratore di sistema  
* Addetto alla personalizzazione della soluzione  

Per ulteriori informazioni, vedere [Impostazione di account utente per l'integrazione con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) e [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md). 

L'account amministratore viene utilizzato solo una volta durante la configurazione a causa di modifiche alla configurazione apportate dalla soluzione CDS di base in [!INCLUDE[d365fin](includes/cds_long_md.md)]. Dopo che la soluzione viene importata l'account non è più necessario. L'integrazione continuerà a utilizzare l'account utente creato specificatamente per integrazione.

Oltre alla personalizzazione di [!INCLUDE[d365fin](includes/cds_long_md.md)], la soluzione di integrazione crea anche i seguenti ruoli in [!INCLUDE[d365fin](includes/cds_long_md.md)] per l'integrazione:

* **Amministratore di integrazione** - Consente agli utenti di gestire la connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[d365fin](includes/cds_long_md.md)]. Assegnato in genere solo all'account utente per la sincronizzazione.  
* **Utente integrazione** - Consente agli utenti di accedere ai dati sincronizzati. Assegnato in genere all'account utente per la sincronizzazione e altri utenti che devono visualizzare o accedere ai dati sincronizzati.

Per dettagli su ciascun ruolo, come le autorizzazioni e i livelli di accesso, vedere [Impostazione di account utente per l'integrazione con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Durante la configurazione della connessione, vengono creati i mapping della tabella di integrazione necessari per sincronizzare i dati. Le entità in Common Data Service vengono mappate a tabelle e campi di tabella in Business Central tramite tabelle di integrazione. Per ulteriori informazioni, vedere [Mapping delle entità standard per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Vedere anche
[Modelli di proprietà dei dati](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



