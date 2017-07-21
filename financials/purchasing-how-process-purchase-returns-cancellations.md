---
title: Utilizzare note di credito di acquisto per elaborare resi o annullamenti | Documenti Microsoft
description: Descrizione di come creare e registrare una nota di credito acquisto quando si desidera effettuare un reso degli articoli a un fornitore o annullare servizi acquistati.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 887add30a1ec72b7de961e03161bfc34826980fc
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Procedura: Elaborare i resi o gli annullamenti acquisti
Se si desidera restituire gli articoli al fornitore o annullare l'assistenza acquistata, è possibile creare e registrare una nota di credito di acquisto in cui viene specificata la modifica richiesta rispetto alla fattura di acquisto originale. Per includere le informazioni corrette della fattura di acquisto, è possibile creare la nota di credito di acquisto da una fattura d'acquisto registrata o utilizzare la funzione di copia.

> [!NOTE]  
>   Se una fattura di acquisto registrata non è stata ancora pagata, allora è possibile utilizzare le funzioni **Annulla** o **Rettifica** nella fattura di acquisto registrata per stornare automaticamente le transazioni implicate. Queste funzionano solo per le fatture non pagate e non supportano i resi o le cancellazioni parziali. Per ulteriori informazioni, vedere [Procedura: Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

In genere, si crea una nota di credito di acquisto in risposta a una nota di credito inviata da un fornitore. La nota di credito di acquisto funziona come la documentazione interna del processo relativo alla nota di credito per scopi contabili.

La modifica può essere correlata a tutti o solo ad alcuni prodotti nella fattura di acquisto originale. Di conseguenza, è possibile restituire parzialmente gli articoli ricevuti o richiedere il risarcimento parziale dei servizi ricevuti. In questo caso, è necessario modificare le informazioni della fattura di acquisto copiata.

Oltre alla fattura di acquisto registrata originale, è possibile collegare la nota di credito di acquisto ad altri documenti di acquisto, ad esempio un'altra fattura di acquisto registrata, in quanto si restituiscono anche gli articoli consegnati con la fattura.

La registrazione della nota di credito annullerà anche tutti gli addebiti articolo assegnati al documento registrato, in modo che i movimenti valorizzazione articolo siano identici a prima dell'assegnazione dell'addebito articolo.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Per creare una nota di credito di acquisto da una fattura di acquisto registrata
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di acquisto registrate**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Fatture acquisto registrate** selezionare la fattura di acquisto registrata che si desidera stornare, quindi scegliere l'azione **Crea nota credito di rettifica**.

    La maggior parte dei campi nella testata della nota di credito di acquisto viene compilata con le informazioni della fattura di acquisto registrata. È possibile modificare tutti i campi, ad esempio con nuove informazioni che riflettono il contratto di reso.
3. Modificare le informazioni nelle righe in base al contratto, quali il numero di articoli resi o l'importo da rimborsare.
4. Scegliere l'azione **Collega movimenti**.
5. Nella finestra **Collega movimenti fornitori**, selezionare la riga con il documento di acquisto registrato a cui si desidera collegare la nota di credito di acquisto, quindi scegliere l'azione **Collega-a ID**. Il numero della nota di credito di acquisto viene inserito nel campo **Collega-a ID**.
6. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare se inferiore all'importo originale.

    Nella parte inferiore della finestra **Collega movimenti fornitori** è possibile vedere l'importo totale da collegare per stornare tutti i movimenti coinvolti, ad esempio quando il valore del campo **Saldo** è zero.
7. Scegliere il pulsante **OK**. Quando si registra la nota di credito di acquisto, verrà collegata ai documenti di acquisto registrati specificati.

    Dopo avere creato o modificato le righe della nota di credito di acquisto necessarie e aver specificato uno o più collegamenti, è possibile passare alla registrazione della nota di credito di acquisto.
8. Scegliere l'azione **Registra**.

Le fatture di acquisto registrate a cui si applica la nota di credito vengono ora stornate. Se è già stata pagata la fattura originale, il fornitore dovrà rimborsare il pagamento. Se la nota di credito riguarda solo parte del prodotto nella fattura originale, è possibile pagare solo l'importo restante nella fattura di acquisto originale per chiuderla.

La nota di credito di acquisto viene rimossa e sostituita con un nuovo documento nell'elenco delle note di credito di acquisto registrate.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>Per creare una nota di credito di acquisto da zero
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Note credito acquisto**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** per aprire una nuova nota di credito di acquisto vuota.
3. Nel campo **Fornitore** immettere il nome del fornitore esistente.
4. Scegliere l'azione **Copia documento**.
5. Nella finestra **Copia documento acquisto**, nel campo **Tipo di documento**, selezionare **Fattura registrata**.
6. Scegliere il campo **Nr. documento** per aprire la finestra **Fatture acquisto registrate**, quindi selezionare la fattura di acquisto registrata che contiene le righe da stornare.
7. Selezionare la casella di controllo **Ricalcola righe** se si desidera che le righe copiate della fattura di acquisto registrata vengano aggiornate con le modifiche al prezzo dell'articolo e al costo unitario poiché la fattura è stata registrata.
8. Scegliere il pulsante **OK**. Le righe della fattura copiate vengono inserite nella nota di credito di acquisto.
9. Completare la nota di credito acquisto come descritto nella sezione "Per creare una nota di credito di acquisto da una fattura di acquisto registrata" del presente argomento.

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Procedura: Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

