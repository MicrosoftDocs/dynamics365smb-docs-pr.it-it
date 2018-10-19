---
title: Impostare righe standard per vendite e acquisti ricorrenti| Documenti Microsoft
description: "È possibile impostare righe di vendita e acquisto più frequentemente usate e quindi inserirle nei documenti di vendita e di acquisto per compilare rapidamente le righe con informazioni standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Creare righe di vendite e acquisti ricorrenti
Se è spesso necessario creare righe di vendita e acquisto con informazioni simili, è possibile impostare righe standard da inserire nei documenti di vendita e di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti.  

La seguente procedura illustra come utilizzare le righe di vendita standard. Funziona in modo simile per le righe di acquisto standard.  

## <a name="to-set-up-standard-sales-lines"></a>Per impostare righe di vendita standard  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Righe vendita standard** e quindi scegliere il collegamento correlato.  
2. Nella finestra **Righe vendita standard** scegliere l'azione **Nuovo**.  
3. Compilare i campi appropriati della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Nella Scheda dettaglio **Righe**, immettere le informazioni nei campi per preparare le righe di vendita che riflettono le righe standard che si prevede di utilizzare come righe ricorrenti nei documenti di vendita.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Per inserire le righe di vendita standard in una fattura di vendita
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture** e quindi scegliere il collegamento correlato.
2. Aprire la fattura di vendita in cui si desidera inserire una più righe di vendita standard.
3. Scegliere l'azione **Ottieni righe vendita ricorrenti**.
4. Nella finestra **Righe vendita ricorrenti**, scegliere il pulsante di ricerca nel campo **Codice** e selezionare una serie di righe di vendita standard.

    > [!NOTE]
    > Per utilizzare le righe di vendita ricorrenti impostate insieme al processo batch **Crea fatture di vendita periodiche**, è necessario anche compilare i campi **Data di inizio validità** e **Data di fine validità** nella finestra **Righe vendita ricorrenti**. Per ulteriori informazioni, vedere la sezione "Creare più fatture di vendita in base a codici vendite standard".

5. Scegliere il pulsante **OK** per inserire le righe di vendita standard della fattura, in cui è possibile riutilizzare la riga come è o modificarne le informazioni.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Per creare più fatture di vendita in base alle righe di vendita standard
È possibile utilizzare il processo batch **Crea fatture di vendita periodica** per creare fatture di vendita in base alle righe di vendita standard assegnate ai clienti e con date di registrazione comprese nell'intervallo di date valide specificato nelle righe di vendita standard.

> [!NOTE]
> Nella finestra **Righe vendita ricorrenti** è anche possibile specificare un metodo di pagamento in addebito diretto e un mandato di addebito diretto. Le fatture di vendita create con il processo batch **Crea fattura di vendita periodica** includeranno le informazioni necessarie per riscuotere il pagamento per le fatture di vendita con addebito diretto SEPA. Per ulteriori informazioni, vedere [Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Crea fatture di vendita periodiche** e quindi scegliere il collegamento correlato.
2. Compilare i campi della finestra **Crea fatture di vendita periodica** in base alle esigenze.
3. Nel campo di filtro **Codice** immettere il codice delle righe di vendita standard assegnato a un cliente per cui si desidera creare fatture di vendita.
4. Scegliere il pulsante **OK**.

Le fatture di vendita vengono create per i clienti con il codice di vendita cliente standard specificato e con eventuali informazioni sull'addebito diretto specificate, per la registrazione alla data specificata.

## <a name="see-also"></a>Vedi anche  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

