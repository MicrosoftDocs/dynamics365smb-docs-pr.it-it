---
title: Creare una scheda fornitore per registrare un nuovo fornitore (video)
description: In questo argomento viene illustrato come creare una scheda fornitore per registrare un nuovo fornitore e salvare la scheda fornitore come modello.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: cad131feb9232bbf476b7444ebeb2dd1b9170647
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953361"
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
Puoi aggiungere nuovi venditori manualmente, compilando i campi nella pagina **Scheda fornitore**, oppure puoi usare dei modelli che contengono informazioni predefinite. Per esempio, si può creare un modello per diversi tipi di profili di venditori. L'uso di modelli fa risparmiare tempo quando si aggiungono nuovi fornitori e aiuta a garantire che le informazioni siano corrette ogni volta. Se crei dei modelli per più di un tipo di venditore, puoi scegliere il modello da usare quando aggiungi un venditore. Se si crea un solo modello, questo verrà utilizzato per tutti i nuovi fornitori. Dopo aver creato un modello, è possibile utilizzare l'azione **Applica modello** per applicarlo a uno o più fornitori selezionati. Per creare un modello, si compilano le informazioni che si vogliono riutilizzare nella pagina della Vendor Card, e poi si salva come modello. Per maggiori informazioni, vedi [Salvare la pagina della scheda fornitore come modello](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Può essere utile personalizzare la pagina **Modello fornitore** quando si crea un modello. Per esempio, potresti voler aggiungere un campo che non è già visualizzato nella pagina. Per ulteriori informazioni, vedi [Personalizzare lo spazio di lavoro](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Puoi anche creare un fornitore da un contatto. Per ulteriori informazioni, vedere [Creare un cliente, un fornitore, un dipendente o un conto bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Per creare un nuovo fornitore

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Se non si è certi che verrà utilizzato l'indirizzo di fatturazione per tutte le fatture di un fornitore, non compilare il campo **Nr. fornitore**. Al contrario, scegliere il numero del pagamento al fornitore dopo avere impostato un'offerta in acquisto, un ordine o la testata di una fattura.

Il fornitore è ora registrato e la scheda fornitore è pronta per essere utilizzata nei documenti di acquisto.

Se si desidera utilizzare questa scheda fornitore come modello quando si creano nuove schede fornitore, è possibile salvarla come modello fornitore. Per ulteriori informazioni, vedi la sezione [Per salvare la scheda fornitore come modello](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Cancellazione e modifica delle informazioni del fornitore

Puoi modificare le informazioni sulle carte dei venditori in qualsiasi momento. Tuttavia, se hai inserito una transazione per un venditore, non puoi cancellare la carta perché le voci del libro mastro potrebbero essere necessarie per la revisione contabile. Per eliminare le schede fornitori con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.

> [!TIP]
> È possibile cambiare l'IBAN di un conto bancario di un venditore senza che il cambiamento influisca sulle voci storiche del registro dei bonifici. Le voci del registro dei bonifici memorizzano l'IBAN del destinatario, il numero del conto bancario del destinatario che sono stati specificati nei campi Conto bancario del venditore e Nome del destinatario dalla pagina della Carta del venditore quando le voci sono state create.


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