---
title: Registrare gli acquisti con le fatture di acquisto
description: Viene descritto come acquistare articoli di magazzino o non o risorse creando e registrando le fatture o gli ordini di acquisto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 09/07/2021
ms.author: edupont
ms.openlocfilehash: 18aef7bfc5324d17d2af9f4aa4ff0ba2602c70e0
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482399"
---
# <a name="record-purchases-with-purchase-invoices"></a>Registrare gli acquisti con le fatture di acquisto

È possibile creare una fattura o un ordine di acquisto per registrare il costo di acquisto e per tenere traccia del conto fornitori. Se è necessario verificare un magazzino, anche le fatture e gli ordini di acquisto vengono utilizzati per aggiornare in modo dinamico i livelli di magazzino in modo da ridurre i costi di magazzino al minimo e migliorare l'assistenza clienti. I costi di acquisto, incluse le spese di assistenza, e i valori di magazzino derivanti dalla registrazione delle fatture o degli ordini di acquisto contribuiscono alle cifre di profitto e altri indicatori KPI finanziari in Gestione ruolo utente.

## <a name="create-purchase-invoices"></a>Crea fatture di acquisto

Oltre all'acquisto di articoli fisici (tipi di articolo **Inventario**) che influiscono sulla valutazione del magazzino, è possibile acquistare servizi rappresentati da unità di tempo. Puoi farlo con il tipo di articolo **Servizio** o con il tipo di riga **Risorsa**.

Quando si ricevono gli articoli di magazzino, o quando il servizio acquistato viene completato, si registra la fattura o l'ordine di acquisto per aggiornare il magazzino e i record finanziari e per attivare il pagamento al fornitore in base alle condizioni di pagamento. Per altre informazioni, vedere [Registrazione degli acquisti](ui-post-purchases.md) ed [Effettuare i pagamenti](payables-make-payments.md).

> [!CAUTION]  
> Non registrare gli articoli fisici per una fattura di acquisto fino a quando non si ricevono gli articoli e si conosce il costo finale dell'acquisto, incluse le spese aggiuntive. In caso contrario, il valore di magazzino e le cifre di margine possono risultare distorti.

### <a name="to-create-a-purchase-invoice"></a>Per creare una fattura di acquisto

Di seguito viene descritto come creare una fattura di acquisto. I passaggi sono simili per un ordine di acquisto. La differenza principale è che gli ordini acquisto hanno campi e azioni aggiuntivi per la gestione fisica degli articoli.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.  
2. Nel campo **Fornitore** immettere il nome del fornitore esistente.

    Altri campi nella pagina **Fattura di vendita** ora vengono compilati con le informazioni standard del fornitore selezionato. Se il fornitore non è registrato, è necessario attenersi alla seguente procedura:

    1. Nel campo **Fornitore** immettere il nome del nuovo fornitore.
    2. Nella finestra di dialogo relativa alla registrazione del nuovo fornitore fare clic su **Sì**.
    3. Per ulteriori informazioni su come compilare la scheda fornitore, vedere [Registrare nuovi fornitori](purchasing-how-register-new-vendors.md).  
    4. Una volta completata la scheda fornitore, fare clic su **OK** per tornare alla pagina **Fattura di acquisto**.

3. Compilare i restanti campi della pagina **Fattura di acquisto** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    A questo punto si è pronti a compilare le righe della fattura di acquisto con gli articoli o le risorse acquistati presso il fornitore.

    > [!NOTE]  
    > Se sono state impostate righe di acquisto periodiche per il fornitore, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nella fattura scegliendo l'azione **Ottieni righe acquisto ricorrenti**.
4. Nella Scheda dettaglio **Righe** del campo **Nr. articolo** immettere il numero di un articolo di magazzino o di un servizio.
5. Nel campo **Quantità** immettere il numero di articoli da acquistare.

    Il campo **Importo riga** viene aggiornato al valore del campo **Costo unitario diretto** moltiplicato per il valore del campo **Quantità**.

    Il prezzo e l'importo riga vengono visualizzati con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda fornitore.

    I campi dei totali sotto le righe vengono automaticamente aggiornati quando si creano o si modificano le righe per visualizzare gli importi che verranno registrati nei libri contabili.

6. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.** nella parte inferiore della fattura.

    > [!NOTE]  
    > Se sono stati impostati degli sconti su fattura per il fornitore, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura fornitore** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fattura**.
7. Quando si ricevono l'assistenza o gli articoli acquistati, scegliere **Registra**.

L'acquisto si riflette ora nel magazzino, nei movimenti contabili risorse e nei record finanziari e il pagamento fornitore viene attivato. La fattura di acquisto viene rimossa dall'elenco delle fatture di acquisto e sostituita con un nuovo documento nell'elenco delle fatture di acquisto registrate.  

> [!NOTE]
> In casi rari, gli importi registrati possono discostarsi da ciò che viene visualizzato nei campi dei totali. Ciò è in genere dovuto ai calcoli di arrotondamento in relazione all'IVA o all'imposta sulle vendite.
>
> Per verificare gli importi che verranno effettivamente registrati, è possibile utilizzare la pagina **Statistiche**, che tiene conto dei calcoli di arrotondamento. Inoltre, se si sceglie l'azione **Rilascia**, i campi dei totali verranno aggiornati per includere i calcoli di arrotondamento.

## <a name="when-to-use-purchase-orders"></a>Quando utilizzare gli ordini di acquisto

Utilizzare gli ordini di acquisto se il processo di acquisto richiede la registrazione delle le ricevute parziali di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile presso il fornitore. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di acquisto. Per ulteriori informazioni, vedere [Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di acquisto funzionano come le fatture di acquisto. La seguente procedura è basata su una fattura di acquisto. I passaggi sono simili per un ordine di acquisto.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="selling-non-inventory-items"></a>Vendita di articoli non in magazzino

Gli articoli in una fattura di acquisto possono essere di tipo **Inventario**, **Assistenza**, **Risorsa** e **Non in inventario** per specificare se la scheda articolo rappresenta un'unità fisica di inventario, un'unità di misura del tempo della manodopera o un'unità fisica non gestita in magazzino. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md). Il processo della fattura di acquisto è lo stesso per tutti e tre i tipi di articoli.

> [!NOTE]
> Con il tipo di riga acquisto **Risorsa**, è inoltre possibile acquistare risorse esterne, ad esempio, per fatturare a un fornitore per il lavoro eseguito. Per ulteriori informazioni, vedere [Impostare risorse](projects-how-setup-resources.md).
>
> Per utilizzare una risorsa acquistata, potrebbe essere necessario impostare la capacità della risorsa e assegnarla manualmente a un processo. L'acquisto di una risorsa creerà un movimento contabile di risorsa, tuttavia, i movimenti contabili non vengono monitorati per quantità e valore come, ad esempio, per gli articoli. Se è richiesto il monitoraggio della quantità e del valore, considera l'utilizzo di altri tipi di voci.

## <a name="posted-invoices"></a>Fatture registrate

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

È possibile correggere o annullare in modo semplice una fattura di acquisto registrata prima che venga pagata al fornitore. Ciò risulta utile se si desidera correggere un errore di digitazione o se si desidera modificare l'acquisto in una fase iniziale dell'elaborazione dell'ordine. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Se è già stato eseguito il pagamento degli articoli o dei servizi nella fattura di acquisto registrata, è necessario creare una nota di credito di acquisto per stornare l'acquisto. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md).

[Apri l'elenco **Fatture acquisto registrate**](https://businesscentral.dynamics.com/?page=146) in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Numero di documento esterni

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Impostare risorse](projects-how-setup-resources.md)  
[Registrazione di acquisti](ui-post-purchases.md)  
[Richiedere le offerte](purchasing-how-request-quotes.md)  
[Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md)  
[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Preparare le spedizioni dirette](sales-how-drop-shipment.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]