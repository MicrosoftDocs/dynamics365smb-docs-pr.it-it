---
title: Mettere da parte la produzione in uscita
description: Questo articolo descrive come stoccare l'output di produzione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# Mettere da parte l'output di produzione o di assemblaggio

La modalità di stoccaggio dell'output di produzione dipende dalla modalità di impostazione della warehouse come ubicazione. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).  

In una configurazione di magazzino di base per il flusso in entrata (stoccaggio), nella pagina  **Posizione scheda** per la posizione, attivare le seguenti impostazioni:

* Per la produzione, nel campo  **Prod. Output Whse. Handling**, Seleziona **Inventario stoccaggio**.
* I processi di assemblaggio non supportano gli stoccaggi di magazzino. Si registra un ordine di assemblaggio per registrare l'output. Se usi le collocazioni, puoi spostare gli articoli tra collocazioni in un secondo momento. Per ulteriori informazioni vedi [Spostare gli articoli ad hoc nelle configurazioni warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* Per i progetti, la messa da parte non è applicabile.

Nelle configurazioni di magazzino avanzate in cui è necessario riporre una posizione, creare un documento di stoccaggio interno o un documento di movimento per riporre l'output.  

## Per eseguire lo stoccaggio dell'output di produzione con uno stoccaggio di magazzino

La prima fase del processo di stoccaggio dell'output prevede la creazione della richiesta warehouse in entrata. Questa richiesta comunica alla warehouse che l'output dell'ordine di produzione o assemblaggio è pronto per lo stoccaggio.

### Per creare la richiesta warehouse in entrata  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordine di produzione rilasciato**, quindi scegli il collegamento correlato.  
2. Scegli l'ordine di produzione pronto per lo stoccaggio e scegli l'azione **Crea richiesta whse. in entrata**.  

> [!NOTE]  
> È inoltre possibile creare la richiesta warehouse in entrata scegliendo il campo **Crea richiesta in entrata** quando si aggiorna l'ordine di produzione. Per ulteriori informazioni vedi [Ripianificare o aggiornare gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).  

### Per mettere via l'output con un inventario di stoccaggio  

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Stoccaggio in magazzino**, quindi scegli il collegamento correlato.  
2. Creare un nuovo stoccaggio di magazzino. Per ulteriori informazioni vedi [Eseguire lo stoccaggio con stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Per accedere all'output dell'ordine di produzione, scegliere l'azione **Prendi documenti origine** e selezionare l'ordine di produzione rilasciato.  
4. Compila debitamente le righe di stoccaggio.
5. Quando le righe sono pronte per la registrazione, scegliere l'azione **Registra**. La registrazione crea le voci di magazzino e registra l'output degli articoli.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

È inoltre possibile creare uno **Stoccaggio magazzino** direttamente dall'ordine produzione rilasciato. Per ulteriori informazioni vedi [Eseguire lo stoccaggio con stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Quando si registra un deposito di inventario, si presuppone che tutte le operazioni vengano registrate secondo il routing standard. [!INCLUDE [prod_short](includes/prod_short.md)]  Ovvero, la quantità di output viene registrata in base all'ultima operazione. È possibile utilizzare le registrazioni output per registrare variazioni nella quantità di output e tempi di lavorazione e setup. Se è necessario contabilizzare una parte dopo aver creato l'inventario di stoccaggio, è possibile farlo sui tempi di preparazione e sulle quantità per tutte le operazioni, tranne l'ultima. L'inventario di stoccaggio controlla l'ultima operazione.  

Se è necessario registrare solo il tempo di installazione o di esecuzione nell'ultima operazione, impostare la quantità di output nell'ultima operazione su 0. Puoi scegliere di non pubblicare affatto l'ultima riga, semplicemente eliminandola.

## Per riporre i prodotti di assemblaggio e produzione in configurazioni di magazzino avanzate

Quando si registra l'output di un ordine di produzione o di assemblaggio in un magazzino che utilizza lo stoccaggio e il prelievo guidati, l'output viene inserito nel contenitore definito nell'ordine di produzione o di assemblaggio. Per saperne di più sui diversi modi per spostare gli articoli nel magazzino con configurazioni avanzate, vai a  [Spostare articoli nelle configurazioni avanzate del magazzino](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Non è possibile inserire il numero del documento di origine, ad esempio il numero dell'ordine di produzione, nei documenti di stoccaggio interno, stoccaggio o movimento per processi di assemblaggio o output di produzione.  

## Vedere anche  

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
