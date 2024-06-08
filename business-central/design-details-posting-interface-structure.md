---
title: Dettagli di progettazione - Struttura dell'interfaccia di registrazione
description: Questo argomento fornisce una sintesi delle procedure globali e i dettagli di progettazione nella struttura dell'interfaccia di registrazione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Dettagli di progettazione: struttura dell'interfaccia di registrazione
Nella struttura dell'interfaccia di registrazione di [!INCLUDE[prod_short](includes/prod_short.md)] esistono diverse procedure globali che utilizzano la stessa struttura:  
  
* Codice della procedura di chiamata di RunWithoutCheck e di RunWithCheck – interfaccia generica di registrazione per riga registrazioni generali.  
* CustPostApplyCustLedgEntry – registrare il collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati.  
* VendPostApplyVendLedgEntry – registrare il collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati.  
* UnapplyCustLedgEntry – registrare l'annullamento del collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati  
* UnapplyVendLedgEntry – registrare l'annullamento del collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati  
  
## Vedi anche  
[Dettagli di progettazione: struttura del motore di registrazione](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]