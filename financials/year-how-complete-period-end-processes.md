---
title: "Attività facoltative per periodi di chiusura | Documenti Microsoft"
description: "In questo argomento vengono descritti i processi e le attività facoltativi per la chiusura dei periodi contabili in Financials."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: ddc2dbda549414a7beecf5f307c525b53166fa15
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Panoramica delle attività per la chiusura dei periodi contabili
In [!INCLUDE[d365fin](includes/d365fin_md.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere. In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.  

## <a name="general-ledger"></a>Contabilità generale
* Specificare periodi di registrazione a livello di sistema e specifici dell'utente.  

    Ciò specifica le date tra le quali è ammessa la registrazione. In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura. Per ulteriori informazioni, vedere [Procedura: Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).  
* Apportare tutte le rettifiche C/G necessarie.  
* Aggiornare e contabilizzare le registrazioni periodiche.  
  <!--* Process Consolidations-->
* Eseguire le situazioni contabili come segue:  
  * Aprire la finestra **Situazione contabile** e quindi scegliere l'azione **Stampa**.  

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

Cespiti
* Registrare tutti i costi di manutenzione che sono stati registrati tramite le registrazioni cespiti o le fatture.
* Registrare le rettifiche.
* Registrare la rivalutazione.
* Registrare l'ammortamento.
* Aggiornare e registrare le registrazioni periodiche cespiti.

Intercompany
* Elaborare transazioni Intercompany

## <a name="calculate-and-process-sales-tax"></a>Calcolare ed elaborare l'imposta di vendita.
* Completare le dichiarazioni fiscali.  

## <a name="see-also"></a>Vedi anche
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Chiusura registri](year-close-books.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

