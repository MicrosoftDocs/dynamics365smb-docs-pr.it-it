---
title: Come connettere Power BI a Finance and Operations, Business edition | Documenti Microsoft
description: "Ottenere informazioni approfondite, business intelligence e KPI sui dati di Finance and Operations, Business edition è semplice con Power BI e con i pacchetti di contenuto di Finance and Operations, Business edition."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a>Pacchetti di contenuto per connessione di Power BI a Finance and Operations, Business edition
Ottenere informazioni approfondite sui dati di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] è semplice con Power BI e con i pacchetti di contenuto di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Power BI recupera i dati e quindi sviluppa un dashboard e i report pronti per l'uso basati su tali dati.

> [!NOTE]  
>  È necessario disporre di un account valido con Dynamics 365 e con Power BI. Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  I pacchetti di contenuto di Power BI richiedono l'autorizzazione per l'accesso alle tabelle da dove vengono recuperati i dati. Più informazioni dettagliate sui requisiti sono descritte di seguito.  

## <a name="how-to-connect"></a>Come ci si connette
1. Selezionare **Ottieni i dati** nella parte inferiore del riquadro di spostamento sinistro.  
![Passare a Ottieni i dati](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. Nella casella **Servizi**, selezionare **Ottieni**. Viene visualizzata una finestra con **AppSource** e **App per app Power BI**.  
![Scegliere i pacchetti di contenuto da servizi in linea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Selezionare **App** dalla scheda **App per app di Power BI** e scegliere il pacchetto di contenuti **Microsoft Dynamics 365 for Finance and Operations** che si desidera utilizzare e selezionare **Ottienilo ora**.  
![Selezionare Dynamics 365 for Finance and Operations, Business edition e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Quando richiesto immettere il nome della *società* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Questo non è il nome visualizzato.  
![Selezionare Dynamics 365 for Finance and Operations, Business edition e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Una volta eseguita la connessione, un dashboard, un report e un set di dati verranno automaticamente caricati nell'area di lavoro Power BI. Al termine, i riquadri saranno aggiornati con i dati dell'account.
![Selezionare Dynamics 365 for Finance and Operations, Business edition e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Operazioni successive

- Provare a [porre una domanda nella casella delle domande e risposte](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) nella parte superiore del dashboard.  
- [Modificare i riquadri](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) nel dashboard.  
- [Selezionare un riquadro](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) per aprire il report sottostante.  
- Poiché il set di dati verrà programmato per l'aggiornamento giornaliero, è possibile modificare la pianificazione dell'aggiornamento o provare ad aggiornare su richiesta usando **Aggiorna ora**.

## <a name="system-requirements"></a>Requisiti di sistema
Per importare i dati di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI, è necessario disporre delle autorizzazioni per accedere ai servizi Web utilizzati per recuperare i dati. I servizi Web necessari per ogni pacchetto di contenuti sono:

**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**
- PowerBIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**
- Lista commesse
- Righe pianificazione commessa
- Righe task commessa

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard
- Power_BI_Customer_List
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Articoli
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Articoli
- SalesDashboard
- Power_BI_Customer_List
- ItemSalesbyCustomer
- Power_BI_Vendor_List
- ExcelTemplateViewCompany

## <a name="web-services"></a>Servizi Web
Un modo facile di individuare i servizi Web consiste nel ricercarli in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Nell'elenco assicurarsi che la casella Pubblica sia contrassegnata per i servizi Web sopra elencati.

## <a name="troubleshooting"></a>Troubleshooting
Il dashboard di Power BI si basa sui servizi Web rilasciati che sono elencati sopra e visualizza i dati della società demo o della società dell'utente se si importano i dati della soluzione finanziario corrente. Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.

### <a name="incorrect-company-name"></a>Nome della società non corretto  
Un errore comune consiste nell'immettere il nome visualizzato della società al posto del nome della società. Per individuare il nome della società, cercare **Società**. Quindi utilizzare il campo **Nome** quando si immette il nome della società.

### <a name="incorrect-user-name-and-password"></a>Nome utente e password errate  
Il nome utente e la password utilizzati per connettersi sono uguali a quelli usati per connettersi all'account Microsoft Office 365.  

I pacchetti di contenuto richiedono inoltre la presenza di un account Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Una volta immesse le credenziali, verranno individuati tutti i tenant Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a cui è possibile accedere. Se non si dispone di un account Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] con licenza o di prova, verrà visualizzato un messaggio di errore.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nessuna riga corrispondente alla chiave nella tabella
Se si immette un nome di società non valido durante il processo di connessione, è possibile che sia visualizzato il messaggio di errore "Nessuna riga corrispondente alla chiave nella tabella". Immettere il nome di società corretto e riprovare.

## <a name="see-also"></a>Vedi anche
[Introduzione a Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Concetti](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
[Setup della creazione di report per [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)  

