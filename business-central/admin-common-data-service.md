---
title: Utilizzo di Microsoft Dataverse
description: Introduzione su come integrare e utilizzare Microsoft Dataverse e i relativi componenti per connettersi ad altre applicazioni Dynamics 365.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 06/14/2021
---

# Integrazione con Microsoft Dataverse

Le app aziendali utilizzano spesso dati provenienti da più di un'origine. [!INCLUDE[prod_short](includes/cds_long_md.md)] combina i dati in un unico set di logica che semplifica la connessione di altre applicazioni Dynamics 365, ad esempio [!INCLUDE[crm_md](includes/crm_md.md)] o la tua applicazione basata su [!INCLUDE[prod_short](includes/cds_long_md.md)], per [!INCLUDE[prod_short_md](includes/prod_short.md)]. Per altre informazioni su [!INCLUDE[prod_short](includes/cds_long_md.md)], vedi [Cos'è Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)

I passaggi seguenti forniscono una panoramica delle operazioni per l'integrazione di [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)]integrare.

> [!Note]  
> Queste task richiedono il ruolo di sicurezza **Amministratore di sistema** in [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Assegnare licenze per [!INCLUDE[prod_short](includes/cds_long_md.md)] agli utenti [!INCLUDE[prod_short](includes/prod_short.md)] che utilizzeranno le app integrate.

2. Impostare una connessione a [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ulteriori informazioni, vedere [Connettersi a Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Sincronizzazione i dati tra le app. Per ulteriori informazioni, vedere [Sincronizzazione di Business Central e Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Introduzione a [!INCLUDE[prod_short](includes/cds_long_md.md)]

Per iniziare con [!INCLUDE[prod_short](includes/cds_long_md.md)] avrai bisogno di un account Microsoft Power Apps. Se non hai già un account Power Apps, puoi ottenerne uno gratuitamente visitando [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) e scegliendo il collegamento **Inizia gratis**. Per saperne di più su come iniziare con [!INCLUDE[prod_short](includes/cds_long_md.md)], vedere il modulo [Introduzione a Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) del training Microsoft.

## Sincronizzazione dei dati bidirezionale o unidirezionale

A seconda delle esigenze aziendali, puoi configurare l'integrazione per sincronizzare i dati da o verso un'app aziendale di Dynamics 365 a un'altra, o in entrambe le direzioni in tempo quasi reale tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ad esempio, se si integra [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] tramite [!INCLUDE[prod_short](includes/cds_long_md.md)], un venditore può creare un ordine cliente in [!INCLUDE[crm_md](includes/crm_md.md)] e l'ordine verrà sincronizzato con [!INCLUDE[prod_short](includes/prod_short.md)]. Al contrario, da [!INCLUDE[crm_md](includes/crm_md.md)], il venditore può visualizzare le informazioni da [!INCLUDE[prod_short](includes/prod_short.md)] sulla disponibilità dell'articolo nell'ordine. 

## Entità standard e personalizzate

[!INCLUDE[prod_short](includes/cds_long_md.md)] archivia in modo sicuro i dati in un set di tabelle, che sono insiemi di record simili a come una tabella archivia i dati all'interno di un database. [!INCLUDE[prod_short](includes/cds_long_md.md)] include un set di base di tabelle standard che coprono scenari tipici, ma puoi anche creare tabelle personalizzate specifiche per la tua organizzazione. In [!INCLUDE[prod_short](includes/prod_short.md)], puoi visualizzare le tabelle standard e personalizzate sincronizzate nella pagina Mapping tabella integrazione.

## Informazioni sulla soluzione di integrazione di base di Business Central

La soluzione di integrazione di base è un componente chiave dell'integrazione. La soluzione aggiunge i ruoli obbligatori e i livelli di accesso agli account utente per l'integrazione e crea tabelle necessarie per mappare la società [!INCLUDE[prod_short](includes/prod_short.md)] a unità di business in [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Per impostazione predefinita, la guida al setup assistito **Configurare la connessione [!INCLUDE[prod_short](includes/cds_long_md.md)]** importerà la soluzione. A questo proposito, la guida al setup utilizza un account utente amministratore specificato. Questo account deve essere un utente valido in [!INCLUDE[prod_short](includes/cds_long_md.md)] con il ruolo di sicurezza seguenti:

* Amministratore di sistema  

Per ulteriori informazioni, vedere [Impostazione di account utente per l'integrazione con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) e [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

L'account amministratore viene utilizzato solo una volta durante la configurazione per le modifiche alla configurazione apportate dalla soluzione di integrazione di base in [!INCLUDE[prod_short](includes/cds_long_md.md)]. Dopo che la soluzione viene importata l'account non è più necessario. L'integrazione continuerà a utilizzare l'account utente automaticamente creato specificatamente per integrazione.

Oltre alla personalizzazione di [!INCLUDE[prod_short](includes/cds_long_md.md)], la soluzione di integrazione crea anche i seguenti ruoli in [!INCLUDE[prod_short](includes/cds_long_md.md)] per l'integrazione:

* **Amministratore di integrazione** - Consente agli utenti di gestire la connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)]. Assegnato in genere solo all'account utente automaticamente creato per la sincronizzazione.  
* **Utente integrazione** - Consente agli utenti di accedere ai dati sincronizzati. Assegnato in genere all'account utente automaticamente creato per la sincronizzazione e altri utenti che devono visualizzare o accedere ai dati sincronizzati.

Per dettagli su ciascun ruolo, come le autorizzazioni e i livelli di accesso, vedere [Impostazione di account utente per l'integrazione con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Durante la configurazione della connessione, vengono creati i mapping della tabella di integrazione necessari per sincronizzare i dati. Le entità in [!INCLUDE[prod_short](includes/cds_long_md.md)] vengono mappate a tabelle e campi di tabella in Business Central tramite tabelle di integrazione. Per ulteriori informazioni, vedere [Mapping delle entità standard per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Vedi il relativo [training Microsoft](/training/modules/use-model-driven-apps-common-data-service/)

## Vedere anche

[Modelli di proprietà dei dati](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
