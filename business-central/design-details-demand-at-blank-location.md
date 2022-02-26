---
title: 'Dettagli di progettazione: Domanda e approvvigionamento | Microsoft Docs'
description: Questo argomento introduce il concetto di domanda, ovvero il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 62abcd0e37a9871efd6158a898538b7c18b6b47f
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215330"
---
# <a name="design-details-demand-at-blank-location"></a>Dettagli di progettazione: Domanda nell'ubicazione Vuota
Quando un utente crea un evento di domanda, ad esempio una riga dell'ordine di vendita, il programma consente a volte all'utente di specificare un codice ubicazione e in altre non lo consente, ovvero viene utilizzata un'ubicazione vuota.

Per la domanda con o senza codici ubicazione, il sistema di pianificazione agisce in modo diretto nei casi indicati di seguito.

- Le righe della domanda includono sempre codici ubicazione e il sistema utilizza completamente le USK, incluso il setup dell'ubicazione appropriato.
- Le righe della domanda non includono mai i codici ubicazione e il sistema non utilizza le USK o il setup dell'ubicazione (come nel caso dell'ultimo scenario riportato di seguito).

Se tuttavia i codici ubicazione sono a volte inclusi e a volte non inclusi negli eventi della domanda, il sistema di pianificazione segue regole specifiche in base al setup.

## <a name="demand-at-location"></a>Domanda nell'ubicazione
In caso di rilevamento di una domanda in corrispondenza di un'ubicazione, il funzionamento del sistema di pianificazione varia in base a tre importanti valori di setup. Durante l'esecuzione della pianificazione, viene eseguito il controllo dei tre valori di setup in sequenza, quindi la pianificazione viene eseguita in base a tali valori.

1. Viene verificata la presenza di un segno di spunta nel campo **Ubicazione Obbligatoria**.

    In caso affermativo

2. Viene verificata la presenza dell'unità di stockkeeping (USK) per l'articolo.

    In caso affermativo

    L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.

    In caso negativo

3. Viene verificata la presenza del codice ubicazione richiesto nel campo Componenti nell'Ubicazione.

  In caso affermativo

  L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

  In caso negativo

  L'articolo viene pianificato in base a quanto segue: Metodi di Riordino = Lotto-per-Lotto, Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti, articoli che utilizzano il Metodo di riordino = Il sistema continuerà a utilizzare l'Ordine e tutte le altre impostazioni.

> [!NOTE]
> L'impostazione della pianificazione eccezionale che viene resa come l'ultima reazione nel passaggio 3 precedente viene indicata di seguito come "l'alternativa minima". Questa impostazione di pianificazione copre solo la domanda esatta e tutti gli altri parametri di pianificazione vengono ignorati.

Per informazioni sulle variazioni della logica di pianificazione, vedere la sezione relativa agli scenari di seguito riportata.

## <a name="demand-at-blank-location"></a>Domanda nell'ubicazione vuota
Anche se il campo **Ubicazione obbligatoria** è selezionato, il programma consentirà la creazione delle righe della domanda senza un codice ubicazione, definita anche come ubicazione vuota. Si tratta di una deviazione per il sistema perché dispone di diversi valori setup ottimizzati per gestire le ubicazioni (vedere sopra) e di conseguenza il motore di pianificazione non creerà una riga di pianificazione per tale riga della domanda.

Se il campo **Ubicazione obbligatoria** non è selezionato ma è presente uno dei valori di impostazione ubicazione disponibili, verrà considerato una deviazione e il sistema di pianificazione reagirà utilizzando un'"alternativa minima". L'articolo viene pianificato in base a: metodo di riordino = lotto per lotto (ordine rimane ordine), Includi giacenze = Sì, tutti gli altri parametri di pianificazione = vuoti.

## <a name="scenarios"></a>Scenari
Gli scenari seguenti descrivono le variazioni di domanda nell'ubicazione vuota e come il sistema di pianificazione risolve con "un'alternativa minima".

### <a name="setup-1"></a>Setup 1:
Ubicazione Obbligatoria = Sì

Unità di stockkeeping impostate su ROSSO

Componenti nell'ubicazione = BLU

#### <a name="case-11-demand-is-at-red-location"></a>Caso 1.1: domanda nell'ubicazione ROSSA
L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.

#### <a name="case-12-demand-is-at-blue-location"></a>Caso 1.2: domanda nell'ubicazione BLU
L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.

#### <a name="case-13-demand-is-at-green-location"></a>Caso 1.3: domanda nell'ubicazione VERDE
L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.

#### <a name="case-14-demand-is-at-blank-location"></a>Caso 1.4: domanda nell'ubicazione VUOTA
L'articolo non viene pianificato perché non è definita alcuna ubicazione nella riga della domanda.

### <a name="setup-2"></a>Setup 2:
Ubicazione Obbligatoria = Sì

Nessuna USK esistente

Componenti nell'ubicazione = BLU

#### <a name="case-21-demand-is-at-red-location"></a>Caso 2.1: domanda nell'ubicazione ROSSA
L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.

#### <a name="case-22-demand-is-at-blue-location"></a>Caso 2.2: domanda nell'ubicazione BLU
L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

### <a name="setup-3"></a>Setup 3:
Ubicazione Obbligatoria = No

Nessuna USK esistente

Componenti nell'ubicazione = BLU

#### <a name="case-31-demand-is-at-red-location"></a>Caso 3.1: domanda nell'ubicazione ROSSA
L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.

#### <a name="case-32-demand-is-at-blue-location"></a>Caso 3.2: domanda nell'ubicazione BLU
L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

#### <a name="case-33-demand-is-at-blank-location"></a>Caso 3.3: domanda nell'ubicazione VUOTA
L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.

### <a name="setup-4"></a>Setup 4:
Ubicazione Obbligatoria = No

Nessuna USK esistente

Componenti nell'ubicazione = VUOTO

#### <a name="case-41-demand-is-at-blue-location"></a>Caso 4.1: domanda nell'ubicazione BLU
L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.

#### <a name="case-42-demand-is-at-blank-location"></a>Caso 4.2: domanda nell'ubicazione VUOTA
L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

Come illustrato nell'ultimo scenario, l'unico modo per ottenere un risultato corretto per una riga della domanda senza un codice ubicazione consiste nel disabilitare i valori di setup relativi alle ubicazioni. In modo analogo, l'unico modo per ottenere risultati di pianificazione stabili per la domanda nelle ubicazioni consiste nell'utilizzare le USK. Se le società eseguono spesso la pianificazione per la domanda nelle ubicazioni, si consiglia pertanto di utilizzare l'area Unità di Stockkeeping.

## <a name="see-also"></a>Vedere anche  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]