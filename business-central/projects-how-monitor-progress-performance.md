---
title: Monitorare l'avanzamento e le prestazioni dei progetti
description: Descrive come creare un metodo semilavorati (WIP) e calcolare il WIP per stimare il valore finanziario dei progetti in corso.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---
# <a name="monitor-project-progress-and-performance"></a>Monitorare l'avanzamento e le prestazioni dei progetti

La funzionalità WIP (Work in Process) consente di stimare il valore finanziario dei progetti in corso nella contabilità generale.

Durante lo svolgimento di un progetto, vengono consumati materiali, risorse ed effettuate altre spese che devono essere registrate nel progetto. In molti casi è possibile che sia necessario registrare le spese per un progetto prima di fatturare. Se sono state registrate solo le spese, il rendiconto finanziario non sarà accurato. Per tenere traccia del valore effettivo del progetto, calcolare il WIP e registrarlo nella contabilità generale. Ulteriori informazioni su [Metodi WIP](projects-understanding-wip.md).

È possibile calcolare il WIP sulla base dei seguenti fattori:

* Valore coso
* Valore vendite
* Costo riconoscibile
* Percentuale di completamento
* Contratto completato

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-project-wip-method"></a>creare un metodo WIP progetto

Creare un metodo WIP progetto che corrisponda alle esigenze dell'organizzazione e impostarlo come predefinito.  

> [!NOTE]
> Dopo aver utilizzato il nuovo metodo per creare movimenti WIP, non è possibile modificarlo o eliminarlo.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Metodi WIP progetto**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Chiudere la pagina.   
4. Per rendere predefinito questo nuovo metodo, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup progetti**, quindi scegli il collegamento correlato.  
5. Nel campo **Metodo WIP di default** , selezionare il metodo dall'elenco.

## <a name="define-a-wip-method-for-a-project"></a>Definire un metodo WIP per un progetto

Quando si crea un nuovo progetto, è necessario specificare il metodo WIP progetto da applicare. In alcuni casi, il metodo WIP progetto utilizzato è già impostato come predefinito.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti** e scegli il collegamento relativo.
2. Scegli l'azione **Nuovo**. Per ulteriori informazioni vedere [Creare progetti](projects-how-create-jobs.md).  
3. Nella pagina **Scheda progetto**, nel campo **Metodo WIP**, selezionare un metodo WIP dall'elenco. Se è stato definito un metodo di default, è possibile selezionare un'altra opzione, se necessario.  

### <a name="define-a-wip-method-for-a-project-task"></a>Definire un metodo WIP per un'attività di progetto

Puoi definire un metodo WIP per un'attività di progetto, escludere alcune attività di progetto dal calcolo WIP o raggruppare le attività da calcolare insieme. 

Se si desidera calcolare il WIP per ciascuna attività di progetto individualmente, la registrazione WIP fornisce dimensioni definite per le attività specifiche.

**WIP-Totale** specifica le attività di progetto che si desidera raggruppare quando si calcola WIP e corrispettivo. In un gruppo di attività qualsiasi deve essere presente un'attività che soddisfi due condizioni:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Ha **WIP-Totale** impostato su *Totale*. Se non sono presenti attività di progetto con **WIP-Totale** impostato su *Totale*, *Totale* viene impostato automaticamente per l'ultima riga di attività di progetto quando il WIP viene calcolato per la prima volta.

* Ha il numero **Nr. attività di progetto** che è quello finale nel gruppo o nell'intervallo di attività di progetto.

Nella seguente tabella vengono illustrate tre opzioni:

| Campo | Descrizione |
|--|--|
| **\<blank\>** | Lasciare vuoto se lattività di progetto fa parte di un gruppo di attività. |
| **Totale** | Definisce l'intervallo o il gruppo di attività incluso nel calcolo di WIP e corrispettivo. Qualsiasi attività di progetto nel gruppo con **Tipo di attività di progetto** impostato su **Registrazione** è incluso nel totale WIP, a meno che il campo **WIP-Totale** dell'attività sia impostato su **Escluso**. |
| **Escluso** | Si applica solo a un'attività con impostato **NAV** come **Tipo di attività di progetto**, nel qual caso l'attività non viene inclusa quando vengono calcolati WIP e corrispettivo. |

Nell'esempio seguente, le attività di progetto sono divise in due raggruppamenti totali WIP, dimostrando come funziona il campo **WIP-Totale**:

|Nr. attività di progetto|Descrizione|Tipo di attività di progetto|Campo **WIP-Totale**|  
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

* Da *1000* a *1299*: il calcolo del WIP viene eseguito separatamente per questo gruppo di attività di progetto. Nota tuttavia che due delle attività, 1010 e 1110, sono escluse dal calcolo WIP perché il loro tipo di attività di progetto è **Registrazione**.

* Da *1300* a *1399*: il calcolo del WIP viene eseguito separatamente per questo gruppo di attività di progetto.

## <a name="calculate-wip"></a>Calcola WIP

È possibile determinare l'importo WIP che deve essere registrato per i conti patrimoniali per il reporting di fine periodo. A tale scopo, utilizzare il progetto batch **Progetto - Calcola WIP**.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetto - Calcola WIP**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Calcola WIP**.
3. Nella pagina **Progetto - Calcola WIP** compilare i campi in base alle esigenze.
4. Scegli il pulsante **OK**.  

> [!NOTE]  
> Il progetto batch calcola solo il WIP, ma non ne esegue la registrazione nella contabilità generale. Per registrarlo, è necessario eseguire il progetto batch **Registra WIP in C/G** dopo avere calcolato il WIP. Ulteriori informazioni nella procedura riportata di seguito.

## <a name="post-wip"></a>Registra WIP

Dopo avere calcolato il WIP, è possibile registrarlo nei conti patrimoniali per il reporting di fine periodo. A tale scopo, utilizzare il progetto batch **Progetto - Registra WIP in C/G**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetto - Registra WIP in C/G**, quindi scegli il collegamento correlato.  
2. Nella pagina **Progetto - Registra WIP in C/G** compilare i campi come necessario.  
3. Scegli il pulsante **OK**.

## <a name="calculate-and-post-project-completion-entries"></a>Calcolare e registrare movimenti di completamento di progetti

Al termine di tutte le operazioni di registrazione e fatturazione dell'utilizzo per un progetto, è necessario aggiornare lo stato del progetto di modo che sia **Completato**. Successivamente, è necessario stornare eventuali WIP registrati nella contabilità generale.

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti** e scegli il collegamento relativo.  
2. Selezionare un progetto aperto, quindi scegliere l'azione **Modifica**.
3. Nel campo **Stato** selezionare **Completato**.
4. Seguire i passaggi di assistenza per calcolare e registrare il WIP oppure seguire i passaggi 5 e 6 per farlo manualmente.  
5. Scegliere l'azione **Calcola WIP**.
6. Nella pagina **Progetto - Calcola WIP** compilare i campi in base alle esigenze.  

     Per i movimenti WIP progetto creati tramite l'esecuzione del processo batch la casella di controllo **Progetto completato** sarà selezionata, a indicare che si tratta di movimenti di completamento.  
7. Scegliere l'azione **Registra WIP in C/G**.
8. Nella pagina **Progetto - Registra WIP in C/G** compilare i campi come necessario.  

     Per i movimenti C/G WIP progetto creati tramite l'esecuzione del progetto batch la casella di controllo **Progetto completato** sarà selezionata, a indicare che si tratta di movimenti di completamento.

## <a name="view-project-ledger-entries"></a>Visualizzare movimenti contabili progetto

Tutti i movimenti correlati a un progetto vengono registrati nei registri progetti e numerati in sequenza a partire da 1. Dal registro progetti è possibile ottenere una panoramica di tutti i movimenti contabili progetto.    

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri progetti**, quindi scegli il collegamento correlato.
2. Selezionare un registro pertinente quindi scegliere l'azione **Contabilità progetti**.

Nella pagina **Movimenti contabili progetto** è possibile esaminare i movimenti associate a qualsiasi progetto.  

## <a name="see-also"></a>Vedere anche

[Procedura dettagliata: Calcolo del valore WIP per un progetto](walkthrough-calculating-work-in-process-for-a-job.md)
[Gestione di progetti](projects-manage-projects.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
