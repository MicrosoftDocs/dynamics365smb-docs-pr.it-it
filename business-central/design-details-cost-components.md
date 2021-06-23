---
title: 'Dettagli di progettazione: Componenti costo | Microsoft Docs'
description: I componenti di costo sono diversi tipi di costi che compongono il valore di un aumento o di una riduzione di magazzino.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1c1dd2eafb648a7c6053406ea3c931d6e7cecb76
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215360"
---
# <a name="design-details-cost-components"></a>Dettagli di progettazione: Componenti costo
I componenti di costo sono diversi tipi di costi che compongono il valore di un aumento o di una riduzione di magazzino.  

 Nella seguente tabella vengono mostrati i diversi componenti di costo e i relativi componenti secondari.  

|Componente di costo|Componente di costo secondario|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Costo diretto|Costo unitario (prezzo di acquisto diretto)|Costo che è possibile far risalire direttamente a un oggetto di costo.|  
|Costo diretto|Costo trasporto (addebito articolo)|Costo che è possibile far risalire direttamente a un oggetto di costo.|  
|Costo diretto|Costo assicurazione (addebito articolo)|Costo che è possibile far risalire direttamente a un oggetto di costo.|  
|Costo indiretto||Costo che non è possibile far risalire direttamente a un oggetto di costo.|  
|Scostamenti|Scostamento acquisto|Differenza tra costi effettivi e costi standard, che viene registrata per gli articoli solo utilizzando il metodo di costing **Standard**.|  
|Scostamenti|Scostamento materiali|Differenza tra costi effettivi e costi standard, che viene registrata per gli articoli solo utilizzando il metodo di costing **Standard**.|  
|Scostamenti|Scostamenti capacità|Differenza tra costi effettivi e costi standard, che viene registrata per gli articoli solo utilizzando il metodo di costing **Standard**.|  
|Scostamenti|Scost. conto lav.|Differenza tra costi effettivi e costi standard, che viene registrata per gli articoli solo utilizzando il metodo di costing **Standard**.|  
|Scostamenti|Scostamento costi gen. capacità|Differenza tra costi effettivi e costi standard, che viene registrata per gli articoli solo utilizzando il metodo di costing **Standard**.|  
|Scostamenti|Scostamento costi generali produzione|Differenza tra costi effettivi e costi standard, che viene registrata per gli articoli solo utilizzando il metodo di costing **Standard**.|  
|Rivalutazione||Ammortamento o rivalutazione del valore di magazzino corrente.|  
|Arrotondamento||Vengono calcolate le differenze causate dal modo in cui diminuisce la valutazione del magazzino.|  

> [!NOTE]  
>  I costi di assicurazione e di spedizione sono addebiti articoli che possono aggiunti al costo di un articolo in qualsiasi momento. Quando si esegue il processo batch **Rettifica costo - Movimenti articoli**, il valore delle riduzioni di magazzino correlate viene aggiornato di conseguenza.  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Scostamento](design-details-variance.md) [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]