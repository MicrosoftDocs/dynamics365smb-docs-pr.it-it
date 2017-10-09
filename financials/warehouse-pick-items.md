---
title: Prelevare articoli | Documenti Microsoft
description: "L'attività di warehouse di prelievo degli articoli prima della spedizione o dell'utilizzo viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse. La complessità [delle operazioni di setup](../configure-warehouse-processes.md) può andare dall'assenza delle funzionalità di warehouse, alle configurazioni di warehouse di base per la gestione ordine per ordine in una o più attività, fino alle configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro guidato."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 13db47dcfcc7eb6d30230490baa5ac961fc825a8
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="pick-items"></a>Prelievo degli articoli
L'attività di warehouse di prelievo degli articoli prima della spedizione o dell'utilizzo viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse. La complessità può andare dall'assenza delle funzionalità di warehouse, alle configurazioni di warehouse di base per la gestione ordine per ordine in una o più attività, fino alle configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro guidato. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Se si decide di organizzare e di registrare l'attività di prelievo associata a documenti di warehouse, inserire un segno di spunta nel campo **Richiesto prelievo** nella scheda Ubicazione. Ciò indica che, nel caso di articoli che devono essere prelevati per un documento di origine in uscita, il prelievo dovrà essere controllato dal sistema. Un documento di origine in uscita può essere un ordine di vendita, un ordine di reso da acquisto, un ordine di trasferimento in uscita, un ordine di assistenza o un ordine di produzione di cui è richiesto il prelievo dei componenti.

> [!NOTE]
> Anche se l'impostazione è chiamata **Richiesto prelievo**, è possibile registrare carichi e spedizioni direttamente dal documento aziendale di origine nell'ubicazione in cui si seleziona questa casella di controllo.

Se l'ubicazione è impostata per la richiesta dell'elaborazione del prelievo, ma non della spedizione, è necessario utilizzare la finestra **Prelievo magazzino** per organizzare le informazioni relative al prelievo, stamparle, immettere i risultati del prelievo e registrare tali informazioni, operazioni che comportano anche la spedizione degli articoli. Nel caso del prelievo di componenti per un ordine di produzione, la registrazione del prelievo comprende anche il consumo.

Se l'ubicazione è impostata in modo da richiedere l'elaborazione di prelievi e di spedizioni, inserendo un segno di spunta nei campi **Richiesta prelievo** e **Richiesta spedizione** della scheda Ubicazione, occorrerà utilizzare la finestra **Prelievo warehouse** per gestire il prelievo. Il prelievo warehouse presenta un funzionamento analogo a quello di magazzino, ad eccezione del fatto che invece di registrare le informazioni sul prelievo viene registrato il prelievo stesso. Tale processo non include la registrazione della spedizione ma semplicemente rende disponibili gli articoli per la spedizione. Il responsabile di warehouse può utilizzare i prospetti prelievi per organizzare le informazioni di prelievo prima di creare le istruzioni di prelievo dalla singola warehouse.

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|
|------------|-------------|  
|Registrare la spedizione degli articoli direttamente nel documento ordine in uscita in quanto non sono disponibili funzionalità di warehouse. (Funzionamento analogo per ordini di vendita, ordini di trasferimento in uscita e spedizioni di reso.)|[Procedura: Spedire articoli](warehouse-how-ship-items.md)|  
|Prelevare gli articoli ordine per ordine e registrare la spedizione nella stessa attività, in una configurazione di base della warehouse.|[Procedura: prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Prelevare gli articoli per più ordini in una configurazione avanzata della warehouse.|[Procedura: Prelevare articoli con prelievi warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Prelevare i componenti per la produzione o l'assemblaggio in una configurazione di base o avanzata della warehouse.|[Procedura: Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md)|  
|Pianificare istruzioni di prelievo ottimizzate per diverse spedizioni anziché lasciare che i lavoratori warehouse agiscano direttamente sulle spedizioni registrate.|[Procedura: Pianificare prelievi nei prospetti](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Prelevare tecnicamente gli articoli per uno scopo specifico, ad esempio per un'unità di produzione che necessita di componenti aggiuntivi, in modo che gli articoli non escano tecnicamente dalla warehouse.|[Procedura: Selezionare e stoccare senza un documento di origine](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Comprendere come prelevare automaticamente gli articoli in base alla loro data di scadenza, ad esempio beni deperibili.|[Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md)|
|Dividere una riga di prelievo in più righe, ad esempio perché non vi sono articoli sufficienti da prelevare nella collocazione designata.|[Procedura: Suddividere le righe attività warehouse](warehouse-how-to-split-warehouse-activity-lines.md)|
|Ottenere accesso immediato ai prelievi che sono stati assegnati a un lavoratore della warehouse.|[Procedura: Individuare le assegnazioni della warehouse](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

