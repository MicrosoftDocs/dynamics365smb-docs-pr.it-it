---
title: Impostare il log delle e-mail | Documenti Microsoft
description: Informazioni su come trasformare le interazioni e-mail tra venditori e clienti in reali opportunità di vendita.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 59e5a37bc24c78ea9af9f5d518b98c2ada7764a4
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382616"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti

Ottenere di più dalle comunicazioni tra i venditori e i tuoi clienti esistenti o potenziali monitorando gli scambi di e-mail e trasformandoli in opportunità fruibili. [!INCLUDE[prod_short](includes/prod_short.md)] può utilizzare Exchange Online per tenere un log dei messaggi in entrata e in uscita. È possibile visualizzare e analizzare i contenuti di ciascun messaggio nella pagina **Movimenti log interazione**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Impostare le cartelle pubbliche e le regole per il log delle e-mail in Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Quindi, connettersi a [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Impostare [!INCLUDE[prod_short](includes/prod_short.md)] per registrare i messaggi e-mail

Iniziare la registrazione dei messaggi e-mail con due semplici passaggi:

1. Collegare [!INCLUDE[prod_short](includes/prod_short.md)]con Exchange Online per l'abbonamento a Microsoft 365. Exchange Online gestisce i messaggi di posta elettronica. Questo passaggio è stato semplificato con una guida di installazione assistita. Sono necessarie solo le credenziali di amministratore per l'account amministratore in Microsoft 365. Per iniziare la guida, andare alla pagina **Setup assistito** e quindi selezionare la guida **Configurare la registrazione e-mail**.  

2. Assicurarsi che siano stati inseriti indirizzi email validi in [!INCLUDE[prod_short](includes/prod_short.md)] per gli addetti alle vendite e i contatti, a seconda che si tratti di clienti potenziali o esistenti. Per fare ciò, per ogni cliente o venditore, aprire la scheda **Contatto** o **Venditore/Acquirente** e osservare il campo **E-mail**.

> [!Tip]
> Dopo aver completato i passaggi nella guida, è possibile verificare se la connessione ha avuto esito positivo. Cercare **Impostazione marketing** e selezionare **Accesso**, quindi **Funzioni** e **Convalida configurazione registrazione email**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visualizzazione degli scambi di messaggi e-mail nel log delle interazioni

[!INCLUDE[prod_short](includes/prod_short.md)] crea una voce nella pagina **Log delle interazioni** ogni volta che un venditore e un contatto scambiano un messaggio di posta elettronica. Per visualizzare il log delle interazioni, aprire la scheda **Contatto** per la persona, scegliere **Correlato**, quindi **Cronologia** e **Movimenti log interazione**. Ci sono alcune cose che si possono fare con ogni voce del log, ad esempio:

- Visualizzare il contenuto del messaggio di posta elettronica che è stato scambiato selezionando **Processo** e quindi **Mostra allegati**.
- Trasformare uno scambio di e-mail in un'opportunità di vendita: se una voce sembra promettente, è possibile trasformarla in un'opportunità e gestirne i progressi verso una vendita. A questo proposito, selezionare la voce, quindi selezionare **Processo** e quindi **Crea opportunità**. Per ulteriori informazioni, vedere [Gestire opportunità di vendita](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Connessione delle versioni locali a Microsoft Exchange

È possibile connettere [!INCLUDE[prod_short](includes/prod_short.md)] in locale a Exchange in locale o a Exchange Online per il log delle e-mail. Per entrambe le versioni di Exchange, le impostazioni per la connessione sono disponibili nella pagina **Setup marketing**. Per Exchange Online, è anche possibile utilizzare una guida alla al setup assistito.

### <a name="connecting-to-exchange-on-premises"></a>Connessione a Exchange in locale

Per connettere [!INCLUDE[prod_short](includes/prod_short.md)] in locale a Exchange in locale, nella pagina **Setup marketing**, è possibile utilizzare **Di base** come **Tipo di autenticazione** e quindi immettere le credenziali per l'account utente per Exchange in locale. Quindi attivare l'interruttore **Abilitato** per avviare il log delle e-mail.

### <a name="connecting-to-exchange-online"></a>Connessione a Exchange Online

Per connettersi a Exchange Online, è necessario usare **OAuth2** come **Tipo di autenticazione**. È inoltre necessario registrare un'applicazione in Azure Active Directory e fornire l'ID applicazione, il segreto del key vault e l'URL di reindirizzamento da utilizzare. L'URL di reindirizzamento è precompilato e dovrebbe funzionare per la maggior parte delle installazioni. Per ulteriori informazioni, vedere Per registrare un'applicazione in Azure AD per la connessione da Business Central a Exchange Online di seguito.

È necessario configurare l'installazione per utilizzare HTTPS. Per ulteriori informazioni, vedere [Configurazione di SSL per proteggere la connessione client Web di Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Se si sta configurando il server in modo da avere una home page diversa, è possibile cambiare l'URL. Il segreto del client verrà salvato come stringa crittografata nel database.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Per registrare un'applicazione in Azure AD per la connessione da Business Central a Exchange Online

I seguenti passaggi presuppongono che si stia utilizzando Azure Active Directory per gestire identità e accesso. Per ulteriori informazioni, vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app). Se non si utilizza Azure Active Directory vedere [Utilizzo di un altro servizio di gestione dell'identità e degli accessi](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

1. Nel portale di Azure, in **Gestisci** selezionare **Autenticazione**.
2. In **URL di reindirizzamento**, aggiungere l'URL di reindirizzamento suggerito nella pagina **Setup marketing** in [!INCLUDE[prod_short](includes/prod_short.md)]. Se l'URL di reindirizzamento nella pagina Setup marketing è vuoto, trovare l'URL di reindirizzamento suggerito nella pagina **Setup assistito log delle e-mail**.

    > [!NOTE]
    > Se non si specifica l'URL di reindirizzamento, è possibile farlo in seguito scegliendo **Aggiungi una piattaforma** e quindi **Web** per aggiungere l'applicazione Web e l'URL di reindirizzamento. 

3. In **Gestisci**, scegliere **Manifesto**.
4. Individuare la proprietà **requiredResourceAccess** nel manifest e aggiungere il codice seguente tra parentesi ([]) per aggiungere le autorizzazioni richieste. Per ulteriori informazioni, vedere [Registrare l'applicazione](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Selezionare **Salva**.
6. Sotto **Gestisci**, scegliere **Autorizzazioni API**, quindi verificare che siano elencate le seguenti autorizzazioni:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. In **Gestisci**, scegliere **Certificati e segreti**, quindi creare un nuovo segreto per l'app. Si utilizzerà il segreto in [!INCLUDE[prod_short](includes/prod_short.md)], nel campo **Segreto client** della pagina **Setup marketing** o lo si archivierà in un archivio sicuro per utilizzarlo in una sottoscrizione di eventi.
8. Scegliere **Panoramica**, quindi trovare il valore **ID applicazione (client)**. Questo è l'ID client dell'applicazione. È necessario inserirlo nella **pagina Setup connessione** nel campo **ID client** o archiviarlo in un archivio sicuro e fornirlo in una sottoscrizione di eventi.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], configurare il log delle e-mail nella pagina **Setup marketing** o usare la guida **Setup assistito log delle e-mail** per assistenza con il processo.
    * Fornire l'account di posta elettronica dell'utente per conto del quale il processo programmato si connetterà Exchange Online ed elaborerà le e-mail. L'utente deve disporre di una licenza valida per Exchange Online.
    * Fornire l'URL per Exchange Online. In genere, questo è il dominio specificato nell'indirizzo di posta elettronica dell'utente.
    * Specificare il **Percorso cartella coda** e il **Percorso cartella archiviazione**.
10. Per avviare il log delle e-mail, attivare l'interruttore **Abilitato**.
11. Accedere con l'account amministratore per Azure Active Directory (questo account deve avere una licenza valida per Exchange ed essere un amministratore in Exchange Online). Dopo aver effettuato l'accesso, verrà richiesto di consentire all'applicazione registrata l'accesso a Exchange Online per conto dell'organizzazione. È necessario fornire il consenso per completare il setup.

   > [!NOTE]
   > Se non viene richiesto di accedere con il proprio account amministratore, è possibile che i popup siano bloccati. Per accedere, consentire i popup da https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Utilizzo di un altro servizio di gestione dell'identità e degli accessi
Se non si sta usando Azure Active Directory per gestire le identità e l'accesso, è necessario l'aiuto di uno sviluppatore. Se si preferisce archiviare l'ID app e il segreto in una posizione diversa, è possibile lasciare vuoti i campi ID client e Segreto client e scrivere un'estensione per recuperare l'ID e il segreto dalla posizione. È possibile fornire il segreto in fase di esecuzione sottoscrivendo gli eventi OnGetCDSConnectionClientId e OnGetCDSConnectionClientSecret nella codeunit 1641 "Setup log delle e-mail".

### <a name="to-stop-logging-email"></a>Per interrompere il log delle e-mail
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup marketing**, quindi scegli il collegamento correlato.
2. Disattivare l'interruttore **Abilitato**.

## <a name="see-also"></a>Vedere anche
[Gestione delle relazioni](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]