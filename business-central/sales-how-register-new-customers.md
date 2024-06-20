---
title: Registrare nuovi clienti creando una scheda cliente (contiene video)
description: Descrive come creare una scheda cliente per registrare informazioni su ogni nuovo cliente a cui sono rivolte le vendite.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 02/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="register-new-customers"></a>Registrazione di nuovi clienti

I clienti sono l'origine del reddito. È necessario registrare ogni cliente, cui è stata effettuata una vendita, come una scheda cliente. Le schede cliente contengono le informazioni richieste per la vendita dei prodotti al cliente. Ulteriori informazioni in [Fatturare le vendite](sales-how-invoice-sales.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).  

Prima di registrare nuovi clienti, è necessario impostare vari codici di vendita selezionabili durante la compilazione delle schede cliente. Ulteriori informazioni in [Setup vendite](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="add-new-customers"></a>Aggiungere nuovi clienti

Puoi aggiungere nuovi clienti manualmente, compilando la pagina della **Scheda cliente**, oppure puoi usare dei modelli che contengono informazioni predefinite. Per esempio, è possibile creare un modello per diversi tipi di profili di clienti. L'uso di modelli fa risparmiare tempo quando si aggiungono nuovi clienti e aiuta a garantire che le informazioni siano corrette ogni volta. 

Se crei:
* Più modelli per l'uso con più di un tipo di cliente, è possibile scegliere il modello da utilizzare quando si aggiunge un cliente.
* Viene usato un solo modello per tutti i nuovi clienti. 

Dopo aver creato un modello, è possibile utilizzare l'azione **Applica modello** per applicarlo a uno o più clienti selezionati. Per creare un modello, compila le informazioni che si vogliono riutilizzare nella pagina della **Scheda cliente**, e poi si salva come modello. Ulteriori informazioni nella sezione [Per salvare la scheda cliente come modello](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template)

> [!TIP]
> Può essere utile personalizzare la pagina **Modello cliente** quando si crea un modello. Per esempio, si potrebbe voler aggiungere il campo **Limite di credito** a un modello. Ulteriori informazioni nella sezione [Personalizza l'area di lavoro](/dynamics365/business-central/ui-personalization-user#start-personalizing-by-using-the-personalization-mode).

Puoi anche creare un cliente da un contatto. Ulteriori informazioni nella sezione [Creare un cliente, un fornitore, un dipendente o un conto bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card"></a>Per creare una nuova scheda cliente

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

L'azione **Prezzi e sconti** fornisce opzioni per la gestione di prezzi speciali o sconti per il cliente quando un ordine soddisfa determinati criteri. Quando si acquista un determinato articolo, l'ordine di una quantità minima o l'acquisto prima di una data, ad esempio alla fine di una campagna, sono esempi di tali criteri. Ulteriori informazioni in [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md)

Il cliente è ora registrato e la scheda cliente è pronta per essere utilizzata nei documenti di vendita.  

### <a name="to-save-the-customer-card-as-a-template"></a>Per salvare la scheda cliente come modello

Puoi utilizzare questa scheda cliente come modello quando si creano nuove schede cliente.

1. Nella pagina **Scheda cliente** scegliere l'azione **Salva come modello**. Nella pagina **Modello cliente** verrà visualizzata la scheda cliente come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per il cliente.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede cliente create utilizzando questo modello.  
5. Una volta completato il nuovo modello cliente, scegli **OK**.

Il modello cliente viene aggiunto all'elenco dei modelli cliente, in modo che sia possibile utilizzarlo per creare nuove schede cliente.

## <a name="delete-customer-cards"></a>Eliminare schede cliente

Se registri una transazione per un cliente, non puoi eliminare la scheda cliente perché i movimenti contabili potrebbero essere necessari per il controllo. Per eliminare le schede cliente con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.  

## <a name="manage-credit-limits"></a>Gestire limiti di credito

Limiti di credito, importi saldo e condizioni di pagamento consentono a [!INCLUDE [prod_short](includes/prod_short.md)] di visualizzare automaticamente un avviso relativo a credito e oltre fido quando viene immesso un ordine di vendita. Inoltre, il termine di sollecito e gli elementi della condizione di interessi finanziari ti consentono di fatturare interessi e/o oneri addizionali.  

Il campo **Limite credito** in una scheda cliente specifica l'importo massimo che si consente al cliente di superare rispetto al saldo pagamenti prima che vengano emessi degli avvisi. Quando si immettono informazioni in registrazioni, offerte, ordini e fatture, [!INCLUDE [prod_short](includes/prod_short.md)] verifica l'intestazione di vendita e le singole righe di vendita per determinare se il limite di credito viene superato.

È possibile eseguire la registrazione anche se il limite di credito è stato superato. Un campo vuoto significa che non sarà presente alcun limite di credito per il cliente.  

È possibile scegliere di non ricevere avvisi quando il limite di credito di un cliente viene superato e specificare i tipi di avviso che si desidera visualizzare.

### <a name="to-specify-credit-limit-warnings"></a>Per specificare gli avvisi sui limiti di credito

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.

2. Sulla Scheda dettaglio **Generale**, nel campo **Avvisi credito** selezionare l'opzione pertinente come descritto nella tabella seguente:

    |Opzione| Descrizione|
    |------|------------|
    |**Entr. avvisi**| Entrambi i campi **Limite credito** e **Scaduto** nella scheda del cliente vengono controllati e viene visualizzato un avviso che informa se il cliente supera il proprio limite di credito o ha un oltre fido.|
    |**Limite credito**|Il valore contenuto nel campo **Limite credito** della scheda del cliente viene confrontato con il saldo del cliente e viene visualizzato un avviso che informa se il saldo del cliente supera questo importo.|
    |**Oltre Fido**|Il campo **Oltre fido** viene controllato e viene visualizzato un avviso che informa se il cliente ha un oltre fido.|
    |**Nessun Avviso**|Nessun avviso di credito viene visualizzato sullo stato del cliente.|

## <a name="assign-a-salesperson"></a>Assegnare un agente

Puoi assegnare agenti all'indirizzo di spedizione del cliente anziché al suo indirizzo di fatturazione in modo che i report sulle vendite riflettano la reale distribuzione geografica delle tue vendite. L'assegnazione di un agente all'indirizzo di spedizione di un cliente fornisce informazioni più precise e ottimizza l'allocazione delle risorse.

Assegna un agente nella pagina scheda **Cliente** scegliendo **Cliente**, quindi **Spedire a - Indirizzi** per aprire la pagina **Spedire a - Lista indirizzi**. Scegli **Gestisci**, quindi **Modifica** per aprire la pagina scheda **Spedire a - Indirizzi**. Immetti o scegli un **Codice agente** per selezionare l'agente.

Quando scegli l'opzione **Indirizzo di spedizione alternativo** come ubicazione **Spedire a** in un documento di vendita, il **Codice agente** viene aggiornato per trovare la corrispondenza con l'agente nell'**indirizzo di spedizione** piuttosto che nell'**indirizzo di fatturazione**. 

## <a name="see-also"></a>Vedere anche

[Definizione dei metodi di pagamento](finance-payment-methods.md)  
[Unire record duplicati](sales-how-merge-duplicate-records.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Abilitare spedizioni parziali con avviso di spedizione](sales-how-send-partial-shipments.md)  
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Utilizzare le mappe online per trovare posizioni e indicazioni stradali](across-online-maps.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
