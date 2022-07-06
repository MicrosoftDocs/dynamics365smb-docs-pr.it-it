---
title: Collegare i movimenti in diverse valute
description: Se si effettua una vendita in una valuta e si riceve il pagamento in un'altra, è possibile collegare il movimento contabile in più valute.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.search.form: 148, 460, 25
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ec081740ff45dc018d975f6d84deae4aae907cb
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078702"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Abilitare il collegamento dei movimenti contabili fornitore in valute diverse

Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare il pagamento all'acquisto.

In modo analogo, se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile collegare il pagamento alla fattura di vendita.

Nella procedura riportata di seguito viene descritto come configurare questa impostazione per i movimenti contabili fornitori nella pagina **Setup contabilità fornitori e acquisti**. L'impostazione è simile per i movimenti contabili clienti nella pagina **Setup contabilità clienti e vendite**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Per abilitare il collegamento dei movimenti contabili fornitore in valute diverse

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità fornitori**, quindi scegli il collegamento correlato.
2. Nel campo **Collegamenti tra valute** selezionare una delle seguenti opzioni:

| Opzione | Descrizione |
| --- | --- |
| Nessuno |Collegamento fra valute non consentito. |
| UE |Collegamento fra valute UE consentito |
| Tutto |Collegamento fra tutte le valute consentito |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Per impostare i conti C/G per le differenze di arrotondamento di applicazione delle valute

Se movimenti in diverse valute vengono collegati, è necessario impostare il conto di contabilità generale in cui verranno registrate le differenze di arrotondamento.  

> [!NOTE]  
> È necessario impostare i conti di contabilità generale prima di completare il task. Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cat. reg. clienti**, quindi scegli il collegamento correlato.  
2. Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.  
3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cat. reg. fornitori**, quindi scegli il collegamento correlato.  
4. Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/process-foreign-currency-payments-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]