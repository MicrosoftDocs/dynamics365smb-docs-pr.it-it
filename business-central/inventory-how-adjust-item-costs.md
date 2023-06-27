---
title: Modificare manualmente i costi degli articoli
description: È possibile modificare la valutazione di magazzino di un articolo mediante i metodi di costing Media o FIFO quando cambiano i costi dei prodotti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="adjust-item-costs"></a>Rettifica costi articolo
Il costo di un articolo (valore di magazzino) che si acquista e in seguito si vende può variare nel tempo, ad esempio perché un costo di spedizione viene aggiunto al costo di acquisto dopo che è stato venduto l'articolo. La rettifica dei costi è un'operazione particolarmente importante nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Per conoscere sempre il valore di magazzino corretto, i costi degli articoli devono quindi essere regolarmente rettificati. In questo modo si garantisce che le statistiche relative ai margini siano aggiornate e che gli indicatore KPI finanziari siano corretti. Per ulteriori informazioni, vedere [Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md).

Come regola, il valore nel campo **Costo unitario** nella scheda articolo si basa sul costo standard per gli articoli con un metodo di costing standard. Per gli articoli con tutti gli altri metodi di costing, tale valore viene calcolato dividendo le giacenze attuali, ovvero costi fatturati e costi previsti, per il magazzino. Per ulteriori informazioni vedere [Informazioni sul calcolo costo unitario](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

In [!INCLUDE[prod_short](includes/prod_short.md)]i costi degli articoli vengono rettificati automaticamente ogni volta che avviene una transazione di magazzino , ad esempio quando si registra una fattura di acquisto per un articolo.

È inoltre possibile utilizzare una funzione che consente di rettificare manualmente i costi di uno o più articoli. Ciò risulta utile, ad esempio, quando si è certi che i costi degli articoli vengono modificati per motivi diversi dalle transazioni dell'articolo.

I costi dell'articolo vengono rettificati dal metodo di costing FIFO o Media, a seconda dell'opzione selezionata nella guida al setup assistito **Imposta società** o nel campo **Metodo di costing** della scheda articolo. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).  

Se si utilizza il metodo di costing FIFO, il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo. Il magazzino viene valutato presupponendo che il primo articolo posizionato nel magazzino venga venduto per primo.

Se si utilizza il metodo di costing Media, il costo unitario di un articolo viene calcolato come il costo unitario medio in ogni momento dopo un acquisto. Il magazzino viene valutato presupponendo che tutte le giacenze siano vendute simultaneamente. Per gli articoli che utilizzano il metodo di costing, è possibile selezionare il campo **Costo unitario** nella scheda articolo per visualizzare lo storico delle transazioni da cui viene calcolato il costo medio

Tramite i processi della funzione di rettifica dei costi vengono elaborati solo i movimenti di valorizzazione che non sono ancora stati rettificati. Se si verifica una situazione in cui è necessario trasferire costi in entrata modificati ai movimenti in uscita associati, vengono creati nuovi movimenti di valorizzazione di rettifica, basati sulle informazioni dei movimenti di valorizzazione originali, ma che contengono l'importo di rettifica. La funzione di rettifica dei costi viene utilizzata la data di registrazione del movimento di valorizzazione originale, a meno che tale data non sia inclusa in un periodo di magazzino chiuso. In tal caso, viene utilizzata la data di inizio del successivo periodo di magazzino aperto. Se non si utilizzano i periodi magazzino, la data nel campo **Consenti registraz. da** della pagina **Setup contabilità generale** verrà definita quando la rettifica viene registrata.

## <a name="to-adjust-item-costs-manually"></a>Per rettificare i costi degli articoli manualmente
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Rettifica costo - Mov. art.**, quindi scegli il collegamento correlato.
2. Nella pagina **Rettifica costo - Movimenti articoli** specificare per quali articoli rettificare i costi.
3. Scegliere il pulsante **OK**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Per apportare modifiche generali nel costo diretto unitario
Se si desidera modificare il costo diretto unitario per vari articoli, si può utilizzare il processo batch **Rett. costi/Prezzi articoli**.  

 Il processo batch modificherà il contenuto del campo **Prezzo unitario** della scheda articolo. Il contenuto del campo verrà modificato nello stesso modo per tutti gli articoli o per quelli selezionati. La modifica viene eseguita moltiplicando il valore nel campo per un fattore di rettifica specificato.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Rettifica costi/prezzi articoli**, quindi scegli il collegamento correlato.  
2. Nel campo **Rettifica campo**, indicare il campo della scheda articolo o SKU da rettificare.  
3. Nel campo **Fattore rettifica** specificare il fattore in base al quale il valore verrà rettificato. Ad esempio, immettere **1,5** per aumentare il valore del 50%.  
4. Nella Scheda dettaglio **Articolo**, impostare i filtri per specificare, per esempio, gli articoli da lavorare con il processo batch.  
5. Scegliere il pulsante **OK**.  

## <a name="understanding-unit-cost-calculation"></a>Informazioni sul calcolo costo unitario
Come regola, il valore nel campo **Costo unitario** nella scheda articolo si basa sul costo standard per gli articoli con un metodo di costing standard. Per gli articoli con tutti gli altri metodi di costing, tale valore viene calcolato dividendo le giacenze attuali, ovvero costi fatturati e costi previsti, per il magazzino.  

 Il modo in cui il contenuto del campo **Metodo di Costing** influisce sul calcolo dei costi unitari per gli acquisti e per le vendite è descritto in modo più dettagliato nelle sezioni illustrate di seguito.  

## <a name="unit-cost-calculation-for-purchases"></a>Calcolo del costo unitario per gli acquisti
 Quando si acquistano degli articoli, il valore contenuto nel campo **Ultimo costo diretto** nella scheda articolo viene copiato nel campo **Costo unitario diretto** di una riga di acquisto oppure nella riga Importo unitario di una riga di registrazione magazzino.  

 In base all'opzione selezionata nel campo **Metodo di costing**, [!INCLUDE[prod_short](includes/prod_short.md)] calcola il contenuto del campo **Costo Unitario** delle righe.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Metodo di costing FIFO, LIFO, Specifico o Medio
 [!INCLUDE[prod_short](includes/prod_short.md)] calcola il contenuto del campo **Costo unitario VL** della riga di acquisto o il contenuto del campo **Costo unitario** della riga di registrazione magazzino in base alla seguente formula:  

 Costo unitario (VL) = (Costo diretto unitario - (Importo sconto/ Quantità)) * (1 + Costo indiretto % / 100) + Coefficiente costi generali  

### <a name="costing-method-standard"></a>Metodo di costing standard
 Il campo **Costo Unitario (VL)** nella riga di acquisto e il campo **Costo Unitario** nella riga di registrazioni magazzino vengono compilati automaticamente copiando il valore nel campo **Costo Unitario** nella scheda relativa all'articolo. Utilizzando il metodo di costing impostato come Standard, il valore di riferimento è sempre il costo standard.  

 Alla registrazione dell'acquisto, il costo unitario viene copiato dalla riga di acquisto o dalla riga di registrazioni magazzino nella fattura di acquisto e può essere visualizzato nella lista dei movimenti relativi all'articolo.  

### <a name="all-costing-methods"></a>Tutti i metodi di costing
 Per calcolare il contenuto del campo **Importo costo effettivo** oppure, se pertinente, del campo **Importo costo previsto** relativo a questo movimento articolo viene sempre utilizzato il costo unitario indicato nella riga del documento di origine, indipendentemente dal metodo di costing dell'articolo.  

## <a name="unit-cost-calculation-for-sales"></a>Calcolo del costo unitario per le vendite
 Quando vengono venduti degli articoli, il costo unitario viene copiato dal campo Costo unitario della scheda articolo alla riga di vendita o la riga di registrazioni di magazzino.  

 Al momento della registrazione, il costo unitario viene copiato nella fattura di vendita dell'articolo e può essere visualizzato nella lista dei movimenti relativi all'articolo. Il costo unitario indicato nella riga del documento di origine viene utilizzato da [!INCLUDE[prod_short](includes/prod_short.md)] per calcolare il contenuto del campo **Importo costo effettivo** oppure, se pertinente, del campo **Importo costo previsto** nel movimento di valorizzazione connesso a questo movimento articolo.  

## <a name="see-also"></a>Vedi anche
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
