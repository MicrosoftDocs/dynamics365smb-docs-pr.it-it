---
title: Assegnare un livello di priorità a un fornitore (video)
description: È possibile assegnare dei numeri ai fornitori per assegnare loro una priorità e semplificare i suggerimenti di pagamento in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'supplier, payment priority'
ms.search.form: '26, 27'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Attribuire un ordine di priorità ai fornitori

[!INCLUDE[prod_short](includes/prod_short.md)] può fornire suggerimenti di pagamento ai fornitori, ad esempio pagamenti con scadenza a breve termine oppure pagamenti che prevedono uno sconto. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).

Innanzitutto, è necessario assegnare una priorità ai fornitori assegnando loro dei numeri.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## Per attribuire un ordine di priorità ai fornitori

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Selezionare il fornitore appropriato e scegliere **Modifica**.
3. Nel campo **Priorità** immettere un numero.

In [!INCLUDE[prod_short](includes/prod_short.md)] il numero più basso, escluso lo 0, ha la massima priorità. Così, ad esempio, se si usano 1, 2 e 3, 1 avrà la massima priorità.

Se non si desidera dare la priorità a un fornitore, lasciare vuoto il campo **Priorità**. Quindi, se si usa la funzione di suggerimento di pagamento, il fornitore si troverà dopo tutti i fornitori che hanno un numero di priorità. Si possono immettere tutti i livelli di priorità necessari.

## Vedere anche

[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
