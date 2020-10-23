---
title: Importazione di numerose immagini articolo da un file ZIP| Microsoft Docs
description: È possibile importare più immagini articolo contemporaneamente. Assegnare ai file immagine dei nomi che corrispondono ai numeri degli articoli, comprimere i file in un file zip, quindi utilizzare la pagina Importa immagini articolo per gestire le immagini articolo da importare.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4da0f30f47827515f8591802ce2ca49c245009ab
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922896"
---
# <a name="import-multiple-item-pictures"></a>Importare molteplici immagini articolo
È possibile importare più immagini articolo contemporaneamente. Assegnare ai file immagine dei nomi che corrispondono ai numeri degli articoli, comprimere i file in un file ZIP, quindi utilizzare la pagina **Importa immagini articolo** per gestire le immagini articolo da importare.

Tutti i formati di file comuni sono supportati.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Per denominare i file immagine con i nile degli articoli e prepare il file ZIP
1. Nella posizione in cui le immagini articolo sono archiviate, assegnare un nome a ciascun file in base al numero dell'articolo correlato. Ad esempio:

    |Nr. Articolo|Nome file|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Comprimere tutti i file in un file ZIP. Ad esempio, in Windows Explorer, selezionare i file, quindi scegliere **Invia a**, **Cartella compressa**.     

## <a name="to-import-item-pictures"></a>Per importare immagini articolo
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup magazzino** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Importa immagini articolo**.
3. Nel campo **Selezionare un file zip**, selezionare la cartella ZIP pertinente quindi scegliere il pulsante **Apri**.

    Una riga per ciascun articolo e immagine viene creata nella pagina **Importa immagini articolo**.

    > [!NOTE]
    > Per le schede articolo che hanno già un'immagine, la casella di controllo **L'immagine esiste già** è selezionata. Se non si desidera sostituire alcuna immagine esistente, deselezionare la casella di controllo **Sostituisci immagini**. Se non si desidera sostituire singole immagini esistenti, eliminare le righe in questione.

3. Scegliere l'azione **Importa immagini**.

Il campo **Stato importazione** viene aggiornato per indicare se l'importazione di un'immagine è stata ignorata o completata.       

## <a name="see-also"></a>Vedere anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
