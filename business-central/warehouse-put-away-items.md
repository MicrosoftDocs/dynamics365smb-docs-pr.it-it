---
title: Stoccare articoli | Documenti Microsoft
description: "L'attività di warehouse di stoccaggio degli articoli dopo la ricezione o l'output viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5e732e27921f632c3e15b1d832d7295d32f4b8a2
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="putting-items-away"></a>Stoccaggio di articoli
L'attività di warehouse di stoccaggio degli articoli dopo la ricezione o l'output viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse. La complessità può andare dall'assenza delle funzionalità di warehouse, alle configurazioni di warehouse di base per la gestione ordine per ordine in una o più attività, fino alle configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro guidato. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Se si decide di organizzare e di registrare informazioni di stoccaggio con documenti warehouse, inserire un segno di spunta nel campo **Richiesta stoccaggio** nella scheda Ubicazione. Ciò indica che, nel caso di articoli che giungono nell'ubicazione della warehouse mediante un documento di origine in entrata, lo stoccaggio di tali articoli dovrà essere controllato dal sistema. Un documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di produzione il cui output è pronto per lo stoccaggio.  

Se l'ubicazione è impostata per l'utilizzo dell'elaborazione degli stoccaggi ma non dei carichi, è necessario utilizzare la finestra **Stoccaggio magazzino** per organizzare le informazioni relative allo stoccaggio, stamparle, immettere i risultati dello stoccaggio effettivo e registrare tali informazioni, operazioni che comportano anche la registrazione delle informazioni relative al carico per il documento di origine. Nel caso di un ordine di produzione, il processo di registrazione comprende la registrazione dell'output dell'ordine e il completamento dell'ordine di produzione.

Se l'ubicazione è impostata per l'elaborazione dei carichi e degli stoccaggi, per cui è necessario immettere un segno di spunta nei campi **Richiesta carico** e **Richiesta stoccaggio** della scheda Ubicazione, per lo stoccaggio degli articoli è previsto un sistema diverso. In questo caso, viene utilizzata la finestra **Stoccaggio warehouse** per gestire lo stoccaggio. Lo stoccaggio warehouse presenta un funzionamento analogo a quello dello stoccaggio magazzino, ad eccezione del fatto che invece di registrare le informazioni viene registrato lo stoccaggio. Si noti che la registrazione dello stoccaggio warehouse non implica la registrazione del carico degli articoli. Viene solo aggiornato il contenuto collocazione. Il responsabile di warehouse può utilizzare i prospetti stoccaggio per organizzare le informazioni di stoccaggio prima di creare le istruzioni di stoccaggio dalla singola warehouse.

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Registrare il carico degli articoli direttamente dal documento dell'ordine in entrata e pertanto registrare lo stoccaggio poiché non esistono configurazioni della warehouse.|[Ricevere articoli](warehouse-how-receive-items.md)|  
|Stoccare gli articoli ordine per ordine e registrare il carico nella stessa attività, in una configurazione di base della warehouse.|[Eseguire lo stoccaggio con Stoccaggi Magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Stoccare gli articoli per più ordini in una configurazione avanzata della warehouse.|[Eseguire lo stoccaggio con Stoccaggi warehouse:](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Stoccare gli articoli prodotti o assemblati in una configurazione di base o avanzata della warehouse.|[Stoccare l'output produzione o l'output assemblaggio](warehouse-how-to-put-away-production-output.md)|
|Pianificare istruzioni di stoccaggio ottimizzate per diversi carichi warehouse registrati anziché lasciare che i lavoratori warehouse agiscano direttamente sui carichi.|[Pianificare stoccaggi nei prospetti](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Ricollocare gli articoli prelevati tecnicamente con un prelievo interno, ad esempio per un ordine di produzione per il quale non è stata utilizzata la quantità prevista.|[Selezionare e stoccare senza un documento di origine](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Dividere una riga di stoccaggio per inserire parte della quantità di stoccaggio nelle collocazioni disponibili in quanto la collocazione designata è piena.|[Suddividere righe attività warehouse](warehouse-how-to-split-warehouse-activity-lines.md)|
|Ottenere accesso immediato agli stoccaggi avuti in assegnazione in veste di lavoratore warehouse.|[Individuare le assegnazioni della warehouse](warehouse-how-to-find-your-warehouse-assignments.md)|    

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

