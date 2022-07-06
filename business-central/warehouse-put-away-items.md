---
title: Stoccaggio degli articoli
description: Lo stoccaggio degli articoli dopo la ricezione o l'output viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5770, 5783, 5784, 5786, 5795, 7334, 7352, 7354, 7356, 7375, 7379, 7390, 7394, 7396, 9312, 9315, 9343
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 4ae110e18307105893e9ee3efccf136ff3efe02f
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079482"
---
# <a name="putting-items-away"></a>Stoccaggio di articoli

L'attività di warehouse di stoccaggio degli articoli dopo la ricezione o l'output viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse. La complessità può andare dall'assenza delle funzionalità di warehouse, alle configurazioni di warehouse di base per la gestione ordine per ordine in una o più attività, fino alle configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro guidato. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Se si decide di organizzare e di registrare informazioni di stoccaggio con documenti warehouse, inserire un segno di spunta nel campo **Richiesta stoccaggio** nella scheda Ubicazione. Ciò indica che, nel caso di articoli che giungono nell'ubicazione della warehouse mediante un documento di origine in entrata, lo stoccaggio di tali articoli dovrà essere controllato dal sistema. Un documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di produzione il cui output è pronto per lo stoccaggio.  

Se l'ubicazione è impostata per l'utilizzo dell'elaborazione degli stoccaggi ma non dei carichi, è necessario utilizzare la pagina **Stoccaggio magazzino** per organizzare le informazioni relative allo stoccaggio, stamparle, immettere i risultati dello stoccaggio effettivo e registrare tali informazioni, operazioni che comportano anche la registrazione delle informazioni relative al carico per il documento di origine. Nel caso di un ordine di produzione, il processo di registrazione comprende la registrazione dell'output dell'ordine e il completamento dell'ordine di produzione.

Se l'ubicazione è impostata per l'elaborazione dei carichi e degli stoccaggi, per cui è necessario immettere un segno di spunta nei campi **Richiesta carico** e **Richiesta stoccaggio** della scheda Ubicazione, per lo stoccaggio degli articoli è previsto un sistema diverso. In questo caso, viene utilizzata la pagina **Stoccaggio warehouse** per gestire lo stoccaggio. Lo stoccaggio warehouse presenta un funzionamento analogo a quello dello stoccaggio magazzino, ad eccezione del fatto che invece di registrare le informazioni viene registrato lo stoccaggio. Si noti che la registrazione dello stoccaggio warehouse non implica la registrazione del carico degli articoli. Viene solo aggiornato il contenuto collocazione. Il responsabile di warehouse può utilizzare i prospetti stoccaggio per organizzare le informazioni di stoccaggio prima di creare le istruzioni di stoccaggio dalla singola warehouse.

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

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/receive-put-away-items/)

## <a name="see-also"></a>Vedere anche

[Warehouse Management](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]