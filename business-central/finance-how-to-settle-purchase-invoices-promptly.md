---
title: Saldare immediatamente le fatture di acquisto
description: Se si deve pagare il fornitore in contanti o con assegno, è possibile effettuare la necessaria registrazione contemporaneamente a quella della fattura.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: bac023393d95623a2731ef1b2ada7d30b135063b
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968361"
---
# <a name="settle-purchase-invoices-promptly"></a>Saldare immediatamente le fatture di acquisto

Se si deve pagare il fornitore in contanti o con assegno, è possibile registrare il pagamento mentre si registra la fattura.  

> [!NOTE]  
> Se le fatture di acquisto sono spesso pagate in contanti, in assegni o con bonifico è una buona idea impostare un metodo di pagamento specifico con una contropartita e immetterlo nel campo **Metodo Pagamento** nella scheda del fornitore. Il numero della contropartita verrà immesso automaticamente nella testata della fattura ogni volta che ne verrà creata una nuova. Per ulteriori informazioni, vedere [Definizione dei metodi di pagamento](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>Per saldare immediatamente le fatture di acquisto

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Per pagare in contanti o tramite bonifico, immettere il numero del conto cassa di contabilità generale o il conto corrente bancario nel campo **Nr. contropartita**.  

> [!IMPORTANT]  
> I campi **Tipo Contropartita** e **Contropartita** non sono inclusi nel layout standard della testata della fattura. Per registrare il pagamento di una fattura è necessario contattare un partner Microsoft che può aggiungere i campi tramite codice.  
>
> Questa personalizzazione è richiesta solo se non si specificano conti di contropartita per i metodi di pagamento come descritto sopra.

## <a name="see-also"></a>Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
