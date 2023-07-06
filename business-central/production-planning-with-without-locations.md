---
title: Pianificazione con o senza ubicazioni
description: 'In questo argomento vengono fornite informazioni sulla produzione, inclusa la pianificazione degli approvvigionamenti, in Business Central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: edupont
---
# <a name="planning-with-or-without-locations"></a><a name="planning-with-or-without-locations"></a><a name="planning-with-or-without-locations"></a>Pianificazione con o senza ubicazioni

Prima di iniziare a utilizzare il motore di pianificazione, ti consigliamo di decidere se utilizzare o meno le posizioni. Ci sono due semplici modalità principali:

* Le righe della domanda includono sempre codici ubicazione e il sistema utilizza completamente le unità di stockkeeping, incluso il setup dell'ubicazione appropriato. Ulteriori informazioni su [Domanda nell'ubicazione](#demand-at-location).  
* le righe di domanda non contengono mai codici ubicazione e il sistema utilizza la scheda articolo. Vedi lo scenario [Domanda nell'"ubicazione vuota"](#demand-at-blank-location) sottostante.

## <a name="demand-at-location"></a><a name="demand-at-location"></a><a name="demand-at-location"></a>Domanda nell'ubicazione

In caso di rilevamento di una domanda in corrispondenza di un'ubicazione, ovvero una riga con un codice ubicazione, il funzionamento del sistema di pianificazione varia in base a 2 importanti valori di setup.  

Durante l'esecuzione della pianificazione, viene eseguito il controllo dei 2 valori di setup in sequenza, quindi la pianificazione viene eseguita in base a tali valori, come indicato di seguito.  

1. Esiste uno SKU per l'articolo nell'ubicazione richiesta?  

    In caso affermativo  

    L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.  

    In caso negativo  

2. Il campo **Componenti nell'ubicazione** nella pagina **Setup manufacturing** contiene il codice ubicazione richiesto?  

    In caso affermativo  

    L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

    In caso negativo  

    L'articolo è pianificato secondo l'"alternativa minima" che copre l'esatta domanda. I parametri di pianificazione sono impostati come: Metodi di Riordino = *Lotto-per-Lotto*, Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti. Nel caso degli articoli per i quali è utilizzato il metodo di riordino *Ordine*, il sistema continuerà a utilizzare *Ordine* e tutte le altre impostazioni.

> [!TIP]
> Se risulta spesso necessario pianificare la domanda in diverse ubicazioni, è consigliabile utilizzare la funzionalità Unità di stockkeeping ed evitare di eseguire una domanda su un'ubicazione vuota. Ulteriori informazioni in [Impostare le unità di stockkeeping](inventory-how-to-set-up-stockkeeping-units.md)

Vedere le differenze di [scenario riportate di seguito](#scenarios).

> [!NOTE]
> Il campo, **Componenti nell'Ubicazione** nella pagina **Setup manufacturing** è molto importante nella gestione di come il sistema di pianificazione gestisce le righe domanda della produzione.
>
> Per quanto riguarda la domanda di produzione, [!INCLUDE [prod_short](includes/prod_short.md)] utilizzerà la stessa ubicazione per il subassemblaggio e i componenti di quella indicata nell'ordine di produzione. Compilando questo campo, tuttavia, è possibile reindirizzare i componenti e il subassemblaggio a un'altra ubicazione.
>
> È possibile definire ciò anche per un'unità di stockkeeping specifica selezionando un codice ubicazione diverso nel campo **Componenti nell'ubicazione** della scheda relativa. Si noti, tuttavia, che questo è difficilmente consigliabile perché la logica di pianificazione può essere distorta nella pianificazione del componente USK.

## <a name="demand-at-blank-location"></a><a name="demand-at-blank-location"></a><a name="demand-at-blank-location"></a>Domanda in "ubicazione vuota"

In generale, quando il sistema di pianificazione rileva la domanda in un'ubicazione vuota (una riga senza un codice ubicazione), l'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

Il campo **Ubicazioni obbligatorie** nella pagina **Setup magazzino**, il campo **Componenti nell'ubicazione** nella pagina **Setup manufacturing** o le unità di stockkeeping avranno effetto su come il sistema di pianificazione gestisce le righe della domanda con/senza codici ubicazione. Se una delle seguenti dichiarazioni è vera, la domanda sull'ubicazione vuota viene inoltre considerata una deviazione e il sistema di pianificazione reagirà tramite l'emissione di un'"alternativa minima": l'articolo viene pianificato in base a: Metodo di riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi giacenze = *Sì*, tutti gli altri parametri di pianificazione = Vuoto.

* Il campo **Componenti nell'ubicazione** nella pagina **Setup manufacturing** ha un valore.
* Per l'articolo pianificato esiste un'unità di stockkeeping.
* Il campo **Ubicazione Obbligatoria** è selezionato.

## <a name="scenarios"></a><a name="scenarios"></a><a name="scenarios"></a>Scenari

Vedere le differenze negli scenari di setup riportati di seguito.

### <a name="setup-1"></a><a name="setup-1"></a><a name="setup-1"></a>Setup 1

* Ubicazione Obbligatoria = *Sì*  
* SKU è configurato su *OVEST*  
* Componenti nell'Ubicazione = *EST*  

#### <a name="case-11-demand-is-at-west-location"></a><a name="case-11-demand-is-at-west-location"></a><a name="case-11-demand-is-at-west-location"></a>Caso 1.1: domanda nell'ubicazione *OVEST*

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK, incluso il possibile trasferimento.

#### <a name="case-12-demand-is-at-east-location"></a><a name="case-12-demand-is-at-east-location"></a><a name="case-12-demand-is-at-east-location"></a>Caso 1.2: domanda nell'ubicazione *EST*

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

#### <a name="case-13-demand-is-at-north-location"></a><a name="case-13-demand-is-at-north-location"></a><a name="case-13-demand-is-at-north-location"></a>Caso 1.3: domanda nell'ubicazione  *NORD*

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti.

#### <a name="case-14-demand-is-at-blank-location"></a><a name="case-14-demand-is-at-blank-location"></a><a name="case-14-demand-is-at-blank-location"></a>Caso 1.4: domanda nell'ubicazione *VUOTA*

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti.

### <a name="setup-2"></a><a name="setup-2"></a><a name="setup-2"></a>Setup 2

* Ubicazione Obbligatoria = *Sì*  
* Nessuna USK esistente  
* Componenti nell'Ubicazione = *EST*  

#### <a name="case-21-demand-is-at-west-location"></a><a name="case-21-demand-is-at-west-location"></a><a name="case-21-demand-is-at-west-location"></a>Caso 2.1: domanda nell'ubicazione *OVEST*

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti.

#### <a name="case-22-demand-is-at-east-location"></a><a name="case-22-demand-is-at-east-location"></a><a name="case-22-demand-is-at-east-location"></a>Caso 2.2: domanda nell'ubicazione *EST*

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

### <a name="setup-3"></a><a name="setup-3"></a><a name="setup-3"></a>Setup 3

* Ubicazione Obbligatoria = *No*  
* Nessuna USK esistente  
* Componenti nell'Ubicazione = *EST*  

#### <a name="case-31-demand-is-at-west-location"></a><a name="case-31-demand-is-at-west-location"></a><a name="case-31-demand-is-at-west-location"></a>Caso 3.1: domanda nell'ubicazione *OVEST*

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti.

#### <a name="case-32-demand-is-at-east-location"></a><a name="case-32-demand-is-at-east-location"></a><a name="case-32-demand-is-at-east-location"></a>Caso 3.2: domanda nell'ubicazione *EST*

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.  

#### <a name="case-33-demand-is-at-blank-location"></a><a name="case-33-demand-is-at-blank-location"></a><a name="case-33-demand-is-at-blank-location"></a>Caso 3.3: domanda nell'ubicazione *VUOTA*

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti.

### <a name="setup-4"></a><a name="setup-4"></a><a name="setup-4"></a>Setup 4

* Ubicazione Obbligatoria = *No*  
* Nessuna USK esistente  
* Componenti nell'Ubicazione = *VUOTO*  

#### <a name="case-41-demand-is-at-east-location"></a><a name="case-41-demand-is-at-east-location"></a><a name="case-41-demand-is-at-east-location"></a>Caso 4.1: domanda nell'ubicazione *EST*

L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = *Lotto-per-Lotto* (*Ordine* rimane *Ordine*), Includi Giacenze = *Sì*, tutti gli altri parametri di pianificazione vuoti.

#### <a name="case-42-demand-is-at-blank-location"></a><a name="case-42-demand-is-at-blank-location"></a><a name="case-42-demand-is-at-blank-location"></a>Caso 4.2: domanda nell'ubicazione *VUOTA*

L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.

Come risulta evidente dall'ultimo scenario, l'unico modo per ottenere un risultato corretto per una riga della domanda senza un codice ubicazione consiste nel disabilitare i valori di setup relativi alle ubicazioni. In modo analogo, l'unico modo per ottenere risultati di pianificazione stabili per la domanda nelle ubicazioni consiste nell'utilizzare le unità di stockkeeping.  

Pertanto, se risulta spesso necessario pianificare la domanda in varie ubicazioni, è consigliabile utilizzare la funzionalità Unità di stockkeeping.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Pianif.](production-planning.md)  
[Impostare la produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostare le unità di stockkeeping](inventory-how-to-set-up-stockkeeping-units.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
