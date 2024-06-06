---
title: Assemblaggio su progetto
description: Scopri come utilizzare l'assemblaggio su ordine per un progetto.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="assemble-to-project"></a>Assemblaggio su progetto

L'assemblaggio su progetto ti aiuta a migliorare la gestione dell'inventario eseguendo l'assemblaggio su ordine solo quando è richiesto.

Quando scegli un articolo di assemblaggio su ordine in una riga di pianificazione progetto, [!INCLUDE [prod_short](includes/prod_short.md)] crea un ordine di assemblaggio. L'ordine di assemblaggio è basato sulla riga di pianificazione progetto e le relative righe sono basate sulla distinta base di assemblaggio dell'articolo. Per ulteriori informazioni sulle distinte materiali di assemblaggio, vai a [Utilizzare le distinte materiali di assemblaggio](assembly-how-work-assembly-boms.md). La quantità di componenti nella distinta base di assemblaggio viene moltiplicata per la quantità dell'ordine. La pagina **Righe assemblaggio su ordine** mostra i dettagli sulle righe dell'ordine di assemblaggio collegate. I dettagli possono aiutarti a personalizzare l'articolo di assemblaggio. Come in Sales, non è possibile registrare direttamente ordini di assemblaggio collegati. Per ulteriori informazioni sugli ordini di assemblaggio, vedi [Vendere gli articoli di magazzino nei flussi di assemblaggio su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Gli ordini di assemblaggio sono riservati ai progetti e [!INCLUDE [prod_short](includes/prod_short.md)] sincronizza la tracciabilità degli articoli tra le righe di pianificazione progetto e l'ordine di assemblaggio.

## <a name="integrate-with-warehouse-management"></a>Eseguire l'integrazione con la gestione warehouse

Assemblaggio su progetto si integra con le funzionalità di gestione warehouse per facilitare l'assemblaggio e la spedizione. Il processo aiuta inoltre a garantire che il flusso di assemblaggio su consegna del progetto si svolga senza intoppi nei processi di warehouse interni. Per ulteriori informazioni sui flussi di warehouse interni per progetti, vedi [Flussi per produzione, assemblaggio e processi](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

La seguente tabella descrive le configurazioni di warehouse supportate dall'assemblaggio su ordine.

|Configurazione  |Descrizione  |
|---------|---------|
|**Nessuna gestione della warehouse**|Utilizza una registrazione progetti per registrare l'utilizzo completo o parziale. L'output e il consumo dei componenti vengono registrati automaticamente per l'ordine di assemblaggio.         |
|**Prelievo inventario**|Utilizza un prelievo inventario per registrare l'utilizzo completo o parziale. L'output e il consumo dei componenti vengono registrati automaticamente per l'ordine di assemblaggio.          |
|**Prelievo warehouse**|Crea e registra prelievi warehouse per i componenti, quindi utilizza una registrazione progetti per registrare l'utilizzo. [!INCLUDE [prod_short](includes/prod_short.md)] verifica se i componenti di assemblaggio consumati sono stati prelevati. L'output e il consumo dei componenti vengono registrati automaticamente per l'ordine di assemblaggio.         |

## <a name="known-limitations"></a>Limitazioni note

In questa sezione vengono descritte le limitazioni note per l'assemblaggio su progetto.

* Il campo **Quantità per assemblaggio su ordine** non è disponibile per i progetti chiusi.
* Per gli scenari di prelievo warehouse, la **Quantità per assemblaggio su ordine** può essere zero o uguale alla quantità. Non puoi combinare l'assemblaggio su ordine e l'assemblaggio per magazzino in una riga di pianificazione progetto. Devi creare righe di pianificazione progetto distinte.
* L'assemblaggio su ordine non influisce sulle parti fatturabili di un progetto. Un assemblaggio è incluso nelle fatture di vendita, ma non i relativi componenti. Non puoi modificare il campo **Quantità per assemblaggio su ordine** per le righe fatturabili.
* La pianificazione degli ordini e il prospetto di pianificazione non sono interessati poiché il progetto costituisce l'input per la pianificazione. Il motore di pianificazione considera l'assemblaggio come domanda.
* Non puoi inserire una quantità negativa nel campo **Quantità per assemblaggio su ordine**.
* Non è possibile annullare un assemblaggio.

## <a name="see-also"></a>Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Creare commesse](projects-how-create-jobs.md)
