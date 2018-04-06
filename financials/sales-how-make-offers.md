---
title: Creare un'offerta di vendita per un cliente | Documenti Microsoft
description: Descrive come creare un documento di un'offerta di vendita o una richiesta di offerta (RdO) per registrare la propria offerta a un cliente per la vendita di prodotti in base a termini determinati.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 66a78ebc362d0e01c0e6df4bd4a2d74568845159
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="make-offers"></a>Fare offerte
Creare un'offerta di vendita per registrare la propria offerta al cliente per vendere alcuni prodotti a determinate condizioni di consegna e di pagamento. È possibile inviare l'offerta di vendita al cliente per comunicare l'offerta. È possibile inviare il documento via e-mail come allegato PDF. È inoltre possibile fare in modo che il corpo e-mail venga precompilato con un riepilogo dell'offerta. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Quando si negozia con il cliente, è possibile modificare e inviare nuovamente l'offerta di vendita in base alle esigenze. Se il cliente accetta l'offerta, si converte l'offerta di vendita in un ordine o una fattura di vendita in cui viene elaborata la vendita. Per ulteriori informazioni vedere [Fatturare le vendite](sales-how-invoice-sales.md) o [Vendere prodotti](sales-how-sell-products.md).

È possibile compilare i campi cliente nell'offerta di vendita in due modi a seconda che il cliente sia già registrato o meno. Vedere i passaggi 2 e 3 della procedura riportata di seguito.

## <a name="to-create-a-sales-quote"></a>Per creare un'offerta di vendita
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Offerte di vendita**, quindi scegliere il collegamento correlato.
2. Nel campo **Cliente** immettere il nome di un cliente esistente.

   Altri campi nella finestra **Offerte di vendita** contengono informazioni standard del cliente selezionato. Se il cliente non è registrato, è necessario attenersi alla seguente procedura:
3. Nel campo **Cliente** immettere il nome del nuovo cliente.
4. Nella finestra di dialogo relativa alla registrazione del nuovo cliente fare clic su **Sì**.
5. Nella finestra **Selezionare un modello per un nuovo cliente** scegliere un modello su cui basare la scheda del nuovo cliente, quindi scegliere **OK**.
6. Una nuova scheda cliente verrà visualizzata con le informazioni sul modello cliente selezionato. Compilare i campi rimanenti. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).  
7. Una volta completata la scheda cliente, scegliere **OK** per tornare alla finestra **Offerta di vendita**.

   Diversi campi nell'offerta di vendita sono ora compilati con le informazioni specificate nella nuova scheda cliente.  
8. Compilare i restanti campi della finestra **Offerta di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

È ora possibile compilare le righe dell'ordine di vendita per i prodotti che si vendono al cliente o per ogni transazione con il cliente per il quale si desidera effettuare la registrazione in un conto C/G.   

Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.  
9. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.
10. Nel campo **Nr.** selezionare un record per effettuare la registrazione in base al valore nel campo **Tipo**.

 Lasciare il campo **Nr.** vuoto nei seguenti casi: - se la riga è destinata a un commento. Compilare il commento nel campo **Descrizione**.
 - Se la riga è destinata a un articolo non in stock. Scegliere l'aziona **Seleziona articoli non in stock**. Per ulteriori informazioni, vedere [Utilizzare gli articoli non in stock](inventory-how-work-nonstock-items.md).

11. Nel campo **Quantità** immettere qui il numero di unità di articoli, addebiti o transazioni che la riga registrerà per il cliente.

    > [!NOTE]  
>   Per gli articoli di tipo **Magazzino - Assistenza** o **Risorsa** la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga.  

    Il valore nel campo **Importo riga** viene calcolato come segue *Prezzo unitario* x *Quantità*.  

    Il prezzo e gli importi riga sono con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.  
12. Se si desidera assegnare uno sconto, immettere una percentuale nel campo **% sconto riga**. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.  

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dei vendita vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Ripetere i passaggi da 9 a 12 per ogni prodotto che si desidera offrire al cliente.  

    I totali sotto le righe vengono automaticamente calcolati quando si creano o si modificano le righe.  
14. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati degli sconti su fattura per il cliente, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fatt. IVA esclusa**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).
15. Una volta completate le righe dell'offerta di vendita, scegliere l'azione **Invia tramite messaggio e-mail**.
16. Nella finestra **Invia messaggio e-mail** compilare tutti i campi restanti ed esaminare l'offerta di vendita inclusa. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).
17. Se il cliente accetta l'offerta, scegliere l'azione **Crea fattura** o **Crea ordine**.

L'offerta di vendita viene rimossa dal database. Viene creata una fattura, o un ordine, di vendita basata sulle informazioni contenute nell'offerta di vendita nella quale è possibile elaborare la vendita. Nel campo **Nr. offerta** dell'ordine o della fattura di vendita è presente il numero dell'offerta di vendita da cui è stato convertito. Per ulteriori informazioni vedere [Fatturare le vendite](sales-how-invoice-sales.md) o [Vendere prodotti](sales-how-sell-products.md).

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

