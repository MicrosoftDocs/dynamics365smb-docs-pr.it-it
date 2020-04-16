---
title: Utilizzare report di Business Central in Power BI | Microsoft Docs
description: Rendere disponibili i dati come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187894"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Uso di [!INCLUDE [prodlong](includes/prodlong.md)] come origine dati di Power BI per la creazione di report

È possibile rendere disponibili i dati di [!INCLUDE[prodlong](includes/prodlong.md)] come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.  

È necessario disporre di un account valido con [!INCLUDE[prodshort](includes/prodshort.md)] e con Power BI. Devi anche scaricare [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Per ulteriori informazioni, vedere [Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Per aggiungere [!INCLUDE[prodshort](includes/prodshort.md)] come origine dati in Power BI Desktop

1. In Power BI Desktop, nel riquadro di spostamento sinistro, scegliere **Ottieni i dati**.
2. Nella pagina **Ottieni i dati**, scegliere **Servizi online**, quindi **Microsoft Dynamics 365 Business Central** e infine il pulsante **Connetti**.
3. Power BI visualizza una procedura guidata per il processo di connessione, incluso l'accesso a [!INCLUDE [prodshort](includes/prodshort.md)]. Scegli **Accedi**, quindi seleziona l'account pertinente. Utilizza lo stesso account usato per accedere a [!INCLUDE [prodshort](includes/prodshort.md)].
4. Fare clic sul pulsante **Connetti** per continuare. La procedura guidata di Power BI mostra un elenco di ambienti, origini dati e società di Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le origini dati, indicano tutti i servizi Web pubblicati tramite [!INCLUDE [prodshort](includes/prodshort.md)].

    Puoi anche creare un nuovo URL del servizio web in [!INCLUDE [prodshort](includes/prodshort.md)]. Scegli uno dei seguenti metodi:

      - Usa l'azione **Crea set di dati** della pagina **Servizi Web**
      - Usa la guida del setup assistito **Imposta creazione di report**
      - Scegli l'azione **Modifica in Excel** in qualsiasi elenco

5. Specificare i dati che si desidera aggiungere al modello dati quindi scegliere il pulsante **Carica**.
6. Ripetere i passaggi precedenti per aggiungere ulteriori [!INCLUDE [prodshort](includes/prodshort.md)], o altri dati, per il modello dati Power BI.

> [!NOTE]  
> Una volta eseguita la connessione a [!INCLUDE [prodshort](includes/prodshort.md)], non verrà richiesto nuovamente di eseguire l'accesso.

Dopo che i dati sono stati caricati puoi vederli nel riquadro di spostamento destro nella pagina. Hai stabilito correttamente la connessione ai dati di [!INCLUDE [prodshort](includes/prodshort.md)] e sei pronto per iniziare a creare il report di Power BI.  

Prima di creare il report, è consigliabile importare il file del tema [!INCLUDE [prodshort](includes/prodshort.md)].  Il file del tema creerà una tavolozza dei colori in modo da creare report con lo stesso stile cromatico delle app [!INCLUDE [prodshort](includes/prodshort.md)] senza dover defifnire i colori personalizzati per ogni elemento grafico.

Per ulteriori informazioni, vedere [Documentazione di Power BI](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Abilitare i dati aziendali per Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
