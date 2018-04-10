---
title: Creare una scheda fornitore per registrare un nuovo fornitore | Documenti Microsoft
description: Informazioni su come creare una scheda fornitore per registrare un nuovo fornitore.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: d17ed41b7beb6ba342c17e007496314d9be743f0
ms.contentlocale: it-it
ms.lasthandoff: 03/28/2018

---
# <a name="register-new-vendors"></a>Registrare nuovi fornitori
I fornitori forniscono i prodotti venduti. Ogni fornitore da cui si acquista deve essere registrato come una scheda fornitore.

Prima di registrare nuovi fornitori, è necessario impostare vari codici di acquisto che sarà possibile selezionare durante la compilazione delle schede fornitore. Dopo la creazione di tutta l'anagrafica necessaria, è possibile eseguire ulteriori operazioni di configurazione del fornitore, ad esempio impostare il fornitore come prioritario per i pagamenti ed elencare gli articoli che tale fornitore e altri fornitori possono mettere a disposizione. Un altro gruppo di attività di impostazione dei fornitori è costituito dalla registrazione degli accordi relativi a sconti, prezzi e metodi di pagamento. Per ulteriori informazioni, vedere [Impostazioni acquisti](purchasing-setup-purchasing.md).

Le schede fornitore conservano le informazioni richieste per acquistare i prodotti presso i fornitori. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).

> [!NOTE]  
>   Se esistono modelli fornitore per diversi tipi di fornitore, durante la creazione di una nuova scheda fornitore, verrà visualizzata una finestra nella quale sarà possibile selezionare un modello appropriato. Se esiste solo un modello fornitore, allora le nuove schede fornitore utilizzeranno sempre tale modello.

## <a name="to-create-a-new-vendor-card"></a>Per creare una nuova scheda fornitore
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fornitori**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Fornitori** scegliere **Nuovo**.

    Se esistono più modelli fornitore, verrà aperta una finestra nella quale sarà possibile selezionare un modello. In questo caso, seguire i due passaggi successivi.
3. Nella finestra **Selezionare un modello per un nuovo fornitore** scegliere il modello da utilizzare per la nuova scheda fornitore.
4. Scegliere il pulsante **OK**. Verrà visualizzata una nuova scheda fornitore con alcuni campi compilati con le informazioni del modello.
5. Continuare a compilare o a modificare i campi della scheda fornitore in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Se non si è certi che verrà utilizzato l'indirizzo di fatturazione per tutte le fatture di un fornitore, non compilare il campo **Pagare a**. Al contrario, scegliere il numero del pagamento al fornitore dopo avere impostato un'offerta in acquisto, un ordine o la testata di una fattura.

Il fornitore è ora registrato e la scheda fornitore è pronta per essere utilizzata nei documenti di acquisto.

Se si desidera utilizzare questa scheda fornitore come modello quando si creano nuove schede fornitore, è possibile salvarla come modello fornitore. Per ulteriori informazioni, vedere la seguente sezione:

## <a name="to-save-the-vendor-card-as-a-template"></a>Per salvare la scheda fornitore come modello
1. Nella finestra **Scheda fornitore** scegliere l'azione **Salva come modello**. Nella finestra **Modello fornitore** verrà visualizzata la scheda fornitore come modello.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Verrà visualizzata la finestra **Modelli dimensioni** nella quale saranno indicati tutti i codici per le dimensioni che sono impostati per il fornitore.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede fornitore create utilizzando la definizione.
5. Una volta completato il nuovo modello fornitore, scegliere **OK**.  
   Il modello fornitore viene aggiunto all'elenco dei modelli fornitore, in modo che sia possibile utilizzarlo per creare nuove schede fornitore.

## <a name="see-also"></a>Vedi anche
[Creazione di numerazioni](ui-create-number-series.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)   
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

