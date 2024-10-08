---
title: Utilizzo dell'estensione PayPal Payments Standard
description: Questo articolo descrive come utilizzare l'estensione standard per consentire ai clienti di eseguire pagamenti con PayPal.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="the-paypal-payments-standard-extension"></a>Estensione PayPal Payments Standard

L'estensione PayPal Payments Standard può aiutarti ad aumentare i livelli di servizio clienti semplificando il pagamento delle bollette da parte dei tuoi clienti.

In alternativa alla riscossione dei pagamenti tramite bonifico bancario o carta di credito Schede, i clienti possono pagare tramite il proprio conto PayPal. Quando invii una fattura di vendita tramite e-mail, nel corpo e-mail e nel documento PDF allegato è presente un collegamento a PayPal. Se il cliente sceglie collegare, si apre la pagina di servizio del suo account PayPal e mostra i dettagli del pagamento. Il cliente può quindi pagare la fattura con la stessa modalità di un qualsiasi altro pagamento PayPal.

Il servizio PayPal Payments Standard offre i seguenti vantaggi:

* I pagamenti dei clienti arrivano più velocemente nel conto corrente bancario.
* I clienti hanno più modi a disposizione per pagare le fatture.
* PayPal offre un servizio di pagamento affidabile, che i clienti preferiscono all'immissione dei dati delle carte di credito sui siti Web.
* PayPal offre molteplici modalità di gestione dei pagamenti, inclusa l'elaborazione delle carte di credito, i conti PayPal e altre risorse.
* È possibile aggiungere automaticamente il collegamento di PayPal ai documenti di vendita. Può farlo anche manualmente l'utente interessato.
* Il servizio PayPal Payments Standard non prevede costi mensili o di installazione.
* Dal momento che si tratta di un'estensione, il servizio PayPal Payment Standard può essere abilitato facilmente quando e se richiesto.  

Per saperne di più su come configurare l'estensione, vai a [Abilita il pagamento del cliente tramite PayPal](sales-how-enable-payment-service-extensions.md).

## <a name="register-payments-automatically-for-business-accounts"></a>Registra automaticamente i pagamenti per i conti aziendali

[!INCLUDE [prod_short](includes/prod_short.md)] puoi registrare i pagamenti automaticamente se disponi di un account Commerciante Business per la piattaforma PayPal Commerce. Quando i tuoi clienti utilizzano PayPal collegare per pagare una fattura, [!INCLUDE [prod_short](includes/prod_short.md)] pubblica le voci e Chiudi il documento.

Per utilizzare questa funzionalità, nella pagina  **Impostazione registrazione pagamenti** in [!INCLUDE [prod_short](includes/prod_short.md)], attiva l'opzione  **Registra pagamenti automaticamente** e verifica gli account che utilizzerai per i pagamenti. Se decidi di non voler più registrare i pagamenti automaticamente, puoi disattivarla nuovamente.

> [!TIP]
> Gli sviluppatori possono utilizzare account sandbox per testare la configurazione. Per farlo, cambia l'URL di PayPal in **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] utilizza la notifica immediata dei pagamenti (IPN) di PayPal tramite notify_url.

## <a name="see-also"></a>Vedere anche

[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Setup Vendite](sales-setup-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
