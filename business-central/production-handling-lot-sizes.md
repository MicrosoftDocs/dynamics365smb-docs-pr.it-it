---
title: Gestione delle dimensioni dei lotti
description: In questo argomento vengono descritti i diversi modi per gestire le dimensioni lotti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="handling-lot-sizes-in-production" />Gestione delle dimensioni lotti in produzione
In termini di quantità, il numero di articoli prodotti in un'operazione di produzione potrebbe non essere correlato alla modalità di vendita degli stessi. Ad esempio, si potrebbero produrre centinaia di articoli in un unico lotto, ma vendere ogni articolo singolarmente. Quando si configurano i cicli di produzione e le distinte base (BOM), vi sono alcune sfumature da considerare per quanto riguarda le dimensioni lotti. In questo argomento viene descritto in che modo le dimensioni lotti influiscono sui calcoli dei costi e sulla pianificazione delle risorse.

## <a name="units-of-measure-in-production-bill-of-materials" />Unità di misura nella distinta base di produzione
Sebbene si specifichi l'unità di misura di base per un articolo, la distinta base potrebbe utilizzare un'unità di misura di base diversa per il prodotto finito. Ad esempio, l'unità di misura di base per un articolo potrebbe essere PZ, ma la distinta base potrebbe richiedere pallet o tonnellate. Ciò è utile quando le macchine oi componenti grezzi determinano il volume. Ad esempio, probabilmente non si vorrebbe cuocere un unico muffin poiché è difficile usare una porzione di un uovo. Invece, si cuociono vari muffin per ridurre gli sprechi. Per ulteriori informazioni, vedere [Creare distinte base di produzione](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines" />Dimensione lotto nelle righe del ciclo
Dal punto di vista del ciclo di produzione, è possibile specificare una dimensione lotto nelle righe del ciclo per allinearla alla capacità delle macchine che producono gli articoli. Il tempo di lavorazione nelle righe del ciclo viene ridotto proporzionalmente alla dimensione lotto. 

È la soluzione appropriata quando la quantità in un ordine di produzione è un fattore della dimensione lotto nel ciclo. Ad esempio, se la teglia può contenere 10 muffin, se ne dovrebbero cuocere 10, 20, 30 e così via e non 5 o 15.  È molto meno di un problema se si gestiscono grandi quantità.

La dimensione lotto è anche popolare negli ambienti di produzione in cui la produzione viene misurata come quantità che è possibile produrre durante un periodo di tempo fisso. Ad esempio, se volume per turno di 9 ore è 25000 piedi cubi, è possibile impostare il tempo di lavorazione su 9 ore e la dimensione lotto su 25000.
La quantità dell'ordine di produzione diventa meno importante poiché nell'ordine di produzione il tempo di lavorazione viene calcolato come Tempo lavorazione / Dimensione lotto per ottenere il tempo di lavorazione per pezzo.
 
> [!NOTE]
> Il valore definito in Dimensione lotto non ha alcun impatto sul tempo specificato in **Tempo di setup** della riga del ciclo. Il setup verrà eseguito una sola volta, anche se sono presenti più lotti. Ad esempio, in modo da non dover riscaldare il forno per il secondo lotto di muffin. Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units" />Dimensioni lotti per articoli e unità di stockkeeping
Le dimensioni lotti definite per i cicli non sono uguali a quelle per gli articoli o le unità di stockkeeping. Questi valori vengono utilizzati per uno scopo diverso e non influiscono sulla capacità di produzione. 

## <a name="lot-size-on-item-and-stockkeeping-units" />Dimensione lotto per articoli e unità di stockkeeping
Per gli articoli e le unità di stockkeeping, le dimensioni lotti hanno i seguenti effetti sul calcolo dei costi e sulla pianificazione degli approvvigionamenti:

* Per il calcolo dei costi standard, se si abilita **Costi setup incluso** nella pagina **Setup manufacturing**, il costo per il setup viene aggiunto ai costi standard. Se si specifica una dimensione lotto, il costo di setup per l'operazione del ciclo verrà ridotto in base a una dimensione lotto. Ad esempio, se la dimensione lotto definita nella scheda articolo è 10 e sono necessari 15 minuti per riscaldare il forno, il costo del carburante assegnato ai 10 muffin sarà di circa 1,5 minuti. 

> [!NOTE]
> I costi di setup vengono gestiti in modo diverso rispetto a un costo standard e alle prospettive di allocazione della capacità. Se la quantità prodotta non corrisponde alla dimensione lotto definita nella scheda articolo, si avrà una variazione. Per ulteriori informazioni, vedere [Gestione dei costi di magazzino](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Per la pianificazione degli approvvigionamenti, l'impostazione della dimensione lotto per gli articoli funziona con **Percentuale stabilizzazione di default** nella pagina **Setup manufacturing**. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerà le modifiche nella domanda che sono al di sotto della percentuale di stabilizzazione e non creerà suggerimenti di pianificazione. Ad esempio, 15 è specificato nel campo % stabilizzazione predefinita e abbiamo un ordine di produzione di 20 muffin per 20 ospiti, ma un ospite non può partecipare. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerà l'ospite mancante perché è solo il 10% della dimensione lotto 10 definita per l'articolo. Tuttavia, se mancano due ospiti, [!INCLUDE[prod_short](includes/prod_short.md)] suggerirà di ridurre la quantità dell'ordine perché due rappresenta il 20% della dimensione lotto. Per ulteriori informazioni sulla pianificazione, vedere [Pianificazione](production-planning.md).

## <a name="see-also" />Vedere anche
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Utilizzare le unità di misura batch di produzione](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Creare cicli](production-how-to-create-routings.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
