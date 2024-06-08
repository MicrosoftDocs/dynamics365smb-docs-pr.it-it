---
title: Registrare e rettificare l'utilizzo e i prezzi delle risorse
description: 'Descrive come registrare l''utilizzo o il consumo di risorse associato a un progetto, per tenere traccia e gestire i costi, i prezzi e i tipi di lavoro.'
author: brentholtorf
ms.topic: how-to
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '201,206, 207, 271, 493'
ms.date: 02/22/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Uso delle risorse per i progetti

Si registra l'utilizzo di risorse nella registrazione progetti per tenere traccia dei costi, dei prezzi e dei tipi di lavoro che sono collegati ai progetti. Per ulteriori informazioni, vedi [Registrare l'utilizzo per i progetti](projects-how-record-job-usage.md).

> [!NOTE]
> Puoi inoltre acquistare risorse esterne, ad esempio, per fatturare a un fornitore per il lavoro eseguito. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).

Si può anche registrare l'utilizzo di una risorsa nelle registrazioni risorse. Le voci registrate nelle registrazioni risorse non influiscono sulla contabilità generale.

## Per assegnare risorse a progetti

È possibile assegnare risorse a progetti creando righe di pianificazione progetto per il progetto. Per ulteriori informazioni, vedi [Creare progetti](projects-how-create-jobs.md).

## Per registrare l'utilizzo delle risorse per un progetto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.
2. Apri il batch di registrazioni progetti pertinente e compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Una volta completate le registrazioni, scegliere l'azione **Registra**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Per rettificare i prezzi delle risorse

Se si desidera modificare i costi o i prezzi di un gran numero di risorse, si può usare un processo batch.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Rettifica costi/prezzi risorse**, quindi scegli il collegamento correlato.
2. Compilare i campi su una riga in base alle esigenze, quindi scegliere **OK**.

> [!NOTE]  
> Questo processo batch non consente di creare o rettificare costi e prezzi alternativi per le risorse. Modifica soltanto il contenuto del campo nella scheda risorsa per il campo **Rettifica campo** selezionato nel processo batch. Poiché la rettifica diventerà effettiva immediatamente per le risorse, controllare i fattori di rettifica prima di eseguire il processo batch.

## Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi esistenti

Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modifiche prezzi risorse**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Sugg. modif. prezzo ris. (prezzo)** e compilare i campi in base alle esigenze.
3. Scegliere il pulsante **OK**.  
4. Al termine del processo batch, i relativi risultati saranno visualizzati nella pagina **Modifiche prezzi risorsa**.

## Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi standard

Se si desidera impostare più prezzi di risorsa alternativi basati sui prezzi standard nelle schede risorse, è possibile utilizzare un processo batch .  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Modifiche prezzi risorse**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Sugg. mod. prezzo ris. (ris.)** e compilare i campi in base alle esigenze.  
3. Scegliere il pulsante **OK**.  
4. Al termine del processo batch, aprire la pagina **Modifiche prezzi risorsa** per visualizzarne i risultati.

## Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi

Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Sugg. mod. prezzo ris. (prezzo)**, quindi scegli il collegamento correlato.  
2. Compilare i campi, se necessario.
3. Scegliere il pulsante **OK**.  
4. Al termine del processo batch, aprire la pagina **Modifiche prezzi risorsa** per visualizzarne i risultati.

## Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)     
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]