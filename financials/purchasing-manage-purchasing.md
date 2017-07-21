---
title: Panoramica dei task per la gestione degli acquisti | Documenti Microsoft
description: Descrive i task di gestione dei processi di acquisto o approvvigionamento, incluso l'utilizzo delle fatture di acquisto e degli ordini di acquisto.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 653cd9b5e9651f2039ab18f3e7a26b299238d817
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="purchasing"></a>Acquisti
È possibile creare una fattura o un ordine di acquisto per registrare il costo di acquisto e per tenere traccia del conto fornitori. Se è necessario verificare un magazzino, anche le fatture di acquisto vengono utilizzate per aggiornare in modo dinamico i livelli di magazzino in modo da ridurre i costi di magazzino al minimo e migliorare l'assistenza clienti. I costi di acquisto, incluse le spese di assistenza, e i valori di magazzino derivanti dalla registrazione delle fatture di acquisto contribuiscono alle cifre di profitto e altri indicatori KPI finanziari presenti nella home page.

Utilizzare gli ordini di acquisto se il processo di acquisto richiede la registrazione delle le ricevute parziali di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile presso il fornitore. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di acquisto. Per ulteriori informazioni, vedere [Procedura: Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di acquisto funzionano come le fatture di acquisto.

È possibile creare le fatture di acquisto automaticamente utilizzando il servizio OCR (riconoscimento ottico dei caratteri) per convertire le fatture PDF ricevute dai fornitori in documenti elettronici, che verranno successivamente convertiti in fatture di acquisto da un workflow. Per utilizzare questa funzionalità, è necessario innanzitutto iscriversi al servizio OCR e impostarlo. Per ulteriori informazioni, vedere [Procedura: Elaborare i documenti in entrata](across-process-income-documents.md).      

I prodotti possono essere sia articoli di magazzino che servizi. Per ulteriori informazioni, vedere [Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md).

Per tutti i processi di acquisto, è possibile incorporare un workflow di approvazione, ad esempio, per richiedere che gli acquisti di grande volume siano approvati dal responsabile della contabilità. Per ulteriori informazioni, vedere [Utilizzo dei workflow di approvazione](across-how-use-approval-workflows.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono. Questi task sono elencati nell'ordine in cui vengono in genere eseguiti.

| Per | Vedere |
| --- | --- |
| Creare una fattura di acquisto per registrare il contratto con un fornitore per acquistare prodotti con determinate condizioni di consegna e pagamento. |[Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md) |
| Creare una fattura di acquisto per tutte le righe o quelle selezionate in una fattura di vendita. |[Procedura: Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md) |
| Eseguire un'azione in una fattura di acquisto registrata non pagata per creare automaticamente una nota di credito e per annullare la fattura di acquisto o per ricrearla in modo da apportare correzioni. |[Procedura: Correggere o annullare le fatture di vendita non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Creare una nota di credito di acquisto per stornare una fattura di acquisto registrata specifica per riflettere i prodotti resi al fornitore e l'importo di pagamento ricevuto. |[Procedura: Elaborare i resi o gli annullamenti acquisti](purchasing-how-register-new-vendors.md) |
| Creare una scheda fornitore per ogni fornitore da cui si acquista. |[Procedura: Registrare nuovi fornitori](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>Vedi anche
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione di progetti](projects-manage-projects.md)    
[Catena di approvvigionamento](madeira-supply-chain.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
