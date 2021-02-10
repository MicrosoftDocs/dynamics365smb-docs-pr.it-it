---
title: Visualizzare report Power BI personalizzati per i dati di Business Central | Microsoft Docs
description: È possibile usare i report Power BI per ottenere informazioni aggiuntive sui dati negli elenchi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 069efcef517cd442539f13fad5e5a2c89e1533ff
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754469"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] include un elemento di controllo Dettaglio informazioni in una serie di pagine elenco chiave che offrono informazioni aggiuntive sui dati in elenco. Spostandosi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata. È possibile creare report personalizzati da visualizzare in questo controllo. Tuttavia, esistono alcune regole da seguire per garantire che i report funzionino come previsto.  

## <a name="prerequisites"></a>Prerequisiti

- Un account Power BI.
- Power BI Desktop.

Per ulteriori informazioni su come iniziare, vedere [Uso di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Definizione del set di dati del report

Specificare l'origine dati che contiene i dati relativi all'elenco. Ad esempio, per creare un report per la lista di vendita, verificare che il set di dati contenga le informazioni relative alle vendite.  

## <a name="defining-the-report-filter"></a>Definizione del filtro report

Per aggiornare i dati al record selezionato nell'elenco, aggiungere un filtro al report. Il filtro deve includere un campo dell'origine dati utilizzata come *chiave primaria*. Nella maggior parte dei casi, la chiave primaria per un elenco è **Nr.** .

Per definire un filtro per il report, selezionare la chiave primaria dall'elenco dei campi disponibili e quindi trascinare il campo nella sezione **Filtro Report**. Il filtro deve essere un filtro di report di base definito per tutte le pagine. Non può essere un filtro di pagina, visivo o avanzato.

![Impostare il filtro del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Impostazione della dimensione e del colore del report

La dimensione del report deve essere impostata su 325 x 310 pixel. Questa dimensione fornisce il corretto ridimensionamento del report nello spazio disponibile dal controllo del riquadro dettaglio informazioni Power BI in [!INCLUDE[prod_short](includes/prod_short.md)]. Per definire la dimensione del report, posizionare il focus all'esterno dell'area del layout di report e quindi scegliere l'icona del rullo di verniciatura.

![Impostare la larghezza e l'altezza del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

È possibile modificare la larghezza e l'altezza del report scegliendo **Personalizzato** nel campo **Tipo**.

Se si desidera che lo sfondo del report sfumi con il colore di sfondo del controllo del riquadro dettaglio informazioni di Power BI, impostare un colore di sfondo personalizzato del report *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Uso dei report con più pagine

Power BI consente di creare un unico report con più pagine. Tuttavia, per i report che verranno visualizzati con le pagine di elenco, non è consigliabile che abbiano più di una pagina. Il riquadro Dettaglio informazioni Power BI mostrerà solo la prima pagina del report.

## <a name="naming-the-report"></a>Assegnazione di un nome al report

Assegnare al report un nome che contenga il nome della pagina di elenco associata al report. Ad esempio, se il report è per la pagina di elenco **Fornitore**, includere la parola *fornitore* da qualche parte nel nome.  

Questa convenzione di denominazione non è un requisito. Tuttavia, rende la selezione dei report in [!INCLUDE[prod_short](includes/prod_short.md)] più veloce. Quando la pagina di selezione del report si apre da una pagina di elenco, viene automaticamente filtrata in base al nome della pagina. Questo filtro viene eseguito per limitare i report visualizzati. Gli utenti possono rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.  

## <a name="fixing-problems"></a>Risolvere i problemi

In questa sezione viene fornita una soluzione alternativa per i problemi più comuni che si verificano quando si creano report Power BI.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Non è possibile visualizzare un report nella pagina Seleziona report

Probabilmente è perché il nome del report non contiene il nome della pagina di elenco. Rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Il report è caricato ma è vuoto, non filtrato o filtrato in modo errato

Verificare che il filtro del report contenga la chiave primaria corretta. Nella maggior parte dei casi, questo è il campo **Nr.** ma nella tabella **Movimenti C/G**, ad esempio, è necessario utilizzare il campo **Nr. movimento**.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Il report è caricato, ma mostra una pagina non prevista

Verificare che la pagina da visualizzare sia la prima pagina del report.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Il report viene visualizzato con un bordo grigio indesiderato o è troppo piccolo o troppo grande

Verificare che la dimensione del report sia impostata su 325 x 310 pixel. Salvare il report quindi aggiornare la pagina elenco.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Abilitare i dati aziendali per Power BI](admin-powerbi.md)  
[Uso di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Introduzione](product-get-started.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  
