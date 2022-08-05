---
title: Come limitare e consentire l'utilizzo di un record
description: Se vuoi limitare l'utilizzo di un record, puoi includere due risposte in un flusso di lavoro che controlla l'utilizzo del record.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130147"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Limitare e consentire l'utilizzo di un record

Se si desidera limitare l'utilizzo di un record in determinate attività, ad esempio, fino all'approvazione del record, è possibile includere due risposte in un flusso di lavoro che controlla l'utilizzo del record. Una risposta del flusso di lavoro limiterà l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro. Un'altra risposta del flusso di lavoro consentirà l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro. Esistono due risposte nella versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)] per questo scopo: **Aggiungere limitazione record** e **Rimuovere limitazione record**.

> [!NOTE]  
> La versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)] offre il supporto per limitare la registrazione di un record, l'esportazione come pagamento e la stampa come controllo. Per supportare altre restrizioni, è necessario che un partner Microsoft personalizzi il codice dell'applicazione.  

> [!NOTE]  
> La funzionalità del flusso di lavoro per limitare e consentire l'utilizzo dei record non è correlata alla funzionalità per bloccare la registrazione di record relativi a fornitori, clienti e articoli.

Nella procedura riportata di seguito viene descritto come limitare la registrazione degli ordini di acquisto fino all'approvazione. Il nuovo flusso di lavoro si baserà sul modello esistente del flusso di lavoro di approvazione della fattura di acquisto.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Per creare una fase del flusso di lavoro che limiti la registrazione degli ordini di acquisto non approvati

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Nella pagina **Workflow** scegliere l'azione **Nuovo workflow da modello**. Per ulteriori informazioni, vedi [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).
3. Nella pagina **Modelli del workflow**, seleziona il modello *Flusso di lavoro approvazione ordine acquisto*.  

   Si noti che le prime due fasi del flusso di lavoro sono relative alla limitazione e all'autorizzazione dell'utilizzo delle fatture di acquisto. Continuare a modificare la condizione di evento nella prima fase del nuovo flusso di lavoro per specificare che si applica agli ordini di acquisto.  
4. Nella Scheda dettaglio **Fasi workflow** scegli il campo **Condizione** per il primo passaggio e per il filtro **Tipo di documento** scegli **Ordine**.  
5. Continuare per modificare, eliminare o aggiungere altre fasi del flusso di lavoro per creare un processo aziendale che inizia limitando la registrazione degli ordini di acquisto non approvati.  

## <a name="see-also"></a>Vedere anche

[Creare i workflow](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]