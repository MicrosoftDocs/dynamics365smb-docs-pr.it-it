---
title: Monitorare lo stato di avanzamento e le prestazioni delle commesse
description: Descrive come creare un metodo semilavorati (WIP) e calcolare il WIP per stimare il valore finanziario delle commesse in corso.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.search.form: 89, 92, 1010
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f79829b3f227b6a5dcc94c95aa1aaf9826b3d7ce
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131287"
---
# <a name="monitor-job-progress-and-performance"></a>Monitorare lo stato di avanzamento e le prestazioni delle commesse
Durante lo svolgimento di una commessa, vengono consumati materiali, risorse ed effettuate altre spese che devono essere registrate nella commessa. La funzionalità WIP (Work in Process) consente di stimare il valore finanziario delle commesse nella contabilità generale nelle varie fasi di una commessa. In molti casi è possibile registrare le spese relative a una commessa prima di fatturarla. Se sono state registrate solo le spese, il rendiconto finanziario non sarà accurato. Per ulteriori informazioni, vedere [Metodi WIP](projects-understanding-wip.md).

Per tenere traccia del valore nella contabilità generale, è possibile calcolare il WIP e registrare il valore nella contabilità generale.

È possibile calcolare il WIP sulla base dei seguenti fattori:

* Valore costo
* Valore vendite
* Costo riconoscibile
* Percentuale di completamento
* Contratto completato

Se si desidera visualizzare il risultato utilizzando un metodo diverso, è possibile cambiare il metodo e ricalcolare il WIP. È possibile calcolare il WIP senza limitazioni. Il WIP viene solo calcolato ma non registrato nella contabilità generale. Dopo aver calcolato il WIP, è possibile effettuare la registrazione nella contabilità generale.

## <a name="to-create-a-job-wip-method"></a>Per creare un metodo WIP commessa
È possibile creare un metodo WIP commessa che corrisponda alle esigenze dell'organizzazione. Dopo averlo creato, è possibile impostarlo come metodo di default di calcolo del WIP commessa da utilizzare nella propria organizzazione.  

> [!NOTE]
> Dopo aver utilizzato il nuovo metodo per creare movimenti WIP, non è possibile eliminare il metodo o modificarlo.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Metodi WIP commessa**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Chiudere la pagina.   
4. Per rendere predefinito questo nuovo metodo, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup commesse**, quindi scegli il collegamento correlato.  
5. Nel campo **Metodo WIP di default** , selezionare il metodo dall'elenco.

## <a name="to-define-a-wip-method-for-a-job"></a>Per definire un metodo WIP per una commessa
Quando si crea una nuova commessa, è necessario specificare il metodo WIP commessa da applicare. In alcuni casi, il metodo WIP commessa che è possibile utilizzare viene impostata automaticamente come default.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commesse**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**. Per ulteriori informazioni, vedere [Creare le commesse](projects-how-create-jobs.md).  
3. Nella pagina **Scheda commessa**, nel campo **Metodo WIP**, selezionare un metodo WIP dall'elenco. Se è stato definito un metodo di default, è possibile selezionare un'altra opzione, se necessario.  

## <a name="to-calculate-wip"></a>Per calcolare il WIP
È possibile determinare l'importo WIP che deve essere registrato per i conti patrimoniali per il reporting di fine periodo. A tale scopo, utilizzare il processo batch **Commessa - Calcola WIP**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commessa - Calcola WIP**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Calcola WIP**.
3. Nella pagina **Commessa - Calcola WIP** compilare i campi in base alle esigenze.
4. Scegliere il pulsante **OK**.  

> [!NOTE]  
>   Il processo batch consente di calcolare il WIP. ma non registrato nella contabilità generale. A tale scopo, è necessario eseguire il processo batch **Registra WIP in C/G** dopo avere calcolato il WIP. Per ulteriori informazioni, vedere la seguente procedura.

## <a name="to-post-wip"></a>Per registrare il WIP
Dopo avere calcolato il WIP, è possibile registrarlo nei conti patrimoniali per il reporting di fine periodo. A tale scopo, utilizzare il processo batch **Commessa - Registra WIP in C/G**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commessa - Registra WIP in C/G**, quindi scegli il collegamento correlato.  
2. Nella pagina **Commessa - Registra WIP in C/G** compilare i campi in base alle esigenze.  
3. Scegliere il pulsante **OK**.

## <a name="to-calculate-and-post-job-completion-entries"></a>Per calcolare e registrare i movimenti di completamento della commessa
Al termine di tutte le operazioni di registrazione e fatturazione dell'utilizzo per una commessa, è necessario aggiornare la commessa in modo che il campo **Stato** sia impostato su **Completato**. Successivamente, è necessario stornare eventuali WIP registrati nella contabilità generale.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Selezionare una commessa aperta, quindi scegliere l'azione **Modifica**.
3. Nel campo **Stato** selezionare **Completato**.
4. Seguire i passaggi di assistenza per calcolare e registrare il WIP. In alternativa, seguire i passaggi 5 e 6 per effettuare questa operazione manualmente.  
5. Scegliere l'azione **Calcola WIP**.
6. Nella pagina **Commessa - Calcola WIP** compilare i campi in base alle esigenze.  

     Per i movimenti WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.  
7. Scegliere l'azione **Commessa - Registra WIP in C/G**.
8. Nella pagina **Commessa - Registra WIP in C/G** compilare i campi in base alle esigenze.  

     Per i movimenti C/G WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.

## <a name="to-view-job-ledger-entries"></a>Per visualizzare i movimenti contabili commesse
Tutti i movimenti correlati a una commessa vengono annotati nei registri commesse e numerati in sequenza a partire da 1. Dal registro commesse è possibile ottenere una panoramica di tutti i movimenti contabili della commessa.    

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri commesse**, quindi scegli il collegamento correlato.
2. Selezionare un registro appropriato quindi scegliere l'azione **Movimenti commesse**.

Nella pagina **Movimenti cont. commesse** è possibile esaminare le voci associate a qualsiasi commessa.  

## <a name="see-also"></a>Vedi anche
[Gestione di progetti](projects-manage-projects.md)
[Gestione costi di magazzino](finance-manage-inventory-costs.md)   
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
