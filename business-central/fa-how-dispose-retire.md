---
title: Cessione o ritiro dei cespiti
description: In caso di vendita o cessione di un cespite, occorre registrare il valore di cessione per calcolare e registrare il guadagno o la perdita.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: 5628, 5610, 5611, 5629, 5633
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: dd8e374a0f7124084d789858767d08c4935d1631
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077321"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Smaltimento o ritiro dei cespiti

In caso di vendita o cessione di un cespite, occorre registrare il valore di cessione per calcolare e registrare il guadagno o la perdita. L'ultimo movimento registrato per un cespite deve essere un movimento di cessione. In caso di cessione parziale di un cespite è possibile registrare più di un movimento di cessione. Il totale di tutti gli importi di cessione registrati deve essere un importo in Avere.  

> [!NOTE]  
> In caso di cessione di un cespite in cambio di un altro cespite, occorre registrare sia la vendita del cespite precedente (cessione) sia l'acquisto del nuovo (acquisizione). Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).  

I seguenti passaggi presuppongono che le categorie di registrazione pertinenti siano già state impostate nella pagina **Categorie registrazione cespiti**. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Per registrare una cessione tramite Registrazioni Cespiti in C/G

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.  
2. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Nel campo **Tipo reg. cespite** scegliere **Cessione**.  
4. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della cessione.  

    > [!NOTE]  
    >  Il passaggio 4 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite, il campo **Conto cessione** contiene il conto di addebito contabilità generale e il campo **Conto saldo cessione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Scegliere l'azione **Registra**.  

In caso di vendita o di cessione parziale di un cespite occorre suddividere il cespite prima di registrare la transazione di cessione. Per ulteriori informazioni, vedere [Trasferimento, divisione o raggruppamento dei cespiti](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Per visualizzare i movimenti contabili di cessione

In caso di vendita o di cessione di un cespite, il valore di cessione viene registrato nella contabilità generale dove è possibile visualizzare il risultato.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.  
2. Selezionare il cespite di cui visualizzare i movimenti, quindi scegliere l'azione **Registri beni ammortizzabili**.  
3. Selezionare il registro beni ammortizzabili di cui visualizzare i movimenti, quindi scegliere l'azione **Movimenti contabili**.  
4. Selezionare una riga con **Cessione** nel campo **Categoria reg. cespite** e scegliere l'azione **Trova movimenti**.  
5. Nella pagina **Trova movimenti** scegliere la riga del movimento contabile e fare clic sull'azione **Mostra movimenti correlati**.  

Viene visualizzata la pagina **Movimenti C/G** in cui è possibile visualizzare i movimenti che hanno comportato la registrazione di cessione.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/dispose-fixed-assets/)

## <a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finanze](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Trova movimenti](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]