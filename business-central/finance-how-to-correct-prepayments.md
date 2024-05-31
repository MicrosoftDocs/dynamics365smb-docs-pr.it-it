---
title: Rettificare i pagamenti anticipati
description: È possibile correggere un ordine dopo aver registrato una fattura di pagamento anticipato per l'ordine e aggiungere nuove righe a un ordine dopo aver emesso un pagamento anticipato.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '44, 48, 42, 50, 52, 9305, 9307'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rettificare i pagamenti anticipati

È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso. È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato.  

> [!TIP]
> Se è stata registrata una fattura di pagamento anticipato per una fattura di vendita che si corregge o si annulla, è necessario correggere o annullare anche il pagamento anticipato.

## Per rettificare un pagamento anticipato

La procedura seguente illustra come emettere una nota di credito di pagamento anticipato per annullare tutti i pagamenti anticipati fatturati per un ordine di vendita.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di vendita appropriato.
3. Scegliere l'azione **Pagamento anticipato**, quindi scegliere l'azione **Registra nota credito pagamento anticipato** o l'azione **Registra e stampa nota cr. pagam. ant.**  
4. Nella pagina **Nota credito vendita** rettificare i movimenti desiderati, come per qualsiasi nota di credito vendita. Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Per ridurre l'importo nel campo **Importo riga**, è necessario prima aumentare la percentuale pagamento anticipato nella riga in modo che il valore nel campo **Importo riga pagam. ant.** non scenda sotto il valore del campo **Fattura importo pagam. ant.**.

5. Per creare una fattura pagamento anticipato per le nuove righe nota di credito di vendita,, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato** o l'azione **Registra e stampa fattura pagam. ant.**.  
6. Per emettere una fattura pagamento anticipato aggiuntiva, aumentare l'importo pagamento anticipato in una o più righe e registrare la fattura pagamento anticipato. Verrà creata una nuova fattura per la differenza tra gli importi di pagamenti anticipati fatturati e i nuovi importi di pagamenti anticipati.  

## Vedere anche

[Fatturazione dei pagamenti anticipati](finance-invoice-prepayments.md)  
[Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
