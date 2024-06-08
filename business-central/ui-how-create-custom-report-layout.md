---
title: Creare e modificare layout personalizzati per report e documenti
description: 'Informazioni su come creare i layout personalizzati che consentono di modificare l''aspetto del report quando viene visualizzato, stampato o salvato.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Legacy) Creare e modificare layout di report personalizzati

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Per impostazione predefinita, i report hanno un layout integrato. Il layout del report può essere un layout del report RDLC (Report Definition Language lato client), un layout del report Microsoft Word o entrambi. E mentre non puoi modificare i layout integrati, puoi creare layout personalizzati. Un report può avere più layout di report personalizzati.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)], il termine "report" riguarda anche i documenti esterni, quali fatture di vendita e conferme di ordini inviate a clienti come file PDF.

Per creare un layout personalizzato, copia un layout personalizzato esistente o aggiungi un nuovo layout personalizzato. I layout personalizzati sono spesso basati su un layout integrato. Quando aggiungi un nuovo layout personalizzato, puoi scegliere di aggiungere un tipo di layout di report RDLC o Word oppure entrambi. Il nuovo layout personalizzato si baserà sul layout predefinito per il report, se ce n'è uno disponibile. Se non esiste un layout integrato per il tipo di report, viene creato un nuovo layout vuoto. Dovrai modificare e progettare da zero questo layout vuoto. Per ulteriori informazioni sui layout di report RDLC e Word, sui layout personalizzati integrati e altro ancora, vedi [Gestire i layout dei report](ui-manage-report-layouts.md).  

> [!TIP]
> Utilizza i report finanziari per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. Per ulteriori informazioni, vedi [Preparare Financial Reporting con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md).

Dopo aver definito i layout di report personalizzati, è possibile selezionarli nelle pagine Scheda cliente e Scheda fornitore. I layout vengono utilizzati durante la creazione di documenti per il cliente o il fornitore. Per ulteriori informazioni, vedi [Definire layout di documenti per clienti e fornitori](ui-define-customer-vendor-document-layouts.md).

Puoi utilizzare i layout personalizzati anche per aggiungere contenuti ai messaggi di posta elettronica. I layout dei report possono far risparmiare tempo e contribuire a garantire la coerenza riutilizzando lo stesso contenuto quando comunichi con i clienti. Per utilizzare i layout di report personalizzati con e-mail, il tipo di file per il layout deve essere Word, non puoi usare il tipo di file RDLC. Per ulteriori informazioni, vedi [Impostare testi e-mail riutilizzabili e layout](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Creare un layout personalizzato

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Selezione layout report**, quindi scegli il collegamento correlato.

    Nella pagina **Selezione layout report** sono elencati tutti i report disponibili nella società che è specificata nel campo **Nome società** nella parte superiore della pagina.
2. Nel campo **Società** scegli la società per cui vuoi creare il layout di report.
3. Seleziona la riga per il report per il quale vuoi creare il layout, quindi scegli l'azione **Layout personalizzati**.  

   Viene visualizzata la pagina **Layout report personalizzati** nella quale sono elencati tutti i layout personalizzati che sono disponibili per il report selezionato.
4. Per creare una copia di un layout personalizzato esistente, seleziona il layout personalizzato esistente nell'elenco, quindi scegli l'azione **Copia**.  

   La copia del layout personalizzato viene visualizzata nella pagina **Layout report personalizzati** e nel campo *Descrizione* è presente la dicitura **Copia di**.
5. Se vuoi aggiungere un nuovo layout personalizzato basato su un layout predefinito, attieniti alla seguente procedura:  
   1. Scegli l'azione **Nuovo**. La pagina **Inserisci layout integrato per un report** viene visualizzata con i campi **ID** e **Nome** compilati automaticamente.
   2. Attiva l'interruttore **Inserisci layout Word** per aggiungere un tipo di layout di report Word personalizzato OPPURE attiva l'interruttore **Inserisci layout RDLC** per aggiungere un tipo di layout di report RDLC personalizzato.
   4. Scegli il pulsante **OK**.  

    Il nuovo layout personalizzato viene visualizzato nella pagina **Layout report personalizzati**. Se un nuovo layout è basato su un layout predefinito, contiene le parole **Copia di un layout predefinito** nel campo **Descrizione**. Se non è disponibile alcun layout predefinito per il report, il nuovo layout presenta la dicitura **Nuovo layout** nel campo **Descrizione**. Questa dicitura indica che il layout personalizzato è vuoto.
6. Per impostazione predefinita, il campo **Nome società** è vuoto e il layout personalizzato è disponibile per i report in tutte le società. Per rendere il layout personalizzato disponibile solo a una società specifica, scegli **Modifica**, quindi imposta il campo **Nome società** sulla società desiderata.

Il layout personalizzato è stato creato e puoi modificarlo a tuo piacimento.

> [!TIP]
> Puoi esportare i risultati del report in un file Microsoft Excel per visualizzare l'intero set di dati, comprese tutte le colonne, ma senza layout. Il file Excel può aiutarti a verificare che il report restituisca i dati previsti o diagnosticare i problemi. Per informazioni, vedi [Analisi dei dati del report con Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Modifica di un layout personalizzato

Per modificare un layout di report personalizzato, è necessario prima esportare il layout di report come file in un percorso sul computer o sulla rete. Quindi, apri il documento esportato e apporta le modifiche. Quando sono state apportate tutte le modifiche, importa il layout di report.

### <a name="modify-a-custom-layout"></a>Modificare un layout personalizzato

1. Esporta un layout personalizzato dalla pagina **Layout report personalizzati**. Se la pagina non è già aperta, cerca e apri la pagina **Selezione layout report**, seleziona il report che ha il layout da modificare, quindi scegli l'azione **Layout personalizzati**.  
2. Nella pagina **Layout report personalizzati**, seleziona il layout che si desidera modificare, scegli l'azione **Esporta layout** e quindi scegli **Salva** o **Salva con nome** per salvare il documento di layout nel computer o in una rete.  
3. Apri il documento di layout del report che hai salvato e apporta le modifiche.

   Se modifichi un layout Word, apri il documento di layout in Word. Per ulteriori informazioni sulla modifica dei report di Word, vedi [Lavorare con i layout di Word](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   I layout di report RDLC sono più avanzati dei layout di report Word. Per ulteriori informazioni su come modificare un layout di report RDLC, vedi [Progettazione di layout di report RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Ricordarsi di salvare le modifiche effettuate.

4. Torna alla pagina **Layout report personalizzati**, seleziona il layout di report esportato e modificato, quindi scegli l'azione **Importa layout**.  

5. Nella finestra di dialogo **Importa**, seleziona **Scegli** per trovare e selezionare il documento di layout di report modificato, quindi scegli **Apri**.

> [!IMPORTANT]
> Ricordati di importare il documento di layout del report che hai modificato. In caso contrario, il nuovo layout del report non sarà disponibile.

<!--
## <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a>Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

### <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a>Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>To remove a label or data field

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### <a name="adding-data-fields"></a>Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-also"></a>Vedere anche

[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Modificare il layout del report corrente](ui-how-change-layout-currently-used-report.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Utilizzare report, processi batch e XMLport](ui-work-report.md)  
[Preparare Financial Reporting con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
