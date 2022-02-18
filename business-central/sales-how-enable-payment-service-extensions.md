---
title: Abilitare i pagamenti clienti con i servizi di pagamento
description: Facilita ai clienti il pagamento delle fatture abilitando i pagamenti clienti tramite i servizi di pagamento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.search.forms: 1060, 1061, 1062
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 8216c4f34cf63b1dcc9a501747ae8738309ba511
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059858"
---
# <a name="enable-customer-payments-through-payment-services"></a>Abilitare i pagamenti clienti tramite i servizi di pagamento
Come alternativa alla riscossione dei pagamenti tramite bonifico o carte di credito, i clienti possono pagare utilizzando il conto personale e servizi di pagamento, quali PayPal o WorldPay.  

Dopo che viene abilitato un servizio di pagamento in [!INCLUDE[prod_short](includes/prod_short.md)], un collegamento all'assistenza è disponibile nei documenti di vendita inviati tramite e-mail ai clienti. I clienti possono utilizzare il collegamento per andare al servizio di pagamento e per pagare la fattura, direttamente dal documento di vendita. Se non si desidera includere il collegamento, ad esempio, se un cliente pagherà in contanti, è possibile rimuovere il servizio di pagamento dalla fattura prima della registrazione.  

Le estensioni PayPal Payments Standard e WorldPay Payments Standard sono installate in [!INCLUDE[prod_short](includes/prod_short.md)] e pronte per essere abilitate.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Per abilitare un servizio di pagamento in [!INCLUDE[prod_short](includes/prod_short.md)]
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Servizi di pagamento**, quindi scegli il collegamento correlato.  
2. Nella pagina **Servizi di pagamento** scegliere l'azione **Nuovo**.  
3. Selezionare il servizio di pagamento e chiudere la pagina.  
4. Nella pagina **Servizi di pagamento** scegliere l'azione **Setup**.  
5. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Chiudere la pagina.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Per selezionare un servizio di pagamento di una fattura di vendita
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.  
2. Aprire una fattura di vendita che si desidera pagare utilizzando il servizio di pagamento.  
3. Nel campo **Servizio di pagamento** scegliere il servizio di pagamento.  

    > [!NOTE]  
    > Il campo **Servizio di pagamento** è disponibile solo se è stato abilitato il servizio di pagamento.  

## <a name="see-also"></a>Vedi anche  
[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]