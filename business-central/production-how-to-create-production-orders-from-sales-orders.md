---
title: Creare gli ordini di produzione dagli ordini di vendita
description: Informazioni sui diversi modi per creare ordini di produzione per gli articoli prodotti direttamente dagli ordini di vendita.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# <a name="create-production-orders-from-sales-orders"></a><a name="create-production-orders-from-sales-orders"></a>Creare gli ordini di produzione dagli ordini di vendita

È possibile creare ordini di produzione per gli articoli prodotti direttamente dagli ordini di vendita.  

## <a name="to-create-a-production-order-from-a-sales-order"></a><a name="to-create-a-production-order-from-a-sales-order"></a>Per creare gli ordini di produzione dagli ordini di vendita

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Selezionare l'ordine di vendita per il quale creare un ordine di produzione.  
3. Scegliere l'azione **Pianifica**. La pagina **Pianifica ordine vendita** mostra la disponibilità dell'articolo.  
4. Selezionare l'azione **Crea ordine produzione**.  
5. Selezionare lo stato e il tipo di ordine.  
6. Scegli il pulsante **Sì** per creare uno o più ordini di produzione per le righe che hanno **Ordine prod.** nel loro campo **Sistema di rifornimento**.

    > [!NOTE]  
    > Le righe della domanda che hanno **Ord. prod.** nel campo **Sistema di rifornimento** rappresentano gli ordini di produzione sottostanti. Dopo aver generato questi ordini di produzione, ricordati di identificare eventuali domande di componenti non soddisfatte. Utilizza la pagina **Pianificazione ordini** o l'azione **Ripianifica** per identificare la domanda non soddisfatta.
    >
    > Quando crei ordini di produzione per gli ordini di vendita con la pagina Pianificazione ordini di vendita, vengono applicati collegamenti ordine su ordine tra la domanda e l'offerta. Quando sono presenti collegamenti ordine su ordine, il sistema di pianificazione non include l'approvvigionamento o il magazzino collegato nella procedura di bilanciamento. Per ulteriori informazioni sul bilanciamento, vai a [Collegamenti ordine su ordine](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## <a name="order-type"></a><a name="order-type"></a>Tipo ordine

La seguente tabella descrive due modi per creare ordini di produzione.

|Opzione|Descrizione|
|------|-----------|
|Ordine articolo|Viene creato un ordine di produzione per ogni articolo rappresentato da una riga nella pagina **Pianifica ordine vendita**.|
|Ordine progetto|Viene creato un ordine di produzione di più righe per tutti gli articoli rappresentati dalle righe nella pagina **Pianifica ordine vendita**. Quando usi gli ordini di progetto, il campo **Tipo di origine** dell'ordine di produzione contiene **Intestazione vendite**. L'ordine ha una riga per ogni articolo della riga di vendita che deve essere prodotto.|

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
