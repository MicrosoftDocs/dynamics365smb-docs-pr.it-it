---
title: Creare un ordine di vendita e vendere i prodotti | Documenti Microsoft
description: Descrive come creare un ordine di vendita per registrare l'accordo con un cliente per vendere o commercializzare prodotti secondo termini specifici.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 19b32e8faa6b9e56505379d1f06fd5ad79466614
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115517"
---
# <a name="sell-products"></a>Vendere prodotti

Si crea una fattura di vendita o un ordine di vendita per registrare il contratto con un cliente per vendere alcuni prodotti con determinate condizioni di consegna e pagamento.

> [!NOTE]  
> Utilizzare gli ordini di vendita se il processo di vendita richiede che si possano spedire parti di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile in una sola volta. Se si utilizzano fatture di vendita, [!INCLUDE [prod_short](includes/prod_short.md)] presuppone che si spedisca l'intero quantitativo quando si registra la fattura. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di vendita. Per ulteriori informazioni, vedere [Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di vendita funzionano come le fatture di vendita. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).

È possibile negoziare con il cliente prima di tutto creando un'offerta di vendita, che è possibile convertire in un ordine di vendita quando ci si accorda sulla vendita. Per ulteriori informazioni, vedere [Creare offerte di vendita](sales-how-make-offers.md).

Dopo che il cliente ha confermato il contratto, ad esempio dopo un processo di offerta, è possibile inviare una conferma dell'ordine per registrare l'obbligo di consegnare i prodotti come concordato.

Quando si consegnano i prodotti, nella quantità totale o parziale, si registra l'ordine di vendita come spedito o come spedito e fatturato per creare i relativi movimenti contabili articolo e cliente nel sistema. Quando si registra l'ordine di vendita, è possibile inviare via email il documento come allegato PDF. È possibile impostare il messaggio con un testo precompilato che riepiloga le informazioni dell'ordine e per il pagamento, ad esempio con un collegamento a PayPal. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Negli ambienti aziendali in cui il cliente paga qualche tempo dopo la consegna, in base al termine di pagamento, una fattura di vendita registrata rimane aperta (non pagata) fino a quando il reparto Contabilità clienti verifica che il pagamento sia stato ricevuto e applica il pagamento alla fattura di vendita pubblicata. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

Negli ambienti aziendali in cui il cliente paga immediatamente, ad esempio tramite PayPal o contanti, il pagamento viene registrato immediatamente quando si registra l'ordine di vendita come fatturato, vale a dire la fattura di vendita pubblicata viene chiusa come interamente applicata. Selezionare il metodo rilevante nel campo **Codice metodo di pagamento** nell'ordine cliente. Vedere il passaggio 8. Per i pagamenti elettronici, come PayPal, compilare anche il campo **Servizio di pagamento**. Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti tramite i servizi di pagamento](sales-how-enable-payment-service-extensions.md).

È persino possibile creare ordini pagati direttamente per clienti non registrati impostando dapprima una scheda "cliente per vendite in contanti", selezionabile nell'ordine di vendita. Per ulteriori informazioni, vedere [Impostare i clienti per vendite in contanti](finance-how-to-set-up-cash-customers.md).

È possibile rettificare o annullare facilmente una fattura di vendita registrata, risultante da un ordine di vendita, prima di pagarla. Ciò risulta utile se si desidera correggere un errore di digitazione o se il cliente richiede una modifica in anticipo nell'elaborazione dell'ordine. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md). Se la fattura di vendita registrata è stata pagata, allora sarà necessario creare una nota di credito di vendita per stornare la vendita. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).

a scheda articolo può essere di tipo **Inventario**, **Assistenza** e **Non in inventario** per specificare se la scheda articolo rappresenta un'unità fisica di inventario, un'unità di misura del tempo della manodopera o un'unità fisica non gestita in magazzino Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md). Il processo dell'ordine di vendita è lo stesso per tutti e tre i tipi di articoli.

È possibile compilare i campi cliente nell'ordine di vendita in due modi a seconda che il cliente sia già registrato o meno. Vedere il passaggio 2 della procedura riportata di seguito.

## <a name="to-create-a-sales-order"></a>Per creare un ordine di vendita

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.
2. Nel campo **Cliente** immettere il nome di un cliente esistente.

    Altri campi nella pagina **Ordine di vendita** vengono compilati con le informazioni standard del cliente selezionato.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]  

    Diversi campi nell'ordine di vendita sono ora compilati con le informazioni specificate nella nuova scheda cliente.
3. Compilare i restanti campi della pagina **Ordine di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Se si consente al cliente di pagare immediatamente, ad esempio, tramite carta di credito o PayPal, compilare il campo **Codice metodo di pagamento**. Il pagamento viene quindi registrato non appena si registra l'ordine di vendita come fatturato. Se si seleziona CASSA, il pagamento viene registrato in un conto di contropartita specificato.

    A questo punto compilare le righe dell'ordine di vendita con gli articoli di magazzino o i servizi che si desidera vendere al cliente.

    Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.
4. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.

5. Nel campo **Nr.** immettere il numero di un'assistenza o di un articolo di magazzino.

    Lasciare il campo **Nr.** vuoto nei seguenti casi:

    * Se la riga è destinata a un commento. Compilare il commento nel campo **Descrizione**.
    * Se la riga è destinata a un articolo di catalogo. Scegliere l'azione **Seleziona articoli di catalogo**. Per ulteriori informazioni, vedere [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).
6. Nel campo **Quantità** immettere il numero di articoli da vendere.

    > [!NOTE]  
    > Per gli articoli di tipo *Risorsa* o *Assistenza*, la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga. Per ulteriori informazioni, vedere [Impostare unità di misura articolo](inventory-how-setup-units-of-measure.md).

    Il campo **Importo riga** viene aggiornato al valore del campo **Prezzo unitario** moltiplicato per il valore del campo **Quantità**.

    Il prezzo e gli importi riga vengono visualizzati con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.
7. Nel campo **% sconto riga** immettere una percentuale se si intende concedere al cliente uno sconto sul prodotto. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dell'offerta vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).
8. Per aggiungere un commento sulla riga dell'offerta che il cliente può vedere sull'offerta di vendita stampata, scrivere un testo nel campo **Descrizione** nella riga vuota.  
9. Ripetere i passaggi da 4 a 8 per ogni articolo che si desidera vendere al cliente.

    I campi dei totali sotto le righe vengono automaticamente aggiornati quando si creano o si modificano le righe per visualizzare gli importi che verranno registrati nei libri contabili.

    > [!NOTE]
    > In casi molto rari, gli importi registrati possono discostarsi da ciò che viene visualizzato nei campi dei totali. Ciò è in genere dovuto ai calcoli di arrotondamento in relazione all'IVA o all'imposta sulle vendite.
    >
    > Per verificare gli importi che verranno effettivamente registrati, è possibile utilizzare la pagina **Statistiche**, che tiene conto dei calcoli di arrotondamento. Inoltre, se si sceglie l'azione **Rilascia**, i campi dei totali verranno aggiornati per includere i calcoli di arrotondamento.  

10. Facoltativamente, nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati degli sconti su fattura per il cliente, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fatt. IVA esclusa**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).
11. Per spedire solo una parte della quantità ordinata, immettere la quantità desiderata nel campo **Qtà da spedire**. Il valore viene copiato nel campo **Qtà da fatturare**.
12. Per fatturare solo una parte della quantità spedita, immettere la quantità desiderata nel campo **Qtà da fatturare**. La quantità deve essere inferiore al valore presente nel campo **Qtà da spedire**.  
13. Una volta completate le righe dell'ordine di vendita, scegliere l'azione **Registra e invia**.

Viene visualizzata la finestra dialogo **Registra e invia conferma** con il metodo preferito del cliente per la ricezione dei documenti. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).

I movimenti contabili cliente e articolo sono ora creati nel sistema e l'ordine di vendita è emesso come documento PDF. Una volta che l'ordine di vendita è completamente registrato, viene rimosso dalla lista degli ordini di vendita e viene sostituito con nuovi documenti nella lista delle fatture di vendita registrate e nella lista delle spedizioni vendite registrate.  

## <a name="external-document-number"></a>Numero di documento esterni

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Stampare la lista prelievo](sales-how-print-picking-list.md)  
[Magazzino](inventory-manage-inventory.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]