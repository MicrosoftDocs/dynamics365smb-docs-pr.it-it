---
title: Risoluzione dei problemi di sincronizzazione tra Shopify e Business Central
description: Scopri cosa fare in caso di errore durante la sincronizzazione dei dati tra Shopify e Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 83678c6c81b29a524405699425be877459b6568d
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075319"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Risoluzione dei problemi di sincronizzazione tra Shopify Business Central

È possibile imbattersi in situazioni in cui è necessario risolvere i problemi quando si sincronizzano i dati tra Shopify e [!INCLUDE[prod_short](../includes/prod_short.md)]. Questa pagina definisce i passaggi per la risoluzione dei problemi di alcuni scenari comuni che potrebbero verificarsi.

## <a name="logs"></a>Log

Se un'attività di sincronizzazione non riesce, è possibile attivare la registrazione attivando **Abilita registro** nella **Scheda punto vendita Shopify**. Attiva manualmente l'attività di sincronizzazione e rivedi i log.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Movimenti di registri Shopify**, quindi scegli il collegamento correlato.
2. Seleziona la voce di registro correlata e apri la finestra **Voce di registro Shopify**.
3. Esamina la richiesta, il codice di stato e la descrizione e la risposta.

Ricordati di disattivare la registrazione per evitare un impatto negativo sulle prestazioni e aumentare le dimensioni del database.

Dalla finestra **Voci di registro Shopify**, è possibile attivare l'eliminazione di tutte le voci di registro o di quelle più vecchie di sette giorni.

## <a name="data-capture"></a>Acquisizione dati

Indipendentemente dalle impostazioni **Log attivato** alcune risposte da Shopify vengono sempre registrate in modo da poterle esaminare o scaricare tramite la finestra **Lista acquisizione dati**.

Scegli l'azione **Dati Shopify recuperati** in una delle seguenti pagine:

- **Ordine Shopify**
- **Evasioni ordini Shopify**
- **Costi di spedizione ordine Shopify**
- **Transazioni ordine Shopify**
- **Pagamenti Shopify**
- **Transazioni di pagamento Shopify**
- **Transazioni Shopify**

## <a name="reset-sync"></a>Reimposta sincronizzazione

Per prestazioni ottimali, il connettore importa solo clienti, prodotti e ordini creati o modificati dall'ultima sincronizzazione. Nella **Scheda punto vendita Shopify**, sono disponibili funzioni per modificare la data/ora dell'ultima sincronizzazione o ripristinarla completamente. Questa funzione garantisce che quando viene eseguita la sincronizzazione, tutti i dati vengano sincronizzati e non solo le modifiche dall'ultima sincronizzazione.

Questa funzione si applica solo alle sincronizzazioni da Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)] e può essere utile se è necessario ripristinare i dati eliminati come prodotti, clienti o ordini eliminati.

## <a name="request-the-access-token"></a>Richiedere il token di accesso

Se [!INCLUDE[prod_short](../includes/prod_short.md)] non è in grado di connettere il tuo account Shopify, prova a richiedere il token di accesso da Shopify. Questa richiesta potrebbe essere necessaria in caso di rotazione delle chiavi di sicurezza o modifiche alle autorizzazioni (ambito) richieste.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri recuperare il token di accesso per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Richiedi accesso**.
4. Se richiesto, accedi al tuo account Shopify.

L'interruttore **Con chiave di accesso** verrà attivato.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Verificare e abilitare le autorizzazioni per effettuare richieste HTTP durante l'esecuzione in un ambiente non di produzione

Per funzionare correttamente, l'estensione connettore Shopify richiede l'autorizzazione per effettuare richieste HTTP. Durante il test nel sandbox, le richieste HTTP sono vietate per tutte le estensioni.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Gestione estensioni**, quindi scegli il collegamento correlato.
2. Seleziona l'estensione *Connettore Shopify*.
3. Scegli l'azione **Configura** per aprire la pagina **Impostazione estensione**.
4. Assicurati che l'interruttore **Consenti richieste HTTPClient** sia abilitato.

## <a name="rotate-the-shopify-access-key"></a>Ruotare la chiave di accesso Shopify

Le procedure seguenti descrivono come ruotare il token di accesso utilizzato dal Connettore Shopify per accedere al tuo punto vendita Shopify online.

### <a name="in-shopify"></a>In Shopify

1. Da **Amministratore Shopify**, vai ad [App](https://www.shopify.com/admin/apps).
2. In fila con l'app **Dynamics 365 Business Central* seleziona **Elimina**.
3. Nel messaggio che verrà visualizzato, seleziona **Elimina**.

### <a name="in-prod_short"></a>In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi 1](../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") e immetti **Punti vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri ruotare il token di accesso per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Scegli l'azione **Richiedi accesso**.
4. Se richiesto, accedi al tuo account Shopify, rivedi privacy e autorizzazioni, quindi scegli il pulsante **Installa app**.

## <a name="see-also"></a>Vedere anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  