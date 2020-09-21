---
title: Impostare documenti in entrata| Documenti Microsoft
description: Utilizzare la funzione Documenti in entrata per creare documenti elettronici, gestire le attività OCR, importare le fatture e convertire i file immagine.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 08/10/2020
ms.author: edupont
ms.openlocfilehash: 1b0942c53f435a79cae733fe4d7287e628cf7478
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780512"
---
# <a name="set-up-incoming-documents"></a>Impostare documenti in entrata

Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella pagina **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.

Se non si desidera che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in arrivo prima che i documenti siano approvati, è necessario impostare i responsabili dell'approvazione.

Per trasformare file PDF e file di immagine in documenti elettronici convertibili, ad esempio, in fatture di acquisto [!INCLUDE[d365fin](includes/d365fin_md.md)]', è necessario innanzitutto impostare la funzionalità OCR e abilitare il servizio. Scegliere un pacchetto di servizi appropriato per l'organizzazione e/o paese/area geografica. In alternativa, è possibile creare manualmente voci per rappresentare i documenti esterni.  

Se la funzionalità Documenti in entrata è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti. Per ulteriori informazioni, vedere [Elaborazione di documenti in entrata](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Per impostare la funzione Documenti in entrata

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup documenti in entrata** e quindi scegliere il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Come parte del setup, è necessario decidere se si desidera richiedere l'approvazione dei documenti in arrivo. Per richiedere l'approvazione, è necessario impostare responsabili approvazione e workflow di approvazione. Se l'organizzazione non intende richiedere l'approvazione, è possibile ignorare la sezione successiva.  

Infine, se si utilizza un servizio per convertire file PDF o di immagine che rappresentano documenti in arrivo, è necessario configurarlo. In caso contrario, è possibile ignorare anche quella sezione.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Per impostare i responsabili dell'approvazione dei record di documenti in entrata

Facoltativamente, impostare un processo di approvazione per i documenti in arrivo. I responsabili dell'approvazione dei documenti in ingresso devono essere impostati come utenti del workflow di approvazione.

Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione. Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Per impostare un servizio OCR

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup servizio OCR** e quindi scegliere il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> I dati di accesso vengono automaticamente crittografati.

Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Vedere anche

[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
