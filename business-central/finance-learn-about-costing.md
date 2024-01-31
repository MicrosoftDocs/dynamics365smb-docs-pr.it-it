---
title: Informazioni sul costing di magazzino
description: La gestione dei costi di inventario include la registrazione e il reporting dei costi operativi business e il reporting dei costi di produzione e di magazzino.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Informazioni sul costing di magazzino
La gestione dei costi di magazzino include la registrazione e il reporting dei costi operativi business. Comprende inoltre il reporting dei costi di produzione e di magazzino, ovvero il valore degli articoli.  

 Di seguito sono elencati i principi fondamentali di questa materia: i metodi di costing definiscono il modo in cui gli articoli vengono valutati quando escono dal magazzino, la rettifica dei costi aggiorna il costo della merce venduta con costi di acquisto correlati registrati dopo la vendita e infine il valore di magazzino deve essere registrato in appositi conti C/G con periodicità regolare.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Distinguere i diversi metodi di costing e il relativo effetto sui flussi dei costi.|[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)|  
|Ottenere informazioni sul modo in cui i movimenti di collegamento articoli collegano dinamicamente le riduzioni con gli aumenti di magazzino per mantenere il controllo dei flussi dei costi.|[Dettagli di progettazione: Collegamento articoli](design-details-item-application.md)|  
|Ottenere informazioni sul modo in cui il costo unitario di un articolo viene continuamente aggiornato con il costo dell'ultima transazione in base al metodo di costing dell'articolo.|[Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)|  
|Ottenere informazioni sul modo in cui il costo medio di un articolo viene calcolato dinamicamente in base al costo medio del periodo selezionato.|[Dettagli di progettazione: Costo medio](design-details-average-cost.md)|  
|Distinguere il costo previsto (non ancora fatturato) dal costo effettivo e apprendere come viene gestito nella contabilità generale.|[Dettagli di progettazione: Registrazione del costo previsto](design-details-expected-cost-posting.md)|  
|Comprendere il meccanismo di rettifica dei costi, che assicura il riporto dei costi anche se le transazioni di magazzino avvengono in modo casuale.|[Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)|  
|Apprendere per quale motivo i costi standard vengono spesso utilizzati dalle aziende manifatturiere come base di valutazione per componenti e articoli finali.|[Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md)|  
|Comprendere il modo in cui il valore di magazzino viene riflesso nella contabilità generale.|[Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|Ottenere informazioni sul modo in cui gli addebiti articoli, come le spese di trasposto e l'assicurazione, possono attribuire componenti di costo supplementari al costo unitario di un articolo.|[Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md)|  
|Apprendere come i periodi di magazzino consentano a una società di controllare il valore di magazzino nel tempo mediante la definizione di periodi più brevi, che possono essere chiusi per la registrazione con l'avanzamento dell'anno fiscale.|[Utilizzare periodi di magazzino](finance-how-to-work-with-inventory-periods.md)|  
|Comprendere tutti i meccanismi del motore di costing, incluso quanto accade quando si registrano transazioni di produzione e di assemblaggio.|[Dettagli di progettazione: determinazione dei costi di inventario](design-details-inventory-costing.md)|  

## Vedere anche
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]