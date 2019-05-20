---
title: Come impostare metodi di ammortamento alternativi
description: I metodi di ammortamento alternativi includono l'ammortamento anticipato, accelerato e ridotto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: aa54049b88a2be889e44eece12d85eb1b862503b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246101"
---
# <a name="set-up-alternate-depreciation-methods"></a>Impostare metodi di ammortamento alternativi
Di seguito sono indicati alcuni metodi di ammortamento alternativi:  

- Ammortamento anticipato.  
- Ammortamento accelerato.  
- Ammortamento ridotto.  

Per impostare questi metodi di ammortamento, è necessario creare tabelle di ammortamento.  

## <a name="to-set-up-alternate-depreciation-methods"></a>Per impostare metodi di ammortamento alternativi  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Tabelle ammortamento**, quindi scegliere il collegamento correlato.  
2.  Nella pagina **Lista tabelle ammortamento** scegliere l'azione **Nuovo**.  
3.  Nella Scheda Dettaglio **Generale** compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Codice**|Codice per la tabella di ammortamento.|  
    |**Description**|Descrizione per la tabella di ammortamento.|  
    |**Durata periodo**|Durata del periodo a cui si applicherà ogni riga della tabella di ammortamento.|  
    |**Nr. totale di unità**|Numero totale di unità che si prevede che il cespite produrrà nella sua durata.|  

4.  Nella Scheda dettaglio **Righe** compilare i campi come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**% ammortamento periodo**|Percentuale di ammortamento da applicare al periodo.|  
    |**Nr. unità nel periodo**|Numero di unità prodotte dal cespite a cui si applica la tabella di ammortamento.|  
    |**% anticipata**|Percentuale di ammortamento anticipata.|  
    |**% accelerata/ridotta**|Percentuale di ammortamento effettiva.|  

5.  Nel campo **% totale ammortamento** immettere la percentuale totale di ammortamento.  
6.  Scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedi anche  
 [Impostare l'ammortamento dei cespiti](../../fa-how-setup-depreciation.md)   
 [Cespiti italiani](italian-fixed-assets.md)   
 [Creare più schede cespite](how-to-create-multiple-fixed-asset-cards.md)   
 [Impostazione dell'ammortamento compresso dei cespiti](how-to-set-up-compressed-depreciation-of-fixed-assets.md)   
 [Stampare report dei registri dei beni ammortizzabili](how-to-print-depreciation-book-reports.md)