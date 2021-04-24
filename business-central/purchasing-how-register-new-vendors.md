---
title: Creare una scheda fornitore per registrare un nuovo fornitore | Documenti Microsoft
description: Informazioni su come creare una scheda fornitore per registrare un nuovo fornitore.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772656"
---
# <a name="register-new-vendors"></a>Registrare nuovi fornitori

I fornitori forniscono i prodotti venduti. Ogni fornitore da cui si acquista deve essere registrato come una scheda fornitore.

Prima di registrare nuovi fornitori, è necessario impostare vari codici di acquisto che sarà possibile selezionare durante la compilazione delle schede fornitore. Dopo la creazione di tutta l'anagrafica necessaria, è possibile eseguire ulteriori operazioni di configurazione del fornitore, ad esempio impostare il fornitore come prioritario per i pagamenti ed elencare gli articoli che tale fornitore e altri fornitori possono mettere a disposizione. Un altro gruppo di attività di impostazione dei fornitori è costituito dalla registrazione degli accordi relativi a sconti, prezzi e metodi di pagamento. Per ulteriori informazioni, vedere [Impostazioni acquisti](purchasing-setup-purchasing.md).

Le schede fornitore conservano le informazioni richieste per acquistare i prodotti presso i fornitori. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).

> [!NOTE]  
> Se esistono modelli fornitore per diversi tipi di fornitore, durante la creazione di una nuova scheda fornitore, verrà visualizzata una pagina nella quale sarà possibile selezionare un modello appropriato. Se esiste solo un modello fornitore, allora le nuove schede fornitore utilizzeranno sempre tale modello.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Aggiunta di nuovi fornitori

Per registrare un nuovo fornitore, è necessario compilare una scheda fornitore. È possibile stabilire modelli per profili di fornitore diversi oppure aggiungere fornitori senza modelli. Puoi anche creare un fornitore da un contatto. Per ulteriori informazioni, vedi [Per creare un contatto come cliente, fornitore, dipendente o conto corrente bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Se esistono modelli fornitore per diversi tipi di fornitore, durante la creazione di una nuova scheda fornitore, verrà visualizzata una pagina nella quale sarà possibile selezionare un modello appropriato. Se esiste solo un modello fornitore, allora le nuove schede fornitore utilizzeranno sempre tale modello.  

### <a name="to-create-a-new-vendor-card"></a>Per creare una nuova scheda fornitore

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Fornitori** selezionare **Nuovo**.

    Se esistono più modelli fornitore, verrà aperta una pagina nella quale sarà possibile selezionare un modello. In questo caso, seguire i due passaggi successivi.
    1. Nella pagina **Selezionare un modello per un nuovo fornitore** scegliere il modello da utilizzare per la nuova scheda fornitore.
    2. Scegliere il pulsante **OK**. Verrà visualizzata una nuova scheda fornitore con alcuni campi compilati con le informazioni del modello.
3. Continuare a compilare o a modificare i campi della scheda fornitore in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > Se non si è certi che verrà utilizzato l'indirizzo di fatturazione per tutte le fatture di un fornitore, non compilare il campo **Nr. fornitore**. Al contrario, scegliere il numero del pagamento al fornitore dopo avere impostato un'offerta in acquisto, un ordine o la testata di una fattura.

Il fornitore è ora registrato e la scheda fornitore è pronta per essere utilizzata nei documenti di acquisto.

Se si desidera utilizzare questa scheda fornitore come modello quando si creano nuove schede fornitore, è possibile salvarla come modello fornitore. Per ulteriori informazioni, vedi la sezione [Per salvare la scheda fornitore come modello](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-vendor-cards"></a>Eliminazione delle schede fornitori

Se è stata registrata una transazione per un fornitore, non è possibile eliminare la scheda perché i movimenti contabili potrebbero essere necessari per il controllo. Per eliminare le schede fornitori con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.

## <a name="to-save-the-vendor-card-as-a-template"></a>Per salvare la scheda fornitore come modello

1. Nella pagina **Scheda fornitore** scegliere l'azione **Salva come modello**. Nella pagina **Modello fornitore** verrà visualizzata la scheda fornitore come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per il fornitore.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede fornitore create utilizzando la definizione.
5. Una volta completato il nuovo modello fornitore, scegliere **OK**.  
   Il modello fornitore viene aggiunto all'elenco dei modelli fornitore, in modo che sia possibile utilizzarlo per creare nuove schede fornitore.

## <a name="see-also"></a>Vedere anche

[Unire record duplicati](sales-how-merge-duplicate-records.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]