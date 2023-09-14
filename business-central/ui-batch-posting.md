---
title: Registrare più documenti contemporaneamente
description: Informazioni su come selezionare più documenti non registrati in un elenco per la registrazione batch immediata o pianificata in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.reviewer: bholtorf
ms.date: 06/25/2021
ms.author: bholtorf
---
# Registrare più documenti contemporaneamente

Anziché registrare un singolo documento alla volta, è possibile selezionare più documenti non registrati in un elenco per una registrazione immediata o una registrazione batch programmata, ad esempio, per la fine della giornata. Ciò può essere utile se solo un supervisore può registrare documenti creati da altri utenti o per evitare problemi di prestazioni del sistema dovuti alla registrazione durante l'orario di lavoro.

## Per registrare immediatamente più ordini di acquisto

La seguente procedura descrive come registrare immediatamente più ordini di acquisto. I passaggi sono simili per tutti i documenti di acquisto e vendita.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Nella pagina **Ordini acquisto**, selezionare tutti gli ordini da registrare:
3. Nel campo **Nr.** selezionare i tre punti verticali per aprire il menu di scelta rapida, quindi scegliere il l'azione **Seleziona più elementi**.
4. Selezionare la casella di controllo per tutte le righe che rappresentano gli ordini che si desidera registrare contemporaneamente.
5. Scegliere l'azione **Registrazione** e quindi l'azione **Registra**.
6. Scegliere il pulsante **Sì** nel messaggio di conferma.

## Per eseguire registrazioni batch di ordini di acquisto

La seguente procedura descrive come eseguire registrazioni batch di ordini di acquisto. I passaggi sono simili per tutti i documenti di acquisto e vendita in cui l'azione **Registra batch** è disponibile.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
2. Nella pagina **Ordini acquisto**, selezionare tutti gli ordini da registrare:
3. Nel campo **Nr.** selezionare i tre punti verticali per aprire il menu di scelta rapida, quindi scegliere il l'azione **Seleziona più elementi**.
4. Selezionare la casella di controllo per tutte le righe che rappresentano gli ordini che si desidera registrare contemporaneamente.
5. Scegliere l'azione **Registrazione** e quindi l'azione **Registra batch**.
6. Nella pagina **Aggior. batch ordini acquisto**, riempire i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Scegliere il pulsante **OK**.
8. Per visualizzare potenziali problemi verificatisi durante la registrazione batch di documenti, aprire la pagina **Registro messaggi di errore**.

> [!NOTE]
> La registrazione di più documenti potrebbe richiedere tempo e bloccare altri utenti. Considerare l'abilitazione della registrazione in background. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## Per configurare la registrazione background con le code processi
Le code processi sono un efficace strumento per programmare l'esecuzione dei processi aziendali in background, ad esempio quando più utenti tentano di registrare gli ordini di vendita, ma un solo ordine può essere elaborato alla volta.  

La procedura seguente illustra come configurare la registrazione in background di ordini di vendita. I passaggi sono simili per un acquisto.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità clienti**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup contabilità clienti e vendite**, selezionare la casella di controllo **Registra mediante coda processi**.
3. Scegliere il campo **Codice categoria coda processi** e specificare il codice **SALESPOST**.

    > [!NOTE]
    > Alcuni processi modificano gli stessi dati e non devono essere eseguiti contemporaneamente perché possono causare conflitti. Ad esempio, i processi in background per i documenti di vendita proveranno a modificare gli stessi dati contemporaneamente. Le categorie della coda lavori aiutano a prevenire questo tipo di conflitti garantendo che quando un lavoro è in esecuzione, un altro lavoro appartenente alla stessa categoria di coda lavori non verrà eseguito fino al termine del primo. Ad esempio, un processo che appartiene a una categoria della coda lavori di vendita attenderà fino al completamento di tutti gli altri processi relativi alle vendite. Specificare una categoria di coda lavori nella scheda dettaglio **Registrazione background** della pagina **Setup contabilità clienti**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] fornisce le categorie delle code lavoro per vendite, acquisti e registrazioni di contabilità generale. Si consiglia di specificare sempre una di queste categorie o una creata dall'utente. Se si verificano errori dovuti a conflitti, prendere in considerazione la possibilità di impostare una categoria per le vendite, gli acquisti e la registrazione in background della contabilità generale.

    Se anche i documenti di vendita devono essere stampati al momento della registrazione, selezionare la casella di controllo **Registra e stampa mediante coda processi** nella pagina **Setup contabilità clienti e vendite**.  
    Se si seleziona **PDF** nel campo **Tipo di output report**, gli ordini di acquisto registrati correttamente saranno disponibili nella parte **Report elaborati** in Gestione ruolo utente.

    > [!IMPORTANT]  
    > Se si imposta un processo che prevede la registrazione e la stampa di documenti e nella stampante viene visualizzata una finestra di dialogo, ad esempio una richiesta di credenziali o un avvertimento sul basso livello di inchiostro della stampante, il documento viene registrato ma non stampato. Il movimento coda processi corrispondente alla fine incorre in un timeout e il campo **Stato** viene impostato su **Errore**. Di conseguenza, è consigliabile non utilizzare un setup di stampante che richieda l'interazione con la visualizzazione delle finestre di dialogo della stampante insieme alla registrazione in background.

    La prossima volta che si pubblicano documenti di vendita, [!INCLUDE [prod_short](includes/prod_short.md)] crea automaticamente una voce nella coda processi per ogni documento ed esegue i lavori in background, uno per uno.

4. Per verificare che la coda processi stia funzionando come previsto, registrare un ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
    Gli ordini vendita verranno ora aggiunti a un movimento coda processi dedicato, che definisce quando i documenti vengono registrati. 

### Per visualizzare lo stato di un documento di vendita o di acquisto
Se la coda processi non può registrare l'ordine di vendita, lo stato viene modificato in **Errore** e l'ordine di vendita viene aggiunto all'elenco degli ordini di vendita che l'utente deve gestire manualmente.
1. Dal documento che si è tentato di registrare con la registrazione in background, scegliere il campo **Stato coda processi**, che conterrà **Errore**.
2. Analizzare il messaggio di errore e correggere il problema.

In alternativa, è possibile verificare nella pagina **Voci log coda processi** se l'ordine di vendita è stato registrato correttamente. Per ulteriori informazioni, vedere la sezione [Monitorare la coda processi](#monitor-the-job-queue).

## Per creare un movimento coda processi per la registrazione batch di ordini di vendita

In alternativa, è possibile rimandare le registrazioni nelle ore in cui è conveniente per la propria organizzazione. Ad esempio, può avere senso nella propria l'attività commerciale eseguire determinate procedure quando si è conclusa la maggior parte dell'immissione dati del giorno. Per riuscirci, impostare la coda commesse sull'esecuzione di diversi report di registrazione tramite processo batch, come i report **Registra ordini vendite tramite processo batch**, **Registra fatture vendita tramite processo batch** e report simili. [!INCLUDE[prod_short](includes/prod_short.md)] supporta la registrazione in background per tutti i documenti di vendita, acquisto e assistenza.

La seguente procedura illustra come impostare il report **Registra batch ordini vendite** per registrare automaticamente gli ordini di vendita alle ore 16 nei giorni della settimana.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti coda processi**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Tipo oggetto da eseguire**, selezionare **Report**.  
4. Nel campo **ID oggetto da eseguire**, selezionare 296, **Registra batch ordini vendite**.

   È possibile anche utilizzare i seguenti report:
  
   * 900 **Aggior. batch ordini assemblaggio**
   * 497 **Agg. batch fatture acquisti**
   * 496 **Aggior. batch ordini acquisto**
   * 498 **Registrare nota cr. acquisti tramite processo batch**
   * 6665 **Batch registra ordini resi acq.**
   * 298 **Registrare le note di cr. vend. tramite processo batch**
   * 297 **Registra batch fatture vendita**
   * 296 **Registra batch ordini vendite**
   * 6655 **Batch reg. ordini resi vendita**
   * 6005 **Registra batch note cr. assistenza**
   * 6004 **Registra batch fatture assistenza**
   * 6001 **Batch ord. ass. registrati**

5. Selezionare la casella controllo **Pagina di richiesta report**.
6. Nella pagina di richiesta **Registra batch ordini vendite**, definire cosa includere durante la registrazione automatica di ordini di vendita quindi scegliere il pulsante **OK**.

    > [!IMPORTANT]
    > Ricordarsi di impostare filtri rigorosi; altrimenti, [!INCLUDE [prod_short](includes/prod_short.md)] pubblicherà tutti i documenti, anche se non sono pronti. Considerare l'idea di impostare un filtro sul campo **Stato** per il valore *Rilasciato* e un filtro sul campo **Data pubblicazione** per il valore *oggi*. Per ulteriori informazioni, vedere [Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md).
7. Selezionare tutte le caselle di controllo da **Esegui di Lunedì** a **Esegui di Venerdì**.
8. Nel campo **Ora inizio**, immettere 16.
9. Scegliere l'azione **Imposta stato su Pronto**.

Gli ordini di vendita entro i filtri definiti saranno registrati ogni giorno della settimana alle ore 16.

## Monitorare la coda processi

Se si imposta la pubblicazione in background con code processi, monitorare regolarmente la coda processi per rilevare eventuali problemi. È possibile tenere traccia dello stato nella pagina **Movimenti coda processi**. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).  

In qualità di amministratore, è possibile usare [Application Insights](/azure/azure-monitor/app/app-insights-overview) per raccogliere e analizzare i dati di telemetria da utilizzare per identificare i problemi. Per ulteriori informazioni, vedere [Monitoraggio e analisi della telemetria](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) nel contenuto per sviluppatori e amministratori.  

## Vedere anche

[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Modificare i documenti registrati](across-edit-posted-document.md)  
[Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]