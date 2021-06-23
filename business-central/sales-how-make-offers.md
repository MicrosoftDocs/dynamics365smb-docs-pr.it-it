---
title: Crea un'offerta di vendita per un cliente
description: Descrive come creare un documento di un'offerta di vendita o una richiesta di offerta (RdO) per registrare la propria offerta a un cliente per la vendita di prodotti in base a termini determinati.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: a538b7099521b10227bf5aeaefad0a9c60971068
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115542"
---
# <a name="make-sales-quotes"></a>Creare offerte di vendita

Creare un'offerta di vendita per registrare la propria offerta al cliente per vendere alcuni prodotti a determinate condizioni di consegna e di pagamento. È possibile inviare l'offerta di vendita al cliente per comunicare l'offerta. È possibile inviare il documento via e-mail come allegato PDF. È inoltre possibile fare in modo che il corpo e-mail venga precompilato con un riepilogo dell'offerta. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Quando si negozia con il cliente, è possibile modificare e inviare nuovamente l'offerta di vendita in base alle esigenze. Se il cliente accetta l'offerta, si converte l'offerta di vendita in un ordine o una fattura di vendita in cui viene elaborata la vendita. Per ulteriori informazioni vedere [Fatturare le vendite](sales-how-invoice-sales.md) o [Vendere prodotti](sales-how-sell-products.md).

È possibile compilare i campi cliente nell'offerta di vendita in due modi a seconda che il cliente sia già registrato o meno. Vedere i passaggi 2 e 3 della procedura riportata di seguito.

## <a name="to-create-a-sales-quote"></a>Per creare un'offerta di vendita

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Offerte vendita** e quindi scegliere il collegamento correlato.
2. Nel campo **Cliente** immettere il nome di un cliente esistente.

   Altri campi nella pagina **Offerte di vendita** contengono informazioni standard del cliente selezionato.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]

    Diversi campi nell'offerta di vendita sono ora compilati con le informazioni specificate nella nuova scheda cliente.  
3. Compilare i restanti campi della pagina **Offerta di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    È ora possibile compilare le righe dell'ordine di vendita per i prodotti che si vendono al cliente o per ogni transazione con il cliente per il quale si desidera effettuare la registrazione in un conto C/G.  

    Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.  

4. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.
5. Nel campo **Nr.** selezionare un record per effettuare la registrazione in base al valore nel campo **Tipo**.

    Lasciare il campo **Nr.** vuoto nei seguenti casi:
    - Se la riga è destinata a un commento. Compilare il commento nel campo **Descrizione**.
    - Se la riga è destinata a un articolo di catalogo. Scegliere l'azione **Seleziona articoli di catalogo**. Per ulteriori informazioni, vedere [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).

6. Nel campo **Quantità** immettere qui il numero di unità di articoli, addebiti o transazioni che la riga registrerà per il cliente.

    > [!NOTE]  
    >  Se l'articolo è di tipo **Assistenza** o se il campo **Tipo** contiene **Risorsa**, la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga. Per ulteriori informazioni, vedere [Impostare unità di misura articolo](inventory-how-setup-units-of-measure.md).

    Il valore nel campo **Importo riga** viene calcolato come *Prezzo unitario* x *Quantità*.  

    Il prezzo e gli importi riga sono con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.  
7. Se si desidera assegnare uno sconto, immettere una percentuale nel campo **% sconto riga**. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.  

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dei vendita vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Ripetere i passaggi da 4 a 7 per ogni prodotto che si desidera offrire al cliente.

    I totali sotto le righe vengono automaticamente calcolati quando si creano o si modificano le righe.  
9. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati degli sconti su fattura per il cliente, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fatt. IVA esclusa**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Per compilare automaticamente il campo **Offerta valida fino alla data** con un determinato numero di giorni dopo la creazione di un'offerta, è possibile compilare il campo **Calcolo validità offerta** nella pagina **Contabilità clienti**.

10. Una volta completate le righe dell'offerta di vendita, scegliere l'azione **Invia tramite messaggio e-mail**.
11. Nella pagina **Invia messaggio e-mail** compilare tutti i campi restanti ed esaminare l'offerta di vendita inclusa. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).
12. Se il cliente accetta l'offerta, scegliere l'azione **Crea fattura** o **Crea ordine**.

L'offerta di vendita viene rimossa dal database. Viene creata una fattura, o un ordine, di vendita basata sulle informazioni contenute nell'offerta di vendita nella quale è possibile elaborare la vendita. Nel campo **Nr. offerta** dell'ordine o della fattura di vendita è presente il numero dell'offerta di vendita da cui è stato convertito. Per ulteriori informazioni vedere [Fatturare le vendite](sales-how-invoice-sales.md) o [Vendere prodotti](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Numero di documento esterni

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]