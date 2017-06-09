---
title: 'Procedura: Utilizzare gli assegni | Documenti Microsoft'
description: 'Procedura: Utilizzo degli assegni'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6debfe7d1f5e9726ba1f70d023076d73f123ef24
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-checks"></a>Procedura: Utilizzo degli assegni
È possibile emettere assegni elettronici e manuali in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In entrambi i metodi vengono utilizzate le registrazioni pagamenti per emettere assegni ai fornitori. È inoltre possibile annullare assegni e visualizzare movimenti contabili assegni.

Il processo di emissione degli assegni comporta il suggerimento di pagamenti, la creazione di movimenti contabili e la stampa di assegni automatici.

**Note**: per assicurarsi che la banca compensi solo gli assegni e gli importi convalidati, è possibile inviarle un file che contenga informazioni sul fornitore, l'assegno e il pagamento. Per ulteriori informazioni, vedere [Procedura: Esportare un file Positive Pay](finance-how-positive-pay.md).

La stampante deve essere configurata per i moduli di assegni e deve essere definito il layout dell'assegno da utilizzare. Per ulteriori informazioni, vedere [Procedura: Definire i layout degli assegni](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Per emettere assegni
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registraz. pagamenti**, quindi scegliere il collegamento correlato.
2. Compilare le registrazioni con pagamenti rilevanti, ad esempio utilizzando la funzione Sugg. pagamenti fornitore. Per ulteriori informazioni, vedere [Procedura: Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).
3. Nel campo **Tipo pagamento banca** nelle righe di registrazione per il pagamento che si desidera effettuare con assegni, selezionare una delle seguenti opzioni:

   * **Assegno automatico**: selezionare questa opzione per stampare un assegno relativo all'importo specificato nella riga di registrazione pagamenti. È necessario stampare gli assegni prima di poter registrare le righe di registrazione. È possibile selezionare **Assegno automatico** solo se il campo **Tipo contropartita** o il campo **Tipo conto** è impostato su **Conto bancario**.
   * **Assegno manuale**: selezionare questa opzione se è stato creato un assegno manualmente e si desidera creare un corrispondente movimento contabile per questo importo. Non è possibile stampare assegni tramite questa opzione da [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile selezionare **Assegno manuale** solo se il campo **Tipo contropartita** o il campo **Tipo conto** è impostato su **Conto bancario**.

     **Nota**: è necessario stampare gli assegni automatici prima di poter registrare le righe di registrazione correlate.
4. In caso di assegni automatici, scegliere **Stampa assegno**.
5. Nella finestra **Assegno** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Selezionare il pulsante **Stampa**.

**Nota**: se è necessario stampare automaticamente gli assegni provenienti da vari conti correnti bancari utilizzando più di una valuta, eseguire un singolo processo batch **Stampa assegno** per ogni valuta, specificando il conto corrente bancario appropriato.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Per annullare assegni stampati che non sono registrati
È possibile annullare gli assegni non registrati dopo che sono stati stampati utilizzando l'azione **Annullo assegno** della finestra **Registrazioni pagamenti**.

1. Nella finestra **Registrazioni pagamenti** scegliere **Annullo assegno**, quindi scegliere gli assegni da annullare.

## <a name="to-void-checks"></a>Per annullare gli assegni
Una volta che i pagamenti tramite assegno sono stati registrati, è possibile annullare gli assegni dai movimenti contabili bancari risultanti.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Conti Correnti Bancari**, quindi scegliere il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato, scegliere l'azione **Modifica**, quindi scegliere l'azione **Mov. contabili assegni**.
3. Nella finestra **Mov. contabili assegni** scegliere l'azione **Annullo assegno**.
4. Selezionare la casella di controllo **Annullo solo assegno**.
5. Scegliere il pulsante **OK**.

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Procedura: Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

