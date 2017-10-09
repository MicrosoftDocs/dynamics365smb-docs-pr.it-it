---
title: 'Procedura: Analizzare articoli tracciati | Documenti Microsoft'
description: "È possibile analizzare dove è stato utilizzato un articolo tracciato, nonché ottenere informazioni su come e quando l'articolo è stato ricevuto o prodotto, trasferito, venduto, consumato o reso. È inoltre possibile trovare tutte le istanze correnti di un numero seriale o di un numero di lotto specifico nel database. A tale scopo si utilizzano le funzionalità Tracciabilità articolo e Naviga."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c9944bc25131a5cb51015483511bd7d4854f4c1a
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-trace-item-tracked-items"></a>Procedura: Analizzare articoli tracciati
È possibile analizzare dove è stato utilizzato un articolo tracciato, nonché ottenere informazioni su come e quando l'articolo è stato ricevuto o prodotto, trasferito, venduto, consumato o reso. È inoltre possibile trovare tutte le istanze correnti di un numero seriale o di un numero di lotto specifico nel database. A tale scopo si utilizzano le funzionalità Tracciabilità articolo e Naviga.  

 Queste funzionalità possono essere particolarmente utili in ambito di controllo qualità quando è necessario determinare quali clienti hanno ricevuto prodotti con un numero di lotto specifico o quando si desidera stabilire da quale lotto proviene un componente difettoso.  

 Nella finestra **Tracciabilità articolo** è possibile analizzare in avanti e indietro in una sequenza di transazioni di magazzino registrate per il numero seriale o di lotto.  

 Nella finestra **Naviga** non è possibile visualizzare la sequenza di transazioni, ma è possibile visualizzare tutti i record del numero seriale o di lotto, sia i movimenti registrati che i record aperti.  

 Le due funzionalità possono essere utilizzate in combinazione trasferendo un numero seriale o un numero di lotto analizzato alla finestra **Naviga** per completare lo scenario di analisi. Per ulteriori informazioni, vedere [Procedura dettagliata: Tracciabilità dei numeri seriali/di lotto](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Analizzare articoli tracciati  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Tracciabilità articolo**, quindi scegliere il collegamento correlato.  
2.  Nei campi di filtro nella parte superiore della finestra immettere numeri di articolo specifici o utilizzare un filtro per i numeri di articolo che si desidera analizzare.  
3.  Nel campo **Mostra componenti** definire se si desidera visualizzare anche la provenienza dei componenti dell'articolo. Le opzioni disponibili sono le seguenti.  

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**No**|selezionare questa opzione se non si desidera visualizzare i componenti.|  
    |**Solo articoli tracciati**|selezionare questa opzione se si desidera visualizzare solo i componenti con numeri di lotto o seriali.|  
    |**Tutto**|selezionare questa opzione se si desidera visualizzare tutti i componenti.|  

4.  Nel campo **Metodo analisi** selezionare il metodo che si desidera utilizzare per analizzare l'articolo. Sono disponibili le opzioni seguenti:  

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**Utilizzo->Origine**|Questo metodo consente di analizzare l'articolo a partire dal punto di entrata fino al punto di utilizzo. Se, ad esempio, un articolo lavorato è stato venduto a un cliente, nella finestra **Analisi articolo** viene prima visualizzata la riga di spedizione di vendita, che può essere espansa per individuare l'ordine di produzione di provenienza.|  
    |**Origine->Utilizzo**|questo metodo consente di analizzare l'articolo a partire dal punto di entrata nel magazzino fino al punto di utilizzo. Se, ad esempio, un articolo lavorato è stato venduto a un cliente, nella finestra **Analisi articolo** viene prima visualizzato l'ordine di produzione chiuso, che può essere espanso per individuare le righe di spedizione di vendita in cui l'articolo è stato utilizzato.|  

5.  Scegliere l'azione **Analizza** per eseguire l'analisi.  

> [!NOTE]  
>  Se uno stesso lotto è stato ricevuto in più transazioni, la finestra **Tracciabilità articolo** può non riportare tutte le transazioni. Solo le transazioni collegate vengono visualizzate.  

> [!NOTE]  
>  Se lo storico delle transazioni aggiuntive sotto una riga di analisi articolo è già stato analizzato da un'altra riga superiore, la casella di controllo **Elemento già analizzato** risulta selezionata. Per fornire una visualizzazione più semplice, tali righe sottostanti non sono mostrate.  
>   
>  Per individuare le righe di tracciabilità dell'articolo in cui lo storico delle transazioni è già stato analizzato, fare clic sul pulsante **Vai a Elemento già analizzato**. La riga di tracciabilità articolo in questione viene selezionata e tutte le righe sottostanti vengono espanse.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Per trovare gli articoli tracciati con la funzionalità Naviga  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Naviga**, quindi scegliere il collegamento correlato.  
2.  Nella Scheda dettaglio **Tracciabilità articolo**, nei campi **Nr. lotto** e **Nr. seriale**, immettere i numeri di tracciabilità articolo che si desidera analizzare.  
3.  Scegliere l'azione **Trova** per trovare tutte le istanze del numero seriale o di lotto nel database.  

## <a name="see-also"></a>Vedi anche  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Procedura: Impegnare articoli](inventory-how-to-reserve-items.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Procedura dettagliata: Tracciabilità dei numeri seriali/di lotto](walkthrough-tracing-serial-lot-numbers.md)

