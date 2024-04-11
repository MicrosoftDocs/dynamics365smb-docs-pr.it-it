---
title: Rettificare manualmente i costi degli articoli
description: È possibile rettificare la valutazione di magazzino di un articolo mediante i metodi di costing Media o FIFO quando cambiano i costi dei prodotti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="adjust-item-costs"></a>Rettificare i costi degli articoli

Il costo di un articolo (valore di magazzino) che si acquista e in seguito si vende potrebbe variare durante il relativo ciclo di vita, ad esempio perché un costo di spedizione viene aggiunto al costo di acquisto dopo la vendita dell'articolo. La rettifica dei costi è un'operazione particolarmente importante nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Per conoscere sempre il valore di magazzino corretto, devi regolarmente rettificare i costi degli articoli. I costi corretti garantiscono che le statistiche relative a vendite e margini siano aggiornate e che gli indicatori KPI finanziari siano corretti. Per ulteriori informazioni, vedere [Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md).

Il valore nel campo **Costo unitario** nella scheda articolo si basa sul costo standard per gli articoli con il metodo di costing Standard. Per gli articoli con qualsiasi altro metodo di costing, il valore è basato sul calcolo delle scorte disponibili, ovvero costi fatturati e costi previsti, diviso per la giacenza. Per ulteriori informazioni vedere [Informazioni sul calcolo costo unitario](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

In [!INCLUDE[prod_short](includes/prod_short.md)]i costi degli articoli vengono rettificati automaticamente ogni volta che avviene una transazione di magazzino , ad esempio quando si registra una fattura di acquisto per un articolo.

È inoltre possibile rettificare manualmente i costi di uno o più articoli. Ad esempio, le rettifiche manuali sono utili quando si sa che i costi degli articoli vengono modificati per motivi diversi dalle transazioni dell'articolo.

I costi dell'articolo vengono rettificati dal metodo di costing FIFO o Media, a seconda dell'opzione selezionata nella guida al setup assistito **Imposta società** o nel campo **Metodo di costing** della scheda articolo. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).  

Per il metodo di costing FIFO, il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo. Il magazzino viene valutato presupponendo che il primo articolo posizionato nel magazzino venga venduto per primo.

Se si utilizza il metodo di costing Media, il costo unitario di un articolo viene calcolato come il costo unitario medio in ogni momento dopo un acquisto. Il magazzino viene valutato presupponendo che tutte le giacenze siano vendute simultaneamente. Per gli articoli che utilizzano il metodo di costing, è possibile selezionare il campo **Costo unitario** nella scheda articolo per visualizzare lo storico delle transazioni da cui viene calcolato il costo medio

La rettifica dei costi elabora solo i movimenti di valorizzazione che non sono rettificati. In una situazione in cui i costi in entrata modificati devono essere inoltrati ai movimenti di uscita correlati, crea nuovi movimenti di valorizzazione di rettifica. I movimenti di valorizzazione di rettifica si basano sulle informazioni nei movimenti di valorizzazione originali ma includono l'importo di rettifica. La funzione di rettifica dei costi viene utilizzata la data di registrazione del movimento di valorizzazione originale, a meno che tale data non sia inclusa in un periodo di magazzino chiuso. In tal caso, viene utilizzata la data di inizio del successivo periodo di magazzino aperto. Se non si utilizzano periodi magazzino, la data nel campo **Consenti registraz. da** della pagina **Setup contabilità generale** definisce quando il movimento di rettifica viene registrato.

## <a name="to-adjust-item-costs-manually"></a>Per rettificare i costi degli articoli manualmente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Rettifica costo - Mov. art.**, quindi scegli il collegamento correlato.
2. Nella pagina **Rettifica costo - Movimenti articoli** specificare per quali articoli rettificare i costi.
3. Scegliere il pulsante **OK**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Per apportare modifiche generali nel costo diretto unitario

Se si desidera modificare il costo diretto unitario per vari articoli, si può utilizzare il processo batch **Rett. costi/Prezzi articoli**.  

Il processo batch modificherà il contenuto del campo **Prezzo unitario** della scheda articolo. Il contenuto del campo verrà modificato nello stesso modo per tutti gli articoli o per quelli selezionati. La modifica viene eseguita moltiplicando il valore nel campo per un fattore di rettifica specificato.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Rettifica costi/prezzi articoli**, quindi scegli il collegamento correlato.  
2. Nel campo **Rettifica campo**, indicare il campo della scheda articolo o SKU da rettificare.  
3. Nel campo **Fattore rettifica** specifica il fattore in base al quale il valore viene rettificato. Ad esempio, immettere **1,5** per aumentare il valore del 50%.  
4. Nella Scheda dettaglio **Articolo**, impostare i filtri per specificare, per esempio, gli articoli da lavorare con il processo batch.  
5. Scegli il pulsante **OK**.  

## <a name="understanding-unit-cost-calculation"></a>Informazioni sul calcolo del costo unitario

Il valore nel campo **Costo unitario** nella scheda articolo si basa sul costo standard per gli articoli con il metodo di costing Standard. Per gli articoli con qualsiasi altro metodo di costing, il valore viene calcolato dividendo le scorte disponibili, ovvero costi fatturati e costi previsti, per la giacenza.  

Il modo in cui il contenuto del campo **Metodo di Costing** influisce sul calcolo dei costi unitari per gli acquisti e per le vendite è descritto in modo più dettagliato nelle sezioni illustrate di seguito.  

## <a name="unit-cost-calculation-for-purchases"></a>Calcolo del costo unitario per gli acquisti

Quando si acquistano degli articoli, il valore contenuto nel campo **Ultimo costo diretto** nella scheda articolo viene copiato nel campo **Costo unitario diretto** di una riga di acquisto oppure nella riga **Importo unitario** di una riga di registrazione magazzino.  

In base all'opzione selezionata nel campo **Metodo di costing**, [!INCLUDE[prod_short](includes/prod_short.md)] calcola il contenuto del campo **Costo Unitario** delle righe.  

### <a name="fifo-lifo-specific-or-average-costing-methods"></a>Metodi di costing FIFO, LIFO, Specifico o Medio

[!INCLUDE[prod_short](includes/prod_short.md)] utilizza la seguente formula per calcolare il contenuto del campo **Costo unitario VL** nella riga di acquisto o il contenuto del campo **Costo unitario** nella riga di registrazione magazzino:  

Costo unitario (VL) = (Costo diretto unitario - (Importo sconto/ Quantità)) * (1 + Costo indiretto % / 100) + Coefficiente costi generali  

### <a name="standard-costing-method"></a>Metodo di costing Standard

Il campo **Costo Unitario (VL)** nella riga di acquisto e il campo **Costo Unitario** nella riga di registrazioni magazzino vengono compilati automaticamente copiando il valore nel campo **Costo Unitario** nella scheda relativa all'articolo. Se usi il metodo di costing Standard, il valore è sempre basato sul costo standard.  

Alla registrazione di un acquisto, il costo unitario della riga di acquisto o dalla riga di registrazione magazzino viene copiato nella fattura di acquisto. Viene visualizzato nell'elenco di movimenti per l'articolo.  

### <a name="all-costing-methods"></a>Tutti i metodi di costing

Il costo unitario nella riga del documento di origine viene utilizzato per calcolare il valore del campo **Importo costo effettivo** oppure, se pertinente, del campo **Importo costo previsto** correlato a questo movimento articolo. Il costo è incluso nel calcolo indipendentemente dal metodo di costing dell'articolo.  

## <a name="unit-cost-calculation-for-sales"></a>Calcolo del costo unitario per le vendite

Quando vendi gli articoli, il costo unitario viene copiato dal campo **Costo unitario** della scheda articolo alla riga di vendita o alla riga di registrazione magazzino.  

Al momento della registrazione, il costo unitario viene copiato nel movimento dell'articolo nella fattura di vendita e viene visualizzato nell'elenco dei movimenti relativi all'articolo. Il costo unitario nella riga del documento di origine viene utilizzato da [!INCLUDE[prod_short](includes/prod_short.md)] per calcolare il contenuto del campo **Importo costo effettivo** oppure, se pertinente, del campo **Importo costo previsto** nel movimento di valorizzazione correlato a questo movimento articolo.  

## <a name="track-item-cost-adjustments"></a>Tenere traccia delle rettifiche dei costi degli articoli

I costi degli articoli possono cambiare per molti motivi, quindi è importante tenere traccia delle rettifiche dei costi. Utilizza la pagina **Rettifica costo inventario** per gestire e monitorare il processo di rettifica dei costi. In questa pagina vengono visualizzati gli articoli insieme ai relativi parametri di costing e allo stato di rettifica dei costi. Puoi filtrare l'elenco per concentrarti sugli articoli che richiedono una rettifica o che sono esclusi dal processo di rettifica dei costi. Per ulteriori informazioni sulla tracciabilità delle rettifiche dei costi, vedi [Tenere traccia delle rettifiche dei costi degli articoli](finance-track-inventory-costs.md).

## <a name="see-also"></a>Vedere anche

[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Inventario](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
