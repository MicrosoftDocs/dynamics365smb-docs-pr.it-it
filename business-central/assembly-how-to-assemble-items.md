---
title: Assemblare articoli
description: Se nel campo Sistema di rifornimento nella scheda articolo è indicato Assemblaggio, il metodo predefinito per l'approvvigionamento dell'articolo consiste nell'assemblarlo da componenti definiti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 13f1a68ebb3c9a16c06cdc0cf9382867403ba5ca
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079248"
---
# <a name="assemble-items"></a>Assemblare articoli

Se nel campo **Sistema di rifornimento** nella scheda articolo è indicato **Assemblaggio**, il metodo di default per l'approvvigionamento dell'articolo consiste nell'assemblarlo da componenti definiti e potenzialmente tramite una risorsa definita.  

I componenti e le risorse che rientrano in questo tipo di articolo di assemblaggio devono essere definiti in una DB di assemblaggio. Per altre informazioni, vedere [Utilizzare le distinte base](inventory-how-work-BOMs.md).  

Gli articoli di assemblaggio possono essere impostati per due diversi processi di assemblaggio:  

-   Assemblaggio per magazzino.  
-   Assemblaggio su ordine.  

In genere si utilizza l'**assemblaggio per magazzino** per gli articoli che si desidera assemblare prima delle vendite, ad esempio preparare una campagna di kit e tenerli in stock fino a quando vengono ordinati. Tali articoli sono in genere articoli standard, ad esempio in kit in pacchetti di cui non viene offerta la personalizzazione in base richieste del cliente.  

In genere si utilizza l'**assemblaggio su ordine** per gli articoli che non si desidera immagazzinare perché si prevede di personalizzarli in base alle richieste del cliente o perché si desidera ridurre i costi di trasporto a magazzino, approvvigionandoli secondo il metodo JIT (Just-In-Time). Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

Per ulteriori informazioni sull'impostazione di un articolo di assemblaggio, vedere [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).  

Queste opzioni di setup sono impostazioni di default che gestiscono il modo in cui le righe ordine di assemblaggio e di vendita vengono inizialmente elaborate. È possibile ignorare queste impostazioni di default r approvvigionare l'articolo di assemblaggio nel modo ottimale durante l'elaborazione di una vendita. Per ulteriori informazioni, vedere [Vendere gli articoli di magazzino nei flussi assemblaggio su ordine](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) e [Vedere insieme articoli assemblaggio su ordine e articoli in magazzino](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> I componenti di assemblaggio sono gestiti in modo speciale in configurazioni di warehouse di base. Per altre informazioni, vedere la sezione "Gestione di articoli da assemblare su ordine in prelievi magazzino" in [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).   

In questa procedura, viene creato ed elaborato un ordine di assemblaggio per gli articoli che vengono assemblati per magazzino, ovvero senza un ordine di vendita collegato. I passaggi includono la creazione dell'ordine di assemblaggio, la gestione dei potenziali problemi di disponibilità dei componenti e la registrazione parziale dell'output dell'articolo di assemblaggio.

## <a name="to-assemble-an-item"></a>Per assemblare un articolo

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di assemblaggio**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**. Verrà visualizzata la pagina **Nuovo ordine di assemblaggio**.  
3.  Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Nel campo **Nr. articolo** selezionare dell'articolo di assemblaggio che si desidera elaborare. Il campo viene filtrato in modo da visualizzare solo gli articoli impostati per l'assemblaggio, ovvero quelli a cui sono assegnate DB di assemblaggio.  
5.  Nel campo **Quantità** immettere il numero di unità dell'articolo che si desidera assemblare.  

    > [!NOTE]  
    >  Se uno o più componenti non sono disponibili per soddisfare la quantità dell'articolo di assemblaggio alla data di scadenza definita, la pagina **Disponibilità assemblaggio** viene visualizzata automaticamente per fornire informazioni dettagliate relative al numero di articoli di assemblaggio che è possibile assemblare in base alla disponibilità dei componenti. Per altre informazioni, vedere [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md).  Quando si chiude la pagina, l'ordine di assemblaggio viene creato con avvisi di disponibilità nelle righe del componente interessato.  

    Le righe ordine di assemblaggio vengono compilate automaticamente con il contenuto della DB di assemblaggio e con le quantità delle righe in base alla testata ordine di assemblaggio.  

    > [!NOTE]  
    >  Se la pagina **Disponibilità assemblaggio** è stata aperta al momento della compilazione della testata dell'ordine di assemblaggio, ogni riga dell'ordine di assemblaggio interessata contiene **Sì** nel campo **Avviso di disponibilità** con un collegamento alle informazioni dettagliate sulla disponibilità. Per ulteriori informazioni, vedere Controllo disponibilità. È possibile risolvere un problema di disponibilità dei componenti rimandando la data di inizio, sostituendo il componente con un altro articolo o selezionando una sostituzione disponibile, se definita.  

6.  Nel campo **Quantità da assemblare** immettere il numero di unità dell'articolo di assemblaggio che si desidera registrare come output alla successiva registrazione dell'ordine di assemblaggio. Questa quantità può essere inferiore al valore nel campo **Quantità** per riflettere una registrazione di output parziale.  

    > [!NOTE]  
    >  Per garantire che la registrazione del consumo di componenti corrisponda alla registrazione di output dell'articolo di assemblaggio, i campi relativi alla quantità nelle righe dell'ordine di assemblaggio verranno rettificati automaticamente in base al valore immesso nel campo **Quantità da assemblare**.  
7.  Nelle righe ordine di assemblaggio di tipo **Articolo** o **Risorsa**, nel campo **Quantità da consumare** immettere il numero di unità che si desidera registrare come consumate alla successiva registrazione dell'ordine di assemblaggio.
8.  Quando si è pronti per registrare parzialmente o completamente, scegliere l'azione **Registra**.  

    > [!NOTE]  
    >  Se gli avvisi sono ancora presenti in una qualsiasi delle righe ordini di assemblaggio, la registrazione viene bloccata. Viene visualizzato un messaggio sul componente o sui componenti non presenti in magazzino.  

Una volta effettuata la registrazione, l'articolo di assemblaggio viene registrato come output nel codice ubicazione e nel codice collocazione potenziale definiti nell'ordine di assemblaggio. Per gli ordini di assemblaggio creati manualmente, l'ubicazione può essere copiata dal campo di setup **Ubicazione di default per gli ordini**. Per i flussi di assemblaggio su ordine, il codice ubicazione può essere copiato dalla riga ordine di vendita.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]