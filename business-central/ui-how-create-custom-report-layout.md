---
title: Creare e modificare layout personalizzati per report e documenti
description: Informazioni su come creare i layout personalizzati che consentono di modificare l'aspetto del report quando viene visualizzato, stampato o salvato.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d629b2639325b95ab90db8aaf8ac9a3e5d51fc33
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511443"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Legacy) Creare e modificare layout di report personalizzati

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Per impostazione predefinita, un report avrà un layout di report RDLC o Word predefinito o entrambi. Non è possibile modificare i layout predefiniti. Tuttavia puoi creare i propri layout personalizzati che consentono di modificare l'aspetto del report quando è visualizzato, stampato o salvato. È possibile creare più layout di report personalizzati per lo stesso report e alternare il layout utilizzato in un report in base alle esigenze.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)], il termine "report" riguarda anche i documenti esterni, quali fatture di vendita e conferme di ordini inviate a clienti come file PDF.

Per creare un layout personalizzato, puoi effettuare una copia di un layout personalizzato esistente o aggiungere un nuovo layout personalizzato, che nella maggior parte dei casi è basato su un layout predefinito. Quando si aggiunge un nuovo layout personalizzato, è possibile scegliere di aggiungere un tipo di layout di report RDLC o Word oppure entrambi. Il nuovo layout personalizzato si baserà automaticamente sul layout predefinito per il report, se ce n'è uno disponibile. Se non esiste un layout integrato per il tipo, viene creato un nuovo layout vuoto. Dovrai modificare e progettare da zero questo layout vuoto. Per ulteriori informazioni sui layout di report RDLC e Word, sui layout personalizzati integrati e altro ancora, vedere [Gestire i layout dei report](ui-manage-report-layouts.md).  

> [!TIP]
> Utilizzare le situazioni contabili per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. Per ulteriori informazioni, vedere [Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti](bi-how-work-account-schedule.md).

Quando vengono definiti layout di report personalizzati, puoi selezionarli da schede cliente e fornitore per specificare che i layout selezionati verranno utilizzati per documenti creati per il cliente o il fornitore in questione. Per ulteriori informazioni, vedere [Definire layout di documenti per clienti e fornitori](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>Per creare un layout personalizzato

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Selezione layout report**, quindi scegli il collegamento correlato.

    Nella pagina **Selezione layout report** sono elencati tutti i report disponibili nella società che è specificata nel campo **Nome società** nella parte superiore della pagina.
2. Impostare il campo **Società** alla società per la quale si desidera creare il layout di report.
3. Selezionare la riga per il report per il quale si desidera creare il layout, quindi scegliere l'azione **Layout personalizzati**.  

   Viene visualizzata la pagina **Layout report personalizzati** nella quale sono elencati tutti i layout personalizzati che sono disponibili per il report selezionato.
4. Per creare una copia di un layout personalizzato esistente, selezionare il layout personalizzato esistente nell'elenco, quindi scegliere l'azione **Copia**.  

   La copia del layout personalizzato viene visualizzata nella pagina **Layout report personalizzati** e nel campo *Descrizione* è presente la dicitura **Copia di**.
5. Se vuoi aggiungere un nuovo layout personalizzato basato su un layout predefinito, segui la seguente procedura:  
   1. Scegliere l'azione **Nuovo**. Viene visualizzata la pagina **Inserisci layout predefinito per un report**. I campi **ID** e **Nome** vengono automaticamente compilati.
   2. Per aggiungere un tipo di layout di report Word personalizzato, selezionare la casella di controllo **Inserisci layout Word**.
   3. Per aggiungere un tipo di layout di report RDLC personalizzato, selezionare la casella di controllo **Inserisci layout RDLC**.
   4. Scegli il pulsante **OK**.  

    Il nuovo layout personalizzato viene visualizzato nella pagina **Layout report personalizzati**. Se un nuovo layout è basato su un layout predefinito, contiene le parole **Copia di un layout predefinito** nel campo **Descrizione**. Se non è disponibile alcun layout predefinito per il report, il nuovo layout presenta la dicitura **Nuovo layout** nel campo **Descrizione**. Questa dicitura indica che il layout personalizzato è vuoto.
6. Per impostazione predefinita, il campo **Nome società** è vuoto, il che significa che il layout personalizzato sarà disponibile per il report in tutte le società. Per rendere il layout personalizzato disponibile solo a una società specifica, scegliere **Modifica**, quindi impostare il campo **Nome società** sulla società desiderata.

Il layout personalizzato è stato creato. È ora possibile modificare il layout personalizzato in base alle esigenze.

> [!TIP]
> Puoi esportare i risultati del report in un file Excel per visualizzare l'intero set di dati, comprese tutte le colonne, ma senza layout. Il file Excel può aiutarti a verificare che il report restituisca i dati previsti o diagnosticare i problemi. Per ulteriori informazioni vedi [Analisi dei dati del report con Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Modifica di un layout personalizzato

Per modificare un layout di report, è necessario prima esportare il layout di report come file in un percorso sul computer o sulla rete. Quindi, apri il documento esportato e apporta le modifiche. Quando sono state apportate tutte le modifiche, importa il layout di report.

### <a name="to-modify-a-custom-layout"></a>Per modificare un layout personalizzato

1. Esportare un layout personalizzato dalla pagina **Layout report personalizzati**. Se questa pagina non è già aperta, cerca e apri la pagina **Selezione layout report**, seleziona il report che ha il layout da modificare, quindi scegli l'azione **Layout personalizzati**.  
2. Nella pagina **Layout report personalizzati**, selezionare il layout che si desidera modificare, scegliere l'azione **Esporta layout** e quindi scegliere **Salva** o **Salva con nome** per salvare il documento di layout nel computer o in una rete.  
3. Apri il documento di layout del report che hai salvato, quindi apporta le modifiche.

   Se modifichi un layout Word, apri il documento di layout in Word. Per i dettagli sulla modifica, vedi [Utilizzare i layout di Word](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   I layout di report RDLC sono più avanzati dei layout di report Word. Per ulteriori informazioni su come modificare un layout di report RDLC, vedere [Progettazione di layout di report RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Ricordarsi di salvare le modifiche effettuate.

4. Tornare alla pagina **Layout report personalizzati**, selezionare il layout di report esportato e modificato, quindi scegliere l'azione **Importa layout**.  

5. Nella finestra di dialogo **Importa**, seleziona **Scegli** per trovare e selezionare il documento di layout di report modificato, quindi scegli **Apri**.

> [!IMPORTANT]
> Ricordati di importare il documento di layout del report che hai modificato. In caso contrario, il nuovo layout del report non sarà disponibile.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Modificare il layout del report corrente](ui-how-change-layout-currently-used-report.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Utilizzare report, processi batch e XMLport](ui-work-report.md)  
[Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]