---
title: Utilizzo delle note di credito di vendita per elaborare resi o annullamenti di vendite | Documenti Microsoft
description: "Descrive come creare una nota di credito vendita per elaborare un reso, un annullamento o il rimborso per articoli o servizi per cui si è ricevuto il pagamento."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 06/21/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f08526054e99f742cedfefe036d8903304e54a56
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Procedura: Elaborare i resi o gli annullamenti vendite
Se un cliente desidera restituire gli articoli o ottenere il rimborso degli articoli o dei servizi che gli sono stati venduti e che ha pagato, è necessario creare e registrare una nota di credito di vendita in cui viene specificata la modifica richiesta. Per includere le informazioni corrette della fattura di vendita, è possibile creare la nota di credito di vendita da una fattura di vendita registrata o utilizzare la funzione di copia.  

> [!NOTE]  
>   Se una fattura di vendita registrata non è stata ancora pagata, è possibile utilizzare la funzione **Rettifica** o **Annulla** nella fattura di vendita registrata per stornare le transazioni. Queste funzionano solo per le fatture non pagate e non supportano i resi o le cancellazioni parziali. Per ulteriori informazioni, vedere [Procedura: Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md).

Oltre alla fattura di vendita registrata originale, è possibile collegare la nota di credito di vendita ad altri documenti di vendita, ad esempio un'altra fattura di vendita registrata, in quanto il cliente restituisce anche gli articoli consegnati con la fattura.

Un reso o un risarcimento può essere correlato solo ad alcuni degli articoli o dei servizi nella fattura di vendita originale. In questo caso, è necessario modificare le informazioni nelle righe della nota di credito di vendita. Quando si registra la nota di credito di vendita, i documenti di vendita influenzati dalla variazione vengono stornati ed è possibile creare un pagamento di rimborso per il cliente.  

È possibile inviare la nota di credito vendita registrata al cliente per confermare il reso o l'annullamento e comunicare che il valore correlato verrà rimborsato, ad esempio quando gli articoli vengono resi.

La registrazione della nota di credito annullerà anche tutti gli addebiti articolo assegnati al documento registrato, in modo che i movimenti valorizzazione articolo siano identici a prima dell'assegnazione dell'addebito articolo.

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Per creare una nuova nota di credito di vendita da una fattura di vendita registrata
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di vendita registrate**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Fatture vendita registrate** selezionare la fattura di vendita registrata che si desidera stornare, quindi scegliere l'azione **Crea nota credito di rettifica**.

    Nell'intestazione della nota di credito di vendita sono incluse alcune informazioni contenute nella fattura di vendita registrata. Tali informazioni possono, ad esempio, essere sostituite da nuove informazioni che riflettono il contratto di reso.  
3. Modificare le informazioni nelle righe in base al contratto, quali il numero di articoli resi o l'importo da rimborsare.
4. Scegliere l'azione **Collega movimenti**.
5. Nella finestra **Collega movimenti clienti**, selezionare la riga con il documento di vendita registrato a cui si desidera collegare la nota di credito di vendita, quindi scegliere l'azione **Collega-a ID**.

    L'identificativo della nota di credito di vendita viene visualizzato nel campo **Collega-a ID**.
6. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare se è inferiore all'importo originale.  

    Nella parte inferiore della finestra **Collega movimenti clienti** è possibile vedere l'importo totale da collegare per stornare tutti i movimenti coinvolti, ad esempio quando il valore del campo **Saldo** è zero.
7. Scegliere il pulsante **OK**. Quando si registra la nota di credito di vendita, viene applicata ai documenti di vendita registrati.

    Dopo avere creato o modificato le righe della nota di credito di vendita e avere specificato le applicazioni singole o multiple, è possibile passare alla registrazione della nota di credito di vendita.   
8. Scegliere l'azione **Registra e invia**.  

Viene visualizzata la finestra di dialogo **Registra e invia conferma** contenente il metodo di invio preferito del cliente. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Per ulteriori informazioni, vedere [Procedura: Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  

I documenti di vendita registrati che sono stati collegati alla nota di credito sono ora stornati ed è possibile creare un pagamento del rimborso per il cliente. La nota di credito di vendita viene rimossa e sostituita con un nuovo documento nell'elenco delle note di credito di vendita registrate.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Per creare una nota di credito di vendita da zero
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Note credito vendita**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** per aprire una nuova nota di credito di vendita vuota.
3. Nel campo **Cliente** immettere il nome di un cliente esistente.
4. Scegliere l'azione **Copia documento**.
5. Nella finestra **Copia documento vendita**, nel campo **Tipo di documento**, selezionare **Fattura registrata**.
6. Scegliere il campo **Nr. documento** per aprire la finestra **Fatture vendita registrate**, quindi selezionare la fattura di vendita registrata che contiene le righe da stornare.
7. Selezionare la casella di controllo **Ricalcola righe** se si desidera che le righe copiate della fattura di vendita registrata vengano aggiornate con le modifiche al prezzo dell'articolo e al costo unitario poiché la fattura è stata registrata.
8. Scegliere il pulsante **OK**. Le righe della fattura copiate vengono inserite nella nota di credito vendite.
9. Completare la nota di credito di vendita come descritto nella sezione "Per creare una nota di credito di vendita da una fattura di vendita registrata" del presente argomento.

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Procedura: Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

