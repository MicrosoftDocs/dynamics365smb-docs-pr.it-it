---
title: 'Procedura: Registrare nuovi articoli | Documenti Microsoft'
description: Creare schede per i nuovi prodotti fisici, che si vendono dal magazzino, ad esempio pezzi, o per i servizi, che si vendono a ore.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 582e006291e51e19d80304d24ae055ce6ac8d698
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-items"></a>Procedura: Registrare nuovi articoli
Gli articoli, tra gli altri prodotti, sono alla base dell'azienda, delle merci o dei servizi trattati. Ogni articolo deve essere registrato come scheda articolo.

Le schede articolo contengono le informazioni richieste per l'acquisto, l'archiviazione, la consegna e la contabilità degli articoli.

La scheda articolo può essere di tipo **Magazzino** o **Assistenza** per specificare se l'articolo corrisponde a un'unità fisica o a un'unità di tempo di lavoro. Oltre ad alcuni campi correlati agli aspetti fisici di un articolo, tutti i campi della scheda articolo funzionano in modo analogo per gli articoli e i servizi di magazzino. Per ulteriori informazioni sulla vendita di un articolo, vedere [Procedura: Vendere prodotti](sales-how-sell-products.md) o [Procedura: Fatturare le vendite](sales-how-invoice-sales.md).

È possibile che un articolo sia strutturato come articolo padre con elementi figlio sottostanti in una distinta base (BOM). In [!INCLUDE[d365fin](includes/d365fin_md.md)] una distinta base è detta DB assemblaggio. Utilizzare le DB assemblaggio per strutturare gli articoli padre da vendere come kit costituiti da componenti del padre o da assemblare su ordine o per magazzino. Per ulteriori informazioni, vedere [Procedura: Utilizzare le distinte base](inventory-how-work-BOMs.md).

**Nota**: se esistono i modelli articolo per diversi tipi di articolo, allora verrà visualizzata una finestra quando si crea una nuova scheda articolo da cui è possibile selezionare un modello appropriato. Se esiste solo un modello articolo, allora le nuove schede articolo utilizzeranno sempre tale modello.

## <a name="to-create-a-new-item-card"></a>Per creare una nuova scheda articolo
1. Nella home page scegliere l'azione **Articoli** per aprire l'elenco degli articoli esistenti.  
2. Nella finestra **Articoli** scegliere l'azione **Nuovo**.

    Se esiste solo un modello articolo, allora verrà visualizzata una nuova scheda articolo con alcuni campi compilati con le informazioni derivanti dal modello.
3. Nella finestra **Selezionare un modello per un nuovo articolo** scegliere il modello da utilizzare per la nuova scheda articolo.
4. Scegliere il pulsante **OK**. Una nuova scheda articolo verrà visualizzata con alcuni campi compilati con le informazioni del modello.
5. Continuare a compilare o a modificare i campi della scheda articolo in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nella Scheda dettaglio **Prezzo e registrazione** è possibile visualizzare gli sconti o i prezzi speciali che si concedono per l'articolo se vengono soddisfatti determinati criteri, come cliente, quantità minima di ordine o data di scadenza. Ogni riga rappresenta un prezzo speciale o uno sconto riga. Ogni colonna rappresenta un criterio da applicare per garantire il prezzo speciale immesso nel campo **Prezzo unitario** o lo sconto riga immesso nel campo **Sconto riga**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).

L'articolo è ora registrato e la scheda articolo è pronta per essere utilizzata nei documenti di acquisto e vendita.

Se si desidera utilizzare questa scheda articolo come modello quando si creano nuove schede articolo, è possibile salvarla come modello. Per ulteriori informazioni, vedere la seguente sezione:

## <a name="to-save-the-item-card-as-a-template"></a>Per salvare la scheda articolo come modello
1. Nella finestra **Scheda articolo** scegliere l'azione **Salva come modello**. Nella finestra **Modello articolo** verrà visualizzata la scheda articolo come modello.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella finestra **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per l'articolo.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede articolo create utilizzando la definizione.
5. Una volta completato il nuovo modello articolo, scegliere **OK**.

Il modello articolo viene aggiunto all'elenco dei modelli articolo, in modo che sia possibile utilizzarlo per creare nuove schede articolo.

## <a name="see-also"></a>Vedi anche
  [Magazzino](inventory-manage-inventory.md)  
  [Acquisti](purchasing-manage-purchasing.md)  
  [Vendite](sales-manage-sales.md)  
  [Utilizzo di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
