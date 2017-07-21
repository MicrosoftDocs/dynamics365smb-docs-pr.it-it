---
title: Connettere i dati a Flow| Documenti Microsoft
description: "È possibile rendere disponibili i dati di Financials come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato
È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.  

> [!NOTE]  
>   È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Flow
1. Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com/en-us/), quindi accedere.
2. Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.
3. Nella finestra **I miei flussi** selezionare **Creare da Vuoto**.
4. Selezionare uno dei trigger disponibili, selezionare uno dei due trigger di [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibili: *Alla creazione di un record* o *Alla modifica di un record*.
5. In Flow verrà visualizzata una pagina di connessione in cui verranno richieste le informazioni necessarie per accedere ai propri dati di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per connettersi automaticamente, è necessario specificare un nome per la connessione, un URL OData, nome utente, password e nome della società.

   Per l'*URL OData* è possibile copiare l'URL OData V4 di qualsiasi servizio Web elencato nella pagina **Servizi Web** in [!INCLUDE[d365fin](includes/d365fin_md.md)], come `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Per *Nome Società*, utilizzare il nome che viene visualizzato nel campo **Nome** nella finestra **Informazioni Società** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene più società, scegliere il nome della società appropriata dall'elenco nella finestra **Società**. In entrambi i casi, verificare che il nome specificato nella procedura guidata di PowerApps corrisponda esattamente al testo contenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)], come `My Company`.

   Per nome utente e password, utilizzare il nome e la chiave del servizio di accesso Web specificata per l'account nella finestra **Utenti** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, il nome utente è *ADMIN* e la chiave del servizio di accesso Web utilizzata è *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Per ulteriori informazioni, vedere [Procedura: Gestire gli utenti e le autorizzazioni](ui-how-users-permissions.md).
6. Scegliere il pulsante **Crea** nella parte inferiore della pagina per procedere.

   In Flow verrà visualizzata una lista delle tabelle disponibili tramite [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le tabelle, o punti finali, indicano tutti i servizi Web pubblicati tramite [!INCLUDE[d365fin](includes/d365fin_md.md)].

   In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.
7. Scegliere i dati da utilizzare per in Flow.

A questo punto, è stata stabilita correttamente la connessione ai dati di Dynamics 365 e si è pronti per iniziare a creare la Flow. Per ulteriori informazioni, vedere la [Documentazione di Flow](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Vedi anche
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Procedura: Gestire gli utenti e le autorizzazioni](ui-how-users-permissions.md)    
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  

