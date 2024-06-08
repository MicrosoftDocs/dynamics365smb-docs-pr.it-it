---
title: 'Prelevare o spostare articoli per produzione, assemblaggio o commesse in configurazioni warehouse di base'
description: 'Quando l''ubicazione della warehouse richiede l''elaborazione dei prelievi ma non delle spedizioni, usa la pagina Prelievi magazzino per registrare il prelievo di componenti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Prelevare per produzione, assemblaggio o commesse in configurazioni di warehouse di base

La modalità di stoccaggio dei componenti di prelievo per le commesse, gli ordini di produzione o di assemblaggio dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

In una configurazione warehouse di base per il flusso in uscita (prelievo), attiva l'interruttore **Richiesto prelievo** nella pagina **Scheda ubicazione** per l'ubicazione ma disattiva l'interruttore **Richiesta spedizione**.

Usa i seguenti documenti per le operazioni interne:

* Prelievi magazzino
* Movimento di magazzino

## <a name="inventory-picks"></a>Prelievi magazzino

* Quando si registra un prelievo da magazzino per un'operazione interna, come la produzione o una commessa, il consumo dei componenti prelevati viene registrato contemporaneamente.
* L'interruttore **Collocazione obbligatoria** nella pagina **Scheda ubicazione** è facoltativo.
* Quando usi i prelievi da magazzino, il campo **Cod. collocazione** nella riga di componente di un ordine di produzione o nelle righe di pianificazione progetto definisce la collocazione *prendere*. I componenti vengono diminuiti nella collocazione quando registri il consumo.

## <a name="inventory-movements"></a>Movimenti di magazzino

* I movimenti di magazzino richiedono l'attivazione dell'opzione **Collocazione obbligatoria** nella pagina **Scheda ubicazione** per l'ubicazione.
* I movimenti di magazzino funzionano solo con le righe dei componenti dell'ordine di produzione e le righe dell'ordine di assemblaggio.
* Quando si inserisce un movimento di magazzino per un'operazione interna, si registra solo la movimentazione fisica dei componenti a una collocazione nell'area di operazione. Non registri il consumo.
* Quando usi i movimenti da magazzino, il campo **Cod. collocazione** nelle righe di componente di un ordine di produzione definisce la collocazione *mettere* nell'area di operazione. La collocazione mettere è il luogo in cui i dipendenti della warehouse devono mettere i componenti.
* Registra separatamente il consumo dei componenti prelevati contabilizzando le registrazioni consumi o un ordine di assemblaggio.

>[!NOTE]
> Anche se l'interruttore **Richiesto prelievo** è disattivato, puoi utilizzare un documento **Prelievo warehouse**. I documenti prelievo warehouse sono simili ai documenti **prelievo in magazzino**. Ciò è utile se vuoi utilizzare i prelievi nelle operazioni e la spedizione nei flussi warehouse in uscita.

### <a name="production"></a>Produzione

Utilizza i documenti **prelievo in magazzino** per il prelievo dei componenti di produzione nel flusso verso la produzione.

Per un'ubicazione che utilizza le collocazioni, è possibile estendere il flusso alla produzione utilizzando i documenti **Movimento di magazzino**. I movimenti di magazzino sono particolarmente utili per la consuntivazione dei componenti. Per ulteriori informazioni su come il consumo del componente è consuntivato dalla collocazione articoli per produzione o produzione aperta, vedi [Consuntivazione dei componenti di produzione in una configurazione warehouse di base](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Assemblaggio

Utilizza i documenti **Movimento magazzino** per spostare i componenti dell'assemblaggio nell'area di assemblaggio.

> [!NOTE]
> I documenti **movimento di magazzino** richiedono collocazioni.

[!INCLUDE [prod_short](includes/prod_short.md)] supporta tipi di flusso assemblaggio su ordine e assemblaggio per magazzino. Per ulteriori informazioni sull'assemblaggio su ordine nel flusso di warehouse in uscita, vai a [Gestione di articoli assemblaggio su ordine con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Gestione progetti

Utilizza i documenti **prelievo magazzino** per il prelievo dei componenti di commessa nel flusso verso la gestione progetti.

Per le ubicazioni che utilizzano le collocazioni, è possibile estendere il flusso alle commesse con i documenti **Movimento di magazzino**.

> [!NOTE]
> È stata aggiunta la possibilità di selezionare i componenti per le righe di pianificazione progetto in [!INCLUDE[d365fin](includes/d365fin_md.md)] nel secondo ciclo di rilascio del 2022. Per iniziare a utilizzare la funzionalità, un amministratore deve attivare **Aggiornamento funzionalità: abilitazione del prelievo magazzino e warehouse da commesse** nella pagina **Gestione funzionalità**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] utilizza il valore del campo **Quantità rimanente** nella riga di pianificazione progetto quando crea prelievi magazzino. Per utilizzare i prelievi magazzino per le commesse, è necessario attivare l'interruttore **Applica collegamento utilizzo** nella pagina **Scheda progetto** per la commessa. Ciò ti consente di monitorare l'utilizzo rispetto al tuo piano. Se non si attiva l'interruttore, la quantità rimanente rimarrà a **0** e il prelievo magazzino non verrà creato. Per ulteriori informazioni, vedi [Per impostare la tracciabilità dell'utilizzo di un progetto](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-project-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-projects-in-a-basic-warehouse-configuration"></a>Prelevare o spostare per produzione, assemblaggio e progetti in una configurazione warehouse di base

È possibile creare un prelievo da magazzino o un movimento di magazzino in tre modi:  

* Dal documento di origine stesso.  
* Per più documenti di origine contemporaneamente utilizzando un processo batch.  
* In due passaggi. Rilascia il documento di origine per renderlo pronto per il prelievo. Crea il prelievo o il movimento di magazzino dai documenti **Prelievo di magazzino** o **Movimento di magazzino**. Il prelievo o il movimento di magazzino si basano sul documento di origine.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Per creare un prelievo magazzino dal documento di origine

1. Nel documento di origine, che può essere un ordine di produzione o una commessa, scegli l'azione **Crea stoccaggio/prelievo di magazzino**.  
2. Seleziona la casella di controllo **Crea prelievo mag.**.
3. Scegli il pulsante **OK**.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Per creare un movimento di magazzino dal documento origine

1. Nel documento di origine, che può essere un ordine di produzione, un ordine di assemblaggio o una commessa, scegli l'azione **Crea stoccaggio/prelievo di magazzino**.  
2. Seleziona la casella di controllo **Crea movimento di magazzino**.
3. Scegli il pulsante **OK**.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Per creare più prelievi o movimenti di magazzino utilizzando un processo batch

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Crea stoccaggio/prelievo/movimento magazzino**, quindi seleziona il collegamento correlato.  
2. Nella Scheda dettaglio **Richiesta warehouse**, utilizza i campi **Nr. origine** e **Documento origine** per filtrare i tipi di documenti oppure gli intervalli di numeri di documenti. Ad esempio, è possibile creare prelievi solo per gli ordini di produzione.
3. Nella Scheda dettaglio **Opzioni**, attiva l'interruttore **Crea prelievo mag.** o **Crea movimento mag.**.
4. Scegli il pulsante **OK**.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>Per creare prelievi o movimenti di magazzino in due passaggi

Per prelevare o spostare i componenti per i documenti di origine in due passaggi, è necessario rilasciare il documento di origine per renderlo pronto per il prelievo. Rilasciare i documenti di origine per le operazioni interne nei seguenti modi.  

|Documento origine|Metodo di rilascio|  
|---------------------|--------------------|  
|Ordine di produzione|Nella pagina **Ordine di produzione pianificato** modifica lo stato di un ordine in **Rilasciato** o utilizza la pagina **Ordine di produzione rilasciato** per creare un ordine di produzione rilasciato.|  
|Ordine di assemblaggio|Modifica lo stato di un ordine di assemblaggio in **Rilasciato**.|
|Commesse | Cambia lo stato di una commessa in **Aperto** o crea subito una commessa con stato Aperto.|  

Un dipendente warehouse addetto al prelievo degli articoli può creare un documento di stoccaggio magazzino per il documento di origine.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi magazzino** o **Movimento di magazzino**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Nel campo **Documento origine**, seleziona il tipo di documento di origine per cui esegui lo stoccaggio.

    > [!NOTE]
    > Non è possibile utilizzare i documenti **Prelievo magazzino** per il prelievo dei componenti di assemblaggio.
4. Nel campo **Nr. origine** selezionare il documento di origine.  
5. In alternativa, scegli l'azione **Prendi documento origine** per selezionare il documento da una lista di documenti di origine in entrata pronti per il prelievo presso l'ubicazione.  
6. Seleziona il pulsante **OK** per compilare le righe di prelievo o movimento in base al documento di origine selezionato.  

## <a name="to-record-the-inventory-pick"></a>Per registrare il prelievo magazzino

1. Nella pagina **Prelievo magazzino** apri il documento per cui registrare un prelievo.  
2. Nel campo **Codice collocazione** sulle righe di prelievo, la collocazione da cui gli articoli devono essere prelevati dalla collocazione in cui l'articolo è disponibile. Se necessario, puoi modificare la collocazione.
3. Esegui il prelievo e immetti la quantità prelevata nel campo **Qtà da gestire**.

    Se è necessario prelevare gli articoli relativi a una riga da più collocazioni, ad esempio perché la collocazione non contiene tutta la quantità, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.  
4. Scegli l'azione **Registra**.  

Durante il processo di registrazione si verifica quanto segue:

* Registra il consumo delle righe del documento di origine prelevate.
* Se l'ubicazione prevede l'utilizzo di collocazioni, verranno creati movimenti warehouse per la registrazione delle modifiche delle quantità nelle collocazioni.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>Per registrare il movimento di magazzino

1. Nella pagina **Movimento di magazzino** apri il documento per cui registrare un movimento.  
2. Nel campo **Codice collocazione** sulle righe di movimento, la collocazione da cui prelevare è suggerita sulla base della collocazione predefinita dell'articolo e della disponibilità. Se necessario, puoi modificare la collocazione.  
3. Esegui il movimento e immetti la quantità spostata nel campo **Qtà da gestire**. Il valore nelle righe Prendere e Mettere deve essere identico. In caso contrario, non è possibile registrare la movimentazione.

    Se è necessario prendere gli articoli relativi a una riga da più collocazioni, ad esempio perché la collocazione non contiene tutta la quantità, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.  
4. Seleziona l'azione **Registra movimento di magazzino**.  

Durante il processo di registrazione si verifica quanto segue:

* I movimenti warehouse ora indicano che i componenti sono nelle collocazioni specificate nelle righe ordine del documento di origine. Ad esempio, l'ordine di assemblaggio, il componente di produzione o la riga di pianificazione progetto.

>[!NOTE]
> A differenza di quando si spostano componenti con un prelievo magazzino, il consumo non è registrato quando si registra un movimento di magazzino. Registra il consumo come passaggio separato registrando il documento di origine.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>Consuntivazione componenti di produzione in una configurazione warehouse di base

I metodi di consuntivazione influiscono sul flusso dei componenti in produzione. Per ulteriori informazioni vedi [Eseguire la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md). A seconda del metodo di consuntivazione selezionato, è possibile prelevare i componenti per la produzione nei seguenti modi:

* Utilizza un documento **Prelievo magazzino** per registrare il prelievo per gli articoli che utilizzano il metodo di consuntivazione **Manuale**. Quando si registra un prelievo da magazzino, viene registrato il consumo dei componenti prelevati. 
* Utilizza un documento **Movimento di magazzino** con riferimento a un documento di origine per registrare i prelievi per i componenti che utilizzano il metodo di consuntivazione **Manuale**. Dovrai registrare il consumo separatamente. Per ulteriori informazioni vedi [Registrare il consumo produzione tramite processo batch](production-how-to-post-consumption.md). 
* Utilizza un documento **Movimento di magazzino** con riferimento a un documento di origine per registrare i prelievi per i componenti che utilizzano il metodo di consuntivazione **Prelievo + Avanti**, **Prelievo + Indietro**. Il consumo dei componenti avverrà automaticamente quando modifichi lo stato dell'ordine di produzione oppure avvii o termini un'operazione. Tutti i componenti obbligatori devono essere disponibili. In caso contrario, la registrazione del consumo della consuntivazione viene interrotta per tale componente.
* Utilizza un documento **Movimento di magazzino** senza riferimento a un documento di origine o altri modi per registrare il movimento di componenti che utilizzano il metodo di consuntivazione **Avanti** o **Indietro**. Il consumo dei componenti avverrà automaticamente quando modifichi lo stato dell'ordine di produzione oppure avvii o termini un'operazione. Tutti i componenti obbligatori devono essere disponibili. In caso contrario, la registrazione del consumo della consuntivazione viene interrotta per tale componente. Per ulteriori informazioni vedi [Spostare gli articoli internamente nelle configurazioni warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Esempio

Esiste un ordine di produzione per 15 PZ dell'articolo SP-SCM1004. Alcuni degli articoli nell'elenco dei componenti devono essere consuntivati manualmente in una registrazione di consumo, mentre altri articoli possono essere prelevati e consuntivati automaticamente utilizzando il metodo di consuntivazione **Prelievo + Indietro**.  

I seguenti passaggi forniscono un esempio delle azioni eseguite da utenti differenti e le risposte correlate:  

1. Il supervisore di produzione rilascia l'ordine di produzione. Gli articoli con il metodo di consuntivazione in **Avanti** e privi di un collegamento ciclo-distinta base vengono dedotti dalla collocazione produzione aperta.  
2. Il supervisore di produzione sceglie l'azione **Crea stoccaggio/prelievo magazzino** sull'ordine di produzione e attiva l'azione **Crea prelievo magazzino** e **Crea movimento magazzino**. Un documento di prelievo magazzino viene creato per gli articoli con il metodo di consuntivazione **Manuale** e un movimento di magazzino viene creato per il articoli con i metodi di consuntivazione **Prelievo + Indietro** e **Prelievo + Avanti**.
3. Il responsabile di warehouse assegna i prelievi e i movimenti a un dipendente warehouse.
4. Il dipendente warehouse seleziona gli articoli dalle collocazioni appropriate e li inserisce nella collocazione articoli per produzione o nella collocazione specificata nel movimento di magazzino. La collocazione può essere una collocazione centro di lavoro o area di produzione.  
5. Il dipendente warehouse registra il prelievo. La quantità viene detratta dalle collocazioni.
6. Il dipendente warehouse registra il movimento. La quantità viene sottratta dalle collocazioni di prelievo e aggiunta alla collocazione di consumo. Il campo **Qtà prelevata** nell'elenco dei componenti per tutti gli articoli selezionati viene aggiornato.  
7. L'operatore di macchina informa il responsabile di produzione che gli articoli finali sono terminati.  
8. Il supervisore di produzione utilizza le registrazioni output o le registrazioni di produzione per registrare l'output. La quantità di articoli componenti che utilizzano i metodi di consuntivazione **Prelievo + Avanti** o **Prelievo + Indietro** con collegamenti di ciclo viene detratta dalla collocazione articoli per produzione.
9. Il responsabile di produzione cambia lo stato dell'ordine di produzione in **Completato**. La quantità di articoli componenti che utilizzano il metodo di consuntivazione **Indietro** viene dedotta dalla collocazione produzione aperta e la quantità di articoli componente che utilizzano il metodo di consuntivazione **Prelievo + Indietro** senza collegamento di ciclo, viene dedotta dalla collocazione articoli per produzione.  

 Nell'illustrazione seguente viene mostrato quando il campo **Cod. collocazione** nell'elenco di componenti viene compilato in base all'ubicazione o all'impostazione area di produzione/centro di lavoro.  

:::image type="content" source="media/binflow.png" alt-text="Panoramica del momento e della modalità con cui il campo Codice collocazione viene compilato.":::

## <a name="see-also"></a>Vedere anche

[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
