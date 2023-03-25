---
title: Iniziare con il connettore per Shopify
description: Primi passaggi per la configurazione della connessione tra Business Central e Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Iniziare a usare il connettore Shopify

Collega il tuo negozio (o negozi) Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] e massimizza la produttività della tua azienda. Gestisci e visualizza le informazioni dettagliate della tua azienda e del tuo negozio Shopify come un'unica unità.

Per usare Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], devi prima fare un paio di cose. Questo articolo funge da guida per integrare il tuo negozio Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## Prerequisiti per Shopify

Devi avere:

- Un account Shopify
- Un punto vendita online Shopify

Scopri di più su come creare versioni di valutazione e impostazioni consigliate Shopify, vai a [Creare e configurare l'account Shopify](shopify-account.md).

## Prerequisiti per Business Central

- Assicurati che l'app **[Connettore Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** sia installata.

  L'app è preinstallata per tutte le nuove iscrizioni e versioni di valutazione. Per ulteriori informazioni sull'installazione delle app da AppSource, vedi [Installazione e disinstallazione delle estensioni](../ui-extensions-install-uninstall.md#install). Segui i passaggi elencati di seguito se non hai [!INCLUDE[prod_short](../includes/prod_short.md)].

- Assicurarsi che l'utente disponga di autorizzazioni sufficienti. Il connettore Shopify è coperto dal set di autorizzazioni *Shopify – Amministrazione (SHPFY – ADMIN)* . Ulteriori informazioni in [Creare utenti in base alle licenze](../ui-how-users-permissions.md) e [Assegnare autorizzazioni a utenti e gruppi](../ui-define-granular-permissions.md)


## Installa l'app Dynamics 365 Business Central nel tuo negozio Shopify online

Per [!INCLUDE[prod_short](../includes/prod_short.md)] esistente, questo passaggio è facoltativo e può essere saltato.

1. Individua l'app [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) in [Shopify AppStore](https://apps.shopify.com/)
2. Scegliere il pulsante **Aggiungi app**. Se richiesto, accedi al tuo account Shopify. Seleziona il negozio online richiesto se ne hai più di uno.
3. Dopo aver esaminato la privacy e le autorizzazioni, scegli il pulsante **Installa app**.

   Puoi trovare e aprire l'app **Dynamics 365 Business Central** installata nella sezione **App** sulla barra laterale della pagina **Amministratore Shopify**.
4. Scegli **Iscriviti ora** per iniziare una versione di valutazione di [!INCLUDE[prod_short](../includes/prod_short.md)] o **accedi** se hai già [!INCLUDE[prod_short](../includes/prod_short.md)]. Verrà eseguito il reindirizzamento alla pagina [Business Central](https://businesscentral.dynamics.com).
5. I passaggi successivi devono essere eseguiti in [!INCLUDE[prod_short](../includes/prod_short.md)].

## Collegamento di Business Central al negozio online Shopify

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Negozio Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.  
3. Nel campo **Codice**, inserisci il codice che lo renderà facilmente reperibile in [!INCLUDE[prod_short](../includes/prod_short.md)]. Il nome potrebbe riflettere ciò che un negozio vende, ad esempio "Mobili" o "Caffè", oppure il paese o la regione in cui opera.
4. Nel campo **URL Shopify**, digita l'URL del tuo negozio online, che deve essere collegato. Usa il seguente formato: `https://{shop}.myshopify.com/`.
5. Attiva l'interruttore **Abilitato**, rivedi e accetta i termini e le condizioni.
6. Se richiesto, accedi al tuo account Shopify, rivedi le condizioni di privacy e autorizzazioni, quindi scegli il pulsante **Installa app**.

Ripeti i passaggi 2-6 per tutti i negozi online che si desidera collegare.

### Problemi noti

- Il browser blocca la finestra pop-up. Quando attivi l'interruttore **Abilitato** il sistema apre la pagina **In attesa di risposta, non chiudere questa pagina**, che è in attesa di un token di accesso da Shopify, se quella pagina è chiusa o bloccata, non puoi connetterti a Shopify. Ulteriori informazioni in [Richiedere il token di accesso](troubleshoot.md#request-the-access-token)
- [Errore Oauth invalid_request: impossibile trovare l'API per l'applicazione Shopify con api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Impossibile connettersi dalla sandbox](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Passaggi successivi

Ora il tuo negozio online è connesso a [!INCLUDE[prod_short](../includes/prod_short.md)]. Nei passaggi successivi definirai come e cosa sincronizzare.

- [Sincronizzazione elementi](synchronize-items.md)
- [Sincronizzare clienti](synchronize-customers.md)
- [Sincronizzare ordini](synchronize-orders.md)

## Vedere anche

[Procedura dettagliata: Impostazione e utilizzo di un connettore Shopify](walkthrough-setting-up-and-using-shopify.md)  

