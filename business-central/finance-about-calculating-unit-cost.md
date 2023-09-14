---
title: Informazioni sul calcolo costo unitario
description: Scopri come il metodo di determinazione dei costi e altri fattori influenzano il campo Costo unitario della scheda Articolo.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: bholtorf
---
# Informazioni sul calcolo costo unitario

Ogni articolo ha un costo unitario che viene calcolato in base al metodo di determinazione dei costi dell'azienda e ad altri fattori. Di regola, il valore nel campo **Costo unitario** si basa sul costo *Standard* per l'articolo. Per tutti gli altri metodi di costo (*FIFO*, *LIFO*, *Specifico*, e *Media*), il costo unitario viene calcolato in base al costo unitario medio in un periodo di tempo.  

Per ulteriori informazioni, vedere [Gestione dei costi di magazzino](finance-manage-inventory-costs.md).  

## Quando viene aggiornato il campo del costo unitario

Il metodo di determinazione dei costi scelto influisce sull'aggiornamento del campo **Costo unitario**.

Quando il metodo di determinazione dei costi è impostato su *Standard*, il campo **Costo unitario** viene aggiornato ogni volta che viene modificato il costo standard e gli utenti non possono modificare il campo **Costo unitario**. Per ulteriori informazioni, vedi [Aggiornamento dei costi standard](finance-how-to-update-standard-costs.md).

Se il metodo di costing è *FIFO*, *LIFO*, *Specifico*, o *Media*, il **costo unitario** viene aggiornato nei casi seguenti:

* Quando il costo dell'articolo viene rettificato, automaticamente o tramite un'attività [Rettifica costo](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Durante la registrazione della rettifica di fatture di acquisto, output o positiva se una delle seguenti condizioni è vera:
  * La quantità netta fatturata dell'articolo passa da un valore negativo, o zero, a un valore positivo.
  * Il costo unitario attuale è zero.

Se una di queste condizioni è vera, il campo **Costo unitario** viene aggiornato con il valore del campo **Ultimo costo diretto** relativo della scheda articolo.

> [!NOTE]
> Il campo **Costo unitario** non viene aggiornato se il costo unitario corrente è maggiore di zero e il nuovo costo unitario è zero. Un costo unitario pari a zero è considerato un'eccezione rispetto alle normali attività. Pertanto, l'attuale costo unitario viene mantenuto per fornire l'ultimo valore noto e rilevante. Questa eccezione si applica anche se l'inventario esistente è stato rivalutato a zero.

Nel campo **Costo unitario** della scheda articolo, è possibile visualizzare la cronologia delle transazioni da cui viene calcolato il costo medio delle unità disponibili nel **Panoramica del calcolo dei costi medi**.

## Calcolo del costo unitario per gli acquisti

Quando si acquistano degli articoli, il valore contenuto nel campo **Ultimo costo diretto** nella scheda articolo viene copiato nel campo **Costo unitario diretto** di una riga di acquisto oppure nella riga **Importo unitario** di una riga di registrazione magazzino.

In base all'opzione selezionata nel campo **Metodo di costing**, [!INCLUDE[prod_short](includes/prod_short.md)] calcola il contenuto del campo **Costo Unitario** delle righe.

### Metodo di costing FIFO, LIFO, Specifico o Medio

[!INCLUDE[prod_short](includes/prod_short.md)] calcola il contenuto del campo **Costo unitario VL** della riga di acquisto o il contenuto del campo **Costo unitario** della riga di registrazione magazzino in base alla seguente formula:

*Costo unitario (VL) = (Costo diretto unitario - (Importo sconto / Quantità)) x (1 + Costo indiretto % / 100) + Coefficiente costi generali*

### Metodo di costing standard

Il campo **Costo Unitario (VL)** nella riga di acquisto e il campo **Costo Unitario** nella riga di registrazioni magazzino vengono compilati automaticamente copiando il valore nel campo **Costo Unitario** nella scheda relativa all'articolo. Utilizzando il metodo di costing impostato come *Standard*, il valore di riferimento è sempre il costo standard.

Alla registrazione dell'acquisto, [!INCLUDE[prod_short](includes/prod_short.md)] usa il costo unitario dalla riga di acquisto o dalla riga di registrazioni magazzino nella fattura di acquisto. Puoi vederlo nell'elenco di voci per l'articolo.

### Tutti i metodi di costing

Per calcolare il contenuto del campo **Importo costo effettivo** oppure, se pertinente, del campo **Importo costo previsto** relativo a questo movimento articolo viene sempre utilizzato il costo unitario indicato nella riga del documento di origine, indipendentemente dal metodo di costing dell'articolo.

## Calcolo del costo unitario per le vendite

Quando vengono venduti degli articoli, il costo unitario viene copiato dal campo **Costo unitario** della scheda articolo alla riga di vendita o la riga di registrazioni di magazzino.

Al momento della registrazione, il costo unitario viene copiato nella fattura di vendita dell'articolo e può essere visualizzato nella lista dei movimenti relativi all'articolo. Il costo unitario indicato nella riga del documento di origine viene utilizzato da [!INCLUDE[prod_short](includes/prod_short.md)] per calcolare il contenuto del campo **Importo costo effettivo** oppure, se pertinente, del campo **Importo costo previsto** nel movimento di valorizzazione connesso a questo movimento articolo.

## Vedere anche

[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Registrazione di nuovi articoli](inventory-how-register-new-items.md)  
[Informazioni sulla determinazione dei costi di magazzino](finance-learn-about-costing.md)  
[Magazzino](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: IVA non detraibile](design-details-nondeductible-vat.md)
[Impostare le procedure ottimali: metodo di costing](setup-best-practices-costing-method.md)  
[Dettagli di progettazione: metodi di determinazione dei costi](design-details-costing-methods.md)  
[Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
