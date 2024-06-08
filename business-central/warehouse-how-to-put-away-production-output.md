---
title: Stoccare l'output di produzione
description: Questo articolo descrive come stoccare l'output di produzione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Stoccare l'output produzione o l'output assemblaggio

La modalità di stoccaggio dell'output di produzione dipende dalla modalità di impostazione della warehouse come ubicazione. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).  

Nelle configurazioni di warehouse di base in cui l'ubicazione richiede l'elaborazione degli stoccaggi, utilizza il documento **Stoccaggio magazzino** per registrare l'output di produzione e lo stoccaggio dell'output.  

> [!NOTE]  
> I processi di assemblaggio non supportano gli stoccaggi di magazzino. Si registra un ordine di assemblaggio per registrare l'output. Se usi le collocazioni, puoi spostare gli articoli tra collocazioni in un secondo momento. Per ulteriori informazioni vedi [Spostare gli articoli ad hoc nelle configurazioni warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Nelle configurazioni di warehouse avanzate in cui l'ubicazione richiede sia l'elaborazione degli stoccaggi che dei carichi, crea un documento di stoccaggio interno oppure un documento di movimento per stoccare l'output.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Per eseguire lo stoccaggio dell'output di produzione con uno stoccaggio di magazzino

La prima fase del processo di stoccaggio dell'output prevede la creazione della richiesta warehouse in entrata. Questa richiesta comunica alla warehouse che l'output dell'ordine di produzione o assemblaggio è pronto per lo stoccaggio.

### <a name="to-create-the-inbound-warehouse-request"></a>Per creare la richiesta warehouse in entrata

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordine di produzione rilasciato**, quindi scegli il collegamento correlato.  
2. Scegli l'ordine di produzione pronto per lo stoccaggio e scegli l'azione **Crea richiesta whse. in entrata**.  

> [!NOTE]  
> È inoltre possibile creare la richiesta warehouse in entrata scegliendo il campo **Crea richiesta in entrata** quando si aggiorna l'ordine di produzione. Per ulteriori informazioni vedi [Ripianificare o aggiornare gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Per eseguire lo stoccaggio dell'output con uno stoccaggio di magazzino

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Stoccaggio in magazzino**, quindi scegli il collegamento correlato.  
2. Creare un nuovo stoccaggio di magazzino. Per ulteriori informazioni vedi [Eseguire lo stoccaggio con stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Per accedere all'output dell'ordine di produzione, scegliere l'azione **Prendi documenti origine** e selezionare l'ordine di produzione rilasciato.  
4. Compila debitamente le righe di stoccaggio.
5. Quando le righe sono pronte per la registrazione, scegliere l'azione **Registra**. Verranno creati i movimenti di warehouse e verrà registrato l'output degli articoli.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

È inoltre possibile creare uno **Stoccaggio magazzino** direttamente dall'ordine produzione rilasciato. Per ulteriori informazioni vedi [Eseguire lo stoccaggio con stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Quando registri uno stoccaggio magazzino, si presume che tutte le operazioni siano registrate in base al ciclo standard. Ovvero, la quantità di output viene registrata in base all'ultima operazione. È possibile utilizzare le registrazioni output per registrare variazioni nella quantità di output e tempi di lavorazione e setup. Se è necessario eseguire una registrazione parziale dopo lo stoccaggio magazzino, puoi farlo impostando tempi e quantità per tutte le operazioni, eccetto l'ultima. L'ultima operazione è controllata dallo stoccaggio magazzino.  

Se è necessario registrare il tempo di setup o di esecuzione sull'ultima operazione, imposta la quantità di output dell'ultima operazione su 0. Puoi scegliere di non registrare affatto l'ultima riga semplicemente eliminandola.

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Per stoccare l'output di produzione o assemblaggio in configurazioni di warehouse avanzate

Quando registri l'output dell'ordine di produzione o di assemblaggio nella warehouse che utilizza lo stoccaggio e il prelievo diretti, l'output viene posizionato nella collocazione definita nell'ordine di produzione o di assemblaggio. Scopri di più sui diversi modi per spostare gli articoli nella warehouse con le configurazioni avanzate, vai a [Spostare gli articoli nelle configurazioni warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Non è possibile inserire il numero del documento di origine, ad esempio il numero dell'ordine di produzione, nei documenti di stoccaggio interno, stoccaggio o movimento per processi di assemblaggio o output di produzione.  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
