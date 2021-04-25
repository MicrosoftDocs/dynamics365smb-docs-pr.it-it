---
title: Collegare i movimenti in diverse valute| Documenti Microsoft
description: Se si effettua una vendita in una valuta e si riceve il pagamento in un'altra, è possibile collegare il movimento contabile in più valute.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f0c56a6cc8ed428a8984cb40f43887bd297fca2a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784867"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Abilitare il collegamento dei movimenti contabili fornitore in valute diverse
Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare il pagamento all'acquisto.

In modo analogo, se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile collegare il pagamento alla fattura di vendita.

Nella procedura riportata di seguito viene descritto come configurare questa impostazione per i movimenti contabili fornitori nella pagina **Setup contabilità fornitori e acquisti**. L'impostazione è simile per i movimenti contabili clienti nella pagina **Setup contabilità clienti e vendite**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Per abilitare il collegamento dei movimenti contabili fornitore in valute diverse
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità fornitori e acquisti** e quindi scegliere il collegamento correlato.
2. Nel campo **Collegamenti tra valute** selezionare una delle seguenti opzioni:

| Opzione | Descrizione |
| --- | --- |
| Nessuno |Collegamento fra valute non consentito. |
| UE |Collegamento fra valute UE consentito |
| Tutto |Collegamento fra tutte le valute consentito |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Per impostare i conti C/G per le differenze di arrotondamento di applicazione delle valute  
Se movimenti in diverse valute vengono collegati, è necessario impostare il conto di contabilità generale in cui verranno registrate le differenze di arrotondamento.  

> [!NOTE]  
>  È necessario impostare i conti di contabilità generale prima di completare il task. Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie registrazione clienti** e quindi scegliere il collegamento correlato.  
2. Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.  
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cat. reg. fornitori** e quindi scegliere il collegamento correlato.  
4. Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.  

## <a name="see-also"></a>Vedere anche
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]