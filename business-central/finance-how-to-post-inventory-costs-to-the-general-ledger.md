---
title: Riconciliare i costi di magazzino con la contabilità generale
description: 'Al termine dei periodi contabili, è necessario eseguire una sequenza di task di revisione e controllo dei costi in modo da comunicare il valore di magazzino corretto e bilanciato.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: 9297
ms.date: 06/16/2021
ms.author: edupont
---
# Riconciliare i costi di magazzino con la contabilità generale

Quando si registrano transazioni di magazzino, ad esempio spedizioni, fatture di vendite o rettifiche di magazzino, le modifiche ai costi degli articoli vengono registrate automaticamente nei movimenti di valorizzazione. Per riflettere la modifica del valore di magazzino nei registri finanziari, i costi di magazzino vengono registrati automaticamente nei conti giacenza magazzino correlati in contabilità generale. Per ogni transazione di magazzino registrata, verranno registrati i valori appropriati nel conto giacenza magazzino, nel conto di rettifica e nel conto COGS nella contabilità generale.

La registrazione automatica dei costi viene definita dal campo **Reg. automatica costi** nella pagina **Setup magazzino**.

Anche se i costi vengono registrati automaticamente in contabilità generale, è comunque necessario assicurarsi che i costi delle merci vengano trasferiti alle transazioni in uscita correlate, in particolare nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Questa operazione è detta rettifica dei costi. I costi dell'articolo vengono rettificati automaticamente quando si registrano le transazioni articolo, ma è possibile anche rettificarli manualmente. Per ulteriori informazioni, vedere [Rettificare i costi articoli](inventory-how-adjust-item-costs.md).

## Per registrare manualmente i costi di magazzino

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registra costo magazzino in C/G**, quindi scegli il collegamento correlato.
2. Per registrare manualmente i costi di magazzino nella contabilità generale, eseguire il processo batch. Quando si esegue questo processo batch, vengono creati i movimenti C/G sulla base dei movimenti di valorizzazione. È possibile registrare i movimenti in modo che vengano riepilogati per categoria di registrazione.

> [!NOTE]  
> Quando si esegue questo processo batch, potrebbero verificarsi errori dovuti a setup mancante o setup delle dimensioni incompatibile. Se vengono rilevati errori nel setup delle dimensioni, questi vengono ignorati e vengono utilizzate le dimensioni del movimento di valorizzazione. In caso di errori di altro tipo, la registrazione dei movimenti di valorizzazione viene saltata e i movimenti vengono elencati alla fine del report in una sezione relativa ai “movimenti saltati”. Per registrare questi movimenti, è prima necessario correggere gli errori.

Per visualizzare un elenco di errori prima di eseguire il processo batch di registrazione, eseguire il report **Registra costo mag. in C/G - Test**. Nel report di test vengono elencati tutti gli errori rilevati durante una registrazione di test. È quindi possibile correggere gli errori e poi eseguire il processo batch di registrazione del costo di magazzino senza saltare alcun movimento.

Se si desidera semplicemente ottenere informazioni sui valori che possono essere registrati nella contabilità generale senza eseguire la registrazione, è possibile eseguire il processo batch **Registra costo magazzino in C/G** senza effettuare la registrazione dei valori nella contabilità generale. A tale scopo, è necessario deselezionare il campo **Registra** dalla pagina di richiesta. In questo modo, quando si esegue il processo batch, viene esclusivamente prodotto il report in cui sono indicati i valori pronti per essere registrati nella contabilità generale, ma che non sono stati ancora registrati.

## Per controllare la riconciliazione tra il movimento contabile di inventario e la contabilità generale
La pagina **Magazzino - Riconciliazione C/G** offre le informazioni seguenti:

- Esposizione delle differenze di riconciliazione attraverso un confronto tra i dati registrati nella contabilità generale e i dati registrati nella contabilità di magazzino (movimenti di valorizzazione).
- Visualizzazione degli importi dei costi non riconciliati nei movimenti di valorizzazione se sono stati mappati ai corrispondenti conti correlati al magazzino in contabilità generale e confronto con i totali effettivamente registrati negli stessi conti in contabilità generale.
- Visualizzazione della struttura a movimenti doppi della contabilità generale attraverso la presentazione visiva dei dati in base a tale struttura. Ad esempio a un movimento COGS corrisponde un movimento di magazzino.
- Possibilità per gli utenti di eseguire il drill-down e di visualizzare i movimenti che costituiscono gli importi di costo.
- Inclusione dei filtri che consentono di restringere le analisi in base alla data, all'articolo e all'ubicazione.
- Descrizione dei motivi per la riconciliazione delle differenze in messaggi informativi.


La colonna **Nome** all'estrema sinistra della griglia elenca i vari tipi di conti C/G che sono associati al magazzino.

Le colonne **Magazzino**, **Magazzino (Provvis.)** e **Magazzino WIP** mostrano i totali fatturati, non fatturati e i totali WIP di ciascun tipo di conto C/G. Tali importi vengono calcolati da movimenti di valorizzazione, cioè sono previsti nei tipi di conto C/G in cui verranno inseriti una volta registrati in contabilità generale.

La colonna **Totale** mostra la somma (in grassetto) degli importi dei movimenti di valorizzazione presenti nelle tre colonne di magazzino.

La colonna **Totale C/G** mostra gli importi (in grassetto) per ciascun tipo di conto G/L presente in contabilità generale. Tali importi vengono calcolati da movimenti C/G, cioè rappresentano i costi di magazzino già registrati in C/G.

La colonna **Differenza** rappresenta la differenza tra i valori nei campi **Totale C/G** e **Totale**.

Nella parte superiore della pagina **Magazzino - Riconciliazione C/G** è possibile immettere filtri per limitare, ad esempio, il periodo di tempo per il quale si desidera ottenere informazioni.

Se si seleziona la casella di controllo **Mostra avviso** e vi sono discrepanze tra i totali di magazzino e quelli del conto C/G, nel campo **Avviso** della griglia vengono visualizzati messaggi in cui viene illustrata la discrepanza. Se si seleziona il campo Avviso, vengono fornite ulteriori informazioni sul significato dell'avviso.

Una volta specificati tutti i filtri desiderati, scegliere l'azione **Mostra matrice**. I dati vengono calcolati e viene visualizzata la pagina della matrice.

Nella colonna a sinistra della griglia vengono visualizzati i diversi tipi di conti di contabilità generale associati al magazzino. Sono quindi visualizzati i totali di magazzino fatturati, non fatturati (provvisori) e WIP per ognuno dei tipi di conto. Tali totali vengono calcolati automaticamente dai movimenti di valorizzazione.

Nelle colonne successive sono visualizzati i totali per gli stessi tipi di conto calcolati dai movimenti C/G.

Scegliere l'importo in qualsiasi campo relativo ai totali per visualizzare i movimenti report magazzino utilizzati per calcolare i totali. Per i totali di magazzino, i movimenti report magazzino sono costituiti dalle somme dei movimenti di valorizzazione per gli articoli. Per i totali del conto C/G, i movimenti report magazzino sono costituiti dalle somme calcolate dai movimenti C/G.

## Creazione di report dei costi e riconciliazione con la contabilità generale
Altri report, funzioni di tracciabilità e uno speciale strumento di riconciliazione sono a disposizione del revisore o del controllore responsabile della comunicazione di un valore di magazzino corretto e bilanciato al reparto finanziario.

Questi sono descritti nella tabella seguente.    

|**Per**|**Vedere**|  
|------------|-------------|  
|Visualizzare il valore di magazzino degli articoli selezionati, incluse le informazioni relative alle quantità e ai valori di aumenti e diminuzioni del magazzino per un determinato periodo.|Report **Valutazione magazzino**|  
|Visualizzare il valore di magazzino degli ordini di produzione selezionati nel magazzino WIP, ad esempio le quantità e i valori del consumo, l'utilizzo della capacità e l'output negli ordini di produzione in corso.|Report **Valutazione magazzino - WIP**|  
|Visualizzare il valore di magazzino degli articoli selezionati, incluso il relativo costo effettivo e previsto alla data specificata.|Report **Valutazione magazzino - Specifica costi**|  
|Utilizzare un report per analizzare i motivi delle variazioni di costo o per ottenere informazioni relative al dettaglio costi degli articoli venduti (COGS).|Report **Breakdown dettaglio costi**|  

## Vedere anche  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]