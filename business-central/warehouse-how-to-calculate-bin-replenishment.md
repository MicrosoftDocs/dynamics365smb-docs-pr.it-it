---
title: Calcola rifornimento collocazione
description: Quando l'ubicazione è impostata per l'utilizzo di stoccaggi e prelievi guidati, per effettuare lo stoccaggio dei carichi vengono prese in considerazione le priorità del modello di stoccaggio per l'ubicazione.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 7315, 7351
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0f2653087df90ca6801f0d2e972f142e1f65b889
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530813"
---
# <a name="calculate-bin-replenishment"></a>Calcola rifornimento collocazione

Quando l'ubicazione è impostata per l'utilizzo di stoccaggi e prelievi guidati, per effettuare lo stoccaggio dei carichi vengono prese in considerazione le priorità del modello di stoccaggio per l'ubicazione. Le priorità includono le quantità minima e massima di contenuto collocazione fissate per una collocazione specifica e le valutazioni delle collocazioni. Pertanto, se gli articoli giungono in magazzino a intervalli regolari, le collocazioni di prelievo più utilizzate vengono riempite non appena vengono svuotate.  

Tuttavia, non sempre la frequenza di arrivo degli articoli in magazzino è costante. Talvolta la società acquista grandi quantitativi di articoli in modo da ottenere una riduzione sul prezzo oppure l'unità di produzione può attendere che venga terminato un intero lotto di un singolo articolo in modo da ridurre il costo unitario. In tal caso, l'arrivo degli articoli nella warehouse si interromperà per un certo periodo e si renderà necessario spostare periodicamente gli articoli dalle aree di immagazzinamento a massa alle collocazioni di prelievo.  

È inoltre possibile che sia previsto l'arrivo di una nuova partita di merce a breve termine e si desideri svuotare l'area di immagazzinamento a massa prima che gli articoli giungano nella warehouse.  

Infine, se per le collocazioni di immagazzinamento a massa è stato impostato un tipo di collocazione a cui è associata la sola azione **Stoccaggio**, ovvero per il tipo di collocazione non è stata selezionata l'azione **Prelievo**, sarà necessario rifornire continuamente le collocazioni di prelievo poiché non vengono forniti suggerimenti circa le collocazioni di tipo stoccaggio per un prelievo delle quantità in giacenza.  

## <a name="to-replenish-pick-bins"></a>Per rifornire le collocazioni di prelievo

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto movimentazioni**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Calcola rifornimento collocazione** per aprire la pagina di richiesta report.  
3.  Compilare i campi della pagina di richiesta del processo batch in modo da circoscrivere l'ambito dei suggerimenti calcolati relativi al rifornimento. È ad esempio possibile che si sia interessati solo a specifici articoli, zone o collocazioni.  
4.  Scegliere il pulsante **OK**. Le righe vengono create per i movimenti di rifornimento da eseguire in base alle regole impostate per le collocazioni e il relativo contenuto, ovvero articoli nelle collocazioni.  
5.  Se si desidera effettuare tutti i rifornimenti suggeriti, scegliere l'azione **Crea movimento**. A questo punto, gli impiegati potranno visualizzare le istruzioni utilizzando la voce di menu **Movimentazioni**, eseguirle e registrarle.  
6.  Se si desidera che vengano eseguiti solo alcuni suggerimenti, eliminare le righe meno importanti e creare un movimento.  

Al successivo calcolo per il rifornimento delle collocazioni, i suggerimenti precedentemente eliminati verranno ricreati, qualora risultino ancora validi.  

> [!NOTE]  
>  Se per l'articolo vengono soddisfatte le seguenti condizioni:  
>   
>  -   L'articolo ha una data di scadenza  
> -   Il campo **Prelievo in base a FEFO** della scheda ubicazione viene selezionato  
> -   Viene utilizzata la funzionalità **Calcola rifornimento collocazione**  
>   
>  I campi **Dal codice zona** e **Dal codice collocazione** non saranno specificati, in quanto l'algoritmo per calcolare la posizione in cui spostare gli articoli viene attivato solo quando si utilizza la funzione **Crea movimento**.  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/move-items/)

## <a name="see-also"></a>Vedere anche

[Warehouse Management](warehouse-manage-warehouse.md)  
[Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
