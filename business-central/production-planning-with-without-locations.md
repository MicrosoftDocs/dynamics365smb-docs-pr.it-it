---
title: Pianificazione con o senza ubicazioni | Microsoft Docs
description: È importante comprendere la pianificazione con o senza codici ubicazione nelle righe della domanda.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2d9afd30c3b81912797ad95871256207d135b673
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783984"
---
# <a name="planning-with-or-without-locations"></a>Pianificazione con o senza ubicazioni
Nel caso della pianificazione con o senza codici ubicazione nelle righe della domanda, il sistema di pianificazione agisce in modo diretto nei casi indicati di seguito.  

-   Le righe della domanda includono sempre codici ubicazione e il sistema utilizza completamente le unità di stockkeeping, incluso il setup dell'ubicazione appropriato.  
-   Le righe della domanda non includono mai i codici ubicazione e il sistema non utilizza le USK o il setup dell'ubicazione, come nel caso dell'ultimo scenario riportato di seguito.  

Se tuttavia i codici ubicazione sono a volte inclusi e a volte non inclusi nelle righe della domanda, il sistema di pianificazione segue regole specifiche in base al setup.  

## <a name="demand-at-location"></a>Domanda nell'ubicazione  
In caso di rilevamento di una domanda in corrispondenza di un'ubicazione, ovvero una riga con un codice ubicazione, il funzionamento del sistema di pianificazione varia in base a 3 importanti valori di setup.  

Durante l'esecuzione della pianificazione, viene eseguito il controllo dei 3 valori di setup in sequenza, quindi la pianificazione viene eseguita in base a tali valori, come indicato di seguito.  

1.  Viene verificata la presenza di un segno di spunta nel campo **Ubicazione Obbligatoria**.  

    In caso affermativo  

2.  Viene verificata la presenza dell'unità di stockkeeping (USK) per l'articolo.  

    In caso affermativo  

    L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.  

    In caso negativo  

3.  Viene verificata la presenza del codice ubicazione richiesto nel campo **Componenti nell'Ubicazione**.  

    In caso affermativo  

    L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

    In caso negativo  

    L'articolo viene pianificato in base a quanto segue: Metodi di Riordino =  *Lotto-per-Lotto*, Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti. Nel caso degli articoli per i quali è utilizzato il metodo di riordino  *Ordine*, il sistema continuerà a utilizzare  *Ordine* e tutte le altre impostazioni.  

> [!NOTE]  
>  Questa "alternativa minima" riguarda esclusivamente la domanda. Gli eventuali parametri di pianificazione definiti vengono ignorati.  

Vedere le differenze di scenario riportate di seguito.  

## <a name="demand-at-blank-location"></a>Domanda nell'"ubicazione vuota"  
Anche se la casella di controllo **Ubicazione obbligatoria** è selezionata, il sistema consente la creazione delle righe della domanda senza un codice ubicazione, definita anche come ubicazione *VUOTA*. Si tratta di una deviazione per il sistema perché dispone di diversi valori setup ottimizzati per gestire le ubicazioni (vedere sopra) e di conseguenza il motore di pianificazione non creerà una riga di pianificazione per tale riga della domanda. Se il campo **Ubicazione obbligatoria** non è selezionato ma non esiste nessuno dei valori setup dell'ubicazione, anche questa è considerata una deviazione e il sistema di pianificazione reagirà restituendo l'"alternativa minima":   
L'articolo viene pertanto pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane *Ordine)*, Includi Giacenze =  *Sì*, tutti gli altri parametri vuoti.  

Vedere le differenze negli scenari di setup riportati di seguito.  

### <a name="setup-1"></a>Setup 1:  

-   Ubicazione Obbligatoria = *Sì*  
-   Unità di stockkeeping =  *ROSSO*  
-   Componenti nell'Ubicazione =  *BLU*  

#### <a name="case-11-demand-is-at--red-location"></a>Caso 1.1: domanda nell'ubicazione *ROSSO*  

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK, incluso il possibile trasferimento.  

#### <a name="case-12-demand-is-at--blue-location"></a>Caso 1.2: domanda nell'ubicazione *BLU*  

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

#### <a name="case-13-demand-is-at--green-location"></a>Caso 1.3: domanda nell'ubicazione  *VERDE*  

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.  

#### <a name="case-14-demand-is-at--blank-location"></a>Caso 1.4: domanda nell'ubicazione  *VUOTA*  

L'articolo non viene pianificato perché non è definita alcuna ubicazione nella riga della domanda.  

### <a name="setup-2"></a>Setup 2:  

-   Ubicazione Obbligatoria = *Sì*  
-   Nessuna USK esistente  
-   Componenti nell'Ubicazione =  *BLU*  

#### <a name="case-21-demand-is-at--red-location"></a>Caso 2.1: domanda nell'ubicazione  *ROSSO*  

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.  

#### <a name="case-22-demand-is-at--blue-location"></a>Caso 2.2: domanda nell'ubicazione *BLU*  

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

### <a name="setup-3"></a>Setup 3:  

-   Ubicazione Obbligatoria = *No*  
-   Nessuna USK esistente  
-   Componenti nell'Ubicazione =  *BLU*  

#### <a name="case-31-demand-is-at--red-location"></a>Caso 3.1: domanda nell'ubicazione  *ROSSO*  

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.  

#### <a name="case-32-demand-is-at--blue-location"></a>Caso 3.2: domanda nell'ubicazione *BLU*  

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

#### <a name="case-33-demand-is-at--blank-location"></a>Caso 3.3: domanda nell'ubicazione  *VUOTA*  

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.  

### <a name="setup-4"></a>Setup 4:  

-   Ubicazione Obbligatoria = *No*  
-   Nessuna USK esistente  
-   Componenti nell'Ubicazione =  *VUOTO*  

#### <a name="case-41-demand-is-at--blue-location"></a>Caso 4.1: domanda nell'ubicazione  *BLU*  

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.  

#### <a name="case-42-demand-is-at--blank-location"></a>Caso 4.2: domanda nell'ubicazione  *VUOTA*  

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

Come risulta evidente dall'ultimo scenario, l'unico modo per ottenere un risultato corretto per una riga della domanda senza un codice ubicazione consiste nel disabilitare i valori di setup relativi alle ubicazioni. In modo analogo, l'unico modo per ottenere risultati di pianificazione stabili per la domanda nelle ubicazioni consiste nell'utilizzare le unità di stockkeeping.  

Se si esegue spesso la pianificazione per la domanda nelle ubicazioni, si consiglia pertanto di utilizzare la funzionalità Unità di Stockkeeping.  

## <a name="see-also"></a>Vedi anche
[Pianif.](production-planning.md)    
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
