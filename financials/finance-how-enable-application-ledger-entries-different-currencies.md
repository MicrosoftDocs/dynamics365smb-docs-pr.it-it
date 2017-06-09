---
title: 'Procedura: Abilitare il collegamento dei movimenti contabili fornitore in valute diverse | Documenti Microsoft'
description: Informazioni su come collegare movimenti contabili fornitore in valute diverse.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4f904d1600d56a83238581915726a7b7fd6cca38
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a>Procedura: Abilitare il collegamento dei movimenti contabili fornitore in valute diverse
Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare il pagamento all'acquisto.

In modo analogo, se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile collegare il pagamento alla fattura di vendita.

Nella procedura riportata di seguito viene descritto come configurare questa impostazione per i movimenti contabili fornitori nella finestra **Setup contabilità fornitori e acquisti**. L'impostazione è simile per i movimenti contabili clienti nella finestra **Setup contabilità clienti e vendite**.

**Nota**: questa funzionalità richiede che l'esperienza sia impostata su ***** Suite *****. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Per abilitare il collegamento dei movimenti contabili fornitore in valute diverse
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Setup contabilità fornitori e acquisti**, quindi scegliere il collegamento correlato.
2. Nel campo **Collegamenti tra valute** selezionare una delle seguenti opzioni:

| Opzione | Descrizione |
| --- | --- |
| Nessuno |Collegamento fra valute non consentito. |
| UE |Collegamento fra valute UE consentito |
| Tutto |Collegamento fra tutte le valute consentito |

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

