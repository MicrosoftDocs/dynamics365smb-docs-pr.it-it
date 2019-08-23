---
title: Creare schede articolo per beni o servizi| Documenti Microsoft
description: Creare le schede articolo per i servizi che si vendono a ora e per i prodotti fisici, ad esempio articoli di assemblaggio, prodotti finiti, componenti o materie prime, che si vendono dal magazzino.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 06/20/2019
ms.author: sgroespe
ms.openlocfilehash: 854af39ef866d0d8959410c928acf65d65ffcb3d
ms.sourcegitcommit: acbbe80503e61296310ea7f787a9d7f4bc6dccd7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870548"
---
# <a name="register-new-items"></a>Registrare nuovi articoli
Gli articoli, tra gli altri prodotti, sono alla base dell'azienda, sono i beni o i servizi trattati. Ogni articolo deve essere registrato come scheda articolo.

Le schede articolo contengono le informazioni richieste per l'acquisto, l'archiviazione, la consegna e la contabilità degli articoli.

La scheda articolo può essere di tipo **Inventario**, **Assistenza** o **Non in inventario** per specificare se la scheda articolo rappresenta un'unità fisica di inventario, un'unità di misura del tempo della manodopera o un'unità fisica non registrata in magazzino Per ulteriori informazioni, vedere [Informazioni sui tipi di articolo](inventory-about-item-types.md).

È possibile che un articolo sia strutturato come articolo padre con elementi figlio sottostanti in una distinta base (BOM). In [!INCLUDE[d365fin](includes/d365fin_md.md)], una distinta base può essere una DB di assemblaggio o una DB di produzione, a seconda dell'utilizzo. Per altre informazioni, vedere [Utilizzare le distinte base](inventory-how-work-BOMs.md).

Se si acquista lo stesso articolo da più di un fornitore, è possibile collegare i fornitori alla scheda articolo. I fornitori vengono quindi visualizzati nella pagina **Catalogo art. fornitori** per poter selezionare facilmente un fornitore alternativo.

Gli articoli offerti ai clienti che non si desidera gestire nel sistema fino a quando non si inizia a venderli possono essere impostati come articoli di catalogo. Gli articoli di catalogo non devono essere confusi con articoli normali di tipo **Non in inventario**. Per ulteriori informazioni, vedere [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Se esistono i modelli articolo per diversi tipi di articolo, allora verrà visualizzata una pagina quando si crea una nuova scheda articolo da cui è possibile selezionare un modello appropriato. Se esiste solo un modello articolo, allora le nuove schede articolo utilizzeranno sempre tale modello.

La seguente procedura illustra come creare manualmente una scheda articolo da zero. È anche possibile creare nuove schede articolo copiando quelle esistenti. Per ulteriori informazioni, vedere [Copiare articoli esistenti per creare nuovi articoli](inventory-how-copy-items.md).

## <a name="to-create-a-new-item-card"></a>Per creare una nuova scheda articolo
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Articoli** scegliere l'azione **Nuovo**.

    Se esiste solo un modello articolo, allora verrà visualizzata una nuova scheda articolo con alcuni campi compilati con le informazioni derivanti dal modello.
3. Nella pagina **Selezionare un modello per un nuovo articolo** scegliere il modello da utilizzare per la nuova scheda articolo.
4. Scegliere il pulsante **OK**. Una nuova scheda articolo verrà visualizzata con alcuni campi compilati con le informazioni del modello.
5. Continuare a compilare o a modificare i campi della scheda articolo in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Nel campo **Metodo di costing** si imposta la modalità in cui viene calcolato il costo unitario dell'articolo tramite presupposizioni sul flusso degli articoli nell'azienda. Cinque metodi di costing sono disponibili, a seconda del tipo di articolo. Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md).
>
> Se si seleziona **Media**, il costo unitario di un articolo viene calcolato come il costo unitario medio in ogni momento dopo un acquisto. Il magazzino viene valutato presupponendo che tutte le giacenze siano vendute simultaneamente. Con questa impostazione, è possibile selezionare il campo **Costo unitario** nella pagina **Sintesi calc. costo medio** per visualizzare lo storico delle transazioni da cui viene calcolato il costo medio.

Nella Scheda dettaglio **Prezzo e registrazione** è possibile visualizzare gli sconti o i prezzi speciali che si concedono per l'articolo se vengono soddisfatti determinati criteri, come cliente, quantità minima di ordine o data di scadenza. Ogni riga rappresenta un prezzo speciale o uno sconto riga. Ogni colonna rappresenta un criterio da applicare per garantire il prezzo speciale immesso nel campo **Prezzo unitario** o lo sconto riga immesso nel campo **Sconto riga**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).

L'articolo è ora registrato e la scheda articolo è pronta per essere utilizzata nei documenti di acquisto e vendita.

Se si desidera utilizzare questa scheda articolo come modello quando si creano nuove schede articolo, è possibile salvarla come modello. Per ulteriori informazioni, vedere la seguente sezione:

## <a name="to-save-the-item-card-as-a-template"></a>Per salvare la scheda articolo come modello
1. Nella pagina **Scheda articolo** scegliere l'azione **Salva come modello**. Nella pagina **Modello articolo** verrà visualizzata la scheda articolo come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per l'articolo.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede articolo create utilizzando la definizione.
5. Una volta completato il nuovo modello articolo, scegliere **OK**.

Il modello articolo viene aggiunto all'elenco dei modelli articolo, in modo che sia possibile utilizzarlo per creare nuove schede articolo.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Per impostare più fornitori per un articolo  
Se si acquista lo stesso articolo da più di un fornitore, occorre immettere le informazioni relative a ogni singolo fornitore dell'articolo quali il prezzo, il lead time, lo sconto e così via.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2.  Selezionare il relativo articolo, quindi scegliere l'azione **Modifica**.  
3.  Scegliere l'azione **Fornitori**.  
4.  Selezionare il campo **Nr. fornitore** e selezionare il fornitore che si intende impostare per l'articolo.  
5.  Facoltativamente, compilare i campi restanti.  
6.  Ripetere i passaggi da 2 a 5 per ogni fornitore da cui si desidera acquistare l'articolo.

I fornitori vengono quindi visualizzati nella pagina **Catalogo art. fornitori** che si apre dalla scheda articolo per poter selezionare facilmente un fornitore alternativo.

## <a name="see-also"></a>Vedi anche
[Creazione di numerazioni](ui-create-number-series.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
