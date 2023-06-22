---
title: Annullare una registrazione con un movimento di storno
description: 'Se rilevi un errore in un giornale di registrazione generale registrato, puoi utilizzare l''azione Storno transazione per annullare la registrazione con un audit trail corretto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments" />Stornare le registrazioni e annullare carichi/spedizioni errati

Le registrazioni contabili di storno sono utili, ad esempio, per correggere gli errori e per cancellare un vecchio movimento di ratei prima di inserirne uno nuovo. Un movimento di storno è uguale all'originale ma ha segno opposto nel campo **Importo**. Il movimento di storno deve avere lo stesso numero di documento e la stessa data di registrazione del movimento originale. Dopo lo storno di un movimento, è necessario creare il movimento corretto.

È possibile stornare solo movimenti immessi da una riga di registrazioni generali. Un movimento può essere stornato una volta.

Per annullare la registrazione di un carico o di una spedizione, prima che vengano registrati come fatturati, è possibile utilizzare la funzione **Annulla** nel documento registrato. È possibile annullare le quantità di tipo **Articolo** e **Risorsa**.

Se è stata eseguita una registrazione di quantità negativa non corretta, ad esempio se è stato creato un ordine di acquisto con un numero errato di articoli e lo si è registrato come ricevuto (ma non fatturato), è possibile annullare la registrazione.

Se è stata eseguita una registrazione di quantità positiva, ad esempio se è stata creata una spedizione vendita o una spedizione di reso acquisto con un numero errato di articoli e lo si è registrato come spedito ma non fatturato, è possibile annullare la registrazione.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry" />Per stornare la registrazione di un movimento di contabilità generale

È possibile stornare i movimenti da tutte le pagine **Movimenti contabili**. La seguente procedura è basata sulla pagina **Movimenti C/G**.

> [!NOTE]
> Il movimento deve derivare da una registrazione.
>
> Inoltre, non è possibile annullare i movimenti registrati con le informazioni di un processo o che hanno realizzato utili e perdite all'interno della stessa transazione.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimenti C/G**, quindi scegli il collegamento correlato.
2. Selezionare il movimento che si desidera stornare quindi scegliere l'azione **Storno**.
3. Nella pagina **Storna movimenti transazioni**, scegliere l'azione **Storna**.
4. Seleziona **Sì** per confermare lo storno.

## <a name="to-post-a-negative-entry" />Per registrare un movimento negativo

Utilizza il campo **Correzione** per registrare un addebito negativo anziché un credito oppure un accredito negativo anziché un addebito su un conto. Per impostazione predefinita, il campo è disponibile in tutti i giornali. I campi **Dare** e **Avere** includono il movimento originale e il movimento corretto. Questi campi non influiscono sul saldo del conto.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato  
2. Nel campo **Nome batch** selezionare il nome di batch necessario.  
3. Immettere informazioni nei campi rilevanti.  
4. Nella riga di registrazione che si desidera attivare per i movimenti negativi, selezionare la casella di controllo **Correzione**.  
5. Per contabilizzare la registrazione, scegliere l'azione **Registra**, quindi scegliere il pulsante **Sì**.

## <a name="to-undo-a-quantity-on-a-posted-purchase-receipt" />Per annullare una quantità in una ricezione acquisti registrata

Di seguito viene descritto come annullare un carico registrato di articoli o risorse. I passaggi sono simili a quelli per le spedizioni registrate.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Carichi acquisti registrati**, quindi scegli il collegamento correlato.  
2. Aprire il carico registrato che si desidera annullare.  
3. Selezionare la riga o le righe che si desidera annullare.  
4. Scegliere l'azione **Annulla carico**.

Una riga di rettifica viene aggiunta sotto la riga di carico selezionata. Se la quantità è stata ricevuta in un carico warehouse, una riga di rettifica viene aggiunta nel carico warehouse registrato.  

I campi **Quantità ricevuta** e **Qtà carichi non fatt.** nell'ordine di acquisto collegato verranno impostati su un valore pari a zero.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment" />Per annullare e successivamente ripetere la registrazione di una quantità in una spedizione di reso registrata

Nei passaggi successivi viene descritto come effettuare le seguenti operazioni:

* Annulla una spedizione di reso registrata di articoli o risorse.
* Pubblica nuovamente il reso dell'acquisto con una nuova quantità.

I passaggi sono simili a quelli per i carichi da reso registrati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni reso registrate**, quindi scegli il collegamento correlato.  
2. Apri la spedizione reso registrata per annullare.
3. Seleziona la riga o le righe da annullare.  

4. Scegliere l'azione **Eliminare spedizione reso**.  

    Nel documento registrato viene inserita una riga correttiva e i campi **Qtà reso spedita** e **Reso spedito non fatt.** nell'ordine di reso vengono impostati su un valore pari a zero.  

    Ora tornare all'ordine di reso di acquisto per ripetere la registrazione.  

5. Nella pagina **Spedizione reso registrata** prendere nota del numero nel campo **Nr. ordine di reso**. .  
6. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di reso acquisto**, quindi seleziona il collegamento correlato.  
7. Aprire l'ordine di reso in questione quindi scegliere l'azione **Riapri**.  
8. Correggere la voce nel campo **Quantità** e registrare nuovamente l'ordine di reso acquisto.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## <a name="see-also" />Vedere anche

[Annullare la registrazione di assemblaggi](assembly-how-to-undo-assembly-posting.md)  
[Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
