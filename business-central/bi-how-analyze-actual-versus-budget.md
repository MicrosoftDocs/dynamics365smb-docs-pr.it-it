---
title: Analisi degli importi effettivi e degli importi di budget
description: 'Questo articolo descrive come analizzare gli importi effettivi rispetto agli importi a budget per raccogliere, analizzare e condividere i dati dell''azienda.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts" />Analisi degli importi effettivi e degli importi di budget

Come parte della raccolta, dell'analisi e della condivisione dei dati della società, si visualizzano gli importi effettivi rispetto agli importi di budget per tutti i conti e per diversi periodi.

Per analizzare gli importi di budget, è prima necessario creare budget di contabilità generale (C/G). Per ulteriori informazioni, vedi [Creare budget C/G](finance-how-create-budgets.md).

## <a name="view-a-gl-budget" />Visualizzare un budget C/G

In un budget per cui siano state impostate delle dimensioni è possibile filtrare i movimenti e visualizzare budget specifici.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Budget C/G**, quindi scegli il collegamento correlato.
2. Nella pagina **Budget CG** apri il budget che vuoi visualizzare.  
3. All'inizio della pagina, compila i campi secondo le necessità per definire cosa viene visualizzato. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Se hai selezionato il valore **Periodo** nel campo **Mostra come righe** oppure nel campo **Mostra come colonne**, è necessario compilare il campo **Visualizza per**. Se non hai selezionato il valore **Periodo** nei campi, immetti il periodo appropriato nel campo **Filtro data**.  

> [!NOTE]  
> Sono inclusi nel calcolo solo i movimenti del budget contabilità generale con i codici di filtro che vengono immessi nella Scheda dettaglio **Filtri**. I movimenti di budget senza o con altri codici di filtro ne sono esclusi. Finché il filtro rimane nella pagina nel budget vengono visualizzati unicamente i movimenti con questi codici di filtro.  

> [!TIP]  
> Utilizza l'azione **Modifica budget** per modificare il budget. Nel riquadro budget, scegli un importo per visualizzare i movimenti del budget della contabilità generale sottostanti.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts" />Visualizzare gli importi effettivi e preventivati di tutti i conti

È possibile visualizzare budget di contabilità generale e confrontarli con le cifre effettive in diverse aree di [!INCLUDE[prod_short](includes/prod_short.md)].

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Piano dei conti**, selezionare l'azione **Saldo budget C/G**.
3. Nella scheda dettaglio **Opzioni**, compila i campi secondo le necessità per definire cosa viene visualizzato nella tabella.  
4. Passa il mouse su un campo della tabella per leggere una breve descrizione dell'importo visualizzato.

> [!NOTE]  
> I filtri impostati nella testata della pagina verranno applicati sia ai movimenti C/G che ai movimenti budget.

Le colonne a sinistra contengono il piano dei conti. Delle quattro colonne sulla destra, le prime quattro indicano gli importi dare e avere effettivi e previsti per ciascun conto. La quinta indica la relazione proporzionale tra gli importi effettivi e preventivati del conto C/G.  

> [!TIP]  
> Utilizzare il campo **Visualizza per** nella pagina **Saldo budget C/G** per selezionare la durata del periodo. Utilizza il campo **Visualizza come** per selezionare la modalità di calcolo degli importi, **Saldo periodo** o **Saldo alla data**. Scegliere l'azione **Periodo precedente** o **Periodo successivo** per modificare il periodo.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods" />Per visualizzare importi effettivi e preventivati per più periodi

Oltre a visualizzare importi effettivi e preventivati di tutti i conti all'interno di un unico periodo è possibile visualizzare un certo numero di periodo per un unico conto.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Piano dei conti**, seleziona il conto di contabilità generale pertinente quindi scegli l'azione **Confronto budget/contabilità generale**.  
3. Nella scheda dettaglio **Opzioni**, compila i campi secondo le necessità per definire cosa viene visualizzato nella tabella.  
4. Nella scheda dettaglio **Righe** passa il mouse su un campo della tabella per leggere una breve descrizione dell'importo visualizzato.  

## <a name="see-related-training-at-microsoft-learn" />Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index).

## <a name="see-also" />Vedere anche

[Business Intelligence finanziario](bi.md)  
[Utilizzare i report finanziari](bi-how-work-account-schedule.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
