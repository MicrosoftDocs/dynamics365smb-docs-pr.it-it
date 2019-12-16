---
title: Impostare i metodi di pagamento| Documenti Microsoft
description: Utilizzare i metodi di pagamento, ad esempio, assegni, bonifici, contanti o PayPal, per definire le modalità di pagamento di fatture di vendita e di acquisto.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 753b9f30648059a68c22b524008e21c6c866d19c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882544"
---
# <a name="defining-payment-methods"></a>Definizione dei metodi di pagamento
I metodi di pagamento consentono di definire il modo in cui si desidera essere pagati dai clienti e quello in cui si intende pagare i fornitori. Il metodo può variare per ogni cliente o fornitore. Esempi di metodi di pagamento tipici sono **banca**, **contanti**, **assegno**, **conto**.

È possibile assegnare un metodo di pagamento a clienti e fornitori di modo che lo stesso metodo sia sempre utilizzato per i documenti di vendita e di acquisto create per essi. Se necessario, è possibile modificare il metodo nel documento di vendita o di acquisto. Ad esempio, se si desidera pagare una determinata fattura di acquisto in contanti anziché tramite assegno. Ciò non modifica il metodo di pagamento di default assegnato al fornitore.

Gli stessi metodi di pagamento sono utilizzati per documenti di vendita e di acquisto. Ad esempio, il metodo di pagamento _contanti_ viene utilizzato quando si effettuano e si ricevono pagamenti. [!INCLUDE[d365fin](includes/d365fin_md.md)] presuppone che quando si crea una fattura di vendita si prevede di ricevere un pagamento e il contrario per le fatture di acquisto.

Le note di credito per i resi, tuttavia, sono eccezioni in quanto il flusso di denaro avviene in direzioni opposte, dall'utente al cliente e dal venditore all'utente. Di conseguenza, il metodo di pagamento di default non è assegnato alle note di credito. Esiste, tuttavia, una soluzione alternativa se sono stati specificati i termini di pagamento per il cliente o il fornitore. Sebbene il campo **Calc. sc. pagam. su note credito** non sia destinato a questo scopo, se si sceglie la casella di controllo nella pagina **Condizioni pagamento** il metodo di pagamento di default verrà aggiunto quando si crea una nota di credito. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys]

## <a name="to-set-up-a-payment-method"></a>Per impostare un metodo di pagamento
[!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce alcuni metodi di pagamento utilizzati spesso dalle aziende. È tuttavia possibile aggiungere tutti quelli desiderati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Metodi di pagamento** e quindi scegliere il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Per assegnare un metodo di pagamento a un cliente o un fornitore
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cliente** o **Fornitore** e quindi scegliere il collegamento correlato.
2. Nel campo **Codice metodo di pagamento**, scegliere il metodo da utilizzare per impostazione predefinita per il cliente o il fornitore.

## <a name="see-also"></a>Vedere anche
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
