---
title: Iniziare con il connettore per Shopify
description: Primi passaggi per la configurazione della connessione tra Business Central e Shopify
ms.date: 04/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="get-started-with-the-shopify-connector"></a>Iniziare a usare il connettore Shopify

Collega il tuo punto vendita (o punti vendita) Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] e massimizza la produttività della tua azienda. Gestisci e visualizza le informazioni dettagliate della tua azienda e del tuo negozio Shopify come un'unica unità.

Per usare Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], devi prima fare un paio di cose. Questo articolo funge da guida per integrare il tuo negozio Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Prerequisiti per Shopify

Devi avere:

- Un account Shopify
- Un punto vendita online Shopify

Scopri di più su come creare valutazioni di prova e impostazioni consigliate Shopify in [Creare e configurare l'account Shopify](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Prerequisiti per Business Central

- Assicurati che l'app **[Connettore Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** sia installata.

  L'app è preinstallata per tutte le nuove iscrizioni e versioni di valutazione. Per ulteriori informazioni sull'installazione delle app da AppSource, vedi [Installazione e disinstallazione delle estensioni](../ui-extensions-install-uninstall.md#install). Segui i passaggi elencati di seguito se non hai [!INCLUDE[prod_short](../includes/prod_short.md)].

- Assicurati che l'utente disponga di autorizzazioni corrette. Il connettore Shopify è coperto dal set di autorizzazioni **Shopify – Amministrazione (SHPFY – ADMIN)** . Ulteriori informazioni in [Creare utenti in base alle licenze](../ui-how-users-permissions.md) e [Assegnare autorizzazioni a utenti e gruppi](../ui-define-granular-permissions.md).

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installa l'app Dynamics 365 Business Central nel tuo negozio Shopify online

Per le istanze esistenti di [!INCLUDE[prod_short](../includes/prod_short.md)], questo passaggio è facoltativo e può essere saltato.

1. Individua l'app [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) in [Shopify AppStore](https://apps.shopify.com/).
2. Scegliere il pulsante **Aggiungi app**. Se richiesto, accedi al tuo account Shopify. Seleziona il negozio online se ne hai più di uno.
3. Dopo aver esaminato la privacy e le autorizzazioni, scegli il pulsante **Installa app**.

   Puoi trovare e aprire l'app **Dynamics 365 Business Central** installata nella sezione **App** sulla barra laterale della pagina **Amministratore Shopify**.
4. Scegli **Iscriviti ora** per iniziare una versione di valutazione di [!INCLUDE[prod_short](../includes/prod_short.md)] o **accedi** se hai già [!INCLUDE[prod_short](../includes/prod_short.md)]. Verrà eseguito il reindirizzamento alla pagina [Business Central](https://businesscentral.dynamics.com).
5. In [!INCLUDE[prod_short](../includes/prod_short.md)] effettua i seguenti passaggi.

## <a name="connect-business-central-to-the-shopify-online-store"></a>Collegamento di Business Central al negozio online Shopify

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.  
3. Nel campo **Codice**, inserisci un codice che lo renderà facilmente reperibile in [!INCLUDE[prod_short](../includes/prod_short.md)]. Il nome potrebbe riflettere ciò che un negozio vende, ad esempio "Mobili" o "Caffè", oppure il paese o la regione in cui opera.
4. Nel campo **URL Shopify**, immetti l'URL del punto vendita online a cui desideri connetterti. Usa il seguente formato: `https://{shop}.myshopify.com/`.

   > [!TIP]
   > Puoi copiare l'URL dall'amministrazione di Shopify, come `https://admin.shopify.com/store/{shop}`, e il connettore lo convertirà nel formato richiesto.

5. Attiva l'interruttore **Abilitato** quindi rivedi e accetta i termini e le condizioni.
6. Se richiesto, accedi al tuo account Shopify. Dopo aver esaminato la privacy e le autorizzazioni, scegli il pulsante **Installa app**.

Ripeti i passaggi 2-6 per tutti i negozi online che si desidera collegare.

### <a name="known-issues"></a>Problemi noti

- Il browser blocca la finestra pop-up. Quando attivi l'interruttore **Abilitato**, [!INCLUDE [prod_short](../includes/prod_short.md)] si apre nella pagina **In attesa di risposta - non chiudere questa pagina** mentre attende un token di accesso da Shopify. Se quella pagina è chiusa o bloccata, non puoi connetterti a Shopify. Ulteriori informazioni in [Richiedere il token di accesso](troubleshoot.md#request-the-access-token).
- Potrebbe essere una buona idea avere Amministrazione Shopify aperto nello stesso browser di [!INCLUDE [prod_short](../includes/prod_short.md)].
- [Errore Oauthinvalid_request: impossibile trovare l'API per l'applicazione Shopify con api_key.](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Errore: errore Oauth invalid_request: il tuo account non dispone dell'autorizzazione per concedere l'accesso richiesto per questa app.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Impossibile connettersi dalla sandbox](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)
- Assicurati di inserire l'URL corretto nel campo **URL Shopify**. Puoi creare l'URL combinando l'ID del negozio dall'URL di amministrazione. Ad esempio, `admin.shopify.com/store/{shop}` e `.myshopify.com` per ottenere `https://{shop}.myshopify.com/`.

## <a name="next-steps"></a>Passaggi successivi

Ora il tuo negozio online è connesso a [!INCLUDE[prod_short](../includes/prod_short.md)]. Nei passaggi successivi definirai come e cosa sincronizzare.

- [Sincronizzare articoli e inventario](synchronize-items.md)
- [Sincronizza clienti](synchronize-customers.md)
- [Sincronizzare ordini](synchronize-orders.md)

## <a name="testing-strategies"></a>Strategie di test

Esistono diversi approcci per testare un'integrazione e ogni approccio ha i suoi pro e contro.

Puoi collegare i conti [!INCLUDE[prod_short](../includes/prod_short.md)] e Shopify tutte le volte che vuoi. Il connettore Shopify interessa solo l'ambiente, o per essere più precisi, l'azienda in cui è abilitato. Puoi connetterti allo stesso negozio online Shopify da più ambienti o aziende. È possibile disabilitare e riabilitare il connettore.

È facile ripetere i test di sincronizzazione. Il connettore consente di eliminare i dati importati, come prodotti, clienti e ordini, e quindi importarli nuovamente. Basta solo [reimpostare la sincronizzazione](troubleshoot.md#reset-sync).

### <a name="shopify-sandbox-and-business-central-sandbox"></a>Sandbox Shopify e sandbox Business Central

Questo è probabilmente il modo più sicuro per testare l'integrazione. Invece di utilizzare una sandbox Shopify puoi utilizzare un abbonamento di prova o un punto vendita per lo sviluppo. In [!INCLUDE[prod_short](../includes/prod_short.md)], puoi anche utilizzare un'azienda di test in un ambiente di produzione.

Per ulteriori informazioni sulle sandbox [!INCLUDE[prod_short](../includes/prod_short.md)], vai a [Creare un nuovo ambiente](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### <a name="shopify-sandbox-and-business-central-production"></a>Sandbox Shopify e produzione Business Central

Questa *non è* una configurazione consigliata per il test perché il connettore Shopify può creare o modificare articoli e clienti. Può anche creare documenti di vendita come ordini e fatture. Questi documenti possono essere difficili da annullare.

Se devi utilizzare questa configurazione, ti consigliamo di rivedere e probabilmente disabilitare le seguenti impostazioni:

- **Crea automaticamente articolo sconosciuto** per non creare articoli.
- **Shopify può aggiornare gli articoli** per non aggiornare gli articoli mappati.
- **Crea automaticamente cliente sconosciuto** per non creare clienti e contatti.
- **Shopify può aggiornare i clienti** per non aggiornare i clienti esistenti.
- **Crea automaticamente ordine di vendita** per non creare ordini di vendita e fatture di vendita.

Per ulteriori informazioni, vedi [Ripristino di un ambiente](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### <a name="shopify-production-and-business-central-sandbox"></a>Produzione Shopify e sandbox Business Central

Potrebbe essere una buona idea eseguire il backup dei dati. Ad esempio, esporta i tuoi prodotti e clienti. Per ulteriori informazioni, vedi [Utilizzo di file CSV per eseguire il backup delle informazioni del punto vendita](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Disattiva l'interruttore **Consenti sincronizzazione dati a Shopify** in modo che [!INCLUDE[prod_short](../includes/prod_short.md)] non scriva su Shopify. In questo caso, potrai importare prodotti, immagini, clienti e ordini da Shopify. Ma non sarai in grado di inviare informazioni su articoli, prezzi, livelli di inventario, clienti, evasione ordini a Shopify.

Se mantieni abilitata l'opzione **Consenti sincronizzazione dati a Shopify** le misure di protezione aggiuntive sono:

- Seleziona **Bozza** nel campo **Stato per creazione prodotto** per assicurarti che i prodotti esportati non siano disponibili per gli acquirenti. Puoi verificare l'aspetto dei prodotti nel negozio online, sincronizzare prezzi, opzioni e livelli delle scorte. Assicurati di utilizzare i filtri nella pagina **Aggiungi articolo a Shopify** per limitare il numero di articoli esportati.
- Disattiva l'interruttore **Esporta cliente in Shopify** in modo da non inviare clienti a Shopify.

## <a name="see-also"></a>Vedere anche

[Procedura dettagliata: Impostazione e utilizzo di un connettore Shopify](walkthrough-setting-up-and-using-shopify.md)  

