---
title: 'Dettagli di progettazione: Valutazione di magazzino | Microsoft Docs'
description: La valutazione magazzino è la determinazione del costo di un articolo di magazzino.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# <a name="design-details-inventory-valuation"></a>Dettagli di progettazione: Valutazione di magazzino
La valutazione magazzino è la determinazione del costo assegnato a un articolo di magazzino, espresso dalla seguente equazione.  

Magazzino finale = magazzino iniziale + acquisti netti – costo dei beni venduti  

Il calcolo della valutazione di magazzino utilizza il campo **Importo costo (effettivo)** dei movimenti di valorizzazione per l'articolo. I movimenti vengono classificati in base al tipo di movimento che corrisponde ai componenti di costo, al costo diretto, al costo indiretto, allo scostamento, alla rivalutazione e all'arrotondamento. Per ulteriori informazioni, vedere [Dettagli di progettazione: Componenti costo](design-details-cost-components.md).  

I movimenti collegati tra loro, tramite il collegamento fisso o in base all'ipotesi generale di costo-flusso definita dal metodo di costing. Un movimento di riduzione di magazzino può essere collegato a più di un movimento di aumento con differenti date di registrazione e possibilmente con costi di acquisto diversi. Per ulteriori informazioni, vedere [Dettagli di progettazione: Collegamento articoli](design-details-item-application.md). Di conseguenza, il calcolo del valore di magazzino in una specifica data è basato sulla somma dei movimenti di valorizzazione positivi e negativi.  

## <a name="inventory-valuation-report"></a>Report Valutazione magazzino
Per calcolare il valore di magazzino nel report **Valutazione magazzino**, il report inizia calcolando il valore del magazzino dell'articolo alla data di inizio specificata. Aggiunge quindi gli aumenti del valore di magazzino e sottrae le diminuzioni del valore di magazzino fino a una data finale specificata. Il risultato finale è il valore di magazzino alla data di fine. Il report calcola questi valori sommando i valori nel campo **Importo costo (effettivo)** nei movimenti di valorizzazione, utilizzando le date di registrazione come filtri.  

Nel report stampato vengono sempre visualizzati gli importi effettivi, vale a dire il costo dei movimenti che sono stati registrati come fatturati. Se viene selezionato il campo Includi costo previsto della Scheda dettaglio Opzioni, nel report verrà stampato anche il costo previsto di movimenti che sono stati registrati come ricevuti o spediti.  

> [!IMPORTANT]  
>  I valori del report **Valutazione magazzino** sono riconciliati con il conto giacenza magazzino nella contabilità generale, ovvero i movimenti di valorizzazione in questione sono stati registrati nella contabilità generale.  

> [!IMPORTANT]  
>  Gli importi nelle colonne **Valore** del report sono basati sulla data di registrazione delle transazioni per un articolo.  

## <a name="inventory-valuation---wip-report"></a>Report Valutazione magazzino - WIP
Un'azienda manifatturiera deve determinare il valore di tre tipi di magazzino:  

* Magazzino di materie prime  
* Magazzino WIP  
* Magazzino di prodotti finiti  

Il valore del magazzino WIP è determinato dalla seguente equazione:  

* Magazzino WIP finale = Magazzino WIP iniziale + costi di produzione – costi delle merci lavorate  

Come per il magazzino acquistato, i movimenti di valorizzazione forniscono la base della valutazione di magazzino. Il calcolo viene eseguito utilizzando i valori del campo **Importo costo (effettivo)** dei movimenti di valorizzazione di capacità e dell'articolo associati a un ordine di produzione.  

Lo scopo della valutazione di magazzino WIP consiste nel determinare il valore degli articoli la cui produzione non è ancora stata completata alla data stabilita. Di conseguenza il valore di magazzino WIP è basato sui movimenti di valorizzazione correlati ai movimenti contabili capacità e consumo. I movimenti contabili del consumo devono essere completamente fatturati alla data di valutazione. Di conseguenza, il report **Valutazione magazzino - WIP** mostra i costi che rappresentano il valore di magazzino WIP in due categorie: consumo e capacità.  

## <a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Riconciliazione con la contabilità generale](design-details-reconciliation-with-the-general-ledger.md)   
[Dettagli di progettazione: Rivalutazione](design-details-revaluation.md)   
[Dettagli di progettazione: Registrazione dell'ordine di produzione](design-details-production-order-posting.md)
[ Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
