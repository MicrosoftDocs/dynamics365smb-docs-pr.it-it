---
title: 'Procedura: Impostare i modelli di stoccaggio | Documenti Microsoft'
description: "Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0316dfe2d8e601077ed67317b4a077036e0a8c33
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-put-away-templates"></a>Impostare i modelli di stoccaggio
Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse.  

È possibile impostare più modelli di stoccaggio e selezionarne uno per gestire gli stoccaggi nella warehouse. È inoltre possibile selezionare un modello di stoccaggio per qualsiasi articolo o unità di stockkeeping che presenta speciali requisiti di stoccaggio.  

## <a name="to-set-up-put-away-templates"></a>Per impostare i modelli di stoccaggio  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Modelli stoccaggio**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Specificare un codice che costituisce l'identificatore unico del modello da creare.  
4.  Se lo si desidera, immettere una breve descrizione.  
5.  Compilare la prima riga specificando i requisiti prioritari relativi alle collocazioni che dovranno essere soddisfatti nei suggerimenti per uno stoccaggio.  
6.  Compilare la seconda riga specificando i requisiti relativi alle collocazioni che dovranno essere soddisfatti in seconda istanza durante la ricerca di una collocazione per lo stoccaggio. La seconda riga viene utilizzata solo se non è possibile trovare una collocazione che soddisfi i requisiti specificati nella prima riga.  
7.  Compilare le righe successive fino a completa definizione di tutte le collocazioni accettabili che si desidera vengano utilizzate nel processo di stoccaggio.  
8.  Nell'ultima riga del modello di stoccaggio selezionare la casella di controllo **Trova collocazione variabile**.  

È possibile creare diversi modelli di stoccaggio e applicarli in base alle esigenze. Viene utilizzato innanzitutto il modello di stoccaggio selezionato per l'articolo o l'unità di stockkeeping, qualora disponibile. Se questi campi non vengono compilati, verrà utilizzato il modello di stoccaggio selezionato per la warehouse nella Scheda dettaglio **Criteri per collocazione** della scheda ubicazione.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

