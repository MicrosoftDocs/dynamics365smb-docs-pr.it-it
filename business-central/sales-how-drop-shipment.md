---
title: Collegare un ordine di vendita a un ordine di acquisto per una spedizione diretta (video) | Documenti Microsoft
description: Viene descritto come creare un ordine di vendita collegato a un ordine di acquisto per consentire la spedizione diretta dal fornitore al cliente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 19bfb28494a6ee5a4650f32fd2794c0254eff561
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144829"
---
# <a name="make-drop-shipments"></a>Effettuare spedizioni dirette

Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.

Quando un ordine cliente è contrassegnato per la spedizione di consegna e si crea un ordine d'acquisto specificando il cliente nel campo **Spedire a** **Indirizzo cliente**, è possibile collegare i due documenti e istruire il fornitore spedire direttamente al cliente.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Per creare un ordine di vendita per una spedizione diretta

Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo e indicare sulla riga di vendita che la vendita richiede la spedizione diretta.

1. Creare un ordine cliente per un articolo. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
2. Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**. Utilizzare la funzione **Scegli colonne** se il campo non è visualizzato. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Per creare l'ordine di acquisto per la spedizione diretta

Per preparare una spedizione diretta, indicare nell'ordine di acquisto che l'articolo deve essere spedito al cliente, non a se stessi.

1. Creare un ordine di acquisto. Non compilare i campi nelle righe. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).
2. Nel campo **Spedire a**, selezionare **Indirizzo cliente**.
3. Nel campo **Cliente**, selezionare il cliente a cui si sta vendendo.
4. Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.
5. Nella pagina **Lista vendite**, selezionare l'ordine di vendita che è stato preparato nella sezione [Per creare un ordine di vendita per una spedizione diretta](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
6. Scegliere il pulsante **OK**.

Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.

È possibile istruire il fornitore di spedire gli articoli al cliente, ad esempio spedendo l'ordine di acquisto come PDF.     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Per creare più ordini di acquisto per spedizioni dirette

È inoltre possibile utilizzare la richiesta di approvvigionamento per creare l'ordine di acquisto per il fornitore. Il vantaggio di utilizzare la richiesta di approvvigionamento è che è possibile creare ordini di acquisto per tutte le spedizioni dirette in sospeso, quindi non è necessario crearle singolarmente.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Richieste di approvvigionamento**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.
3. Scegliere il pulsante **OK**.
4. Rivedere le righe dell'ordine di acquisto e nel campo **Nr. fornitore**, selezionare il fornitore che fornisce le merci richieste. 
5. Scegliere l'azione **Esegui messaggi di azione** per convertire le righe riviste in un ordine di acquisto.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita

* Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.

## <a name="to-post-a-drop-shipment"></a>Per registrare una spedizione diretta

Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito. È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Aprire l'ordine di vendita creato nella sezione [Per creare un ordine di vendita per una spedizione diretta](#to-create-a-sales-order-for-drop-shipment).
3. Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.
4. Scegliere l'azione **Registra** o **Registra e invia**.
5. Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.

## <a name="see-also"></a>Vedi anche

[Creare ordini speciali](sales-how-to-create-special-orders.md)  
[Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md)  
[Vendere prodotti](sales-how-sell-products.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Vendite](sales-manage-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]