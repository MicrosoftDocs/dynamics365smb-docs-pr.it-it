---
title: Rapporti e analisi di inventario e warehouse
description: Vedere quali report e analisi di inventario e warehouse sono disponibili nella versione standard di Business Central in modo da poter tenere traccia della propria attività.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216376"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Rapporti e analisi di inventario e warehouse in Business Central

Il report di inventario e warehouse in [!INCLUDE [prod_short](includes/prod_short.md)] consente ai professionisti di inventario e aziendali di ottenere approfondimenti e statistiche sulle attività di inventario e warehouse attuali e passate.  

## <a name="reports"></a>Report

La tabella seguente descrive alcuni dei report di inventario e warehouse chiave.

|Report |ID oggetto|Descrizione  |
|---------|---------|---------|
|**Magazzino - Piano disponibilità**|707|Se desideri avere una panoramica su articoli/unità di stoccaggio specifici e sulla loro disponibilità. Questo report mostra i valori cumulati come i fabbisogni lordi, le entrate programmate e pianificate, l'inventario e così via. |
|**Valutazione magazzino**|1001|Visualizza la valutazione magazzino di articoli selezionati dall'inventario. Il report mostra inoltre informazioni sul valore degli aumenti e delle diminuzioni del magazzino nel tempo.|
|**Scadenza articolo - Quantità**|5809|Mostra una panoramica delle quantità degli articoli di magazzino selezionati le cui date di scadenza rientrano in un determinato periodo. Nell'elenco viene indicato il numero di unità dell'articolo selezionato che scadranno in un determinato periodo. Per ognuno degli articoli specificati durante il setup del report, nel documento stampato vengono indicati il numero di unità che scadranno durante ognuno dei tre periodi di uguale durata e la quantità di magazzino totale dell'articolo selezionato.<br>È possibile definire il contenuto del report impostando filtri. Se non si imposta alcun filtro, nel report verranno inclusi tutti i record. Le quantità indicate nel report riflettono solo le quantità dell'articolo per le quali sono state definite date di scadenza.|
|**Articolo Età Composizione - Quantità** o **Articolo Età Composizione - Valore**|5807 oppure 5808|Mostra una sintesi della composizione per età corrente di una selezione di articoli in giacenza. Nella lista viene visualizzato il numero di unità o valore dell'articolo selezionato che sono state aggiunte o eliminate dall'inventario e il momento in cui ciò è avvenuto. Gli articoli possono venire aggiunti o eliminati dalla giacenza in seguito ad acquisti, vendite o rettifiche positive e negative.|
|**Costo magazzino e listino prezzi**|716|Visualizza una lista di informazioni relative ai prezzi degli articoli o delle unità di stockkeeping selezionati: costo unitario diretto, ultimo costo diretto, prezzo unitario, percentuale di profitto e profitto. |
|**Lista collocazioni warehouse**|7319|Mostra una panoramica delle collocazioni di warehouse, la loro configurazione e la quantità di articoli all'interno delle collocazioni. Questo report può essere utilizzato per tutte le sedi che hanno "collocazione" come campo obbligatorio. |
|**Stato spedizione warehouse**|7313|Mostra una panoramica di documenti origine aperti con articoli spediti o da spedire per ubicazione. Questo rapporto può essere utilizzato per tutte le località in cui è abilitato **Richiedi spedizione**. **Stato della spedizione del magazzino** mostra ubicazioni, codici bin, stato del documento, quantità.|
|**Lista prelievi magazzino**|813|Visualizza una lista degli ordini vendita nei quali è incluso un determinato articolo. Per ogni articolo vengono visualizzate le seguenti informazioni: riga di ordine vendita con nome del cliente, codice variante, codice ubicazione, codice collocazione, data spedizione, quantità da spedire e unità di misura. Per ciascun articolo viene calcolato il totale della quantità da spedire. Il report può essere utilizzato quando gli articoli vengono prelevati dal magazzino.<br>NOTA : questa funzionalità non è disponibile per la funzionalità di warehouse avanzata.|
|**Collocazione rettifica warehouse**|7320|Questo report speciale è pensato solo per un magazzino avanzato e mostra le quantità rimanenti che sono ancora immagazzinate nella stessa collocazione di rettifica. Normalmente questa collocazione specifica dovrebbe essere vuoto. L'unico motivo per cui questa collocazione verrà completata è il risultato del processo di conteggio fisico o se quantità di articoli sono state rimosse o aggiunte al warehouse|


## <a name="tasks"></a>Attività

I seguenti articoli descrivono alcune delle attività chiave per analizzare lo stato del tuo business:

* [Creare report di analisi](bi-how-create-analysis-views-reports.md)  
* [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)


## <a name="see-also"></a>Vedere anche

[Impostazione del magazzino](inventory-setup-inventory.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)  
[Gestione warehouse](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
