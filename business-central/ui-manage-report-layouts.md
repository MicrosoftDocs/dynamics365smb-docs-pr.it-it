---
title: Gestione dei layout di report e documento
description: 'Utilizzare i layout di report per personalizzare i documenti, ad esempio, per personalizzare il carattere, il logo o le impostazioni della pagina di file PDF da inviare ai clienti.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650, 9660'
ms.date: 05/23/2023
ms.author: jswymer
---
# Panoramica dei layout di report e documento

Un layout di report controlla il contenuto e il formato del report, compresi quali campi di dati di un set di dati vengono visualizzati nel report e come siano disposti, lo stile del testo, le immagini e altro. Da [!INCLUDE[prod_short](includes/prod_short.md)] è possibile cambiare il layout utilizzato in un report, creare un nuovo layout o modificare i layout esistenti.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)], il termine "report" riguarda anche i documenti esterni, quali fatture di vendita e conferme di ordini inviate a clienti come file PDF.

Puoi utilizzare i layout anche per aggiungere contenuti ai messaggi di posta elettronica. Ad esempio, i layout dei report possono far risparmiare tempo e contribuire a garantire la coerenza riutilizzando lo stesso contenuto quando comunichi con i clienti. Per utilizzare i layout di report personalizzati con e-mail, il tipo di file per il layout deve essere Word. Non è possibile utilizzare il tipo di file RDLC. Per ulteriori informazioni, vedi [Impostare testi e layout e-mail riutilizzabili](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Introduzione

In particolare, un layout di report imposta quanto segue:

* I campi etichetta e dati da includere dal set di dati del report [!INCLUDE[prod_short](includes/prod_short.md)] report.
* Il formato del testo, ad esempio il tipo di carattere, le dimensioni e il colore.
* Il logo della società e la relativa ubicazione.
* Impostazioni generali della pagina, ad esempio i margini e le immagini di sfondo.

Un report può essere impostato con diversi layout di report, che è possibile alternare a seconda delle necessità. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Ci sono due aspetti importanti dei layout di report che influenzeranno il modo in cui li utilizzi: il *tipo di layout* e l'*origine del layout*. Il tipo di layout indica la tipologia di file su cui si basa il layout. L'origine del layout specifica l'origine del layout.

## Tipi di layout

Esistono quattro tipi di layout che è possibile utilizzare nei report: Word, RDLC, Excel ed esterno.

### Word

I layout di Word si basano sui documenti di Word (tipo di file .docx). I layout di Word consentono di progettare layout utilizzando Microsoft Word. Un layout di Word determina il contenuto del report, controllando la disposizione e l'aspetto degli elementi del contenuto. Un documento di layout di Word in genere utilizza tabelle per la disposizione del contenuto, le cui celle possono contenere campi di dati, testo o immagini.

[![Esempio di un documento di layout di report Word per Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Per ulteriori informazioni, vedi [Utilizzare i layout di Word](ui-how-add-fields-word-report-layout.md).

### Excel

I layout di Excel si basano sulle cartelle di lavoro Microsoft Excel (tipo di file .xlsx). Consentono di creare report utilizzando le familiari funzionalità di Excel per il riepilogo, l'analisi e la presentazione dei dati con strumenti come formule, tabelle pivot, grafici pivot e altro

[![Mostra un esempio di layout di Excel.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Per ulteriori informazioni, vedi [Utilizzare i layout di Excel](ui-excel-report-layouts.md).

### RDLC

I layout RDLC sono basati sui file di layout di definizione dei report dei client (tipi di file .rdl o .rdlc). Questi layout vengono creati e modificati utilizzando il Generatore report di SQL Server o Microsoft RDLC Report Designer. Il concetto di progettazione per i layout RDLC è simile ai layout di Word, in cui il layout determina quali campi mostrare e come sono disposti. Tuttavia la progettazione dei layout RDLC è un'operazione più avanzata, rispetto ai layout Word.

[![Mostra un esempio di layout di RDLC.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Per ulteriori informazioni, vedi [Utilizzare i layout RDLC](ui-rdlc-report-layouts.md).

### Esterno

Un tipo di layout esterno si riferisce a un tipo avanzato appositamente progettato per report specifici. I report e i layout stessi sono in genere forniti dai partner, non da Microsoft. Il tipo di file effettivo del layout varia a seconda del provider.

Per ulteriori informazioni, vedi [Sviluppo di un rendering di report personalizzato](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## Origini del layout

Oltre al tipo, i layout sono ulteriormente suddivisi in tre categorie, in base alla loro origine o fonte.

* Layout di estensione

   I layout di estensione sono layout che fanno parte di un'estensione che è stata installata nell'ambiente. Questi layout sono in genere layout standard forniti da Microsoft, ad esempio, nell'applicazione di base. Oppure possono essere layout inclusi nelle estensioni di altri fornitori di software. È possibile riconoscere i layout di estensione nella pagina **Layout report** perché il nome dell'estensione e l'editore sono mostrati nella colonna **Estensione**.

* Layout definiti dall'utente

   L'altra origine di layout è l'utente finale. Da Business Central, un utente con le autorizzazioni appropriate può aggiungere nuovi layout in vari modi. Ad esempio, puoi iniziare da un layout di estensione esistente o da un altro layout definito dall'utente. Nella pagina **Layout report**, il layout definito dall'utente avrà la colonna **Estensione** vuota.

   Per ulteriori informazioni, vedi [Iniziare a creare layout di report](ui-get-started-layouts.md).

* Layout personalizzati

  I layout personalizzati sono anche layout creati dagli utenti. La differenza è che questi layout sono creati dalla pagina legacy **Layout report personalizzati** e possono essere solo di tipo Word e RDLC. Sebbene sia ancora possibile creare layout personalizzati, vengono gradualmente eliminati a favore dei layout definiti dall'utente.

  Per ulteriori informazioni, vedi [(Legacy) Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

Per informazioni che ti aiuteranno a decidere qual è il tipo megliore per te, vedi [Decidere quale tipo di layout usare](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Una cosa importante da ricordare è che non è possibile modificare i layout di estensione dal client Business Central. Ad esempio, non è consentito modificare il nome o il tipo di layout, né caricarlo e sostituirlo con un'altra versione. Se tenti, viene visualizzato un messaggio di errore. Dovrai invece creare un layout personalizzato o definito dall'utente in base al layout di estensione.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## Vedi il relativo [training Microsoft](/training/modules/change-documents-dynamics-365-business-central/index)

## Vedi anche

[Aggiornare layout report personalizzati](ui-update-report-layouts.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Definire layout di documenti speciali per clienti e fornitori](ui-define-customer-vendor-document-layouts.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzare report, processi batch e XMLport](ui-work-report.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
