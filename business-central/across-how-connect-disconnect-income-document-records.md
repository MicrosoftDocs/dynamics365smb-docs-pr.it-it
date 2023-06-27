---
title: Creare i record di documenti in entrata da documenti
description: Puoi archiviare i documenti aziendali esterni allegando i file del documento ai record di documento in entrata correlati.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries" />Creare i record di documenti in entrata direttamente da documenti e movimenti

È possibile archiviare i documenti aziendali esterni in [!INCLUDE[prod_short](includes/prod_short.md)] allegando i file del documento ai record di documento in entrata correlati. Se il documento, ad esempio una fattura di acquisto, non è stato creato come record di documento in arrivo, è comunque possibile creare e connettere ad esso un record di documento in arrivo in un secondo momento. È inoltre possibile allegare file di documento in entrata a documenti di vendita e di acquisto registrati e a movimenti di contabilità cliente o fornitore utilizzando il Dettaglio informazioni di **File di documento in entrata** ad esempio nelle pagine **Fatture acquisto registrate** e **Movimenti contabili fornitori**.

Nelle pagine **Piano dei conti** e **Movimenti C/G** puoi utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti di vendita e di acquisto registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati. Per ulteriori informazioni, vedere [Trovare documenti registrati senza record di documenti in entrata](across-how-find-posted-documents-without-income-document-records.md).

Le procedure riportate di seguito mostrano come allegare un file a un movimento contabile fornitore o una fattura di acquisto esistente che non è stata creata da un record di documento in entrata. L'operazione di allegare un file a documenti di vendita o di acquisto registrati funziona in modo analogo.

## <a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice" />Per creare e connettere un record di documento in entrata da una fattura di acquisto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.
2. Selezionare la riga relativa a una fattura di acquisto a cui si desidera allegare un file e quindi scegliere l'azione **Crea documento in entrata da file**.
3. In alternativa, selezionare la riga relativa a una fattura di acquisto a cui si desidera allegare un file e, successivamente, scegliere l'azione **Allega file**.
4. Nella pagina **Inserisci file** selezionare il file che rappresenta il documento in entrata in questione, quindi scegliere il pulsante **Apri**.

## <a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry" />Per creare e connettere un record di documento in entrata da un movimento di contabilità fornitori

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimenti contabili fornitori**, quindi scegli il collegamento correlato.
2. Selezionare una riga relativa a un movimento contabile fornitore a cui si desidera allegare un file e quindi scegliere l'azione **Crea documento in entrata da file**.
3. In alternativa, selezionare la riga relativa a un movimento contabile fornitore a cui si desidera allegare un file e, successivamente, scegliere l'azione **Allega file**.
4. Nella pagina **Inserisci file** selezionare il file che rappresenta il documento in entrata in questione, quindi scegliere il pulsante **Apri**.

## <a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document" />Per rimuovere una connessione dal record di un documento in entrata a un documento registrato

È possibile rimuovere i file allegati da documenti non registrati in qualsiasi momento eliminando il record del documento in entrata correlato. Se il documento è registrato, è innanzitutto necessario rimuovere la connessione dal record del documento in entrata.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Documenti in entrata**, quindi scegli il collegamento correlato.
2. Selezionare la riga per un record in entrata del documento connesso a un documento registrato che si desidera rimuovere quindi selezionare l'azione **Rimuovi riferimento a record**.

La connessione al documento registrato viene rimossa. È ora possibile connettere un altro record di documento in entrata al documento registrato come descritto in questo articolo.

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Creare i record di documenti in entrata](across-how-create-income-document-records.md)
[Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md)
[Trovare documenti registrati senza record di documenti in entrata](across-how-find-posted-documents-without-income-document-records.md)
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
