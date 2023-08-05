---
title: Correggere o annullare le fatture di acquisto non pagate (video)
description: Descrive come correggere o annullare una fattura di acquisto registrata e creare automaticamente una nota di credito di acquisto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '138, 140, 146'
ms.date: 04/01/2021
ms.author: edupont
---
# Correggere o annullare le fatture di acquisto non pagate

È possibile correggere o annullare una fattura di acquisto registrata. Ciò risulta utile se si desidera correggere un errore di digitazione o se si desidera modificare l'acquisto in una fase iniziale dell'elaborazione dell'ordine.

Se è già stato eseguito il pagamento dei prodotti nella fattura di acquisto registrata, non è possibile correggerli o annullarli dalla fattura di acquisto registrata. È necessario creare manualmente una nota di credito acquisto per stornare l'acquisto, facoltativamente gestito con un ordine di reso acquisto. Lo stesso vale se si desidera modificare una fattura di acquisto registrata basata su ricevute di acquisto combinate. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md).

Nella pagina **Fattura acquisto registrata** è possibile scegliere il pulsante **Rettifica** o il pulsante **Annulla**. Quando si rettifica o si annulla una fattura di acquisto registrata, la nota di credito di acquisto viene applicata a tutti i movimenti contabili generali e di inventario creati quando la fattura di acquisto iniziale è stata registrata. Ciò consente di stornare la fattura di acquisto nei record finanziari e lascia la nota di credito di acquisto registrata correttiva per l'audit trail. Di seguito viene descritto l'utilizzo di **Rettifica** e di **Annulla**.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## Per correggere una fattura di acquisto registrata

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto registrate**, quindi scegli il collegamento correlato.  
2. Selezionare la fattura di acquisto che si desidera rettificare.  

    > [!NOTE]  
    >   Se viene selezionata la casella di controllo **Annullata**, non è possibile rettificare la fattura di acquisto registrata poiché è già stata rettificata o annullata.
3. Nella pagina **Fattura acquisto registrata** scegliere **Rettifica**.

    Viene creata una nuova fattura di acquisto con le stesse informazioni in cui è possibile apportare la rettifica. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md). Il campo **Annullato** nella fattura di acquisto registrata iniziale viene modificato in **Sì**.

    Una nota di credito di acquisto viene automaticamente creata e registrata per annullare la fattura di acquisto registrata iniziale.
4. Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di acquisto registrata che annulla la fattura di acquisto registrata iniziale.

## Per annullare una fattura di acquisto registrata

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto registrate**, quindi scegli il collegamento correlato.  
2. Selezionare la fattura di acquisto che si desidera annullare.

    > [!NOTE]  
    >   Se viene selezionata la casella di controllo **Annullata**, non è possibile annullare la fattura di acquisto registrata poiché è già stata rettificata o annullata.
3. Nella pagina **Fattura acquisto registrata** scegliere **Annulla**.

    Una nota di credito di acquisto viene automaticamente creata e registrata per annullare la fattura di acquisto registrata iniziale. Il campo **Annullato** nella fattura di acquisto registrata iniziale viene modificato in **Sì**.
4. Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di acquisto registrata che annulla la fattura di acquisto registrata iniziale.

### Anche la registrazione parziale delle fatture è supportata

Se l'annullamento è correlato a una registrazione parziale della fattura, la riga dell'ordine di acquisto di origine viene aggiornata per riflettere la quantità fatturata annullata. I campi **Qtà da fatturare** e **Qtà fatturata** nella riga dell'ordine fornitore correlato vengono reimpostati sui valori precedenti alla registrazione parziale.

## Vedi il relativo [training Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/)

## Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
