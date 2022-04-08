---
title: Ricerca di movimenti
description: In questo articolo viene descritto la correlazione tra documenti e movimenti
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: 344, 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6e6e6f6f622d1938fb2195bc2dde2c2ba689a59f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517689"
---
# <a name="finding-related-entries-for-posted-documents"></a>Ricerca di movimenti correlati per documenti registrati 

In questo articolo viene illustrato come trovare documenti e movimenti correlati tra loro in base a informazioni comuni, come:

- Numero del documento o data di registrazione
- Tipo di contatto commerciale, numero o numero di documento esterno
- Numero di serie dell'articolo o numero di lotto

Questa funzione risulta utile per cercare i movimenti contabili ottenuti da determinate transazioni. Durante la ricerca per numero di documento, è possibile stampare il riepilogo dal report Movimenti documento.

## <a name="get-started"></a>Inizia

La funzione Trova movimenti è immediatamente disponibile sulla maggior parte delle pagine che visualizzano documenti registrati o movimenti di documenti registrati, sia per elenchi che per schede. Quindi il primo passo è aprire una di queste pagine. Quindi, scegli l'azione **Trova movimenti** o premi i tasti Ctrl+Alt+G.

La pagina **Trova movimenti** include tutti i documenti e i movimenti correlati basati sul numero di documento e sulla data di registrazione. La pagina è divisa in tre sezioni:

- La sezione superiore mostra i campi e le azioni che si utilizzano per filtrare la ricerca.
- La sezione centrale mostra i documenti correlati in base alla ricerca.
- La sezione inferiore mostra le informazioni sul documento di origine trovato durante la ricerca.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Ricerca di movimenti

È possibile cercare movimenti in base alle informazioni sul documento, al contatto commerciale o al riferimento articolo. Per modificare la ricerca, selezionare **Azioni**, **Trova per**, quindi una delle seguenti azioni:

|Azione|Descrizione|
|------|-----------|
|Trova per documento|Visualizzare i movimenti in base a un numero di documento o una data di registrazione specifici.|
|Contatto business |Visualizzare i movimenti in base a un tipo di contatto specifico, numero di contatto e/o numero di documento esterno. È possibile immettere le informazioni sul documento assegnato da un fornitore o un cliente. Utilizzare i campi disponibili per ricercare i documenti del fornitore utilizzando i numeri da lui assegnati ai documenti.|
|Riferimento articolo|Visualizzare i movimenti in base a un numero di serie o un numero di lotto. È possibile immettere il numero seriale o di lotto oppure un filtro sui numeri seriali o di lotto di cui si desidera eseguire la ricerca. Questa azione risulta utile per visualizzare elementi in cui è stato utilizzato un numero di tracciabilità articolo specifico, individuarne il fornitore di origine o il cliente a cui è stata effettuata la vendita.|

Dopo aver effettuato una selezione, inserire le informazioni di ricerca pertinenti nei campi in alto. Usare i suggerimenti dei campi come aiuto. Al termine, scegliere **Trova** per avviare la ricerca. Se si modifica qualsiasi filtro, è necessario scegliere nuovamente **Trova**.

> [!TIP]
> Per un paio di esempi sull'uso di **Trova voci**, vedi [Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md) <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Utilizzare Business Central](ui-work-product.md)  
[Aggiungere un'azione di pagina a Gestione ruolo utente](ui-bookmarks.md)  
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
