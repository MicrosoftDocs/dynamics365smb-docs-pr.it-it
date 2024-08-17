---
title: Attività facoltative per i periodi di chiusura
description: In questo articolo vengono descritti i processi e le attività facoltativi per la chiusura dei periodi contabili in Business Central.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/02/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="overview-of-tasks-to-close-accounting-periods"></a>Panoramica delle attività per i periodi contabili Chiudi

[!INCLUDE[prod_short](includes/prod_short.md)] non ti obbliga a Chiudi mestruazioni, tuttavia ci sono molte attività di fine ciclo (fine mese) che puoi fare. Questo articolo fornisce una panoramica dei processi e delle attività facoltativi per i periodi di chiusura.  

## <a name="general-ledger"></a>Contabilità generale

* Specificare periodi di registrazione a livello di sistema e specifici dell'utente.  

    Ciò specifica le date tra le quali è ammessa la registrazione. A seconda della tua attività, potresti voler consentire la pubblicazione all'inizio del periodo o verso la fine. Per ulteriori informazioni vedi [Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).  
* Apporta tutte le rettifiche di contabilità generale (C/G) necessarie.  
* Aggiorna e contabilizza le registrazioni periodiche.  
  <!--* Process Consolidations-->
* Esegui i report finanziari come segue:  
  * Apri la pagina **Report finanziari** e quindi scegli l'azione **Stampa**.  

## <a name="sales-and-receivables"></a>Contabilità clienti

* Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.  
* Contabilizzare tutte le registrazioni incassi.  
* Aggiorna e registra le registrazioni periodiche correlate alla contabilità clienti.  
* Riconciliare i crediti v/clienti nella contabilità generale.  
* Eseguire il processo batch **Elimina ord. vendita fatturati**.  

## <a name="purchases-and-payables"></a>Contabilità fornitori

* Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.  
* Contabilizzare tutte le registrazioni pagamenti.  
* Aggiorna e registra le registrazioni periodiche correlate alla contabilità fornitori.  
* Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.  
* Eseguire il processo batch **Elimina ordini acquisto fatturati**.  

## <a name="fixed-assets"></a>Cespiti

* Registra tutti i costi di manutenzione che sono stati registrati tramite le registrazioni cespiti o le fatture.
* Registrare le rettifiche.
* Registrare la rivalutazione.
* Registrare l'ammortamento.
* Aggiornare e registrare le registrazioni periodiche cespiti.

## <a name="intercompany"></a>Interaziendale

* Elabora le transazioni Intercompany.

## <a name="calculate-and-process-sales-tax"></a>Calcolare ed elaborare l'IVA

* Completa le dichiarazioni fiscali.  

## <a name="see-also"></a>Vedere anche

[Chiusura di anni e periodi](year-close-years-periods.md)  
[Chiusura registri](year-close-books.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
