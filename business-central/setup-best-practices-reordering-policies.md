---
title: 'Impostare le procedure ottimali: metodi di riordino | Microsoft Docs'
description: Nel campo Metodo di riordino delle schede articolo vengono offerti quattro diversi metodi di pianificazione che determinano la modalità di interazione dei singoli parametri di pianificazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 97d299372bc140c29138d6b83c34ec18254c4fcd
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882232"
---
# <a name="setup-best-practices-reordering-policies"></a>Impostare le procedure ottimali: metodi di riordino
Nel campo **Metodo di riordino** delle schede articolo vengono offerti quattro diversi metodi di pianificazione che determinano la modalità di interazione dei singoli parametri di pianificazione.  

Una delle migliori basi per la selezione di un metodo di riordino è la classificazione ABC dell'articolo. Quando si utilizza la classificazione ABC per il controllo del magazzino e la pianificazione degli approvvigionamenti, gli articoli vengono gestiti secondo tre classi diverse a seconda del valore e del volume rispetto allo stock totale. La distribuzione di valore-volume delle tre classi viene visualizzata nella seguente tabella.

|Classe|Percentuale del volume dello stock totale|Percentuale del valore dello stock totale|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|C|60-70|10-30|

La classificazione ABC stabilisce che è possibile risparmiare tempo e denaro applicando un controllo meno restrittivo agli articoli con un valore-volume basso rispetto agli articoli con un valore-volume alto. L'esempio seguente mostra quale metodo di riordino in [!INCLUDE[d365fin](includes/d365fin_md.md)] è più appropriato per gli articoli con classificazione A, B e C rispettivamente.

![Classificazione di ABC](media/abc_classification.png "abc_classification")

Nella seguente tabella vengono fornite le procedure consigliate per la selezione tra quattro metodi.  

|Opzione di setup|Procedura consigliata|Commento|  
|------------------|-------------------|-------------|  
|**Ordine**|Utilizzare per gli articoli A.<br /><br /> Utilizzare per gli articoli di tipo produzione su ordine.<br /><br /> Nella produzione utilizzare per gli articoli di livello massimo e per i componenti e i sottoassemblaggi costosi.<br /><br /> Utilizzare per gli articoli che vengono acquistati come spedizioni dirette e ordini speciali.<br /><br /> Non utilizzare se non si accetta l'impegno automatico.|Gli articoli A, ad esempio divani in cuoio in un reparto di mobili, sono articoli di elevato valore con una velocità di ordini bassa e irregolare dove il magazzino è inaccettabile oppure gli attributi richiesti variano. Il migliore metodo di riordino è pertanto quello in cui effettua la pianificazione in particolare per ogni domanda.|  
|**Lotto-per-Lotto**|Utilizzare per gli articoli B.<br /><br /> Nella produzione utilizzare per i componenti che si verificano in più DB. In questo modo si garantisce che gli ordini di acquisto siano combinati per lo stesso fornitore, in modo da poter negoziare i prezzi migliori.<br /><br /> Utilizzare se non si è certi quale metodo di riordino selezionare.|Gli articoli B, ad esempio le sedie da pranzo, presentano una velocità di ordini costante e abbastanza elevata, ma anche costi di mantenimento elevati. Il miglior metodo di riordino per gli articoli B è pertanto un metodo economico, creando la domanda nel ciclo di riordino.<br /><br /> Questo metodo può essere utilizzato per l'80 percento degli articoli.<br /><br /> Può essere utilizzato correttamente senza parametri di pianificazione.|  
|**Qtà Riordino Fissa**|Utilizzare per gli articoli C.<br /><br /> Combinare con i parametri del punto di riordino.<br /><br /> Nella produzione utilizzare per i componenti di ultimo livello.<br /><br /> Non utilizzare se l'articolo è spesso impegnato.|Gli articoli C, ad esempio, tazze di tè, sono articoli di basso valore con velocità di ordine elevata e costante. Il migliore metodo di riordino per gli articoli C pertanto è un metodo che garantisce la disponibilità costante, rimanendo sempre al di sopra di un punto di riordino.<br /><br /> Se l'utente impegna una quantità per una domanda remota, la struttura di pianificazione verrà disturbata. Anche se il livello della quantità scorte previste è ammesso relativamente al punto di riordino, le quantità potrebbero non essere disponibili a causa dell'impegno.|  
|**Qtà Massima**|Utilizzare per gli articoli C con costi di mantenimento o limitazioni di archiviazione elevati.<br /><br /> Combinare con uno più modificatori ordine (Quantità minima ordine/Quantità massima ordine o Molteplicità ordine).|Gli articoli C, ad esempio, tazze di tè, sono articoli di basso valore con velocità di ordine elevata e costante. Il migliore metodo di riordino per gli articoli C pertanto è un metodo che garantisce la disponibilità costante, rimanendo sempre al di sopra di un punto di riordino, ma al di sotto di una quantità di giacenza massima.<br /><br /> Per modificare l'ordine suggerito, è possibile diminuire la quantità dell'ordine alla quantità massima ordine specificata, aumentarla a una quantità minima ordine specificata o arrotondarla per eccesso per soddisfare una molteplicità ordine. **Nota:** Se utilizzato con un punto di riordino, il magazzino è tra il punto di riordino e la quantità massima.|  

## <a name="see-also"></a>Vedi anche  
 [Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)   
 [Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md)   
 [Dettagli di progettazione: Ordine](design-details-order.md)   
 [Dettagli di progettazione: Lotto-per-Lotto](design-details-lot-for-lot.md)   
 [Dettagli di progettazione: Qtà riordino fissa](design-details-fixed-reorder-qty.md)   
 [Dettagli di progettazione: Qtà Massima](design-details-maximum-qty.md)   
 [Impostare aree di applicazione complesse utilizzando le procedure ottimali](set-up-complex-application-areas-using-best-practices.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
