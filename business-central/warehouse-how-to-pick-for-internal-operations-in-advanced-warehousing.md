---
title: Prelevare per le operazioni interne in configurazioni warehouse avanzate
description: 'Se le ubicazioni utilizzano il prelievo e la spedizione, preleva i componenti per le attività di produzione, assemblaggio e commessa nella pagina Prelievo warehouse.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Prelevare per produzione, assemblaggio o commesse in configurazioni warehouse avanzate

La modalità di stoccaggio dei componenti di prelievo per le commesse, gli ordini di produzione o di assemblaggio dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

In una configurazione warehouse avanzata per il flusso in uscita (prelievo), attiva gli interruttori **Richiesto prelievo** e **Richiesta spedizione** nella pagina **Scheda ubicazione** per l'ubicazione.

Quando l'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi e delle spedizioni warehouse, utilizza i documenti di prelievo warehouse per creare ed elaborare le informazioni di prelievo prima della registrazione dell'utilizzo o del consumo dei componenti.  

Puoi creare i documenti di prelievo warehouse da zero. I prelievi fanno parte di un flusso di lavoro in cui una persona che sta elaborando un ordine li crea in modalità push o l'addetto alla warehouse li crea in modalità pull:

- In una modalità push, dove usi l'azione **Crea prelievo** nella pagina **Ordine di produzione**, **Ordine di assemblaggio**, **Scheda progetto**. Seleziona le righe da prelevare e prepara i prelievi specificando, ad esempio, le collocazioni da cui prelevare, quelle in cui inserire e il numero di unità da gestire. Le collocazioni possono essere predefinite per l'ubicazione o la risorsa warehouse.
- In modalità pull, dove rilasci un **Ordine di produzione**, **Ordine di assemblaggio**, **Scheda progetto** alla warehouse che rende gli articoli disponibili per il prelievo. Quindi, nella pagina **Prospetto prelievi**, i dipendenti della warehouse possono utilizzare l'azione **Prendi documenti warehouse** per prendere i prelievi assegnati.

Per prelevare o spostare i componenti per i documenti di origine in modalità pull, è necessario rilasciare il documento di origine per renderlo pronto per il prelievo. Rilasciare i documenti di origine per le operazioni interne nei seguenti modi.  

|Documento origine|Metodo di rilascio|  
|---------------------|--------------------|  
|Ordine di produzione|Modifica lo stato dell'ordine in Rilasciato o crea subito un ordine di produzione rilasciato.|  
|Ordine di assemblaggio|Modificare lo stato in Rilasciato.|
|Commesse | Cambia lo stato in Aperto o crea subito una commessa con stato Aperto.|  

## <a name="production"></a>Produzione

Utilizza i documenti **prelievo warehouse** per il prelievo dei componenti di produzione nel flusso verso la produzione.

Per un'ubicazione che utilizza le collocazioni per spostare gli articoli nelle collocazioni aperte in produzione, è possibile utilizzare i seguenti metodi:

* Per un'ubicazione che utilizza lo stoccaggio e il prelievo diretti, segui i passaggi nell'articolo [Spostare articoli nelle configurazioni warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md).
* Per le altre ubicazioni, segui le indicazioni nell'articolo [Spostare gli articoli internamente nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a>Assemblaggio

Utilizza i documenti **Prelievo warehouse** per spostare i componenti dell'assemblaggio nell'area di assemblaggio.

[!INCLUDE [prod_short](includes/prod_short.md)] supporta tipi di flusso assemblaggio su ordine e assemblaggio per magazzino. Per ulteriori informazioni sull'assemblaggio su ordine nel flusso di warehouse in uscita, vai a [Gestione di articoli assemblaggio su ordine nelle spedizioni warehouse](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Gestione progetti

Utilizza i documenti **prelievo warehouse** per il prelievo dei componenti di commessa nel flusso verso la gestione progetti.

> [!NOTE]
> È stata aggiunta la possibilità di selezionare i componenti per le righe di pianificazione progetto in [!INCLUDE[d365fin](includes/d365fin_md.md)] nel secondo ciclo di rilascio del 2022. Per iniziare a utilizzare la funzionalità, un amministratore deve attivare **Aggiornamento funzionalità: abilitazione del prelievo magazzino e warehouse da commesse** nella pagina **Gestione funzionalità**.
>
> Le commesse non supportano le configurazioni avanzate in cui l'interruttore **Prelievo e stoccaggio diretti** è attivato.

## <a name="check-whether-items-are-available-for-picking"></a>Controllare se gli articoli sono disponibili per il prelievo

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Per creare documenti di prelievo in blocco con i prospetti prelievi

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto prelievi**, quindi scegli il collegamento correlato.  

2. Scegliere l'azione **Prendi documenti warehouse**.  

    La lista mostra la produzione rilasciata, le commesse, gli ordini di assemblaggio che sono stati inoltrati alla funzione di prelievo. Gli ordini includono quelli per i quali sono già state create istruzioni di prelievo. I documenti contenenti righe di prelievo per le quali il prelievo è stato eseguito e registrato non vengono visualizzati in questa lista.  
3. Seleziona gli ordini per cui vuoi preparare un prelievo.

    > [!NOTE]  
    > Se selezioni un documento che ha già le istruzioni per tutte le sue righe, [!INCLUDE [prod_short](includes/prod_short.md)] ti informa che non c'è niente da gestire. Per combinare le istruzioni di prelievo warehouse già create in un'unica istruzione di prelievo, elimina prima i singoli prelievi warehouse.

4. Compilare il campo **Metodo di Sort** per ordinare le righe nel modo desiderato.  

    > [!NOTE]  
    > Il modo in cui le righe vengono ordinate nel prospetto non si applica automaticamente all'istruzione di prelievo. Tuttavia, sono disponibili gli stessi strumenti di ordinamento, insieme alla valutazione collocazione. È possibile ricreare facilmente l'ordine delle righe pianificate nel prospetto quando si creano le istruzioni di prelievo o ordinandole nelle istruzioni di prelievo.

5. Compilare il campo **Qtà da gestire**. Scegliere l'azione **Autocompil. qtà da gestire** oppure compilare i campi manualmente.  

    La pagina mostra le quantità disponibili nelle collocazioni cross-dock, utili per pianificare le assegnazioni del lavoro in situazioni di cross-dock. [!INCLUDE[prod_short](includes/prod_short.md)] proporrà sempre prima un prelievo da una collocazione cross-dock.

6. Le righe possono essere modificate manualmente, se necessario. È inoltre possibile eliminare alcune righe per creare un prelievo più efficiente. Se ad esempio vi sono più righe con articoli nelle collocazioni di cross-dock, puoi creare un prelievo per tutte le righe. Gli articoli sottoposti a cross-dock vengono prelevati con gli altri articoli nel documento di origine e nelle collocazioni di cross-dock è disponibile una maggiore quantità di spazio per ulteriori articoli in entrata.

    > [!NOTE]  
    >  Le righe vengono eliminate solo da questo prospetto e non dalla lista di selezione dei prelievi.  

7. Scegliere l'azione **Crea prelievo**. Si apre la pagina **Crea prelievo**, dove puoi aggiungere ulteriori informazioni sul prelievo.  

    Specifica in che modo combinare le righe di prelievo nei documenti di prelievo selezionando una delle opzioni seguenti.  

    |Opzione|Descrizione|
    |-|-|
    |Per documento whse. Documento|Crea documenti di prelievo distinti per le righe del prospetto con lo stesso documento warehouse di origine.|
    |Per cliente/forn./ubicazione|Crea documenti di prelievo separati per ogni cliente (commesse)|
    |Per articolo|Crea documenti di prelievo separati per ogni articolo nel prospetto prelievi.|
    |Per Da zona|Crea documenti di prelievo separati per ogni zona da cui vengono prelevati articoli.|
    |Per collocazione|Crea documenti di prelievo separati per ogni collocazione da cui vengono prelevati articoli.|
    |Per scadenza|Crea documenti di prelievo separati per i documenti di origine che hanno la stessa data di scadenza.|

    Specifica in che modo vengono creati i documenti di prelievo selezionando una delle opzioni seguenti.  

    |Opzione|Descrizione|
    |-|-|
    |Importo massimo No. di righe prelievo|Crea documenti di prelievo con un numero di righe in ogni documento non superiore a quello specificato.|
    |Importo massimo No. di doc. origine prelievo|Crea documenti di prelievo che si riferiscono al numero di documenti origine specificato.|
    |ID utente assegnato|Crea documenti di prelievo solo per le righe del prospetto assegnate all'impiegato warehouse selezionato.|
    |Metodo di ordinamento per righe di prelievo|Scegli una delle opzioni disponibili per ordinare le righe nel documento di prelievo creato.|
    |Impostare filtro breakbulk|Nasconde le righe prelievo di breakbulk intermedie quando un'unità di misura più grande viene convertita in un'unità di misura più piccola e prelevata.|
    |Qtà da gestire non compilata|Lascia il campo **Qtà. da gestire** vuoto nelle righe di prelievo create.|
    |Stampa prelievo|Stampa i documenti di prelievo al momento della creazione. È inoltre possibile stampare dai documenti di prelievo creati.|

8. Scegli il pulsante **OK**.  

## <a name="to-pick-items-for-a-productions-order-assembly-order-job"></a>Per prelevare articoli per un ordine di produzione, un ordine di assemblaggio, una commessa

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi**, quindi scegli il collegamento correlato.  

    Se è necessario utilizzare un determinato prelievo, seleziona il prelievo dalla lista oppure filtra la lista per individuare i prelievi assegnati a te. Aprire la scheda prelievo.  
2. Se il campo **ID utente assegnato** è vuoto, immetti il tuo ID per identificarti, se necessario.  
3. Preleva gli articoli.  

    Se la warehouse prevede l'utilizzo di collocazioni, vengono utilizzate le collocazioni predefinite degli articoli per suggerire la posizione da cui prelevare gli articoli. Le istruzioni contengono almeno due righe distinte, una per ogni azione Prendere e Mettere.  

    Le aree operative come le officine di produzione potrebbero avere una collocazione predefinita per i componenti di cui hanno bisogno. In tal caso, il codice collocazione predefinito viene aggiunto al documento di prelievo warehouse per indicare dove inserire gli articoli. Per ulteriori informazioni, vedi i suggerimenti per i campi **Cod. coll. art. per produzione**, **Cod. coll. art. per assembl.** e **A commessa - Codice collocazione**.

    Se la warehouse prevede l'utilizzo di stoccaggi e prelievi guidati, viene utilizzata la valutazione collocazione per calcolare le migliori collocazioni da cui effettuare il prelievo. Tali collocazioni vengono quindi suggerite nelle righe prelievo. Le istruzioni contengono almeno due righe distinte, una per ogni azione Prendere e Mettere.  

    * La prima riga, in cui il campo **Tipo azione** è impostato su **Prendere**, indica l'ubicazione degli articoli nell'area di prelievo. Se si spedisce un numero elevato di articoli in una riga di spedizione, potrebbe essere necessario prelevare gli articoli in diverse collocazioni, pertanto è presente una riga Prendere per ogni collocazione.
    * Nelle righe successive, in cui il campo **Tipo azione** è impostato su **Mettere**, viene indicata la posizione in cui inserire gli articoli nella warehouse. Non è possibile modificare la zona e la collocazione in questa riga.

    > [!NOTE]
    > Se è necessario prelevare o inserire gli articoli relativi a una riga in più collocazioni, ad esempio perché la collocazione designata è piena, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.

      Puoi ordinare le righe di prelievo in base a diversi criteri, ad esempio per articolo, numero di scaffale o data di scadenza. L'ordinamento può aiutare a ottimizzare il processo di stoccaggio, ad esempio:

    * Se le righe Prendere e Mettere per ciascuna riga di spedizione non sono consecutive, è possibile ordinarle selezionando **Articolo** nel campo **Metodo ordinamento**.  
    * Se le valutazioni collocazione riflettono il layout fisico della warehouse, utilizza il metodo di ordinamento **Valutazione collocazione** per organizzare la gestione delle ubicazioni della collocazione.

  > [!NOTE]  
  > Le righe sono ordinate in ordine crescente in base ai criteri selezionati. Se ordini per documento, l'ordinamento viene eseguito prima per tipo di documento in base al campo **Documento origine attività warehouse**. Se ordini per spedizione, l'ordinamento viene eseguito prima per tipo di destinazione in base al campo **Tipo di destinazione warehouse**.

4. Dopo avere prelevato e posizionato gli articoli nell'area di produzione, assemblaggio o commessa o nella collocazione, scegli l'azione **Registra prelievo**.  

    È ora possibile portare gli articoli nella rispettiva area e registrare l'utilizzo o il consumo dei componenti prelevati contabilizzando le registrazioni consumi, l'ordine di assemblaggio o la registrazione progetti. Per ulteriori informazioni, vedi i seguenti articoli:

    * [Registrare i consumi e l'output relativi a una singola riga dell'ordine di produzione rilasciato](production-how-to-register-consumption-and-output.md)
    * [Assemblare articoli](assembly-how-to-assemble-items.md)
    * [Registrare il consumo o l'uso per i progetti](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Consuntivazione dei componenti di produzione in una configurazione warehouse avanzata

I metodi di consuntivazione influiscono sul flusso dei componenti in produzione. Per ulteriori informazioni vedi [Eseguire la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md). A seconda del metodo di consuntivazione selezionato, è possibile prelevare i componenti per la produzione nei seguenti modi:

* Utilizza un documento **Prelievo warehouse** per registrare il prelievo per gli articoli che utilizzano il metodo di consuntivazione **Manuale**. Devi registrare il consumo separatamente. Per ulteriori informazioni vedi [Registrare il consumo produzione tramite processo batch](production-how-to-post-consumption.md).
* Utilizza un documento **Prelievo warehouse** per registrare il prelievo per gli articoli che utilizzano il metodo di consuntivazione **Prelievo + Avanti**, **Prelievo + Indietro**. Il consumo dei componenti avviene automaticamente quando modifichi lo stato dell'ordine di produzione oppure avvii o termini un'operazione. Tutti i componenti obbligatori devono essere disponibili. In caso contrario, la registrazione del consumo della consuntivazione viene interrotta per tale componente.
* Utilizza un documento **Movimento warehouse** senza riferimento a un documento di origine o altri modi per registrare il movimento di componenti che utilizzano il metodo di consuntivazione **Avanti** o **Indietro**. I componenti vengono automaticamente consumati quando modifichi lo stato dell'ordine di produzione oppure avvii o termini un'operazione. Tutti i componenti obbligatori devono essere disponibili. In caso contrario, la registrazione del consumo della consuntivazione viene interrotta per tale componente. Per ulteriori informazioni vedi [Spostare articoli](warehouse-move-items.md).

### <a name="example"></a>Esempio

Esiste un ordine di produzione per 15 PZ dell'articolo SP-SCM1004. Alcuni articoli nella lista dei componenti devono essere sottoposti manualmente a consuntivazione nelle registrazioni consumi. Altri articoli possono essere prelevati e sottoposti a consuntivazione automaticamente utilizzando il metodo di consuntivazione **Preleva + Indietro**.  

I seguenti passaggi descrivono le azioni eseguite da utenti differenti e la risposta correlata:  

1. Il supervisore di produzione rilascia l'ordine di produzione. Gli articoli con il metodo di consuntivazione in **Avanti** e privi di un collegamento ciclo-distinta base vengono dedotti dalla collocazione produzione aperta.  
2. Il supervisore di produzione fa clic sull'azione **Crea prelievo warehouse** nell'ordine di produzione. Un documento di prelievo warehouse viene creato per il prelievo degli articoli con i metodi di flushing **Manuale**, **Prelievo + Indietro** e **Prelievo + Avanti**. Questi articoli si trovano nella collocazione articoli per produzione.  
3. Il responsabile di warehouse assegna i prelievi a un dipendente warehouse.  
4. Il dipendente warehouse seleziona gli articoli dalle collocazioni appropriate e li inserisce nella collocazione articoli per produzione o nella collocazione specificata nel prelievo warehouse. La collocazione potrebbe essere una collocazione centro di lavoro o area di produzione.
5. Il dipendente warehouse registra il prelievo. La quantità viene trasferita dalla collocazione di prelievo nella collocazione di consumo. Il campo **Qtà prelevata** nell'elenco dei componenti per tutti gli articoli selezionati viene aggiornato.

    > [!NOTE]  
    >  Solo la quantità prelevata può essere utilizzata.  
6. L'operatore di macchina informa il responsabile di produzione che gli articoli finali sono terminati.
7. Il supervisore di produzione utilizza le registrazioni di produzione o di consumo per registrare il consumo di articoli componenti che utilizzano il metodo di consuntivazione **Manuale**.
8. Il supervisore di produzione utilizza le registrazioni output o le registrazioni di produzione per registrare l'output. La quantità di articoli componenti che utilizzano i metodi di consuntivazione **Prelievo + Avanti** o **Prelievo + Indietro** con collegamenti di ciclo viene detratta dalla collocazione articoli per produzione.
9. Il responsabile di produzione cambia lo stato dell'ordine di produzione in **Completato**. La quantità di articoli componenti che utilizzano il metodo di consuntivazione **Indietro** viene dedotta dalla collocazione produzione aperta e la quantità di articoli componente che utilizzano il metodo di consuntivazione **Prelievo + Indietro** senza collegamento di ciclo, viene dedotta dalla collocazione articoli per produzione.  

Nell'illustrazione seguente viene mostrato quando il campo **Cod. collocazione** nell'elenco di componenti viene compilato in base all'ubicazione o all'impostazione area di produzione/centro di lavoro.  

:::image type="content" source="media/binflow.png" alt-text="Panoramica del momento e della modalità con cui il campo Codice collocazione viene compilato.":::

## <a name="make-to-order-mto-production-components-in-an-advanced-warehouse-configuration"></a>Componenti di produzione Prod. su ordine in una configurazione warehouse avanzata

Negli scenari in cui un articolo prodotto è costituito da materie prime e articoli semilavorati con il criterio di produzione impostato su **Prod. su ordine**, il prelievo in warehouse per tali componenti semilavorati viene aggiunto allo stesso ordine di produzione con il campo **Cod. livello pianificazione** compilato. Si prevede che gli articoli semilavorati siano immediatamente disponibili per il consumo e non richiedano il prelievo, pertanto non sono inclusi nel documento di prelievo in warehouse. I prelievi in warehouse creati includono solo le materie prime per gli articoli prodotti e per gli articoli semilavorati.

Tuttavia, se gli articoli semilavorati sono disponibili in magazzino, il sistema di pianificazione suggerisce di consumarli invece di produrre l'intera quantità. Ad esempio, un articolo prodotto richiede cinque componenti semilavorati, ma tre sono già disponibili in magazzino. In questo caso, nei componenti dell'ordine di produzione vengono elencati cinque articoli semilavorati, ma solo due vengono prodotti nello stesso ordine di produzione come riga ordine di produzione separata.
Tale impostazione non è compatibile con i prelievi in warehouse e, a seconda della frequenza, per tali articoli semilavorati devi impostare il criterio di produzione **Prod. per Magazzino** o suddividere manualmente la riga componente dell'ordine di produzione quando devi prelevare gli articoli semilavorati prodotti in precedenza.


## <a name="see-also"></a>Vedere anche

- [Gestire i costi del magazzino](inventory-manage-inventory.md)  
- [Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
- [Gestione assemblaggio](assembly-assemble-items.md)  
- [Panoramica della gestione warehouse](design-details-warehouse-management.md)
- [Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
