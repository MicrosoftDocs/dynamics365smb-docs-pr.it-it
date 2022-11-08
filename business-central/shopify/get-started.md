---
title: Iniziare con il connettore per Shopify
description: Primi passaggi per la configurazione della connessione tra Business Central e Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b79691660ca84309057c3abab3d3a3df47271f58
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728412"
---
# <a name="get-started-with-the-shopify-connector"></a>Iniziare a utilizzare il connettore Shopify

Collega il tuo negozio (o negozi) Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] e massimizza la produttività della tua azienda. Gestisci e visualizza le informazioni dettagliate della tua azienda e del tuo negozio Shopify come un'unica unità.

Il connettore Shopify include le seguenti funzionalità:

- Supporto per più di un negozio Shopify.
  - Ogni negozio ha la propria configurazione, inclusa una raccolta di prodotti, posizioni utilizzate per calcolare l'inventario e listini prezzi.  
- Sincronizzazione bidirezionale di articoli o prodotti.
  - Il connettore sincronizzerà immagini, varianti articolo, codici a barre, numeri articolo fornitore, testi estesi e tag.  
  - Esoirta gli attributi articolo in Shopify.  
  - Utilizza gruppi di prezzi cliente e sconti selezionati per definire i prezzi esportati in Shopify.  
  - Decidi se gli articoli possono essere creati automaticamente o consenti solo gli aggiornamenti ai prodotti esistenti.  
- Sincronizzazione dei livelli di inventario.
  - Scegli alcune o tutte le posizioni disponibili in [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Aggiorna i livelli di inventario in più posizioni in Shopify.  
- Sincronizzazione bidirezionale dei clienti.
  - Mapping intelligente dei clienti per telefono ed e-mail.  
  - Utilizza modelli specifici per paese durante la creazione dei clienti, il che aiuta a garantire che le impostazioni fiscali siano corrette.  
- Importare gli ordini da Shopify.
  - Durante l'importazione, puoi creare automaticamente clienti in [!INCLUDE [prod_short](../includes/prod_short.md)] o decidere di gestire i clienti in Shopify.  
  - Includi gli ordini creati in altri canali, ad esempio Shopify POS o Amazon.  
  - Costi di spedizione, buoni regalo, mance, metodi di spedizione e pagamento, transazioni e rischio di frode.  
  - Ricevi informazioni sul pagamento da Shopify Payments.  
- Tracciabilità delle informazioni di evasione.
  - Facoltativamente, scegli di trasferire le informazioni di tracciabilità dell'articolo da [!INCLUDE [prod_short](../includes/prod_short.md)] a Shopify.  

Per usare Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], devi prima fare un paio di cose. Questo articolo funge da guida per integrare il tuo negozio Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Prerequisiti per Shopify

Devi avere:

- Un account Shopify.
- Un negozio online con Shopify.

Per creare un nuovo account Shopify o registrarti per una versione di valutazione gratuita di 14 giorni, vai a [Shopify.com](https://www.shopify.com/). Ulteriori informazioni su come creare e personalizzare il tuo negozio online in [Centro assistenza Shopify](https://help.shopify.com/).
  
Sono supportati altri canali di vendita, ad esempio Shopify POS.

### <a name="recommended-settings"></a>Impostazioni consigliate

- Disattiva **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni [**Checkout**](https://www.shopify.com/admin/settings/checkout) nel tuo **Amministratore Shopify**.

Ulteriori informazioni sulle impostazioni di Shopify per scenari demo e di valutazione, in [Scenari di test e formazione ](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Prerequisiti per Business Central

- Assicurati che l'app **[Connettore Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** sia installata.

L'app è preinstallata per tutte le nuove iscrizioni e versioni di valutazione. Per ulteriori informazioni sull'installazione delle app da AppSource, vedi [Installazione e disinstallazione delle estensioni](../ui-extensions-install-uninstall.md#install). Segui i passaggi elencati di seguito se non hai [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installa l'app Dynamics 365 Business Central nel tuo negozio Shopify online

Per [!INCLUDE[prod_short](../includes/prod_short.md)] esistente, questo passaggio è facoltativo e può essere saltato.

1. Individua l'app [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) in [Shopify AppStore](https://apps.shopify.com/)
2. Scegliere il pulsante **Aggiungi app**. Se richiesto, accedi al tuo account Shopify. Seleziona il negozio online richiesto se ne hai più di uno.
3. Dopo aver esaminato la privacy e le autorizzazioni, scegli il pulsante **Installa app**.

   Puoi trovare e aprire l'app **Dynamics 365 Business Central** installata nella sezione **App** sulla barra laterale della pagina **Amministratore Shopify**.
4. Scegli **Iscriviti ora** per iniziare una versione di valutazione di [!INCLUDE[prod_short](../includes/prod_short.md)] o **accedi** se hai già [!INCLUDE[prod_short](../includes/prod_short.md)]. Verrà eseguito il reindirizzamento alla pagina [Business Central](https://businesscentral.dynamics.com).
5. I passaggi successivi devono essere eseguiti in [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Collegamento di Business Central al negozio online Shopify

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Negozio Shopify**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.  
3. Nel campo **Codice**, inserisci il codice che lo renderà facilmente reperibile in [!INCLUDE[prod_short](../includes/prod_short.md)]. Il nome potrebbe riflettere ciò che un negozio vende, ad esempio "Mobili" o "Caffè", oppure il paese o la regione in cui opera.
4. Nel campo **URL Shopify**, digita l'URL del tuo negozio online, che deve essere collegato. Usa il seguente formato: `https://{shop}.myshopify.com/`.
5. Attiva l'interruttore **Abilitato**, rivedi e accetta i termini e le condizioni.
6. Se richiesto, accedi al tuo account Shopify, rivedi le condizioni di privacy e autorizzazioni, quindi scegli il pulsante **Installa app**.

Ripeti i passaggi 2-6 per tutti i negozi online che si desidera collegare.

> [!NOTE]
> Assicurati che il tuo browser non blocchi le finestre pop-up. Quando attivi l'interruttore **Abilitato** il sistema apre la pagina **In attesa di risposta, non chiudere questa pagina**, che è in attesa di un token di accesso da Shopify, se quella pagina è chiusa o bloccata, non puoi connetterti a Shopify. Ulteriori informazioni in [Richiedere il token di accesso](troubleshoot.md#request-the-access-token)

### <a name="next-steps"></a>Passaggi successivi

Ora il tuo negozio online è connesso a [!INCLUDE[prod_short](../includes/prod_short.md)]. Nei passaggi successivi definirai come e cosa sincronizzare.

- [Sincronizzazione elementi](synchronize-items.md)
- [Sincronizzare clienti](synchronize-customers.md)
- [Sincronizzare ordini](synchronize-orders.md)

## <a name="see-also"></a>Vedere anche

[Scenari di test e formazione](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).
