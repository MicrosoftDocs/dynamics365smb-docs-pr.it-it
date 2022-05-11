---
title: Spedire articoli
description: Questo argomento descrive come spedire gli articoli dalla warehouse in base alla configurazione warehouse per l'elaborazione della spedizione.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 5af803495f90590e288ad3d4e919995bb60e06b2
ms.sourcegitcommit: cfe4e924af2c89c09250270245e7a1eef1184bfc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626605"
---
# <a name="ship-items"></a>Spedire articoli

Quando gli articoli partono da una warehouse che non è impostata per l'elaborazione delle spedizioni warehouse, occorre registrare semplicemente la spedizione nel documento aziendale correlato, ad esempio un ordine di vendita, un ordine di assistenza, un ordine di reso acquisto o un ordine di trasferimento in uscita.

Quando gli articoli vengono spediti da una warehouse impostata in modo da richiedere l'elaborazione delle spedizioni warehouse, è possibile spedire articoli solo in base ai documenti di origine rilasciati alla warehouse da altri reparti della società affinché vengano elaborati.

> [!NOTE]
> Se la warehouse prevede cross-docking e collocazioni, per ogni riga, è possibile visualizzare la quantità di articoli inseriti nelle collocazioni di cross-dock. L'applicazione calcola le quantità automaticamente ogni volta che i campi della spedizione vengono aggiornati. Se si tratta di articoli facenti parte della spedizione che si sta preparando, è possibile creare un prelievo per tutte le righe e completare la spedizione. Per ulteriori informazioni, vedere [Sottoporre gli articoli a cross-dock](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>Per spedire gli articoli con un ordine di vendita

Di seguito viene descritto come spedire gli articoli da un ordine di vendita. I passaggi riguardanti gli ordini di reso acquisto, gli ordini di assistenza e gli ordini di trasferimento in uscita sono simili.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Aprire un ordine di vendita esistente o crearne uno. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
3. Nel campo **Qtà da Spedire** immettere la quantità spedita.

    Il valore nel campo **Qtà spedita** viene aggiornato. Se si tratta di una spedizione parziale, il valore è inferiore al valore nel campo **Quantità**.
4. Scegliere l'azione **Registra**.

> [!NOTE]
> Se l'organizzazione non utilizza gli ordini di vendita quando si registra la fattura di vendita, [!INCLUDE [prod_short](includes/prod_short.md)] presume che l'intero quantitativo sia stato spedito. Se ciò è in contraddizione con il funzionamento dell'organizzazione, si consiglia di utilizzare gli ordini di vendita e registrare le spedizioni come spiegato in questo articolo.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Per spedire gli articoli con una spedizione warehouse

Innanzitutto, creare un documento di spedizione da un documento di origine aziendale. Selezionare gli articoli specificati per la spedizione.

### <a name="to-create-a-warehouse-shipment"></a>Per creare una spedizione warehouse

In genere, l'impiegato responsabile della spedizione crea una spedizione warehouse. La seguente procedura descrive come creare manualmente la spedizione nella versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)], ma l'organizzazione potrebbe avere una parte automatizzata del processo, ad esempio con l'uso di scanner portatili o montati supportati da provider esterni.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Spedizioni warehouse**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  

    Compilare i campi della Scheda dettaglio **Generale**. Quando si recuperano le righe dei documenti di origine, alcune informazioni vengono copiate in ciascuna riga.  

    Per la configurazione warehouse con stoccaggi e prelievi guidati, se l'ubicazione dispone di una zona e di una collocazione di default per le spedizioni, i campi **Cod. zona** e **Cod. Collocazione** vengono compilati automaticamente ma è possibile modificarli in base alle esigenze.  

    > [!NOTE]  
    > Se si desidera spedire gli articoli con codici classe warehouse diversi dal codice classe della collocazione specificato nel campo **Cod. collocazione** della testata del documento, è necessario eliminare il contenuto del campo **Cod. collocazione** della testata prima di recuperare le righe del documento di origine per gli articoli.  
3. Scegliere l'azione **Prendi documenti origine**. Verrà visualizzata la pagina **Documenti origine**.

    Da una spedizione warehouse nuova o aperta, è possibile utilizzare la pagina **Filtri per ottenere documenti origine** per recuperare le righe del documento di origine rilasciato che definiscono quali articoli spedire.

    1. Scegliere l'azione **Usa filtri per richiamare doc. orig.**.  
    2. Per impostare un nuovo filtro, immettere un codice descrittivo nel campo **Codice**, quindi scegliere l'azione **Modifica**.  
    3. Definire il tipo di righe del documento origine che si desidera recuperare compilando i campi Filtro appropriati.  
    4. Scegliere l'azione **Esegui**.  

    Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono inserite nella pagina **Spedizione warehouse** da cui è stata attivata la funzione di filtro.  

    Le combinazioni di filtri definite vengono salvate nella pagina **Filtri per ottenere documenti origine** finché non saranno necessarie in momento successivo. È possibile creare un numero indefinito di combinazioni di filtri. È possibile modificare i criteri in qualsiasi momento scegliendo l'azione **Modifica**.

4. Selezionare i documenti di origine per i quali si desidera spedire gli articoli, quindi scegliere **OK**.  

Le righe dei documenti di origine verranno visualizzate nella pagina **Spedizione warehouse**. Il campo **Qtà da spedire** viene compilato con la quantità inevasa per ciascuna riga, ma è possibile modificare tale quantità in base alle esigenze. Se è stato eliminato il contenuto del campo **Cod. collocazione** della Scheda dettaglio **Generale** prima di recuperare le righe, è necessario immettere un codice collocazione appropriato in ogni riga di spedizione.  

> [!NOTE]  
> Non è possibile spedire un numero di articoli maggiore di quello indicato nel campo **Qtà inevasa** della riga del documento di origine. Per spedire più articoli, recuperare un altro documento di origine contenente una riga per l'articolo utilizzando la funzione di filtro appropriata.  

Dopo avere recuperato le righe per la spedizione, è possibile avviare il processo che consente di inviare le righe agli impiegati warehouse affinché procedano al prelievo.

### <a name="to-pick-and-ship"></a>Per prelevare gli articoli e procedere alla spedizione

In genere, un lavoratore warehouse responsabile del prelievo crea un documento di prelievo o apre un documento di prelievo già creato.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Spedizioni warehouse**, quindi scegli il collegamento correlato.
2. Selezionare la spedizione warehouse da cui si desidera prelevare, quindi scegliere l'azione **Crea prelievo**.
3. Compilare i campi della pagina di richiesta, quindi fare clic sul pulsante **OK**. Verrà creato il documento di prelievo della warehouse specificato.

    In alternativa, aprire un prelievo warehouse esistente.
4. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi**, quindi scegli il collegamento correlato. Selezionare il prelievo warehouse che si desidera utilizzare.

    Se la warehouse è impostata per l'utilizzo delle collocazioni, le righe di prelievo vengono convertite in righe di azione Prendere e Mettere.

    È possibile ordinare le righe, assegnare un addetto al prelievo, impostare un filtro breakbulk, se si utilizzano stoccaggi e prelievi guidati, e stampare le istruzioni di prelievo.

5. Eseguire il prelievo effettivo degli articoli e posizionarli nella collocazione di spedizione specificata, o nell'area di spedizione, se non si utilizzano le collocazioni.
6. Scegliere l'azione **Registra prelievo**.

    I campi **Qtà da spedire** e **Stato del documento** nella testata del documento di spedizione verranno aggiornati. Gli articoli prelevati non saranno più disponibili per il prelievo per altre spedizioni o per operazioni interne.
7. Stampare i documenti di spedizione, preparare i colli per la spedizione e registrare la spedizione.

Per ulteriori informazioni sul prelievo per spedizioni warehouse, vedere [Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).

È anche possibile utilizzare il prospetto prelievi per combinare diverse istruzioni di prelievo in un'unica istruzione (per più spedizioni) e ottimizzare in tal modo le operazioni di prelievo nella warehouse. Per ulteriori informazioni, vedere [Pianificare i prelievi nei prospetti](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Se si sta attendendo l'arrivo di determinati articoli nella warehouse e si utilizza la funzionalità di cross-dock, per ciascuna riga di spedizione o del prospetto prelievi in [!INCLUDE[prod_short](includes/prod_short.md)] verrà calcolata la quantità dell'articolo disponibile nella collocazione di cross-dock. Tale valore viene aggiornato ogni volta che si apre e si chiude il prospetto o il documento di spedizione. Per ulteriori informazioni, vedere [Sottoporre gli articoli a cross-dock](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Vedi anche

[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]