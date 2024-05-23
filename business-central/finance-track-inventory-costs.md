---
title: Tenere traccia delle rettifiche dei costi degli articoli
description: Scopri come le rettifiche di tracciabilità dei costi degli articoli possono aiutarti a mantenere accurati i dati sui costi degli articoli.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="track-item-cost-adjustments"></a>Tenere traccia delle rettifiche dei costi degli articoli

È importante mantenere accurati i costi degli articoli e ridurre il tempo che intercorre tra il momento in cui registri un movimento e il momento in cui il costo viene riportato nella contabilità generale. Puoi tenere traccia delle prestazioni delle rettifiche dei costi per singole esecuzioni e articoli di rettifica. Se si verificano degli errori, puoi identificare gli elementi problematici e apportare correzioni. Ad esempio, puoi escludere gli articoli dai calcoli per garantire che le rettifiche non vengano interrotte per altri articoli. Puoi rettificare i costi per singoli articoli oppure creare batch di articoli e rettificarli tutti contemporaneamente.

## <a name="start-tracking-cost-adjustments"></a>Avviare la tracciabilità delle rettifiche dei costi

È facile iniziare. Nella pagina **Setup magazzino**, il campo **Registrazione rettifica costi** offre alcune opzioni:

* **Disabilitato** significa che non vengono registrate le esecuzioni di rettifica dei costi.
* **Solo errori** significa registrare solo le esecuzioni non riuscite.
* **Tutto** significa registrare tutte le esecuzioni.

> [!NOTE]
> Per ridurre al minimo la dimensione del registro, [!INCLUDE [prod_short](includes/prod_short.md)] non registra le rettifiche che avvengono automaticamente quando qualcuno registra un articolo.

Devi inoltre impostare il movimento nella coda di processi **Registra costo magazzino in C/G (1002)**. Questo movimento della coda di processi rettifica automaticamente i costi in base a una pianificazione. Per ulteriori informazioni sui movimenti della coda di processi, vedi [Usare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md).

## <a name="manage-cost-adjustments"></a>Gestire le rettifiche dei costi

Utilizza la pagina **Rettifica costo inventario** per gestire e monitorare il processo di rettifica dei costi. In questa pagina vengono visualizzati gli articoli insieme ai relativi parametri di costing e allo stato di rettifica dei costi. Puoi filtrare l'elenco per concentrarti sugli articoli che richiedono una rettifica o che sono esclusi dal processo di rettifica dei costi.

### <a name="about-item-batches"></a>Informazioni su batch di articoli

Puoi eseguire la rettifica dei costi per diversi articoli raggruppandoli in batch. I batch semplificano la rettifica separata di alcuni articoli, ad esempio perché la relativa rettifica richiede più tempo. I batch possono anche aiutare a identificare gli articoli che presentano problemi.

Per creare un batch, nella pagina **Rettifica costo inventario**, effettuare una delle seguenti operazioni:

* Seleziona gli articoli nell'elenco, scegli **Esegui rettifica costi**, quindi scegli **Aggiungi batch**.
* Per creare un batch ed eseguire immediatamente la rettifica dei costi, seleziona gli elementi nell'elenco, scegli **Esegui rettifica costi**, quindi scegli **Aggiungi batch ed esegui**.
* Scegli **Esegui rettifica costi**, scegli **Batch di articoli**, quindi inserisci un filtro nel campo **Filtro articolo**.
  
> [!TIP]
> Per creare rapidamente un altro batch per tutti gli articoli che non sono già inclusi in un batch, nella pagina **Rettifica costo - Batch articoli**, scegli **Aggiungi articoli mancanti**.

Al termine dell'esecuzione di un batch, il batch presenta uno dei seguenti stati nella pagina **Batch di articoli**:

* **Riuscito**: la rettifica dei costi ha avuto esito positivo.
* **Non riuscito**: se la rettifica dei costi non riesce, [!INCLUDE [prod_short](includes/prod_short.md)] identifica l'articolo che ha causato l'errore e quindi divide il batch corrente in due. Un batch con l'articolo problematico e un altro con gli articoli rimanenti. La rettifica dei costi viene eseguita di nuovo per il batch con gli articoli rimanenti. Se ha di nuovo un esito negativo, il processo viene ripetuto. Sei tu a definire il numero massimo di divisioni nel campo **Max. tentativi**. Il valore predefinito per i tentativi è 10, ma è possibile immettere un nuovo limite.
* **Timeout**: se la rettifica dei costi per un batch non termina entro il periodo specificato nel campo **Timeout (minuti)** (compreso tra 1 e 720 minuti), la sessione termina e viene eseguito il rollback delle modifiche. [!INCLUDE [prod_short](includes/prod_short.md)] quindi divide il batch corrente a metà ed esegue nuovamente il processo di rettifica dei costi per ciascuna metà. Questo processo continua fino a che la rettifica dei costi non ha esito positivo o raggiunge il numero massimo di tentativi.

> [SUGGERIMENTO!] Ogni batch viene eseguito in una sessione separata. Per monitorare l'avanzamento, utilizza l'azione **Aggiorna**.

### <a name="run-cost-adjustment"></a>Esegui rettifica costi

Utilizza la pagina **Rettifica costo inventario** per apportare modifiche.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Rettifica costo inventario**, quindi scegli il collegamento correlato.
1. A seconda di cosa vuoi fare, utilizza una delle seguenti opzioni:

  * Per uno o più articoli immediatamente, seleziona gli articoli nell'elenco e quindi scegli **Esegui rettifica costi**.
  * Per i batch, utilizza una delle seguenti opzioni:

    * Per creare un batch e rettificare i costi immediatamente, scegli gli elementi nell'elenco, scegli **Esegui rettifica costi**, quindi scegli **Aggiungi batch ed esegui**.
    * Per eseguirlo per tutti i batch, seleziona **Esegui rettifica costi**, **Batch di articoli**, quindi scegli **Esegui**.
    
    Per ulteriori informazioni sui batch, vedi [Informazioni di batch di articoli](#about-item-batches).

### <a name="explore-item-details"></a>Esplorare i dettagli degli articoli

Utilizza il menu **Articolo** per accedere alle informazioni sulle rettifiche dei costi per un articolo selezionato.

* **Movimenti contabili articolo**: elenca i movimenti per l'articolo. L'azione **Contrassegna per rettifica** ti consente di forzare la riesecuzione della rettifica dei costi per gli articoli direttamente o indirettamente collegati ai movimenti in entrata che selezioni. Forzare una nuova esecuzione può essere utile se le esecuzioni precedenti hanno portato a costi errati.
* **Movimenti valorizzazione**: elenca i movimenti di valorizzazione per l'articolo.
* **Punti di ingresso rettifica costi**: apri la pagina **Rettifica costo medio cod. spedizioni Intrastat**, utilizzata principalmente per calcolare il costo medio. Nella pagina vengono visualizzate combinazioni di articoli, ubicazioni, varianti e date di valutazione per le quali le rettifiche dei costi vengono o devono essere eseguite.
* **Ordini di rettifica costi**: apri la pagina **Movimento di rettifica inventario**, in cui rettifichi gli ordini di produzione e di assemblaggio. Mostra che gli ordini sono stati rettificati o che richiedono una rettifica.

### <a name="view-the-outcome"></a>Visualizzare il risultato

Utilizza il menu **Log per** per visualizzare il risultato delle rettifiche dei costi:

* **Esegui**: mostra i registri di rettifica dei costi per ogni esecuzione. Il registro include dati su filtro degli articoli, stato (Riuscito/Non riuscito/Timeout), data/ora di inizio e fine, durata e differenze di costo generate dall'esecuzione.
* **Articolo**: mostra informazioni dettagliate sul processo di rettifica per l'articolo selezionato.

### <a name="include-or-exclude-items-from-adjustments"></a>Includere o escludere articoli dalle rettifiche

Se uno o più articoli non riescono, è possibile escluderli dall'esecuzione della rettifica e quindi includerli nelle esecuzioni successive. Nel menu **Funzioni**, scegli una delle seguenti opzioni:

* **Escludi articolo da rettifica** e **Includi articolo nella rettifica**: disabilita temporaneamente e quindi riabilita la rettifica dei costi per un articolo selezionato. La rettifica dei costi continua a mantenere accurati i costi per altri articoli mentre esamini un problema con un articolo specifico.

## <a name="post-adjusted-costs-to-the-general-ledger"></a>Registrare i costi rettificati nella contabilità generale

In genere, i nuovi movimenti di valorizzazione vengono registrati nella contabilità generale in base alla pianificazione per il movimento della coda di processi **Registra costo magazzino in C/G (1002)**. Tuttavia, puoi registrare immediatamente le rettifiche nella contabilità generale dalla pagina **Rettifica costo inventario**. Nel menu **Funzioni**, scegli **Registra costo magazzino in C/G**.

## <a name="troubleshoot-cost-adjustments"></a>Risolvere i problemi relativi alle rettifiche dei costi

Utilizza le seguenti opzioni nel menu **Diagnostica** per risolvere i problemi relativi alle esecuzioni di rettifica dei costi.

* **Esporta dati articolo**: esporta i dati relativi all'articolo in un file di testo. Puoi utilizzare il file per ulteriori analisi in un ambiente sandbox o allegarlo a una richiesta di supporto durante l'analisi dei problemi di calcolo dei costi.
* **Importa dati articolo**: importa nuovamente nel database il file di testo precedentemente esportato. Questa azione è abilitata solo in ambienti sandbox o società di valutazione.
* **Ripristina costo rettificato**: reimposta l'interruttore **Costo rettificato** su articoli, ordini di produzione o ordini di assemblaggio. Questa impostazione consente di forzare la riesecuzione della rettifica dei costi per tali elementi.
* **Report Rilevamento problemi di costing**: diagnostica problemi tipici relativi ai dati che causano errori di calcolo nei costi. Verifica se i movimenti contabili articoli, i movimenti di valorizzazione, i movimenti di collegamento articolo e i movimenti contabili di capacità sono corretti.
* **Elimina dati articolo**: cancella tutte le tabelle relative agli articoli nel database. Questa azione è disponibile solo in ambienti sandbox o società di valutazione.

## <a name="see-also"></a>Vedere anche

[Rettificare i costi degli articoli](inventory-how-adjust-item-costs.md)  
[Dettagli di progettazione: rettifica costo](design-details-cost-adjustment.md)  
