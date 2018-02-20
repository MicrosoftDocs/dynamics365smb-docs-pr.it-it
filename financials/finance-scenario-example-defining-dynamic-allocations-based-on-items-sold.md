---
title: Esempio di scenario - Definizione delle allocazioni dinamiche in base agli articoli venduti | Documenti Microsoft
description: In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica.
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
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Esempio dello scenario: definizione delle allocazioni dinamiche in base agli articoli venduti
In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica. Nell'esempio è possibile modificare l'assegnazione dinamica dei costi per il centro di costo VENDITE per supportare il nuovo oggetto di costo ATTREZZATURA IT. I numeri degli articoli dei colli di ATTREZZATURA IT sono inclusi nell'intervallo compreso tra 8904-W e 8924-W. Utilizzare le cifre di vendita dell'anno precedente per calcolare la quota. L'allocazione viene registrata nel tipo di costo di supporto 9903.  

> [!NOTE]  
>  Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Per definire le allocazioni dinamiche in base agli articoli venduti nell'anno precedente  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Allocazioni costi**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Allocazione costi** scegliere l'azione **Nuovo**.  
3.  Nel campo **ID** premere INVIO o immettere un ID.  
4.  Nel campo **Livello** immettere **1**.  
5.  Nei campi **Data di inizio validità** e **Data di fine validità**, immettere le date appropriate.  
6.  Nel campo **Codice centro di costo** immettere **VENDITE**.  
7.  Nel campo **Importo dare in tipo di costo** immettere il tipo di costo **9903**.  
8.  Nel campo **Tipo di costo di destinazione** immettere il tipo di costo **9903**.  
9. Nel campo **Oggetto di costo di destinazione** selezionare **Nuovo** per creare un nuovo oggetto di costo ATTREZZATURA IT e compilare i campi in base alle esigenze. Selezionare **ATTREZZATURA IT**. Lasciare vuoto il campo **Centro di costo di destinazione**.  
10. Nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi accumulati.  
11. Nel campo **Base** selezionare la base di allocazione **Articoli venduti (importo)**.  
12. Nel campo **Filtro nr.** immettere **8904-W..8924-W**.  
13. Nel campo **Codice filtro data**, immettere **Anno Precedente**.  
14. Per calcolare la quota, scegliere l'azione **Calcola chiave di allocazione**.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] In  vengono utilizzate le cifre di vendita degli anni precedenti per calcolare una quota di 1.596,50 VL con il 100% dei colli di ATTREZZATURA IT. Pertanto, tutti gli articoli venduti nell'ultimo anno verranno assegnati all'oggetto di costo ATTREZZATURA IT.  

## <a name="see-also"></a>Vedi anche  
 [Impostazione di filtri per le basi di allocazione dinamica](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Impostare origini e destinazioni dell'allocazione](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)   
 [Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)   
 [Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)

