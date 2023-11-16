---
title: Gestire budget per i cespiti
description: 'Impostare le informazioni relative agli investimenti futuri, alle cessioni e all''ammortamento dei cespiti per preparare i budget e le previsioni.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.search.form: '5610, 5611'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="manage-budgets-for-fixed-assets"></a>Gestione dei budget per i cespiti

È possibile impostare i cespiti previsti. Ad esempio, ciò consente di includere qualsiasi vendita o acquisto previsto nei report.  

Per preparare una stima di estratto conto, di conto di bilancio o un budget di cassa occorre disporre di informazioni relative agli investimenti futuri, alle cessioni e all'ammortamento dei cespiti. Queste informazioni sono reperibili nel report **Cespite - Valore previsto**. Prima di stampare questo report occorre preparare il budget.  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Per prevedere i costi di acquisto di un cespite

Al fine di preparare un budget occorre impostare le schede cespiti per i cespiti che si desidera acquistare in futuro. I cespiti del budget vengono impostati come cespiti generici, ma è necessario impostarli in modo che non venga effettuata la registrazione nella contabilità generale.

Durante la registrazione del costo di acquisto, immettere il numero del cespite previsto nel campo **Nr. cespite previsto**. Ciò provocherà la registrazione del costo di acquisto con segno opposto per il cespite previsto. Ne consegue che il costo totale di acquisto del cespite previsto risulta dalla differenza tra il costo di acquisto previsto e quello effettivo.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo** per creare una nuova scheda cespite per il cespite previsto.
3. Selezionare la casella di controllo **Cespite previsto** per evitare la registrazione nella contabilità generale.
4. Compilare i campi rimanenti, assegnare un registro beni ammortizzabili e registrare il primo costo di acquisto con il cespite previsto immesso nel campo **Nr. cespite previsto** nella riga delle registrazioni. Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Per prevedere la cessione di un cespite

Nel caso in cui si progetti la vendita di cespiti all'interno del periodo di budget è possibile immettere informazioni relative al prezzo di vendita e alla data di vendita.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite da cedere e scegliere l'azione **Registri beni ammortizz.**.
3. Nella pagina **Registro beni amm. cespiti** compilare i campi **Data cessione prev.** e **Proventi di cessione previsti**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Per visualizzare i valori di cessione previsti

Per visualizzare i valori di cessione previsti e calcolare i profitti e perdite è possibile utilizzare il report **Cespite - Valore Previsto**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Valore previsto cespiti**, quindi scegli il collegamento correlato.
2. Compilare i campi, se necessario.
3. Selezionare il pulsante **Stampa** o **Anteprima**.

## <a name="to-budget-depreciation"></a>Per prevedere l'ammortamento

Utilizzare il report **Cespite - Valore Previsto** per calcolare l'ammortamento futuro. Il report mostra il valore contabile e l'ammortamento accumulato all'inizio del periodo selezionato, le modifiche apportate durante il periodo, il valore contabile e l'ammortamento accumulato alla fine del periodo selezionato.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Valore previsto cespiti**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze.
3. Per visualizzare i valori totali di tutti i cespiti, deselezionare la casella di controllo **Stampa per cespite**.
4. Non compilare la Scheda dettaglio **Cespite** in modo che vengano inclusi tutti i cespiti. Nel campo **Cespite previsto** immettere **No** per escludere i cespiti previsti o **Sì** per visualizzare solo i cespiti previsti.
5. Seleziona il pulsante **Stampa** o **Anteprima**.

## <a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Dati finanziari](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
