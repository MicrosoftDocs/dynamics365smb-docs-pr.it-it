---
title: Impostare la sincronizzazione dei contatti di Outlook per Business Central locale
description: Informazioni su come configurare un ambiente locale di Business Central per sincronizzare i contatti in Business Central e Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
---

# <a name="set-up-contact-sync-with-outlook-for-business-central-on-premises"></a>Impostare la sincronizzazione dei contatti di Outlook per Business Central locale

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

In questo articolo imparerai come configurare [!INCLUDE[prod_short](includes/prod_short.md)] locale per sincronizzare i contatti in [!INCLUDE[prod_short](includes/prod_short.md)] con i contatti in Outlook. Per ulteriori informazioni sulla funzione, vai a [Sincronizzare i contatti in Business Central con i contatti in Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## <a name="introduction"></a>Introduzione

La sincronizzazione dei contatti richiede l'utilizzo del protocollo OAuth 2.0 per l'autenticazione con Exchange Online. In precedenza, era supportata anche l'autenticazione di base, ma è stata deprecata e non è più supportata con Exchange Online. Puoi leggere ulteriori informazioni sulla deprecazione in [Deprecazione dell'autenticazione di base in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Questa modifica significa che la sincronizzazione dei contatti in Business Central potrebbe aver smesso di funzionare nell'ambiente locale. Questo articolo spiegherà come farla funzionare di nuovo.

## <a name="prerequisites"></a>Prerequisiti

- Exchange Online, una versione autonoma o tramite piano di Microsoft 365  
- Accedere al tenant Microsoft Entra utilizzato da Exchange Online
- Gli utenti [!INCLUDE[prod_short](includes/prod_short.md)] hanno un account e-mail Microsoft 365 o Exchange Online, che è assegnato ai loro account in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile controllare questa impostazione nella sezione di **autenticazione Microsoft 365** del profilo utente nell'elenco **Utenti**. 

## <a name="set-up-contact-sync"></a>Impostare la sincronizzazione dei contatti

Completa i seguenti passaggi per configurare la sincronizzazione dei contatti. Se stai eseguendo [!INCLUDE[prod_short](includes/prod_short.md)] Spring 2019 (v.14), dovrai eseguire un passaggio aggiuntivo che modifica il codice dell'applicazione o configura una connessione a Power BI.

1. <a name="registerapp"></a>Registra un'app per l'API Exchange Online nel tenant di Microsoft Entra.

   In questo passaggio aggiungi un'app registrata nel tenant Microsoft Entra del tuo piano Microsoft 365 o Exchange Online. Come altri servizi Azure che lavorano con Business Central, Exchange Online richiede un'app registrata in Microsoft Entra ID. L'app registrata fornisce servizi di autenticazione e autorizzazione tra Business Central ed Exchange Online.

   Segui le istruzioni dettagliate nella guida per sviluppatori e professionisti IT in [Registrare un'applicazione in Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Mentre segui le istruzioni, ricorda i seguenti punti:

   - Se hai già registrato un'applicazione come parte di un'integrazione con un altro prodotto Microsoft, come Power BI, allora puoi riutilizzare l'app registrata. In questo caso, devi solo impostare l'app con le autorizzazioni di Office 365 Exchange Online descritte al prossimo punto.

   - Configura l'app registrata con le seguenti autorizzazioni delegate all'API Office 365 Exchange Online:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Per [!INCLUDE[prod_short](includes/prod_short.md)] versione 14, esegui una delle seguenti attività:

   - Modifica la pagina 6700 cambiando `FALSE` in `TRUE` nella seguente riga di codice nel trigger `OnPageOpen`:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Crea una nuova pagina con il seguente codice nel trigger OnPageOpen:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Configura Power BI seguendo le istruzioni in [Configurare Business Central locale per l'integrazione di Power BI](admin-powerbi-setup.md#setup).

   Dopo che la soluzione scelta è stata implementata, chiedi agli utenti di eseguire la pagina nuova/modificata o di [connettersi a Power BI](across-working-with-powerbi.md#connect). Devono eseguire questo passaggio solo una volta.

## <a name="next-steps"></a>Passaggi successivi

[Sincronizzare i contatti di Business Central con i contatti di Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
