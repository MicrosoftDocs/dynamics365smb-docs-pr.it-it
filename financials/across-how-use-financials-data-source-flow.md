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
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato
È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.  

> [!NOTE]  
>   È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Flow
1. Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com/en-us/), quindi accedere.
2. Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.
3. Nella finestra **I miei flussi** selezionare **Creare da Vuoto**.
4. Selezionare uno dei trigger [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibili dall'elenco dei trigger:  
    *Creazione di un record*,  
    *Eliminazione di un record*,  
    *Modifica di un record*,  
    *Approvazione di un cliente necessaria*,  
    *Approvazione batch registrazioni COGE necessaria*,  
    *Approvazione riga registrazioni COGE necessaria*,  
    *Approvazione articolo necessaria*,  
    *Approvazione di un documento di acquisto necessaria*,  
    *Approvazione di un documento di vendita necessaria*, o  
    *Approvazione di un fornitore necessaria*.
5. In Flow verrà visualizzata la richiesta per le informazioni necessarie per accedere ai dati di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se è stato selezionato uno dei seguenti trigger: *Creazione di un record*, *Modifica di un record* e *Eliminazione di un record* è necessario selezionare un nome di società e un nome di tabella. Con qualsiasi altro trigger, è richiesto soltanto il nome della società per connettersi.

   In Flow verrà visualizzata una lista delle società e delle tabelle disponibili tramite [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le tabelle, o punti finali, indicano tutti i servizi Web pubblicati tramite [!INCLUDE[d365fin](includes/d365fin_md.md)].

   In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.

A questo punto, è stata stabilita correttamente la connessione ai dati di Finance and Operations, Business edition e si è pronti per iniziare a creare un flusso. Per ulteriori informazioni, vedere la [Documentazione di Flow](https://flow.microsoft.com/documentation/getting-started/).

Per la risoluzione dei problemi di Microsoft Flow, vedere [Risoluzione dei problemi di integrazione con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Vedi anche
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)    
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  

