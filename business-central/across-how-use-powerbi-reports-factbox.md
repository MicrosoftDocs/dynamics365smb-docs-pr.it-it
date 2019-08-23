---
title: Visualizzare i report personalizzati di Power BI | Microsoft Docs
description: È possibile usare i report Power BI per ottenere informazioni aggiuntive sui dati negli elenchi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: acf9462db8b4f559a5fbc40381b4e5009cdac088
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755197"
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Visualizzazione dei dati degli elenchi nei report Power BI in Business Central

[!INCLUDE[prodlong](includes/prodlong.md)] include un elemento di controllo Dettaglio informazioni in una serie di pagine elenco chiave che offrono informazioni aggiuntive sui dati in elenco. Spostandosi tra le righe dell'elenco, il report viene aggiornato e filtrato per la voce selezionata. È possibile creare i report personalizzati da visualizzare in questo controllo, ma vi sono alcune regole da seguire nella creazione di report per assicurare il comportamento desiderato.  

> [!NOTE]  
> È necessario disporre di un account valido con [!INCLUDE[prodshort](includes/prodshort.md)] e con Power BI. Inoltre, per creare report personalizzati, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Per ulteriori informazioni, vedere [Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Set di dati del report
Quando si crea il report in Power BI Desktop, specificare l'origine dei dati o il servizio Web che contiene i dati relativi all'elenco che si desidera associare al report. Ad esempio, se si desidera creare un report per la lista di vendita, verificare che il set di dati contenga le informazioni relative alle vendite.  

Per filtrare i dati nei report basati sul record selezionato nella pagina elenco, la chiave primaria deve essere utilizzata come filtro nel report. Le chiavi primarie dovranno fa parte di un set di dati in modo che i report vengano filtrati correttamente. Nella maggior parte dei casi, la chiave primaria per un elenco è **Nr.** .  

## <a name="defining-the-report-filter"></a>Definizione del filtro report
Il report richiede un filtro di base del report (non una pagina o un filtro visivo e non un filtro avanzato) per filtrare correttamente nel controllo del riquadro dettaglio informazioni di Power BI. Il filtro che viene trasmesso al report Power BI da ogni pagina elenco sarà basato sulla chiave primaria come descritto nella precedente sezione.  

Per definire un filtro per il report, selezionare la chiave primaria dall'elenco dei campi disponibili e quindi trascinare il campo nella sezione **Filtro Report**.  

![Impostare il filtro del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Dimensione e colori del report
La dimensione del report deve essere impostata su 325 x 310 pixel. Ciò è necessario per il corretto ridimensionamento del report nello spazio disponibile consentito dal controllo del riquadro dettaglio informazioni di Power BI. Per definire la dimensione del report, posizionare il focus all'esterno dell'area del layout di report e quindi scegliere l'icona del rullo di verniciatura.

![Impostare la larghezza e l'altezza del report per il report Attività Fattura vendita](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

È possibile modificare la larghezza e l'altezza del report scegliendo **Personalizzato** nel campo **Tipo**.

Allo stesso modo, se si desidera che lo sfondo del report sfumi con il colore di sfondo del controllo del riquadro dettaglio informazioni di Power BI, definire un colore di sfondo personalizzato del report *E5E5E5*. Questo campo è facoltativo.  

## <a name="reports-with-multiple-pages"></a>Report con più pagine
Power BI consente di creare un unico report con più pagine. Gli elementi grafici che si desidera visualizzare nelle pagine elenco di [!INCLUDE[d365fin](includes/d365fin_md.md)] devono essere nella prima pagina del report di Power BI.  

> [!NOTE]  
> Il riquadro dettaglio informazioni di Power BI può mostrare solo la prima pagina del report. Se si desidera visualizzare altre pagine, è necessario espandere il report e utilizzare le schede nella parte inferiore del report per passare ad atre pagine.  

## <a name="saving-your-report"></a>Salvare il report

Quando si salva il report, è una buona pratica che il nome del report contenga il nome della pagina elenco in cui si desidera visualizzare il report. Ad esempio, la parola *Fornitore* deve essere contenuta da qualche parte nel nome del report per i report che si desidera rendere disponibili nell'elenco Fornitori.  

Questo non è un requisito; tuttavia, renderà il processo di selezione dei report più veloce. Quando la pagina di selezione dei report viene aperta da una pagina elenco, si passerà in un filtro in base al nome della pagina per limitare i report da visualizzare.  È possibile rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.  

## <a name="troubleshooting"></a>Risoluzione dei problemi
In questa sezione viene fornita una soluzione alternativa per i problemi più comuni che si verificano quando si creano report Power BI.  

**L'utente non visualizza un report che desidera selezionare nella pagina di selezione report.** Se non è possibile selezionare un report, è possibile verificare il nome del report per assicurarsi che esso contenga il nome della pagina elenco. È anche possibile rimuovere il filtro per ottenere un elenco completo dei report disponibili in Power BI.  

**Il report viene caricato ma è vuoto, non filtrato o filtrato erroneamente** Verificare che il filtro del report contenga la chiave primaria corretta. Nella maggior parte dei casi, questo è il campo **Nr.** ma nella tabella **Movimenti C/G**, ad esempio, è necessario utilizzare il campo **Nr. movimento**.

**Il report viene caricato ma non viene visualizzata la pagina prevista** Verificare che la pagina che si desidera visualizzare sia la prima pagina del report.  

**Il report viene visualizzato con bordi grigi indesiderati, è troppo piccolo o troppo grande**

Verificare che la dimensione del report sia impostata su 325 x 310 pixel. Salvare il report quindi aggiornare la pagina elenco.  

## <a name="see-also"></a>Vedere anche

[Abilitare i dati aziendali per Power BI](admin-powerbi.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Introduzione](product-get-started.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
