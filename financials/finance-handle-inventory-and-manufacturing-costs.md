---
title: Gestire i costi del magazzino e di produzione | Microsoft Docs
description: "Sebbene la maggior parte della funzionalità di contabilizzazione dei costi venga espressa in processi sottostanti senza interazione da parte dell'utente, ad esempio il collegamento dei movimenti contabili e la rettifica automatica dei costi, numerosi campi, finestre e report sono destinati agli utenti affinché possano gestire, direttamente o indirettamente, il costo degli articoli o delle operazioni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2745d8b06967549b32c8014a24ab9958c72c1c9d
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="handling-inventory-and-manufacturing-costs"></a>Gestione dei costi del magazzino e di produzione
Sebbene la maggior parte della funzionalità di contabilizzazione dei costi venga espressa in processi sottostanti senza interazione da parte dell'utente, ad esempio il collegamento dei movimenti contabili e la rettifica automatica dei costi, numerosi campi, finestre e report sono destinati agli utenti affinché possano gestire, direttamente o indirettamente, il costo degli articoli o delle operazioni.  

 L'assegnazione degli addebiti articoli ai documenti di acquisto è un esempio di task di contabilizzazione dei costi indiretti. L'aggiornamento del costo unitario di un articolo DB di produzione o di assemblaggio è un task di contabilizzazione dei costi diretti.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Aggiornare periodicamente o automaticamente il costo unitario di uno o più articoli per trasferire le eventuali modifiche dei costi dai movimenti in entrata, ad esempio movimenti per acquisti o output di produzione, ai movimenti in uscita correlati, ad esempio consumo o trasferimenti.|[Procedura: Rettificare i costi degli articoli](inventory-how-adjust-item-costs.md)|  
|Ottenere informazioni dettagliate sulla dinamica del costo medio per assumere decisioni relative ai prezzi o tenere traccia delle fluttuazioni dei costi causate da errori di immissione dei dati.|[Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md)|  
|Creare un costo standard per gli articoli di produzione mediante l'immissione dei tre elementi di costo: costo del materiale, costo di capacità e costo di conto lavoro.|[Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md)|  
|Calcolare il costo unitario di una articolo della DB in base ai costi unitari dei componenti sottostanti.|[Procedura: Utilizzare le distinte base](inventory-how-work-BOMs.md)|  
|Completare il ciclo di vita del costing di un articolo prodotto mediante la rettifica dei costi e la riconciliazione dei movimenti di valorizzazione con la contabilità generale.|[Informazioni sui costi di un ordine di produzione chiuso](finance-about-finished-production-order-costs.md)|  
|Modificare il valore di un articolo in magazzino o il valore di un movimento contabile articolo, ad esempio una transazione di acquisto.|[Procedura: Rivalutare il magazzino](inventory-how-revalue-inventory.md)|
|Annullare manualmente il collegamento di un articolo o riapplicare i movimenti contabili articoli creati dal programma.|[Procedura: Rimuovere e ricollegare movimenti contabili articolo](finance-how-to-remove-and-reapply-item-entries.md)|  
|Utilizzare il campo **Collega-da mov.** nelle registrazioni articoli per creare manualmente un collegamento fisso tra una transazione in entrata e la transazione in uscita originale.|[Procedura: Chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Vedi anche  
[Gestire i costi del magazzino](finance-manage-inventory-costs.md)
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)

