---
title: Definizione e allocazione dei costi | Microsoft Docs
description: "Con le allocazioni costi è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. È possibile definire tutte le allocazioni necessarie."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 050b0bd997629ca189cfbe035e361de7a252d079
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="defining-and-allocating-costs"></a>Definizione e allocazione dei costi
Con le allocazioni costi è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. È possibile definire tutte le allocazioni necessarie. Ogni allocazione è costituita da:  

-   Un'origine allocazione.  
-   Uno o più destinazioni di allocazione.  

L'origine dell'allocazione stabilisce quali costi devono essere assegnati, mentre le destinazioni di allocazione determinano dove i costi devono essere allocati. Ad esempio, i costi per il tipo di costo Elettricità e riscaldamento sono un'origine di allocazione. Allocare tutti i costi del riscaldamento e dell'elettricità a tre centri di costo: Workshop, Produzione e Vendite. Questi centri di costi sono le destinazioni di allocazione.  

Per ogni origine di allocazione, è possibile definire un livello di allocazione, un periodo di validità e una variante come identificatore di gruppo. È possibile utilizzare un processo batch per impostare i filtri per selezionare le definizioni di allocazione e quindi eseguire le allocazioni costi automaticamente.  

Per ogni destinazione di allocazione, è possibile definire una base di allocazione. La base di allocazione può essere statica o dinamica.  

-   Le basi di allocazioni statiche sono basate su un valore definito, come la superficie o un rapporto di allocazione stabilito, ad esempio 5:2:4.  
-   Le basi di allocazioni dinamiche dipendono da valori variabili, quali il numero di impiegati in un centro di costo o i ricavi di vendite di un oggetto di costo in un determinato periodo di tempo.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

|A|Vedere|  
|--------|---------|  
|Impostare origini e destinazioni dell'allocazione.|[Procedura: Impostare origini e destinazioni dell'allocazione](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Impostare vari filtri per le basi di allocazione dinamica.|[Impostazione di filtri per le basi di allocazione dinamica](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Visualizzare un esempio su come definire un'allocazione statica.|[Esempio di scenario: Definizione delle allocazioni statiche in base al rapporto di allocazione](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Visualizzare un esempio su come definire un'allocazione dinamica.|[Esempio dello scenario: definizione delle allocazioni dinamiche in base agli articoli venduti](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Vedi anche  
 [Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)   
 [Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)   
 [Contabilizzazione dei costi](finance-manage-cost-accounting.md)   
 [Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)   
 [Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)

