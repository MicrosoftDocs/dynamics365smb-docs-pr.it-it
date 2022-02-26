---
title: Impostare documenti in entrata| Documenti Microsoft
description: Utilizzare la funzione Documenti in entrata per creare documenti elettronici, gestire le attività OCR, importare le fatture e convertire i file immagine.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 313de95353fc42b222fa95cd36d320881a7fbdb8
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442587"
---
# <a name="set-up-incoming-documents"></a>Impostare documenti in entrata

Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella pagina **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.

Se non si desidera che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in arrivo prima che i documenti siano approvati, è necessario impostare i responsabili dell'approvazione.

Per trasformare file PDF e file di immagine in documenti elettronici convertibili, ad esempio, in fatture di acquisto [!INCLUDE[prod_short](includes/prod_short.md)]', è necessario innanzitutto impostare la funzionalità OCR e abilitare il servizio. Scegliere un pacchetto di servizi appropriato per l'organizzazione e/o paese/area geografica. In alternativa, è possibile creare manualmente voci per rappresentare i documenti esterni.  

Se la funzionalità Documenti in entrata è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti. Per ulteriori informazioni, vedere [Elaborazione di documenti in entrata](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Per impostare la funzione Documenti in entrata

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup documenti in entrata**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Come parte del setup, è necessario decidere se si desidera richiedere l'approvazione dei documenti in arrivo. Per richiedere l'approvazione, è necessario impostare responsabili approvazione e workflow di approvazione. Se l'organizzazione non intende richiedere l'approvazione, è possibile ignorare la sezione successiva.  

Infine, se si utilizza un servizio per convertire file PDF o di immagine che rappresentano documenti in arrivo, è necessario configurarlo. In caso contrario, è possibile ignorare anche quella sezione.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Per impostare i responsabili dell'approvazione dei record di documenti in entrata

Facoltativamente, impostare un processo di approvazione per i documenti in arrivo. I responsabili dell'approvazione dei documenti in ingresso devono essere impostati come utenti del workflow di approvazione.

Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione. Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Per impostare un servizio OCR

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup servizio OCR**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> I dati di accesso vengono automaticamente crittografati.

Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Vedere anche

[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]