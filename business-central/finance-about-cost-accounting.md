---
title: Informazioni sulla contabilità industriale | Microsoft Docs
description: La contabilità industriale può essere utilizzata per comprendere i costi operativi di un'attività.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ba956c883c567e7acc2cd625d8d5e51d94ee753
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784917"
---
# <a name="about-cost-accounting"></a>Informazioni sulla contabilità industriale
La contabilità industriale può essere utilizzata per comprendere i costi operativi di un'attività. Le informazioni sulla contabilità generale sono concepite per analizzare:  

-   Tipi di costi sostenuti per l'attività aziendale  
-   A quali settori sono correlati i costi  
-   Persone che sostengono i costi  

Nella contabilità industriale, i costi effettivi e previsti per consumi, reparti, prodotti e progetti vengono allocati per analizzare la redditività della società.  

## <a name="workflow-in-cost-accounting"></a>Flusso di lavoro nella contabilità industriale  
La contabilità industriale presenta i seguenti componenti principali:  

-   Tipi di costo, centri di costo e oggetti di costo  
-   Movimenti di costi e registrazioni costi  
-   Allocazioni costi  
-   Budget costi
-   Reporting dei costi  

Nel diagramma seguente viene mostrato il flusso di lavoro nella contabilità industriale.  

![Sintesi della contabilità industriale](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Tipi di costo, centri di costo e oggetti di costo  
Vengono definiti i tipi di costo, i centri di costo e gli oggetti di costo per analizzare quali sono i costi, da dove essi derivano e chi deve sostenerli.  

Viene definito un piano dei tipi di costo con una struttura e una funzionalità che sono simili a quelle del piano dei conti di contabilità generale. È possibile trasferire i conti economici di contabilità generale o creare il proprio piano dei tipi di costo.  

I centri di costo sono i reparti e i centri profitto responsabili dei costi e delle entrate. Spesso sono impostati più centri di costo nella contabilità industriale che in qualsiasi dimensione impostata nella contabilità generale. Nella contabilità generale vengono utilizzati in genere solo i centri di costo del primo livello per i costi diretti e i costi iniziali. Nella contabilità industriale vengono creati ulteriori centri di costo per i livelli di allocazione aggiuntivi.  

Gli oggetti di costo sono i prodotti, i gruppi prodotto o i servizi di una società. Si tratta dei prodotti finiti di cui una società sostiene i costi.  

In una società i centri di costo possono essere collegati ai reparti e gli oggetti di costo ai progetti. Tuttavia, i centri di costo e gli oggetti di costo possono essere collegati a qualsiasi dimensione nella contabilità generale ed essere completati con i subtotali e i titoli.  

## <a name="cost-entries-and-cost-journals"></a>Movimenti di costi e registrazioni costi  
I costi operativi possono essere trasferiti dalla contabilità generale. I movimenti di costi possono essere trasferiti automaticamente dalla contabilità generale ai movimenti di costi con ciascuna registrazione. È inoltre possibile utilizzare un processo batch per trasferire i movimenti C/G ai movimenti di costi in base alle registrazioni riepilogative quotidiane e mensili.  

Nelle registrazioni costi è possibile registrare il costo e le attività che non derivano dalla contabilità generale né vengono generati dalle allocazioni. Ad esempio, è possibile registrare i costi operativi, le spese interne, le allocazioni e i movimenti di rettifica effettivi tra i tipi di costo, i centri di costo e gli oggetti di costo singolarmente o in modo ricorrente.  

## <a name="cost-allocations"></a>Allocazioni costi  
Con le allocazioni è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. I costi generali vengono innanzitutto registrati nei centri di costo e in seguito addebitati agli oggetti di costo. Ad esempio, questa operazione potrebbe essere effettuata in un reparto vendite che vende diversi prodotti contemporaneamente. I costi diretti possono essere allocati direttamente a un oggetto di costo, ad esempio il materiale acquistato per un prodotto specifico.  

La base di allocazione utilizzata e la precisione della definizione di allocazione influiscono sui risultati delle allocazioni di costi. La definizione di allocazione viene utilizzata per allocare i costi innanzitutto dai cosiddetti centri di pre-costo ai centri di costo principali e, successivamente, dai centri di costo agli oggetti di costo.  

Ogni allocazione è costituita da un'origine di allocazione e da una o più destinazioni di allocazione. È possibile allocare i valori effettivi o quelli previsti utilizzando il metodo di allocazione statica che è basato su un valore definito, ad esempio la superficie o un rapporto di allocazione stabilito pari a 5:2:4. È inoltre possibile allocare i valori effettivi o previsti utilizzando il metodo di allocazione dinamica con nove basi di allocazione predefinite e 12 intervalli di date dinamici.  

## <a name="cost-budgets"></a>Budget costi  
È possibile creare tutti i budget costi necessari. È possibile copiare un budget costi nel budget di contabilità generale e viceversa. È possibile trasferire i costi previsti come costi effettivi.  

## <a name="cost-reporting"></a>Reporting dei costi  
La maggior parte dei report e delle statistiche è basata sui movimenti di costi registrati. È possibile impostare l'ordinamento dei risultati e utilizzare filtri per definire quali dati devono essere visualizzati. È possibile creare report per l'analisi di distribuzione dei costi. Inoltre, è possibile utilizzare le situazioni contabili standard per definire come vengono visualizzati i report del piano dei tipi di costo.  

## <a name="see-also"></a>Vedi anche  
 [Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
 [Finanze](finance.md)   
 [Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)  
 [Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]