---
title: Trasferimento automatico e movimenti combinati | Microsoft Docs
description: "Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata. È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo. Nella seguente tabella vengono illustrate le diverse opzioni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4f1bcf009b397438bb302a16a23be2f4638cefc4
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a>Trasferimento automatico e movimenti combinati
Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata. È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo. Nella seguente tabella vengono illustrate le diverse opzioni.  

|Cumula movimenti|Descrizione|  
|---------------------|-----------------|  
|Nessuno|Ogni movimento C/G viene trasferito singolarmente al tipo di costo corrispondente.|  
|Giorno|I movimenti C/G con la stessa data di registrazione vengono trasferiti come un unico movimento nel tipo di costo corrispondente.|  
|Mese|Tutti i movimenti C/G dello stesso mese di calendario vengono trasferiti come un unico movimento nel tipo di costo corrispondente.|  

> [!IMPORTANT]  
>  Se si è selezionata la casella di controllo **Trasferimento automatico da CG** nella finestra **Setup contabilità industriale**, [!INCLUDE[d365fin](includes/d365fin_md.md)] aggiorna la contabilità dopo ogni registrazione nella contabilità generale. Le entità combinate non sono possibili.  

## <a name="see-also"></a>Vedi anche  
 [Trasferire movimenti C/G a movimenti di costi](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Criteri per trasferire movimenti C/G ai movimenti di costi](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Risultati del trasferimento](finance-results-of-the-transfer.md)   
 [Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

