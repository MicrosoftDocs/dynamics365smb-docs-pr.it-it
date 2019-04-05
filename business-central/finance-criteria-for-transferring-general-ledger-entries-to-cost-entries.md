---
title: Criteri per trasferire movimenti C/G ai movimenti di costi | Microsoft Docs
description: È importante comprendere i criteri per trasferire i movimenti C/G nei movimenti di costi. Durante il trasferimento, il processo batch **Trasferisci movimenti C/G a CA** utilizza i seguenti criteri per determinare se e come i movimenti C/G vengono trasferiti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6e5fcfedbb899633f61c05b0b8b5ec8125112d65
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801279"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Criteri per trasferire movimenti C/G ai movimenti di costi
È importante comprendere i criteri per trasferire i movimenti C/G nei movimenti di costi. Durante il trasferimento, il processo batch **Trasferisci movimenti C/G a CA** utilizza i seguenti criteri per determinare se e come i movimenti C/G vengono trasferiti.  

I movimenti C/G vengono trasferiti nei seguenti casi:  

-   Ai movimenti sono associati valori dimensioni che corrispondono a un centro di costo o un oggetto di costo.  
-   Ai movimenti sono associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo. Per questi movimenti, il centro di costo ha la precedenza. Questo consente di evitare una situazione in cui un tipo di costo viene visualizzato sia in un oggetto di costo sia in un centro di costo, venendo pertanto conteggiato due volte nelle statistiche.  
-   Il numero di documento nei movimenti è vuoto, pertanto verrà visualizzato con un numero di documento pari a 0000 nei movimenti di costo.  
-   I movimenti vengono trasferiti in un tipo di costo che consente movimenti combinati e tali movimenti vengono trasferiti come movimento combinato mensilmente o giornalmente.  

I movimenti C/G non vengono trasferiti nei seguenti casi:  

-   Ai movimenti sono associati valori dimensioni che non corrispondono a un centro di costo o un oggetto di costo.  
-   Ai movimenti è associato un importo pari a zero.  
-   Ai movimenti è associato un conto di contabilità generale che è stato eliminato.  
-   Ai movimenti è associato un conto di contabilità generale che non è di tipo **Conto economico**.  
-   Ai movimenti è associato un conto di contabilità generale a cui non è assegnato un tipo di costo.  
-   I movimenti hanno una data di registrazione anteriore alla **Data inizio per trasferimento CG**.  
-   Registrazione dei movimenti con data chiusura completata. Si tratta in genere di movimenti che reimpostano il saldo del conto economico alla fine dell'anno.  

## <a name="see-also"></a>Vedi anche  
[Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
 [Trasferire movimenti C/G a movimenti di costi](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)   
 [Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
