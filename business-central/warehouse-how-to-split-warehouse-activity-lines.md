---
title: 'Procedura: Suddividere le righe attività di warehouse | Documenti Microsoft'
description: Nei prelievi, nei movimenti o negli stoccaggi warehouse, nonché nei prelievi e negli stoccaggi magazzino, vengono forniti suggerimenti circa le collocazioni per il prelievo o lo stoccaggio di articoli. Nella collocazione suggerita la quantità effettiva può non essere sufficiente o non vi è abbastanza spazio per stoccare la quantità richiesta. In questi casi è necessario suddividere la riga in modo che gli articoli ad essa corrispondenti vengano prelevati da o posti in più collocazioni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8a9fef52a67072e15f611162c0c038d92ebd4ff0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914712"
---
# <a name="split-warehouse-activity-lines"></a>Suddividere righe attività warehouse
Nei prelievi, nei movimenti o negli stoccaggi warehouse, nonché nei prelievi e negli stoccaggi magazzino, vengono forniti suggerimenti circa le collocazioni per il prelievo o lo stoccaggio di articoli. Nella collocazione suggerita la quantità effettiva può non essere sufficiente o non vi è abbastanza spazio per stoccare la quantità richiesta. In questi casi è necessario suddividere la riga in modo che gli articoli ad essa corrispondenti vengano prelevati da o posti in più collocazioni.  

La seguente procedura si applica ai documenti warehouse, ad esempio stoccaggio warehouse, movimentazione e righe prelievo oppure stoccaggio magazzino, movimentazione e righe prelievo.  

## <a name="to-split-warehouse-activity-lines"></a>Per suddividere righe attività warehouse  
1.  Aprire una riga attività warehouse in cui si sta tentando di gestire una quantità insufficiente.  
2.  Nel campo **Qtà da gestire** immettere la quantità ridotta che si è in grado di gestire.  
3.  Nella Scheda dettaglio **Righe** scegliere le azioni **Azioni**, **Funzioni** e **Dividi riga**. Verrà visualizzata una nuova riga, costituita da una copia di quella originale tranne per il fatto che il campo **Qtà da gestire** contiene il valore sottratto dalla riga originale.  
4.  Assegnare una collocazione appropriata alla nuova riga, nonché una zona se si utilizzano stoccaggi e prelievi guidati, oppure continuare a suddividere la riga fino a quando non si trovano le collocazioni appropriate per gestire l'intera quantità.  

> [!NOTE]  
>  Se per l'ubicazione vengono utilizzati stoccaggi e prelievi guidati e si procede alla suddivisione delle righe, è necessario avere familiarità con la warehouse ed essere in grado di scegliere una collocazione che corrisponda ai requisiti di immagazzinamento dell'articolo e che soddisfi i requisiti generali del documento di warehouse. Ad esempio, non è consigliabile suddividere una riga in un documento di prelievo e posizionare alcuni articoli nell'area di immagazzinamento a massa.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
