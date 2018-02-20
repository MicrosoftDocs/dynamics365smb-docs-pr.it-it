---
title: Impostazione di filtri per le basi di allocazione dinamica | Microsoft Docs
description: Il metodo di allocazione dinamica si basa su valori variabili. Ad esempio, il numero di dipendenti in un centro di costo o gli articoli venduti di un oggetto di costo in un determinato intervallo di tempo specifico. Esistono nove basi di allocazione predefinite e dodici intervalli di date dinamici. Si impostano filtri diversi a seconda della base di allocazione.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cd6aaf4ca0c1de1cea400ce5abe434f7c37040f9
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Impostazione di filtri per le basi di allocazione dinamica
Il metodo di allocazione dinamica si basa su valori variabili. Ad esempio, il numero di dipendenti in un centro di costo o gli articoli venduti di un oggetto di costo in un determinato intervallo di tempo specifico. Esistono nove basi di allocazione predefinite e dodici intervalli di date dinamici. Si impostano filtri diversi a seconda della base di allocazione.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Impostazione di filtri per le basi di allocazione dinamica  
 Nella tabella seguente vengono indicati i filtri possibili per le diverse basi di allocazione e i valori validi nei campi **Filtro nr.** e **Filtro gruppo**. Premere F1 nel campo **Codice filtro data** per leggere le descrizioni dettagliate.  

|**Base**|**Filtro nr.**|**Codice filtro data**|**Filtro centro di costo**|**Filtro oggetto di costo**|**Filtro gruppo**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Movimenti C/G|Conto C/G|Sì|Sì|Sì|N/D|  
|Movimenti budget C/G|Conto C/G|Sì|Sì|Sì|Nome budget C/G|  
|Movimenti del tipo di costo|Tipo Costo|Sì|Sì|Sì|N/D|  
|Movimenti budget costi|Tipo Costo|Sì|Sì|Sì|Nome Budget|  
|Nr. di impiegati|N/D|Sì|Sì|Sì|N/D|  
|Articoli venduti (qtà)|Nr. Articolo|Sì|Sì|Sì|Cat. reg. magazzino|  
|Articoli acquistati (qtà)|Nr. Articolo|Sì|Sì|Sì|Cat. reg. magazzino|  
|Articoli venduti (importo)|Nr. Articolo|Sì|Sì|Sì|Cat. reg. magazzino|  
|Articoli acquistati (importo)|Nr. articolo|Sì|Sì|Sì|Cat. reg. magazzino|  

## <a name="see-also"></a>Vedi anche  
 [Esempio di scenario: definizione delle allocazioni dinamiche in base agli articoli venduti](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Impostare origini e destinazioni dell'allocazione](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)

