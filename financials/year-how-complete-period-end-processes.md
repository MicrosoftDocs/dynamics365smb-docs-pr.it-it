---
title: Periodi di chiusura | Documenti Microsoft
description: Vengono illustrati i processi per completare la chiusura di un periodo.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 03/21/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1d0af3dbc94c32447facfbd24747ddc140cc1691
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="closing-periods"></a>Periodi di chiusura
In [!INCLUDE[d365fin](includes/d365fin_md.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere. In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.  

## <a name="general-ledger"></a>Contabilità generale
* Specificare periodi di registrazione a livello di sistema e specifici dell'utente.  

    Ciò specifica le date tra le quali è ammessa la registrazione. In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura. Per ulteriori informazioni, vedere [Procedura: Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).  
* Apportare tutte le rettifiche C/G necessarie.  
* Aggiornare e contabilizzare le registrazioni periodiche.  
  <!--* Process Consolidations-->
* Eseguire le situazioni contabili come segue:  
  * Aprire la finestra **Situazione contabile** e scegliere l'azione **Stampa**.  

## <a name="sales-and-receivables"></a>Contabilità clienti
* Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.  
* Contabilizzare tutte le registrazioni incassi.  
* Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità clienti.  
* Riconciliare i crediti v/clienti nella contabilità generale.  
* Eseguire il processo batch **Elimina ord. vendita fatturati**.  

## <a name="purchases-and-payables"></a>Contabilità fornitori
* Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.  
* Contabilizzare tutte le registrazioni pagamenti.  
* Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità fornitori.  
* Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.  
* Eseguire il processo batch **Elimina ordini acquisto fatturati**.  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a>Calcolare ed elaborare l'imposta di vendita.
* Completare le dichiarazioni fiscali.  

## <a name="see-also"></a>Vedi anche
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Chiusura registri](year-close-books.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

