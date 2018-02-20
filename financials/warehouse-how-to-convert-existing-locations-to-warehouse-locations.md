---
title: 'Procedura: Convertire le ubicazioni esistenti in ubicazione warehouse | Documenti Microsoft'
description: "È possibile consentire l'utilizzo di zone e collocazioni in un'ubicazione magazzino esistente, in modo da utilizzare tale ubicazione come ubicazione warehouse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7d4b2c86174386faa86ab6c09faa463d26d3d2ac
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Convertire le ubicazioni esistenti in ubicazione warehouse
È possibile consentire l'utilizzo di zone e collocazioni in un'ubicazione magazzino esistente, in modo da utilizzare tale ubicazione come ubicazione warehouse.  

Il processo batch per l'abilitazione di un'ubicazione per le attività warehouse comporta la creazione di movimenti warehouse iniziali per la collocazione di rettifica della warehouse per tutti gli articoli in magazzino nell'ubicazione. Tali movimenti iniziali verranno convertiti quando i movimenti di inventario fisico della warehouse vengono immessi dopo l'esecuzione del processo batch.  

È possibile creare zone e collocazioni prima o dopo la conversione. L'unica collocazione da creare prima della conversione è quella da utilizzare come collocazione di rettifica futura.  

> [!IMPORTANT]  
>  Per eliminare tutte le giacenze negative ed eventuali documenti warehouse aperti prima di convertire l'ubicazione per la gestione warehouse, eseguire un report per identificare gli articoli con giacenza negativa e documenti warehouse aperti per l'ubicazione specificata. Per ulteriori informazioni, vedere Verifica giacenze negative.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Per abilitare un'ubicazione esistente come ubicazione di warehouse  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Crea ubicazione warehouse**, quindi scegliere il collegamento correlato.  
2.  Nel campo **Cod. ubicazione** specificare l'ubicazione che si desidera abilitare per l'elaborazione warehouse.  
3.  Nel campo **Codice collocazione rettifica** specificare la collocazione nell'ubicazione in cui sono archiviati i movimenti warehouse non sincronizzati. Per ulteriori informazioni, vedere la sezione "Per sincronizzare i movimenti warehouse rettificati con i movimenti contabili articoli correlati in [Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md).  

    Utilizzando i movimenti contabili articoli aperti per l'ubicazione specificata, vengono create righe di registrazione warehouse, in cui vengono riassunte tutte le combinazioni di Nr. Articolo, Cod. Variante, Cod. Unità di Misura e, se necessario, Nr. Lotto e Nr. Seriale nei movimenti contabili articoli. Le righe di registrazione warehouse vengono quindi registrate, in modo da creare movimenti warehouse che consentano di inserire il magazzino nella collocazione di rettifica della warehouse. Viene inoltre impostata l'opzione **Codice collocazione rettifica** nella scheda Ubicazione.  

4.  Per visualizzare gli articoli aggiunti alla collocazione di rettifica durante il processo batch, è possibile eseguire il report **Collocazione rettifica warehouse**.  
5.  Al termine del processo batch **Crea ubicazione warehouse**, eseguire e registrare un inventario fisico della warehouse. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  È consigliabile eseguire il processo batch **Crea ubicazione warehouse** in un orario che non ostacoli il funzionamento quotidiano del sistema. Durante il processo vengono elaborati tutti i movimenti disponibili nella tabella **Mov. contabili articoli**. Se il numero di movimenti è elevato, tale operazione potrebbe richiedere alcune ore.  

 Nel caso delle ubicazioni in cui i documenti di gestione della warehouse non venivano utilizzati prima della conversione, è necessario riaprire e rilasciare eventuali documenti di origine ricevuti parzialmente o spediti parzialmente prima della conversione.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

