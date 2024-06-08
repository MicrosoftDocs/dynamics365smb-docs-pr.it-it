---
title: Creare fatture per i pagamenti anticipati
description: Informazioni su come gestire situazioni in cui un pagamento anticipato viene richiesto da te o dal fornitore. Usa le percentuali predefinite per ogni riga di vendita o di acquisto oppure rettifica l'importo come necessario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 10/04/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
ms.service: dynamics-365-business-central
---
# <a name="create-prepayment-invoices"></a>Creare fatture per i pagamenti anticipati

Se è necessario che i clienti paghino prima della spedizione di un ordine, è possibile utilizzare le funzionalità di pagamento anticipato. Lo stesso vale se il fornitore richiede di pagare prima di spedire un ordine.  

È possibile creare un processo di pagamento anticipato quando si crea un ordine di vendita o di acquisto. La percentuale di pagamento anticipato predefinita per un articolo dell'ordine o per il cliente o il fornitore, verrà automaticamente inclusa nella fattura di pagamento anticipato. È inoltre possibile specificare una percentuale di pagamento anticipato per l'intero documento.

Dopo avere creato un ordine di vendita o di acquisto, è possibile creare una fattura pagamento anticipato. Usa le percentuali predefinite per ogni riga di vendita o di acquisto oppure rettifica l'importo. È ad esempio possibile specificare un importo totale per l'intero ordine.  

La procedura seguente descrive come fatturare un pagamento anticipato per un ordine di vendita. I passaggi sono simili per un ordine di acquisto.  

## <a name="to-create-a-prepayment-invoice"></a>Per creare una fattura di pagamento anticipato

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Creare un nuovo ordine di vendita per un cliente pertinente. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).  

    Nella scheda dettaglio **Pagamento anticipato** il campo **% pagamento anticipato** specifica la percentuale da utilizzare per calcolare l'importo del pagamento anticipato. Se nella scheda cliente è impostata una percentuale pagamento anticipato di default, il campo viene compilato automaticamente. È possibile modificare la percentuale. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Scegliere il campo **Comprimi pagamento anticipato** se si desidera creare righe nella fattura di pagamento anticipato che combinano righe dell'ordine cliente se:  

    - Le righe hanno lo stesso conto di contabilità generale per i pagamenti anticipati, come determinato in Setup registrazioni COGE.  
    - Le righe hanno le stesse dimensioni.  

    Se vuoi specificare una fattura pagamento anticipato con una riga per ogni riga dell'ordine di vendita associata a una percentuale pagamento anticipato, non scegliere il campo **Comprimi pagamento anticipato**.  

    La data di scadenza per il pagamento anticipato viene calcolata automaticamente in base al valore di **Cod. condizioni pagam. ant.**.

    > [!NOTE]
    > Quando alcune righe di una fattura richiedono il pagamento anticipato del 100% e altre righe no e sul conto di pagamento anticipato è presente l'IVA, l'importo arrotondato potrebbe causare un errore durante la creazione di una fattura di pagamento anticipato. L'errore si verifica perché l'importo della fattura di pagamento anticipato è superiore agli importi nelle righe del documento. Per risolvere il problema, modifica gli importi su una o tutte le righe che richiedono il pagamento anticipato del 100%. La modifica ricalcolerà l'arrotondamento dell'importo IVA e utilizzerà la differenza di arrotondamento accumulata nell'ultima riga modificata.
    >
    > Altri due modi per risolvere il problema sono:
    >
    > * Crea un gruppo di registrazione prodotto IVA separato e un'impostazione di registrazione IVA con un identificatore IVA separato e utilizzalo per gli articoli o le righe che richiedono il pagamento anticipato del 100%. L'arrotondamento viene eseguito per ciascun identificatore IVA, pertanto verrà eseguito un arrotondamento separato per gli articoli assegnati al gruppo di registrazione articoli/servizi IVA.
    > * Utilizza una fattura separata per gli articoli o le righe che richiedono e non richiedono pagamenti anticipati del 100%.

3. Compilare le righe di vendita.  

    Se è stata specificata una percentuale di pagamento anticipato predefinita per il cliente o nella scheda dettaglio **Pagamento anticipato** sul documento, questo valore viene copiato in ogni riga. È possibile modificare il contenuto del campo **% pagamento anticipato** nella riga.  

    > [!TIP]
    > Se il campo **% pagamento anticipato** non è visualizzato, è possibile aggiungerlo tramite personalizzazione.  Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

4. Per visualizzare l'importo del pagamento anticipato totale, scegliere l'azione **Statistiche**.

    Se si desidera rettificare l'importo del pagamento anticipato totale per l'ordine, è possibile modificare il contenuto del campo **Importo pagamento anticipato** nella pagina **Statistiche ordini vendita**.  

    Se il campo **Prezzi IVA inclusa** è selezionato, il campo **Importo pagam. ant. IVA incl.** è modificabile.  

    Se modifichi il contenuto del campo **Importo pagamento anticipato**, l'importo verrà distribuito proporzionalmente tra tutte le righe, ad eccezione di quelle in cui è presente il valore **0** nel campo **% pagamento anticipato**.  

5. Per stampare un report test prima di registrare una fattura pagamento anticipato, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Report test pagamento anticipato**.  
6. Per registrare la fattura pagamento anticipato, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato**.  

    Per registrare e stampare la fattura pagamento anticipato, scegliere l'azione **Registra e stampa fattura pagam. ant.**  

Puoi emettere altre fatture pagamento anticipato per l'ordine. A tale fine, aumenta l'importo pagamento anticipato in una o più righe, rettifica la data del documento, se necessario, e registra la fattura pagamento anticipato. Verrà creata una nuova fattura per la differenza tra gli importi pagamento anticipato fatturati fino a quel momento e il nuovo importo pagamento anticipato.  

> [!NOTE]  
> Se ci si trova in America del Nord, non è possibile modificare la percentuale di pagamento anticipato dopo che la fattura pagamento anticipato è stata registrata. Ciò è impedito nella versione nordamericana di [!INCLUDE[prod_short](includes/prod_short.md)] perché altrimenti il calcolo dell'imposta sulle vendite risulterebbe errato.  

 Quando sei pronto per registrare il resto della fattura, effettua la registrazione come con qualsiasi fattura. L'importo pagamento anticipato verrà automaticamente dedotto dall'importo dovuto.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Aggiornare automaticamente lo stato degli ordini con pagamento anticipato e delle fatture

È possibile velocizzare l'elaborazione di ordini e fatture impostando movimenti nella coda processi che aggiornano automaticamente lo stato di tali documenti. Quando viene pagata una fattura con pagamento anticipato, le voci della coda processi possono modificare automaticamente lo stato del documento da **In attesa di pagamento anticipato** a **Rilasciato**. Quando imposti le voci della coda processi, le codeunit che dovrai utilizzare sono **384 Aggiornamento pagamento anticipato vendita in sospeso** e **384 Aggiornamento pagamento anticipato acquisto in sospeso**. Ti consigliamo di pianificare l'esecuzione frequente delle voci, ad esempio ogni minuto. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Vedere anche

[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
