---
title: Configura l'accesso con licenze Microsoft 365
description: Una guida su come gli amministratori possono configurare l'accesso a Business Central con licenze Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Configurazione degli accessi a Business Central in Teams con licenze Microsoft 365

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Gli amministratori devono completare più attività prima che gli utenti possano accedere a [!INCLUDE [prod_short](includes/prod_short.md)] con la propria licenza Microsoft 365. I passaggi seguenti rappresentano la configurazione minima richiesta per iniziare. Per ulteriori informazioni sull'accesso con licenze Microsoft 365, vai ad [Accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md).

## <a name="guidelines"></a>Linee guida

La configurazione dell'accesso con licenze Microsoft 365 comporta le seguenti attività:

|Passaggio|Attività|Obbligatorio|
|-|-|-|
|1|[Configura quali dati di Business Central gli utenti Microsoft 365 con licenza sono autorizzati a visualizzare](#configure-permissions)|![segno di spunta](media/check.png "selezionato")|
|2|[Abilita l'accesso con licenze Microsoft 365 nell'ambiente Business Central](#enable-access-with-microsoft-365-licenses)|![segno di spunta](media/check.png "selezionato")|
|3|[Assegnare il gruppo di sicurezza all'ambiente](#choose-who-gets-access-by-using-security-group)|
|4|[Sviluppare l'app Business Central per Teams agli utenti](#deploy-the-business-central-app-for-teams)|![segno di spunta](media/check.png "selezionato")|
|5|[Provare la configurazione.](#test-your-setup)||

> [!TIP]
> Ad eccezione dell'ultima attività, puoi completare le attività in qualsiasi ordine. Puoi eseguire le attività separatamente, come descritto nelle sezioni che seguono o utilizzare la guida alla configurazione assistita **Accesso con licenze Microsoft 365** per informazioni su di esse.
>
> Per eseguire la configurazione assistita, attieniti a questa procedura:
>
> 1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Setup assistito**e poi scegliere il link relativo.
> 2. Nella pagina **Configurazione assistita**, vai alla sezione **Altre attività con Business Central** e seleziona **Accesso con licenze Microsoft 365**.
> 3. Segui le istruzioni.  

## <a name="configure-permissions"></a>Configura autorizzazioni

[!INCLUDE [prod_short](includes/prod_short.md)] è sicuro fin dalla progettazione e riduce al minimo i rischi non concedendo autorizzazioni agli utenti Microsoft 365 per impostazione predefinita. Gli amministratori devono configurare le autorizzazioni per gli oggetti che determinano a quali tabelle, pagine e report è possibile accedere in Teams solo con una licenza Microsoft 365. Queste autorizzazioni sono le autorizzazioni iniziali assegnate quando un utente accede per la prima volta con la propria licenza Microsoft 365. 

Per configurare le autorizzazioni di avvio:

1. In [!INCLUDE [prod_short](includes/prod_short.md)], cerca **Configurazione licenza**.
2. Seleziona la licenza Microsoft 365.
3. Nella parte superiore della pagina della licenza **Microsoft 365**, seleziona l'icona di modifica ![Icona Modifica](media/edit-pencil.png), quindi abilita **Personalizza autorizzazioni**. 
4. Nella sezione **Set di autorizzazioni personalizzate**, aggiungi i set di autorizzazioni appropriati e scegli se sono applicabili a una singola azienda o a tutte le aziende all'interno dell'ambiente.

Con questa configurazione, gli utenti con solo la licenza Microsoft 365 vengono aggiunti all'elenco **Utenti** quando accedono a [!INCLUDE [prod_short](includes/prod_short.md)] per la prima volta. Per ulteriori informazioni sugli utenti, vai a [Creazione di utenti in base alle licenze](ui-how-users-permissions.md).

> [!NOTE]
> Durante la sincronizzazione dell'elenco utenti in Bu[!INCLUDE [prod_short](includes/prod_short.md)] con gli utenti in Microsoft 365, solo gli utenti che dispongono di una licenza [!INCLUDE [prod_short](includes/prod_short.md)] vengono aggiunti all'elenco utenti di [!INCLUDE [prod_short](includes/prod_short.md)]. Per un maggiore controllo amministrativo su autorizzazioni e profili, puoi assegnare un gruppo di sicurezza all'ambiente. Quando gli ambienti sono protetti utilizzando un gruppo di sicurezza e si abilita l'accesso con licenze Microsoft 365, l'azione **Aggiorna utenti da Microsoft 365** nella pagina **Utenti** includerà anche gli utenti che hanno solo una licenza Microsoft 365. Per informazioni sulla protezione degli ambienti, vedi [Gestire l'accesso utilizzando gruppi Microsoft Entra](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) nella guida per sviluppatori e professionisti IT.

> [!TIP]
> Cerchi un modo più rapido per iniziare quando provi questa funzione sandbox o società di valutazione? Assegna il set di autorizzazioni di **D365 lettura**, che concede l'autorizzazione alla maggior parte degli oggetti.  

Quando si lavora con più ambienti, la configurazione delle licenze deve essere applicata a ciascun ambiente e può essere diversa per ogni ambiente.

Ulteriori informazioni in [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md) e [Composizione di set di autorizzazioni](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="enable-access-with-microsoft-365-licenses"></a>Abilitare l'accesso con le licenze Microsoft 365

L'accesso licenze Microsoft 365 è disabilitato per impostazione predefinita. L'accesso deve essere abilitato per ogni ambiente in modo indipendente, offrendo agli amministratori il controllo e consentendo un'implementazione graduale in tutta l'organizzazione. Puoi abilitare l'accesso utilizzando l'interfaccia di amministrazione di [!INCLUDE [prod_short](includes/prod_short.md)]: 

1. Nell'angolo in alto a destra, seleziona **Impostazioni** ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") > **Interfaccia di amministrazione**.  
2. Nell'interfaccia di amministrazione, seleziona  **Ambienti**, quindi seleziona l'ambiente in cui desideri modificare l'accesso alla licenza. 
3. Nella pagina **Dettagli ambiente**, seleziona **Modifica** per l'impostazione **Accedi con licenze Microsoft 365**.
4. Nel riquadro **Licenze Microsoft 365**, abilita l'interruttore. 
5. Seleziona **Salva** al termine e accetta la conferma. La modifica entra in vigore immediatamente.

## <a name="choose-who-gets-access-by-using-security-group"></a>Scegli chi può accedere utilizzando il gruppo di sicurezza

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Nell'interfaccia di amministrazione di Business Center, un ambiente può essere assegnato a uno o più gruppi di sicurezza per controllare l'accesso. Puoi assegnare un gruppo Microsoft Entra all'ambiente. Assegnando un gruppo Microsoft Entra a un ambiente, solo i membri diretti e indiretti del gruppo hanno accesso all'ambiente. I membri indiretti sono utenti in un altro gruppo, che a sua volta è un membro del gruppo assegnato all'ambiente. Sebbene tutti gli utenti con licenza in Microsoft Entra ID verranno aggiunti all'ambiente quando è sincronizzato con Microsoft 365, solo i membri del gruppo possono eseguire l'accesso. Per ulteriori informazioni, vai a [Gestire l'accesso utilizzando gruppi Microsoft Entra](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) nella guida per sviluppatori e professionisti IT.

## <a name="deploy-the-business-central-app-for-teams"></a>Distribuisci l'app Business Central per Teams

Affinché i titolari di licenza [!INCLUDE [prod_short](includes/prod_short.md)] possano condividere i dati in Teams e affinché i titolari di licenza Microsoft 365 possano accedere a tali dati, ciascuno deve avere l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams installata. Sebbene gli utenti possano installare l'app da soli, si consiglia agli amministratori di usare la distribuzione centralizzata. La distribuzione centralizzata ti consente di distribuire l'app a un pubblico più ampio in tutta l'organizzazione e ridurre al minimo lo sforzo dei singoli utenti. 

Per informazioni su come distribuire centralmente l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams, vedi [Installazione dell'app Business Central tramite la distribuzione centralizzata](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Se in precedenza hai eseguito la distribuzione centralizzata e hai distribuito l'app solo al gruppo di sicurezza degli utenti [!INCLUDE [prod_short](includes/prod_short.md)] con licenza, dovrai eseguirla di nuovo per distribuirla a gruppi aggiuntivi o all'intera organizzazione, a seconda di come stai configurando l'accesso.

> [!TIP]
> Cerchi un modo più rapido per iniziare quando provi questa funzione? Gli utenti di prova possono installare l'app all'indirizzo [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="test-your-setup"></a>Esegui un test della tua configurazione

Per verificare che la tua configurazione sia pronta per la produzione, i passaggi seguenti ti aiuteranno a creare la certezza che tutto funzioni come dovrebbe.

1. Crea o identifica due utenti di test (A e B).

   - L'utente di test A deve disporre di una licenza [!INCLUDE [prod_short](includes/prod_short.md)] e di una licenza Microsoft 365 con accesso a Teams.
   - L'utente di test B deve avere solo una licenza Microsoft 365 con accesso a Teams.

2. Accedi al client Web [!INCLUDE [prod_short](includes/prod_short.md)] come utente di prova A.

   1. Apri un record a cui l'utente di test B dovrebbe avere accesso, ad esempio una scheda **Articolo** nell'azienda e nell'ambiente appropriati.
   2. Seleziona **Condividi** ![!Azione Condividi con altre app nelle pagine.](media/share-icon.png) > **Condividi su Teams** per visualizzare la finestra Condividi su Teams.
   3. Nel campo **Condividi su**, aggiungi l'utente di test B come destinatario.
   4. Attendi che il collegamento si espanda a una scheda e seleziona Condividi.

3. Accedi a Microsoft Teams come utente di test B.

   1. Seleziona Chat e apri la conversazione con l'utente di test A.
   2. Nel messaggio inviato dall'utente di test A, seleziona il pulsante Dettagli sulla scheda. Se il client [!INCLUDE [prod_short](includes/prod_short.md)] viene visualizzato ed è di sola lettura, la configurazione è riuscita.

> [!TIP]
> Si è verificato un errore. Consulta [Risoluzione dei problemi di accesso con licenze Microsoft 365](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Vedere anche

[Panoramica dell'accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Risoluzione dei problemi di accesso con licenze Microsoft 365](admin-access-with-m365-license-troubleshooting.md)  
[Business Central e integrazione Microsoft Teams](across-teams-overview.md)  
