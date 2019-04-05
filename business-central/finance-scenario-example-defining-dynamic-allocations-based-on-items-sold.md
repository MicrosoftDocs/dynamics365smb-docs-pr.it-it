---
title: Esempio di scenario - Definizione delle allocazioni dinamiche in base agli articoli venduti | Documenti Microsoft
description: In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 3103583c9781c283479c5f66e90f0e875faf46cc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801485"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Esempio dello scenario: definizione delle allocazioni dinamiche in base agli articoli venduti
In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica. Nell'esempio è possibile modificare l'assegnazione dinamica dei costi per il centro di costo VENDITE per supportare il nuovo oggetto di costo ATTREZZATURA IT. I numeri degli articoli dei colli di ATTREZZATURA IT sono inclusi nell'intervallo compreso tra 8904-W e 8924-W. Utilizzare le cifre di vendita dell'anno precedente per calcolare la quota. L'allocazione viene registrata nel tipo di costo di supporto 9903.  

> [!NOTE]  
>  Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Per definire le allocazioni dinamiche in base agli articoli venduti nell'anno precedente  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Allocazioni costi** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Allocazione costi** scegliere l'azione **Nuovo**.  
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
    >  In [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono utilizzate le cifre di vendita degli anni precedenti per calcolare una quota di 1.596,50 VL con il 100% dei colli di ATTREZZATURA IT. Pertanto, tutti gli articoli venduti nell'ultimo anno verranno assegnati all'oggetto di costo ATTREZZATURA IT.  

## <a name="see-also"></a>Vedi anche  
[Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)  
[Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)   
[Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)
