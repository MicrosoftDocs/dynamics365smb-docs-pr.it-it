---
title: Tracciare gli articoli tracciati
description: 'È possibile analizzare dove è stato utilizzato un articolo tracciato, nonché ottenere informazioni su come e quando l''articolo è stato ricevuto, prodotto o reso con le funzionalità Tracciabilità articolo e Trova movimenti.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6520,'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="trace-item-tracked-items" />Tracciare gli articoli tracciati

È possibile analizzare dove è stato utilizzato un articolo tracciato, nonché ottenere informazioni su come e quando l'articolo è stato ricevuto o prodotto, trasferito, venduto, consumato o reso. È inoltre possibile trovare tutte le istanze correnti di un numero seriale o di un numero di lotto specifico nel database. A tale scopo si utilizzano le funzionalità Tracciabilità articolo e [Trova movimenti](ui-find-entries.md).  

Queste funzionalità possono essere particolarmente utili in ambito di controllo qualità quando è necessario determinare quali clienti hanno ricevuto prodotti con un numero di lotto specifico o quando si desidera stabilire da quale lotto proviene un componente difettoso.  

 Nella pagina **Tracciabilità articolo** è possibile analizzare in avanti e indietro in una sequenza di transazioni di magazzino registrate per il numero seriale o di lotto.  

 Nella pagina **Trova movimenti** non è possibile visualizzare la sequenza di transazioni, ma è possibile visualizzare tutti i record del numero seriale o di lotto, sia i movimenti registrati che i record aperti.  

 Le due funzionalità possono essere utilizzate in combinazione trasferendo un numero seriale o un numero di lotto analizzato alla pagina **Trova movimenti** per completare lo scenario di analisi. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items" />Analizzare articoli tracciati

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tracciabilità articolo**, quindi scegli il collegamento correlato.  
2.  Nei campi di filtro nella parte superiore della pagina immettere numeri di articolo specifici o utilizzare un filtro per i numeri di articolo che si desidera analizzare.  
3.  Nel campo **Mostra componenti** definisci se visualizzare anche la provenienza dei componenti dell'articolo. Nella seguente tabella vengono illustrate le opzioni.  

    |Campo|Descrizione|  
    |----------------------------------|---------------------------------------|  
    |**No**|Non visualizzare i componenti.|  
    |**Solo articoli tracciati**|Mostra solo i componenti che hanno numeri di lotto o di serie.|  
    |**Tutto**|Mostra tutti i componenti.|  

4.  Nel campo **Metodo analisi** seleziona il metodo da utilizzare per analizzare l'articolo. Nella seguente tabella vengono illustrate le opzioni.  

    |Campo|Descrizione|  
    |----------------------------------|---------------------------------------|  
    |**Utilizzo->Origine**|Analizza l'articolo dal punto di utilizzo al punto di entrata. Se, ad esempio, un articolo lavorato è stato venduto a un cliente, nella pagina **Analisi articolo** viene prima visualizzata la riga di spedizione di vendita, che può essere espansa per individuare l'ordine di produzione di provenienza.|  
    |**Origine->Utilizzo**|Analizza l'articolo dal punto di entrata in magazzino al punto di utilizzo. Se, ad esempio, un articolo lavorato è stato venduto a un cliente, nella pagina **Analisi articolo** viene prima visualizzato l'ordine di produzione chiuso, che può essere espanso per individuare le righe di spedizione di vendita in cui l'articolo è stato utilizzato.|  

5.  Scegliere l'azione **Analizza** per eseguire l'analisi.  

> [!NOTE]  
>  Solo le transazioni collegate vengono visualizzate. Se uno stesso lotto è stato ricevuto in più transazioni, la pagina **Tracciabilità articolo** può non riportare tutte le transazioni.   

> [!NOTE]  
>  Se lo storico delle transazioni aggiuntive sotto una riga di analisi articolo è già stato analizzato da un'altra riga superiore, la casella di controllo **Elemento già analizzato** risulta selezionata. Per fornire una visualizzazione più semplice, tali righe sottostanti non sono mostrate.  
>   
>  Per individuare le righe di tracciabilità dell'articolo in cui lo storico delle transazioni è già stato analizzato, fare clic sul pulsante **Vai a Elemento già analizzato**. La riga di tracciabilità articolo in questione viene selezionata e tutte le righe sottostanti vengono espanse.  

## <a name="to-find-item-tracked-items-with-find-entries" />Per trovare gli articoli tracciati con la funzionalità Trova movimenti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Trova movimenti**, quindi seleziona il collegamento correlato.  
2. Scegliere **Azioni** > **Trova per** > **Trova per riferimento articolo**.
3. Nei campi **Nr. lotto** e **Nr. seriale**, immettere i numeri di tracciabilità articolo che si desidera analizzare.  
4. Scegliere l'azione **Trova** per trovare tutte le istanze del numero seriale o di lotto nel database.  

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/prepare-item-tracking/)

## <a name="see-also" />Vedere anche

[Magazzino](inventory-manage-inventory.md)  
[Utilizzo dei numeri di serie, di lotto e di pacchetto](inventory-how-work-item-tracking.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Trova movimenti](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
