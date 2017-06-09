---
title: 'Procedura: Trovare documenti registrati senza record di documenti in entrata | Documenti Microsoft'
description: 'Procedura: Trovare documenti registrati senza record di documenti in entrata'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e0925bde31e7079ca9f3d0f7acb16d4dd75c1987
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-find-posted-documents-without-incoming-document-records"></a>Procedura: Trovare documenti registrati senza record di documenti in entrata
Nelle finestre **Piano dei conti** e **Movimenti C/G** è possibile utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti di vendita e di acquisto registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Per trovare documenti registrati senza record di documenti in entrata
1. Nell'angolo superiore destro scegliere l'icona **Ricerca della pagina o del report** ![Ricerca della pagina o del report](media/ui-search/search_small.png "icona Ricerca della pagina o del report"), inserire **Piano dei conti**, quindi scegliere il collegamento correlato.
2. Selezionare una riga relativa a un conto CO/GE per quei movimenti di contabilità generale di cui si desidera vedere i documenti di vendita e di acquisto registrati senza record di documenti in entrata. Quindi scegliere l'azione **Documenti registrati senza documento in entrata**.
3. In alternativa, scegliere l'azione **Movimenti contabili**.
4. Nella finestra **Movimenti C/G**, scegliere l'azione **Documenti registrati senza documenti in entrata**.

Viene visualizzata la finestra **Documenti registrati senza documento in entrata** che mostra i documenti di vendita e di acquisto registrati senza i record di documenti in entrata rappresentati dai movimenti di contabilità generale nel conto COGE per il quale è stata aperta la finestra. La finestra può visualizzare un massimo di 1.000 righe. Per impostazione predefinita, il campo **Filtro data** contiene quindi un filtro che limita la visualizzazione ai movimenti con date di registrazione dall'inizio del periodo contabile alla data del lavoro.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Per connettere i documenti trovati a record di documento in entrata esistenti
1. Nella finestra **Documenti registrati senza documento in entrata** selezionare la riga relativa a un documento registrato che si desidera connettere a un record di documento in entrata esistente, quindi scegliere l'azione **Documenti registrati senza documento in entrata**.
2. Nella finestra **Documenti in entrata** selezionare il record di documento in entrata che si desidera connettere al documento registrato trovato, quindi scegliere **OK**.
3. Nella finestra **Documenti registrati senza documento in entrata**, il record di documento in entrata selezionato è ora connesso al documento registrato, come indicato nel Dettaglio informazioni **File documento in entrata**.

Se nella finestra **Documenti in entrata** non è presente un record di documento in entrata adeguato, è possibile crearlo. Per ulteriori informazioni, vedere [Procedura: Creare i record di documenti in entrata](across-how-create-income-document-records.md).

## <a name="see-also"></a>Vedi anche
[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

