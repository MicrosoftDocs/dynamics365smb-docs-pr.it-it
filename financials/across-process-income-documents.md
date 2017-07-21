---
title: Elaborare i documenti in entrata| Documenti Microsoft
description: "Per registrare un documento esterno, ad esempio un PDF, in Dynamics 365 for Financials è necessario prima creare o completare un record di documento in entrata."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b4d344c52bf6f10d00f2157fbdb45903402f6c55
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="processing-incoming-documents"></a>Elaborazione di documenti in entrata
Per registrare un documento esterno in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario prima creare o completare un record di documento in entrata. Questa operazione può essere eseguita manualmente oppure scattando una foto del documento e quindi creando un record del documento in entrata con il file immagine allegato.

Dai PDF o dai file di immagine che si ricevono dai partner commerciali, è possibile impostare che un servizio OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) generi documenti elettronici che si possono convertire in record di documento in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, quando si riceve una fattura nel formato PDF dal fornitore, è possibile inviarla al servizio OCR dalla finestra **Documenti in entrata**. In alternativa, è possibile inviare il file al servizio OCR tramite posta elettronica. Successivamente, quando si riceve il documento elettronico, un record di documento entrata correlato viene creato automaticamente. Dopo alcuni secondi, viene ricevuto il file dal servizio OCR come fattura elettronica che può essere convertita in una fattura di acquisto per il fornitore.

| Per | Vedere |
| --- | --- |
| Creare i record del documento in entrata manualmente o automaticamente scattando una foto di una ricevuta cartacea, ad esempio. |[Procedura: Creare i record di documenti in entrata](across-how-create-income-document-records.md) |
| Utilizzare un servizio di OCR per convertire file PDF e file di immagine in documenti elettronici che possono essere convertiti in fatture di acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio. Istruire il servizio OCR a evitare errori la volta successiva che elabora i dati simili. |[Procedura: Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md) |
| Connettere o rimuovere i record di un documento in entrata per qualsiasi documento di vendita o acquisto non registrato e a qualsiasi cliente, fornitore o movimento di contabilità generale specificato nel documento o movimento. |[Procedura: Creare i record di documenti in entrata direttamente da documenti e movimenti](across-how-connect-disconnect-income-document-records.md) |
| Nelle finestre **Piano dei conti** e **Movimenti C/G** utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati. |[Procedura: Trovare documenti registrati senza record di documenti in entrata](across-how-find-posted-documents-without-income-document-records.md) |
| Per ottenere una panoramica migliore è possibile impostare i record del documento in entrata su Elaborato per rimuoverli dalla visualizzazione predefinita. |[Procedura: Gestire più record di documenti in entrata](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Vedi anche
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

