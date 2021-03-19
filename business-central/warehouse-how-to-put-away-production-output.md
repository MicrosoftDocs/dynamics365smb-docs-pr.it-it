---
title: Stoccare l'output di produzione
description: La modalità di stoccaggio dell'output di produzione dipende dalla modalità di impostazione della warehouse come ubicazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e97f0e13f7b07ff59fd05908b6a3239d6cf70ebd
ms.sourcegitcommit: 026484766988b8727649c02fc8990b0646999bf1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5498639"
---
# <a name="put-away-production-or-assembly-output"></a>Stoccare l'output produzione o l'output assemblaggio

La modalità di stoccaggio dell'output di produzione dipende dalla modalità di impostazione della warehouse come ubicazione. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).  

Nelle configurazioni di warehouse di base in cui l'ubicazione richiede l'elaborazione degli stoccaggi, utilizzare il documento **Stoccaggio magazzino** per registrare l'output di produzione e lo stoccaggio dell'output.  

> [!NOTE]  
> Lo stoccaggio di magazzino non è supportato per i processi di assemblaggio. Si registra un ordine di assemblaggio per registrare l'output. Se si utilizzano le collocazioni, è possibile spostare gli articoli tra collocazioni in un secondo momento. Per ulteriori informazioni, vedere [Spostare articoli ad hoc nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Nelle configurazioni di warehouse avanzate in cui l'ubicazione richiede sia l'elaborazione degli stoccaggi che dei carichi, è possibile creare un documento di stoccaggio interno oppure un documento di movimento per stoccare l'output.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Per eseguire lo stoccaggio dell'output di produzione con uno stoccaggio di magazzino

La prima fase del processo di creazione dello stoccaggio dell'output prevede la creazione della richiesta warehouse in entrata. Questa richiesta comunica alla warehouse che l'output dell'ordine di produzione o assemblaggio è pronto per lo stoccaggio.

### <a name="to-create-the-inbound-warehouse-request"></a>Per creare la richiesta warehouse in entrata  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordine produzione rilasciato** e quindi scegliere il collegamento correlato.  
2.  Nell'ordine di produzione pronto per lo stoccaggio, scegliere l'azione **Crea richiesta whse. in entrata**.  

> [!NOTE]  
> È inoltre possibile creare la richiesta warehouse in entrata scegliendo il campo **Crea richiesta in entrata** quando si aggiorna l'ordine di produzione. Per ulteriori informazioni, vedere [Ripianificare o aggiornare gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Per eseguire lo stoccaggio dell'output con uno stoccaggio di magazzino  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stoccaggio in magazzino** e quindi scegliere il collegamento correlato.  
2.  Creare un nuovo stoccaggio di magazzino. Per ulteriori informazioni, vedere [Stoccare articoli con gli stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Per accedere all'output dell'ordine di produzione, scegliere l'azione **Prendi documenti origine** e selezionare l'ordine di produzione rilasciato.  
4.  Compilare debitamente le righe di stoccaggio.
5.  Quando le righe sono pronte per la registrazione, scegliere l'azione **Registra**. Verranno creati i movimenti di warehouse necessari e verrà registrato l'output degli articoli.  

È inoltre possibile creare uno **Stoccaggio magazzino** direttamente dall'ordine produzione rilasciato. Per ulteriori informazioni, vedere [Stoccare articoli con gli stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Quando si registra uno stoccaggio magazzino, si presume che tutte le operazioni siano registrate in base al ciclo standard, ovvero la quantità di output viene registrata in base all'ultima operazione. È possibile utilizzare le registrazioni output per registrare variazioni nella quantità di output e tempi di lavorazione e setup. Se è necessario eseguire una registrazione parziale dopo lo stoccaggio magazzino, è possibile farlo nel setup di tempi e quantità per tutte le operazioni, eccetto l'ultima. In questo caso, l'ultima operazione è controllata dallo stoccaggio magazzino.  

Se è necessario registrare il tempo di setup o di esecuzione sull'ultima operazione, impostare la quantità di output dell'ultima operazione su 0. In alternativa, è possibile scegliere di non registrare affatto l'ultima riga semplicemente eliminandola  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Per stoccare l'output di produzione o assemblaggio in configurazioni di warehouse avanzate
Quando si registra l'output dell'ordine di produzione o di assemblaggio nella warehouse impostata per utilizzare lo stoccaggio e il prelievo diretti, l'output viene posizionato nella collocazione definita nell'ordine di produzione o di assemblaggio. 

La tabella seguente descrive i diversi modi di spostare gli articoli all'interno della warehouse con configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro diretto. 

|**Per**|**Vedere**|  
|------------|-------------|  
|Spostare gli articoli con il prospetto movimentazioni warehouse.|[Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Creare uno stoccaggio interno per stoccare gli articoli prodotti o assemblati in una configurazione di warehouse avanzata.|[Creare uno stoccaggio interno](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Entrambe le procedure non prevedono l'immissione del numero del documento di origine, ad esempio il numero dell'ordine di produzione, nei documenti per operazioni di stoccaggio interno, stoccaggio o movimentazione.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
