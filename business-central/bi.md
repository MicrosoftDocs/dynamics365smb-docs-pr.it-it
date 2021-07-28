---
title: Business Intelligence
description: Business Central contiene una serie di funzionalità che ti consentono di raccogliere, analizzare e condividere dati aziendali preziosi per la business intelligence e il processo decisionale.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 866cfa9c35e7af7abb17ba9c9171244e2107de4d
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "6323745"
---
# <a name="business-intelligence"></a>Business Intelligence
Durante lo svolgimento dell'attività quotidiana, le aziende acquisiscono una quantità enorme di dati che riflettono, ad esempio, le cifre relative alle vendite, agli acquisti, alle spese operative, agli stipendi dei dipendenti e ai budget dell'organizzazione e possono diventare informazioni preziose, vale a dire Business Intelligence, per i responsabili decisionali. In [!INCLUDE[prod_short](includes/prod_short.md)] sono disponibili numerose funzionalità che facilitano la raccolta, l'analisi e la condivisione dei dati della società.

La funzionalità Dimensioni svolge un ruolo importante in business intelligence. Una dimensione corrisponde ai dati che è possibile aggiungere a un movimento come una specie di contrassegno. Tali dati vengono utilizzati per raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Tra altri utilizzi, le dimensioni si usano quando si definiscono le visualizzazioni analisi e si creano le situazioni contabili analisi per il reporting. Per ulteriori informazioni, vedere [Utilizzo delle dimensioni](finance-dimensions.md).

> [!TIP]
> Un modo rapido per analizzare i dati transazionali in base alle dimensioni consiste nel filtrare i totali nel piano dei conti e le voci in tutte le pagine **Voci** in base alle dimensioni. Cercare l'azione **Imposta filtro dimensione**.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

| A | Vedere |
| --- | --- |
|Visualizzare gli importi effettivi rispetto agli importi previsti per tutti i conti e per diversi periodi.|[Analisi degli importi effettivi e degli importi di budget](bi-how-analyze-actual-versus-budget.md)|
|Creare nuove situazioni contabili per definire i rendiconti finanziari per il reporting o la visualizzazione in grafici.|[Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti](bi-how-work-account-schedule.md)|
|Analizzare le prestazioni finanziarie impostando indicatori KPI basati su situazioni contabili che si pubblicano come servizi Web. Gli indicatori KPI situazione contabile pubblicati possono essere visualizzati su un sito Web o essere importati in Microsoft Excel utilizzando i servizi Web OData.|[Impostare e pubblicare servizi Web KPI basati sulle situazioni contabili](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)|
|Impostare le visualizzazioni di analisi per analizzare i dati utilizzando le dimensioni.|[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)|
|Creare nuovi report di analisi per vendite, acquisti e magazzino e impostare modelli di analisi.|[Creare report di analisi](bi-how-create-analysis-views-reports.md)|
|Abilitare il reporting finanziario globale da parte di organizzazioni contabili internazionali con lo standard eXtensible Business Reporting Language.|[Creare report con XBRL](bi-create-reports-with-xbrl.md)|
|Modificare l'intento di accesso al database su report, pagine di tipo API e query per ridurre il carico e migliorare le prestazioni.|[Gestire l'intento di accesso al database](admin-data-access-intent.md)|

## <a name="see-also"></a>Vedere anche
[Finanze](finance.md)    
[Uso di Business Central come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Chiusura di periodi fiscali](year-close-years-periods.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]