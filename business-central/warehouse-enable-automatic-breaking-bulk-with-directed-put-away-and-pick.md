---
title: Breakbulk automatico con stoccaggi e prelievi guidati | Documenti Microsoft
description: Per le ubicazioni che utilizzano stoccaggi e prelievi guidati, è possibile suddividere unità di misura più grandi in unità di misura più piccole, durante la creazione delle istruzioni di warehouse che consentono di soddisfare le richieste di documenti di origine, ordini di produzione o prelievi e stoccaggi interni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ea8cbc3b701d8e4fab0d720390db7bab6e1a4e59
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914762"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Abilitare breakbulk automatico con stoccaggi e prelievi guidati
Per le ubicazioni che utilizzano stoccaggi e prelievi guidati, [!INCLUDE[d365fin](includes/d365fin_md.md)] consente di eseguire in varie situazioni il breakbulk automatico, ovvero la suddivisione di unità di misura più grandi in unità di misura più piccole, durante la creazione delle istruzioni di warehouse che consentono di soddisfare le richieste di documenti di origine, ordini di produzione o prelievi e stoccaggi interni. Talvolta il breakbulk consente di raggruppare unità di misura più piccole, se necessario, in modo da soddisfare le richieste in uscita suddividendo le unità di misura più grandi nel documento di origine o nell'ordine di produzione in unità di misura più piccole disponibili nella warehouse.   

## <a name="breakbulking-in-picks"></a>Breakbulk relativo ai prelievi  
Se si desidera immagazzinare articoli con unità di misura differenti e consentire di combinarli automaticamente a seconda delle esigenze nel processo di prelievo, selezionare il campo **Permettere breakbulk** nella scheda ubicazione.  

Per eseguire un'attività, l'applicazione cerca automaticamente un articolo con la stessa unità di misura. Se tuttavia non è possibile individuare l'articolo sotto tale forma e il campo è selezionato, viene automaticamente suggerito di convertire un'unità di misura più grande nell'unità di misura richiesta.  

Se vengono individuate solo le unità di misura più piccole, viene suggerito di raggruppare gli articoli in modo da soddisfare la quantità specificata nell'ordine di spedizione o di produzione. Di fatto, l'unità di misura più grande riportata nel documento di origine viene suddivisa in unità di misura più piccole per il prelievo.  

## <a name="breakbulking-in-put-aways"></a>Breakbulk relativo agli stoccaggi  
Durante lo stoccaggio nella warehouse, la dimensione automaticamente suggerita nelle righe di azione Mettere è l'unità di misura di stoccaggio, ad esempio pezzi, anche se gli articoli giungono nella warehouse in unità di misura differenti.  

## <a name="breakbulking-in-movements"></a>Breakbulk relativo ai movimenti  
L'applicazione esegue automaticamente il breakbulk anche nei movimenti di rifornimento qualora venga selezionato il campo **Permettere breakbulk** della Scheda dettaglio **Opzione** nella pagina **Calcola rifornimento collocazione**.  

I risultati del processo di conversione da un'unità di misura all'altra possono essere visualizzati come righe di breakbulk intermedie nelle istruzioni di stoccaggio, prelievo o movimento.  

> [!NOTE]  
>  Se si seleziona il campo **Impostare filtro breakbulk** dell'intestazione delle istruzioni relative alla warehouse, le righe di breakbulk vengono automaticamente nascoste ogni volta che viene utilizzata l'intera unità di misura più grande. Se, ad esempio, un pallet è costituito da 12 pezzi e viene utilizzata l'intera unità di misura (12 pezzi), viene indicato di prelevare 1 pallet e posizionare 12 pezzi. Se, tuttavia, occorre prelevare solo 9 pezzi, le righe di breakbulk non vengono nascoste, anche se è stato selezionato il campo **Filtro breakbulk**, in quanto è necessario trovare una collocazione per i tre pezzi rimanenti all'interno della warehouse.  

> [!NOTE]  
>  Se si desidera ottimizzare l'impiego delle unità di misura nell'applicazione di warehouse, anche in concomitanza con l'utilizzo della funzionalità di breakbulk, si consiglia di eseguire, ove possibile, le seguenti operazioni:  
>   
> - Impostare l'unità di misura di base per un articolo sull'unità di misura minima che si prevede di gestire nelle attività di warehouse.  
> - Impostare unità di misura alternative per l'articolo utilizzando multipli dell'unità di base.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
