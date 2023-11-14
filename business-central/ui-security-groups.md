---
title: Controllo dell'accesso tramite i gruppi di sicurezza
description: Questo articolo descrive come utilizzare i gruppi di sicurezza per definire le autorizzazioni utente.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Controllare l'accesso a Business Central utilizzando i gruppi di sicurezza

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I gruppi di sicurezza semplificano la gestione delle autorizzazioni degli utenti da parte degli amministratori. Ad esempio, per [!INCLUDE [prod_short](includes/prod_short.md)] online, sono riutilizzabili nelle applicazioni Dynamics 365, quali SharePoint Online, CRM Online e [!INCLUDE [prod_short](includes/prod_short.md)]. Gli amministratori aggiungono autorizzazioni ai propri gruppi di sicurezza di [!INCLUDE [prod_short](includes/prod_short.md)] e, quando aggiungono utenti al gruppo, le autorizzazioni si applicano a tutti i membri. Ad esempio, un amministratore può creare un gruppo di sicurezza di [!INCLUDE [prod_short](includes/prod_short.md)] che offre ai venditori la possibilità di creare e registrare ordini di vendita. Oppure, lascia che gli acquirenti facciano lo stesso per gli ordini di acquisto.

## Business Central Online e in locale

Puoi utilizzare i gruppi di sicurezza per le versioni online e locali di [!INCLUDE [prod_short](includes/prod_short.md)]. A seconda della versione del prodotto, crea gruppi in una delle seguenti modalità:

* Per la versione online, usa i gruppi di sicurezza di Microsoft Entra. Per ulteriori informazioni sulla creazione del gruppo, vai a [Creare, modificare o eliminare un gruppo di sicurezza nell'interfaccia di amministrazione Microsoft 365](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* In locale, usa i gruppi di Windows Active Directory. Per saperne di più, vedi [Crea un account di gruppo in Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory).

In seguito, crea un relativo gruppo di sicurezza in [!INCLUDE [prod_short](includes/prod_short.md)] e quindi collegalo al gruppo di sicurezza creato. Per ulteriori informazioni, vai a [Aggiungere un gruppo di sicurezza in Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Se hai configurato un tipo speciale di utente con un tipo di licenza gruppo di Windows in una versione di [!INCLUDE [prod_short](includes/prod_short.md)] locale precedente al primo ciclo di rilascio del 2023, quando esegui l'aggiornamento [!INCLUDE [prod_short](includes/prod_short.md)] converte l'utente in un gruppo di sicurezza. Il nuovo gruppo di sicurezza ha lo stesso nome del nome del gruppo di Windows. Il gruppo di sicurezza offre una migliore panoramica dei membri del gruppo e delle loro autorizzazioni effettive.

## Aggiungere un gruppo di sicurezza in Business Central

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi di sicurezza**, quindi scegli il collegamento correlato.
1. Scegli **Nuovo** per creare un gruppo.
1. Crea il collegamento al tuo gruppo, come segue:

    * Per [!INCLUDE [prod_short](includes/prod_short.md)] online, scegli il gruppo nel campo **Nome gruppo di sicurezza Microsoft Entra**.
    * Per [!INCLUDE [prod_short](includes/prod_short.md)] in locale, scegli il gruppo nel campo **Nome gruppo Windows**.

> [!NOTE]
> Gli utenti vengono visualizzati nella scheda **Membri** nel riquadro Dettaglio informazioni o nella pagina **Membri del gruppo di sicurezza** solo se sono stati aggiunti come utenti in [!INCLUDE [prod_short](includes/prod_short.md)]. Per altre informazioni sull'aggiunta di utenti, vedi [Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central](ui-how-users-permissions.md#adduser).  

### Assegnare autorizzazioni a un gruppo di sicurezza

1. Nella pagina **Gruppi di sicurezza** scegli il gruppo e quindi l'azione **Autorizzazioni**.
1. Assegna le autorizzazioni nei seguenti modi:

    * Per assegnare i set di autorizzazioni singolarmente, nel campo **Set di autorizzazioni** scegli le autorizzazioni da assegnare.
    * Per assegnare più set di autorizzazioni, scegli l'azione **Seleziona set di autorizzazioni**, quindi scegli i set da assegnare.

## Esaminare le autorizzazioni di un gruppo di sicurezza

Nella pagina **Gruppi di sicurezza**, il riquadro Dettaglio informazioni mostra i **Set di autorizzazioni** che sono assegnati al gruppo. Ogni utente elencato nella scheda **Membri** dispone di tali autorizzazioni. L'azione **Set di autorizzazioni per gruppo di sicurezza** fornisce una visualizzazione più dettagliata. Puoi anche esplorare le singole autorizzazioni in ciascun gruppo di sicurezza.

Le autorizzazioni sono disponibili anche nella pagina **Utenti**. Il riquadro Dettaglio informazioni mostra le schede **Set di autorizzazioni da gruppo di sicurezza** e **Appartenenze al gruppo di sicurezza** per l'utente selezionato.

## Gruppi di sicurezza e gruppi di utenti

> [!NOTE]
> I gruppi di utenti non saranno più disponibili in una versione futura.

I gruppi di sicurezza sono molto simili ai gruppi utenti attualmente disponibili. Tuttavia, i gruppi utenti sono rilevanti solo per [!INCLUDE [prod_short](includes/prod_short.md)]. I gruppi di sicurezza si basano sui gruppi in Microsoft Entra ID o Windows Active Directory, a seconda che tu stia utilizzando [!INCLUDE [prod_short](includes/prod_short.md)] rispettivamente online o in locale. I gruppi dispongono di amministratori perché possono utilizzarli con altre app Dynamics 365. Ad esempio, se i venditori utilizzano [!INCLUDE [prod_short](includes/prod_short.md)] e SharePoint, gli amministratori non devono ricreare il gruppo e i suoi membri.

### Facoltativo: converti i gruppi di utenti in set di autorizzazioni

Nel primo ciclo di rilascio del 2023 e successivi, puoi convertire i gruppi di utenti in set di autorizzazioni nel tuo tenant. I set di autorizzazioni forniscono la stessa funzionalità dei gruppi di utenti. Di seguito vengono forniti alcuni esempi:

* Puoi usare il riquadro Dettaglio informazioni **Utenti** per gestire le autorizzazioni per gli utenti.
* Puoi visualizzare in dettaglio il nome del set di autorizzazioni per aggiungere altri set di autorizzazioni all'insieme su cui stai lavorando. Per ulteriori informazioni, vai a [Per aggiungere altri set di autorizzazioni](ui-define-granular-permissions.md#to-add-other-permission-sets).

Usa la guida alla configurazione assistita **Migrazione del gruppo di utenti** per convertire i tuoi gruppi. Per iniziare la guida, nella pagina **Gestione funzionalità** trova **Funzionalità: convertire le autorizzazioni dei gruppi utenti**, quindi scegli **Tutti gli utenti** nel campo **Abilitato per**. La guida al setup assistito offre le seguenti opzioni per la conversione.

|Opzione  |Descrizione  |
|---------|---------|
|Assegna a utente     | Assegna le autorizzazioni nei gruppi di utenti direttamente agli utenti assegnati al gruppo e rimuove le assegnazioni dei gruppi utenti.        |
|Converti in un set di autorizzazioni     | Crea una nuova autorizzazione per le autorizzazioni in ogni gruppo di utenti. Il nuovo set di autorizzazioni viene assegnato a tutti i membri di ogni gruppo di utenti.          |

### Le configurazioni della licenza sono sempre valide

Puoi configurare le autorizzazioni in [!INCLUDE [prod_short](includes/prod_short.md)] in base alle licenze. Tali autorizzazioni vengono assegnate direttamente a nuovi utenti. Queste configurazioni sono sempre valide, anche se inizi a utilizzare gruppi di sicurezza.

Per utilizzare gruppi di sicurezza in modo esclusivo, ti consigliamo di rimuovere le configurazioni della licenza. Per ulteriori informazioni sulle configurazioni delle licenze, vedi [Creare utenti in base alle licenze](ui-how-users-permissions.md).

Puoi rimuovere le configurazioni della licenza nella pagina **Configurazione della licenza**. Scegli una licenza, quindi elimina tutti i set di autorizzazioni ad essa assegnati.

## Vedi anche

[Creare utenti in base alle licenze](ui-how-users-permissions.md)  
[Configurazione degli accessi a Business Central in Teams con licenze Microsoft 365](admin-access-with-m365-license-setup.md)  
[Informazioni su gruppi e diritti di accesso in Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Gruppi di sicurezza di Microsoft Entra](/windows-server/identity/ad-ds/manage/understand-security-groups)  
