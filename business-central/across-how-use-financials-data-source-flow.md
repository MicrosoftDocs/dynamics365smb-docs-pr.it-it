---
title: Connettere i dati a Flow| Documenti Microsoft
description: "È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f79bd9a5e3f79d4366a1a43411fe39942ac4e4f
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato
È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.

> [!NOTE]
> Oltre a Microsoft Flow, è possibile utilizzare la funzionalità Workflow in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si noti che sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso creato con Microsoft Flow viene aggiunta all'elenco dei modelli di flusso in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
>   È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Flow
1. Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com/en-us/), quindi accedere.
2. Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.
3. Sono disponibili 2 modi per creare un flusso: **Crea da modello** e **Crea da vuoto**. Un modello è un flusso predefinito che è stato creato per l'utente.  Per utilizzare un modello, selezionarlo semplicemente e creare una connessione per ogni servizio utilizato dal modello. Un modello vuoto consente di creare un nuovo flusso completamente da zero.
4. Per creare da un modello vuoto, nella pagina **I miei flussi** selezionare l'opzione **Crea da vuoto**.
5. Cercare il connettore **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Selezionare uno dei trigger [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibili dall'elenco dei trigger:  
    *Approvazione di un cliente necessaria*,  
    *Approvazione batch registrazioni COGE necessaria*,  
    *Approvazione riga registrazioni COGE necessaria*,  
    *Approvazione articolo necessaria*,  
    *Approvazione di un documento di acquisto necessaria*,  
    *Approvazione di un documento di vendita necessaria*, o  
    *Approvazione di un fornitore necessaria*.
7. Il flusso richiederà di selezionare una società all'interno del tenant [!INCLUDE[d365fin](includes/d365fin_md.md)], nonché tutti i termini nei dati che si desidera ascoltare.

A questo punto, è stata stabilita correttamente la connessione ai dati di Business Central e si è pronti per iniziare a creare il flusso.

8. Per creare da un modello, selezionare l'opzione **Crea da modello**.
9. Cercare i modelli **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
10. Selezionare uno dei modelli disponibili dall'elenco.  
    *Richiesta di approvazione per ordine di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per offerta di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per fattura di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per nota di credito di vendita Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per cliente Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per acquisto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per fattura d'acquisto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per nota di credito di acquisto Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per articolo Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per fornitore Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per batch registrazioni COGE Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Richiesta di approvazione per righe registrazioni COGE Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
11. Flow richiederà la selezione di una società presso il tenant [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Poiché ogni fase del flusso è indipendente dalla successiva, è possibile che sia necessario definire la società più volte quando si utilizza un modello di flusso di [!INCLUDE[d365fin_md](includes/d365fin_md.md)].

Per ulteriori informazioni, vedere la [Documentazione di Flow](https://docs.microsoft.com/en-us/flow/getting-started).

Per la risoluzione dei problemi di Microsoft Flow, vedere [Risoluzione dei problemi di integrazione con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Vedi anche
[Introduzione](product-get-started.md)  
[Workflow](across-workflow.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)   
[Gestire flussi di lavoro [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Setup utente approvazione](across-how-to-set-up-approval-users.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  

