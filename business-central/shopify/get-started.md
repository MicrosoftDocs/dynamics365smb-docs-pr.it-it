---
title: Iniziare con il connettore per Shopify
description: Primi passaggi per la configurazione della connessione tra Business Central e Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768152"
---
# <a name="get-started-with-the-shopify-connector"></a>Iniziare a utilizzare il connettore Shopify

[!INCLUDE [prod_short](../includes/prod_short.md)] offre la flessibilità necessaria per connettere il tuo negozio (o i tuoi negozi) Shopify con esso per massimizzare la produttività della tua azienda. Puoi gestire e visualizzare le informazioni dettagliate dalla tua attività e dal tuo negozio online Shopify come un'unica unità utilizzando il connettore Shopify. Per utilizzare Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], è necessario seguire alcuni passaggi. Questa pagina funge da guida per completare l'integrazione del tuo negozio Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Prerequisiti per Shopify

Devi avere:

- Un account Shopify
- Un negozio online con Shopify

Per creare un nuovo account Shopify o registrarti per una versione di valutazione gratuita di 14 giorni, vai a [Shopify](https://www.shopify.com/). Per ulteriori informazioni su come creare e personalizzare il tuo negozio online, vedi il [Centro assistenza Shopify](https://help.shopify.com/).
  
- Sono supportati altri canali di vendita, ad esempio Shopify POS.

### <a name="recommended-settings"></a>Impostazioni consigliate

- Disattiva **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni [**Checkout**](https://www.shopify.com/admin/settings/checkout) nel tuo **Amministratore Shopify**.

Per altre informazioni sulle impostazioni di Shopify per scenari demo e di valutazione, vedere [Scenari di test e formazione ](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Prerequisiti per Business Central

- Verifica che l'estensione **Connettiti a Shopify per [!INCLUDE[prod_short](../includes/prod_short.md)]** sia installata.

L'estensione è preinstallata per tutte le nuove iscrizioni e versioni di valutazione. Se hai bisogno di installare estensioni da Marketplace, visita [Installazione e disinstallazione delle estensioni](../ui-extensions-install-uninstall.md#install). Segui i passaggi elencati di seguito se non hai [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Collegamento di Business Central al negozio online Shopify

1. Vai alla ![lampadina che apre la funzione Dimmi.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Negozio Shopify**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Codice** immettere il codice desiderato.  
4. Nel campo **URL Shopify**, digita l'URL del tuo negozio online, che deve essere collegato.
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

