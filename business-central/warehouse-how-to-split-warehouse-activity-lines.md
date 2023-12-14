---
title: Come suddividere le righe attività di warehouse
description: Scopri come suddividere le righe di attività di warehouse se la capacità disponibile in una collocazione suggerita non è sufficiente.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# <a name="split-warehouse-activity-lines"></a>Suddividere righe attività warehouse

Nei prelievi, nei movimenti o negli stoccaggi warehouse, nonché nei prelievi e negli stoccaggi magazzino, vengono forniti suggerimenti circa le collocazioni per il prelievo o lo stoccaggio di articoli. Nella collocazione suggerita la quantità effettiva può non essere sufficiente o non vi è abbastanza spazio per stoccare la quantità richiesta. In questi casi puoi suddividere la riga in modo che gli articoli ad essa corrispondenti vengano prelevati da o riposti in più collocazioni.  

La seguente procedura si applica ai seguenti documenti di warehouse:

* Stoccaggi warehouse
* Movimentazioni warehouse
* Prelievi warehouse
* Stoccaggi magazzino
* Movimenti di magazzino
* Prelievi magazzino  

## <a name="to-split-warehouse-activity-lines"></a>Per suddividere righe attività warehouse

1. Aprire una riga attività warehouse in cui si sta tentando di gestire una quantità insufficiente.  
2. Nel campo **Qtà da gestire** immetti la quantità ridotta che sei in grado di gestire.  
3. Nella Scheda dettaglio **Righe** scegliere le azioni **Azioni**, **Funzioni** e **Dividi riga**. Viene visualizzata una nuova riga. La riga è una copia di quella originale tranne per il fatto che il campo **Qtà da gestire** contiene il valore sottratto dalla riga originale.  
4. Assegna una collocazione e una zona se usi stoccaggi e prelievi diretti, oppure continua a suddividere la riga fino a quando non trovi le collocazioni appropriate per l'intera quantità.  

> [!NOTE]  
> Se per l'ubicazione vengono utilizzati stoccaggi e prelievi guidati e si procede alla suddivisione delle righe, è necessario avere familiarità con la warehouse ed essere in grado di scegliere una collocazione che corrisponda ai requisiti di immagazzinamento dell'articolo e che soddisfi i requisiti generali del documento di warehouse. Ad esempio, non è consigliabile suddividere una riga in un documento di prelievo e posizionare alcuni articoli nell'area di immagazzinamento a massa.  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
