---
title: 'Dettagli di progettazione: Conti nella contabilità generale | Microsoft Docs'
description: 'Per riconciliare i movimenti di inventario e i movimenti contabili capacità con la contabilità generale, i movimenti di valorizzazione correlati vengono registrati in conti diversi nella contabilità generale.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Dettagli di progettazione: Conti nella contabilità generale
Per riconciliare i movimenti di inventario e i movimenti contabili capacità con la contabilità generale, i movimenti di valorizzazione correlati vengono registrati in conti diversi nella contabilità generale. Per ulteriori informazioni, vedere [Dettagli di progettazione: Riconciliazione con la contabilità generale](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Dai contabili inventario
Nella seguente tabella viene mostrata la relazione tra i diversi tipi di movimenti di valorizzazione magazzino e i conti e le contropartite nella contabilità generale.  

|**Tipo mov. articolo**|**Tipo mov. valorizz.**|**Tipo scostamento**|**Costo previsto**|**Conto**|**Contropartita**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Acquisto|Costo diretto||Sì|Magazzino (Provvis.)|Conto ratei magaz. (provvis.)|  
|Acquisto|Costo diretto||No|Magazzino|Costo diretto collegato|  
|Acquisto|Costo indiretto||No|Magazzino|Costi generali collegati|  
|Acquisto|Scostamenti|Acquisto|No|Magazzino|Scostamento acquisto|  
|Acquisto|Rivalutazione||No|Magazzino|Rettifica magazzino|  
|Acquisto|Arrotondamento||No|Magazzino|Rettifica magazzino|  
|Vendita|Costo diretto||Sì|Magazzino (Provvis.)|COGS (Provvis.)|  
|Vendita|Costo diretto||No|Magazzino|COGS|  
|Vendita|Rivalutazione||No|Magazzino|Rettifica magazzino|  
|Vendita|Arrotondamento||No|Magazzino|Rettifica magazzino|  
|Rettifiche Positive,Rettifiche Negative, Trasferimento|Costo diretto||No|Magazzino|Rettifica magazzino|  
|Rettifiche Positive,Rettifiche Negative, Trasferimento|Rivalutazione||No|Magazzino|Rettifica magazzino|  
|Rettifiche Positive,Rettifiche Negative, Trasferimento|Arrotondamento||No|Magazzino|Rettifica magazzino|  
|Consumo (produzione)|Costo diretto||No|Magazzino|WIP|  
|Consumo (produzione)|Rivalutazione||No|Magazzino|Rettifica magazzino|  
|Consumo (produzione)|Arrotondamento||No|Magazzino|Rettifica magazzino|  
|Consumo assemblaggio|Costo diretto||No|Magazzino|Rettifica magazzino|  
|Consumo assemblaggio|Costo diretto||No|Costo diretto collegato|Rettifica magazzino|  
|Consumo assemblaggio|Costo indiretto||No|Costi generali collegati|Rettifica magazzino|  
|Output (produzione)|Costo diretto||Sì|Magazzino (Provvis.)|WIP|  
|Output (produzione)|Costo diretto||No|Magazzino|WIP|  
|Output (produzione)|Costo indiretto||No|Magazzino|Costi generali collegati|  
|Output (produzione)|Scostamenti|Materiale|No|Magazzino|Scost. su mat.|  
|Output (produzione)|Scostamenti|Capacità|No|Magazzino|Scostamenti capacità|  
|Output (produzione)|Scostamenti|Conto lavoro|No|Magazzino|Scost. conto lav.|  
|Output (produzione)|Scostamenti|Costi generali capacità|No|Magazzino|Scost. costi gen. cap.|  
|Output (produzione)|Scostamenti|Costi generali produzione|No|Magazzino|Scost. costi gen. mfg|  
|Output (produzione)|Rivalutazione||No|Magazzino|Rettifica magazzino|  
|Output (produzione)|Arrotondamento||No|Magazzino|Rettifica magazzino|  
|Output assemblaggio|Costo diretto||No|Magazzino|Rettifica magazzino|  
|Output assemblaggio|Rivalutazione||No|Magazzino|Rettifica magazzino|  
|Output assemblaggio|Costo indiretto||No|Magazzino|Costi generali collegati|  
|Output assemblaggio|Scostamenti|Materiale|No|Magazzino|Scost. su mat.|  
|Output assemblaggio|Scostamenti|Capacità|No|Magazzino|Scostamenti capacità|  
|Output assemblaggio|Scostamenti|Costi generali capacità|No|Magazzino|Scost. costi gen. cap.|  
|Output assemblaggio|Scostamenti|Costi generali produzione|No|Magazzino|Scost. costi gen. mfg|  
|Output assemblaggio|Arrotondamento||No|Magazzino|Rettifica magazzino|  

## <a name="from-the-capacity-ledger"></a>Dal contabile capacità
 Nella seguente tabella viene mostrata la relazione tra i diversi tipi di movimenti di valorizzazione capacità e i conti e le contropartite nella contabilità generale. I movimenti contabili capacità rappresentano il tempo di lavoro utilizzato nel lavoro di assemblaggio o di produzione.  

|**Tipo di lavoro**|**Tipo mov. contabile capacità**|**Tipo mov. valorizz.**|**Conto**|**Contropartita**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Assemblaggio|Risorsa|Costo diretto|Costo diretto collegato|Rettifica magazzino|  
|Assemblaggio|Risorsa|Costo Indiretto|Costi generali collegati|Rettifica magazzino|  
|Produzione|Centro di lavoro/Area di produzione|Costo Diretto|Conto WIP|Costo diretto collegato|  
|Produzione|Centro di lavoro/Area di produzione|Costo Indiretto|Conto WIP|Costi generali collegati|  

## <a name="assembly-costs-are-always-actual"></a>I costi di assemblaggio sono sempre effettivi
 Come illustrato nella tabella precedente, le registrazioni di assemblaggio non sono rappresentate nei conti provvisori. Questo perché il concetto di semilavorati (WIP) non si applica alla registrazione di output assemblaggio, a differenza della registrazione dell'output di produzione. I costi di assemblaggio vengono registrati solo come costo effettivo, mai come costo previsto.  

 Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Calcolo della quantità da registrare nella contabilità generale
 I seguenti campi nella tabella **Movimenti valorizzazione** vengono utilizzati per calcolare l'importo del costo previsto che viene registrato nella contabilità generale:  

-   Importo costo (effettivo)  
-   Costo registrato in C/G  
-   Importo costo (previsto)  
-   Costo prev. registrato in C/G  

Nella seguente tabella viene mostrato in che modo vengono calcolati gli importi da registrare nella contabilità generale per i due diversi tipi di costo.  

|Tipo costo|Calcolo|  
|---------------|-----------------|  
|Costo effettivo|Importo Costo (Effettivo) - Costo Registrato in C/G|  
|Costo previsto|Importo Costo (Previsto) - Costo Registrato in C/G|  

## <a name="see-also"></a>Vedi anche
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Registrazione di magazzino](design-details-inventory-posting.md)   
 [Dettagli di progettazione: Registrazione del costo previsto](design-details-expected-cost-posting.md)  
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
