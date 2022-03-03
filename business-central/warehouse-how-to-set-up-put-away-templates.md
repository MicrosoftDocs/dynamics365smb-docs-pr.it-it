---
title: Impostare i modelli di stoccaggio
description: Usa i modelli di stoccaggio per farti suggerire le collocazioni più appropriate per i tuoi articoli in un dato momento.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7312, 7313, 7314, 7321, 7322, 7323, 7329
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 0498ac73900c151bab10ad10ac7bbf85ebdd8526
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129476"
---
# <a name="set-up-put-away-templates"></a>Impostare i modelli di stoccaggio

Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse.  

È possibile impostare più modelli di stoccaggio e selezionarne uno per gestire gli stoccaggi nella warehouse. È inoltre possibile selezionare un modello di stoccaggio per qualsiasi articolo o unità di stockkeeping che presenta speciali requisiti di stoccaggio.  

## <a name="to-set-up-put-away-templates"></a>Per impostare i modelli di stoccaggio

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Modelli di stoccaggio**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Specificare un codice che costituisce l'identificatore unico del modello da creare.  
4. Se lo si desidera, immettere una breve descrizione.  
5. Compilare la prima riga specificando i requisiti prioritari relativi alle collocazioni che dovranno essere soddisfatti nei suggerimenti per uno stoccaggio.

    Ad esempio, se si desidera che il metodo di stoccaggio predefinito sia basato su collocazioni fisse scegliere il campo **Trova collocazione fissa**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Compilare la seconda riga specificando i requisiti relativi alle collocazioni che dovranno essere soddisfatti in seconda istanza durante la ricerca di una collocazione per lo stoccaggio. La seconda riga viene utilizzata solo se non è possibile trovare una collocazione che soddisfi i requisiti specificati nella prima riga.  
7. Compilare le righe successive fino a completa definizione di tutte le collocazioni accettabili che si desidera vengano utilizzate nel processo di stoccaggio.  
8. Nell'ultima riga del modello di stoccaggio selezionare la casella di controllo **Trova collocazione variabile**.  

È possibile creare diversi modelli di stoccaggio e applicarli in base alle esigenze. Viene utilizzato innanzitutto il modello di stoccaggio selezionato per l'articolo o l'unità di stockkeeping, qualora disponibile. Se questi campi non vengono compilati, verrà utilizzato il modello di stoccaggio selezionato per la warehouse nella Scheda dettaglio **Criteri per collocazione** della scheda ubicazione.  

## <a name="see-also"></a>Vedi anche

[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]