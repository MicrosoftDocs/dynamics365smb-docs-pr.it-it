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

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

I gruppi di sicurezza semplificano agli amministratori la gestione delle autorizzazioni utente nelle loro applicazioni Dynamics 365, ad esempio SharePoint Online, CRM Online, e la versione online di [!INCLUDE [prod_short](includes/prod_short.md)]. Gli amministratori aggiungono autorizzazioni ai propri gruppi di sicurezza e, quando aggiungono utenti al gruppo, le autorizzazioni si applicano a tutti i membri. Ad esempio, un amministratore può creare un gruppo di sicurezza che offre ai venditori la possibilità di creare e registrare ordini di vendita. Oppure, lascia che gli acquirenti facciano lo stesso per gli ordini di acquisto.

Crea i tuoi gruppi di sicurezza nell'interfaccia di amministrazione di Microsoft 365 o in Azure Active Directory. Questo articolo descrive i passaggi nell'interfaccia di amministrazione di Microsoft 365, ma i passaggi sono simili in entrambi i sistemi.

## Aggiungere un gruppo di sicurezza nell'interfaccia di amministrazione di Microsoft 365

1. Nell'interfaccia di amministrazione di Microsoft 365, vai alla pagina **Team e gruppi attivi**.
2. Scegli **Aggiungi un gruppo**.
3. Scegli il tipo di gruppo di **sicurezza** e scegli **Avanti**.
4. Specifica le basi per il tuo gruppo.
5. Facoltativo: rendi i membri del gruppo disponibili per l'assegnazione del ruolo. Per ulteriori informazioni sulle assegnazioni, vai a [Utilizzare i gruppi Azure AD per gestire le assegnazioni di ruolo](/azure/active-directory/roles/groups-concept).
6. Apri il gruppo, quindi utilizza la scheda **Aggiungi membri** per includere le persone nel gruppo.

## Aggiungere un gruppo di sicurezza in Business Central

In [!INCLUDE [prod_short](includes/prod_short.md)], crea un gruppo di sicurezza e poi collegalo al gruppo di sicurezza nell'interfaccia di amministrazione di Microsoft 365. Il tuo nuovo gruppo contiene i membri che hai aggiunto nell'interfaccia di amministrazione di Microsoft 365.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gruppi di sicurezza**, quindi scegli il collegamento correlato.
2. Scegli **Nuovo** per creare un gruppo.
3. Nel campo **Nome** immetti un nome per il gruppo.
4. Nel campo **Nome gruppo di sicurezza AAD** inserisci il nome del gruppo di sicurezza esattamente come appare nell'interfaccia di amministrazione di Microsoft 365. [!INCLUDE [prod_short](includes/prod_short.md)] troverà quel gruppo e lo collegherà a questo gruppo.

> [!NOTE]
> Gli utenti vengono visualizzati nella scheda **Membri** nel riquadro Dettaglio informazioni o nella pagina **Membri del gruppo di sicurezza** solo se sono stati aggiunti come utenti in [!INCLUDE [prod_short](includes/prod_short.md)]. Per altre informazioni sull'aggiunta di utenti, vedi [Per aggiungere utenti o aggiornare le informazioni utente e le assegnazioni della licenza in Business Central](ui-how-users-permissions.md#adduser).  

### Assegnare le autorizzazioni al gruppo

1. Nella pagina **Gruppi di sicurezza** scegli il gruppo e quindi l'azione **Autorizzazioni**.
1. Assegna le autorizzazioni nei seguenti modi:
    * Per assegnare i set di autorizzazioni singolarmente, nel campo **Set di autorizzazioni** scegli le autorizzazioni da assegnare.
    * Per assegnare più set di autorizzazioni, scegli l'azione **Seleziona set di autorizzazioni**, quindi scegli i set da assegnare.

## Esaminare le autorizzazioni di un gruppo di sicurezza

Nella pagina **Gruppi di sicurezza**, il riquadro Dettaglio informazioni mostra i **Set di autorizzazioni** che sono assegnati al gruppo. Ogni utente elencato nella scheda **Membri** dispone di tali autorizzazioni. L'azione **Set di autorizzazioni per gruppo di sicurezza** fornisce una visualizzazione più dettagliata. Puoi anche esplorare le singole autorizzazioni in ciascun gruppo di sicurezza.

Le autorizzazioni sono disponibili anche nella pagina **Utenti**. Il riquadro Dettaglio informazioni mostra le schede **Set di autorizzazioni da gruppo di sicurezza** e **Appartenenze al gruppo di sicurezza** per l'utente selezionato.

## Gruppi di sicurezza e gruppi di utenti

Se disponi di gruppi di utenti, puoi convertire i gruppi in set di autorizzazioni nel tuo tenant utilizzando la guida al setup assistito **Migrazione dei gruppi di utenti**. Per iniziare la guida, nella pagina **Gestione funzionalità** trova **Funzionalità: convertire le autorizzazioni dei gruppi utenti**, quindi scegli **Tutti gli utenti** nel campo **Abilitato per**. La guida al setup assistito offre le seguenti opzioni per la conversione.

|Opzione  |Descrizione  |
|---------|---------|
|Assegna a utente     | Assegna le autorizzazioni nei gruppi di utenti direttamente agli utenti assegnati al gruppo e rimuove le assegnazioni dei gruppi utenti.        |
|Converti in un set di autorizzazioni     | Crea una nuova autorizzazione per le autorizzazioni in ogni gruppo di utenti. Il nuovo set di autorizzazioni viene assegnato a tutti i membri di ogni gruppo di utenti.          |

## Vedere anche

[Creare utenti in base alle licenze](ui-how-users-permissions.md)  
[Configurazione degli accessi a Business Central in Teams con licenze Microsoft 365](admin-access-with-m365-license-setup.md)  
[Informazioni su gruppi e diritti di accesso in Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Gruppi di sicurezza di Active Directory](/windows-server/identity/ad-ds/manage/understand-security-groups)  