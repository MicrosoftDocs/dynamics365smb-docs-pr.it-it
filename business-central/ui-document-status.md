---
title: Campo stato nei documenti
description: 'Ulteriori informazioni sullo stato "Aperto" e "Rilasciato" su offerte, ordini o documenti di nota di credito.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents"></a>Campo stato nei documenti

Quando crei un'offerta, un ordine o una nota di credito, il campo **Stato** nella testata del documento contiene l'opzione predefinita **Aperto**.

Dopo aver compilato il documento, puoi rilasciarlo e [!INCLUDE[prod_short](includes/prod_short.md)] cambia il valore nel campo **Stato** in **Rilasciato**. Questo stato indica che l'ordine è pronto per la fase di elaborazione successiva prima che venga registrato.

| Stato | Descrizione |
| ------ | ----------- |
| Apri   | È possibile apportare modifiche al documento. |
| Rilasciato | Il documento è stato rilasciato per la fase di elaborazione successiva e non è possibile apportare modifiche alle righe di tipo *Articolo* e *Cespite*.<br /><br />È possibile riaprire un documento rilasciato se si desidera modificarlo. Per portare il documento corretto alla fase di elaborazione successiva, è necessario rilasciarlo nuovamente. |
| Approvazione in sospeso   | Il documento è in attesa di approvazione. |
| Pagamento anticipato in sospeso | Una fattura pagamento anticipato è stata registrata per il documento. |

## <a name="release-process"></a>Rilascia processo

Il processo di rilascio può essere utilizzato in diversi modi per semplificare il workflow standard, ad esempio, per seguire le procedure utilizzate dall'azienda in relazione alle approvazioni per avviare le attività della warehouse.

### <a name="approval-procedures"></a>Procedure di approvazione

L'azienda può utilizzare la procedura di rilascio per indicare che un altro utente ha approvato il documento oppure che un contatto esterno può soddisfare le specifiche indicate del documento, come indicato negli esempi illustrati di seguito.

* È possibile rilasciare un ordine di acquisto quando il fornitore ha indicato di essere pronto a fornire l'ordine.
* L'utente crea un ordine e un secondo utente deve approvarlo, per ragioni di sicurezza, prima che l'utente stesso possa rilasciarlo.
* Una nota di credito creata dall'utente deve essere rilasciata dal responsabile dell'approvazione di tutti i rimborsi.

Ulteriori informazioni sui flussi di lavoro di approvazione in [Usare i flussi di lavoro](across-use-workflows.md).

### <a name="warehouse-activities"></a>Attività di warehouse

Se lo stato dell'ordine è **Aperto**, nel deposito non si comincerà a preparare la spedizione, perché non si prevede di ricevere gli articoli di un ordine di acquisto. Quando l'ordine viene rilasciato, si indica che è completo e la warehouse può inserirlo nelle sue attività.

## <a name="reopen-a-released-order"></a>Riaprire un ordine rilasciato

Se un ordine è stato rilasciato è possibile apportarvi delle modifiche riaprendolo. L'unica modifica possibile tuttavia alle righe già elaborate nella warehouse è l'incremento della quantità.

Dopo aver apportato le modifiche e aver rilasciato l'ordine di nuovo, [!INCLUDE [prod_short](includes/prod_short.md)] ricalcola l'IVA e lo sconto fattura.

Se si apportano modifiche ad un ordine rilasciato, è necessario comunicare alla warehouse le modifiche apportate.

> [!NOTE]
> Se si intende registrare un singolo ordine aperto o una nota di credito senza aver rilasciato in precedenza i rispettivi documenti, [!INCLUDE [prod_short](includes/prod_short.md)] rilascerà automaticamente il documento quando questo viene registrato. Se gli ordini o le note di credito vengono registrati utilizzando la funzione **Registra batch**, puoi registrare soltanto gli ordini o le note di credito che sono stati rilasciati.

## <a name="see-also"></a>Vedere anche

[Vendere prodotti con un ordine di vendita al cliente](sales-how-sell-products.md)  
[Registrare gli acquisti con le fatture d'acquisto](purchasing-how-record-purchases.md)  
[Spedire articoli](warehouse-how-ship-items.md)  
[Ricevere articoli](warehouse-how-receive-items.md)  
[Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md)  
[Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md)  
[Archiviare documenti](across-how-to-archive-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
