---
title: Esegui attività in background e in modo ricorrente
description: Configura la sincronizzazione dei dati tra Business Central e Shopify in background.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
---

# <a name="run-tasks-in-the-background" />Eseguire attività in background

È efficiente eseguire alcune attività contemporaneamente e in modo automatizzato. È possibile eseguire tali attività in background e anche impostare una pianificazione quando si desidera che tali attività vengano eseguite automaticamente. Per eseguire attività in background, sono supportate due modalità:

- Le attività attivate manualmente vengono pianificate immediatamente tramite **Movimenti coda processi**.
- Le attività ricorrenti sono pianificate **Movimenti coda processi**.

## <a name="run-tasks-in-the-background-for-a-specific-shop" />Eseguire attività in background per un negozio specifico

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita che desideri sincronizzare in background per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Attiva l'opzione **Consenti sincronizzazioni in background**.

Ora, quando viene attivata l'azione di sincronizzazione, invece di un'attività in esecuzione in primo piano, ti verrà chiesto di attendere. Al termine, puoi procedere con l'azione successiva. L'attività viene creata come **Movimento coda processi** e si avvia istantaneamente.

## <a name="to-schedule-recurring-tasks" />Per pianificare attività ricorrenti

È possibile pianificare le seguenti attività ricorrenti da eseguire in modo automatizzato. Per ulteriori informazioni sulla pianificazione di attività, vedi [Coda processi](../admin-job-queues-schedule-tasks.md).

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

> [!NOTE]
> Alcuni elementi potrebbero essere aggiornati da diverse attività, ad esempio durante l'importazione degli ordini, a seconda dell'impostazione in **Scheda punto vendita Shopify**, il sistema può anche importare e aggiornare i dati dei clienti e/o dei prodotti. Ricordati di utilizzare la stessa categoria della coda processi per evitare conflitti.

Altre attività che possono essere utili per automatizzare ulteriormente l'elaborazione dei documenti di vendita:

- report 297 Agg. batch fatture vendite
- report 296 Aggior. batch ordini vendita

È possibile utilizzare il campo **Nr. ordine Shopify** per identificare i documenti di vendita che sono stati importati da Shopify.

Per ulteriori informazioni sulla registrazione di ordini di vendita in un batch, vai a [Per creare un movimento coda processi per la registrazione batch degli ordini di vendita](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="see-also" />Vedere anche

[Iniziare a usare il connettore per Shopify](get-started.md)  
