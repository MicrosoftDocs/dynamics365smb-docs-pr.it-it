---
title: Utilizzo di Dynamics 365 for Financials come origine dati in Power BI | Documenti di Microsoft
description: "È possibile rendere disponibili i dati Financials come origine di dati in Power BI e sviluppare report efficaci dello stato dell&quot;attività."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5213b515dfdf1f0e538a6d003cf921781ca6b3ff
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-power-bi-data-source"></a>Utilizzo di Dynamics 365 for Financials come origine dati in Power BI
È possibile rendere disponibili i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.  

**Nota**: è necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Power BI. Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Power BI Desktop
1. In Power BI Desktop, nel riquadro di spostamento sinistro, scegliere **Ottieni i dati**.
2. Nella finestra **Ottieni i dati**, scegliere **Servizi online**, quindi **Dynamics 365 for Financials** e infine scegliere il pulsante **Connetti**.

   Power BI visualizza una procedura guidata per il processo di connessione. Il primo passo consiste nell'immettere un URL OData e il nome della società associato con l'account [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Per l'*URL OData* è possibile copiare l'URL OData V4 di qualsiasi servizio Web elencato nella pagina **Servizi Web** in [!INCLUDE[d365fin](includes/d365fin_md.md)], come `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Per *Nome Società*, utilizzare il nome che viene visualizzato nel campo **Nome** nella finestra **Informazioni Società** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene più società, scegliere il nome della società appropriata dall'elenco nella finestra **Società**. In entrambi i casi, verificare che il nome specificato nella procedura guidata di Power BI corrisponda esattamente al testo contenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)], come `My Company`.
3. Dopo aver immesso le informazioni richieste, fare clic sul pulsante OK. Il passaggio successivo consiste nell'immettere il nome utente e password.

   **Nota**: se sono disponibili altre opzioni di autenticazione nel pannello di navigazione di sinistra, scegliere *Di base*.
4. Immettere il nome utente e password. È possibile trovare queste informazioni nella finestra di dialogo **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilizzare **Chiave di accesso Web** come password.

   Ad esempio, il nome utente è *ADMIN* e la chiave del servizio di accesso Web utilizzata è *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Fare clic sul pulsante **Connessione** per continuare. La procedura guidata di Power BI mostra un elenco di origini dati di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le origini dati, indicano tutti i servizi Web pubblicati tramite [!INCLUDE[d365fin](includes/d365fin_md.md)].

   In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.
6. Specificare i dati che si desidera aggiungere al modello dati quindi scegliere il pulsante **Carica**.
7. Ripetere i passaggi precedenti per aggiungere altri dati [!INCLUDE[d365fin](includes/d365fin_md.md)] per il modello dati Power BI.

   **Nota**: una volta stabilita la connessione a [!INCLUDE[d365fin](includes/d365fin_md.md)], non verrà nuovamente richiesto l'URL OData, il nome utente o la password.

Dopo che i dati sono stati caricati verranno visualizzati nel riquadro di spostamento destro nella pagina. A questo punto, è stata stabilita correttamente la connessione ai dati di Dynamics 365 e si è pronti per iniziare a creare il report di Power BI. Per ulteriori informazioni, vedere la [Documentazione di Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Vedi anche
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Impostare [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanza](finance.md)  

