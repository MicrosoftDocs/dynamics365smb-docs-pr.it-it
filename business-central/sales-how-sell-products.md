---
title: Creare un ordine di vendita cliente e vendere i prodotti
description: Descrive come creare un ordine di vendita per registrare l'accordo con un cliente per vendere o commercializzare prodotti secondo termini specifici.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: soalex
ms.topic: conceptual
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 02/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="sell-products-with-a-customer-sales-order"></a>Vendere prodotti con un ordine di vendita cliente

Questo articolo fornisce istruzioni su quando utilizzare un ordine di vendita cliente oltre a una fattura. Se il processo di vendita richiede di spedire solo parte di un ordine, forse perché la quantità completa non è disponibile, è necessario elaborare la vendita effettuando un ordine di vendita.

Devi anche utilizzare gli ordini di vendita se vendi articoli con consegna diretta dal fornitore al cliente, detto anche spedizione diretta. Ulteriori informazioni su [Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di vendita funzionano come le fatture di vendita. Ulteriori informazioni in [Fatturare le vendite](sales-how-invoice-sales.md).

Quando si consegnano i prodotti, nella quantità totale o parziale, si registra l'ordine di vendita come spedito o come spedito e fatturato per creare i relativi movimenti contabili articolo e cliente nel sistema. Quando si registra l'ordine di vendita, è possibile inviarla via email come allegato PDF. Puoi precompilare il corpo dell'e-mail con un riepilogo delle informazioni dell'ordine e per il pagamento, ad esempio con un collegamento a PayPal. Ulteriori informazioni in [Spedire articoli](warehouse-how-ship-items.md) e [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Negli ambienti aziendali in cui il cliente paga immediatamente, ad esempio tramite PayPal o contanti, il pagamento viene registrato immediatamente quando si registra la fattura di vendita, vale a dire la fattura di vendita pubblicata viene chiusa come interamente applicata. Selezionare il metodo rilevante nel campo **Codice metodo di pagamento** nell'ordine cliente. Vedere il passaggio 5 di seguito. Per i pagamenti elettronici, come PayPal, compilare anche il campo **Servizio di pagamento**. Ulteriori informazioni in [Abilitare i pagamenti clienti tramite i servizi di pagamento](sales-how-enable-payment-service-extensions.md).

È persino possibile creare ordini pagati direttamente per clienti non registrati impostando dapprima una scheda "cliente per vendite in contanti", selezionabile nell'ordine di vendita. Ulteriori informazioni in [Impostare i clienti per vendite in contanti](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order"></a>Creare un ordine di vendita

> [!NOTE]  
> La seguente procedura presuppone che il cliente sia già impostato. Per istruzioni su come eseguire questa operazione, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare **Nuovo** per creare una nuova voce.
3. Nel campo **Cliente** immettere il nome di un cliente esistente.

    Altri campi nella pagina **Ordine di vendita** vengono compilati con le informazioni standard del cliente selezionato.  

4. Compilare i restanti campi della pagina **Ordine di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Se si consente al cliente di pagare immediatamente, ad esempio, tramite carta di credito o PayPal, compilare il campo **Codice metodo di pagamento**. Il pagamento viene quindi registrato non appena si registra l'ordine di vendita come fatturato. Se si seleziona *Cassa*, il pagamento viene registrato in un conto di contropartita specificato.

    A questo punto compilare le righe dell'ordine di vendita con gli articoli di magazzino o i servizi che si desidera vendere al cliente.

    Se imposti le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, puoi inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.
5. Nella Scheda dettaglio **Righe**, nel campo **Tipo**, seleziona il tipo di prodotto, addebito o transazione che vuoi registrare per il cliente con la linea di vendita.

6. Nel campo **Nr.** immettere il numero di un'assistenza o di un articolo di magazzino.

    Lasciare il campo **Nr.** vuoto se la riga è per:

    * Commento. Compilare il commento nel campo **Descrizione**.
    * Articolo di catalogo. Scegliere l'azione **Seleziona articoli di catalogo**. Ulteriori informazioni su [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).
7. Nel campo **Quantità** immettere il numero di articoli da vendere.

    > [!NOTE]  
    > Per gli articoli di tipo *Risorsa* o *Assistenza*, la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga. Ulteriori informazioni in [Impostare unità di misura articolo](inventory-how-setup-units-of-measure.md).

    Il campo **Importo riga** viene aggiornato al valore del campo **Prezzo unitario** moltiplicato per il numero del campo **Quantità**.

    Il prezzo e gli importi riga vengono visualizzati con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.
8. Nel campo **% sconto riga** immettere una percentuale se si intende concedere al cliente uno sconto sul prodotto. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** nella scheda cliente o articolo, e se vengono soddisfatti i criteri di prezzo, il prezzo e l'importo nella riga di vendita vengono automaticamente aggiornati. Ulteriori informazioni in [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md)
9. Per aggiungere un commento sulla riga dell'ordine che il cliente può vedere sull'ordine di vendita stampato, scrivi un commento in una riga vuota nel campo **Descrizione**.  
10. Ripeti i passi da 5 a 9 per ogni articolo che vuoi vendere al cliente.

    I campi dei totali sotto le righe vengono automaticamente aggiornati quando si creano o si modificano le righe per visualizzare gli importi che verranno registrati nei libri contabili.

    > [!NOTE]
    > In casi molto rari, gli importi registrati possono discostarsi da ciò che viene visualizzato nei campi dei totali. Ciò è in genere dovuto ai calcoli di arrotondamento in relazione all'IVA o all'imposta sulle vendite.
    >
    > Per verificare gli importi che verranno effettivamente registrati, è possibile utilizzare la pagina **Statistiche**, che tiene conto dei calcoli di arrotondamento. Inoltre, se si sceglie l'azione **Rilascia**, i campi dei totali verranno aggiornati per includere i calcoli di arrotondamento.  

11. Facoltativamente, nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati gli sconti fattura per il cliente e se vengono soddisfatti i criteri, la percentuale specificata viene automaticamente inserita nel campo **% sconto fattura**. E il relativo importo viene quindi inserito nel campo **Importo sconto fatt. IVA esclusa**. Ulteriori informazioni in [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md)
12. Per spedire solo una parte della quantità ordinata, immettere la quantità desiderata nel campo **Qtà da spedire**. Il valore viene copiato automaticamente nel campo **Qtà da fatturare**.

    > [!NOTE]
    > Se il campo **Avviso spedizione** è impostato su **Completato** nella Scheda dettaglio **Spedizione e fatturazione**, non puoi registrare spedizioni parziali. Ulteriori informazioni in [Elaborare spedizioni parziali](sales-how-send-partial-shipments.md).
13. Per fatturare solo una parte della quantità spedita, immettere la quantità desiderata nel campo **Qtà da fatturare**. La quantità deve essere inferiore al valore presente nel campo **Qtà da spedire**.  
14. Una volta completate le righe dell'ordine di vendita, scegliere l'azione **Registra e invia**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Viene visualizzata la finestra dialogo **Registra e invia conferma** con il metodo preferito del cliente per la ricezione dei documenti. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Ulteriori informazioni in [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).

I movimenti contabili cliente e articolo sono ora creati nel sistema e l'ordine di vendita è emesso come documento PDF. Una volta che l'ordine di vendita è completamente registrato, viene rimosso dall'elenco degli ordini di vendita e viene sostituito con nuovi documenti nell'elenco delle fatture di vendita e delle spedizioni di vendita.  

## <a name="external-document-number"></a>Numero di documento esterni

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="working-with-amount-fields"></a>Utilizzo dei campi importo

I valori nei campi che mostrano gli importi possono essere positivi o negativi, a seconda che il valore rappresenti un credito o un debito. Questo video mostra come usare i campi che mostrano gli importi.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1h96P]

## <a name="see-also"></a>Vedere anche

[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Registrazione di vendite](ui-post-sales.md)  
[Spedire articoli](warehouse-how-ship-items.md)  
[Effettuare spedizioni dirette](sales-how-drop-shipment.md)  
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Stampare la lista prelievo](sales-how-print-picking-list.md)  
[Elaborare spedizioni parziali](sales-how-send-partial-shipments.md)  
[Magazzino](inventory-manage-inventory.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
