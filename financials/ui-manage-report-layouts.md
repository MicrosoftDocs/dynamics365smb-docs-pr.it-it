---
title: Gestione dei layout dei report | Documenti Microsoft
description: Informazioni sui layout dei report.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e221f5264190a90e04132ed4326afe2cf8364164
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="managing-report-and-document-layouts"></a>Gestione dei layout dei report e dei documenti
Il layout del report controlla il contenuto e il formato del report, compresi quali campi di dati di un set di dati vengono visualizzati nel report e come siano disposti, lo stile del testo, le immagini e altro. Da [!INCLUDE[d365fin](includes/d365fin_md.md)] è possibile cambiare il layout utilizzato in un report, creare un nuovo layout o modificare i layout esistenti.

**Nota**: in [!INCLUDE[d365fin](includes/d365fin_md.md)] il termine "report" riguarda anche i documenti esterni, quali fatture di vendita e conferme di ordini inviate a clienti come file PDF.

In particolare, un layout del report imposta quanto segue:

* I campi etichetta e dati da includere dal set di dati del report [!INCLUDE[d365fin](includes/d365fin_md.md)] report.
* Il formato del testo, ad esempio il tipo di carattere, le dimensioni e il colore.
* Il logo della società e la relativa ubicazione.
* Impostazioni generali della pagina, ad esempio i margini e le immagini di sfondo.

Un report di [!INCLUDE[d365fin](includes/d365fin_md.md)] può essere impostato con diversi layout di report, che è possibile alternare a seconda delle necessità. È possibile utilizzare uno dei layout dei report predefiniti oppure creare i layout dei report personalizzato e assegnarli ai report in base alle esigenze. Per ulteriori informazioni, vedere [Procedura: Creare un layout del documento o del report personalizzato](ui-how-create-custom-report-layout.md).

Esistono due tipi di layout di report che è possibile utilizzare nei report: Word e RDLC.

## <a name="word-report-layout-overview"></a>Panoramica del layout di report di Word
Il layout del report di Word si basa sui documenti di Word (tipo di file .docx). I layout di report di Word consentono di progettare layout utilizzando Microsoft Word 2013 o versioni successive. Un layout di report di Word determina il contenuto del report, controllando la disposizione e l'aspetto degli elementi del contenuto. Un documento di layout del report di Word in genere utilizza tabelle per la disposizione del contenuto, le cui celle possono contenere campi di dati, testo o immagini.

## <a name="rdlc-layout-overview"></a>Panoramica del layout RDLC
I layout di RDLC sono basati sui layout di definizione dei report dei client (tipi di file .rdl o .rdlc). Questi layout vengono creati e modificati utilizzando il Generatore report di SQL Server. Il concetto di progetto per i layout di RDLC è simile ai layout di Word, in cui il layout definisce lo schema generale del report e determina i campi del set di dati da includere. Progettare layout di RDLC è un'operazione più avanzata, rispetto ai layout di Word.

## <a name="built-in-and-custom-report-layouts"></a>Layout di report personalizzati e predefiniti
[!INCLUDE[d365fin](includes/d365fin_md.md)] include diversi layout predefiniti. I layout integrati sono layout predefiniti creati per report specifici. I report in [!INCLUDE[d365fin](includes/d365fin_md.md)] avranno un layout integrato come layout RDLC, layout di Word o in alcuni casi entrambi. Non è possibile modificare un layout di report predefinito da [!INCLUDE[d365fin](includes/d365fin_md.md)], ma è possibile utilizzarlo come base per generare layout di report personalizzati.

I layout personalizzati sono layout del report progettati per modificare l'aspetto di un report. In genere si crea un layout personalizzato in base a un layout predefinito, ma è possibile crearlo da zero o da una copia di un layout personalizzato esistente. I layout personalizzati consentono di avere più layout per lo stesso report con la possibilità di cambiarli in base alle esigenze. Ad esempio, è possibile avere diversi layout per ogni società di [!INCLUDE[d365fin](includes/d365fin_md.md)] oppure è possibile avere diversi layout per la medesima società in alcune occasioni o eventi, come una campagna speciale o il periodo di ferie.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Scelta tra un layout di report RDLC o di Word
Il layout del report può essere basato su un documento Word o su un file RDLC. Decidere se utilizzare un layout dei report di Word o di RDLC dipende dall'aspetto che si desidera per il report generato e dalla conoscenza di Word e Generatore di report di SQL Server.

I concetti di progetto generali dei layout Word e RDLC sono molto simili. Tuttavia ogni tipologia presenta determinate caratteristiche progettuali che influiscono sulla visualizzazione del report generato in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò significa che lo stesso report può apparire diverso quando si utilizza il layout dei report di Word rispetto al layout dei report di RDLC.

Il processo di impostazione dei layout dei report di Word e RDLC nei report è lo stesso. La differenza principale sta nel modo in cui modificano i layout. I layout dei report di Word in genere sono più facili da creare e modificare rispetto ai layout dei report di RDLC perché è possibile utilizzare Word. I layout dei report di RDLC vengono modificati utilizzando il Generatore report di SQL Server, che è indirizzato agli utenti più avanzati.

Per informazioni su come cambiare il layout da utilizzare, vedere [Procedura: Modificare il layout attualmente utilizzato in un report](ui-how-change-layout-currently-used-report.md)

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Procedura: Creare un layout del documento o del report personalizzato](ui-how-create-custom-report-layout.md)  
[Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md)

