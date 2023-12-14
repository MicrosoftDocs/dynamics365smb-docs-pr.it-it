---
title: Monitorare lo stato di avanzamento e le prestazioni delle commesse
description: Descrive come creare un metodo semilavorati (WIP) e calcolare il WIP per stimare il valore finanziario delle commesse in corso.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# <a name="monitor-job-progress-and-performance"></a>Monitorare lo stato di avanzamento e le prestazioni delle commesse

La funzionalità WIP (Work in Process) consente di stimare il valore finanziario delle commesse nella contabilità generale.

Durante lo svolgimento di una commessa, vengono consumati materiali, risorse ed effettuate altre spese che devono essere registrate nella commessa. In molti casi è possibile registrare le spese relative prima di fatturare. Se sono state registrate solo le spese, il rendiconto finanziario non sarà accurato. Per tenere traccia del valore effettivo del lavoro, calcolare il WIP e registrarlo nella contabilità generale. Ulteriori informazioni su [Metodi WIP](projects-understanding-wip.md).

È possibile calcolare il WIP sulla base dei seguenti fattori:

* Valore coso
* Valore vendite
* Costo riconoscibile
* Percentuale di completamento
* Contratto completato

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-job-wip-method"></a>Creare un metodo WIP commessa

Creare un metodo WIP commessa che corrisponda alle esigenze dell'organizzazione e impostarlo come predefinito.  

> [!NOTE]
> Dopo aver utilizzato il nuovo metodo per creare movimenti WIP, non è possibile modificarlo o eliminarlo.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Metodi WIP commessa**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Chiudere la pagina.   
4. Per rendere predefinito questo nuovo metodo, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup commesse**, quindi scegli il collegamento correlato.  
5. Nel campo **Metodo WIP di default** , selezionare il metodo dall'elenco.

## <a name="define-a-wip-method-for-a-job"></a>Definire un metodo WIP per una commessa

Quando si crea una nuova commessa, è necessario specificare il metodo WIP commessa da applicare. In alcuni casi, il metodo WIP del lavoro utilizzato è già impostato come predefinito.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**. Ulteriori informazioni in [Crea lavori](projects-how-create-jobs.md).  
3. Nella pagina **Scheda commessa**, nel campo **Metodo WIP**, selezionare un metodo WIP dall'elenco. Se è stato definito un metodo di default, è possibile selezionare un'altra opzione, se necessario.  

### <a name="define-a-wip-method-for-a-job-task"></a>Definire un metodo WIP per una commessa

Puoi definire un metodo WIP per un'attività commessa, escludere alcune attività dal calcolo WIP o raggruppare le attività da calcolare insieme. 

Se desideri calcolare il WIP per ciascuna attività individualmente, la registrazione WIP fornisce dimensioni definite per le attività specifiche.

**WIP-Totale** specifica le attività commesse che si desidera raggruppare quando si calcola WIP e Corrispettivo. In un gruppo di attività qualsiasi deve essere presente un'attività che soddisfi due condizioni:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Ha **WIP-Totale** impostato su *Totale*. Se non sono presenti task commesse con **WIP-Totale** impostato su *Totale*, *Totale* viene impostata automaticamente quando WIP viene calcolato per la prima volta.

* Disporre di un numero **Nr. task commessa** finale nel gruppo o nell'intervallo di task commesse.

Nella seguente tabella vengono illustrate tre opzioni:

| Campo | Descrizione |
|--|--|
| **\<blank\>** | Lasciare vuota se l'attività commessa fa parte di un gruppo di attività. |
| **Totale** | Definisce l'intervallo o il gruppo di attività incluso nel calcolo di WIP e corrispettivo. Qualsiasi attività commessa all'interno del gruppo con **Tipo task commessa** impostato su **Registrazione** è incluso nel totale WIP, a meno che il relativo campo **WIP-Totale** dell'attività sia impostato su **Escluso**. |
| **Escluso** | Si applica solo a un'attività con **Tipo task commessa** di **NAV**, nel qual caso l'attività non viene inclusa quando vengono calcolati WIP e riconoscimento. |

Nell'esempio seguente, le attività lavorative sono divise in due raggruppamenti totali WIP, dimostrando come funziona il campo **WIP-Totale**:

|Nr. task commessa|Descrizione|Tipo task commessa|Campo **WIP-Totale**|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Preparazione|Inizio-Totale|\<blank\>|
|1010|.    Pulizia|Registrazione|**Escluso**|
|1099|Preparazione totale|Fine-Totale|\<blank\>|
|1100|Applicazione tappeto|Inizio-Totale|\<blank\>|
|1110|.    Applicazione di colla sul pavimento|Registrazione|**Escluso**|
|1120|.    Stesura tappeto|Registrazione|\<blank\>|
|1199|Applicazione tappeto totale|Fine-Totale|\<blank\>|
|1200|Fine|Inizio-Totale|\<blank\>|
|1210|.    Pulizia con aspirapolvere del tappeto|Registrazione|\<blank\>|
|1299|Finitura totale|Fine-Totale|**Totale**|
|1300|Correzione errori|Inizio-Totale|\<blank\>|
|1310|.    Correzione errori|Registrazione|\<blank\>|
|1399|Correzione errori totale|Fine-Totale|**Totale**|

Noterai:

* Da *1.000* a *1.299*: il calcolo WIP verrà eseguito separatamente per questo gruppo di attività commessa. Nota tuttavia che due delle attività, 1.010 e 1.110, sono escluse dal calcolo WIP perché il loro tipo di attività lavorativa è **Registrazione**.

* Da *1.300* a *1.399*: il calcolo WIP verrà eseguito separatamente per questo gruppo di attività commessa.

## <a name="calculate-wip"></a>Calcola WIP

È possibile determinare l'importo WIP che deve essere registrato per i conti patrimoniali per il reporting di fine periodo. Utilizzare il processo batch **Commessa - Calcola WIP**.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commessa - Calcola WIP**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Calcola WIP**.
3. Nella pagina **Commessa - Calcola WIP** compilare i campi in base alle esigenze.
4. Scegli il pulsante **OK**.  

> [!NOTE]  
>   Il processo batch calcola solo il WIP, ma non di eseguirne la registrazione nella contabilità generale. Per registrarlo, è necessario eseguire il processo batch **Registra WIP in C/G** dopo avere calcolato il WIP. Ulteriori informazioni nella procedura riportata di seguito.

## <a name="post-wip"></a>Registra WIP

Dopo avere calcolato il WIP, è possibile registrarlo nei conti patrimoniali per il reporting di fine periodo. A tale scopo, utilizzare il processo batch **Commessa - Registra WIP in C/G**.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commessa - Registra WIP in C/G**, quindi scegli il collegamento correlato.  
2. Nella pagina **Commessa - Registra WIP in C/G** compilare i campi in base alle esigenze.  
3. Scegli il pulsante **OK**.

## <a name="calculate-and-post-job-completion-entries"></a>Calcolare e registrare i movimenti di completamento della commessa

Al termine di tutte le operazioni di registrazione e fatturazione dell'utilizzo per una commessa, è necessario aggiornare la commessa in modo che il campo **Stato** sia impostato su **Completato**. Successivamente, è necessario stornare eventuali WIP registrati nella contabilità generale.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Selezionare una commessa aperta, quindi scegliere l'azione **Modifica**.
3. Nel campo **Stato** selezionare **Completato**.
4. Seguire i passaggi di assistenza per calcolare e registrare il WIP. In alternativa, segui i passaggi 5 e 6 per effettuare questa operazione manualmente.  
5. Scegliere l'azione **Calcola WIP**.
6. Nella pagina **Commessa - Calcola WIP** compilare i campi in base alle esigenze.  

     Per i movimenti WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.  
7. Scegliere l'azione **Commessa - Registra WIP in C/G**.
8. Nella pagina **Commessa - Registra WIP in C/G** compilare i campi in base alle esigenze.  

     Per i movimenti C/G WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.

## <a name="view-job-ledger-entries"></a>Visualizzare i movimenti contabili commesse

Tutti i movimenti correlati a una commessa vengono annotati nei registri commesse e numerati in sequenza a partire da 1. Dal registro commesse è possibile ottenere una panoramica di tutti i movimenti contabili della commessa.    

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri commesse**, quindi scegli il collegamento correlato.
2. Selezionare un registro appropriato quindi scegliere l'azione **Movimenti commesse**.

Nella pagina **Movimenti cont. commesse** è possibile esaminare le voci associate a qualsiasi commessa.  

## <a name="see-also"></a>Vedere anche

[Procedura dettagliata: Calcolo del valore WIP per una commessa](walkthrough-calculating-work-in-process-for-a-job.md)
[Gestione di progetti](projects-manage-projects.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
