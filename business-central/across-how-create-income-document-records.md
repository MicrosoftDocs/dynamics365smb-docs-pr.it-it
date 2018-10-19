---
title: Creare i record di documenti in entrata| Documenti Microsoft
description: "È possibile creare i record dei documenti in entrata, ad esempio le fatture elettroniche, e gestire le attività OCR, il commercio elettronico e il servizio di scambio documenti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: de7ad97401529b4dd05bc40daf16df0fe7cd6fb1
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="create-incoming-document-records"></a>Creare i record di documenti in entrata
Nella finestra **Documenti in entrata** è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti.

Per registrare un documento esterno in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario prima creare o completare un record di documento in entrata. Questa operazione può essere eseguita manualmente oppure scattando una foto del documento e quindi creando un record del documento in entrata con il file immagine allegato.

Per poter utilizzare la funzionalità Documenti in entrata, è necessario eseguire l'impostazione necessaria. Per ulteriori informazioni, vedere [Impostare documenti in entrata](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Per approvare o rifiutare un documento in entrata
Se non si desidera consentire agli utenti di creare fatture o righe registrazioni COGE da record di documenti in entrata prima che vengano approvati, è possibile impostare dei responsabili che devono approvare i record prima che possano essere elaborati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Documenti in entrata** e quindi scegliere il collegamento correlato.
2. Selezionare la riga con il documento che si desidera approvare o rifiutare quindi selezionare l'azione **Approva** o **Rifiuta**.

Se si approva il record del documento in entrata, la casella di controllo **Rilasciato** nella riga del documento in entrata è selezionata. L'utente incaricato di creare, ad esempio, le fatture di acquisto può procedere all'elaborazione del record.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Per creare un record di documento in entrata facendo una foto
> [!NOTE]  
>   La seguente procedura si applica solo ai client di [!INCLUDE[d365fin](includes/d365fin_md.md)] per tablet e telefono.

1. Sulla barra delle applicazioni, scegliere il riquadro **Crea documento in entrata da fotocamera** e andare al passaggio 4.
2. In alternativa, nella barra delle applicazioni, fare clic sul pulsante di opzione, selezionare **Documenti in entrata** e scegliere **Tutto**.
3. Nella finestra **Documenti in entrata** scegliere il pulsante con i puntini di sospensione e selezionare **Crea da fotocamera**. La fotocamera del tablet o del telefono è attivata.
4. Scattare la foto di un documento, ad esempio una ricevuta di acquisto, che si desidera elaborare come documento in entrata e fare clic sul pulsante **OK**.

    Viene creato un nuovo record di documento in entrata con l'immagine allegata.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Per allegare un'immagine a un record di documento in entrata facendo una foto
> [!NOTE]  
>   La seguente procedura si applica solo ai client di [!INCLUDE[d365fin](includes/d365fin_md.md)] per tablet e telefono.

1. Nella barra delle applicazioni, fare clic sul pulsante di opzione, selezionare **Documenti in entrata** e scegliere **Tutto**.
2. Aprire la scheda di un record di documento in entrata esistente.
3. Nella finestra **Documento in entrata** scegliere il pulsante con i puntini di sospensione e selezionare **Allega immagine da fotocamera**. La fotocamera del tablet o del telefono è attivata.
4. Scattare la foto di un documento, ad esempio una ricevuta di acquisto, che si desidera elaborare come documento in entrata e fare clic sul pulsante **OK**.

    L'immagine viene allegata al record di documento in entrata.

## <a name="to-create-an-incoming-document-record-manually"></a>Per creare manualmente il record di un documento in entrata
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Documenti in entrata** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Crea da file**.  
3. Nella finestra **Inserisci file** selezionare un file e scegliere **Apri**. Il file viene automaticamente allegato.
4. In alternativa, selezionare l'azione **Nuovo**.
5. Per allegare un file, selezionare l'azione **Allega file**.
6. Nella finestra **Inserisci file** selezionare il file che rappresenta il documento in entrata in questione, quindi scegliere il pulsante **Apri**.
7. Nella finestra **Documento in entrata** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Vedi anche
[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

