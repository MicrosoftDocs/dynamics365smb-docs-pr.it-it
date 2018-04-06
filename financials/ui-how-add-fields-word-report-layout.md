---
title: Come aggiungere campi a un layout di report Word | Microsoft Docs
description: Descrive come aggiungere campi di un set di dati del report a un layout di report Word esistente per un report.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 77f377d6858294aeb54e30fcb178fc9757ac3938
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="add-fields-to-a-word-report-layout"></a>Aggiungere campi a un layout di report Word
Un set di dati del report può consistere di campi nei quali sono visualizzati etichette, dati e immagini. In questo argomento viene descritta la procedura dell'aggiunta dei campi di un set di dati del report a un layout di report Word esistente per un report. Aggiungere i campi utilizzando la parte XML personalizzata di Word per il report e aggiungendo i controlli contenuto che eseguono il mapping ai campi del set di dati del report. L'aggiunta dei campi richiede la conoscenza del set di dati del report, perché sia possibile identificare i campi che si desidera aggiungere al layout.  
  
> [!NOTE]  
>  Non è possibile modificare layout di report predefiniti<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="OpenXMLPart"></a>Per aprire la parte XML personalizzata per il report in Word  
  
1.  Se non è già aperto, aprire il documento di layout di report Word in Word.  
  
     Per ulteriori informazioni, vedere [Creare e modificare un layout di report personalizzato](ui-how-create-custom-report-layout.md).  
  
2.  Mostra la scheda **Sviluppatore** nella barra multifunzione di Microsoft Word.  
  
     Per impostazione predefinita, la scheda **Sviluppatore** non è indicata nella barra multifunzione. Per ulteriori informazioni, vedere [Visualizzare la scheda sviluppatore nella barra multifunzione](http://go.microsoft.com/fwlink/?LinkID=389631).  
  
3.  Nella scheda **Sviluppatore**, scegliere **Riquadro mapping XML**.  
  
4.  Nel riquadro **Mapping XML**, nell'elenco a discesa **Parte XML personalizzata**, scegliere la parte XML personalizzata per il report di ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->, che in genere è l'ultima nell'elenco. Il nome della parte XML personalizzata ha il seguente formato:  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *report_name* è il nome che viene assegnato al report<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *ID* corrisponde al numero di identificazione del report.  
  
     Dopo avere selezionato la parte XML personalizzata, il riquadro del mapping XML visualizza le etichette e i controlli campo disponibili per il report.  
  
### <a name="to-add-a-label-or-data-field"></a>Per aggiungere un campo dati o etichetta  
  
1.  Posizionare il cursore nel documento dove si desidera aggiungere il controllo.  
  
2.  Nel riquadro di ***Mapping XML**, fare clic con il pulsante destro del mouse sul controllo che si desidera aggiungere, scegliere **Immetti controllo contenuto**, quindi **Testo normale**.  
  
    > [!NOTE]  
    >  Non è possibile aggiungere un campo manualmente digitando il nome del campo set di dati nel controllo contenuto. Utilizzare il riquadro di **Mapping XML** per mappare i campi.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Per aggiungere righe ripetuti di campi dati per creare una lista  
  
1.  In una tabella, aggiungere una riga della tabella che include una colonna per ogni campo che si desidera che venga ripetuto.  
  
     Questa riga fungerà come segnaposto per i campi ripetuti.  
  
2.  Seleziona l'intera riga.  
  
3.  Nel riquadro di **Mapping XML**, fare clic con il pulsante destro del mouse sul controllo corrispondente all'elemento dati del report che contiene i campi che si desidera siano ripetuti, scegliere **Immetti controllo contenuto**, quindi scegliere **Ripetizione**.  
  
4.  Aggiungere i campi ripetuti alla riga come segue:  
  
    1.  Posizionare il puntatore in una colonna.  
  
    2.  Nel riquadro di ***Mapping XML**, fare clic con il pulsante destro del mouse sul controllo che si desidera aggiungere, scegliere **Immetti controllo contenuto**, quindi **Testo normale**.  
  
    3.  Ripetere i passaggi a e b per ogni campo.  
  
## <a name="adding-image-fields"></a>Aggiungere campi immagine  
 Un set di dati del report può includere un campo che contiene un'immagine, ad esempio un logo della società o l'immagine di un articolo. Per aggiungere un'immagine dal set di dati del report, si inserisce un controllo contenuto di **Immagine**.  
  
 Le immagini vengono allineate all'angolo in alto a sinistra del controllo contenuto e ridimensionate automaticamente per rispettare il limite del controllo contenuto.  
  
> [!IMPORTANT]  
>  È possibile aggiungere solo immagini con formato supportato da Word, ovvero .BMP, .jpeg e .png. Se si aggiunge un'immagine con un formato non supportato da Word, quando si esegue il report dal client di ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> sarà visualizzato un errore.  
  
#### <a name="to-add-an-image"></a>Per aggiungere un'immagine  
  
1.  Posizionare il puntatore nel documento dove si desidera aggiungere il controllo.  
  
2.  Nel riquadro di ***Mapping XML**, fare clic con il pulsante destro del mouse sul controllo che si desidera aggiungere, scegliere **Immetti controllo contenuto**, quindi **Immagine**.  
  
3.  Per aumentare o diminuire la dimensione dell'immagine, trascinare un quadratino di ridimensionamento verso il centro o lontano dal centro del controllo contenuto.  

## <a name="custom-xml-part-overview"></a>Panoramica della parte XML personalizzata
I layout di report Word sono sviluppati su *parti XML personalizzate*. Una parte XML personalizzata di un report consiste degli elementi corrispondenti agli elementi dati, alle colonne e alle etichette compresi nel set di dati del report. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->La parte XML personalizzata viene utilizzata per mappare i dati in un report all'esecuzione del report.

  
### <a name="xml-structure-of-custom-xml-part"></a>Struttura XML della Parte XML personalizzata  
Nella seguente tabella viene fornita una panoramica semplificata del codice XML di una parte XML personalizzata.  
  
|Elementi XML|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Testata|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Specifica di spazio dei nomi XML. `<reportname>` è il nome assegnato al report. `<id>` corrisponde all'ID assegnato al report.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Contiene tutte le etichette per il report.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--><br />-   Gli elementi delle etichette correlati alle colonne hanno il formato `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />-  Gli elementi delle etichette hanno il formato `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Le etichette sono elencate in ordine alfabetico.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Colonne ed elemento dati di livello principale. Le colonne sono elencate in ordine alfabetico.<!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Gli elementi di dati e le colonne che sono annidati nell'elemento dati di livello superiore. Le colonne sono elencate in ordine alfabetico sotto il rispettivo elemento di dati.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Scegliere gli articoli.|  
  
### <a name="custom-xml-part-in-word"></a>Personalizzare la parte XML in Word  
 In Word, aprire la parte XML personalizzata nel riquadro **Mapping XML**, quindi utilizzare il riquadro per mappare articoli ai controlli contenuto nel documento di Word. Il riquadro **Mapping XML** è accessibile dalla scheda **Sviluppatore**. Per ulteriori informazioni, vedere [Visualizzare la scheda sviluppatore nella barra multifunzione](http://go.microsoft.com/fwlink/?LinkID=389631).  
  
 Gli elementi nel riquadro **Mapping XML** vengono visualizzati in una struttura che è simile all'origine XML. I campi etichetta vengono raggruppati sotto di un elemento comune **Etichette**, mentre gli elementi di dati e le colonne sono disposti in una struttura gerarchica corrispondente all'origine XML, con le colonne elencate in ordine alfabetico. Gli elementi vengono identificati dal proprio nome come definito dalla proprietà nome in Progettazione set di dati del report in ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.  
  
 La figura seguente illustra la parte XML semplice personalizzata dalla sezione precedente nel riquadro **Mapping XML** di un documento Word.  
  
 ![Clip del riquadro Mapping XML in Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Per aggiungere un'etichetta o un campo al layout, si inserisce un controllo contenuto che mappa all'elemento presente nel riquadro di **Mapping XML**.  
  
-   Per creare righe ripetuti di colonne, inserire un controllo contenuto del tipo **Ripetizione** per l'elemento padre dell'elemento dati in questione e aggiungere il controllo contenuto per le colonne.  
  
-   Per le etichette, l'effettivo testo che viene visualizzato nel report generato corrisponde al valore della proprietà **Didascalia** del campo nella tabella elemento di dati (se l'etichetta è correlata alla colonna nel set di dati del report) o un'etichetta in progettazione etichette report (se l'etichetta non è correlata a una colonna del set di dati).  
  
-   La lingua dell'etichetta visualizzata quando si esegue il report dipende dall'impostazione della lingua dell'oggetto del report. <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a>Vedi anche  
 [Creare e modificare un layout di report personalizzato](ui-how-create-custom-report-layout.md)   
