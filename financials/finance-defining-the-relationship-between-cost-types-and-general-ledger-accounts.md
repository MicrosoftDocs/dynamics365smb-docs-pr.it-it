---
title: "Definizione della relazione tra i tipi di costo e i conti di contabilità generale | Microsoft Docs"
description: "Informazioni su come definire la relazione tra il tipo di costo e il conto di contabilità generale."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definizione della relazione tra i tipi di costo e i conti di contabilità generale
La relazione tra il tipo di costo e il conto di contabilità generale viene creata nel tipo di costo e nel conto di contabilità generale.  

* Tramite il campo **Intervallo conti CG** della tabella **Tipo costo** è possibile stabilire quali conti di contabilità generale appartengono a un tipo di costo.  
* Con il campo **Nr. tipo di costo** nel piano dei conti è possibile stabilire il tipo di costo a cui appartiene un conto di contabilità generale.  

Questi due campi vengono compilati automaticamente quando si utilizza la funzione **Ottieni tipi costo da piano dei conti**.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relazione tra i conti di contabilità generale e i tipi di costo  
Tra i conti di contabilità generale e i tipi di costo esiste una relazione n:1. A un tipo di costo possono appartenere più conti di contabilità generale, ma ognuno di questi appartiene a un solo tipo di costo. Nella seguente tabella vengono descritti i dettagli delle relazioni.  

|Relazione|**Intervallo conti C/G**|**Nr. tipo di costo**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Un conto di contabilità generale per ogni tipo di costo|Un conto di contabilità generale|Un tipo di costo|  
|Più conti di contabilità generale per un tipo di costo|Intervallo di conti di contabilità generale, ad esempio da 7110 a 7193, per ciascun conto di contabilità generale|Per ciascun conto di contabilità generale nell'intervallo, esiste un solo tipo di costo|  
|Tipi di costo senza conti di contabilità generale corrispondenti|<Empty>||  
|Conti di contabilità generale i cui movimenti non saranno trasferiti||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Tipi di costo senza una relazione con la contabilità generale  
Un tipo di costo non può avere una relazione con i conti di contabilità generale se una delle seguenti condizioni è vera:  

* I conti per la contabilità operativa, ad esempio il calcolo interessi e l'ammortamento, vengono ricavati solo dalla contabilità operativa.  
* I tipi di costo di supporto, ad esempio i tipi 9901, 9902 e 9903 nel database di [!INCLUDE[d365fin](includes/d365fin_md.md)], vengono utilizzati come dare e avere per le allocazioni.  
* Il conto di supporto, 9920 nel database di [!INCLUDE[d365fin](includes/d365fin_md.md)], contiene i ratei effettivi che mostrano la differenza tra i costi e le spese della contabilità generale.  

## <a name="see-also"></a>Vedi anche  
[Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
[Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)   
[Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

