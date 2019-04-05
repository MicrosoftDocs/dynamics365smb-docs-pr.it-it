---
title: Panoramica dei task per la gestione degli acquisti | Documenti Microsoft
description: Descrive i task di gestione dei processi di acquisto o approvvigionamento, incluso l'utilizzo delle fatture di acquisto e degli ordini di acquisto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 11/15/2018
ms.author: sgroespe
ms.openlocfilehash: 87e3d134abe82e0f55acf4d3680b84fbc2c0c14b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801127"
---
# <a name="purchasing"></a>Acquisti
È possibile creare una fattura o un ordine di acquisto per registrare il costo di acquisto e per tenere traccia del conto fornitori. Se è necessario verificare un magazzino, anche le fatture di acquisto vengono utilizzate per aggiornare in modo dinamico i livelli di magazzino in modo da ridurre i costi di magazzino al minimo e migliorare l'assistenza clienti. I costi di acquisto, incluse le spese di assistenza, e i valori di magazzino derivanti dalla registrazione delle fatture di acquisto contribuiscono alle cifre di profitto e altri indicatori KPI finanziari in Gestione ruolo utente.

Utilizzare gli ordini di acquisto se il processo di acquisto richiede la registrazione delle le ricevute parziali di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile presso il fornitore. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di acquisto. Per ulteriori informazioni, vedere [Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di acquisto funzionano come le fatture di acquisto.

È possibile creare le fatture di acquisto automaticamente utilizzando il servizio OCR (riconoscimento ottico dei caratteri) per convertire le fatture PDF ricevute dai fornitori in documenti elettronici, che verranno successivamente convertiti in fatture di acquisto da un workflow. Per utilizzare questa funzionalità, è necessario innanzitutto iscriversi al servizio OCR e impostarlo. Per ulteriori informazioni, vedere [Elaborare i documenti in entrata](across-process-income-documents.md).      

I prodotti possono essere sia articoli di magazzino che servizi. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

Per tutti i processi di acquisto, è possibile incorporare un workflow di approvazione, ad esempio, per richiedere che gli acquisti di grande volume siano approvati dal responsabile della contabilità. Per ulteriori informazioni, vedere [Utilizzo dei workflow di approvazione](across-how-use-approval-workflows.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| A | Vedere |
| --- | --- |
| Creare una fattura di acquisto per registrare il contratto con un fornitore per acquistare prodotti con determinate condizioni di consegna e pagamento. |[Registrare gli acquisti](purchasing-how-record-purchases.md) |
|Creare un'offerta di acquisto per riflettere una richiesta di offerta di un fornitore che è possibile convertire successivamente in ordine di acquisto.|[Richiedere le offerte](purchasing-how-request-quotes.md)|
| Creare una fattura di acquisto per tutte le righe o quelle selezionate in una fattura di vendita. |[Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md) |
| Eseguire un'azione in una fattura di acquisto registrata non pagata per creare automaticamente una nota di credito e per annullare la fattura di acquisto o per ricrearla in modo da apportare correzioni. |[Correggere o annullare le fatture di vendita non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Creare una nota di credito di acquisto per stornare una fattura di acquisto registrata specifica per riflettere i prodotti resi al fornitore e l'importo di pagamento ricevuto. |[Elaborare i resi o gli annullamenti acquisti](purchasing-how-register-new-vendors.md) |
|Preparare la fattura per più carichi dallo stesso fornitore dopo aver combinato i carichi in una sola fattura.|[Combinare i carichi in una singola fattura](purchasing-how-to-combine-receipts.md)|
|Convertire, ad esempio, le fatture elettroniche dei fornitori in fatture di acquisto in Business Central.|[Ricevere e convertire documenti elettronici](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Informazioni su come vengono effettuati i calcoli [!INCLUDE[d365fin](includes/d365fin_md.md)] quando è necessario ordinare un articolo per riceverlo in una determinata data.|[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)|

## <a name="see-also"></a>Vedi anche
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione di progetti](projects-manage-projects.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
