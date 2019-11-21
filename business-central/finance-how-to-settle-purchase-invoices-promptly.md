---
title: Come saldare immediatamente le fatture di acquisto | Microsoft Docs
description: Se si deve pagare il fornitore in contanti o con assegno, è possibile effettuare la necessaria registrazione contemporaneamente a quella della fattura.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 7392ec07c59974869dce6c1e8172eb48701e1d26
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554016"
---
# <a name="settle-purchase-invoices-promptly"></a>Saldare immediatamente le fatture di acquisto
Se si deve pagare il fornitore in contanti o con assegno, è possibile registrare il pagamento mentre si registra la fattura.  

### <a name="to-settle-purchase-invoices-promptly"></a>Per saldare immediatamente le fatture di acquisto  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture di acquisto** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3.  Per pagare in contanti o tramite bonifico, immettere il numero del conto cassa di contabilità generale o il conto corrente bancario nel campo **Nr. contropartita**.  

> [!IMPORTANT]  
>  I campi **Tipo Contropartita** e **Contropartita** non sono inclusi nel layout standard della testata della fattura. Per registrare il pagamento di una fattura, è necessario immettere tali campi utilizzando le funzioni di progettazione.  

> [!NOTE]  
>  Se le fatture di acquisto sono spesso pagate in contanti, è una buona idea impostare un metodo di pagamento specifico con una contropartita e immetterlo nel campo **Metodo Pagamento** nella scheda del fornitore. Il numero della contropartita verrà immesso automaticamente nella testata della fattura ogni volta che ne verrà creata una nuova.  

## <a name="see-also"></a>Vedi anche  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
