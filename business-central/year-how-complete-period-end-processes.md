---
title: Attività facoltative per periodi di chiusura
description: In questo argomento vengono descritti i processi e le attività facoltativi per la chiusura dei periodi contabili in Business Central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/29/2022
ms.author: jswymer
---
# Panoramica delle attività per la chiusura dei periodi contabili

In [!INCLUDE[prod_short](includes/prod_short.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere. In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.  

## Contabilità generale

* Specificare periodi di registrazione a livello di sistema e specifici dell'utente.  

    Ciò specifica le date tra le quali è ammessa la registrazione. In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura. Per ulteriori informazioni vedi [Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).  
* Apporta tutte le rettifiche di contabilità generale (C/G) necessarie.  
* Aggiorna e contabilizza le registrazioni periodiche.  
  <!--* Process Consolidations-->
* Esegui i report finanziari come segue:  
  * Apri la pagina **Report finanziari** e quindi scegli l'azione **Stampa**.  

## Contabilità clienti

* Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.  
* Contabilizzare tutte le registrazioni incassi.  
* Aggiorna e registra le registrazioni periodiche correlate alla contabilità clienti.  
* Riconciliare i crediti v/clienti nella contabilità generale.  
* Eseguire il processo batch **Elimina ord. vendita fatturati**.  

## Contabilità fornitori

* Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.  
* Contabilizzare tutte le registrazioni pagamenti.  
* Aggiorna e registra le registrazioni periodiche correlate alla contabilità fornitori.  
* Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.  
* Eseguire il processo batch **Elimina ordini acquisto fatturati**.  

## Cespiti

* Registra tutti i costi di manutenzione che sono stati registrati tramite le registrazioni cespiti o le fatture.
* Registrare le rettifiche.
* Registrare la rivalutazione.
* Registrare l'ammortamento.
* Aggiornare e registrare le registrazioni periodiche cespiti.

## Interaziendale

* Elabora le transazioni Intercompany.

## Calcolare ed elaborare l'IVA

* Completa le dichiarazioni fiscali.  

## Vedere anche

[Chiusura di anni e periodi](year-close-years-periods.md)  
[Chiusura registri](year-close-books.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
