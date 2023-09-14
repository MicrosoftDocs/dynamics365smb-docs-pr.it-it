---
title: Effettuare spedizioni dirette (contiene video)
description: Viene descritto come creare un ordine di vendita collegato a un ordine di acquisto per consentire la spedizione diretta dal fornitore al cliente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: bholtorf
---
# Effettuare spedizioni dirette

Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.

Quando un ordine cliente è contrassegnato per la spedizione di consegna e si crea un ordine d'acquisto specificando il cliente nel campo **Spedire a** **Indirizzo cliente**, è possibile collegare i due documenti e istruire il fornitore spedire direttamente al cliente.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## Per creare un ordine di vendita per una spedizione diretta

Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo e indicare sulla riga di vendita che la vendita richiede la spedizione diretta.

1. Creare un ordine cliente per un articolo. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
2. Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**. 

> [!TIP]
> Per impostazione predefinita, la casella di controllo Spedizione diretta non è disponibile sulle righe. In caso contrario, puoi aggiungerla personalizzando la sezione di pagina che contiene le righe. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

## Per creare l'ordine di acquisto per la spedizione diretta

Per preparare una spedizione diretta, indicare nell'ordine di acquisto che l'articolo deve essere spedito al cliente, non a se stessi.

1. Creare un ordine di acquisto. Non compilare i campi nelle righe. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).
2. Nel campo **Spedire a**, selezionare **Indirizzo cliente**.
3. Nel campo **Cliente**, selezionare il cliente a cui si sta vendendo.
4. Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.
5. Nella pagina **Lista vendite**, seleziona l'ordine di vendita che è stato preparato nella sezione [Per creare un ordine di vendita per una spedizione diretta](#to-create-a-sales-order-for-drop-shipment).
6. Scegliere il pulsante **OK**.

Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.

Ora puoi dire al tuo venditore di spedire gli articoli direttamente al cliente. Ad esempio, potresti inviare loro l'ordine tramite e-mail. 

Se il fornitore fornisce un numero di tracciabilità o informazioni simili, è possibile aggiungere tali informazioni in una riga ordine d'acquisto di tipo *Commento*.  

## Per creare più ordini di acquisto per spedizioni dirette

È inoltre possibile utilizzare la richiesta di approvvigionamento per creare l'ordine di acquisto per il fornitore. 

Il vantaggio di utilizzare la richiesta di approvvigionamento è che è possibile creare ordini di acquisto per tutte le spedizioni dirette in sospeso, quindi non è necessario crearle singolarmente. Ciò significa che non dovrai crearne una individualmente.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") icona, immetti **Richiesta di approvvigionamento**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.
3. Scegliere il pulsante **OK**.
4. Rivedere le righe dell'ordine di acquisto e nel campo **Nr. fornitore**, selezionare il fornitore che fornisce le merci richieste. 
5. Scegliere l'azione **Esegui messaggi di azione** per convertire le righe riviste in un ordine di acquisto.

## Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita

* Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.

## Per registrare una spedizione diretta

Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito. È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Aprire l'ordine di vendita creato nella sezione [Per creare un ordine di vendita per una spedizione diretta](#to-create-a-sales-order-for-drop-shipment).
3. Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.
4. Scegliere l'azione **Registra** o **Registra e invia**.
5. Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.

## Vedi il relativo [training Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Vedere anche

[Creare ordini speciali](sales-how-to-create-special-orders.md)  
[Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md)  
[Vendere prodotti](sales-how-sell-products.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Vendite](sales-manage-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
