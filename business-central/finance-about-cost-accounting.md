---
title: Informazioni sulla contabilità industriale
description: La contabilità industriale può essere utilizzata per comprendere i costi operativi di un'attività. Le informazioni sulla contabilità generale sono concepite per analizzare diversi problemi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-cost-accounting"></a>Informazioni sulla contabilità industriale

La contabilità industriale può essere utilizzata per comprendere i costi operativi di un'attività. Le informazioni sulla contabilità generale sono concepite per analizzare:  

- Quali tipi di costi deve sostenere la tua azienda.  
- A quali settori sono correlati i costi.
- Chi sostiene i costi.

Nella contabilità industriale, i costi effettivi e previsti per consumi, reparti, prodotti e progetti vengono allocati per analizzare la redditività della società.  

## <a name="workflow-in-cost-accounting"></a>Flusso di lavoro nella contabilità industriale

La contabilità industriale presenta i seguenti componenti principali:  

- Tipi di costo, centri di costo e oggetti di costo  
- Movimenti di costi e registrazioni costi  
- Allocazioni costi  
- Budget costi
- Reporting dei costi  

Nel diagramma seguente viene mostrato il flusso di lavoro nella contabilità industriale.  

![Sintesi della contabilità industriale.](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Tipi di costo, centri di costo e oggetti di costo

Vengono definiti i tipi di costo, i centri di costo e gli oggetti di costo per analizzare quali sono i costi, da dove essi derivano e chi deve sostenerli.  

Per prima cosa, viene definito un piano dei tipi di costo con una struttura e una funzionalità che sono simili a quelle del piano dei conti di contabilità generale. È possibile creare il proprio grafico dei tipi di costo o farlo trasferendo i conti economici della contabilità generale.  

I centri di costo sono i reparti e i centri profitto responsabili dei costi e delle entrate. Spesso sono impostati più centri di costo nella contabilità industriale che in qualsiasi dimensione impostata nella contabilità generale. Nella contabilità generale vengono utilizzati in genere solo i centri di costo del primo livello per i costi diretti e i costi iniziali. Nella contabilità industriale vengono creati ulteriori centri di costo per i livelli di allocazione aggiuntivi.  

Gli oggetti di costo sono i prodotti, i gruppi prodotto o i servizi offerti da una società. Questi oggetti sono "prodotti finiti" che sostengono i costi.  

In una società i centri di costo possono essere collegati ai reparti e gli oggetti di costo ai progetti. Tramite la contabilità generale, i centri di costo e gli oggetti di costo possono essere collegati a qualsiasi dimensione ed essere completati con i subtotali e i titoli.  

## <a name="cost-entries-and-cost-journals"></a>Movimenti di costi e registrazioni costi

I costi operativi possono essere trasferiti dalla contabilità generale. I movimenti di costi possono essere trasferiti automaticamente dalla contabilità generale ai movimenti di costi con ciascuna registrazione. Puoi inoltre utilizzare un processo batch per trasferire i movimenti C/G ai movimenti di costi in base alle registrazioni riepilogative quotidiane e mensili.  

Nelle registrazioni costi è possibile registrare il costo e le attività che non derivano dalla contabilità generale né vengono generati dalle allocazioni. Ad esempio, è possibile registrare i costi operativi, le spese interne, le allocazioni e i movimenti di rettifica effettivi tra i tipi di costo, i centri di costo e gli oggetti di costo singolarmente o in modo ricorrente.  

## <a name="cost-allocations"></a>Allocazioni costi

Con le allocazioni è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. I costi generali vengono innanzitutto registrati nei centri di costo e in seguito addebitati agli oggetti di costo. Ad esempio, questa operazione può essere effettuata in un reparto vendite che vende diversi prodotti contemporaneamente. I costi generali del reparto, quali stipendi, forniture e spese di viaggio, vengono inizialmente attribuiti al centro di costo vendite. I costi vengono poi ripartiti tra i diversi prodotti (oggetti di costo) venduti, insieme ai materiali acquistati (costo diretto).

La base di allocazione e la precisione della definizione di allocazione influiscono sui risultati delle allocazioni di costi. La definizione di allocazione alloca i costi innanzitutto dai cosiddetti centri di pre-costo ai centri di costo principali e, successivamente, dai centri di costo agli oggetti di costo.  

Ogni allocazione è costituita da un'origine di allocazione e da una o più destinazioni di allocazione. Puoi allocare valori effettivi o valori a budget utilizzando il metodo di allocazione statica basato su un valore definito. Ad esempio, la metratura o un rapporto di allocazione stabilito di 5:2:4. È inoltre possibile allocare i valori effettivi o previsti utilizzando il metodo di allocazione dinamica con nove basi di allocazione predefinite e 12 intervalli di date dinamici.  

## <a name="cost-budgets"></a>Budget costi

Analogamente alla definizione del budget nella contabilità generale, è possibile creare budget per pianificare i costi durante un determinato periodo (un anno fiscale, ad esempio), che possono essere applicati a un centro di costo (reparto aziendale) o a un oggetto di costo (prodotto o servizio). È possibile creare tutti i budget costi necessari. Puoi copiare un budget costi nel budget di contabilità generale e viceversa. E puoi trasferire i costi previsti come costi effettivi.

## <a name="cost-reporting"></a>Reporting dei costi

La maggior parte dei report e delle statistiche è basata sui movimenti di costi registrati. È possibile impostare l'ordinamento dei risultati e utilizzare filtri per definire quali dati devono essere visualizzati. È possibile creare report per l'analisi di distribuzione dei costi. Inoltre, è possibile utilizzare i report finanziari standard per definire come vengono visualizzati i report del piano dei tipi di costo.  

## <a name="see-also"></a>Vedere anche

[Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
[Dati finanziari](finance.md)  
[Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
