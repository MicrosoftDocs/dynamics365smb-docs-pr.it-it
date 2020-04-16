---
title: Layout predefiniti e personalizzati per report e documenti | Documenti Microsoft
description: Utilizzare i layout di report per personalizzare i documenti, ad esempio, per personalizzare il carattere, il logo o le impostazioni della pagina di file PDF da inviare ai clienti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 419c6d48d7370f7bcd6dc21c21ed3bd8d3833b00
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195465"
---
# <a name="managing-report-and-document-layouts"></a>Gestione dei layout di report e documento
Un layout di report controlla il contenuto e il formato del report, compresi quali campi di dati di un set di dati vengono visualizzati nel report e come siano disposti, lo stile del testo, le immagini e altro. Da [!INCLUDE[d365fin](includes/d365fin_md.md)] è possibile cambiare il layout utilizzato in un report, creare un nuovo layout o modificare i layout esistenti.

> [!NOTE]  
>   In [!INCLUDE[d365fin](includes/d365fin_md.md)], il termine "report" riguarda anche i documenti esterni, quali fatture di vendita e conferme di ordini inviate a clienti come file PDF.

In particolare, un layout di report imposta quanto segue:

* I campi etichetta e dati da includere dal set di dati del report [!INCLUDE[d365fin](includes/d365fin_md.md)] report.
* Il formato del testo, ad esempio il tipo di carattere, le dimensioni e il colore.
* Il logo della società e la relativa ubicazione.
* Impostazioni generali della pagina, ad esempio i margini e le immagini di sfondo.

Un report può essere impostato con diversi layout di report, che è possibile alternare a seconda delle necessità. È possibile utilizzare uno dei layout di report predefiniti oppure creare layout di report personalizzati e assegnarli ai report in base alle esigenze. Per ulteriori informazioni, vedere [Creare un layout di documento o report personalizzato](ui-how-create-custom-report-layout.md).

Esistono due tipi di layout di report che è possibile utilizzare nei report: Word e RDLC.

## <a name="word-report-layout-overview"></a>Panoramica del layout di report Word
Un layout di report Word si basa sui documenti di Word (tipo di file .docx). I layout di report Word consentono di progettare layout utilizzando Microsoft Word 2013 o versioni successive. Un layout di report Word determina il contenuto del report, controllando la disposizione e l'aspetto degli elementi del contenuto. Un documento di layout di report Word in genere utilizza tabelle per la disposizione del contenuto, le cui celle possono contenere campi di dati, testo o immagini.

 ![Esempio di un documento di layout di report Word per NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Panoramica del layout RDLC
I layout RDLC sono basati sui layout di definizione dei report dei client (tipi di file .rdl o .rdlc). Questi layout vengono creati e modificati utilizzando il Generatore report di SQL Server. Il concetto di progetto per i layout RDLC è simile ai layout Word, in cui il layout definisce lo schema generale del report e determina i campi del set di dati da includere. Progettare layout RDLC è un'operazione più avanzata, rispetto ai layout Word. Per ulteriori informazioni, vedere [Progettazione di layout di report RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Layout di report personalizzati e predefiniti
[!INCLUDE[d365fin](includes/d365fin_md.md)] include diversi layout predefiniti. I layout integrati sono layout predefiniti creati per report specifici. I report in [!INCLUDE[d365fin](includes/d365fin_md.md)] avranno un layout integrato come layout report RDLC, layout report Word o in alcuni casi entrambi. Non è possibile modificare un layout di report predefinito da [!INCLUDE[d365fin](includes/d365fin_md.md)], ma è possibile utilizzarlo come base per generare layout di report personalizzati.

I layout personalizzati sono layout di report progettati per modificare l'aspetto di un report. In genere si crea un layout personalizzato in base a un layout predefinito, ma è possibile crearlo da zero o da una copia di un layout personalizzato esistente. I layout personalizzati consentono di avere più layout per lo stesso report con la possibilità di cambiarli in base alle esigenze. Ad esempio, è possibile avere diversi layout per ogni società di [!INCLUDE[d365fin](includes/d365fin_md.md)] oppure è possibile avere diversi layout per la medesima società in alcune occasioni o eventi, come una campagna speciale o il periodo di ferie.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Scelta tra un layout di report RDLC o Word
Un layout di report può essere basato su un documento Word o su un file RDLC. Decidere se utilizzare un layout di report Word o RDLC dipende dall'aspetto che si desidera per il report generato e dalla conoscenza di Word e Generatore di report di SQL Server.

I concetti di progetto generali dei layout Word e RDLC sono molto simili. Tuttavia ogni tipologia presenta determinate caratteristiche progettuali che influiscono sulla visualizzazione del report generato in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò significa che lo stesso report può apparire diverso quando si utilizza il layout di report Word rispetto al layout di report RDLC.

Il processo di impostazione dei layout di report Word e RDLC nei report è lo stesso. La differenza principale sta nel modo in cui modificano i layout. I layout di report Word in genere sono più facili da creare e modificare rispetto ai layout di report RDLC perché è possibile utilizzare Word. I layout di report RDLC vengono modificati utilizzando il Generatore report di SQL Server, che è indirizzato agli utenti più avanzati.

Per informazioni su come cambiare il layout da utilizzare, vedere [Modificare il layout del report corrente](ui-how-change-layout-currently-used-report.md).

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Aggiornare layout report personalizzati](ui-update-report-layouts.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Definire layout di documenti speciali per clienti e fornitori](ui-define-customer-vendor-document-layouts.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
