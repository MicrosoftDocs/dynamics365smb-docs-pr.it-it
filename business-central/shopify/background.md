---
title: Esegui attività in background e in modo ricorrente
description: Configura la sincronizzazione dei dati tra Business Central e Shopify in background.
ms.date: 05/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
ms.custom: bap-template
---

# <a name="run-tasks-in-the-background"></a>Eseguire attività in background

È efficiente eseguire alcune attività contemporaneamente e in modo automatizzato. È possibile eseguire tali attività in background e anche impostare una pianificazione quando si desidera che tali attività vengano eseguite automaticamente. Per eseguire attività in background, sono supportate due modalità:

- Le attività attivate manualmente vengono pianificate immediatamente tramite **Movimenti coda processi**.
- Le attività ricorrenti sono pianificate **Movimenti coda processi**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Eseguire attività in background per un negozio specifico

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Punto vendita Shopify**, quindi scegli il collegamento correlato.
2. Seleziona il punto vendita che desideri sincronizzare in background per l'apertura della pagina **Scheda del punto vendita Shopify**.
3. Attiva l'opzione **Consenti sincronizzazioni in background**.

Ora, quando viene attivata l'azione di sincronizzazione, anziché dell'esecuzione di un'attività in primo piano, ti viene chiesto di attendere. Al termine, puoi procedere con l'azione successiva. L'attività viene creata come **Movimento coda processi** e si avvia istantaneamente.

## <a name="to-schedule-recurring-tasks"></a>Per pianificare attività ricorrenti

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
|**Sincronizza società**|Report 30114 Sincronizzare le società Shopify (B2B)|
|**Sincronizzare i pagamenti**|Report 30105 Sincronizzare i pagamenti Shopify|
|**Sincronizza cataloghi**|Rapporto 30115 Sincronizzare i cataloghi Shopify (B2B)|
|**Sincronizza prezzi catalogo**|Report 30116 Sincronizza prezzi catalogo Shopify (B2B)|

> [!NOTE]
> Alcuni elementi potrebbero essere aggiornati da diverse attività. Ad esempio durante l'importazione di ordini, a seconda dell'impostazione nella pagina **Scheda punto vendita Shopify**, il sistema può anche importare e aggiornare i dati dei clienti e/o dei prodotti. Per evitare conflitti ricordati di utilizzare la stessa categoria della coda processi.
>
> Usa l'azione **Pagina di richiesta report** per definire i filtri. Ad esempio, puoi specificare di importare gli ordini solo quando il loro stato è **Interamente pagato**.

Altre attività che possono essere utili per automatizzare ulteriormente l'elaborazione dei documenti di vendita:

- Report 297 Agg. batch fatture vendite
- Report 296 Aggior. batch ordini vendita

È possibile utilizzare il campo **Nr. ordine Shopify** per identificare i documenti di vendita che sono stati importati da Shopify.

Per ulteriori informazioni sulla registrazione di ordini di vendita in un batch, vai a [Per creare un movimento coda processi per la registrazione batch degli ordini di vendita](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="to-check-the-status-of-synchronization"></a>Per verificare lo stato della sincronizzazione

Nella pagina Gestione ruolo utente **Manager aziendale**, la parte **Attività Shopify** offre diversi suggerimenti che possono aiutarti a identificare rapidamente se ci sono problemi con il connettore Shopify.

- **Clienti non mappati**: il cliente Shopify viene importato, ma non è collegato al movimento cliente corrispondente in [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Prodotti non mappati** - Il prodotto Shopify viene importato, ma non è collegato al movimento articolo corrispondente in [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Ordini non elaborati**: gli ordini Shopify vengono importati, ma i documenti di vendita in [!INCLUDE [prod_short](../includes/prod_short.md)] non sono stati creati, spesso a causa di prodotti o clienti non mappati.
- **Spedizioni non elaborate**: le spedizioni vendita registrate hanno avuto origine da ordini Shopify non sincronizzati con Shopify.
- **Errori spedizioni**: il connettore Shopify non ha sincronizzato le spedizioni vendita registrate con Shopify.
- **Errori di sincronizzazione**: sono presenti movimenti non riusciti nella coda dei processi relativi alla sincronizzazione con Shopify.

## <a name="see-also"></a>Vedere anche

[Introduzione al connettore Shopify](get-started.md)  
