---
title: Gestire l'accesso a Business Central
description: Gli amministratori utilizzano un approccio a più livelli per controllare l'accesso a Business Central e alle sue funzionalità.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
---

# Gestire l'accesso a Business Central

Questo articolo offre agli amministratori e agli sviluppatori di applicazioni una panoramica di alto livello su come controllare l'accesso a [!INCLUDE [prod_short](includes/prod_short.md)] e alle sue funzionalità. Utilizzare i collegamenti per accedere ad altri articoli che forniscono maggiori dettagli sugli argomenti.

## Accesso su più livelli

[!INCLUDE [prod_short](includes/prod_short.md)] utilizza un approccio a più livelli alla sicurezza delle applicazioni, come illustrato nel diagramma seguente. Per ulteriori informazioni su ogni livello, vai a [Sicurezza delle applicazioni in Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Sicurezza delle applicazioni su più livelli in Business Central.":::

## Licenze

Agli utenti di [!INCLUDE [prod_short](includes/prod_short.md)] viene assegnata una licenza **Dynamics 365 Business Central** che consente loro di visualizzare, modificare e agire sui propri dati aziendali da qualsiasi interfaccia utente. Per ulteriori informazioni sulle licenze, vai a [Licenze in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Tuttavia, le persone che occasionalmente necessitano di accesso in sola lettura alle informazioni in [!INCLUDE [prod_short](includes/prod_short.md)] possono utilizzare una licenza **Microsoft 365**. Per ulteriori informazioni sull'accesso limitato alle licenze, vai ad [Accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md).

Per ulteriori informazioni sui diversi tipi di licenze e sul funzionamento delle licenze in [!INCLUDE[prod_short](includes/prod_short.md)], [scarica la guida alle licenze di Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

## Attività di amministrazione in Business Central

La tabella seguente elenca in che modo gli amministratori possono controllare l'accesso a [!INCLUDE [prod_short](includes/prod_short.md)] e le funzionalità che verranno utilizzate dagli utenti. Alcune delle attività aiutano anche a mantenere aggiornate le impostazioni di accesso.

|Attività| Ulteriori informazioni |
|--|--|--|
|Ogni persona deve disporre di un account utente prima di poter accedere a [!INCLUDE [prod_short](includes/prod_short.md)]. Il modo più semplice per configurare gli utenti è aggiungerli uno alla volta nell'[interfaccia di amministrazione Microsoft 365](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Aggiungere utenti e assegnare licenze nello stesso tempo](/microsoft-365/admin/add-users/add-users)|
|Gestisci l'accesso per tutti gli utenti a livello di ambiente. Crea un gruppo di sicurezza Azure Active Directory (Azure AD) e assegnalo all'ambiente.<br><br> Puoi anche utilizzare i gruppi di sicurezza per gestire l'accesso per gruppi specifici di utenti. | [Gestire l'accesso agli ambienti](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Controllare l'accesso a Business Central utilizzando i gruppi di sicurezza](ui-security-groups.md) |
|Crea utenti in [!INCLUDE [prod_short](includes/prod_short.md)] e definisci chi può accedere. | [Creare utenti in base alle licenze](ui-how-users-permissions.md) |
|Le autorizzazioni definiscono a quali oggetti un utente può accedere all'interno di ogni database o ambiente, in combinazione con le licenze dell'utente. Specifica se gli utenti possono leggere, modificare o inserire dati negli oggetti di database. |[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)|
|Se un contabile esterno gestisce i tuoi libri e la rendicontazione finanziaria, invitalo nel tuo [!INCLUDE [prod_short](includes/prod_short.md)]. Potranno lavorare più da vicino con te sui tuoi dati fiscali.|[Esperienze di contabile in [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Se sei un [!INCLUDE [prod_short](includes/prod_short.md)] partner rivenditore, puoi inviare un'e-mail a un cliente per richiedere una relazione di rivenditore. È possibile includere nell'e-mail i privilegi di amministratore delegato per Azure Active Directory e Microsoft 365 .| [Accesso dell'amministratore con delega a Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Un tag di servizio di Azure rappresenta un gruppo di indirizzi IP da cui può provenire o indirizzare il traffico per un servizio. Utilizza i tag di servizio per configurare i firewall in modo da consentire il traffico solo da determinati servizi. Il tag **Dynamics365BusinessCentral** ti consente di utilizzare le regole del firewall e del gruppo di sicurezza di rete per limitare il traffico da e verso [!INCLUDE [prod_short](includes/prod_short.md)].| [Tag del servizio di sicurezza di Azure](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Quando si utilizza l'autenticazione Azure Active Directory con [!INCLUDE [prod_short](includes/prod_short.md)], si consiglia di sfruttare l'[autenticazione a più fattori di Azure AD (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). L'MFA salvaguarda ulteriormente l'accesso all'applicazione e ai dati.|[Autenticazione a più fattori per Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## Attività di Business Central per sviluppatori

C'è anche una storia di sviluppatori per la gestione dell'accesso a [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, sviluppatori e amministratori possono creare e connettere applicazioni a [!INCLUDE [prod_short](includes/prod_short.md)] a vantaggio dell'azienda:  

* Semplificazione dei processi aziendali
* Migliorare le interazioni con i clienti
* Prendere decisioni migliori, più velocemente

La tabella seguente contiene collegamenti a informazioni su come concedere ad app ed estensioni l'accesso ai dati [!INCLUDE [prod_short](includes/prod_short.md)].

| Attività | Ulteriori informazioni |
|--|--|
|I due concetti principali per definire l'accesso alle funzionalità sono i diritti e le autorizzazioni. I diritti danno ampio accesso agli oggetti in base a licenze o ai ruoli Azure Active Directory. Le autorizzazioni e gli insiemi di autorizzazioni consentono di ottimizzare l'accesso agli oggetti. |[Panoramica dei diritti e dei set di autorizzazioni](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## Vedi anche

[Sicurezza in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)