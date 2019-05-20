---
title: Come connettere Power BI a Business Central | Documenti Microsoft
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con Power BI e con i pacchetti di contenuto di Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-powerbi
ms.openlocfilehash: b7e844f64a96ba02c1a5fa0231f7b6992f972677
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247400"
---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Collegare Power BI a pacchetti di contenuto di Dynamics 365 Business Central
Ottenere informazioni approfondite sui dati di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] è semplice con Power BI e con i pacchetti di contenuto di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Power BI recupera i dati e quindi sviluppa un dashboard e i report pronti per l'uso basati su tali dati.

È necessario disporre di un account valido con Dynamics 365 e Power BI. Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) per creare i propri report Power BI. I pacchetti di contenuto di Power BI richiedono l'autorizzazione per l'accesso alle tabelle da dove vengono recuperati i dati. Più informazioni dettagliate sui requisiti sono descritte di seguito.  

## <a name="how-to-connect"></a>Come ci si connette
1. Selezionare **Ottieni i dati** nella parte inferiore del riquadro di spostamento sinistro.  
![Passare a Ottieni i dati](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

È inoltre possibile iniziare da Dynamics 365 Business Edition. Dalla Gestione ruolo utente, passare a **Selezione report** nella sezione Gestione ruolo utente Power BI. Selezionare **Assistenza** o **Organizzazione personale** dalla barra multifunzione. Quando viene selezionata una di queste azioni, si verrà reindirizzati alla raccolta dell'organizzazione in Power BI o alla libreria dei servizi in Power BI, che verranno filtrate per visualizzare solo i pacchetti di contenuto relativi a [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. Nella casella **Servizi**, selezionare **Ottieni**. Viene visualizzata una pagina con **AppSource** e **App per app Power BI**.  
![Scegliere i pacchetti di contenuto da servizi in linea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Selezionare **App** dalla scheda **App per app di Power BI** e scegliere il pacchetto di contenuti **Microsoft Dynamics 365 Business Central** che si desidera utilizzare e selezionare **Ottienilo ora**.  
![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Quando richiesto immettere il nome della *società* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Questo non è il nome visualizzato. Il nome della società è disponibile nella pagina 'Società' all'interno dell'istanza di [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. 
![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Una volta eseguita la connessione, un dashboard, un report e un set di dati verranno automaticamente caricati nell'area di lavoro Power BI. Al termine, i riquadri saranno aggiornati con i dati della società [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].
![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Operazioni successive

- Provare a [porre una domanda nella casella delle domande e risposte](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) nella parte superiore del dashboard.
- [Modificare i riquadri](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) nel dashboard.  
- [Selezionare un riquadro](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) per aprire il report sottostante.  
- Poiché il set di dati verrà programmato per l'aggiornamento giornaliero, è possibile modificare la pianificazione dell'aggiornamento o provare ad aggiornare su richiesta usando **Aggiorna ora**.

## <a name="system-requirements"></a>Requisiti di sistema
Per importare i dati di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI, è necessario disporre delle autorizzazioni per accedere ai servizi Web utilizzati per recuperare i dati. I servizi Web necessari per ogni pacchetto di contenuti sono:

## <a name="role-center-reports"></a>Report in Gestione ruolo utente

**Microsoft Dynamics 365 Business Central – CRM**
- Opportunità di vendita
- Modello di Excel Visualizza socetà
- Etichette report Power BI

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Modello di Excel Visualizza società
- Etichette report Power BI

**Microsoft Dynamics 365 Business Central – Jobs**
- Lista commesse
- Righe pianificazione commessa
- Righe task commessa
- Etichette report Power BI
- Modello di Excel Visualizza società

**Microsoft Dynamics 365 Business Central - Sales**
- Dashboard vendite
- Modello di Excel Visualizza società
- Etichette report Power BI

## <a name="list-page-reports"></a>Report pagina liste 

**Microsoft Dynamics 365 Business Central – Customers List**
- Vendite articolo per cliente
- Lista acquisti articolo Power BI
- Lista vendite articolo Power BI
- Dashboard vendite
- Lista clienti Power BI
- ExcelTemplateViewCompany
- Etichette report Power BI 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Lista importo C/G Power BI
- Importo a budget C/G Power BI
- ExcelTemplateViewCompany
- Etichette report Power BI

**Microsoft Dynamics 365 Business Central – Items List**
- Vendite articolo per cliente
- Lista acquisti articolo Power BI
- Lista vendite articolo Power BI
- Dashboard vendite
- ExcelTemplateViewCompany
- Etichette report Power BI

**Microsoft Dynamics 365 Business Central – Jobs List**
- Lista commesse Power BI
- ExcelTemplateViewCompany
- Etichette report Power BI

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Lista acquisti Power BI
- ExcelTemplateViewCompany
- Etichette report Power BI

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Lista vendite Power BI
- ExcelTemplateViewCompany
- Etichette report Power BI


**Microsoft Dynamics 365 Business Central – Vendors List**
- Lista acquisti articolo Power BI
- Lista vendite articolo Power BI
- Lista fornitori  Power BI
- ExcelTemplateViewCompany
- Etichette report Power BI

## <a name="web-services"></a>Servizi Web
Un modo facile di individuare i servizi Web consiste nel ricercarli in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Nell'elenco assicurarsi che la casella Pubblica sia contrassegnata per i servizi Web sopra elencati.

## <a name="troubleshooting"></a>Risoluzione dei problemi
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
[Power BI - Concetti di base](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
[Setup della creazione di report per [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)  
