---
title: Creare una scheda fornitore per registrare un nuovo fornitore (video)
description: Scopri come creare una scheda fornitore per registrare un nuovo fornitore e salvare la scheda fornitore come modello.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: '26, 27, 34, 461, 786, 1379, 1385, 1386, 1628'
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="register-new-vendors" />Registrare nuovi fornitori

I fornitori forniscono i prodotti venduti. Ogni fornitore da cui si acquista deve essere registrato come una scheda fornitore.

Prima di registrare nuovi fornitori, è necessario impostare vari codici di acquisto che sarà possibile selezionare durante la compilazione delle schede fornitore. Dopo la creazione di tutta l'anagrafica necessaria, è possibile aggiungere caratteristiche univoche per un fornitore, ad esempio impostare il fornitore come prioritario per i pagamenti ed elencare gli articoli che tale fornitore e altri fornitori possono mettere a disposizione. Un altro gruppo di attività di impostazione dei fornitori è costituito dalla registrazione degli accordi relativi a sconti, prezzi e metodi di pagamento. Ulteriori informazioni in [Impostazioni acquisti](purchasing-setup-purchasing.md).

Le schede fornitore conservano le informazioni richieste per acquistare i prodotti da ciascun fornitore. Ulteriori informazioni in [Registrare gli acquisti](purchasing-how-record-purchases.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).
<br /><br />  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors" />Aggiunta di nuovi fornitori

Puoi aggiungere nuovi venditori manualmente, compilando nella pagina **Scheda fornitore**, oppure puoi usare dei modelli che contengono informazioni predefinite. Per esempio, si può creare un modello per diversi tipi di profili di venditori. L'uso di modelli fa risparmiare tempo quando si aggiungono nuovi fornitori e aiuta a garantire che le informazioni siano corrette ogni volta.

> [!NOTE]  
> Se esistono modelli fornitore per diversi tipi di fornitore, all'inizio della creazione di una nuova scheda fornitore, verrà visualizzata una pagina nella quale sarà possibile selezionare un modello appropriato. Se esiste solo un modello fornitore, allora le nuove schede fornitore utilizzeranno sempre tale modello.

Dopo aver creato un modello, è possibile utilizzare l'azione **Applica modello** per applicarlo a uno o più fornitori selezionati. Per creare un modello, si compilano le informazioni che si vogliono riutilizzare nella pagina della **Scheda fornitore**, e poi si salva come modello. Ulteriori informazioni nella sezione [Salvare la pagina della scheda fornitore come modello](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Può essere utile personalizzare la pagina **Modello fornitore** quando si crea un modello. Per esempio, potresti voler aggiungere un campo che non è già visualizzato nella pagina. Ulteriori informazioni nella sezione [Personalizza l'area di lavoro](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Puoi anche creare un fornitore da un contatto. Ulteriori informazioni nella sezione [Creare un cliente, un fornitore, un dipendente o un conto bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

Gli indirizzi di rimessa vengono utilizzati quando si stampano assegni per pagare i fornitori e i fornitori possono avere più indirizzi di rimessa per i pagamenti. Ad esempio, un fornitore potrebbe fornire un articolo da una società sussidiaria, ma desidera ricevere il pagamento presso la propria sede. [!INCLUDE [prod_short](includes/prod_short.md)] ti consente di impostare più indirizzi postali per ciascun fornitore e puoi scegliere la posizione corretta a cui inviare i pagamenti fattura per fattura.

Specifica gli indirizzi di rimessa nelle pagine della scheda fornitore e nella scheda dettaglio Spedizioni e pagamenti su ordini di acquisto e fatture. Quando crei le righe di registrazione pagamenti utilizzando le azioni Pagamento fornitore o Crea pagamento nella pagina Elenco fornitori o Scheda fornitore o l'azione Applica movimenti su un giornale di registrazione pagamenti, viene assegnato il codice di rimessa sul movimento contabile fornitore. È possibile sostituire questo valore.

### <a name="to-create-a-new-vendor" />Per creare un nuovo fornitore

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Se non conosci l'indirizzo di fatturazione che verrà utilizzato per ogni fattura di un fornitore, non compilare il campo **Nr.** nella Scheda dettaglio **Generale**. Al contrario, scegliere il numero del pagamento al fornitore dopo avere impostato un'offerta in acquisto, un ordine o la testata di una fattura.

Il fornitore è ora registrato e la scheda fornitore è pronta per essere utilizzata nei documenti di acquisto.

Se si desidera utilizzare questa scheda fornitore come modello quando si creano nuove schede fornitore, è possibile salvarla come modello fornitore. Ulteriori informazioni nella sezione [Per salvare la scheda fornitore come modello](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information" />Cancellazione e modifica delle informazioni del fornitore

Puoi modificare le informazioni sulle carte dei venditori in qualsiasi momento. Tuttavia, se hai inserito una transazione per un venditore, non puoi cancellare la carta perché le voci del libro mastro potrebbero essere necessarie per la revisione contabile. Per eliminare le schede fornitori con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.

> [!TIP]
> È possibile cambiare l'IBAN di un conto bancario di un venditore senza che il cambiamento influisca sulle voci storiche del registro dei bonifici. Le voci del registro dei bonifici memorizzano l'*IBAN del destinatario*, il *Numero del conto bancario del destinatario* che sono stati specificati nei campi **Conto bancario del venditore** e **Nome del destinatario** dalla pagina della **Scheda fornitore** quando le voci sono state create.

> [!TIP]
> Puoi aggiungere indirizzi alternativi sulle schede fornitore scegliendo l'azione **Indirizzi ordine**.

## <a name="to-save-the-vendor-card-as-a-template" />Per salvare la scheda fornitore come modello

1. Nella pagina **Scheda fornitore** scegliere l'azione **Salva come modello**. Nella pagina **Modello fornitore** verrà visualizzata la scheda fornitore come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per il fornitore.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede fornitore create utilizzando la definizione.
5. Una volta completato il nuovo modello fornitore, scegli **OK**.  
   Il modello fornitore viene aggiunto all'elenco dei modelli fornitore, in modo che sia possibile utilizzarlo per creare nuove schede fornitore.

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics--business-central" />Vedi il relativo [training Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/).

## <a name="see-also" />Vedere anche

[Unire record duplicati](sales-how-merge-duplicate-records.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Impostare i conti correnti fornitori](purchasing-how-set-up-vendors-bank-accounts.md)  
[Impostare gli addetti agli acquisti](purchasing-how-setup-purchasers.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Utilizzare le mappe online per trovare posizioni e indicazioni stradali](across-online-maps.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
