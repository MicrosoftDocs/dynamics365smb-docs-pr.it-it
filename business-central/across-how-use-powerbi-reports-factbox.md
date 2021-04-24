---
title: Visualizzare report Power BI personalizzati per i dati di Business Central | Microsoft Docs
description: Puoi usare i report Power BI per ottenere informazioni aggiuntive sui dati negli elenchi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777518"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] include un elemento di controllo Dettaglio informazioni Power BI su diverse pagine elenco chiave. Lo scopo di questo Dettaglio informazioni è di visualizzare i report Power BI che sono correlati ai record negli elenchi, fornendo ulteriori informazioni sui dati. L'idea è di spostarsi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata.

[!INCLUDE[prod_long](includes/prod_long.md)] viene fornito con alcuni di questi report. Puoi anche creare i tuoi report personalizzati che vengono visualizzati in questo Dettaglio informazioni. La creazione di questi report è simile ad altri report. Ma ci sono alcune regole di progettazione che dovrai seguire per assicurarti che i report vengano visualizzati come previsto. Queste regole sono spiegate in questo articolo.

> [!NOTE]
> Per informazioni generali sulla creazione e la pubblicazione di report Power BI per Business Central, vedi [Creazione di report Power BI per visualizzare i dati [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Prerequisiti

- Un account Power BI.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a>Crea un report per una pagina di elenco

1. Avviare Power BI Desktop.
2. Seleziona **Ottieni dati** e inizia a scegliere l'origine dati per il report.

    In questa fase, si specificano le pagine di elenco di Business Central che contengono i dati desiderati nel report. Ad esempio, per creare un report per la lista di vendita, verificare che il set di dati contenga le informazioni relative alle vendite.

    Per ulteriori informazioni, segui le istruzioni [Aggiungi [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Imposta il filtro per i report.

    Per aggiornare i dati al record selezionato nell'elenco, aggiungere un filtro al report. Il filtro deve includere un campo dell'origine dati utilizzato per identificare in modo univoco ogni record nell'elenco. Per gli sviluppatori, questo campo è la *chiave primaria*. Nella maggior parte dei casi, la chiave primaria per un elenco è **Nr.** .

    Per impostare il filtro, procedi nel seguente modo:

    1. In **Filtri**, seleziona il campo della chiave primaria dall'elenco dei campi disponibili.
    2. Trascina il campo sul riquadro **Filtri** e rilascialo nella casella **Filtri su tutte le pagine**.
    3. Imposta il **Tipo di filtro** su **Filtro di base**. Non può essere un filtro di pagina, visivo o avanzato.

    ![Impostare il filtro del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Progetta l'area di disposizione del report.

    Crea l'area di disposizione trascinando i campi e aggiungendo visualizzazioni. Per ulteriori informazioni, vedi [Lavora con la visualizzazione Report in Power BI Desktop](/power-bi/create-reports/desktop-report-view) nella documentazione di Power BI.

5. Vedi le sezioni successive sul dimensionamento del report e sull'utilizzo di più pagine.

6. Salva e assegna un nome al rapporto.

    È importante assegnare al report un nome che contenga il nome della pagina di elenco associata al report. Ad esempio, se il report è per la pagina di elenco **Articoli**, includi la parola *articoli* da qualche parte nel nome.  

    Questa convenzione di denominazione non è un requisito. Tuttavia, rende la selezione dei report in [!INCLUDE[prod_short](includes/prod_short.md)] più veloce. Quando la pagina di selezione del report si apre da una pagina di elenco, viene automaticamente filtrata in base al nome della pagina. Questo filtro viene eseguito per limitare i report visualizzati. Gli utenti possono rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.

7. Quando hai finito, pubblica il report come al solito.

    Per ulteriori informazioni, vedi [Pubblicazione di un report](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Prova il report.

    Una volta che i rapporti sono stati pubblicati nel tuo spazio di lavoro, dovrebbero essere disponibili dal Dettaglio informazioni di Power BI nella pagina dell'elenco in [!INCLUDE[prod_short](includes/prod_short.md)].

    Per provarlo, segui i passaggi seguenti.

    1. Apri [!INCLUDE[prod_short](includes/prod_short.md)] e vai alla pagina dell'elenco.
    2. Se non vedi Dettaglio informazioni di Power BI, vai alla barra delle azioni, quindi seleziona **Azioni** > **Visualizza** > **Mostra/Nascondi report di Power BI**.
    3. In Dettagli informazioni di Power BI, scegli **Seleziona report**, quindi la casella **Abilita** per il report, quindi seleziona **OK**.

    Se progettato correttamente, viene visualizzato il report.  

## <a name="set-the-report-size-and-color"></a>Imposta le dimensioni e il colore del report

La dimensione del report deve essere impostata su 325 x 310 pixel. Questa dimensione fornisce il corretto ridimensionamento del report nello spazio disponibile dal controllo del riquadro dettaglio informazioni Power BI in [!INCLUDE[prod_short](includes/prod_short.md)]. Per definire la dimensione del report, posizionare il focus all'esterno dell'area del layout di report e quindi scegliere l'icona del rullo di verniciatura.

![Impostare la larghezza e l'altezza del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

È possibile modificare la larghezza e l'altezza del report scegliendo **Personalizzato** nel campo **Tipo**.

Se desideri che lo sfondo del report sfumi con il colore di sfondo del controllo del riquadro Dettaglio informazioni di Power BI, imposta un colore di sfondo personalizzato del report *#FFFFFF* (bianco). 

> [!TIP]
> Usa il file del tema di [!INCLUDE [prod_short](includes/prod_short.md)] per creare report con lo stesso stile di colore delle app [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Uso del tema del report [!INCLUDE [prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a>Report con più pagine

Power BI consente di creare un unico report con più pagine. Tuttavia, per i report che verranno visualizzati con le pagine di elenco, non è consigliabile che abbiano più di una pagina. Il riquadro Dettaglio informazioni Power BI mostrerà solo la prima pagina del report.

## <a name="fixing-problems"></a>Risolvere i problemi

Questa sezione fornisce istruzioni su come risolvere i problemi che potresti incontrare durante il tentativo di visualizzare un report di Power BI per una pagina di elenco in [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>Non puoi vedere il Dettaglio informazioni di Power BI in una pagina di elenco

Per impostazione predefinita, il Dettaglio informazioni di Power BI è nascosto alla vista. Per visualizzare il Dettaglio informazioni su una pagina, dalla barra delle azioni, seleziona **Azioni** > **Schermo** > **Mostra/Nascondi report Power BI**.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a>Non è possibile visualizzare il report nel pannello Seleziona report

Probabilmente è perché il nome del report non contiene il nome della pagina di elenco visualizzata. Rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Il report è caricato ma è vuoto, non filtrato o filtrato in modo errato

Verificare che il filtro del report contenga la chiave primaria corretta. Nella maggior parte dei casi, questo è il campo **Nr.** ma nella tabella **Movimenti C/G**, ad esempio, è necessario utilizzare il campo **Nr. movimento**.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Il report è caricato, ma mostra una pagina non prevista

Verificare che la pagina da visualizzare sia la prima pagina del report.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Il report viene visualizzato con un bordo grigio indesiderato o è troppo piccolo o troppo grande

Verificare che la dimensione del report sia impostata su 325 x 310 pixel. Salvare il report quindi aggiornare la pagina elenco.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Abilitare i dati aziendali per Power BI](admin-powerbi.md)  
[Uso di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]