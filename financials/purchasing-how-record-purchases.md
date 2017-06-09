---
title: 'Procedura: Registrare gli acquisti | Documenti Microsoft'
description: Viene descritto come acquistare articoli di tipo Magazzino o Assistenza creando e registrando le fatture o gli ordini di acquisto.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a56cfc08495a8d57eaa9a8f355549bf3575cd29c
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-purchases"></a>Procedura: Registrare gli acquisti
È possibile creare una fattura o un ordine di acquisto per registrare il costo di acquisto e per tenere traccia del conto fornitori. Se è necessario verificare un magazzino, anche le fatture e gli ordini di acquisto vengono utilizzati per aggiornare in modo dinamico i livelli di magazzino in modo da ridurre i costi di magazzino al minimo e migliorare l'assistenza clienti. I costi di acquisto, incluse le spese di assistenza, e i valori di magazzino derivanti dalla registrazione delle fatture o gli ordini di acquisto contribuiscono alle cifre di profitto e altri indicatori KPI finanziari presenti nella home page.

**Nota**: è necessario utilizzare gli ordini di acquisto se il processo di acquisto richiede la registrazione delle le ricevute parziali di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile presso il fornitore. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di acquisto. Per ulteriori informazioni, vedere [Procedura: Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di acquisto funzionano come le fatture di acquisto. La seguente procedura è basata su una fattura di acquisto. I passaggi sono simili per un ordine di acquisto.

Quando si ricevono gli articoli di magazzino, o quando il servizio acquistato viene completato, si registra la fattura o l'ordine di acquisto per aggiornare il magazzino e i record finanziari e per attivare il pagamento al fornitore in base alle condizioni di pagamento. Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).

**Attenzione**: non registrare una fattura di acquisto fino a quando non si ricevono gli articoli e si conosce il costo finale dell'acquisto, incluse le spese aggiuntive. In caso contrario, il valore di magazzino e le cifre di margine possono risultare distorti.

È possibile correggere o annullare in modo semplice una fattura di acquisto registrata prima che venga pagata al fornitore. Ciò risulta utile se si desidera correggere un errore di digitazione o se si desidera modificare l'acquisto in una fase iniziale dell'elaborazione dell'ordine. Per ulteriori informazioni, vedere [Procedura: Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Se è già stato eseguito il pagamento degli articoli nella fattura di acquisto registrata, è necessario creare una nota di credito di acquisto per stornare l'acquisto. Per ulteriori informazioni vedere [Procedura: Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md).

Gli articoli possono essere di tipo **Magazzino** o **Assistenza**. Per ulteriori informazioni, vedere [Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md). Il processo della fattura di acquisto è lo stesso per entrambi i tipi di articoli.

**Nota**: la funzionalità degli ordini di acquisto richiede che l'esperienza sia impostata su **Suite**. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

È possibile compilare i campi fornitore nella fattura di acquisto in due modi a seconda che il fornitore sia già registrato o meno.

## <a name="to-create-a-purchase-invoice"></a>Per creare una fattura di acquisto
1. Nella home page scegliere l'azione **Fattura acquisto**.  
2. Nel campo **Fornitore** immettere il nome del fornitore esistente.

    Altri campi nella finestra **Fattura di vendita** ora vengono compilati con le informazioni standard del fornitore selezionato. Se il fornitore non è registrato, è necessario attenersi alla seguente procedura:
3. Nel campo **Fornitore** immettere il nome del nuovo fornitore.
4. Nella finestra di dialogo relativa alla registrazione del nuovo fornitore fare clic su **Sì**.
5. Nella finestra **Selezionare un modello per un nuovo fornitore** scegliere un modello su cui basare la scheda del nuovo fornitore, quindi scegliere **OK**.
6. Una nuova scheda fornitore verrà visualizzata, precompilata con le informazioni sul modello fornitore selezionato. Il campo **Nome** è precompilato con il nome del nuovo fornitore immesso nella fattura di acquisto.
7. Precedere compilando i restanti campi nella scheda fornitore. Per ulteriori informazioni, vedere [Procedura: Registrare nuovi fornitori](purchasing-how-register-new-vendors.md).  
8. Una volta completata la scheda fornitore, fare clic su **OK** per tornare alla finestra **Fattura di acquisto**.

    Numerosi campi della finestra **Fattura di acquisto** vengono compilati con le informazioni specificate nella nuova scheda fornitore.
9. Compilare i restanti campi della finestra **Fattura di acquisto** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    A questo punto si è pronti a compilare le righe della fattura di acquisto con gli articoli di magazzino o i servizi acquistati presso il fornitore.

    **Nota**: se sono state impostate righe di acquisto periodiche per il fornitore, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nella fattura scegliendo l'azione **Ottieni righe acquisto ricorrenti**.
10. Nella Scheda dettaglio **Righe**, nel campo **Nr. articolo**, immettere il numero di un'assistenza o di un articolo di magazzino.
11. Nel campo **Quantità** immettere il numero di articoli da acquistare.

    **Nota**: per gli articoli di tipo **Assistenza**, la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga.

    Il campo **Importo riga** viene aggiornato al valore del campo **Costo unitario diretto** moltiplicato per il valore del campo **Quantità**.

    Il prezzo e l'importo riga vengono visualizzati con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda fornitore.
12. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.** nella parte inferiore della fattura.

    **Nota**: se sono stati impostati degli sconti su fattura per il fornitore, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura fornitore** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fattura**.
13. Quando si ricevono l'assistenza o gli articoli acquistati, scegliere **Registra**.

L'acquisto si riflette ora nel magazzino e nei record finanziari e il pagamento fornitore viene attivato. La fattura di acquisto viene rimossa dall'elenco delle fatture di acquisto e sostituita con un nuovo documento nell'elenco delle fatture di acquisto registrate.

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Procedura: Acquistare i prodotti per una vendita](purchasing-how-purchase-products-sale.md)  
[Procedura: Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Procedura: Preparare le spedizioni dirette](sales-how-drop-shipment.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

