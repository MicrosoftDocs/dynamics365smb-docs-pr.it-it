---
title: Setup della creazione di report per Finance and Operations, Business edition in Power BI | Documenti Microsoft
description: "È possibile rendere disponibili i dati Financials come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 056761b398737bd052b68488756198051f0cdb9a
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI per la creazione di report
È possibile rendere disponibili i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.  

> [!NOTE]  
> È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Power BI. Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Power BI Desktop
1. In Power BI Desktop, nel riquadro di spostamento sinistro, scegliere **Ottieni i dati**.
2. Nella finestra **Ottieni i dati**, scegliere **Servizi online**, quindi **Dynamics 365 for Finance and Operations, Business edition** e infine scegliere il pulsante **Connetti**.
3. Power BI visualizza una procedura guidata per il [processo di connessione](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Il primo passaggio consiste nell'accedere al servizio. Fare clic su **Accedi** e selezionare l'account che si desidera usare per accedere. È necessario che sia lo stesso account usato per accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Fare clic sul pulsante **Connetti** per continuare. La procedura guidata di Power BI mostra un elenco di origini dati e società di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le origini dati, indicano tutti i servizi Web pubblicati da ogni società in [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.
6. Specificare i dati che si desidera aggiungere al modello dati quindi scegliere il pulsante **Carica**.
7. Ripetere i passaggi precedenti per aggiungere altri dati [!INCLUDE[d365fin](includes/d365fin_md.md)] per il modello dati Power BI.

> [!NOTE]  
> Una volta eseguita la connessione a [!INCLUDE[d365fin](includes/d365fin_md.md)], non verrà richiesto nuovamente di eseguire l'accesso.

Dopo che i dati sono stati caricati verranno visualizzati nel riquadro di spostamento destro nella pagina. A questo punto, è stata stabilita correttamente la connessione ai dati di Finance and Operations, Business edition e si è pronti per iniziare a creare il report di Power BI. Per ulteriori informazioni, vedere la [Documentazione di Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Vedi anche
[Business Intelligence](bi.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finanze](finance.md)  
[Connessione di Power BI a [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

