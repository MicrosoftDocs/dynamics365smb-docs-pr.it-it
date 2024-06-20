---
title: 'Dettagli di progettazione: Riconciliazione con la contabilità generale | Microsoft Docs'
description: 'Questo argomento descrive la riconciliazione con la contabilità generale quando si registrano transazioni di magazzino, ad esempio spedizioni vendite, output di produzione o rettifiche negative.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, reconciliation, general ledger, inventory'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Dettagli di progettazione: Riconciliazione con la contabilità generale
Quando si registrano transazioni di magazzino, ad esempio spedizioni vendite, output di produzione o rettifiche negative, le modifiche alla quantità e al valore del magazzino vengono registrate rispettivamente nei movimenti contabili articoli e nei movimenti di valorizzazione. È quindi necessario registrare i valori di magazzino nei conti giacenza magazzino nella contabilità generale.  

Esistono due modi per riconciliare i movimenti di magazzino con la contabilità generale:  

* Manualmente, tramite l'esecuzione del processo batch **Registra costo magazzino in CG**.  
* Automaticamente, ogni volta che si registra una transazione di magazzino.  

## Processo batch Registra costo magazzino in C/G  
Se si esegue il processo batch **Registra costo magazzino in CG**, i movimenti di contabilità generale vengono creati in base ai movimenti di valorizzazione. È possibile scegliere di riepilogare i movimenti di contabilità generale per ogni movimento di valorizzazione oppure di creare movimenti di contabilità generale per ogni combinazione di data di registrazione, codice ubicazione, categoria di registrazione magazzino, categoria di registrazione business e categoria di registrazione di articoli o servizi.  

Le date di registrazione dei movimenti di contabilità generale vengono impostate sulla data di registrazione del movimento di valorizzazione corrispondente, eccetto quando il movimento di valorizzazione ricade in un periodo contabile chiuso. In questo caso, il movimento di valorizzazione viene ignorato ed è necessario modificare il setup della contabilità generale o il setup utente per abilitare la registrazione nell'intervallo di date.  

Quando si esegue il processo batch **Registra costo magazzino in CG**, è possibile che si verifichino degli errori a causa di impostazioni mancanti o di impostazioni delle dimensioni incompatibili. Se vengono rilevati errori nel setup delle dimensioni, questi vengono ignorati e vengono utilizzate le dimensioni del movimento di valorizzazione. In caso di errori di altro tipo, il processo batch non registra i movimenti di valore e li elenca alla fine del report in una sezione intitolata **Movimenti saltati**. Per registrare questi movimenti, è prima necessario correggere gli errori. Per visualizzare un elenco di errori prima di eseguire il processo batch, è possibile eseguire il report **Registra costo mag. in C/G - Test**. Nel report vengono elencati tutti gli errori che si verificano durante una registrazione di test. È quindi possibile correggere gli errori e quindi eseguire il processo batch di registrazione del costo di magazzino senza saltare alcun movimento.  

## Reg. automatica costi  
Per impostare l'esecuzione automatica della registrazione costi nella contabilità generale quando si registra una transazione di magazzino, selezionare la casella di controllo **Reg. automatica costi** nella pagina **Setup magazzino**. La data di registrazione del movimento di contabilità generale corrisponde alla data di registrazione del movimento contabile articolo.  

## Tipi conto  
Durante la riconciliazione, i valori di magazzino vengano registrati nei conti giacenza magazzino nel conto patrimoniale. La stessa quantità, ma con segno opposto, viene registrata nel conto profitti/perdite pertinente. Normalmente la contropartita è un conto di bilancio patrimoniale. Tuttavia, quando si registra un costo diretto correlato al consumo o all'output, la contropartita è un conto di bilancio patrimoniale. Il tipo di movimento contabile articolo e di movimento di valorizzazione determina il conto di contabilità generale in cui registrare.  

Il tipo di movimento indica in quale conto di contabilità generale effettuare la registrazione. Questo è determinato dal segno della quantità nel movimento contabile articolo o della quantità valutata nel movimento di valorizzazione, poiché le quantità hanno sempre lo stesso segno. Ad esempio, un movimento di vendita con una quantità positiva descrive una riduzione di magazzino causata da una vendita e un movimento di vendita con una quantità negativa descrive un aumento di magazzino causata da un reso di vendita.  

### Esempio  
Nel seguente esempio viene visualizzata una catena di bicicletta fabbricata da collegamenti acquistati. In questo esempio viene mostrato in che modo vengono utilizzati i vari tipi di conto di contabilità generale in uno scenario standard.  

La casella di controllo **Reg. costi previsti in CG** nella pagina **Setup magazzino** viene selezionata e viene definita la configurazione seguente.  

La tabella seguente indica in che modo il collegamento è impostato nella scheda articolo.  

|Campo Setup|Valore|  
|-----------------|-----------|  
|**Metodo di costing**|Standard|  
|**Costo standard**|1,00 VL|  
|**Coefficiente costi generali**|0,02 VL|  

La tabella seguente indica in che modo la catena è impostata nella scheda articolo.  

|Campo Setup|Valore|  
|-----------------|-----------|  
|**Metodo di costing**|Standard|  
|**Costo standard**|150,00 VL|  
|**Coefficiente costi generali**|25,00 VL|  

La tabella seguente indica in che modo l'area di produzione è impostata nella scheda area di produzione.  

|Campo Setup|Valore|  
|-----------------|-----------|  
|**Costo Diretto Unitario**|2,00 VL|  
|**Percentuale di costo indiretto**|10|  

##### Scenario  
1. L'utente acquista 150 collegamenti e registra l'ordine di acquisto come ricevuto. (Acquisti)  
2. L'utente registra l'ordine di acquisto come fatturato. Viene quindi creato un importo dei costi generali di VL 3,00 da allocare e un importo di scostamento di VL 18,00. (Acquisti)  

    1. I conti provvisori vengono cancellati. (Acquisti)  
    2. Il costo diretto viene registrato. (Acquisti)  
    3. Il costo indiretto viene calcolato e registrato. (Acquisti)  
    4. Lo scostamento acquisto viene calcolato e registrato (solo per gli articoli con costo standard). (Acquisti)  
3. L'utente vende una catena e registra l'ordine di vendita come spedito. (Vendita)  
4. L'utente registra l'ordine di vendita come fatturato. (Vendita)  

    1. I conti provvisori vengono cancellati. (Vendita)  
    2. Il costo COGS viene registrato. (Vendita)  

        ![Risultati della registrazione della vendita nei conti C/G.](media/design_details_inventory_costing_3_gl_posting_sales.png "Risultati della registrazione della vendita nei conti C/G")  
5. L'utente registra il consumo di 150 collegamenti, ovvero il numero di collegamenti utilizzati per produrre una catena. (Consumo, materiali)  

    ![Risultati della registrazione dei materiali nei conti C/G.](media/design_details_inventory_costing_3_gl_posting_material.png "Risultati della registrazione dei materiali nei conti C/G")  
6. L'area di produzione ha utilizzato 60 minuti per produrre la catena. L'utente registra il costo di conversione. (Consumo, Capacità)  

    1. I costi diretti vengono registrati. (Consumo, Capacità)  
    2. I costi indiretti vengono calcolati e registrati. (Consumo, Capacità)  

        ![Risultati della registrazione della capacità nei conti C/G.](media/design_details_inventory_costing_3_gl_posting_capacity.png "Risultati della registrazione della capacità nei conti C/G")  
7. L'utente registra il costo previsto di una catena. (Output)  
8. L'utente completa l'ordine di produzione ed esegue il processo batch **Rettifica costo - Movimenti articoli**. (Output)  

    1. I conti provvisori vengono cancellati. (Output)  
    2. Il costo diretto viene trasferito dal conto WIP al conto magazzino. (Output)  
    3. Il costo diretto (costo generale) viene trasferito dal conto dei costi indiretti al conto del magazzino. (Output)  
    4. Ciò risulta in un importo di scostamento di VL 157,00. Gli scostamenti vengono calcolati solo per gli articoli con costo standard. (Output)  

        ![Risultati della registrazione dell'output nei conti C/G.](media/design_details_inventory_costing_3_gl_posting_output.png "Risultati della registrazione dell'output nei conti C/G")  

        > [!NOTE]  
        >  Per semplicità, viene visualizzato solo un solo conto di scostamento. In realtà, sono disponibili cinque diversi conti:  
        >   
        >  * Scost. su mat.  
        >  * Scostamenti capacità  
        >  * Scostamento costi gen. capacità  
        >  * Scost. conto lav.  
        >  * Scostamento costi generali produzione  

9. L'utente rivaluta la catena da VL 150,00 a VL 140,00. (Rettifica/Rivalutazione/Arrotondamento/Trasferimento)  

    ![Risultati della registrazione della rettifica nei conti C/G.](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Risultati della registrazione della rettifica nei conti C/G")  

Per ulteriori informazioni sulla relazione tra i tipi di conto e i diversi tipi di movimenti di valorizzazione, vedere [Dettagli di progettazione: Conti nella contabilità generale](design-details-accounts-in-the-general-ledger.md).  

## Vedi anche  
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
[Dettagli di progettazione: Registrazione del costo previsto](design-details-expected-cost-posting.md)   
[Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]