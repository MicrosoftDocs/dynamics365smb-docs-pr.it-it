---
title: Impostare i tipi di collocazioni
description: 'Assegna tipi e attività di flusso di base alle collocazioni e, in tal modo, definisci il modo in cui le collocazioni vengono utilizzate per particolari attività di magazzino.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: bholtorf
---
# <a name="set-up-bin-types"></a>Impostare i tipi di collocazioni

È possibile controllare e gestire il flusso degli articoli attraverso le collocazioni definite per determinate attività di warehouse. È possibile associare attività di flusso di base alle collocazioni e definire di conseguenza la modalità con cui una collocazione verrà utilizzata, assegnando un tipo a ciascuna collocazione.  

Esistono sei tipi. È possibile gestire la warehouse con tutti e sei i tipi di collocazione o scegliere di utilizzare solo i tipi di collocazione RECEIVE, PUTPICK, SHIP e QC. Questi quattro tipi di collocazione consentono di creare suggerimenti per supportare il flusso di articoli e di registrare le discrepanze di magazzino.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Per impostare i tipi di collocazione da utilizzare

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tipi collocazione**, quindi scegli il collegamento correlato.  
2.  Nella pagina **Tipi collocazione** creare un codice di 10 caratteri per un tipo di collocazione.  
3.  Selezionare le attività che è possibile svolgere con ogni tipo di collocazione.  

> [!NOTE]  
>  I tipi di collocazione sono applicabili solo se si utilizzano stoccaggi e prelievi guidati per l'ubicazione.  

Il tipo di collocazione determina solo la modalità di utilizzo di una collocazione durante l'elaborazione del flusso degli articoli all'interno della warehouse. Sarà comunque possibile ignorare i suggerimenti per qualsiasi documento di warehouse, nonché inserire o prelevare articoli da qualsiasi collocazione eseguendo una movimentazione warehouse.  

Di seguito sono riportati i tipi di collocazione che è possibile creare.  

|Tipo collocazione|Description|  
|------------------|---------------------------------------|  
|AREARICEV|Articoli registrati come carichi registrati ma non ancora stoccati.|  
|SHIP|Articoli prelevati in base alle righe di spedizione warehouse ma non ancora registrati come spediti.|  
|PUT AWAY|In genere, articoli da archiviare in grandi unità di misura, ma a cui non si desidera accedere a scopo di prelievo. Poiché le collocazioni non vengono utilizzate per il prelievo, per gli ordini di produzione o per le spedizioni, l'utilizzo di una collocazione di tipo stoccaggio può essere limitato, ma questo tipo di collocazione può essere utile nel caso in cui venga acquistato un notevole quantitativo di articoli. Si consiglia di assegnare sempre a collocazioni di questo tipo una valutazione di collocazione bassa in modo che, quando gli articoli ricevuti vengono stoccati, vengano stoccate per prime altre collocazioni di tipo PUTPICK con valutazione più alta associate in modo fisso a tali articoli. Se si utilizza questo tipo di collocazione, sarà necessario eseguire periodicamente il rifornimento delle collocazioni in modo che gli articoli immagazzinati nelle collocazioni di questo tipo siano anche disponibili nelle collocazioni di tipo PUTPICK o PICK.|  
|PICK|Articoli da utilizzare solo per il prelievo, ad esempio articoli prossimi alla data di scadenza che sono stati spostati in questo tipo di collocazione. Si consiglia di assegnare a queste collocazioni una valutazione alta, in modo che vengano suggerite in prima istanza per il prelievo.|  
|PUTPICK|Articoli nelle collocazioni suggerite per le funzioni di stoccaggio e di prelievo. Collocazioni di questo tipo hanno presumibilmente valutazioni differenti. È possibile impostare le collocazioni di immagazzinamento a massa come collocazioni di questo tipo con valutazioni basse rispetto alle collocazioni di prelievo ordinarie o alle collocazioni di prelievo in sequenza da inizio ordine.|  
|QC|Questa collocazione viene utilizzata per le rettifiche di magazzino, se la si specifica nel campo **Codice collocazione rettifica** della scheda Ubicazione. È inoltre possibile impostare collocazioni di questo tipo per gli articoli difettosi e gli articoli che vengono controllati. È possibile spostare articoli in collocazioni di questo tipo se si desidera renderli inaccessibili al normale flusso degli articoli.<br /><br /> **NOTA:** A differenza di tutti gli altri tipi di collocazione, il tipo di collocazione **QC** non dispone di alcuna delle caselle di controllo per la gestione degli articoli selezionate per default. Ciò indica che tutti i contenuti inseriti in una collocazione QC sono esclusi dai flussi degli articoli.|  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
