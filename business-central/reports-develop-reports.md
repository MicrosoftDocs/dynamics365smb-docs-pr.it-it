---
title: Sviluppo di layout di report e set di dati
description: Fornisce una panoramica dei dati di Business Central.
author: kennieNP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
---

# <a name="developing-business-central-report-layouts-and-datasets"></a><a name="developing-business-central-report-layouts-and-datasets"></a>Sviluppo di layout di report e set di dati di Business Central

Un report in [!INCLUDE[prod_short](includes/prod_short.md)] consiste in un oggetto report che definisce il _set di dati_ del report (quali dati sono disponibili) e un certo numero di _layout di report_ (come vengono presentati i dati).  

## <a name="developing-report-layouts"></a><a name="developing-report-layouts"></a>Sviluppo dei layout di report

Vuoi modificare i layout dei report esistenti forniti in [!INCLUDE[prod_short](includes/prod_short.md)]? A seconda della tecnologia utilizzata per il layout, questo è qualcosa che potresti essere in grado di fare da solo (layout Excel e forse anche Word), o forse hai bisogno di uno sviluppatore per farlo (layout RDLC pixel-perfetti).

| A | Vedere |
|--|--|
| Ulteriori informazioni sui diversi tipi di layout (Word, Excel e RDLC) | [Tipi di layout (Word, Excel e RDLC)](ui-manage-report-layouts.md) |
| Scopri come creare un nuovo layout di report. | [Creare un nuovo layout](ui-how-create-custom-report-layout.md) |
| Scopri quali caratteri sono installati in [!INCLUDE[prod_short](includes/prod_short.md)] online in modo che possano essere utilizzati nei layout dei report. | [Utilizzo dei caratteri nei layout](ui-fonts.md) |
| Per informazioni su come lavorare con i layout di Word. | [Utilizzare i layout di Word](ui-how-add-fields-word-report-layout.md) |
| Per informazioni su come importare/esportare i file di layout. | [Importare/Esportare un layout](ui-how-import-and-export-report-layout.md) |
| Per informazioni su come aggiornare una definizione di layout in [!INCLUDE[prod_short](includes/prod_short.md)] con un nuovo file di layout. | [Importare/Esportare un layout](ui-how-import-and-export-report-layout.md) |
| Per informazioni su come modificare il layout predefinito per un report. | [Modificare il layout predefinito](ui-how-change-layout-currently-used-report.md) |
<!-- | Per informazioni su come lavorare con i layout di Excel. | [Utilizzare i layout di Excel](ui-how-add-fields-word-report-layout.md) | -->

## <a name="developing-report-datasets"></a><a name="developing-report-datasets"></a>Sviluppo dei set di dati di report

 Per modificare le definizioni del set di dati che stabiliscono quali dati sono disponibili nel report, è necessario uno sviluppatore che conosca il linguaggio di programmazione AL e gli strumenti per sviluppare oggetti di report ed estensioni di report.

| A | Vedere |
|--|--|
| Informazioni su come programmare i report in AL | [Guida allo sviluppo del report](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Informazioni su come eseguire i report | [Guida all'ottimizzazione delle prestazioni del report](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Panoramica di Business Intelligence e creazione di report](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
