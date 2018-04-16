---
title: 'Dettagli di progettazione: Scostamento | Microsoft Docs'
description: "Lo scostamento è definito come la differenza tra il costo effettivo e il costo standard, come descritto nella formula seguente."
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
ms.openlocfilehash: 04faa28799288e272da93c60cbb90fa19fd190f0
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-variance"></a>Dettagli di progettazione: Scostamento
Lo scostamento è definito come la differenza tra il costo effettivo e il costo standard, come descritto nella formula seguente.  

 costo effettivo – costo standard = scostamento  

 Se il costo effettivo cambia, ad esempio, perché si registra un addebito articolo a una data successiva, la varianza verrà aggiornata di conseguenza.  

> [!NOTE]  
>  La rivalutazione non influisce sul calcolo dello scostamento, in quanto la rivalutazione modifica soltanto il valore di magazzino.  

## <a name="example"></a>Esempio  
 Nel seguente esempio viene illustrato in che modo viene calcolato lo scostamento per gli articoli acquistati. Si basa sullo scenario seguente:  

1. L'utente acquista un articolo a VL 90,00, ma il costo standard è di VL 100,00. Di conseguenza, lo scostamento di acquisto è VL 10,00.  
2. VL 10,00 viene accreditato sul conto scostamento acquisto.  
3. L'utente registra un addebito articolo di VL 20,00. Di conseguenza, il costo effettivo viene aumentato a VL 110,00 e il valore dello scostamento acquisto diventa VL 10,00.  
4. VL 20,00 viene addebitato sul conto scostamento acquisto. Di conseguenza, lo scostamento netto di acquisto diventa VL 10,00.  
5. L'utente rivaluta l'articolo da VL 100,00 a VL 70,00. La rivalutazione non influisce sul calcolo dello scostamento, solo sul valore di magazzino.  

   Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

   ![Calcolo scostamento acquisto](media/design_details_inventory_costing_11_purchase_variance.png "design_details_inventory_costing_11_purchase_variance")  

## <a name="determining-the-standard-cost"></a>Determinazione del costo standard  
 Il costo standard viene utilizzato durante il calcolo dello scostamento e dell'importo da capitalizzare. Poiché il costo standard può essere modificato nel tempo a causa di calcoli di aggiornamento manuali, è necessario individuare un momento nel tempo in cui il costo standard è fisso per il calcolo dello scostamento. Questo punto si presenta quando l'aumento di magazzino viene fatturato. Per articoli prodotti o assemblati, il punto in cui il costo standard è determinato è quando il costo viene rettificato.  

 Nella seguente tabella viene mostrato in che modo vengono calcolati i differenti dettagli dei costi per gli articoli prodotti e assemblati quando si utilizza la funzione Calcola costo standard.  

|Dettaglio costi|Articolo acquistato|Articolo prodotto/assemblato|  
|----------------|--------------------|------------------------------|  
|**Costo standard**||Costo materiale - Livello sing. + Costo capacità - Livello singolo + Costo conto lavoro - Liv. sing + Costo gen. cap. - Livello sing. + Costo gen. prod. - Livello sing.|  
|**Costo materiale - Livello sing.**|Costo unitario|![Equazione 1](media/design_details_inventory_costing_11_equation_1.png "design_details_inventory_costing_11_equation_1")|  
|**Costo capacità - Livello singolo**|Non applicabile|![Equazione 2](media/design_details_inventory_costing_11_equation_2.png "design_details_inventory_costing_11_equation_2")|  
|**Costo conto lavoro - Liv. sing.**|Non applicabile|![Equazione 3](media/design_details_inventory_costing_11_equation_3.png "design_details_inventory_costing_11_equation_3")|  
|**Costo gen. cap. - Livello sing.**|Non applicabile|![Equazione 4](media/design_details_inventory_costing_11_equation_4.png "design_details_inventory_costing_11_equation_4")|  
|**Costo gen. prod. - Livello sing.**|Non applicabile|(Costo materiale - Livello sing. + Costo capacità - Livello singolo + Costo conto lavoro - Liv. sing.) * Costo indiretto % / 100 + Coefficiente costi generali|  
|**Costo materiale - Ricalcolo**|Costo unitario|![Equazione 5](media/design_details_inventory_costing_11_equation_5.png "design_details_inventory_costing_11_equation_5")|  
|**Costo capacità - Ricalcolo**|Non applicabile|![Equazione 6](media/design_details_inventory_costing_11_equation_6.png "design_details_inventory_costing_11_equation_6")|  
|**Costo conto lavoro - Ricalcolo**|Non applicabile|![Equazione 7](media/design_details_inventory_costing_11_equation_7.png "design_details_inventory_costing_11_equation_7")|  
|**Costo gen. capacità - Ricalcolo**|Non applicabile|![Equazione 8](media/design_details_inventory_costing_11_equation_8.png "design_details_inventory_costing_11_equation_8")|  
|**Costo gen. prod.- Ricalcolo**|Non applicabile|![Equazione 9](media/design_details_inventory_costing_11_equation_9.png "design_details_inventory_costing_11_equation_9")|  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md) [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

