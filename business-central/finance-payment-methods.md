---
title: Impostare i metodi di pagamento (video)
description: 'Utilizzare i metodi di pagamento, ad esempio, assegni, bonifici, contanti o PayPal, per definire le modalità di pagamento di fatture di vendita e di acquisto.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.search.form: 427
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-payment-methods" />Impostare i metodi di pagamento

I metodi di pagamento consentono di definire il modo in cui si desidera essere pagati dai clienti e quello in cui si intende pagare i fornitori. Il metodo può variare per ogni cliente o fornitore. Esempi di metodi di pagamento tipici sono **banca**, **contanti**, **assegno**, **conto**.

È possibile assegnare un metodo di pagamento a clienti e fornitori di modo che lo stesso metodo sia sempre utilizzato per i documenti di vendita e di acquisto create per essi. Se necessario, è possibile modificare il metodo nel documento di vendita o di acquisto. Ad esempio, se si desidera pagare una determinata fattura di acquisto in contanti anziché tramite assegno. Ciò non modifica il metodo di pagamento di default assegnato al fornitore.

Gli stessi metodi di pagamento sono utilizzati per documenti di vendita e di acquisto. Ad esempio, il metodo di pagamento _contanti_ viene utilizzato quando si effettuano e si ricevono pagamenti. [!INCLUDE[prod_short](includes/prod_short.md)] presuppone che quando si crea una fattura di vendita si prevede di ricevere un pagamento e il contrario per le fatture di acquisto.

Le note di credito per i resi, tuttavia, sono eccezioni in quanto il flusso di denaro avviene in direzioni opposte, dall'utente al cliente e dal venditore all'utente. Di conseguenza, il metodo di pagamento di default non è assegnato alle note di credito. Esiste, tuttavia, una soluzione alternativa se sono stati specificati i termini di pagamento per il cliente o il fornitore. Sebbene il campo **Calc. sc. pagam. su note credito** non sia destinato a questo scopo, se si sceglie la casella di controllo nella pagina **Condizioni pagamento** il metodo di pagamento di default verrà aggiunto quando si crea una nota di credito. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method" />Per impostare un metodo di pagamento

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce alcuni metodi di pagamento utilizzati spesso dalle aziende. Puoi tuttavia aggiungere tutti quelli desiderati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Metodi di pagamento**, quindi scegli il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Facoltativamente, aggiungi condizioni pagamento al metodo di pagamento. Per ulteriori informazioni, vedi [Impostare le condizioni pagamento](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor" />Per assegnare un metodo di pagamento a un cliente o un fornitore

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cliente** o **Fornitore**, quindi scegli il collegamento correlato.
2. Nel campo **Codice metodo di pagamento**, scegliere il metodo da utilizzare per impostazione predefinita per il cliente o il fornitore.

## <a name="see-related-microsoft-trainingtrainingmodulescash-management-dynamics--business-central" />Vedi il relativo [training Microsoft](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Impostare le condizioni pagamento](finance-payment-terms.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
