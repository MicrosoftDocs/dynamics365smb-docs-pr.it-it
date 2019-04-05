---
title: "Dettagli di progettazione: Struttura dell'interfaccia di registrazione | Microsoft Docs"
description: Questo argomento fornisce una sintesi delle procedure globali nella struttura dell'interfaccia di registrazione.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 236cbcc45ccca23905dcb79a491236c80b2bdebf
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801562"
---
# <a name="design-details-posting-interface-structure"></a>Dettagli di progettazione: struttura dell'interfaccia di registrazione
Nella struttura dell'interfaccia di registrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] esistono diverse procedure globali che utilizzano la stessa struttura:  
  
* Codice della procedura di chiamata di RunWithoutCheck e di RunWithCheck – interfaccia generica di registrazione per riga registrazioni COGE.  
* CustPostApplyCustLedgEntry – registrare il collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati.  
* VendPostApplyVendLedgEntry – registrare il collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati.  
* UnapplyCustLedgEntry – registrare l'annullamento del collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati  
* UnapplyVendLedgEntry – registrare l'annullamento del collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: struttura del motore di registrazione](design-details-posting-engine-structure.md)