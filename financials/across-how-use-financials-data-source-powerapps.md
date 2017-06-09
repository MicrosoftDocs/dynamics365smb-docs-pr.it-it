---
title: Utilizzo di Dynamics 365 for Financials come origine dati in PowerApps | Documenti di Microsoft
description: "È possibile rendere disponibili i dati di Financials come origine dati in PowerApps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cedc95b23481b8cb76da85e8459a97b1880a4218
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-powerapps-data-source"></a>Utilizzo di Dynamics 365 for Financials come origine dati in PowerApps
È possibile rendere disponibili i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps.  

**Nota**: è necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps
1. Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), quindi accedere.
2. Nel riquadro di spostamento sinistro scegliere **Nuova app**.
3. Scegliere l'editor, PowerApps Studio per Windows o PowerApps Studio per il Web.

   PowerApps Studio per Windows è un'applicazione desktop utilizzata per creare e pubblicare PowerApps. PowerApps Studio per il Web è una soluzione online utilizzata per creare e pubblicare PowerApps.
4. Il passaggio successivo per creare una PowerApp è selezionare i dati. Scegliere l'icona della freccia, quindi scegliere l'opzione **Nuova connessione** nella parte in alto a sinistra della pagina.
5. Nell'elenco delle connessioni disponibili scegliere **Dynamics 365 for Financials**.
6. In PowerApps verrà visualizzata una pagina di connessione in cui verranno richieste le informazioni necessarie per accedere ai propri dati di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per connettersi, è necessario specificare un URL OData, un nome utente, una password e un nome società.

   Per l'*URL OData* è possibile copiare l'URL OData V4 di qualsiasi servizio Web elencato nella pagina **Servizi Web** in [!INCLUDE[d365fin](includes/d365fin_md.md)], come `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Per *Nome Società*, utilizzare il nome che viene visualizzato nel campo **Nome** nella finestra **Informazioni Società** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene più società, scegliere il nome della società appropriata dall'elenco nella finestra **Società**. In entrambi i casi, verificare che il nome specificato nella procedura guidata di PowerApps corrisponda esattamente al testo contenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)], come `My Company`.

   Per nome utente e password, utilizzare il nome e la chiave del servizio di accesso Web specificata per l'account nella finestra **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, il nome utente è *ADMIN* e la chiave del servizio di accesso Web utilizzata è *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Fare clic sul pulsante **Connessione** per continuare. In PowerApps verrà visualizzato un gruppo di dati di default per [!INCLUDE[d365fin](includes/d365fin_md.md)]. Scegliere il gruppo di dati **Default**.

   In PowerApps verrà visualizzata una lista delle tabelle disponibili tramite [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le tabelle, o punti finali, indicano tutti i servizi Web pubblicati tramite [!INCLUDE[d365fin](includes/d365fin_md.md)].

   In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.
8. Scegliere la tabella che si desidera utilizzare per PowerApp, quindi scegliere il pulsante **Connetti**.
9. Ripetere i passaggi precedenti per aggiungere altri dati [!INCLUDE[d365fin](includes/d365fin_md.md)] per il modello dati Power BI.

   **Nota**: una volta stabilita la connessione a [!INCLUDE[d365fin](includes/d365fin_md.md)], non verrà nuovamente richiesto l'URL OData, il nome utente o la password.

A questo punto, è stata stabilita correttamente la connessione ai dati di Dynamics 365 e si è pronti per iniziare a creare la PowerApp. Per ulteriori informazioni, vedere la [Documentazione di PowerApps](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Vedi anche
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Impostare [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanza](finance.md)  

