---
title: Importazione di numerose immagini articolo da un file ZIP
description: 'Per importare più immagini articolo, assegna ai file immagine dei nomi che corrispondono ai numeri degli articoli, comprimi i file in un file ZIP, quindi utilizza la pagina Importa immagini articolo.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Importare molteplici immagini articolo
È possibile importare più immagini articolo contemporaneamente. Assegnare ai file immagine dei nomi che corrispondono ai numeri degli articoli, comprimere i file in un file zip, quindi utilizzare la pagina Importa immagini articolo per gestire le immagini articolo da importare.

Tutti i formati di file comuni sono supportati.

## Per denominare i file immagine con i nile degli articoli e prepare il file ZIP
1. Nella posizione in cui le immagini articolo sono archiviate, assegnare un nome a ciascun file in base al numero dell'articolo correlato. Ad esempio:

    |Nr. Articolo|Nome file|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Comprimere tutti i file in un file ZIP. Ad esempio, in Windows Explorer, selezionare i file, quindi scegliere **Invia a**, **Cartella compressa**.     

## Per importare immagini articolo
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup magazzino**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Importa immagini articolo**.
3. Nel campo **Selezionare un file zip**, selezionare la cartella ZIP pertinente quindi scegliere il pulsante **Apri**.

    Una riga per ciascun articolo e immagine viene creata nella pagina **Importa immagini articolo**.

    > [!NOTE]
    > Per le schede articolo che hanno già un'immagine, la casella di controllo **L'immagine esiste già** è selezionata. Se non si desidera sostituire alcuna immagine esistente, deselezionare la casella di controllo **Sostituisci immagini**. Se non si desidera sostituire singole immagini esistenti, eliminare le righe in questione.

3. Scegliere l'azione **Importa immagini**.

Il campo **Stato importazione** viene aggiornato per indicare se l'importazione di un'immagine è stata ignorata o completata.       

## Vedere anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]