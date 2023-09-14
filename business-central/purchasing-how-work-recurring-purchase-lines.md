---
title: Righe acquisto ricorrenti standard
description: Imposta le righe di acquisto più frequentemente usate e quindi inseriscile nei documenti di acquisto per compilare rapidamente le righe con informazioni standard.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: bholtorf
---
# Creare righe di acquisto ricorrenti

Se è spesso necessario creare righe di acquisto con informazioni simili, è possibile impostare righe standard da inserire nei documenti di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti.

## Impostare righe di acquisto ricorrenti

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Righe acquisto ricorrenti**, quindi scegli il collegamento correlato.
2. Nella pagina **Righe acquisto ricorrenti** scegli l'azione **Nuovo**.
3. Compilare i campi appropriati della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nella Scheda dettaglio **Righe**, immetti le informazioni nei campi che riflettono le righe standard che prevedi di utilizzare come righe ricorrenti nei documenti di acquisto.

> [!NOTE]
> Non è possibile definire i prezzi nelle righe di acquisto ricorrenti poiché prezzi, sconti e così via sono calcolati nei documenti di acquisto effettivi dopo l'inserimento delle righe di acquisto ricorrenti.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Assegnare righe di acquisto ricorrenti a un fornitore

Assegna una o più righe di acquisto ricorrenti a un fornitore di modo che sia possibile inserirle nei documenti di acquisto di quel fornitore.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Apri la scheda di un fornitore pertinente.
3. Scegli l'azione **Righe acquisto ricorrenti**.
4. Nella pagina **Righe acquisto ricorrenti**, seleziona i codici per le righe di acquisto ricorrenti che intendi inserire nei documenti di acquisto per il fornitore.
5. Compila gli altri campi per definire quando, come e dove le righe di acquisto ricorrenti devono essere utilizzate.
6. Nei quattro campi in cui hai scelto in che modo inserire le righe in ogni tipo di documento, seleziona una delle seguenti opzioni:

|Opzione|Descrizione|
|------|-----------|
|**Manuale**|È possibile cercare e inserire manualmente la riga di acquisto ricorrente esistente per il fornitore.|
|**Automatico**|Se esistono più righe di acquisto ricorrenti per il fornitore, viene visualizzata una notifica da cui è possibile selezionare quale inserire. Se esiste una sola riga di acquisto ricorrente, verrà inserita automaticamente.<br /><br />Ciò funziona solo se il nuovo documento è stato creato da un elenco di documenti, ad esempio selezionando l'azione **Nuovo** nella pagina **Ordini acquisto**. Non funziona se il documento è stato creato, ad esempio, da una scheda fornitore.|
|**Chiedi sempre**|Una notifica verrà visualizzata e tutte le righe di acquisto ricorrenti esistenti vengono visualizzate in modo che sia possibile selezionarne una.

## Inserire le righe di acquisto ricorrenti in una fattura di acquisto

Se esistono righe di acquisto ricorrenti per il fornitore, è possibile inserirle o aggiungerle automaticamente in tutti i tipi di documenti di acquisto come fattura di acquisto. Se hai attivato le opzioni **Chiedi sempre** per l'assegnazione delle righe di acquisto ricorrenti ai fornitori, verrai informato dell'esistenza di righe di acquisto ricorrenti.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.
2. Apri la fattura di acquisto in cui desideri inserire una più righe di acquisto standard.
3. Scegli l'azione **Ottieni righe acquisto ricorrenti**.
4. Nella pagina **Righe acquisto ricorrenti**, scegli il pulsante di ricerca nel campo **Codice** e seleziona una serie di righe di acquisto standard.
5. Scegli il pulsante **OK** per inserire le righe di acquisto standard nella fattura, in cui è possibile riutilizzare la riga così come è o modificarne le informazioni.

## Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Impostare gli acquisti](purchasing-setup-purchasing.md)  
[Creare vendite ricorrenti](sales-how-work-standard-lines.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]