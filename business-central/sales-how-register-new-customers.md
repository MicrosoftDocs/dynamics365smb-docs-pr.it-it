---
title: Registrare nuovi clienti creando una scheda cliente
description: Descrive come creare una scheda cliente per registrare informazioni su ogni nuovo cliente a cui sono rivolte le vendite.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bb323a5cceb4988035d442d6bc8347125f927bf4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436753"
---
# <a name="register-new-customers"></a>Registrare nuovi clienti

I clienti sono l'origine del reddito. È necessario registrare ogni cliente, cui è stata effettuata una vendita, come una scheda cliente. Le schede cliente contengono le informazioni richieste per la vendita dei prodotti al cliente. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).  

Prima di registrare nuovi clienti, è necessario impostare vari codici di vendita selezionabili durante la compilazione delle schede cliente. Per ulteriori informazioni, vedere [Setup Vendite](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Aggiunta di nuovi clienti

Per registrare un nuovo cliente, è necessario compilare una scheda cliente. È possibile stabilire modelli per profili di clienti diversi oppure aggiungere clienti senza modelli. Puoi anche creare un cliente da un contatto. Per ulteriori informazioni, vedi [Per creare un contatto come cliente, fornitore, dipendente o conto corrente bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Se esistono i modelli cliente per diversi tipi di cliente, quando si crea una nuova scheda cliente, verrà visualizzata una pagina automaticamente da cui sarà possibile selezionare un modello appropriato. Se esiste solo un modello cliente, allora le nuove schede cliente utilizzeranno sempre tale modello.  

### <a name="to-create-a-new-customer-card"></a>Per creare una nuova scheda cliente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Clienti** scegliere l'azione **Nuovo**.

    Se esiste solo un modello cliente, allora verrà visualizzata una nuova scheda cliente con alcuni campi compilati con le informazioni derivanti dal modello.

    Se esistono più modelli cliente, verrà aperta una pagina nella quale sarà possibile selezionare un modello cliente. In questo caso, seguire i due passaggi successivi.
3. Nella pagina **Selezionare un modello per un nuovo cliente** scegliere il modello da utilizzare per la nuova scheda cliente.
4. Scegliere il pulsante **OK**. Una nuova scheda cliente verrà visualizzata con alcuni campi compilati con le informazioni del modello.  
5. Continuare a compilare o a modificare i campi della scheda cliente in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nella Scheda dettaglio **Prezzi vendita** è possibile visualizzare gli sconti o i prezzi speciali che si concedono al cliente se vengono soddisfatti determinati criteri come un articolo, la quantità minima di ordine o la data di scadenza. Ogni riga rappresenta un prezzo speciale o uno sconto riga. Ogni colonna rappresenta un criterio da applicare per garantire il prezzo speciale immesso nel campo **Prezzo unitario** o lo sconto riga immesso nel campo **Sconto riga**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).

Il cliente è ora registrato e la scheda cliente è pronta per essere utilizzata nei documenti di vendita.

Se si desidera utilizzare questa scheda cliente come modello quando si creano nuove schede cliente, è possibile salvarla come modello. Per ulteriori informazioni, vedere la seguente sezione:  

### <a name="to-save-the-customer-card-as-a-template"></a>Per salvare la scheda cliente come modello

1. Nella pagina **Scheda cliente** scegliere l'azione **Salva come modello**. Nella pagina **Modello cliente** verrà visualizzata la scheda cliente come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per il cliente.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede cliente create utilizzando la definizione.  
5. Una volta completato il nuovo modello cliente, fare clic su **OK**.

Il modello cliente viene aggiunto all'elenco dei modelli cliente, in modo che sia possibile utilizzarlo per creare nuove schede cliente.

## <a name="deleting-customer-cards"></a>Eliminazione di schede cliente

Se è stata registrata una transazione per un cliente, non è possibile eliminare la scheda perché i movimenti contabili potrebbero essere necessari per il controllo. Per eliminare le schede cliente con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.  

## <a name="managing-credit-limits"></a>Gestione dei limiti di credito

Limiti di credito, importi saldo e condizioni di pagamento consentono a [!INCLUDE [prod_short](includes/prod_short.md)] di visualizzare automaticamente un avviso relativo a credito e oltre fido quando viene immesso un ordine di vendita.  Le funzionalità relative a condizioni di sollecito e condizioni degli interessi finanziari permettono inoltre di fatturare interessi e/o oneri addizionali.  

Il campo **Limite credito** in una scheda cliente specifica l'importo massimo che si consente al cliente di superare rispetto al saldo pagamenti prima che vengano emessi degli avvisi. Quando si immettono quindi informazioni in registrazioni, offerte, ordini e fatture, [!INCLUDE [prod_short](includes/prod_short.md)] controlla la testata di vendita e le singole righe di vendita per verificare se il limite di credito è stato superato.

È possibile eseguire la registrazione anche se il limite di credito è stato superato. Se il campo rimane vuoto, non sarà presente alcun limite di credito per il cliente.  

È possibile scegliere di non ricevere avvisi che informano in merito al superamento del limite di credito di un cliente e specificare i tipi di avviso che si desidera visualizzare.

### <a name="to-specify-credit-limit-warnings"></a>Per specificare gli avvisi sui limiti di credito

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.

2. Sulla Scheda dettaglio **Generale**, nel campo **Avvisi credito** selezionare l'opzione pertinente come descritto nella tabella seguente:

    |Opzione| Descrizione|
    |------|------------|
    |**Entr. avvisi**| Entrambi i campi **Limite credito** e **Scaduto** nella scheda del cliente vengono controllati e viene visualizzato un avviso che informa se il cliente ha superato il proprio limite di credito o ha un oltre fido.|
    |**Limite credito**|Il valore contenuto nel campo **Limite credito** della scheda del cliente viene confrontato con il saldo del cliente e viene visualizzato un avviso che informa se il saldo del cliente supera questo importo.|
    |**Oltre Fido**|Il campo **Oltre fido** viene controllato e viene visualizzato un avviso che informa se il cliente ha un oltre fido.|
    |**Nessun Avviso**|Nessun avviso viene visualizzato sullo stato del cliente.|

## <a name="see-also"></a>Vedere anche

[Definizione dei metodi di pagamento](finance-payment-methods.md)  
[Unire record duplicati](sales-how-merge-duplicate-records.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
