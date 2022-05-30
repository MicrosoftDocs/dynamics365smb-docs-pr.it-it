---
title: Risoluzione dei problemi di sincronizzazione tra Shopify e Business Central
description: Scopri cosa fare in caso di errore durante la sincronizzazione dei dati tra Shopify e Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 01ff5ab1c5e6f132098f914f6bfe97e097cc88b0
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768162"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Risoluzione dei problemi di sincronizzazione tra Shopify Business Central

È possibile imbattersi in situazioni in cui è necessario risolvere i problemi. Questa pagina definisce i passaggi per la risoluzione dei problemi di alcuni scenari comuni che potrebbero verificarsi.

## <a name="logs"></a>Log

Se un'attività di sincronizzazione non riesce, è possibile attivare la registrazione attivando **Abilita registro** nella **Scheda punto vendita Shopify**. Attiva manualmente l'attività di sincronizzazione e rivedi i log.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Movimenti di registri Shopify**, quindi scegli il collegamento correlato.
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

## <a name="update-the-access-token"></a>Aggiornare il token di accesso

Se [!INCLUDE[prod_short](../includes/prod_short.md)] non è in grado di connettere il tuo account Shopify, prova a reimpostare il token di accesso.

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita per il quale desideri recuperare il token di accesso per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Nel campo **Codice** immetti il primo codice.  
4. Scegli l'azione **Richiedi accesso**.
5. Se richiesto, accedi al tuo account Shopify.

## <a name="see-also"></a>Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
