---
title: 'Procedura: Prelevare articoli per la spedizione warehouse | Documenti Microsoft'
description: Quando l'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi e delle spedizioni warehouse, è possibile utilizzare i documenti di prelievo warehouse per creare ed elaborare le informazioni di prelievo prima della registrazione della spedizione warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: fe91ed57af6a93f874ead85f53c97358068e0b4c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192970"
---
# <a name="pick-items-for-warehouse-shipment"></a>Prelevare articoli per la spedizione warehouse
Quando l'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi e delle spedizioni warehouse, è possibile utilizzare i documenti di prelievo warehouse per creare ed elaborare le informazioni di prelievo prima della registrazione della spedizione warehouse.  

Non è possibile creare un documento di prelievo warehouse da zero perché un'attività di prelievo fa sempre parte di un flusso di lavoro, in uno scenario di tipo push o pull.  

È possibile creare documenti di prelievo warehouse in modalità pull aprendo un documento di spedizione warehouse vuoto, rilevare i documenti di origine rilasciati per la spedizione, quindi creare righe di prelievo warehouse per tali spedizioni. È possibile utilizzare le funzioni **Prendi documenti origine** o **Usa filtri per richiamare doc. orig.** per rilevare i documenti di origine pronti per la spedizione.

In alternativa, è possibile utilizzare la pagina **Prospetto prelievi** per estrarre e creare righe prelievo in modalità batch. Per ulteriori informazioni, vedere [Pianificare i prelievi nei prospetti](warehouse-how-to-plan-picks-in-worksheets.md).  

È inoltre possibile creare documenti di prelievo warehouse in modalità push dalla pagina **Spedizione warehouse** selezionando **Crea prelievo**.  

> [!NOTE]  
>  Il prelievo per la spedizione warehouse di articoli assemblati nell'ordine di vendita spedito segue gli stessi passaggi dei normali prelievi warehouse per la spedizione, come descritto in questo argomento. Tuttavia, il numero delle righe prelievo per quantità da spedire può essere molti a uno perché vengono selezionati i componenti, non l'articolo assemblato.  
>   
>  Le righe prelievi warehouse vengono create per il valore nel campo **Quantità residua** sulle righe dell'ordine di assemblaggio collegato alla riga dell'ordine di vendita spedito. In questo modo si garantisce che tutti i componenti vengano prelevati con una sola azione.  
>   
>  Per ulteriori informazioni, vedere la sezione "Gestione di articoli da assemblare su ordine in spedizioni warehouse".  
>   
>  Per informazioni sul prelievo generale di componenti per gli ordini di assemblaggio, incluse le situazioni in cui l'articolo di assemblaggio non fa parte di una spedizione vendita, vedere [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md)..  

## <a name="to-pick-items-for-warehouse-shipment"></a>Per prelevare articoli per la spedizione warehouse  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prelievi** e quindi scegliere il collegamento correlato.  

    Se è necessario utilizzare un determinato prelievo, selezionare il prelievo dalla lista oppure filtrare la lista per individuare i prelievi specificatamente assegnati a se stessi. Aprire la scheda prelievo.  
2.  Se il campo **ID utente assegnato** è vuoto, immettere il proprio ID per identificarsi, se necessario.  
3.  Eseguire il prelievo effettivo di articoli.  

    Se la warehouse prevede l'utilizzo di collocazioni, vengono utilizzate le collocazioni di default degli articoli per suggerire la posizione da cui prelevare gli articoli. Le istruzioni verranno visualizzate su due righe distinte, una per ciascun tipo di azione, ovvero Prendere e Mettere.  

    Se la warehouse prevede l'utilizzo di stoccaggi e prelievi guidati, viene utilizzata la valutazione collocazione per calcolare le migliori collocazioni da cui effettuare il prelievo e tali collocazioni vengono quindi suggerite nelle righe prelievo. Le istruzioni verranno visualizzate su due righe distinte, una per ciascun tipo di azione, ovvero Prendere e Mettere.  

4.  Dopo avere prelevato e posizionato gli articoli nell'area di spedizione o nella collocazione di spedizione, scegliere l'azione **Registra prelievo**.  

A questo punto, la persona responsabile della spedizione può immettere gli articoli al dock di spedizione e registrare la spedizione, incluso il documento di origine correlato, nella pagina **Spedizione warehouse**. Per ulteriori informazioni, vedere [Spedire articoli](warehouse-how-ship-items.md).   

Oltre al prelievo per i documenti di origine, come descritto in questo argomento, è possibile estrarre e inserire articoli tra le collocazioni senza fare riferimento ai documenti di origine. Per ulteriori informazioni, vedere [Selezionare e stoccare senza un documento di origine](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Gestione di articoli da assemblare su ordine in spedizioni warehouse
Negli scenari di assemblaggio su ordine il campo **Qtà da spedire** sulle righe spedizione warehouse viene utilizzato per registrare il numero di unità assemblate. La quantità specificata viene quindi registrata come output assemblaggio quando viene registrata la spedizione warehouse.

Per altre righe spedizione warehouse, il valore del campo **Qtà da spedire** è uguale a zero dall'inizio.

Quando completano l'assemblaggio delle parti o di tutta la quantità da assemblare su ordine, i lavoratori lo registrano nel campo **Qtà da spedire** sulla riga spedizione warehouse e scelgono l'azione **Registrare spedizione**. In questo modo viene registrato l'output assemblaggio corrispondente, incluso il consumo di componenti. Una spedizione di vendita per la quantità viene registrata per l'ordine di vendita.

Nell'ordine di assemblaggio è possibile scegliere **Riga spediz. whse. assem. su ordine** per accedere alla riga spedizione warehouse. Questa operazione è conveniente per i lavoratori che in genere non utilizzano la pagina **Spedizione warehouse**.

Dopo che la spedizione warehouse è stata registrata, i vari campi sulla riga ordine di vendita vengono aggiornati per mostrare lo stato di avanzamento nel warehouse. I seguenti campi vengono inoltre aggiornati per mostrare le quantità rimanente da assemblare su ordine e spedire:

- **Qtà inevasa whse. per assemblaggio su ordine**
- **Qtà inevasa whse. per assemblaggio su ordine (base)**

> [!NOTE]
> Negli scenari di combinazione, in cui una parte della quantità deve essere assemblata e un'altra deve essere spedita dal magazzino, vengono create due righe spedizione warehouse. Una riga corrisponde alla quantità da assemblare su ordine, mentre l'altra corrisponde alla quantità di magazzino.

> In questo caso, la quantità da assemblare su ordine viene gestita come descritto in questo argomento, mentre la quantità di magazzino viene gestita come qualsiasi altra normale riga spedizione warehouse. Per altre informazioni sugli scenari di combinazione, vedere [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
