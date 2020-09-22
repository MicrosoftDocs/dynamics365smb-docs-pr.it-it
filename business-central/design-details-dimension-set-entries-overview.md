---
title: Sintesi movimenti set di dimensioni | Microsoft Docs
description: In questo argomento viene descritto il modo in cui i movimenti set di dimensioni vengono memorizzati e registrati in Dynamcis 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b9b69b539228e92776e1a7ee4c2fb491b20c1a15
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787998"
---
# <a name="dimension-set-entries-overview"></a>Sintesi movimenti set di dimensioni
In questo argomento viene descritto il modo in cui i movimenti set di dimensioni vengono memorizzati e registrati in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="dimension-sets"></a>Set di dimensioni  
Un set di dimensioni è una combinazione univoca di valori dimensioni. Viene archiviato come movimenti set di dimensioni nel database. Ogni movimento set di dimensioni rappresenta un valore dimensioni singolo. Il set di dimensioni è identificato da un ID set di dimensioni comune assegnato a ogni movimento set di dimensioni che appartiene al set di dimensioni.  

Nel seguente esempio viene mostrato un set di dimensioni in cui sono presenti tre relativi movimenti. Il set di dimensioni è identificato da un ID set di dimensioni, vale a dire 108.  

|ID set di dimensioni|Codice Dimensione:|Codice Valore Dimensioni:|Nome valore dimensioni|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|AREA|70|Nord America|  
|108|GRUPPOBUSINES|HOME|Home|  
|108|REPARTO|VENDITE|Vendite|  

## <a name="dimension-set-entries"></a>Movimenti set di dimensioni  
I set di dimensioni vengono archiviati nella tabella **Movimento set di dimensioni** come movimenti di set di dimensioni con lo stesso ID set di dimensioni.  

![Flusso dei movimenti set di dimensioni](media/dimensionentrynav7.png "Flusso dei movimenti set di dimensioni")  

Quando si crea una nuova riga di registrazione, testata del documento o riga documento, è possibile specificare una combinazione di valori dimensioni. Anziché archiviare esplicitamente ogni valore dimensioni nel database, viene assegnato un ID set di dimensioni alla riga di registrazione, alla testata del documento o alla riga del documento per specificare il set di dimensioni.  

Quando si modifica e si chiude la pagina **Modifica movimenti set di dimensioni** , viene eseguito un controllo per verificare se la combinazione dei valori dimensioni esiste come set di dimensioni nella tabella. Se la combinazione si verifica nella tabella, l'ID set di dimensioni corrispondente viene assegnato alla riga di registrazione, alla testata del documento o alla riga del documento. In caso contrario, un nuovo set di dimensioni viene aggiunto alla tabella e il nuovo ID set di dimensioni viene assegnato alla riga di registrazione, alla testata del documento o alla riga del documento.

## <a name="codeunit-408-dimension-management"></a>Gestione dimensioni codeunit 408
Gestione dimensioni codeunit 408 è una libreria di funzioni che gestisce attività comuni correlate alle dimensioni, come la copia da una tabella a un'altra o da un documento a un altro.

## <a name="performance-improvement"></a>Miglioramento delle prestazioni  
Archiviando i set di dimensioni una volta nel database, lo spazio di quest'ultimo viene mantenuto e le prestazioni globali vengono migliorate.  

## <a name="see-also"></a>Vedere anche  
[Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md)   
[Dettagli di progettazione: Struttura della tabella](design-details-table-structure.md)   
[Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md)   
