---
title: Creare una fattura di vendita o un ordine di vendita | Documenti Microsoft
description: Descrive come creare un fattura di vendita o un ordine di vendita per registrare l'accordo con un cliente per vendere prodotti secondo termini specifici.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fb4b1ad14dfedaeca38293e0e0b4496300090c17
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-invoice-sales"></a>Procedura: Fatturare le vendite
Si crea una fattura di vendita o un ordine di vendita per registrare il contratto con un cliente per vendere alcuni prodotti con determinate condizioni di consegna e pagamento.  

> [!NOTE]  
>   In un paio di scenari è necessario utilizzare un ordine di vendita invece di una fattura di vendita:  

* Se è necessario spedire solo una parte della quantità degli ordini, ad esempio, perché la quantità completa non è disponibile.  
* Se si vendono articoli che il fornitore consegna direttamente al cliente. Questa operazione viene denominata spedizione diretta. Per ulteriori informazioni, vedere [Procedura: Effettuare spedizioni dirette](sales-how-drop-shipment.md).  

In tutti gli altri scenari, gli ordini di vendita e le fatture di vendita funzionano nello stesso modo. Per ulteriori informazioni, vedere [Procedura: Vendere prodotti](sales-how-sell-products.md).

È possibile negoziare con il cliente prima di tutto creando un'offerta di vendita, che è possibile convertire in una fattura di vendita quando ci si accorda sulla vendita. Per ulteriori informazioni, vedere [Procedura: Fare offerte](sales-how-make-offers.md).

Se il cliente decide di acquistare, registrare la fattura di vendita per creare i relativi movimenti di quantità e valore. Quando si registra la fattura di vendita, è possibile inviare via email il documento come allegato PDF. È possibile impostare il messaggio con un testo precompilato che riepiloga le informazioni della fattura e per il pagamento, ad esempio con un collegamento a PayPal. Per ulteriori informazioni, vedere [Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md).

Negli ambienti aziendali in cui il cliente deve pagare prima che vengano consegnati i prodotti, ad esempio nelle vendita al dettaglio, è necessario attendere la ricezione del pagamento prima di consegnare i prodotti. Nella maggior parte dei casi, i pagamenti in entrata vengono elaborati alcune settimane dopo la consegna collegando i pagamenti alle relative fatture di vendita non pagate registrate. Per ulteriori informazioni, vedere [Procedura: Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

È possibile correggere o annullare in modo semplice una fattura di vendita registrata prima che venga pagata. Ad esempio, ciò risulta utile se si desidera correggere un errore di digitazione o se il cliente richiede una modifica in anticipo nell'elaborazione dell'ordine. Per ulteriori informazioni, vedere [Procedura: Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md). Se la fattura di vendita registrata è stata pagata, allora sarà necessario creare una nota di credito di vendita per stornare la vendita. Per ulteriori informazioni vedere [Procedura: Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).

Gli articoli possono essere sia articoli di magazzino che servizi di assistenza, in base ai tipi **Articolo - Magazzino** e **Articolo - Assistenza** nelle righe di vendita. Il processo della fattura di vendita è lo stesso per entrambi i tipi di articoli. Per ulteriori informazioni, vedere [Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md).

È possibile compilare i campi cliente nella fattura di vendita in due modi a seconda che il cliente sia già registrato o meno. Vedere i passaggi 2 e 3 della procedura riportata di seguito.

## <a name="to-create-a-sales-invoice"></a>Per creare una fattura di vendita
1. Nella home page scegliere l'azione **Fattura vendita**.  
2. Nel campo **Cliente** immettere il nome di un cliente esistente.

   Altri campi nella finestra **Fattura di vendita** contengono informazioni standard sul cliente selezionato. Se il cliente non è registrato, è necessario attenersi alla seguente procedura:
3. Nel campo **Cliente** immettere il nome del nuovo cliente.
4. Nella finestra di dialogo relativa alla registrazione del nuovo cliente fare clic su **Sì**.
5. Nella finestra **Selezionare un modello per un nuovo cliente** scegliere un modello su cui basare la scheda del nuovo cliente, quindi scegliere **OK**.
6. Una nuova scheda cliente verrà visualizzata con le informazioni sul modello cliente selezionato. Compilare i campi rimanenti. Per ulteriori informazioni, vedere [Procedura: Registrare nuovi clienti](sales-how-register-new-customers.md).  
7. Una volta completata la scheda cliente, scegliere **OK** per tornare alla finestra **Fattura vendita**.

   Diversi campi nella fattura di vendita sono ora compilati con le informazioni specificate nella nuova scheda cliente.  
8. Compilare i restanti campi della finestra **Fattura di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

È ora possibile compilare le righe della fattura di vendita per i prodotti che si sta vendendo al cliente o per ogni transazione con il cliente per il quale si desidera effettuare la registrazione in un conto C/G.   

Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.  
9. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.
10. Nel campo **Nr.** selezionare un record per effettuare la registrazione in base al valore nel campo **Tipo**.

 Lasciare il campo **Nr.** vuoto nei seguenti casi: - se la riga è destinata a un commento. Compilare il commento nel campo **Descrizione**.
 - Se la riga è destinata a un articolo non in stock. Scegliere l'aziona **Seleziona articoli non in stock**. Per ulteriori informazioni, vedere [Procedura: Utilizzare gli articoli non in stock](inventory-how-work-nonstock-items.md).

11. Nel campo **Quantità** immettere qui il numero di unità di articoli, addebiti o transazioni che la riga registrerà per il cliente.  

    > [!NOTE]  
>   Per gli articoli di tipo **Magazzino - Assistenza** o **Risorsa** la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga.  

    Il valore nel campo **Importo riga** viene calcolato come segue *Prezzo unitario* x *Quantità*.  

    Il prezzo e gli importi riga sono con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.  
12. Se si desidera assegnare uno sconto, immettere una percentuale nel campo **% sconto riga**. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.  

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dei vendita vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Ripetere i passaggi da 9 a 12 per ogni prodotto o addebito che si desidera vendere al cliente.  

    I totali sotto le righe vengono automaticamente calcolati quando si creano o si modificano le righe.  
14. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati degli sconti su fattura per il cliente, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fatt. IVA esclusa**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Una volta completate le righe della fattura di vendita, scegliere l'azione **Registra e invia**.  

Viene visualizzata la finestra dialogo **Registra e invia conferma** con il metodo preferito del cliente per la ricezione dei documenti. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Per ulteriori informazioni, vedere [Procedura: Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).

I movimenti articolo e di contabilità cliente sono ora creati nel sistema e la fattura di vendita è emessa come documento PDF. La fattura di vendita viene rimossa dall'elenco delle fatture di vendita e sostituita con un nuovo documento nell'elenco delle fatture di vendita registrate.

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Eseguire la fatturazione in blocco da Microsoft Bookings in Dynamics 365 for Financials](finance-bookings.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

