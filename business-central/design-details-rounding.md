---
title: Dettagli di progettazione - Arrotondamento
description: Le differenze da arrotondamento possono verificarsi quando si valuta il costo di una riduzione di magazzino che viene misurata in una quantità diversa dal corrispondente aumento di magazzino.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Dettagli di progettazione: Arrotondamento
Le differenze da arrotondamento possono verificarsi quando si valuta il costo di una riduzione di magazzino che viene misurata in una quantità diversa dal corrispondente aumento di magazzino. Le differenze da arrotondamento vengono calcolate per tutti i metodi di costing quando si esegue il processo batch **Rettifica costo - Movimenti articoli**.  

 Quando si utilizza il metodo di costing medio, la differenza da arrotondamento viene calcolata e registrata su base movimento per movimento, cumulativa.  

 Quando si utilizza un metodo di costing diverso da Medio, la differenza da arrotondamento viene calcolata quando l'aumento di magazzino viene applicato completamente, ovvero quando la quantità residua dell'aumento di magazzino è uguale a zero. Una voce separata viene quindi creata per la differenza da arrotondamento e la data di registrazione di questo movimento di arrotondamento è la data di registrazione dell'ultimo movimento valorizzazione fatturazione dell'aumento di magazzino.  

## Esempio  
 Nel seguente esempio viene illustrato in che modo le differenze da arrotondamento vengono gestite rispettivamente per il metodo di costing medio e il metodo di costing diverso da quello medio. In entrambi i casi, il processo batch **Rettifica costo - Movimenti articoli** è stato eseguito.  

 Nella seguente tabella vengono mostrati i movimenti contabili articoli su cui si basa l'esempio.  

|Data di registrazione:|Quantità|Nr. movimento|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|02-01-20|-1|2|  
|03-01-20|-1|3|  
|04-01-20|-1|4|  

 Per un articolo che utilizza il metodo di costing medio, il residuo di arrotondamento (1/300) viene calcolato alla prima riduzione (numero di movimento 2) e trasferito in avanti al numero di movimento 3. Di conseguenza, il numero di movimento 3 viene valutato a –3,34.  

 Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

|Data di registrazione:|Quantità|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,34|3|3|  
|04-01-20|-1|-3,33|4|4|  

 Per un articolo che utilizza un metodo di costing diverso da Medio, il residuo di arrotondamento (0,01) viene calcolato quando la quantità residua per l'aumento di magazzino è pari a zero. La differenza da arrotondamento ha un movimento separato (numero 5).  

 Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

|Data di registrazione:|Quantità|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,33|3|3|  
|04-01-20|-1|-3,33|4|4|  
|01-01-20|0|-0,01|1|5|  

## Vedi anche  
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md) [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]