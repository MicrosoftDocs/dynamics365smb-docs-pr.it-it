---
title: Impostare righe standard per vendite e acquisti ricorrenti| Documenti Microsoft
description: È possibile impostare righe di vendita e acquisto più frequentemente usate e quindi inserirle nei documenti di vendita e di acquisto per compilare rapidamente le righe con informazioni standard.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 35395ad71dbc0717410ed5a910f5bcd0170b1d8c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "936790"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Creare righe di vendite e acquisti ricorrenti
Se è spesso necessario creare righe di vendita e acquisto con informazioni simili, è possibile impostare righe standard da inserire nei documenti di vendita e di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti.  

La seguente procedura illustra come utilizzare le righe di vendita standard in una fattura di vendita. I passaggi sono simili per tutti gli altri documenti di acquisto e di vendita.  

## <a name="to-set-up-standard-sales-lines"></a>Per impostare righe di vendita standard  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Righe vendita standard** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Righe vendita standard** scegliere l'azione **Nuovo**.  
3. Compilare i campi appropriati della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Nella Scheda dettaglio **Righe**, immettere le informazioni nei campi per preparare le righe di vendita che riflettono le righe standard che si prevede di utilizzare come righe ricorrenti nei documenti di vendita.  

> [!NOTE]
> Non è possibile definire i prezzi nelle righe di vendita standard poiché prezzi, sconti e così via sono calcolati nei documenti di vendita effettivi dopo l'inserimento delle righe di vendita standard.

## <a name="to-assign-standard-sales-lines-to-a-customers"></a>Per assegnare righe di vendita standard ai clienti
Assegnare una o più righe di vendita standard a un cliente di modo che sia possibile inserirle nei documenti di vendita per quel cliente.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda di un cliente pertinente.
3. Scegliere l'azione **Righe vendita ricorrenti**.
4. Nella pagina **Righe vendita ricorrenti**, selezionare i codici per le righe di vendita ricorrenti che si intende inserire in documenti di vendita per il cliente.
5. Compilare i campi aggiuntivi per definire quando, come e dove le righe di vendita ricorrenti devono essere utilizzate. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Per inserire righe di vendita ricorrenti in una fattura di vendita
Se esistono righe di vendita ricorrenti per il cliente, è possibile inserirle in tutti i tipi di documenti di vendita come una fattura di vendita. Se è stata attivata la notifica in questione, si verrà informati dell'esistenza di righe di vendita ricorrenti.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture** e quindi scegliere il collegamento correlato.
2. Aprire la fattura di vendita in cui si desidera inserire una più righe di vendita standard.
3. Scegliere l'azione **Ottieni righe vendita ricorrenti**.
4. Nella pagina **Righe vendita ricorrenti**, scegliere il pulsante di ricerca nel campo **Codice** e selezionare una serie di righe di vendita standard.

    > [!NOTE]
    > Per utilizzare le righe di vendita ricorrenti impostate insieme al processo batch **Crea fatture di vendita periodiche**, è necessario anche compilare i campi **Data di inizio validità** e **Data di fine validità** nella pagina **Righe vendita ricorrenti**. Per ulteriori informazioni, vedere [Per creare più fatture di vendita in base alle righe di vendita standard](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Scegliere il pulsante **OK** per inserire le righe di vendita standard della fattura, in cui è possibile riutilizzare la riga come è o modificarne le informazioni.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Per creare più fatture di vendita in base alle righe di vendita standard
È possibile utilizzare il processo batch **Crea fatture di vendita periodica** per creare fatture di vendita in base alle righe di vendita standard assegnate ai clienti e con date di registrazione comprese nell'intervallo di date valide specificato nelle righe di vendita standard.

> [!NOTE]
> Nella pagina **Righe vendita ricorrenti** è anche possibile specificare un metodo di pagamento in addebito diretto e un mandato di addebito diretto. Le fatture di vendita create con il processo batch **Crea fattura di vendita periodica** includeranno le informazioni necessarie per riscuotere il pagamento per le fatture di vendita con addebito diretto SEPA. Per ulteriori informazioni, vedere [Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Crea fatture di vendita periodiche** e quindi scegliere il collegamento correlato.
2. Compilare i campi della pagina **Crea fatture di vendita periodica** in base alle esigenze.
3. Nel campo di filtro **Codice** immettere il codice delle righe di vendita standard assegnato a un cliente per cui si desidera creare fatture di vendita.
4. Scegliere il pulsante **OK**.

Le fatture di vendita vengono create per i clienti con il codice di vendita cliente standard specificato e con eventuali informazioni sull'addebito diretto specificate, per la registrazione alla data specificata.

## <a name="see-also"></a>Vedi anche  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)