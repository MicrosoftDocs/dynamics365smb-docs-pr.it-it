---
title: Gestire i costi di inventario e di produzione
description: 'Scopri quanti campi, pagine e report sono destinati agli utenti che gestiscono direttamente o indirettamente i costi degli articoli o delle operazioni.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="handling-inventory-and-manufacturing-costs"></a>Gestione dell'inventario e dei costi di produzione

Sebbene gran parte delle funzionalità di contabilità dei costi sia espressa in processi sottostanti senza interazione da parte dell'utente, come l'applicazione di immissione e l'adeguamento automatico dei costi, molti campi, pagine e report sono rivolti agli utenti che gestiscono direttamente o indirettamente il costo di articoli o operazioni.  

 L'assegnazione degli addebiti articoli ai documenti di acquisto è un esempio di task di contabilizzazione dei costi indiretti. L'aggiornamento del costo unitario di un articolo DB di produzione o di assemblaggio è un task di contabilizzazione dei costi diretti.  

 Nella tabella seguente viene descritta una sequenza di attività, con collegamenti agli articoli che le descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Aggiornare periodicamente o automaticamente il costo unitario di uno o più articoli per trasferire le eventuali modifiche dei costi dai movimenti in entrata, ad esempio movimenti per acquisti o output di produzione, ai movimenti in uscita correlati, ad esempio consumo o trasferimenti.|[Rettifica costi articolo](inventory-how-adjust-item-costs.md)|  
|Ottenere informazioni dettagliate sulla dinamica del costo medio per assumere decisioni relative ai prezzi o tenere traccia delle fluttuazioni dei costi causate da errori di immissione dei dati.|[Registrare nuovi articoli](inventory-how-register-new-items.md)|  
|Creare un costo standard per gli articoli di produzione mediante l'immissione dei tre elementi di costo: costo del materiale, costo di capacità e costo di conto lavoro.|[Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md)|  
|Calcolare il costo unitario di una articolo della DB in base ai costi unitari dei componenti sottostanti.|[Utilizzare le distinte base](inventory-how-work-BOMs.md) |  
|Completare il ciclo di vita del costing di un articolo prodotto mediante la rettifica dei costi e la riconciliazione dei movimenti di valorizzazione con la contabilità generale.|[Informazioni sui costi di un ordine di produzione chiuso](finance-about-finished-production-order-costs.md)|  
|Modificare il valore di un articolo in magazzino o il valore di un movimento contabile articolo, ad esempio una transazione di acquisto.|[Rivalutare il magazzino](inventory-how-revalue-inventory.md)|
|Annullare manualmente il collegamento di un articolo o riapplicare i movimenti contabili articoli creati dall'applicazione.|[Rimuovere e ricollegare movimenti contabili articolo](finance-how-to-remove-and-reapply-item-entries.md)|  
|Utilizzare il campo **Collega-da mov.** nelle registrazioni articoli per creare manualmente un collegamento fisso tra una transazione in entrata e la transazione in uscita originale.|[Chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Vedere anche

[Gestire i costi di inventario](finance-manage-inventory-costs.md)    
[Dettagli di progettazione: determinazione dei costi di magazzino](design-details-inventory-costing.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
