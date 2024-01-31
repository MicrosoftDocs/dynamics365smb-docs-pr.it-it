---
title: Utilizzare i documenti in entrata
description: 'È possibile gestire i documenti aziendali esterni in entrata, ad esempio le ricevute di pagamento o i PDF, gestire attività OCR e convertire i file in record e documenti in formato elettronico.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Documenti in entrata

I documenti commerciali esterni possono arrivare nella società come allegato a un messaggio e-mail o copia cartacea che è possibile scansionare e trasformare in file. Questo scenario è tipico degli acquisti, dove questi file di documenti in entrata rappresentano le ricevute di pagamento per le spese o i piccoli acquisti.

Nella pagina **Documenti in entrata** è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione. I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti.

## Scenario di utilizzo

Puoi registrare file o copie cartacee ricevute dai tuoi partner commerciali in [!INCLUDE[prod_short](includes/prod_short.md)] e creare un record del documento. Ad esempio, una fattura di acquisto o di vendita, una nota di credito o una riga del giornale di registrazione.

Carica i file ricevuti o usa la fotocamera del dispositivo per scattare una foto e crea voci per rappresentare i documenti esterni. Facoltativamente, con i PDF o i file di immagine puoi impostare un servizio esterno OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) in modo che generi documenti elettronici che possono essere convertiti in record di documenti in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> La funzione OCR è fornita da fornitori esterni. Scegliere un pacchetto di servizi appropriato per l'organizzazione e/o paese/area geografica. Trova i servizi compatibili con [!INCLUDE[prod_short](includes/prod_short.md)] e i dettagli sulle funzionalità disponibili su [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Ad esempio, quando si riceve una fattura nel formato PDF dal fornitore, è possibile inviarla al servizio OCR dalla pagina **Documenti in entrata**. In alternativa, alcuni fornitori di OCR offrono la possibilità di elaborare i file inoltrati a un indirizzo e-mail dedicato, che quindi crea automaticamente un record di documento in entrata correlato. Dopo alcuni secondi, viene ricevuto il file dal servizio OCR come fattura elettronica che può essere convertita in una fattura di acquisto per il fornitore.

> [!TIP]
> Crea record di documenti in entrata in [!INCLUDE[prod_short](includes/prod_short.md)] direttamente dalle e-mail inviate dai fornitori utilizzando il componente aggiuntivo di Outlook. Per ulteriori informazioni, vedi [Utilizzare Business Central come Posta in arrivo aziendale in Outlook](work-outlook-addin.md).

## Funzionalità del documento in entrata

L'elaborazione di documenti in entrata è costituita dalle seguenti operazioni principali:

* Registrare i documenti esterni in [!INCLUDE[prod_short](includes/prod_short.md)] creando le righe nella pagina **Documenti in entrata** attenendosi a uno dei modi seguenti:
  * Manualmente da un PC o un dispositivo mobile, in uno dei seguenti modi:
    * Utilizza il pulsante **Crea da file**, carica un file e compila i campi pertinenti nella pagina **Documento in entrata**.
    * Utilizza il pulsante **Nuovo** e compila i campi pertinenti nella pagina **Documento in entrata** e allega manualmente il relativo file.
    * Da un tablet o un telefono, utilizza il pulsante **Crea da fotocamera** per creare un nuovo record di documento in entrata usando la fotocamera incorporata del dispositivo.
  * Automaticamente, ricevendo il documento dal servizio OCR come documento elettronico dopo aver inviato tramite e-mail il PDF o il file di immagine correlato al servizio OCR. La Scheda dettaglio **Informazioni finanziarie** viene automaticamente compilata nella pagina **Documento in entrata**.
* Utilizza il servizio OCR esterno per convertire PDF o file di immagine in documenti elettronici che possono essere convertiti in record di documento in [!INCLUDE[prod_short](includes/prod_short.md)].
* Creare nuovi documenti o righe registrazione COGE dai record di un documento in entrata immettendo le informazioni mentre vengono lette nei file del documento in entrata.
* Allegare i file di documenti in entrata ai documenti di acquisto e vendita con qualsiasi stato, ad esempio fornitore, cliente e movimenti di contabilità generale derivanti dalla registrazione.
* Visualizzare i record di documenti in entrata e i relativi allegati in qualsiasi documento o movimento di acquisto e vendita oppure individuare tutti i movimenti di contabilità generale senza i record di documenti in entrata nella pagina **Piano dei conti**.

> [!NOTE]
> I file allegati a schede e documenti nella scheda **Allegati** non sono inclusi nella pagina **Documenti in entrata**. Per ulteriori informazioni, vedere [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md).

| A | Vedere |
| --- | --- |
| Imposta la funzionalità **Documenti in entrata** e imposta il servizio OCR. |[Impostare documenti in entrata](across-how-setup-income-documents.md) |
| Creare i record del documento in entrata manualmente o automaticamente scattando una foto di una ricevuta cartacea, ad esempio. |[Creare i record di documenti in entrata](across-how-create-income-document-records.md) |
| Utilizzare un servizio di OCR per convertire file PDF e file di immagine in documenti elettronici che possono essere convertiti in fatture di acquisto in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio. Istruire il servizio OCR a evitare errori la volta successiva che elabora i dati simili. |[Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md) |
| Connettere o rimuovere i record di un documento in entrata per qualsiasi documento di vendita o acquisto non registrato e a qualsiasi cliente, fornitore o movimento di contabilità generale specificato nel documento o movimento. |[Creare i record di documenti in entrata direttamente da documenti e movimenti](across-how-connect-disconnect-income-document-records.md) |
| Nelle pagine **Piano dei conti** e **Movimenti C/G** utilizza una funzione di ricerca per trovare movimenti di contabilità generale per documenti registrati che non hanno record di documenti in entrata e successivamente collegali centralmente a record esistenti o creane di nuovi con file di documento allegati. |[Trovare documenti registrati senza record di documenti in entrata](across-how-find-posted-documents-without-income-document-records.md) |
| Per ottenere una panoramica migliore è possibile impostare i record del documento in entrata su *Elaborato* e rimuoverli dalla visualizzazione predefinita. |[Gestire più record di documenti in entrata](across-how-manage-many-income-document-records.md) |

## Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Modifica di documenti registrati](across-edit-posted-document.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Business Central e OneDrive per l'integrazione del business](across-onedrive-overview.md)  
[Utilizzare Business Central come Posta in arrivo aziendale di Outlook](work-outlook-addin.md)  
[Inviare documenti ed e-mail](ui-how-send-documents-email.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
