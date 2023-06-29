---
title: Esecuzione della produzione
description: 'Quando una domanda viene pianificata e i materiali vengono emessi in base alle DB di produzione, le operazioni di produzione effettive possono essere avviate ed eseguite nella sequenza definita dal ciclo dell''ordine di produzione.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5406, 5407, 5728, 8903, 9011, 9012, 9013, 9041, 9044, 9047, 9323, 9324, 9325, 9326, 9327, 99000784, 99000785'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manufacturing"></a><a name="manufacturing"></a>Manufacturing

> [!NOTE]
> La funzionalità descritta in questo argomento e negli argomenti secondari è visibile solo se si dispone dell'esperienza **Premium**. Per ulteriori informazioni, vedere [Modifica delle funzionalità visualizzate](ui-experiences.md).

Quando una domanda viene pianificata e i materiali vengono emessi in base alle DB di produzione, le operazioni di produzione effettive possono essere avviate ed eseguite nella sequenza definita dal ciclo dell'ordine di produzione.  

Una parte importante dell'esecuzione della produzione, dal punto di vista del sistema, è la registrazione dell'output di produzione nel database per indicare l'avanzamento e aggiornare il magazzino con gli articoli finiti. La registrazione dell'output può essere svolta manualmente, compilando e registrando le righe di registrazione dopo le operazioni di produzione. Oppure può essere effettuata automaticamente con il metodo di consuntivazione a ritroso. In tale caso il consumo dei materiali viene registrato automaticamente con l'output quando l'ordine di produzione viene impostato su completato.  

Come alternativa alla registrazione in batch per registrare l'output di più ordini di produzione, è possibile utilizzare la pagina **Registrazioni di produzione** per registrare il consumo e/o l'output per una riga dell'ordine di produzione.

Prima di iniziare a produrre articoli, è necessario creare diverse impostazioni, ad esempio le aree di produzione, i cicli e le distinte base di produzione. Per ulteriori informazioni, vedere [Impostazione della produzione](production-configure-production-processes.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Per**|**Vedere**|  
|------------|-------------|  
|Ottenere informazioni sull'uso degli ordini di produzione.|[Informazioni sugli ordini di produzione](production-about-production-orders.md)|
|Creare manualmente ordini di produzione.|[Creare ordini di produzione](production-how-to-create-production-orders.md)|
|Affidare tutte le operazioni o quelle selezionate in un ordine di produzione a un terzista.|[Gestire le attività di conto lavoro](production-how-to-subcontract-manufacturing.md)|
|Registrare l'output di produzione, nonché i consumi in termini di materiale e tempo relativi a una singola riga dell'ordine di produzione rilasciato.|[Registrare consumo e output per la riga dell'ordine di produzione rilasciato](production-how-to-register-consumption-and-output.md)|  
|Registrare tramite processo batch la quantità di componenti utilizzata per operazione in una registrazione che può elaborare molteplici ordini di produzione pianificati.|[Registrare il consumo tramite processo batch](production-how-to-post-consumption.md)|
|Registrare tramite processo batch la quantità di componenti utilizzata per operazione in una registrazione che può elaborare molteplici ordini di produzione pianificati.|[Registrare l'output e i tempi di lavorazione tramite processo batch](production-how-to-post-output-quantity.md)|
|Annullare l'output, ad esempio a causa di un errore di immissione dei dati e di una quantità non corretta.  |[Stornare la registrazione dell'output](production-how-to-reverse-output-posting.md)|  
|Registrare il numero di articoli prodotti in ogni operazione completata che non vengono qualificati come output finito ma come materiale di scarto.|[Registrare lo scarto](production-how-to-post-scrap.md)|
|Visualizzare il carico della produzione come risultato di ordini di produzione pianificati e rilasciati.|[Visualizzare il carico in aree di produzione e centri di lavoro](production-how-to-view-the-load-on-work-centers.md)|  
|Utilizzare la pagina **Registrazioni capacità** per registrare le capacità consumate non assegnate a un ordine di produzione, ad esempio la manutenzione.|[Registrare le capacità](production-how-to-post-capacities.md)|  
|Calcolare e rettificare il costo degli articoli di produzione terminati e dei componenti consumati ai fini della riconciliazione finanziaria.|[Informazioni sui costi di un ordine di produzione chiuso](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
