---
title: Cessione o ritiro dei cespiti| Documenti Microsoft
description: È necessario registrare un valore di cessione quando si scarta, si vende o si ritira un cespite.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 16d052c67a2d9b5513e9dac901dfeddce0527512
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749420"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Smaltimento o ritiro dei cespiti

In caso di vendita o cessione di un cespite, occorre registrare il valore di cessione per calcolare e registrare il guadagno o la perdita. L'ultimo movimento registrato per un cespite deve essere un movimento di cessione. In caso di cessione parziale di un cespite è possibile registrare più di un movimento di cessione. Il totale di tutti gli importi di cessione registrati deve essere un importo in Avere.  

> [!NOTE]  
> In caso di cessione di un cespite in cambio di un altro cespite, occorre registrare sia la vendita del cespite precedente (cessione) sia l'acquisto del nuovo (acquisizione). Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).  

I seguenti passaggi presuppongono che le categorie di registrazione pertinenti siano già state impostate nella pagina **Categorie registrazione cespiti**. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Per registrare una cessione tramite Registrazioni Cespiti in C/G

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni cespiti in C/G** e quindi scegliere il collegamento correlato.  
2. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Nel campo **Tipo reg. cespite** scegliere **Cessione**.  
4. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della cessione.  

    > [!NOTE]  
    >  Il passaggio 4 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite, il campo **Conto cessione** contiene il conto di addebito contabilità generale e il campo **Conto saldo cessione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Scegliere l'azione **Registra**.  

In caso di vendita o di cessione parziale di un cespite occorre suddividere il cespite prima di registrare la transazione di cessione. Per ulteriori informazioni, vedere [Trasferimento, divisione o raggruppamento dei cespiti](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Per visualizzare i movimenti contabili di cessione
In caso di vendita o di cessione di un cespite, il valore di cessione viene registrato nella contabilità generale dove è possibile visualizzare il risultato.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.  
2. Selezionare il cespite di cui visualizzare i movimenti, quindi scegliere l'azione **Registri beni ammortizzabili**.  
3. Selezionare il registro beni ammortizzabili di cui visualizzare i movimenti, quindi scegliere l'azione **Movimenti contabili**.  
4. Selezionare una riga con **Cessione** nel campo **Categoria reg. cespite** e scegliere l'azione **Trova movimenti**.  
5. Nella pagina **Trova movimenti** scegliere la riga del movimento contabile e fare clic sull'azione **Mostra movimenti correlati**.  

Viene visualizzata la pagina **Movimenti C/G** in cui è possibile visualizzare i movimenti che hanno comportato la registrazione di cessione.  

## <a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finanze](finance.md)  
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Trova movimenti](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]