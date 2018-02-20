---
title: Utilizzare i documenti in entrata| Documenti Microsoft
description: "È possibile gestire i documenti aziendali esterni in entrata, ad esempio le ricevute di pagamento o i PDF, gestire attività OCR e convertire i file in record e documenti in formato elettronico in Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d38f1ed77ac3fac7c9283af6ea0f92479adbf89f
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="incoming-documents"></a>Documenti in entrata
Alcune transazioni commerciali non vengono registrate in [!INCLUDE[d365fin](includes/d365fin_md.md)] dall'inizio. Invece, un documento commerciale esterno arriva nella propria società come allegato a un messaggio e-mail o copia cartacea che è possibile scansionare e trasformare in file. Ciò è tipico degli acquisti, dove questi file di documenti in entrata rappresentano le ricevute di pagamento per le spese o i piccoli acquisti.

Dai PDF o dai file di immagine dei documenti in entrata è possibile impostare un servizio esterno OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) in modo che generi documenti elettronici che possono essere convertiti in record di documenti in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Nella finestra **Documenti in entrata** è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti.

L'elaborazione di documenti in entrata è costituita dalle seguenti operazioni principali:

* Registrare i documenti esterni in [!INCLUDE[d365fin](includes/d365fin_md.md)] creando le righe nella finestra **Documenti in entrata** attenendosi a uno dei modi seguenti:
  * Manualmente, utilizzando le funzioni semplici da un PC o un dispositivo mobile, in uno dei seguenti modi:
    * Utilizzare il pulsante **Crea da file** e compilare i campi pertinenti nella finestra **Documento in entrata**. Il file viene automaticamente allegato.  
    * Utilizzare il pulsante **Nuovo** e compilare i campi pertinenti nella finestra **Documento in entrata** e allegare manualmente il relativo file.
    * Da un tablet o un telefono, utilizzare il pulsante **Crea da fotocamera** per creare un nuovo record di documento in entrata e quindi inviare l'immagine, ad esempio al servizio OCR.
  * Automaticamente, ricevendo il documento dal servizio OCR come documento elettronico dopo aver inviato tramite e-mail il PDF o il file di immagine correlato al servizio OCR. La Scheda dettaglio **Informazioni finanziarie** viene automaticamente compilata nella finestra **Documento in entrata**.
* Utilizzare il servizio OCR per convertire PDF o file di immagine in documenti elettronici che possono essere convertiti in record di documento in [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Creare nuovi documenti o righe registrazione COGE dai record di un documento in entrata immettendo le informazioni mentre vengono lette nei file del documento in entrata.
* Allegare i file di documenti in entrata ai documenti di acquisto e vendita con qualsiasi stato, ad esempio fornitore, cliente e movimenti di contabilità generale derivanti dalla registrazione.
* Visualizzare i record di documenti in entrata e i relativi allegati in qualsiasi documento o movimento di acquisto e vendita oppure individuare tutti i movimenti di contabilità generale senza i record di documenti in entrata nella finestra **Piano dei conti**.

| Per | Vedere |
| --- | --- |
| Impostare la funzionalità Documenti in entrata e impostare il servizio OCR. |[Impostare documenti in entrata](across-how-setup-income-documents.md) |
| Creare i record dei documenti in entrata, allegare i file, utilizzare OCR per convertire i file PDF in documenti elettronici, convertire documenti elettronici in record di documento, controllare i documenti di vendita e di acquisto registrati dei record di documenti in entrata. |[Elaborazione di documenti in entrata](across-process-income-documents.md) |

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

