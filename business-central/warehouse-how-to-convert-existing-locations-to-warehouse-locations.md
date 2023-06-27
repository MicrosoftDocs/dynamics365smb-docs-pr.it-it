---
title: Convertire le ubicazioni esistenti in ubicazione warehouse
description: 'È possibile consentire l''utilizzo di zone e collocazioni in un''ubicazione magazzino esistente, in modo da utilizzare tale ubicazione come ubicazione warehouse.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 15
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Convertire le ubicazioni esistenti in ubicazione warehouse
È possibile consentire l'utilizzo di zone e collocazioni in un'ubicazione magazzino esistente, in modo da utilizzare tale ubicazione come ubicazione warehouse.  

Il processo batch per l'abilitazione di un'ubicazione per le attività warehouse comporta la creazione di movimenti warehouse iniziali per la collocazione di rettifica della warehouse per tutti gli articoli in magazzino nell'ubicazione. Tali movimenti iniziali verranno convertiti quando i movimenti di inventario fisico della warehouse vengono immessi dopo l'esecuzione del processo batch.  

È possibile creare zone e collocazioni prima o dopo la conversione. L'unica collocazione da creare prima della conversione è quella da utilizzare come collocazione di rettifica futura.  

> [!IMPORTANT]  
>  Per eliminare tutte le giacenze negative ed eventuali documenti warehouse aperti prima di convertire l'ubicazione per la gestione warehouse, eseguire un report per identificare gli articoli con giacenza negativa e documenti warehouse aperti per l'ubicazione specificata. Per ulteriori informazioni, vedere Verifica giacenze negative.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Per abilitare un'ubicazione esistente come ubicazione di warehouse
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Crea ubicazione warehouse**, quindi scegli il collegamento correlato.  
2.  Nel campo **Cod. ubicazione** specificare l'ubicazione che si desidera abilitare per l'elaborazione warehouse.  
3.  Nel campo **Codice collocazione rettifica** specificare la collocazione nell'ubicazione in cui sono archiviati i movimenti warehouse non sincronizzati. Per ulteriori informazioni, vedere [Per sincronizzare i movimenti warehouse rettificati con i movimenti contabili articoli correlati](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)  

    Utilizzando i movimenti contabili articoli aperti per l'ubicazione specificata, vengono create righe di registrazione warehouse, in cui vengono riassunte tutte le combinazioni di Nr. Articolo, Cod. Variante, Cod. Unità di Misura e, se necessario, Nr. Lotto e Nr. Seriale nei movimenti contabili articoli. Le righe di registrazione warehouse vengono quindi registrate, in modo da creare movimenti warehouse che consentano di inserire il magazzino nella collocazione di rettifica della warehouse. Viene inoltre impostata l'opzione **Codice collocazione rettifica** nella scheda Ubicazione.  

4.  Per visualizzare gli articoli aggiunti alla collocazione di rettifica durante il processo batch, è possibile eseguire il report **Collocazione rettifica warehouse**.  
5.  Al termine del processo batch **Crea ubicazione warehouse**, eseguire e registrare un inventario fisico della warehouse. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni ](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  È consigliabile eseguire il processo batch **Crea ubicazione warehouse** in un orario che non ostacoli il funzionamento quotidiano del sistema. Durante il processo vengono elaborati tutti i movimenti disponibili nella tabella **Mov. contabili articoli**. Se il numero di movimenti è elevato, tale operazione potrebbe richiedere alcune ore.  

 Nel caso delle ubicazioni in cui i documenti di gestione della warehouse non venivano utilizzati prima della conversione, è necessario riaprire e rilasciare eventuali documenti di origine ricevuti parzialmente o spediti parzialmente prima della conversione.  

## <a name="see-also"></a>Vedere anche
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
