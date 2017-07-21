---
title: Impostare e utilizzare righe standard per vendite e acquisti ricorrenti| Documenti Microsoft
description: "È possibile impostare righe di vendita e acquisto più frequentemente usate e quindi inserirle nei documenti di vendita e di acquisto per compilare rapidamente le righe con informazioni standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a>Procedura: Creare righe di vendite e acquisti ricorrenti
Se è spesso necessario creare righe di vendita e acquisto con informazioni simili, è possibile impostare righe standard da inserire nei documenti di vendita e di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti.  

La seguente procedura illustra come utilizzare le righe di vendita standard. Funziona in modo simile per le righe di acquisto standard.  

## <a name="to-set-up-standard-sales-lines"></a>Per impostare righe di vendita standard  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici vendite standard**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Righe vendita standard** scegliere l'azione **Nuovo**.  
3. Compilare i campi appropriati della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Nella Scheda dettaglio **Righe**, immettere le informazioni nei campi per preparare le righe di vendita che riflettono le righe standard che si prevede di utilizzare come righe ricorrenti nei documenti di vendita.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Per inserire le righe di vendita standard in una fattura di vendita
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture**, quindi scegliere il collegamento correlato.
2. Aprire la fattura di vendita in cui si desidera inserire una più righe di vendita standard.
3. Scegliere l'azione **Ottieni righe vendita ricorrenti**.
4. Nella finestra **Righe vendita ricorrenti**, scegliere il pulsante di ricerca nel campo **Codice** e selezionare una serie di righe di vendita standard.
5. Scegliere il pulsante **OK** per inserire le righe di vendita standard della fattura, in cui è possibile riutilizzare la riga come è o modificarne le informazioni.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Per creare più fatture di vendita in base alle righe di vendita standard
È possibile utilizzare il processo batch **Crea fattura di vendita periodica** per creare fatture di vendita in base a righe di vendita standard assegnate ai clienti e con date di registrazione comprese nell'intervallo di date valide specificato nel codice di vendita standard.

Nella finestra **Righe vendita ricorrenti** è anche possibile specificare un metodo di pagamento in addebito diretto e un mandato di addebito diretto. Le fatture di vendita create con il processo batch **Crea fattura di vendita periodica** includeranno le informazioni necessarie per riscuotere il pagamento per le fatture di vendita con addebito diretto SEPA. Per ulteriori informazioni, vedere Riscuotere pagamenti con addebito diretto SEPA.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Crea fatture di vendita periodiche**, quindi scegliere il collegamento correlato.
2. In **Crea fattura di vendita periodica** compilare i campi come necessario.
3. Nel campo **Codice** immettere il codice delle righe di vendita standard assegnato a un cliente per cui si desidera creare fatture di vendita.
4. Scegliere il pulsante **OK**.

Le fatture di vendita vengono create per i clienti con il codice di vendita cliente standard specificato e con eventuali informazioni sull'addebito diretto specificate, per la registrazione alla data specificata.

## <a name="see-also"></a>Vedi anche  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

