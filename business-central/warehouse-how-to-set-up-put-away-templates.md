---
title: Impostare i modelli di stoccaggio
description: Usa i modelli di stoccaggio per farti suggerire le collocazioni più appropriate per i tuoi articoli in un dato momento.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '7312, 7313, 7314, 7321, 7322, 7323, 7329'
ms.date: 10/04/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Impostare i modelli di stoccaggio

Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse.  

È possibile impostare più modelli di stoccaggio e selezionarne uno per gestire gli stoccaggi nella warehouse. È inoltre possibile selezionare un modello di stoccaggio per qualsiasi articolo o unità di stockkeeping che presenta speciali requisiti di stoccaggio.  

## Per impostare i modelli di stoccaggio

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modelli di stoccaggio**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Specificare un codice che costituisce l'identificatore unico del modello da creare.  
4. Se lo si desidera, immettere una breve descrizione.  
5. Compilare la prima riga specificando i requisiti prioritari relativi alle collocazioni che dovranno essere soddisfatti nei suggerimenti per uno stoccaggio.

    Ad esempio, se si desidera che il metodo di stoccaggio predefinito sia basato su collocazioni fisse scegliere il campo **Trova collocazione fissa**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Compilare la seconda riga specificando i requisiti relativi alle collocazioni che dovranno essere soddisfatti in seconda istanza durante la ricerca di una collocazione per lo stoccaggio. La seconda riga viene utilizzata solo se non è possibile trovare una collocazione che soddisfi i requisiti specificati nella prima riga.  
7. Compilare le righe successive fino a completa definizione di tutte le collocazioni accettabili che si desidera vengano utilizzate nel processo di stoccaggio.  
8. Nell'ultima riga del modello di stoccaggio selezionare la casella di controllo **Trova collocazione variabile**.  

È possibile creare diversi modelli di stoccaggio e applicarli in base alle esigenze. Viene utilizzato innanzitutto il modello di stoccaggio selezionato per l'articolo o l'unità di stockkeeping, qualora disponibile. Se questi campi non vengono compilati, verrà utilizzato il modello di stoccaggio selezionato per la warehouse nella Scheda dettaglio **Criteri per collocazione** della scheda ubicazione.  

## Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)                                
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
