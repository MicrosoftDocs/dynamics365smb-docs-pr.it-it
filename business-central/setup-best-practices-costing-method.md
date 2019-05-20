---
title: 'Impostare le procedure ottimali: Metodo di costing | Documenti Microsoft'
description: Il Metodo di costing sulla scheda articolo definisce come viene registrato il flusso del costo dell'articolo e se un valore effettivo o a budget viene capitalizzato e utilizzato nel calcolo dei costi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8f670b125532300af169cc82f318abddd768e417
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250482"
---
# <a name="setup-best-practices-costing-method"></a>Impostare le procedure ottimali: metodo di costing
Il **Metodo di costing** sulla scheda articolo definisce come viene registrato il flusso del costo dell'articolo e se un valore effettivo o a budget viene capitalizzato e utilizzato nel calcolo dei costi.  

 È importante impostare il metodo di costing corretto in base al tipo di articolo e all'ambiente aziendale per assicurare magazzini economici.  

 Nella seguente tabella vengono fornite le procedure consigliate sulla modalità di impostazione del campo **Metodo di costing**. Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md).  

|Opzione di setup|Procedura consigliata|Commento|  
|------------------|-------------------|-------------|  
|FIFO|Utilizzare quando il costo del prodotto è stabile.<br /><br /> Utilizzare per articoli con una durata a scaffale limitata, poiché le merci più vecchie devono essere vendute prima della data di scadenza.|Il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo, selezionato secondo la regola FIFO.<br /><br /> Nella valutazione di magazzino si presuppone che il primo articolo posizionato nel magazzino venga venduto per primo. **Nota:**  Quando i prezzi salgono, nei conti patrimoniali viene mostrato un valore maggiore. Ciò significa che la soggettività tributaria aumenta mentre il punteggio del credito e la capacità di prendere in prestito soldi migliora.|  
|LIFO|Utilizzare quando i livelli di inventario vengono gestiti in modo coerente o aumentano nel tempo.|Il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo, selezionato secondo la regola LIFO.<br /><br /> Nella valutazione di magazzino si presuppone che gli ultimi articoli posizionati nel magazzino vengano venduti per primo. **Nota:** Quando i prezzi salgono, il valore nel conto economico diminuisce. Ciò significa che la soggettività tributaria diminuisce mentre la capacità di prendere in prestito soldi peggiora. **Importante:** Operazione non consentita in molti paesi, perché può essere utilizzata per ridurre il profitto.|  
|Media|Utilizzare quando il costo del prodotto non è stabile.<br /><br /> Utilizzare quando gli inventari sono impilati o mischiati e non è possibile differenziarli, ad esempio con gli agenti chimici.|Il costo unitario di un articolo è il costo esatto con la particolare unità è stata ricevuta.|  
|Specifico|Utilizzare nella produzione o nel commercio di articoli facilmente identificabili a costi unitari abbastanza elevati.<br /><br /> Utilizzare gli articoli che sono soggetti a regolazione.<br /><br /> Utilizzare per articoli con numeri di serie.|Il costo unitario di un articolo viene calcolato come il costo unitario medio in ogni momento dopo un acquisto.<br /><br /> Per la valutazione magazzino si presuppone che tutte le giacenze siano vendute simultaneamente.|  
|Standard|Utilizzare quando il controllo costi è fondamentale.<br /><br /> Utilizzare nella produzione ripetitiva per stimare i costi di materiale diretto, di manodopera diretta e i costi generali di produzione.<br /><br /> Utilizzare quando esiste una disciplina e del personale per gestire gli standard.|Il costo unitario di un articolo è prestabilito in base a una stima.<br /><br /> Quando il costo effettivo viene realizzato successivamente, il costo standard deve essere rettificato con il costo effettivo tramite i valori di scostamento.|  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)   
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Impostare aree di applicazione complesse utilizzando le procedure ottimali](set-up-complex-application-areas-using-best-practices.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
