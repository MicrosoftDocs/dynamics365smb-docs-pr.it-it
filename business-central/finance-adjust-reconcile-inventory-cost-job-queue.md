---
title: Programmare i lavori per regolare e riconciliare il costo dell'inventario
description: 'Informazioni su come utilizzare la coda processi per spostare in background le attività per la rettifica del costo di magazzino o per riconciliarlo con la contabilità generale. Ad esempio, se la tua società esegue molte attività o elabora molte transazioni.'
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 09/23/2021
ms.author: bholtorf
---
# <a name="schedule-jobs-for-adjusting-and-reconciling-inventory-cost-with-the-general-ledger"></a>Programmare i lavori per aggiustare e riconciliare il costo dell'inventario con la contabilità generale

Per ottimizzare l'esperienza, la rettifica automatica dei costi e la registrazione nella contabilità generale sono attivate per impostazione predefinita. Tuttavia, poiché i dati si accumulano nel tempo, ciò potrebbe influire sulle prestazioni. Per ridurre il carico sull'applicazione, può essere utile usare i movimenti della coda processi per spostare in background le attività da eseguire.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Spostare in background l'attività di rettifica dei costi degli articoli con l'aiuto del setup assistito

La creazione di movimenti della coda processi può essere complicata, anche per un consulente esperto, quindi abbiamo una guida di installazione assistita per semplificare il processo di rettifica dei costi degli articoli.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immettere **Setup magazzino** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Setup magazzino**, disattivare il campo **Reg. automatica costi** oppure specificare **Mai** nel campo **Rettifica costo automatica**.  
3. Nella notifica che ora viene visualizzata nella parte superiore della pagina, scegliere il collegamento **Pianifica movimento coda processi**. Questo apre la guida all'impostazione assistita di **Adeguamento e registrazione dei costi del programma** .  
4. Specificare l'attività da pianificare.  

  > [!NOTE]
  > Non è possibile creare un nuovo movimento della coda processi se esiste già un movimento della coda processi per l'attività specificata.

5. Selezionare il campo **Visualizzare i movimenti della coda processi al termine dell'operazione** per rivedere e regolare le impostazioni. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>Creare un movimento di coda processi per la rettifica e la riconciliazione manuale dei costi di magazzino

In alternativa, è possibile creare manualmente i movimenti di coda processi. La procedura seguente mostra come impostare il processo batch **Rettifica costo - Mov. art.** da eseguire automaticamente ogni giorno, ma gli stessi passaggi si applicano al processo batch **Registra costo magazzino in C/G**.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immettere **Movimenti coda processi** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Tipo oggetto da eseguire**, scegliere *Report*.  
4. Nel campo **ID oggetto da eseguire**, scegliere *795*, **Rettifica costo - Mov. art.**.  
5. Nel campo **Prossima esecuzione formula della data**, immettere *1D*.
6. Nel campo **Ora inizio**, immettere *2 AM*.
7. Scegliere l'azione **Imposta stato su Pronto**.

Ora, il costo dell'inventario verrà aggiornato ogni notte.  

Per pianificare un'attività per la riconciliazione dell'inventario con la contabilità generale, scegliere il codeunit 2846 **Registra costo magazzino in C/G**.

> [!TIP]
> Per evitare il blocco, non pianificate le attività per il lavoro batch **Rettifica costo movimenti articoli**, **Registra costo magazzino in C/GL** codeunit, e le attività per la registrazione delle transazioni di vendita o di acquisto allo stesso tempo. Inoltre, assicuratevi che usino la stessa categoria di coda di lavoro.

## <a name="see-also"></a>Vedere anche

[Rettifica costi articolo](inventory-how-adjust-item-costs.md)  
[Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Utilizzare [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
