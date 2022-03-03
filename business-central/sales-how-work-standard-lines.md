---
title: Righe di vendite e acquisti ricorrenti standard
description: Imposta le righe di vendita e acquisto più frequentemente usate e quindi inseriscile nei documenti di vendita e di acquisto per compilare rapidamente le righe con informazioni standard.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 6039739825964ce059a4f76d1e92f32b581c60a7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144751"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Creare righe di vendite e acquisti ricorrenti
Se è spesso necessario creare righe di vendita e acquisto con informazioni simili, è possibile impostare righe standard da inserire nei documenti di vendita e di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti.  

La seguente procedura illustra come utilizzare le righe di vendita standard in una fattura di vendita. I passaggi sono simili per tutti gli altri documenti di acquisto e di vendita.  

## <a name="to-set-up-recurring-sales-lines"></a>Per impostare righe di vendita ricorrenti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Righe vendita ricorrenti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Righe vendita ricorrenti** scegliere l'azione **Nuovo**.  
3. Compilare i campi appropriati della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Nella Scheda dettaglio **Righe**, immettere le informazioni nei campi per preparare le righe di vendita che riflettono le righe standard che si prevede di utilizzare come righe ricorrenti nei documenti di vendita.  

> [!NOTE]
> Non è possibile definire i prezzi nelle righe di vendita ricorrenti poiché prezzi, sconti e così via sono calcolati nei documenti di vendita effettivi dopo l'inserimento delle righe di vendita ricorrenti.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Per assegnare righe di vendita ricorrenti a un cliente

Assegnare una o più righe di vendita ricorrenti a un cliente di modo che sia possibile inserirle nei documenti di vendita per quel cliente.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Aprire la scheda di un cliente pertinente.
3. Scegliere l'azione **Righe vendita ricorrenti**.
4. Nella pagina **Righe vendita ricorrenti**, selezionare i codici per le righe di vendita ricorrenti che si intende inserire in documenti di vendita per il cliente.
5. Compilare i campi aggiuntivi per definire quando, come e dove le righe di vendita ricorrenti devono essere utilizzate.  

    Se si pensa di utilizzare le righe di vendita ricorrenti impostate insieme al processo batch **Crea fatture di vendita periodiche**, usare i campi **Data di inizio validità** e **Data di fine validità** per limitare quando usare le righe di vendita ricorrenti per la creazione di fatture. Per ulteriori informazioni, vedere [Per creare più fatture di vendita in base alle righe di vendita standard](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-recurring-sales-lines).

    È anche possibile specificare un metodo di pagamento in addebito diretto e un mandato di addebito diretto. Le fatture di vendita create con il processo batch **Crea fattura di vendita periodica** includeranno le informazioni necessarie per riscuotere il pagamento con addebito diretto SEPA. Per ulteriori informazioni, vedere [Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md).

6. Nei quattro campi in cui si è scelto in che modo inserire le righe in quattro tipi di documento, selezionare una delle seguenti opzioni:

|Opzione|Descrizione|
|------|-----------|
|**Manuale**|È possibile cercare e inserire manualmente la riga di vendite ricorrenti esistente per il cliente.|
|**Automatico**|Se esistono più righe di vendite ricorrenti per il cliente, viene visualizzata una notifica da cui è possibile selezionare quale inserire. Se esiste una sola riga di vendite ricorrenti, verrà inserita automaticamente.<br /><br />Si noti che ciò funziona solo se il nuovo documento è stato creato da un elenco di documenti, ad esempio selezionando l'azione **Nuovo** nella pagina **Ordini vendita**. Non funziona se il documento è stato creato, ad esempio, da una scheda cliente.|
|**Chiedi sempre**|Una notifica verrà visualizzata e tutte le righe di vendite ricorrenti esistenti vengono visualizzate in modo che sia possibile selezionarne una.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Per inserire righe di vendita ricorrenti in una fattura di vendita

Se esistono righe di vendita ricorrenti per il cliente, è possibile inserirle o farle inserire in tutti i tipi di documenti di vendita come una fattura di vendita. Se hai attivato le opzioni **Chiedi sempre**, si verrà informati dell'esistenza di righe di vendita ricorrenti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture**, quindi seleziona il collegamento correlato.
2. Aprire la fattura di vendita in cui si desidera inserire una più righe di vendita standard.
3. Scegliere l'azione **Ottieni righe vendita ricorrenti**.
4. Nella pagina **Righe vendita ricorrenti**, scegliere il pulsante di ricerca nel campo **Codice** e selezionare una serie di righe di vendita standard.
5. Scegliere il pulsante **OK** per inserire le righe di vendita standard della fattura, in cui è possibile riutilizzare la riga come è o modificarne le informazioni.

## <a name="to-create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Per creare più fatture di vendita in base alle righe di vendita ricorrenti
È possibile utilizzare il processo batch **Crea fatture di vendita periodica** per creare fatture di vendita in base alle righe di vendita standard assegnate ai clienti e con date di registrazione comprese nell'intervallo di date valide specificato nelle righe di vendita standard.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Crea fatture di vendita periodica**, quindi seleziona il collegamento correlato.
2. Compilare i campi della pagina **Crea fatture di vendita periodica** in base alle esigenze.
3. Nel campo di filtro **Codice** immettere il codice delle righe di vendita standard assegnato a un cliente per cui si desidera creare fatture di vendita.
4. Scegliere il pulsante **OK**.

Le fatture di vendita vengono create per i clienti con il codice di vendita cliente standard specificato e con eventuali informazioni sull'addebito diretto specificate, per la registrazione alla data specificata.

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]