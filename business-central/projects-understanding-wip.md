---
title: Metodi WIP per il calcolo e la registrazione dello stato di avanzamento del progetto
description: 'Vengono descritti i diversi metodi WIP che possono essere utilizzati per registrare, monitorare e calcolare le informazioni finanziarie per i progetti in corso.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="understanding-wip-methods-in-project-management"></a>Comprendere i metodi WIP nella gestione dei progetti

Durante lo svolgimento di un progetto, vengono consumati materiali, risorse ed effettuate altre spese che devono essere registrate nel progetto. La funzionalità WIP (Work in Process) consente di stimare il valore finanziario dei progetti nella contabilità generale nelle varie fasi di un progetto. In molti casi è possibile registrare le spese relative a un progetto prima di fatturarlo. Se sono state registrate solo le spese, il rendiconto finanziario non sarà accurato.

Per tenere traccia del valore nella contabilità generale, è possibile calcolare il WIP e registrare il valore nella contabilità generale. Per ulteriori informazioni, vedere [Monitorare lo stato di avanzamento e le prestazioni dei progetti](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] supporta i seguenti metodi di calcolo e di registrazione del valore WIP.

| Metodo WIP | Formula di calcolo | Descrizione calcolo |
| --- | --- | --- |
| Valore costo |Ricavo riconosciuto = Prezzo fatturato fatturabile <br /><br />Costi totali stimati = Costi totali budget / Prezzo totale budget <br /><br />Costi totali stimati = Prezzo totale fatturabile x Rapporto costi budget <br /><br />Percentuale di completamento = Costi totali utilizzo/Costi totali budget <br /><br />% fatturata = Prezzo fatturato fatturabile / Prezzo totale fatturabile <br /><br />Costo WIP = (Perc. di completamento - % fatturata) x Costi totali stimati <br /><br />Costi riconosciuti  Costi totali utilizzo - Costo WIP|Per calcolare il valore costo iniziare calcolando il valore di quanto è stato fornito facendo una proporzione dei costi totali stimati in base alla percentuale di completamento. I costi fatturati vengono sottratti facendo una proporzione dei costi totali stimati in base alla percentuale fatturata.<br /><br />Questo calcolo richiede che il prezzo totale fatturabile, il prezzo totale budget e i costi totali budget siano inseriti correttamente per l'intero progetto. |
| Costo del venduto |Ricavo riconosciuto = Prezzo fatturato fatturabile<br /><br /> Costi riconosciuti = Costo totale budget x Percentuale fatturata<br /><br /> % fatturata = Prezzo fatturato fatturabile / Prezzo totale fatturabile<br /> La percentuale fatturata esiste come colonna nelle righe di attività di progetto<br /><br /> Costi WIP= Costi totali utilizzo - Costi riconosciuti |Per calcolare il costo del venduto iniziare calcolando i costi riconosciuti. I costi vengono riconosciuti in modo proporzionale in base ai costi totali budget.<br /><br /> Questo calcolo richiede che il prezzo totale fatturabile e i costi totali budget siano inseriti correttamente per l'intero progetto. |
| Valore vendite |Costi riconosciuti = Costi totali utilizzo<br /><br /> Ricavo riconosciuto = Prezzo totale utilizzo x Rapporto fatturazione previsto<br /><br /> % recupero costi = Prezzo totale fatturabile / Prezzo totale budget<br /><br /> Vendite WIP = Vendite riconosciute - Prezzo fatturato fatturabile |I calcoli del valore vendite riconoscono il ricavo in modo proporzionale in base ai costi totali utilizzo e al rapporto di recupero costi previsto.<br /><br /> Questo calcolo richiede che il prezzo totale fatturabile e il prezzo totale budget siano inseriti correttamente per l'intero progetto. |
| Percentuale di completamento |Costi riconosciuti = Costi totali utilizzo<br /><br /> Ricavo riconosciuto = Prezzo totale fatturabile x Percentuale di completamento<br /><br /> Percentuale di completamento = Costi totali utilizzo/Costi totali budget<br /> Aquisita nel campo **% completamento costi** nelle righe di attività di progetto<br /><br /> Vendite WIP = Vendite riconosciute - Prezzo fatturato fatturabile |I calcoli della percentuale di completamento riconoscono il ricavo in modo proporzionale in base alla percentuale di completamento, ovvero il rapporto tra i costi totali utilizzo e i costi di budget.<br /><br /> Questo calcolo richiede che il prezzo totale fatturabile e i costi totali budget siano inseriti correttamente per l'intero progetto. |
| Contratto completato |Importo WIP = Importo costo WIP = Utilizzo (costo totale)<br /><br /> Importo vendita WIP = Fatturabile (prezzo fatturato) |Il ricavo e i costi vengono riconosciuti dal contratto completato solo in seguito al completamento del progetto. Ciò risulta utile qualora le previsioni dei costi e del ricavo del progetto siano particolarmente incerte.<br /><br /> Qualsiasi utilizzo viene registrato in Conto costi WIP (cespiti) e tutte le vendite fatturate vengono registrate in Conto vendite fatturate WIP (passività), fino al completamento del progetto. |

## <a name="see-also"></a>Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
