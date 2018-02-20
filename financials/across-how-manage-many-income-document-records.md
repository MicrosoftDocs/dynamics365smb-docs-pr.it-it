---
title: Definire i documenti in entrata da visualizzare| Documenti Microsoft
description: Modificare la visualizzazione di default dei documenti in entrata, ad esempio le fatture elettroniche, per migliorare la panoramica dei record elaborati e non elaborati.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="manage-many-incoming-document-records"></a>Gestire più record di documenti in entrata
Quando si creano o elaborate i record del documento in entrata, il numero delle righe della finestra **Documenti in entrata** possono aumentare fino a perdere la visibilità di una panoramica. Di conseguenza, è possibile impostare i record del documento in entrata su Elaborato per rimuoverli dalla visualizzazione predefinita. Scegliendo l'azione **Mostra tutto** è possibile visualizzare sia i record elaborati che non elaborati.

> [!NOTE]  
>   Non è possibile modificare le informazioni, allegare i file o eseguire altri processi sui record del documento in entrata che sono impostati su Elaborato. È necessario innanzitutto impostare lo stato Non elaborato.

La casella di controllo **Elaborato** viene selezionata automaticamente sui record del documento in entrata che sono stati elaborati, ma è anche possibile selezionare o deselezionare la casella di controllo manualmente. In base al processo aziendale, un record del documento in entrata può essere elaborato solo quando è stato creato un documento ad esso correlato oppure è stato allegato un file.

> [!NOTE]  
>   Se si apre la finestra **Documenti in entrata** usando l'azione **Documenti in entrata personali** in Gestione ruolo utente, solo i record del documento in entrata non elaborati vengono visualizzati per impostazione predefinita. In questo argomento questa visualizzazione viene indicata come "la visualizzazione predefinita".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Per rimuovere i record del documento in entrata dalla visualizzazione predefinita
1. Nella finestra **Documenti in entrata** selezionare una o più righe dei record del documento in entrata che si desidera rimuovere dalla visualizzazione predefinita.
2. Scegliere l'azione **Imposta su elaborato**.

    I record in entrata del documento vengono eliminate dalla visualizzazione predefinita e viene selezionata la casella di controllo **Elaborato** nelle righe.

> [!NOTE]  
>   È inoltre possibile eseguire questa azione per il singolo record nella finestra **Scheda Documento in entrata**.

## <a name="to-view-all-incoming-document-records"></a>Per visualizzare tutti i record dei documenti in entrata
1. In alternativa, nella finestra **Setup documenti in entrata** scegliere l'azione **Mostra tutto**.

Tutti i record del documento in entrata vengono visualizzati, inclusi quelli in cui non è selezionata la casella di controllo **Elaborato**.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Per aggiungere i record del documento in entrata alla visualizzazione predefinita
1. In alternativa, nella finestra **Setup documenti in entrata** scegliere l'azione **Mostra tutto**.
2. Selezionare una o più righe per i record del documento in entrata che si desidera mostrare nella visualizzazione predefinita.
3. Scegliere l'azione **Imposta su non elaborato**.  

> [!NOTE]  
>   È inoltre possibile eseguire questa azione per il singolo record nella finestra **Scheda Documento in entrata**.

## <a name="see-also"></a>Vedi anche
[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

