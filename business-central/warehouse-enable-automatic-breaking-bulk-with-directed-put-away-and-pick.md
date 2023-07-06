---
title: Breakbulk con stoccaggi e prelievi guidati
description: 'Scopri come abilitare il breakbulk automatico con lo stoccaggio e il prelievo diretti, nonché il breakbulk in prelievo, stoccaggio, movimenti e altro ancora.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Abilitare breakbulk automatico con stoccaggi e prelievi guidati

Per le ubicazioni che utilizzano stoccaggi e prelievi guidati, [!INCLUDE[prod_short](includes/prod_short.md)] può suddividere unità di misura più grandi in unità di misura più piccole, durante la creazione delle istruzioni di warehouse per documenti di origine, ordini di produzione o prelievi e stoccaggi interni. Breakbulk può anche significare raccogliere articoli in unità di misura più piccole per eguagliare la quantità di un'unità di misura più grande su un documento di origine o un ordine di produzione.

## <a name="breakbulk-in-picks"></a><a name="breakbulk-in-picks"></a><a name="breakbulk-in-picks"></a>Breakbulk relativo ai prelievi

Se desideri immagazzinare articoli con unità di misura differenti in una posizione e consentire di combinarli automaticamente nel processo di prelievo, abilita l'interruttore **Permettere breakbulk** nella pagina della scheda Ubicazione. Successivamente, per eseguire un'attività, [!INCLUDE [prod_short](includes/prod_short.md)] cerca un articolo con la stessa unità di misura. Se non lo trova, [!INCLUDE [prod_short](includes/prod_short.md)] suggerirà di suddividere un'unità di misura più grande nell'unità di misura necessaria.  

Sono disponibili solo le unità di misura più piccole, [!INCLUDE [prod_short](includes/prod_short.md)] suggerirà di raggruppare gli articoli in modo da soddisfare la quantità specificata nell'ordine di spedizione o di produzione. Di fatto, l'unità di misura più grande riportata nel documento di origine viene suddivisa in unità di misura più piccole per il prelievo.  

## <a name="breakbulk-in-put-aways"></a><a name="breakbulk-in-put-aways"></a><a name="breakbulk-in-put-aways"></a>Breakbulk relativo agli stoccaggi

Negli stoccaggi di warehouse, [!INCLUDE [prod_short](includes/prod_short.md)] suggerisce le righe di azione Posizione nell'unità di misura di stoccaggio. Ad esempio, potrebbe suggerire pezzi anche se gli articoli arrivano in un'unità di misura diversa.  

## <a name="breakbulk-in-movements"></a><a name="breakbulk-in-movements"></a><a name="breakbulk-in-movements"></a>Breakbulk relativo ai movimenti

[!INCLUDE [prod_short](includes/prod_short.md)] può anche eseguire breakbulk nei movimenti di rifornimento se l'interruttore **Permettere Breakbulk** nella pagina **Calcola rifornimento collocazione** è abilitato.  

I risultati del processo di conversione da un'unità di misura all'altra possono essere visualizzati come righe di breakbulk intermedie nelle istruzioni di stoccaggio, prelievo o movimento.  

> [!NOTE]  
> Se si seleziona il campo **Impostare filtro breakbulk** dell'intestazione delle istruzioni relative alla warehouse, le righe di breakbulk vengono automaticamente nascoste ogni volta che viene utilizzata l'intera unità di misura più grande. Se, ad esempio, un pallet è costituito da 12 pezzi e viene utilizzata l'intera unità di misura (12 pezzi), viene indicato di prelevare 1 pallet e posizionare 12 pezzi. Tuttavia, se devi selezionare solo 9 pezzi, le linee di breakbulk non sono nascoste, anche se hai selezionato il campo **Filtro breakbulk**. Le righe non sono nascoste perché devi mettere i tre pezzi rimanenti altrove nel magazzino.  

> [!NOTE]  
> Se si desidera ottimizzare l'impiego delle unità di misura nell'applicazione di warehouse, anche in concomitanza con l'utilizzo di breakbulk, si consiglia di eseguire le seguenti operazioni:  
>
> - Impostare l'unità di misura di base per un articolo sull'unità di misura minima che si prevede di gestire nelle attività di warehouse.  
> - Impostare unità di misura alternative per l'articolo utilizzando multipli dell'unità di base.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md) 
[Gestione assemblaggio](assembly-assemble-items.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
