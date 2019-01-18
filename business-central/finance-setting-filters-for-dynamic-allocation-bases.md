---
title: Impostazione di filtri per le basi di allocazione dinamica | Microsoft Docs
description: Il metodo di allocazione dinamica si basa su valori variabili. Ad esempio, il numero di dipendenti in un centro di costo o gli articoli venduti di un oggetto di costo in un determinato intervallo di tempo specifico. Esistono nove basi di allocazione predefinite e dodici intervalli di date dinamici. Si impostano filtri diversi a seconda della base di allocazione.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: fcf97328900bb21a85be51452b9e86da8398d195
ms.contentlocale: it-it
ms.lasthandoff: 11/20/2018

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
|Articoli acquistati (importo)|Nr. articolo|Sì|Sì|Sì|Gruppo registrazione magazzino|  

## <a name="see-also"></a>Vedi anche  
[Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)

