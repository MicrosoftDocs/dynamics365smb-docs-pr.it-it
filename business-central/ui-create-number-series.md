---
title: Creazione di numerazioni
description: Informazioni su come impostare la numerazione per assegnare codici di identificazione univoci a conti e documenti in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 02/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Creazione di numerazioni

Per ogni società impostata, è necessario assegnare codici di identificazione univoci a elementi quali i conti di contabilità generale, i conti clienti e i conti fornitori, le fatture e altri documenti. La numerazione non è importante ai fini dell'identificazione. Un sistema di numerazione progettato correttamente inoltre semplifica la gestione e l'analisi della società e può ridurre gli errori di immissione dei dati.

> [!Important]
> Per impostazione predefinita, non sono consentite interruzioni nelle numerazioni poiché, per legge, l'esatta cronologia delle transazioni finanziarie deve essere disponibile per la revisione contabile e pertanto deve seguire una sequenza ininterrotta senza numeri cancellati.
>
> Se si desidera consentire delle interruzioni in determinate numerazioni, consultare il proprio revisore o il proprio responsabile della contabilità per assicurarsi di aderire ai requisiti legali nel proprio paese. Per ulteriori informazioni, vedere la sezione [Interruzioni nelle numerazioni](#gaps-in-number-series).

> [!NOTE]  
> Si consiglia di utilizzare gli stessi codici di numerazione visualizzati nella pagina **Elenco nr. serie** nella società di esempio CRONUS. I codici come *P-INV+* potrebbero non avere significato immediato, ma [!INCLUDE[prod_short](includes/prod_short.md)] dispone di un numero di impostazioni predefinite che dipendono da tali codici di numerazione.

Per creare un sistema di numerazione, è necessario impostare uno o più codici per ogni tipo di anagrafica o documento. È possibile, ad esempio, impostare un codice per la numerazione dei clienti, un altro per la numerazione delle fatture di vendita e un altro ancora per la numerazione di documenti in registrazioni COGE. Dopo avere impostato un codice, è necessario configurare almeno una riga di numerazione. Tale riga contiene informazioni quali il primo e l'ultimo numero nella serie e la data di inizio. È possibile impostare più righe di numerazione per codice di numerazione, con una diversa data di inizio per ogni riga. Le numerazioni verranno utilizzate consecutivamente, avviando ciascuna alla rispettiva data di inizio.

> [!NOTE]
> La lunghezza massima di un numero in una numerazione è di 20 caratteri. Ci sono alcune situazioni in cui [!INCLUDE[prod_short](includes/prod_short.md)] aggiungerà un numero con un ID generato dal sistema. Ad esempio, quando documenti come fatture vengono utilizzati per applicare transazioni, come pagamenti, [!INCLUDE[prod_short](includes/prod_short.md)] genera identificatori per le transazioni applicate. L'identificatore è composto da un numero di una numerazione e da un ID assegnato dal sistema a sei caratteri, come -12345. Se prevedi di elaborare più di 9.999 documenti nei giornali bancari o GIRO o nei giornali di ricevute di contanti, imposta le numerazioni per questi tipi di documenti in modo da includere meno di 14 caratteri.

In genere, si imposta la numerazione per inserire automaticamente il numero immediatamente successivo nelle nuove schede o documenti creati. Tuttavia, è anche possibile impostare una numerazione che consente l'immissione manuale del nuovo numero. A tale scopo selezionare la casella di controllo **Consenti num. manuale**.

Se si desidera utilizzare più codici di numerazione per un tipo di anagrafica, ad esempio per utilizzare una numerazione diversa per diverse categorie di articoli, è possibile utilizzare relazioni tra numerazioni.

## Interruzioni nelle numerazioni

Non tutti i record creati in [!INCLUDE[prod_short](includes/prod_short.md)] sono transazioni finanziarie che devono utilizzare numerazioni sequenziali. Le schede cliente, le offerte di vendita e le attività di warehouse sono esempi di record a cui è assegnato un numero di una numerazione, ma che non sono soggetti a controlli finanziari e/o che possono essere eliminati. Per tali numerazioni, è possibile selezionare la casella di controllo **Consenti interruzioni in num.** nella pagina **Righe nr. serie**. Questa impostazione può essere modificata anche dopo aver creato le numerazioni. Per ulteriori informazioni, vedere [Per creare nuove numerazioni](ui-create-number-series.md#to-create-a-new-number-series).

## Comportamento del campo Nr. in documenti e schede

Nei documenti di vendita, acquisto, trasferimento e assistenza e in tutte le schede, il campo **Nr.** può essere compilato automaticamente da una numerazione predefinita o puoi aggiungerlo manualmente. Tuttavia, in determinate circostanze, il campo **Nr.** è invisibile per impedirti di modificarlo.  

Il campo **Nr.** può essere compilato in tre modi:

1. Se esiste solo una numerazione per il tipo di documento o scheda e il campo **Proponi automaticamente** è selezionato e il campo **Consenti num. manuale.** non è selezionato per la numerazione, il campo viene compilato automaticamente con il numero successivo della numerazione. Il campo **Nr.** non sarà visibile sulla scheda o sul documento.  

    Anche se definisci i modelli con varie numerazioni per i clienti, se la numerazione definita nella pagina **Setup contabilità clienti** è impostata in questo modo, il campo **Nr.** sarà invisibile sulla scheda cliente, indipendentemente dal modello utilizzato. Lo stesso vale per altri tipi di schede e documenti.  

    > [!NOTE]  
    > Se la numerazione non funziona, ad esempio perché ha raggiunto l'ultimo numero definito per il relativo intervallo, il campo **Nr.** viene visualizzato ed è quindi possibile immettere manualmente un numero. Puoi risolvere i problemi nella pagina **N. serie**.

2. Se hai più di una numerazione per un tipo di documento o scheda e la casella di controllo **Proponi automaticamente** non è selezionata per la numerazione assegnata, il campo **Nr.** viene visualizzato e puoi accedere alla pagina **Nr. serie** e selezionare la numerazione che vuoi utilizzare. Il numero successivo della serie viene quindi inserito nel campo **Nr.**. .

3. Se per un tipo di documento o scheda non è stata impostata alcuna numerazione o se il campo **Consenti num. manuale**è selezionato per la numerazione, il campo **Nr.** viene visualizzato ed è necessario immettere manualmente un numero. In questo campo è possibile immettere fino a un massimo di 20 caratteri alfanumerici.

Quando si apre un nuovo documento o scheda per cui esiste una numerazione, si apre la pagina **Setup numerazione** in modo da poter impostare una numerazione per quel tipo di documento o scheda e continuare a lavorare.

> [!NOTE]  
> Se è necessario attivare la numerazione manuale, ad esempio su nuove schede articolo create con un processo di migrazione di dati che ha nascosto il campo **Nr.** per impostazione predefinita, passare alla pagina **Setup magazzino** e scegliere il campo **Nr. articoli** per aprire e impostare la relativa numerazione su **Consenti num. manuale**.
>
> Lo stesso vale se utilizzi le funzionalità di gestione dell'assistenza. Per risolvere quel problema, passare alla pagina **Impostazione gestione assistenza** e scegliere il campo **Nr. articoli in assistenza** per impostare la numerazione su **Consenti num. manuale**.

## Per creare nuove numerazioni

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Nr. serie**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Scegliere l'azione **Righe**.  
5. Nella pagina **Righe nr. serie**, compilare i campi per definire l'uso effettivo e il contenuto delle numerazioni create nel passaggio 2.  
6. Ripetere il passaggio 5 per tutti i vari usi delle numerazioni necessari. Il campo **Data inizio** definisce quale riga di numerazione è attiva.  

> [!TIP]
> Per consentire agli utenti di specificare i numeri manualmente quando registrano un nuovo cliente o fornitore, ad esempio, scegli il campo **Nr. manuali** sulla numerazione stessa. Per non consentire la numerazione manuale, deseleziona il campo.

Puoi assegnare numerazioni ai modelli che hai impostato per i diversi tipi di cliente e fornitore che i tuoi venditori e acquirenti aggiungono più spesso. In tal caso, imposta la numerazione pertinente, collegala tramite relazioni, quindi aggiungi la prima numerazione nella relazione pertinente alla pagina di configurazione pertinente. Quindi, quando un utente crea un cliente, sceglie il modello pertinente e il nuovo cliente riceve un numero assegnato dalla numerazione definita per quel modello.  

## Per creare relazioni tra numerazioni

È possibile creare relazioni tra codici di numerazioni se ne sono stati impostati più di uno per lo stesso tipo di informazione o transazione di base. Questa funzione può essere utile per selezionare il codice corretto, al momento di utilizzare un numero. Impostando una relazione tra un gruppo di numeri di serie, tutte le numerazioni correlate vengono associate a un solo codice di numerazione. Quindi puoi inserire quel codice in un campo della scheda dettaglio **Numerazione** in una delle pagine di configurazione pertinenti, ad esempio **Setup contabilità clienti**.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Nr. serie**, quindi scegli il collegamento correlato.
2. Selezionare la riga contenente la numerazione per la quale si desidera creare delle relazioni, quindi scegliere **Relazioni**.
3. Nel campo **Codice serie** immettere il codice della numerazione che si desidera associare alla serie selezionata nel passaggio 2.
4. Aggiungere una riga per ogni codice che si desidera associare alla numerazione selezionata.
5. Chiudere la pagina.

Ogni volta che verrà impostato un elemento che richiede un numero, è ora possibile utilizzare le relazioni che sono state create per selezionare la numerazione corretta tra quelle poste in relazione.

## Per impostare le aree in cui la numerazione viene utilizzata

La seguente procedura illustra come impostare una numerazione per l'area delle vendite. I passaggi sono simili per altre aree.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Contabilità clienti**, quindi scegli il collegamento correlato.
2. Nella pagina **Contabilità clienti** nella Scheda dettaglio **Numerazioni**, selezionare la numerazione desiderata per ogni scheda di vendita o documento.

Il numero selezionato risulterà utilizzato per compilare il campo **Nr.** nella scheda o nel documento in questione, in base alle impostazioni effettuate nella riga della numerazione.  

## Vedere anche

[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
