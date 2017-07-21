---
title: Panoramica dei task per la gestione delle vendite | Documenti Microsoft
description: "Descrive come si gestiscono le attività di vendita."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 06/30/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ebdcfc8c2be94398c1ebd7d5268a94b568e3b23b
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="sales"></a>Vendite
Si crea una fattura di vendita o un ordine di vendita per registrare il contratto con un cliente per vendere alcuni prodotti con determinate condizioni di consegna e pagamento.

È necessario utilizzare gli ordini di vendita se il processo di vendita richiede che si possano spedire parti di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile in una sola volta. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di vendita. In tutti gli altri aspetti, gli ordini di vendita funzionano come le fatture di vendita.

Per garantire la buona riuscita delle iniziative di marketing e la chiusura delle vendite, è fondamentale prendere le decisioni ottimali nel momento appropriato. La funzionalità di marketing in [!INCLUDE[d365fin](includes/d365fin_md.md)] offre un quadro accurato e tempestivo delle informazioni sui contatti consentendo di presentarsi in modo efficace a potenziali clienti, nonché di incrementare il livello di soddisfazione dei clienti. Per ulteriori informazioni, vedere [Relationship Management](marketing-relationship-management.md).

È possibile negoziare con il cliente prima di tutto creando un'offerta di vendita, che è possibile convertire in una fattura di vendita quando ci si accorda sulla vendita. Dopo che il cliente ha confermato il contratto, ad esempio dopo un processo di offerta, è possibile inviare una conferma dell'ordine per registrare l'obbligo di consegnare i prodotti come concordato.

Quando si consegnano i prodotti, nella quantità totale o parziale, si registra l'ordine di vendita, o la fattura di vendita, come spedito o come spedito e fatturato per creare i relativi movimenti contabili articolo e cliente nel sistema.

Negli ambienti aziendali in cui il cliente deve pagare prima che vengano consegnati i prodotti, ad esempio nelle vendita al dettaglio, è necessario attendere la ricezione del pagamento prima di consegnare i prodotti. Nella maggior parte dei casi, i pagamenti in entrata vengono elaborati alcune settimane dopo la consegna collegando i pagamenti alle relative fatture di vendita non pagate registrate. Per ulteriori informazioni, vedere [Procedura: Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

È possibile correggere o annullare in modo semplice una fattura di vendita registrata prima che venga pagata. Ciò risulta utile se si desidera correggere un errore di digitazione o se il cliente richiede una modifica in anticipo nell'elaborazione dell'ordine. Se la fattura di vendita registrata è stata pagata, allora sarà necessario creare una nota di credito di vendita per stornare la vendita.

I documenti di vendita possono essere inviati come file PDF allegati all'e-mail. Il corpo e-mail conterrà un estratto del documento di vendita, ad esempio i prodotti, l'importo totale e un collegamento al sito di PayPal. Per ulteriori informazioni, vedere [Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md).

Per tutti i processi di vendita, è possibile incorporare un workflow di approvazione, ad esempio, per richiedere che le vendite di grandi volumi siano approvate dal responsabile della contabilità. Per ulteriori informazioni, vedere [Utilizzo dei workflow di approvazione](across-how-use-approval-workflows.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| Per | Vedere |
| --- | --- |
| Creare un'offerta di vendita in cui si presentano prodotti a condizioni negoziabili prima della conversione dell'offerta in una fattura di vendita. |[Procedura: Fare offerte](sales-how-make-offers.md) |
| Creare una fattura di vendita per registrare il contratto con un cliente per vendere prodotti con determinate condizioni di consegna e pagamento. |[Procedura: Fatturare le vendite](sales-how-invoice-sales.md) |
| Elaborare un ordine di vendita con la spedizione parziale o la spedizione diretta. |[Procedura: Vendere prodotti](sales-how-sell-products.md) |
|Impostare righe di vendita o acquisto standard da inserire nei documenti, ad esempio, per ordini di approvvigionamento ricorrenti.|[Procedura: Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md)|  
| Collegare un ordine di vendita a un ordine di acquisto per vender un articolo con spedizione diretta che verrà consegnato direttamente dal fornitore al cliente. |[Procedura: Effettuare spedizioni dirette](sales-how-drop-shipment.md) |
| Eseguire un'azione in una fattura di vendita registrata non pagata per creare automaticamente una nota di credito e per annullare la fattura di vendita o per ricrearla in modo da apportare correzioni. |[Procedura: Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md) |
| Creare una nota di credito vendita per stornare una fattura di vendita registrata specifica per riflettere i prodotti resi dal cliente e l'importo di pagamento da restituire. |[Procedura: Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md) |
| Creare una scheda cliente per ogni cliente a cui si effettua una vendita. |[Procedura: Registrare nuovi clienti](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Vedi anche
[Setup Vendite](sales-setup-sales.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Gestione della contabilità fornitori](payables-manage-payables.MD)  
[Gestione progetti](projects-manage-projects.md)    
[Catena di approvvigionamento](madeira-supply-chain.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

