---
title: Imposta più tassi di interesse per il pagamento ritardato
description: In questo argomento viene spiegato come calcolare gli addebiti di interessi con più tassi di interesse per un periodo specifico.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '6, 431, 432, 572'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Imposta più tassi di interesse per il pagamento ritardato

Puoi utilizzare diversi tassi di interesse in periodi differenti per pagamenti in ritardo nelle transazioni commerciali. [!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]

Ad esempio, un governo specifica il tasso di interesse massimo da imporre ai consumatori. Questo tasso di interesse può essere modificato due volte all'anno, il 1° gennaio e il 1° luglio. Il tasso di interesse tra le aziende (B2B) è concordato tra le parti e non è soggetto ad alcun limite. Il tasso annunciato è in genere superiore del quattro per cento all'interesse bancario normale.

Quando si creano le condizioni di addebito degli interessi e i termini di sollecito, per la penalità di pagamento ritardato, è possibile specificare più tassi di interesse in modo che la penalità sia calcolata in base a tassi di interesse differenti in diversi periodi.  

## Per impostare più tassi d'interesse

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Condiz. interessi finanziari**, quindi scegli il collegamento correlato.  
2. Nella pagina **Condiz. interessi finanziari**, selezionare le condizioni di addebito, quindi scegliere l'azione **Tassi di interesse**.  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere il pulsante **OK**.  
5. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Termini di sollecito**, quindi scegli il collegamento correlato.  
6. Nella pagina **Termini di sollecito**, selezionare i termini di sollecito, quindi scegliere l'azione **Livelli**.  
7. Nella pagina **Livelli di sollecito**, per i livelli di sollecito pertinenti, selezionare il campo **Calcola Interessi**.  

Quando si emette una nota di addebito interessi, la nota mostra gli addebiti di interessi con più tassi di interesse per un periodo di tempo specifico. La nota contiene anche dettagli relativi a contatti del cliente, società che ha emesso la nota, importo addizionale e importo totale. Il movimento di apertura nella nota è visualizzato in grassetto. Gli addebiti di interessi sono calcolati con più tassi di interesse per un periodo di tempo specifico e vengono stampati dopo il movimento di apertura della nota.  

## Vedere anche

[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]