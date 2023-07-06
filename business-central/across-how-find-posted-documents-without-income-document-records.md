---
title: Trovare documenti registrati senza documenti in entrata
description: 'È possibile cercare i movimenti di contabilità generale per i documenti di vendita e di acquisto registrati che non presentano documenti elettronici in entrata, quali fatture importate.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="find-posted-documents-without-incoming-document-records"></a><a name="find-posted-documents-without-incoming-document-records"></a><a name="find-posted-documents-without-incoming-document-records"></a>Trovare documenti registrati senza record di documenti in entrata

Nelle pagine **Piano dei conti** e **Movimenti C/G** puoi utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti di vendita e di acquisto registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati.

## <a name="to-find-posted-documents-without-incoming-document-records"></a><a name="to-find-posted-documents-without-incoming-document-records"></a><a name="to-find-posted-documents-without-incoming-document-records"></a>Per trovare documenti registrati senza record di documenti in entrata

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Piano dei conti**, quindi scegli il collegamento correlato.
2. Selezionare una riga relativa a un conto CO/GE per quei movimenti di contabilità generale di cui si desidera vedere i documenti di vendita e di acquisto registrati senza record di documenti in entrata. Quindi scegliere l'azione **Documenti registrati senza documento in entrata**.
3. In alternativa, scegliere l'azione **Movimenti contabili**.
4. Nella pagina **Movimenti C/G**, scegliere l'azione **Documenti registrati senza documenti in entrata**.

Viene visualizzata la pagina **Documenti registrati senza documento in entrata** che mostra i documenti di vendita e di acquisto registrati senza i record di documenti in entrata rappresentati dai movimenti di contabilità generale nel conto COGE per il quale è stata aperta la pagina. La pagina può visualizzare un massimo di 1.000 righe. Per impostazione predefinita, il campo **Filtro data** contiene quindi un filtro che limita la visualizzazione ai movimenti con date di registrazione dall'inizio del periodo contabile alla data del lavoro.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><a name="to-connect-found-documents-to-existing-incoming-document-records"></a><a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Per connettere i documenti trovati a record di documento in entrata esistenti

1. Nella pagina **Documenti registrati senza documento in entrata** selezionare la riga relativa a un documento registrato che si desidera connettere a un record di documento in entrata esistente, quindi scegliere l'azione **Documenti registrati senza documento in entrata**.
2. Nella pagina **Documenti in entrata** selezionare il record di documento in entrata che si desidera connettere al documento registrato trovato, quindi scegliere **OK**.
3. Nella pagina **Documenti registrati senza documento in entrata**, il record di documento in entrata selezionato è ora connesso al documento registrato, come indicato nel Dettaglio informazioni **File documento in entrata**.

Se nella pagina **Documenti in entrata** non è presente un record di documento in entrata adeguato, è possibile crearlo. Per ulteriori informazioni, vedere [Creare i record di documenti in entrata](across-how-create-income-document-records.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Creare i record di documenti in entrata](across-how-create-income-document-records.md)
[Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md)
[Creare i record di documenti in entrata direttamente da documenti e movimenti](across-how-connect-disconnect-income-document-records.md)
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
