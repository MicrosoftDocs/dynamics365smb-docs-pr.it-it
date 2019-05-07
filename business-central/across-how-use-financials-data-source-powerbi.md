---
title: Setup della creazione di report per Business Central in Power BI | Documenti Microsoft
description: Rendere disponibili i dati come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8dfedbc2685e086f9bdc63706d70327ebb95c2b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "919893"
---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Uso di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] come origine dati di Power BI per la creazione di report
È possibile rendere disponibili i dati di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.  

È necessario disporre di un account valido con [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] e con Power BI. Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Per aggiungere [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] come origine dati in Power BI Desktop
1. In Power BI Desktop, nel riquadro di spostamento sinistro, scegliere **Ottieni i dati**.
2. Nella pagina **Ottieni i dati**, scegliere **Servizi online**, quindi **Microsoft Dynamics 365 Business Central** e infine il pulsante **Connetti**.
3. Power BI visualizza una procedura guidata per il [processo di connessione](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Verrà richiesto di accedere al servizio. Fare clic su **Accedi** e selezionare l'account che si desidera usare per accedere. È necessario che sia lo stesso account usato per accedere a [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Fare clic sul pulsante **Connetti** per continuare. La procedura guidata di Power BI mostra un elenco di origini dati e società di Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le origini dati, indicano tutti i servizi Web pubblicati da ogni società in Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.
6. Specificare i dati che si desidera aggiungere al modello dati quindi scegliere il pulsante **Carica**.
7. Ripetere i passaggi precedenti per aggiungere altri dati di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], o altri dati, per il modello dati Power BI.

> [!NOTE]  
> Una volta eseguita la connessione a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], non verrà richiesto nuovamente di eseguire l'accesso.

Dopo che i dati sono stati caricati verranno visualizzati nel riquadro di spostamento destro nella pagina. A questo punto, è stata stabilita correttamente la connessione ai dati di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] e si è pronti per iniziare a creare il report di Power BI. 

Prima di creare il report, è consigliabile importare il file del tema Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Il file del tema creerà una tavolozza dei colori in modo da creare report con lo stesso stile cromatico dei pacchetti di contenuto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] senza dover defifnire i colori personalizzati per ogni elemento grafico.

Per ulteriori informazioni, vedere [Documentazione di Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Vedi anche
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finanze](finance.md)  
[Connessione di Power BI a [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
