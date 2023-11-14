---
title: Assegnare addebiti articoli a vendite e acquisti (video)
description: 'Assegna gli addebiti articolo quando è necessario che gli articoli di magazzino sostengano costi aggiuntivi, come il trasporto e la movimentazione fisica.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 06/22/2021
ms.author: bholtorf
---
# Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali

Per una valutazione corretta, è necessario includere nei movimenti di magazzino tutti i costi aggiuntivi, quali spedizione, gestione fisica, assicurazione e trasporto sostenuti per l'acquisto o la vendita degli articoli. Per gli acquisti, il costo franco di tutte le spese allo sbarco di un articolo acquistato è dato dal prezzo di acquisto del fornitore più tutti gli addebiti articolo diretti aggiuntivi che è possibile assegnare ai singoli carichi o alle singole spedizioni di reso. Per le vendite, per un'azienda conoscere il costo della spedizione di articoli venduti è altrettanto importante che conoscere il costo franco di tutte le spese di sbarco degli articoli acquistati.

Oltre a registrare il costo aggiuntivo nel valore di magazzino, è possibile utilizzare la funzionalità addebiti per le seguenti attività:

* Determinare il costo franco di tutte le spese allo sbarco di un articolo allo scopo di stabilire strategie più accurate di ottimizzazione della rete di distribuzione.
* Scomporre il costo unitario o il prezzo unitario di un articolo a scopo di analisi.
* Includi gli abbuoni sugli acquisti nel costo unitario e gli abbuoni sulle vendite nel prezzo unitario.

Prima di poter assegnare gli addebiti articolo, è necessario impostare i numeri di addebito articolo per i diversi tipi di addebito articolo. I numeri includono in quali conti C/G registrare i costi relativi a vendite, acquisti e rettifiche di magazzino. Un numero di addebito articolo contiene una combinazione di gruppi di registrazioni di prodotti generali, codici di gruppi imposta, gruppo di registrazione di prodotti IVA e addebiti articoli. Quando si inserisce il numero di addebito articolo in un documento di acquisto o di vendita, viene recuperato il conto C/G. Il conto recuperato viene selezionato in base all'impostazione del numero di addebito dell'articolo e alle informazioni sul documento.

Sia per i documenti di vendita che di acquisto, è possibile assegnare un addebito articolo in due modi:

* Nel documento in cui sono elencati gli articoli ai quali l'addebito si riferisce. In genere questo metodo si utilizza per i documenti che non sono stati ancora completamente registrati.
* In una fattura separata collegando l'addebito articolo a un carico o una spedizione registrata dove vengono elencati gli articoli a cui l'addebito si riferisce.

> [!NOTE]  
> È possibile assegnare addebiti articoli a ordini, fatture e note di credito, per i documenti di vendita e per quelli di acquisto. Di seguito viene descritto come utilizzare gli addebiti articolo per una fattura di acquisto. I passaggi sono simili per tutti gli altri documenti di acquisto o vendita.

## Esempio

Questo video mostra come gestire un costo di spedizione aggiuntivo come parte del costing di magazzino.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## Per impostare i numeri di addebito articolo

I numeri di addebito articolo vengono utilizzati per distinguere fra i vari tipi di addebito.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Addebiti articoli**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo** nella pagina **Addebiti articoli** per creare una nuova riga.
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Per assegnare un addebito articolo direttamente alla fattura di acquisto per l'articolo

Se si conosce l'addebito articolo quando si registra una fattura di acquisto per l'articolo, attenersi alla procedura seguente.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.
2. Creare una nuova fattura di acquisto. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).
3. Assicurarsi che la fattura di acquisto abbia una o più righe di tipo Articolo.
4. In una nuova riga selezionare **Addebito (Articolo)** nel campo **Tipo**.
5. Nel campo **Quantità** immetti il numero di unità dell'addebito articolo che sono state fatturate.
6. Nel campo **Costo Diretto Unitario** immettere l'importo dell'addebito articolo.
7. Compilare i rimanenti campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Nei seguenti passaggi, esegui l'assegnazione effettiva. Finché l'addebito articolo non è assegnato completamente, il valore nel campo **Qtà da assegnare** verrà visualizzato con carattere rosso.
8. Nella Scheda dettaglio **Righe** fare clic sull'azione **Assegnazione addebito articolo**.

    Verrà visualizzata la pagina **Assegnazione addebito articolo** che mostra una riga per ogni riga di tipo Articolo nella fattura di acquisto. Per assegnare l'addebito articolo a una o più righe della fattura, è possibile utilizzare una funzione che assegna e distribuisce l'addebito automaticamente oppure è possibile compilare manualmente il campo **Qtà da assegnare**. Nei seguenti passaggi viene descritto come utilizzare la funzione Suggerisci assegnazione addebiti articoli.

9. Nella pagina **Assegnazione addebito articolo**, selezionare l'azione **Suggerisci assegnazione addebiti articoli**.
10. Se vi sono più di una riga fattura di tipo Articolo, selezionare una delle quattro opzioni di distribuzione.  

Finché l'addebito articolo è assegnato completamente, il valore nel campo **Qtà da assegnare** nella fattura di acquisto verrà visualizzato come zero.

L'addebito è ora assegnato alla fattura di acquisto. Quando si registra il carico della fattura di acquisto, i valori di magazzino degli articoli vengono aggiornati con il costo dell'addebito articolo.  

## Per assegnare un addebito articolo da una fattura distinta alla fattura di acquisto per l'articolo

Se si riceve una fattura per l'addebito articolo dopo aver effettuato la registrazione del carico dell'acquisto originale, attenersi alla procedura seguente.

1. Ripetere i passaggi da 1 a 8 della sezione [Per assegnare un addebito articolo direttamente alla fattura di acquisto per l'articolo](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Nella pagina **Assegnaz. addebito art.** scegliere l'azione **Prendi righe di carico**.
3. Nella pagina **Righe carico acq.** selezionare il carico di acquisto registrato per l'articolo a cui si desidera assegnare l'addebito quindi scegliere **OK**.
4. Scegliere l'azione **Suggerisci ass. addebiti art.**.

Gli addebiti articoli nella fattura di acquisto distinta vengono ora assegnati all'articolo nel carico di acquisto registrato, viene quindi aggiornato il valore di magazzino dell'articolo con il costo dell'addebito articolo.

## Gestire gli addebiti articolo per le ricevute parziali

Analizziamo un esempio di come gestire gli addebiti articolo per una ricevuta parziale.

Hai un ordine di acquisto con tre righe:

* Due righe sono per gli articoli.
* Una riga acquisisce gli addebiti articolo allocati per gli articoli in base all'importo.

Quando gli articoli vengono consegnati, scopri che manca uno degli articoli, quindi non puoi contrassegnare quella riga come ricevuta. È possibile ricevere e registrare la fattura di acquisto solo per il secondo articolo e occuparsi successivamente dell'articolo mancante.

Per gestire il costo dell'articolo per la ricevuta parziale, sulla pagina **Assegnazione addebito articolo** immetti **0** nel campo **Quantità da gestire** sulla riga per l'articolo mancante. Quindi, copia il valore dal campo **Qtà addebito articolo da gestire** al campo **Quantità da fatturare** nelle righe dell'ordine di acquisto.

Quando sei pronto per gestire l'articolo mancante, aggiorna il campo **Quantità da gestire** e invia l'ordine.

## Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
