---
title: Integrazione con Microsoft Dataverse tramite la sincronizzazione dei dati
description: Introduzione su come integrare e utilizzare Microsoft Dataverse e i relativi componenti per connettersi ad altre applicazioni Dynamics 365.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Integrazione con Microsoft Dataverse tramite la sincronizzazione dei dati

Le app aziendali utilizzano spesso dati provenienti da più di un'origine. [!INCLUDE[prod_short](includes/cds_long_md.md)] combina i dati in un unico set di logica che semplifica la connessione di [!INCLUDE[prod_short](includes/prod_short.md)] ad altre applicazioni Dynamics 365. Ad esempio, [!INCLUDE[crm_md](includes/crm_md.md)] o la tua applicazione basata su [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ulteriori informazioni su [!INCLUDE[prod_short](includes/cds_long_md.md)], vai a [Cos'è Dataverse?](/powerapps/maker/common-data-service/data-platform-intro).

I passaggi seguenti forniscono una panoramica delle operazioni per l'integrazione di [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)]integrare.

> [!Note]  
> Queste task richiedono il ruolo di sicurezza **Amministratore di sistema** in [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Assegnare licenze per [!INCLUDE[prod_short](includes/cds_long_md.md)] agli utenti [!INCLUDE[prod_short](includes/prod_short.md)] che utilizzeranno le app integrate.

2. Impostare una connessione a [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ulteriori informazioni, vedere [Connettersi a Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Sincronizzazione i dati tra le app. Per ulteriori informazioni, vedere [Sincronizzazione di Business Central e Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Introduzione a [!INCLUDE[prod_short](includes/cds_long_md.md)]

Per iniziare con [!INCLUDE[prod_short](includes/cds_long_md.md)] avrai bisogno di un account Microsoft Power Apps. Se non hai già un account Power Apps, puoi ottenerne uno gratuitamente visitando [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) e scegliendo il collegamento **Inizia gratis**. Per saperne di più su come iniziare con [!INCLUDE[prod_short](includes/cds_long_md.md)], vai a [Introduzione a Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) del training Microsoft.

## Sincronizzazione dei dati bidirezionale o unidirezionale

Puoi sincronizzare i dati da o verso un'app aziendale di Dynamics 365 a un'altra, o in entrambe le direzioni in tempo quasi reale tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ad esempio, se si integra [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[crm_md](includes/crm_md.md)], un venditore può creare un ordine cliente in [!INCLUDE[crm_md](includes/crm_md.md)] e l'ordine verrà sincronizzato con [!INCLUDE[prod_short](includes/prod_short.md)]. Al contrario, da [!INCLUDE[crm_md](includes/crm_md.md)], il venditore può verificare la disponibilità dell'articolo nell'ordine in [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Entità standard e personalizzate

[!INCLUDE[prod_short](includes/cds_long_md.md)] archivia in modo sicuro i dati in un set di tabelle, che sono insiemi di record simili a come una tabella archivia i dati all'interno di un database. [!INCLUDE[prod_short](includes/cds_long_md.md)] include un set di base di tabelle standard che coprono scenari tipici, ma puoi anche creare tabelle personalizzate specifiche per la tua organizzazione. In [!INCLUDE[prod_short](includes/prod_short.md)], puoi visualizzare le tabelle standard e personalizzate sincronizzate nella pagina Mapping tabella integrazione.

## Informazioni sulla soluzione di integrazione di base di Business Central

La soluzione di integrazione di base è un componente chiave dell'integrazione. La soluzione aggiunge i ruoli obbligatori e i livelli di accesso agli account utente per l'integrazione e crea tabelle necessarie per mappare la società [!INCLUDE[prod_short](includes/prod_short.md)] a unità di business in [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Per impostazione predefinita, la guida al setup assistito **Configurare la connessione [!INCLUDE[prod_short](includes/cds_long_md.md)]** importa la soluzione. A questo proposito, la guida al setup utilizza un account utente amministratore specificato. Questo account deve essere un utente valido in [!INCLUDE[prod_short](includes/cds_long_md.md)] con il ruolo di sicurezza **Amministratore di sistema**.  

Per ulteriori informazioni sugli account utente, consulta i seguenti articoli:

* [Impostazione di account utente per l'integrazione con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Creare gli utenti in Microsoft Dynamics 365 (online) e assegnare i ruoli di sicurezza](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) 

L'account amministratore viene utilizzato solo una volta durante la configurazione per le modifiche alla configurazione apportate dalla soluzione di integrazione di base in [!INCLUDE[prod_short](includes/cds_long_md.md)]. Dopo l'importazione della soluzione, l'account non è più necessario. L'integrazione continuerà a utilizzare l'account utente automaticamente creato specificatamente per integrazione.

Oltre alla personalizzazione di [!INCLUDE [cds_long_md](includes/cds_long_md.md)], la soluzione di integrazione crea anche un ruolo di sicurezza in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] per l'integrazione:

* **Integrazione Dataverse in Business Central**: consente di gestire la connessione tra [!INCLUDE [prod_short](includes/prod_short.md)] e [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Generalmente, questo ruolo è assegnato solo all'account utente automaticamente creato per la sincronizzazione. Per ulteriori informazioni su questo ruolo, vai a [Configurazione degli account utente per l'integrazione con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Durante la configurazione della connessione, crei i mapping della tabella di integrazione necessari per sincronizzare i dati. Le entità in [!INCLUDE[prod_short](includes/cds_long_md.md)] vengono mappate a tabelle e campi di tabella in [!INCLUDE [prod_short](includes/prod_short.md)] tramite tabelle di integrazione. Per ulteriori informazioni sui mapping, vai a [Mapping di entità standard per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Gestisci le differenze nelle valute di transazione locali e di base

Puoi connetterti a un ambiente [!INCLUDE[prod_short](includes/cds_long_md.md)] che ha una valuta di base diversa dalla valuta locale in [!INCLUDE[prod_short](includes/prod_short.md)]. Puoi effettuare la connessione in [!INCLUDE[prod_short](includes/prod_short.md)] nella pagina **Configurazione connessione Dataverse** o utilizzando la guida alla configurazione assistita **Configura connessione a Dataverse**.

Per poterti connettere, assicurati che l'impostazione della valuta della transazione di base in [!INCLUDE[prod_short](includes/cds_long_md.md)] abbia la valuta impostata nella pagina **Valute** in [!INCLUDE [prod_short](includes/prod_short.md)] e almeno un tasso di cambio è specificato per la valuta nella pagina **Tassi di cambio valuta**.

Ecco un esempio. Ti stai collegando [!INCLUDE[prod_short](includes/cds_long_md.md)] con l'euro (EUR) impostato come valuta locale nella pagina **Configurazione registro generale** a un ambiente [!INCLUDE[prod_short](includes/cds_long_md.md)]  con una valuta di transazione di base impostata su dollaro USA (USD). Dovrai avere USD nella pagina **Valute** in [!INCLUDE [prod_short](includes/prod_short.md)] e il tasso di cambio appropriato. 

Quando abiliti la connessione a [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE [prod_short](includes/prod_short.md)] aggiunge la sua valuta locale all'entità **Valuta** in [!INCLUDE[prod_short](includes/cds_long_md.md)] con il tasso di cambio del campo **Fattore valuta** nella pagina **Tassi di cambio valuta**.

La sincronizzazione della valuta è unidirezionale, da [!INCLUDE [prod_short](includes/prod_short.md)] a [!INCLUDE [!INCLUDE[prod_short](includes/cds_long_md.md)], gli importi monetari vengono convertiti e sincronizzati come segue:

* Gli importi nella valuta di base [!INCLUDE[prod_short](includes/cds_long_md.md)] vengono convertiti nella valuta locale [!INCLUDE [prod_short](includes/prod_short.md)] in base all'ultimo tasso di cambio sincronizzato da [!INCLUDE [prod_short](includes/prod_short.md)].
* Gli importi nella valuta locale [!INCLUDE [prod_short](includes/prod_short.md)] si sincronizzano con la valuta locale [!INCLUDE [prod_short](includes/prod_short.md)] in una delle altre valute (non di base) in [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Vedere anche

[Modelli di proprietà dei dati](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
