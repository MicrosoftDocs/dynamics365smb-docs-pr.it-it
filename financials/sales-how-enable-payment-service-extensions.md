---
title: Abilitare i pagamenti clienti tramite i servizi di pagamento| Documenti Microsoft
description: Facilitare ai clienti il pagamento delle fatture abilitando i servizi di pagamento.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c149949b939a551a14236c84f8ba7538fcb54bbe
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a>Procedura: Abilitare i pagamenti clienti tramite i servizi di pagamento
Come alternativa alla riscossione dei pagamenti tramite bonifico o carte di credito, i clienti possono pagare utilizzando il conto personale e servizi di pagamento, quali Microsoft Pay, PayPal o WorldPay.  

Dopo che viene abilitato un servizio di pagamento in [!INCLUDE[d365fin](includes/d365fin_md.md)], un collegamento all'assistenza è disponibile nei documenti di vendita inviati tramite e-mail ai clienti. I clienti possono utilizzare il collegamento per andare al servizio di pagamento e per pagare la fattura, direttamente dal documento di vendita. Se non si desidera includere il collegamento, ad esempio, se un cliente pagherà in contanti, è possibile rimuovere il servizio di pagamento dalla fattura prima della registrazione.  

Le estensioni Microsoft Pay, PayPal Payments Standard e WorldPay Payments Standard vengono installate in [!INCLUDE[d365fin](includes/d365fin_md.md)] e sono pronte per essere abilitate.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Per abilitare un servizio di pagamento in [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Servizi di pagamento**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Servizi di pagamento** scegliere l'azione **Nuovo**.  
3. Selezionare il servizio di pagamento e chiudere la finestra.  
4. Nella finestra **Servizi di pagamento** scegliere l'azione **Setup**.  
5. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Chiudere la finestra.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Per selezionare un servizio di pagamento di una fattura di vendita
1. Nella home page scegliere **Fatture vendite**.  
2. Aprire una fattura di vendita che si desidera pagare utilizzando il servizio di pagamento.  
3. Nel campo **Servizio di pagamento** scegliere il servizio di pagamento.  

    > [!NOTE]  
>   Il campo **Servizio di pagamento** è disponibile solo se è stato abilitato il servizio di pagamento.  

## <a name="see-also"></a>Vedi anche  
[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

