---
title: Come limitare e consentire l'utilizzo di un record | Documenti Microsoft
description: "Se si desidera limitare l'utilizzo di un record in determinate attività, ad esempio, fino all'approvazione del record, è possibile includere due risposte in un flusso di lavoro che controlla l'utilizzo del record."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a95eaa2f0933c6724b1e9158c675ad1a27e0ba2a
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a>Limitare e consentire l'utilizzo di un record
Se si desidera limitare l'utilizzo di un record in determinate attività, ad esempio, fino all'approvazione del record, è possibile includere due risposte in un flusso di lavoro che controlla l'utilizzo del record. Una risposta del flusso di lavoro limiterà l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro. Un'altra risposta del flusso di lavoro consentirà l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro. A tale scopo esistono due risposte nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Limitare l'utilizzo di un record.** e **Consentire l'utilizzo di un record.**.

> [!NOTE]  
>  La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] offre il supporto per limitare la registrazione di un record, l'esportazione come pagamento e la stampa come controllo. Per supportare altre restrizioni, è necessario che un partner Microsoft personalizzi il codice dell'applicazione.  

> [!NOTE]  
>  La funzionalità del flusso di lavoro per limitare e consentire l'utilizzo dei record non è correlata alla funzionalità per bloccare la registrazione di record relativi a fornitori, clienti e articoli.

Nella procedura riportata di seguito viene descritto come limitare la registrazione degli ordini di acquisto fino all'approvazione. Il nuovo flusso di lavoro si baserà sul modello esistente del flusso di lavoro di approvazione della fattura di acquisto.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Per creare una fase del flusso di lavoro che limiti la registrazione degli ordini di acquisto non approvati  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Workflow** creare un nuovo workflow denominato Workflow di approvazione ordine acquisto. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  
3. Scegliere l'azione **Copia flusso di lavoro da modello**.  
4. Scegliere il campo **Codice flusso di lavoro di origine** e nella pagina **Modelli del workflow** scegliere il modello Workflow di approvazione fattura acquisto.  

     Si noti che le prime due fasi del flusso di lavoro sono relative alla limitazione e all'autorizzazione dell'utilizzo delle fatture di acquisto. Continuare a modificare la condizione di evento nella prima fase del nuovo flusso di lavoro per specificare che si applica agli ordini di acquisto.  
5. Nella Scheda dettaglio **Fasi workflow** scegliere il campo **Condizioni evento** e per il filtro **Tipo di documento** scegliere **Ordine**.  
6. Continuare per modificare, eliminare o aggiungere altre fasi del flusso di lavoro per creare un processo aziendale che inizia limitando la registrazione degli ordini di acquisto non approvati.  

## <a name="see-also"></a>Vedi anche  
[Creare i workflow](across-how-to-create-workflows.md)   
[Workflow](across-workflow.md)   

