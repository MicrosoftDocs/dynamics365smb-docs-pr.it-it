---
title: Creare nuove voci di valore per gli articoli nell'inventario | Microsoft Docs
description: Descrive come rivalutare o ammortizzare i movimenti di valorizzazione di uno o più articoli in magazzino registrandone il corrente valore calcolato.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Rivalutare l'inventario
Per rivalutare o ammortizzare un determinato articolo o movimento contabile articolo, è necessario utilizzare le registrazioni rivalutazioni.

## Per rivalutare il magazzino
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni rivalutazioni**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Calcola valore magazzino**.
3. Nella pagina **Calcola valore magazzino** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegli il pulsante **OK**.
5. In ogni riga della pagina  **Giornali di rivalutazione articoli**, nel campo  **Costo unitario (rivalutato)**, immettere il nuovo costo unitario. In alternativa, immettere il nuovo importo totale nel campo **Costo unitario (rivalutato)**.

    I dati pertinenti vengono automaticamente aggiornati. Il campo  **Importo** mostra la variazione effettiva del valore dell'inventario per la voce contabile dell'articolo selezionato. Calcola la differenza tra il campo **Valore Magazzino (Calcolato)** e il campo **Valore Magazzino (Rivalutato)**.
6. Una volta completate tutte le righe nelle registrazioni rivalutazioni, scegliere l'azione **Registra**.

Vengono a questo punto creati i nuovi movimenti di valorizzazione che riflettono le rivalutazioni registrate. È possibile visualizzare i nuovi valori nelle rispettive schede articolo.

## Vedere anche
[Dettagli di progettazione: rivalutazione](design-details-revaluation.md)    
[Magazzino](inventory-manage-inventory.md)    
[Vendite](sales-manage-sales.md)    
[Acquisti](purchasing-manage-purchasing.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]