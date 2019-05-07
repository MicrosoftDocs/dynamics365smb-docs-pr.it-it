---
title: Impostazione di filtri per le basi di allocazione dinamica | Microsoft Docs
description: Il metodo di allocazione dinamica si basa su valori variabili. Ad esempio, il numero di dipendenti in un centro di costo o gli articoli venduti di un oggetto di costo in un determinato intervallo di tempo specifico. Esistono nove basi di allocazione predefinite e dodici intervalli di date dinamici. Si impostano filtri diversi a seconda della base di allocazione.
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
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 35f9a542d57bfe27c9a9ee48f4a41af7071cdd47
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "935498"
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
