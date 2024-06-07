---
title: Triangolazioni intracomunitarie
description: Questo argomento dell'articolo spiega come impostare e utilizzare le triangolazioni intracomunitarie dell'Unione europea (UE).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Triangolazioni intracomunitarie

Il commercio con terzi nell'Unione Europea (UE) si verifica quando ricevi una fattura di acquisto da un cliente in un paese/area geografica dell'UE e i prodotti vengono inviati in un altro paese/area geografica dell'UE senza entrare nel paese di residenza. L'importo della transazione può essere identificato e riportato separatamente per soddisfare i requisiti di dichiarazione dell'imposta sul valore aggiunto (IVA) e del sistema di scambio di informazioni sull'IVA (VIES) di alcuni paesi/regioni dell'UE. Microsoft Dynamics 365 Business Central consente di configurare le transazioni di acquisto come commercio di terzi nell'UE. Le transazioni di terze parti UE registrate possono essere filtrate nelle dichiarazioni IVA ed escluse dall'importo nella colonna **Vendite al cliente** del report **IVA - Dichiarazione su file**.

Anche se la funzione è preinstallata come estensione, non è attivata per impostazione predefinita. Eseguire la procedura seguente per attivare la funzionalità.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), , vai all'area di lavoro **Gestione funzionalità**, quindi seleziona il collegamento correlato.
2. Dall'elenco, trova e seleziona **Aggiornamento della funzionalità: sostituire la funzionalità di acquisto triangolazione intracomunitaria esistente con la nuova estensione di acquisto triangolazione intracomunitaria**.
3. Nella colonna **Abilitato per** seleziona **Tutti gli utenti**.

## Abilita la funzionalità di acquisto triangolazione intracomunitaria dell'UE per un acquisto

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Setup e-mail VAT**, quindi seleziona il collegamento correlato.
2. Nella pagina **Setup IVA**, contrassegna il campo **Abilita acquisto tra tre parti UE**.

## Utilizza la triangolazione intracomunitaria dell'UE

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), , immetti **Fatture di acquisto** (o un altro documento di acquisto), quindi scegli il collegamento correlato.
2. Seleziona una fattura di acquisto esistente o seleziona **Nuova** per crearne una nuova.
3. Nella Scheda dettaglio **Dettagli fattura**, seleziona la casella di controllo **Triangolazione intracomunitaria**.
4. Seleziona **OK**.

## Includi o escludi i record commerciali di terze parti dell'UE nella dichiarazione IVA

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), , immetti **Dichiarazione IVA**, quindi seleziona il collegamento correlato.
2. Nella pagina **Dichiarazione IVA**, seleziona una delle seguenti opzioni per mostrare i record commerciali di terze parti dell'UE utilizzando il campo **Triangolazione intracomunitaria**.

    | Opzione | Descrizione |
    |--------|-------------|
    | Tutto | Mostra tutti i record, indipendentemente dal fatto che il campo **Triangolazione intracomunitaria** nei documenti sia stato contrassegnato. |
    | UE3 | Mostra solo i record dove il campo **Triangolazione intracomunitaria** nei documenti è stato contrassegnato. |
    | Non UE3 | Mostra solo i record dove il campo **Triangolazione intracomunitaria** nei documenti non è stato contrassegnato. |


## Vedere anche
[Gestione contabile](finance.md)  
[Utilizzare Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
