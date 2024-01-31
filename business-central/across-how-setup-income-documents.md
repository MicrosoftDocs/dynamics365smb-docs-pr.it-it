---
title: Impostare documenti in entrata
description: 'Imposta la funzione Documenti in entrata per creare documenti elettronici, gestire le attività OCR, importare le fatture e convertire i file immagine.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Impostare documenti in entrata

Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella pagina **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.

Se la funzionalità **Documenti in entrata** è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti. Per ulteriori informazioni, vedi [Creare i record di documenti in entrata](across-how-create-income-document-records.md).

## Per impostare la funzione Documenti in entrata

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup documenti in entrata**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Come parte del setup, è necessario decidere se si desidera richiedere l'approvazione dei documenti in arrivo. Per richiedere l'approvazione, è necessario [impostare responsabili approvazione e workflow di approvazione](#to-set-up-approvers-of-incoming-document-records). Se l'organizzazione non intende richiedere l'approvazione, è possibile ignorare la sezione successiva.

Infine, se usi un servizio OCR per convertire file PDF o di immagine che rappresentano documenti in entrata, [è necessario configurarlo](#to-set-up-an-ocr-service). In caso contrario, è possibile ignorare anche quella sezione.

## Per impostare i responsabili dell'approvazione dei record di documenti in entrata

Se non vuoi che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in entrata prima che i documenti siano approvati, imposta un processo di approvazione per i documenti in entrata. I responsabili dell'approvazione dei documenti in ingresso devono essere impostati come utenti del workflow di approvazione.

Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione. Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).

## Per impostare un servizio OCR

Per trasformare file PDF e immagini in documenti elettronici che puoi convertire in fatture, note di credito o righe di giornale di registrazione, imposta la funzione OCR. In alternativa, è possibile creare manualmente voci per rappresentare i documenti esterni.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup servizio OCR**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> I dati di accesso vengono automaticamente crittografati.

Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).  

## Vedere anche

[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
