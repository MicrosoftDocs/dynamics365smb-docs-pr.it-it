---
title: 'Dettagli di progettazione: Registrazione dell''ordine di produzione | Microsoft Docs'
description: 'Simile alla registrazione dell''ordine di assemblaggio, i componenti consumati e il tempo macchina utilizzato vengono convertiti e resi come articolo prodotto una volta completato l''ordine di produzione.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# Dettagli di progettazione: Registrazione dell'ordine di produzione
Simile alla registrazione dell'ordine di assemblaggio, i componenti consumati e il tempo macchina utilizzato vengono convertiti e resi come articolo prodotto una volta completato l'ordine di produzione. Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-assembly-order-posting.md). Tuttavia, il flusso dei costi per gli ordini di assemblaggio è meno complesso, soprattutto perché la registrazione dei costi di assemblaggio si verifica solo una volta e pertanto non genera magazzino WIP.


È possibile tenere traccia delle transazioni che si verificano durante il processo di produzione tramite le fasi seguenti:  

1.  Acquisto di materiali e altri input di produzione.  
2.  Conversione in semilavorati.  
3.  Conversione in magazzino di prodotti finiti.  
4.  Vendita di prodotti finiti.  

Di conseguenza, a parte i normali conti giacenza magazzino, un'azienda manifatturiera deve creare tre conti giacenza magazzino separati per registrare le transazioni nelle varie fasi di produzione.  

|Conto giac. magazzino|Description|  
|-----------------------|---------------------------------------|  
|**Conto per materie prime**|Comprende il costo delle materie prime che sono acquistate ma non ancora trasferite alla produzione. Il saldo nel conto delle materie prime indica il costo delle materie prime disponibili.<br /><br /> Quando le materie prime passano al reparto di produzione, il costo delle materie viene trasferito dal conto per materie prime al conto WIP.|  
|**Conto WIP**|Accumula i costi sostenuti durante la produzione nel periodo contabile. Nel conto WIP vengono addebitati il costo delle materie prime che vengono trasferite dalla warehouse di materie prime, il costo di manodopera diretta realizzata e i costi generali di produzione sostenuti.<br /><br /> Al conto WIP viene accreditato il costo di produzione totale di unità che sono completate in fabbrica e trasferite alla warehouse dei prodotti finiti.|  
|**Conto prodotti finiti**|Questo conto comprende il costo di produzione totale di unità che sono completate ma non ancora vendute. Al momento della vendita, il costo delle unità vendute viene trasferito dal conto Prodotti finiti al conto COGS.|  

Il valore di magazzino viene calcolato tenendo traccia dei costi di tutti gli aumenti e le riduzioni con la seguente equazione:  

* valore di magazzino = bilancio iniziale del magazzino + valore di tutti gli aumenti - valore di tutte le riduzioni  

A seconda del tipo di magazzino, gli aumenti e le diminuzioni sono rappresentati dalle diverse transazioni.  

||Aumenti|Diminuzioni|  
|-|---------------|---------------|  
|**Magazzino di materie prime**|-   Acquisti netti di materiale<br />-   Output di sottoassemblaggi<br />-   Consumo negativo|Consumo materiale|  
|**Magazzino WIP**|-   Consumo materiale<br />-   Consumo della capacità<br />-   Costi generali produzione|Output di articoli finali (costo delle merci lavorate)|  
|**Magazzino di prodotti finiti**|Output di articoli finali (costo delle merci lavorate)|-   Vendite (costo degli articoli venduti)<br />-   Output negativo|  
|**Magazzino di materie prime**|-   Acquisti netti di materiale<br />-   Output di sottoassemblaggi<br />-   Consumo negativo|Consumo materiale|  

I valori degli aumenti e delle diminuzioni vengono registrati nei diversi tipi di magazzino lavorato nello stesso modo del magazzino acquistato. Ogni volta che si verifica una transazione di aumento o riduzione magazzino, un movimento contabile articolo e un movimento C/G corrispondente vengono creati per l'importo. Per ulteriori informazioni, vedere [Dettagli di progettazione: Registrazione magazzino](design-details-inventory-posting.md).  

Benché i valori delle transazioni correlate alle merci acquistate siano registrati solo come movimenti contabili articoli con i movimenti di valorizzazione correlati, le transazioni correlate agli articoli prodotti vengono registrate come movimenti contabili capacità ai movimenti di valorizzazione correlati, oltre ai movimenti contabili articoli.  

## Struttura della registrazione  
La registrazione di ordini di produzione nel magazzino WIP include l'output, il consumo e la capacità.  

Nel seguente diagramma vengono mostrate le routine di registrazione implicate nella codeunit 22.  

![Procedure di registrazione ordini di produzione.](media/design_details_inventory_costing_14_production_posting_1.png "Procedure di registrazione ordini di produzione")  

Nel seguente diagramma vengono mostrate le associazioni tra i movimenti risultanti e gli oggetti di costo.  

![Flussi di movimenti produzione.](media/design_details_inventory_costing_14_production_posting_2.png "Flussi di movimenti produzione")  

Il movimento contabile capacità descrive il consumo di capacità in termini di unità di tempo, mentre il corrispondente movimento di valorizzazione descrive il valore del consumo specifico della capacità.  

Il movimento contabile articolo descrive il consumo dei materiali o output in termini di quantità, mentre il movimento di valorizzazione correlato descrive il valore di questo specifico consumo o output di materiale.  

Un movimento di valorizzazione che descrive il valore di magazzino WIP può essere associato a una delle seguenti combinazioni di oggetti di costo:  

-   Una riga dell'ordine di produzione, un centro di lavoro o di produzione e un movimento contabile capacità.  
-   Una riga ordine di produzione, un articolo e un movimento contabile articolo.  
-   Solo una riga dell'ordine di produzione  

Per ulteriori informazioni su come i costi dall'assemblaggio e della produzione vengono registrati nella contabilità generale, vedere [Dettagli di progettazione: Registrazione di magazzino](design-details-inventory-posting.md).  

## Registrazione capacità  
La registrazione dell'output dall'ultima riga del ciclo ordine di produzione comporta la registrazione di un movimento contabile capacità per l'articolo finale, oltre all'aumento di magazzino.  

 Il movimento contabile capacità è un record che indica il tempo dedicato a produrre l'articolo. Il movimento di valorizzazione correlato descrive l'aumento del valore di magazzino WIP, che corrisponde al valore del costo di conversione. Per altre informazioni, vedere "Dal contabile capacità" in [Dettagli di progettazione: Conti nella contabilità generale](design-details-accounts-in-the-general-ledger.md).  

## Determinazione costi ordine di produzione  
 Per controllare i costi di produzione e di magazzino, un'azienda manifatturiera deve misurare il costo degli ordini di produzione, in quanto il costo standard predeterminato di ogni articolo prodotto viene capitalizzato nello stato patrimoniale. Per informazioni sui motivi per i quali gli articoli prodotti utilizzano il metodo di costing standard, vedere [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md).  

> [!NOTE]  
>  Negli ambienti che non utilizzano il metodo di costing standard, viene capitalizzato nel conto patrimoniale il costo effettivo anziché il costo standard degli articoli prodotti.  

Il costo effettivo di un ordine di produzione è costituito dai seguenti componenti di costo:  

-   Costo materiale effettivo  
-   Costo di capacità effettivo o costo di conto lavoro  
-   Costi generali produzione  

I costi effettivi vengono registrati nell'ordine di produzione e confrontati con il costo standard per calcolare gli scostamenti. Gli scostamenti vengono calcolati per ciascun componente di costo dell'articolo: materie prime, capacità, costi dei terzisti, costi generali della capacità e di produzione. È possibile analizzare gli scostamenti per determinare eventuali problemi, ad esempio un eccessivo spreco durante l'elaborazione.  

Negli ambienti con costi standard, il calcolo dei costi di un ordine di produzione si basa sul meccanismo seguente:  

1.  Una volta registrata l'ultima operazione del ciclo, il costo dell'ordine di produzione viene registrato nella contabilità articoli e viene impostato sul costo previsto.  

    Il costo equivale alla quantità di output immessa nelle registrazioni di output moltiplicata per il costo standard che viene copiato dalla scheda articolo. Il costo viene trattato come costo previsto fino al termine dell'ordine di produzione. Per ulteriori informazioni, vedere [Dettagli di progettazione: Registrazione costi previsti](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  È diverso dalla registrazione dell'ordine di assemblaggio, dove vengono sempre registrati i costi effettivi. Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-assembly-order-posting.md).  
2.  Quando l'ordine di produzione viene impostato su **Completato**, l'ordine viene fatturato eseguendo il processo batch **Rettifica costo - Movimenti articoli**. Di conseguenza, il costo totale dell'ordine viene calcolato in base al costo standard dei materiali e della capacità consumati. Gli scostamenti tra i costi standard calcolati e i costi effettivi di produzione vengono calcolati e registrati.  

## Vedi anche  
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Registrazione dell'ordine di assemblaggio](design-details-assembly-order-posting.md)  
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md) [Contabilità](finance.md)  
 [Utilizzare Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]