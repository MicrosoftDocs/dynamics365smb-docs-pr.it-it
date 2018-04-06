---
title: Impostare documenti in entrata| Documenti Microsoft
description: "Utilizzare la funzione Documenti in entrata per creare documenti elettronici, gestire le attività OCR, importare le fatture e convertire i file immagine."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6381fc0949c3f6789a6b3387d119051403bcbb4a
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-incoming-documents"></a>Impostare documenti in entrata
Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella finestra **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.

Se non si desidera che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in entrata prima che i documenti siano approvati, è necessario impostare i responsabili dell'approvazione nella finestra **Responsabili approvazione documenti in entrata**.

Per trasformare file PDF e file di immagine in documenti elettronici convertibili, ad esempio, in fatture di acquisto [!INCLUDE[d365fin](includes/d365fin_md.md)]', è necessario innanzitutto impostare la funzionalità OCR e abilitare il servizio.

Se la funzionalità Documenti in entrata è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti. Per ulteriori informazioni, vedere [Elaborazione di documenti in entrata](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Per impostare la funzione Documenti in entrata
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup documenti in entrata**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Per impostare i responsabili dell'approvazione dei record di documenti in entrata
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup documenti in entrata**, quindi scegliere il collegamento correlato.  
2. In alternativa, nella finestra **Setup documenti in entrata** scegliere l'azione **Responsabili approvazione**.

    Nella finestra **Responsabili approvazione documenti in entrata** vengono elencati tutti gli utenti impostati in [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Selezionare uno o più utenti che possono approvare un documento in entrata prima che possa essere creato un documento o una riga registrazioni correlata.

Se vengono impostati i responsabili dell'approvazione nella finestra **Responsabile approvazione documento in entrata** solo questi utenti possono approvare un documento in entrata se la casella di controllo **Richiedi approvazione per creare** nella finestra **Setup documenti in entrata** è selezionata.

> [!NOTE]  
>   Questa impostazione di approvazione non è correlata ai workflow di approvazione. Per ulteriori informazioni, vedere [Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Per impostare un servizio OCR
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup servizio OCR**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>Per crittografare le informazioni di accesso
Si consiglia di proteggere le informazioni di accesso immesse nella finestra **Setup servizio OCR**. È possibile crittografare dati nel server generando nuove chiavi di crittografia o importando quelle esistenti che vengono abilitate nell'istanza del server che collega al database.

1. Nella finestra **Setup servizio OCR** scegliere l'azione **Gestione crittografia**.
2. Nella finestra **Gestione crittografia dati** abilitare la crittografia dei dati.

## <a name="see-also"></a>Vedi anche
[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

