---
title: Utilizzare i layout di RDLC
description: Ottieni un'introduzione ai layout di report RDLC.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 12/04/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="working-with-rdlc-layouts"></a>Utilizzare i layout di RDLC

I layout RDLC sono basati sui file di layout di definizione dei report (tipi di file .rdl o .rdlc). I concetti di progettazione per i layout RDLC sono simili ad altri tipi di layout. Il layout determina quali campi mostrare e come sono organizzati. Tuttavia la progettazione dei layout RDLC è un'operazione più avanzata, rispetto ai layout Word ed Excel.

[![Mostra i diversi elementi di un layout RDLC.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools"></a>Strumenti necessari

Per modificare i layout RDL, puoi utilizzare Generatore report di Microsoft SQL Server o Microsoft Visual Studio con l'estensione RDLC Report Designer.

- Generatore report è un'app autonoma installata sul tuo computer da te o da un amministratore. Con Business Central in locale, Generatore report viene installato automaticamente con l'installazione di Business Central Server. Per ulteriori informazioni sull'installazione di Generatore report, vedi [Installare Generatore report](/sql/reporting-services/install-windows/install-report-builder) nella documentazione di SQL Server.

- RDLC Report Designer è un'estensione per Visual Studio 2019 e versioni successive. È possibile scaricare e installare RDLC Report Designer dal [Marketplace Visual Studio](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts"></a>Creare e modificare layout RDLC

La creazione e la modifica dei layout RDLC è un'attività avanzata, che in genere viene eseguita da utenti esperti o sviluppatori. I concetti di base non sono specifici dei layout di report di Business Central. Per questo motivo facciamo riferimento alla seguente documentazione:

- [Creare un report con layout RDL](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

   Questo articolo spiega come creare un layout di report RDLC dal codice AL.

- [Report, parti di report e definizioni di report ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

   Esegue il collegamento alla documentazione di SQL Server Reporting Services per RDL/RDLC. Questo articolo spiega i concetti alla base di RDL/RDLC e come utilizzare Generatore report.

> [!NOTE]
> Generatore report riconosce solo il tipo di file .rdl, non .rdlc. I file di layout esportati da Business Central sono tipi di file .rdlc. Quindi, per modificare questi layout in Generatore report devi rinominare il tipo di file in .rdl.

## <a name="see-also"></a>Vedi anche

[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Impostare il layout utilizzato da un report](ui-set-report-layout.md)  
[Iniziare a creare layout di report](ui-get-started-layouts.md)  
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  
[Business Intelligence](bi.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analisi dei dati del report con Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
