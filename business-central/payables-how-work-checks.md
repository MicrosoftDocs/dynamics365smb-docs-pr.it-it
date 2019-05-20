---
title: Emettere, stampare, annullare un assegno| Documenti Microsoft
description: Descrive come emettere o stampare assegni tramite le registrazioni dei pagamenti e annullare movimenti contabili degli assegni in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0eb1c99d38467969f072659996b0f598ba9d6576
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1254047"
---
# <a name="make-check-payments"></a>Effettuare pagamenti tramite assegno
È possibile emettere assegni elettronici e manuali in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In entrambi i metodi vengono utilizzate le registrazioni pagamenti per emettere assegni ai fornitori. È inoltre possibile annullare assegni e visualizzare movimenti contabili assegni.

La seguente procedura mostra come pagare un fornitore con un assegno automatico applicando il pagamento alla fattura del fornitore pertinente, stampando l'assegno e quindi registrando il pagamento come pagato. Questa operazione determina la registrazione di movimenti contabili fornitori positivi, collegati a movimenti contabili negativi della banca e ad assegni fisici per l'elaborazione della banca.

È possibile pagare con due tipi di assegni. Per entrambi i tipi, il campo **Tipo contropartita** o **Tipo conto** deve contenere **Conto bancario**.

- **Assegno automatico**: selezionare questa opzione per stampare un assegno relativo all'importo specificato nella riga di registrazione pagamenti. È necessario stampare gli assegni prima di poter registrare le righe di registrazione. È possibile selezionare **Assegno automatico** solo se
- **Assegno manuale**: selezionare questa opzione se è stato creato un assegno manualmente e si desidera creare un corrispondente movimento contabile per questo importo. Selezionare questa opzione, non è possibile stampare l'assegno.

> [!NOTE]  
> Per assicurarsi che la banca compensi solo gli assegni e gli importi convalidati, è possibile inviarle un file che contenga informazioni sul fornitore, l'assegno e il pagamento. Per ulteriori informazioni, vedere [Esportare un file Positive Pay](finance-how-positive-pay.md).

La stampante deve essere configurata per i moduli di assegni e deve essere definito il layout dell'assegno da utilizzare. Per ulteriori informazioni, vedere [Definire i layout degli assegni](finance-how-define-check-layouts.md)

È possibile stampare fino a 10 fatture in una pagina per una matrice. Se un assegno si applica a più di 10 fatture, quando si stampa la matrice l'assegno viene annullato alla prima pagina e viene stampata la parola ANNULLATO sull'assegno. Quindi si stampa il resto delle fatture e l'importo totale degli assegni nella seconda pagina. 

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Per pagare una fattura fornitore con un assegno automatico
Di seguito viene descritto come pagare un fornitore tramite assegno. I passaggi sono simili al rimborso dei clienti tramite assegno.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.
2. Compilare le righe di registrazione pagamenti. Per ulteriori informazioni, vedere [Registrare pagamenti e rimborsi](payables-how-post-payments-refunds.md).
3. Nel campo **Codice metodo di pagamento** selezionare **Assegno**.
4. Nel campo **Tipo pagamento banca** selezionare **Assegno automatico**.
5. Scegliere l'azione **Stampa assegno**.
6. Nella pagina **Assegno** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Scegliere il pulsante **Invia a**, selezionare l'opzione **Documento PDF** quindi scegliere il pulsante **OK**.

    Gli assegni fisici possono ora essere portati in banca per l'elaborazione. Passare alla registrazione del pagamento come collegato al fornitore e pertanto pagato nel sistema.
8. Scegliere l'azione **Registra**.

Vengono creati movimenti contabili fornitori collegati completamente e movimenti contabili bancari.

> [!NOTE]  
> Se si desidera stampare e pagare gli assegni provenienti da vari conti correnti bancari utilizzando più di una valuta, eseguire un singolo processo batch **Stampa assegno** per ogni valuta, specificando il conto corrente bancario appropriato.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Per annullare assegni stampati che non sono registrati
È possibile annullare gli assegni non registrati dopo che sono stati stampati utilizzando l'azione **Annullo assegno** della pagina **Registrazioni pagamenti**.

1. Nella pagina **Registrazioni pagamenti** scegliere **Annullo assegno**, quindi scegliere gli assegni da annullare.

## <a name="to-void-checks"></a>Per annullare gli assegni
Una volta che i pagamenti tramite assegno sono stati registrati, è possibile annullare gli assegni dai movimenti contabili bancari risultanti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **C/C bancari** e quindi scegliere il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato, scegliere l'azione **Modifica**, quindi scegliere l'azione **Mov. contabili assegni**.
3. Nella pagina **Mov. contabili assegni** scegliere l'azione **Annullo assegno**.
4. Selezionare la casella di controllo **Annullo solo assegno**.
5. Scegliere il pulsante **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Per visualizzare un riepilogo degli assegni registrati
Se si desidera verificare gli assegni registrati, ad esempio per verificare più assegni pagati a un fornitore, è possibile utilizzare il report **C/C bancario - Dettaglio assegni**.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **C/C bancario - Dettaglio assegni** e quindi scegliere il collegamento correlato.
2. Impostare i filtri desiderati quindi scegliere il pulsante **Anteprima**.

## <a name="see-also"></a>Vedi anche
[Effettuare i pagamenti](payables-make-payments.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
