---
title: Eseguire attività in background
description: Configura la sincronizzazione dei dati tra Business Central e Shopify in background.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768134"
---
# <a name="run-tasks-in-the-background"></a>Eseguire attività in background

È efficiente eseguire alcune attività contemporaneamente e in modo automatizzato. È possibile eseguire tali attività in background e anche impostare una pianificazione quando si desidera che tali attività vengano eseguite automaticamente. Per eseguire attività in background, sono supportate due modalità:

- Le attività attivate manualmente vengono pianificate immediatamente tramite **Movimenti coda processi**
- Le attività ricorrenti sono pianificate **Movimenti coda processi**

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Eseguire attività in background per un negozio specifico

1. Vai alla ![lampadina che apre la funzione Dimmi](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") della ricerca. icona, inserisci il nome del **negozio Shopify** e scegli il nome del negozio dall'elenco.
2. Seleziona il punto vendita per il quale desideri sincronizzare gli articoli per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Abilita l'opzione **Consenti sincronizzazioni in background**.

Ora, quando viene attivata l'azione di sincronizzazione, invece di un'attività in esecuzione in primo piano, ti verrà chiesto di attendere. Al termine, puoi procedere con l'azione successiva. L'attività viene creata come **Movimento coda processi** e si avvia istantaneamente in modo non bloccante.

## <a name="to-schedule-recurring-tasks"></a>Per pianificare attività ricorrenti

È possibile pianificare le seguenti attività ricorrenti da eseguire in modo automatizzato. Per ulteriori informazioni sulla pianificazione delle attività, vedi [Coda processi](../admin-job-queues-schedule-tasks.md).

|Attività|Oggetto|
|------|------------|
|**Sincronizzare ordini da Shopify**|Report 30104 Sincronizzare ordini da Shopify|
|**Elaborare ordini di Shopify**|Report 30103 Creazione di ordini di vendita Shopify|
|**Sincronizzare le spedizioni con ShopifyShopify**|Report 30109 Sincronizzare la spedizione con Shopify|
|**Sincronizzare prodotti e/o prezzi**|Rapporto 30108 Sincronizzare i prodotti Shopify|
|**Sincronizzare l'inventario**|Report 30102 Sincronizzare le scorte con Shopify|
|**Sincronizzare le immagini**|Report 30107 Sincronzzare le immagini Shopify|
|**Sincronizzare i clienti**|Rapporto 30100 Sincronizzare i clienti Shopify|
|**Sincronizzare i pagamenti**|Report 30105 Sincronizzare i pagamenti Shopify|

## <a name="see-also"></a>Vedi anche

[Iniziare a utilizzare il connettore per Shopify](get-started.md)  
