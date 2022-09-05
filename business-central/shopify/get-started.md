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
ms.openlocfilehash: e59dd0dcf757fbcf76d4068756adfe7bc9475f54
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361557"
---
# <a name="get-started-with-the-shopify-connector"></a>Iniziare a utilizzare il connettore Shopify

Collega il tuo negozio (o negozi) Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] e massimizza la produttività della tua azienda. Gestisci e visualizza le informazioni dettagliate della tua azienda e del tuo negozio Shopify come un'unica unità. 

Il connettore Shopify include le seguenti funzionalità:

- Supporto per più di un negozio Shopify  

  - Ogni negozio ha la propria configurazione, inclusa una raccolta di prodotti, posizioni utilizzate per calcolare l'inventario e listini prezzi.  
- Sincronizzazione bidirezionale di articoli o prodotti  

  - Il connettore sincronizzerà immagini, varianti articolo, codici a barre, numeri articolo fornitore, testi estesi e tag.  
  -    Esoirta gli attributi articolo in Shopify.  
  -    Utilizza gruppi di prezzi cliente e sconti selezionati per definire i prezzi esportati in Shopify.  
  -    Decidi se gli articoli possono essere creati automaticamente o consenti solo gli aggiornamenti ai prodotti esistenti.  
- Sincronizzazione dei livelli di inventario  

  -    Scegli alcune o tutte le posizioni disponibili in [!INCLUDE [prod_short](../includes/prod_short.md)].  
  -    Aggiorna i livelli di inventario in più posizioni in Shopify.  
- Sincronizzazione bidirezionale dei clienti  

  -    Mapping intelligente dei clienti per telefono ed e-mail.  
  -    Utilizza modelli specifici per paese durante la creazione dei clienti, il che aiuta a garantire che le impostazioni fiscali siano corrette.  
- Importare gli ordini da Shopify  

  -    Durante l'importazione, puoi creare automaticamente clienti in [!INCLUDE [prod_short](../includes/prod_short.md)] o decidere di gestire i clienti in Shopify.  
  -    Includi gli ordini creati in altri canali, ad esempio Shopify POS o Amazon.  
  -    Costi di spedizione, buoni regalo, mance, metodi di spedizione e pagamento, transazioni e rischio di frode.  
  - Ricevi informazioni sul pagamento da Shopify Payments.  
- Facile tracciabilità delle informazioni di evasione  

  -    Facoltativamente, scegli di scrivere le informazioni di tracciabilità dell'articolo da [!INCLUDE [prod_short](../includes/prod_short.md)] in Shopify.  

Per usare Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], devi prima fare un paio di cose. Questo articolo funge da guida per completare l'integrazione del tuo negozio Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Prerequisiti per Shopify

Devi avere:

- Un account Shopify
- Un negozio online con Shopify

Per creare un nuovo account Shopify o registrarti per una versione di valutazione gratuita di 14 giorni, vai a [Shopify](https://www.shopify.com/). Per ulteriori informazioni su come creare e personalizzare il tuo negozio online, vedi il [Centro assistenza Shopify](https://help.shopify.com/).
  
Sono supportati altri canali di vendita, ad esempio Shopify POS.

### <a name="recommended-settings"></a>Impostazioni consigliate

- Disattiva **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni [**Checkout**](https://www.shopify.com/admin/settings/checkout) nel tuo **Amministratore Shopify**.

Per altre informazioni sulle impostazioni di Shopify per scenari demo e di valutazione, vedere [Scenari di test e formazione ](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Prerequisiti per Business Central

- Assicurati che l'app **[Connettore Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** sia installata.

L'app è preinstallata per tutte le nuove iscrizioni e versioni di valutazione. Per ulteriori informazioni sull'installazione delle app da Marketplace, vedi [Installazione e disinstallazione delle estensioni](../ui-extensions-install-uninstall.md#install). Segui i passaggi elencati di seguito se non hai [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installazione dell'app **Dynamics 365 Business Central** nel tuo negozio Shopify online

Per [!INCLUDE[prod_short](../includes/prod_short.md)] esistente, questo passaggio è facoltativo e può essere saltato.

1. Individua l'app [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) in [Shopify AppStore](https://apps.shopify.com/)
2. Scegliere il pulsante **Aggiungi app**. Accedi al tuo account Shopify se richiesto. Seleziona il negozio online richiesto se ne hai più di uno.
3. Dopo aver esaminato la privacy e le autorizzazioni, scegli il pulsante **Installa app**.
  Puoi trovare e aprire l'app **Dynamics 365 Business Central** installata nella sezione **App** sulla barra laterale di **Amministratore Shopify**.
4. Scegli **Iscriviti ora** per iniziare una versione di valutazione di [!INCLUDE[prod_short](../includes/prod_short.md)] o **accedi** se già hai [!INCLUDE[prod_short](../includes/prod_short.md)]. Verrà eseguito il reindirizzamento a [!INCLUDE[prod_short](../includes/prod_short.md)] in [Business Central](https://businesscentral.dynamics.com).
5. I passaggi successivi devono essere eseguiti in [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Collegamento di Business Central al negozio online Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Negozio Shopify**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Codice** immettere il codice desiderato.  
4. Nel campo **URL Shopify**, digita l'URL del tuo negozio online, che deve essere collegato. Usa il seguente formato: `https://{shop}.myshopify.com/`.
5. Attiva l'opzione **Abilitato** , rivedi e accetta i termini e le condizioni.
6. Se richiesto, accedi al tuo account Shopify, rivedi privacy e autorizzazioni, quindi scegli il pulsante **Installa app**.

Ripeti i passaggi 2-6 per tutti i negozi online che si desidera collegare.

### <a name="next-steps"></a>Passaggi successivi

Ora il tuo negozio online è connesso a [!INCLUDE[prod_short](../includes/prod_short.md)]. Nei passaggi successivi definirai come e cosa sincronizzare.

- [Sincronizzazione elementi](synchronize-items.md)
- [Sincronizzare clienti](synchronize-customers.md)
- [Sincronizzare ordini](synchronize-orders.md)

## <a name="see-also"></a>Vedi anche

[Scenari di test e formazione](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

