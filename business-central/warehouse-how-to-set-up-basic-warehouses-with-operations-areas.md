---
title: Impostare le warehouse di base con aree di operazioni
description: 'Imposta le aree operative della warehouse e utilizza i movimenti di magazzino, i prelievi e gli stoccaggi per spostare le merci.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '6774, 6775, 6776'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Impostare le warehouse di base con aree di operazioni

Se le aree delle operazioni interne, ad esempio produzione o assemblaggio, sono presenti nelle configurazioni di base della warehouse in cui le ubicazioni utilizzano il campo di setup **Collocazione obbligatoria** ed eventualmente i campi di setup **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile utilizzare i seguenti documenti warehouse di base per registrare le attività di warehouse per le aree delle operazioni interne:  

- Pagina **Movimento di magazzino**.  
- Pagina **Prelievi magazzino**.  
- Pagina **Stoccaggio in magazzino**.

> [!NOTE]
> Anche se le impostazioni sono definite **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare carichi e spedizioni direttamente dai documenti commerciali di origine nelle ubicazioni in cui si selezionano queste caselle di controllo.  

Per utilizzare queste pagine con le operazioni interne, ad esempio prelevare e spostare componenti in produzione, è necessario impostare alcune o tutte le seguenti procedure di setup in base al livello di controllo richiesto:  

- Abilitare i documenti relativi a prelievi magazzino, spostamento e stoccaggio.  
- Definire le strutture di collocazione di default per i componenti e gli articoli finali trasferiti da e verso le risorse dell'operazione.  
- Creare collocazioni di provenienza e destinazione dedicate alle risorse specifiche dell'operazione per evitare il prelievo degli articoli per i documenti in uscita.

I codici di collocazione impostati nelle schede ubicazione consentono di definire un flusso di warehouse di default per determinate attività, come i componenti di un reparto di assemblaggio. La funzionalità aggiuntiva consente di garantire che quando gli articoli si trovano in una determinata collocazione, non possono essere spostati o prelevati per altre attività. Per ulteriori informazioni, vedere [Per creare collocazioni componenti dedicate](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Le procedure riportate di seguito sono basate sull'impostazione di attività di warehouse di base relative a un'area di produzione. I passaggi sono simili ad altre aree dell'operazione, come assemblaggio, gestione assistenza e commesse.  

> [!NOTE]  
>  Nella procedura riportata di seguito, il campo di setup **Collocazione obbligatoria** nelle schede ubicazione è selezionato come condizione preliminare perché è considerato la base di qualsiasi livello di gestione warehouse.  

## Per abilitare i documenti di magazzino per le attività delle operazioni interne

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Aprire la scheda Ubicazione che si desidera configurare.  
3.  Nella Scheda Dettaglio **Warehouse** selezionare la casella di controllo **Richiesto stoccaggio** per indicare che quando viene rilasciato un documento di origine in entrata o interno con un codice collocazione, può essere creato un documento di stoccaggio magazzino o di movimento di magazzino.  
4.  Selezionare la casella di controllo **Richiesto prelievo** per indicare che quando viene creato un documento di origine in uscita o interno con un codice collocazione, deve essere creato un documento di prelievi magazzino o di movimento di magazzino.  

## Per definire una struttura di collocazione di default nell'area di produzione

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Aprire l'ubicazione che si desidera configurare.  
3.  Nel campo **Codice coll. produzione aperta** della Scheda Dettaglio **Collocazioni** immettere il codice della collocazione nell'area di produzione con tutti i componenti che l'operatore macchina può consumare senza richiedere un'attività di warehouse per portarli alla collocazione. Gli articoli che si trovano in questa collocazione vengono in genere impostati per la registrazione automatica o la consuntivazione. Ciò significa che il campo **Metodo consuntivazione** contiene **Avanti** o **Indietro**.  
4. Nel campo **Cod. coll. art. per produzione** immettere il codice della collocazione nell'area di produzione in cui i componenti prelevati per la produzione in questa ubicazione vengono inseriti per default prima di poter essere consumati. Gli articoli che si trovano in questa collocazione vengono in genere impostati per la registrazione del consumo manuale. Ciò significa che il campo **Metodo consuntivazione** contiene **Manuale** o **Prelievo+Aut.Inizio** o **Prelievo+Aut.Fine** per i prelievi warehouse e i movimenti di magazzino.  

    > [!NOTE]  
    > Quando si utilizzano prelievi da magazzino, il campo **Cod. collocazione** nella riga di componente di un ordine di produzione definisce la collocazione *prendere* da dove vengono diminuiti i componenti quando viene registrato il consumo. Quando si utilizzano i movimenti di magazzino, il campo **Cod. collocazione** nelle righe di componenti dell'ordine di produzione definisce la collocazione *mettere* nell'area di operazione in cui l'addetto alla warehouse deve posizionare i componenti.  

5. Nel campo **Cod. coll. art. da produzione** della Scheda Dettaglio **Collocazioni** immettere il codice della collocazione nell'area di produzione da cui gli articoli finali completati vengono prelevati per default quando il processo comporta un'attività di warehouse. Nelle configurazioni di warehouse di base, l'attività viene registrata come uno stoccaggio o un movimento di magazzino.  

A questo punto, le righe dei componenti dell'ordine di produzione con il codice collocazione di default che necessitano di componenti prelevati a priori vengono posizionate in quel punto. Tuttavia, fino a quando i componenti vengono utilizzati da tale collocazione, in seguito alle domande di altri componenti è possibile prelevare o utilizzare questi ultimi da tale collocazione perché sono ancora considerati contenuti della collocazione disponibili. Per verificare che il contenuto della collocazione sia disponibile solo per la domanda di componenti che utilizza la collocazione articoli per produzione, è necessario selezionare il campo **Dedicata** sulla riga per tale codice collocazione nella pagina **Collocazioni** aperta dalla scheda ubicazione.

Questo diagramma di flusso illustra in che modo il campo **Cod. collocazione** nelle righe del componente dell'ordine di produzione viene compilato in base al setup.  

![Diagramma di flusso collocazione.](media/binflow.png "BinFlow")

## Per definire una struttura di collocazione di default nell'area di assemblaggio

I componenti per gli ordini di assemblaggio non possono essere prelevati o registrati con i prelievi da magazzino. Pertanto, utilizzare la pagina **Movimento di magazzino**. Per ulteriori informazioni, vedi [Prelevare o spostare per produzione, assemblaggio o processi in warehouse di base](warehouse-how-to-pick-for-production.md).

Durante il prelievo e la spedizione di quantità righe di vendita assemblate sull'ordine, è necessario seguire determinate regole per la creazione di righe di prelievo magazzino. Per altre informazioni, vedere la sezione "Gestione di articoli da assemblare su ordine in prelievi magazzino" in [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).

Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md).

### Per impostare la creazione automatica di un movimento di magazzino quando viene creato il prelievo magazzino per l'articolo di assemblaggio

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup assemblaggio**, quindi scegli il collegamento correlato.
2. Selezionare la casella di controllo **Crea movimenti automaticamente**.

### Per impostare la collocazione nell'area di assemblaggio in cui i componenti vengono inseriti per default prima di poter essere consumati in fase di assemblaggio

Il valore in questo campo viene automaticamente inserito nel campo **Codice collocazione** nelle righe ordine di assemblaggio quando questa ubicazione viene immessa nel campo **Codice ubicazione** nella riga di ordine di assemblaggio.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Apri l'ubicazione che desideri configurare.
3. Compilare il campo **Cod. coll. art. per assembl.**.

### Per impostare la collocazione nell'area di assemblaggio in cui gli articoli di assemblaggio completati sono registrati quando vengono assemblati per magazzino

Il valore in questo campo viene automaticamente inserito nel campo **Codice collocazione** nelle testate degli ordini di assemblaggio quando questo codice ubicazione viene immesso nel campo **Codice ubicazione** nella testata dell'ordine di assemblaggio.

I codici collocazione impostati nelle schede ubicazione consentono di definire un flusso di warehouse di default per determinate attività di warehouse, come il consumo di componenti in un'area di assemblaggio. La funzionalità aggiuntiva consente di garantire che quando gli articoli si trovano in una collocazione di default, non possono essere spostati o prelevati per altre attività.

> [!NOTE]
> Questo setup è possibile soltanto per le ubicazioni in cui è selezionato il campo Collocazione obbligatoria.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Apri l'ubicazione che desideri configurare.
3. Compilare il campo **Cod. coll. art. da assembl.**.

### Per impostare la collocazione in cui gli articoli di assemblaggio completati sono registrati quando vengono assemblati per ordine di vendita collegato

Da questa collocazione gli articoli di assemblaggio sono spediti immediatamente, tramite un prelievo di magazzino, per evadere l'ordine di vendita.

> [!NOTE]
> Questo campo non può essere utilizzato se l'ubicazione prevede l'uso di prelievi e stoccaggi guidati.

Il codice collocazione viene copiato dalla riga di ordine di vendita nella testata ordine di assemblaggio per comunicare agli addetti all'assemblaggio dove posizionare l'output per prepararlo alla spedizione. Viene copiato anche nella riga di prelievo magazzino per comunicare agli addetti alla warehouse da dove effettuare il prelievo per la spedizione.

> [!NOTE]
> La collocazione di spedizione Assemblaggio su ordine è sempre vuota. Quando si registra una riga vendite di assemblaggio su ordine, il contenuto della collocazione viene prima rettificato positivamente con l'output di assemblaggio. Subito dopo viene rettificato negativamente con la quantità spedita.

Il valore in questo campo viene automaticamente inserito nel campo Codice collocazione nelle righe ordine di vendita che contengono una quantità nel campo **Qtà per assemblaggio su ordine** o se per l'articolo da vendere è impostato **Assemblaggio su ordine** nel campo **Sistema di rifornimento**.

Se **Cod. coll. sp. ass. su ordine** è vuoto, viene utilizzato il campo **Cod. coll. art. da assembl.**. Se entrambi i campi di setup sono vuoti, la collocazione con contenuto utilizzata per ultima viene utilizzata nel campo **Codice collocazione** nelle righe ordine di vendita.

Lo stesso codice collocazione a sua volta viene copiato nel campo **Codice collocazione** sulla riga di prelievo magazzino che gestisce la spedizione della quantità per l'assemblaggio su ordine. Per altre informazioni, vedere la sezione "Gestione di articoli da assemblare su ordine in prelievi magazzino" in [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Apri l'ubicazione che desideri configurare.
3. Compilare il campo **Cod. coll. sp. ass. su ordine**.

## Per creare collocazioni di componenti dedicate

È possibile specificare che le quantità in una collocazione siano protette dal prelievo per domande diverse da quella corrente.

Le quantità nelle collocazioni dedicate possono comunque essere impegnate. Di conseguenza, le quantità nelle collocazioni dedicate sono incluse nel campo **Quantità totale disponibile** della pagina **Impegno**.

Ad esempio, un'area di produzione impostata con un codice collocazione nel campo **Cod. coll. art. per produzione**. Le righe componenti di ordini di produzione con il codice collocazione che necessitano di componenti prelevati a priori vengono posizionate in quel punto. Tuttavia, fino a quando i componenti vengono utilizzati da tale collocazione, in seguito alle domande di altri componenti è possibile prelevare o utilizzare questi ultimi da tale collocazione perché sono ancora considerati contenuti della collocazione disponibili. Per verificare che il contenuto della collocazione sia disponibile solo per la domanda di componenti che utilizza la collocazione articoli per produzione, è necessario selezionare il campo **Dedicata** sulla riga per tale codice collocazione nella pagina **Collocazioni** aperta dalla scheda ubicazione.

La creazione di una collocazione dedicata fornisce una funzionalità simile all'utilizzo di tipi di collocazione, disponibile solo nella gestione warehouse avanzata. Per ulteriori informazioni, vedere [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Gli articoli nelle collocazioni dedicate non sono protetti quando vengono prelevati e utilizzati come componenti di produzione tramite la pagina Prelievo magazzino.

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato. Selezionare l'ubicazione che si desidera aggiornare.  
2.  Scegliere l'azione **Collocazioni**.  
3.  Selezionare il campo **Dedicata** per ogni collocazione che si desidera utilizzare in modo esclusivo per determinate operazioni interne e in cui si desidera impegnare quantità per tale operazione interna, una volta inserite.  

> [!NOTE]  
>  La collocazione deve essere vuota prima di poter selezionare o deselezionare il campo **Dedicata**.

## Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
