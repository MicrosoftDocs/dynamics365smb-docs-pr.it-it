---
title: Come pianificare prelievi nei prospetti
description: Scopri come rendere disponibili le righe sui documenti di spedizione nei fogli di lavoro di prelievo per gli addetti al magazzino.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 667aa2702d064e44b9b52dc167e2372f98d7944f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530407"
---
# <a name="plan-picks-in-worksheets"></a>Pianificare prelievi nei prospetti

Se il tuo magazzino è impostato per richiedere l'elaborazione sia del prelievo che della spedizione, puoi scegliere di rendere disponibili le righe sui documenti di spedizione nei fogli di lavoro di prelievo invece delle istruzioni di prelievo.  

> [!NOTE]  
> Se le istruzioni di prelievo da warehouse sono già state create e vuoi combinarle in un'unica istruzione di prelievo per migliorarne l'efficienza, è necessario eliminare i singoli prelievi da warehouse. Le righe da prelevare possono essere ora elencate nel prospetto di prelievo.  

Nella pagina **Prospetti prelievi** puoi impostare le liste di prelievo che aiutano i dipendenti a raccogliere gli articoli nel magazzino. La pagina mostra le quantità disponibili nelle collocazioni cross-dock, utili per pianificare le assegnazioni del lavoro in situazioni di cross-dock. [!INCLUDE[prod_short](includes/prod_short.md)] proporrà sempre prima un prelievo da una collocazione cross-dock. Le righe nel foglio di lavoro possono provenire da diversi documenti di origine. Ad esempio, possono provenire da più ordini di vendita. 

> [!NOTE]  
> Il prelievo di articoli assemblati per un ordine di vendita spedito segue gli stessi passaggi dei normali prelievi warehouse per la spedizione. Tuttavia, il numero delle righe prelievo per quantità da spedire può essere molti a uno perché vengono selezionati i componenti, non l'articolo assemblato.  
>
> Le righe prelievi warehouse vengono create per il valore nel campo **Quantità residua** sulle righe dell'ordine di assemblaggio collegato alla riga dell'ordine di vendita spedito. In questo modo si garantisce che tutti i componenti vengano prelevati con una sola azione. Per altre informazioni, vedere [Vendere gli articoli di magazzino nei flussi di assemblaggio su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Per informazioni sul prelievo generale di componenti per gli ordini di assemblaggio, incluse le situazioni in cui l'articolo di assemblaggio non fa parte di una spedizione vendita, vedere [Prelevare per assemblaggio o produzione in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Ordinamento delle righe su un prospetto prelievi

Puoi ordinare le righe per articolo, numero di scaffale, documento di origine, data di scadenza o destinazione. Di seguito vengono forniti alcuni esempi di ordinamento utili.

* Se effettui l'ordinamento in base alla data di scadenza, puoi scegliere di eliminare tutte le righe, eccetto quelle che richiedono attenzione immediata. Le righe meno urgenti non vengono di fatto eliminate, ma vengono semplicemente inviate di nuovo al prospetto **Selezione prelievo**. Le righe vengono ordinate in base alla data di scadenza alla creazione del prelievo e, pertanto, puoi assegnare direttamente il prelievo a un addetto.
* Se le tue collocazioni sono numerate in modo da corrispondere al layout fisico del magazzino, l'ordinamento delle righe per numero di collocazione può semplificare il prelievo di più spedizioni contemporaneamente. 
* Se utilizzi la valutazione collocazione, l'ordinamento in base alla classifica può far risparmiare un po' di tempo. 
* Puoi ordinare per destinazione, consentendoti di assemblare e spedire gli ordini per cliente.

## <a name="to-plan-picks-in-the-worksheet"></a>Per pianificare prelievi nel prospetto

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto prelievi**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Prendi documenti warehouse**.  
3. Selezionare le spedizioni per cui preparare un prelievo. Puoi ordinare le righe, ma l'ordinamento non verrà applicato all'istruzione di prelievo. È inoltre possibile eliminare alcune righe per creare un prelievo più efficace. Se ad esempio vi sono più righe con articoli nelle collocazioni di cross-dock, puoi creare un prelievo per tutte le righe. Gli articoli sottoposti a cross-dock verranno spediti insieme agli altri articoli e nelle collocazioni di cross-dock sarà disponibile una maggiore quantità di spazio per ulteriori articoli in entrata.  
4. Scegli l'azione **Crea prelievo** e compila la pagina **Crea prelievo**. Le righe di prelievo create verranno ordinate in base ai criteri di ordinamento specificati in questa finestra. È ad esempio possibile creare un prelievo per ciascuna zona e ordinare le righe in base alla valutazione della collocazione all'interno di ciascun prelievo.  
5. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prelievi warehouse**, quindi scegli il collegamento correlato. Viene visualizzata la pagina **Prelievi warehouse**.  
6. È possibile individuare l'assegnazione di prelievo selezionando il prelievo con il numero più elevato.  
7. Se necessario, puoi assegnare un utente diverso o ordinare le righe in modo diverso.  
8. Scegliere l'azione **Stampa** per stampare le istruzioni per il prelievo.  
9. Dopo avere completato il prelievo, scegli l'azione **Registra**.  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a>Vedere anche

[Warehouse Management](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
