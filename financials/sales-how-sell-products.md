---
title: Creare un ordine di vendita e vendere i prodotti | Documenti Microsoft
description: Descrive come creare un ordine di vendita per registrare l'accordo con un cliente per vendere o commercializzare prodotti secondo termini specifici.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 01/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b396908f9c63b63eb8eb0a3e9fd84d20cd1c6c32
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="sell-products"></a>Vendere prodotti
Si crea una fattura di vendita o un ordine di vendita per registrare il contratto con un cliente per vendere alcuni prodotti con determinate condizioni di consegna e pagamento.

> [!NOTE]  
>   È necessario utilizzare gli ordini di vendita se il processo di vendita richiede che si possano spedire parti di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile in una sola volta. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di vendita. Per ulteriori informazioni, vedere [Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di vendita funzionano come le fatture di vendita. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).

È possibile negoziare con il cliente prima di tutto creando un'offerta di vendita, che è possibile convertire in un ordine di vendita quando ci si accorda sulla vendita. Per ulteriori informazioni, vedere  [Fare offerte](sales-how-make-offers.md).

Dopo che il cliente ha confermato il contratto, ad esempio dopo un processo di offerta, è possibile inviare una conferma dell'ordine per registrare l'obbligo di consegnare i prodotti come concordato.

Quando si consegnano i prodotti, nella quantità totale o parziale, si registra l'ordine di vendita come spedito o come spedito e fatturato per creare i relativi movimenti contabili articolo e cliente nel sistema. Quando si registra l'ordine di vendita, è possibile inviare via email il documento come allegato PDF. È possibile impostare il messaggio con un testo precompilato che riepiloga le informazioni dell'ordine e per il pagamento, ad esempio con un collegamento a PayPal. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Negli ambienti aziendali in cui il cliente deve pagare prima che vengano consegnati i prodotti, ad esempio nelle vendita al dettaglio, è necessario attendere la ricezione del pagamento prima di consegnare i prodotti. Nella maggior parte dei casi, i pagamenti in entrata vengono elaborati alcune settimane dopo la consegna collegando i pagamenti alle relative fatture di vendita non pagate registrate. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

È possibile rettificare o annullare facilmente una fattura di vendita registrata, risultante da un ordine di vendita, prima di pagarla. Ciò risulta utile se si desidera correggere un errore di digitazione o se il cliente richiede una modifica in anticipo nell'elaborazione dell'ordine. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md). Se la fattura di vendita registrata è stata pagata, allora sarà necessario creare una nota di credito di vendita per stornare la vendita. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).

Gli articoli possono essere sia articoli di magazzino che servizi di assistenza, in base ai tipi **Articolo - Magazzino** e **Articolo - Assistenza** nelle righe di vendita. Il processo dell'ordine di vendita è lo stesso per entrambi i tipi di articoli. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

È possibile compilare i campi cliente nell'ordine di vendita in due modi a seconda che il cliente sia già registrato o meno. Vedere i passaggi 2 e 3 della procedura riportata di seguito.

## <a name="to-create-a-sales-order"></a>Per creare un ordine di vendita
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di vendita**, quindi scegliere il collegamento correlato. 
2. Nel campo **Cliente** immettere il nome di un cliente esistente.

    Altri campi nella finestra **Ordine di vendita** vengono compilati con le informazioni standard del cliente selezionato. Se il cliente non è registrato, è necessario attenersi alla seguente procedura:
3. Nel campo **Cliente** immettere il nome del nuovo cliente.
4. Nella finestra di dialogo relativa alla registrazione del nuovo cliente fare clic su **Sì**.
5. Nella finestra **Selezionare un modello per un nuovo cliente** scegliere un modello su cui basare la scheda del nuovo cliente, quindi scegliere **OK**.

    Una nuova scheda cliente verrà visualizzata, precompilata con le informazioni sul modello cliente selezionato. Il campo **Nome** viene precompilato con il nome del nuovo cliente immesso nell'ordine di vendita.
6. Procedere compilando i restanti campi della scheda cliente. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).  
7. Una volta completata la scheda cliente, scegliere **OK** per tornare alla finestra **Ordine di vendita**.

    Diversi campi nell'ordine di vendita sono ora compilati con le informazioni specificate nella nuova scheda cliente.
8. Compilare i restanti campi della finestra **Ordine di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    A questo punto compilare le righe dell'ordine di vendita con gli articoli di magazzino o i servizi che si desidera vendere al cliente.

    Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.
9. Nella Scheda dettaglio **Righe** del campo **Articolo** immettere il numero di un articolo di magazzino o di un servizio.  
10. Nel campo **Quantità** immettere il numero di articoli da vendere.

    > [!NOTE]  
>   Per gli articoli di tipo Assistenza, la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga.

    Il campo **Importo riga** viene aggiornato al valore del campo **Prezzo unitario** moltiplicato per il valore del campo **Quantità**.

    Il prezzo e gli importi riga vengono visualizzati con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.
11. Nel campo **% sconto riga** immettere una percentuale se si intende concedere al cliente uno sconto sul prodotto. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dell'offerta vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).
12. Per aggiungere un commento sulla riga dell'offerta che il cliente può vedere sull'offerta di vendita stampata, scrivere un testo nel campo **Descrizione** nella riga vuota.  
13. Ripetere i passaggi da 9 a 12 per ogni articolo che si desidera offrire al cliente.

    I totali sotto le righe vengono automaticamente calcolati quando si creano o si modificano le righe.
14. Una nuova scheda cliente verrà visualizzata con le informazioni sul modello cliente selezionato. Compilare i campi rimanenti. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).  
15. Una volta completata la scheda cliente, scegliere **OK** per tornare alla finestra **Ordine di vendita**.

   Diversi campi nell'ordine di vendita sono ora compilati con le informazioni specificate nella nuova scheda cliente.  
16. Compilare i restanti campi della finestra **Ordine di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   È ora possibile compilare le righe dell'ordine di vendita per i prodotti che si vendono al cliente o per ogni transazione con il cliente per il quale si desidera effettuare la registrazione in un conto C/G.   

   Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.  
17. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.
18. Nel campo **Nr.** selezionare un record per effettuare la registrazione in base al valore nel campo **Tipo**.

    Lasciare il campo **Nr.** vuoto nei seguenti casi: - se la riga è destinata a un commento. Compilare il commento nel campo **Descrizione**.
    - Se la riga è destinata a un articolo non in stock. Scegliere l'aziona **Seleziona articoli non in stock**. Per ulteriori informazioni, vedere [Utilizzare gli articoli non in stock](inventory-how-work-nonstock-items.md).

19. Nel campo **Quantità** immettere qui il numero di unità di articoli, addebiti o transazioni che la riga registrerà per il cliente.  

    > [!NOTE]  
>   Per gli articoli di tipo **Magazzino - Assistenza** o **Risorsa** la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga. Per ulteriori informazioni, vedere [Impostare unità di misura articolo](inventory-how-setup-units-of-measure.md).

    Il valore nel campo **Importo riga** viene calcolato come segue *Prezzo unitario* x *Quantità*.  

    Il prezzo e gli importi riga sono con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.  
20. Se si desidera assegnare uno sconto, immettere una percentuale nel campo **% sconto riga**. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.  

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dei vendita vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Ripetere i passaggi da 9 a 12 per ogni prodotto o addebito che si desidera vendere al cliente.  

    I totali sotto le righe vengono automaticamente calcolati quando si creano o si modificano le righe.  
22. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati degli sconti su fattura per il cliente, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fatt. IVA esclusa**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).
23. Per spedire solo una parte della quantità ordinata, immettere la quantità desiderata nel campo **Qtà da spedire**. Il valore viene copiato nel campo **Qtà da fatturare**.
24. Per fatturare solo una parte della quantità spedita, immettere la quantità desiderata nel campo **Qtà da fatturare**. La quantità deve essere inferiore al valore presente nel campo **Qtà da spedire**.   
25. Una volta completate le righe dell'ordine di vendita, scegliere l'azione **Registra e invia**.

Viene visualizzata la finestra dialogo **Registra e invia conferma** con il metodo preferito del cliente per la ricezione dei documenti. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).

I movimenti contabili cliente e articolo sono ora creati nel sistema e l'ordine di vendita è emesso come documento PDF. Una volta che l'ordine di vendita è completamente registrato, viene rimosso dalla lista degli ordini di vendita e viene sostituito con nuovi documenti nella lista delle fatture di vendita registrate e nella lista delle spedizioni vendite registrate.

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

