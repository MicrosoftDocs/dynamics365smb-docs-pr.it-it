---
title: Registrare i prezzi di vendita e gli sconti speciali
description: Descrive come definire gli accordi sui prezzi e sugli sconti per i documenti di vendita.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 06/13/2023
ms.custom: bap-template
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '7022, 7024'
ms.service: dynamics-365-business-central
---

# Registrare i prezzi di vendita e gli sconti speciali

> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 sono stati introdotti nuovi processi facilitati per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti che utilizzano l'ultima versione, trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni vedi [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management) nel contenuto per amministratori.

[!INCLUDE[prod_short](includes/prod_short.md)] supporta varie strategie di prezzo, come ad esempio:

* Modelli a prezzo unico in cui un articolo viene venduto sempre allo stesso prezzo.
* Accordi di prezzi speciali con clienti specifici o gruppi di clienti.
* Campagne quando una vendita soddisfa i criteri per un'offerta speciale. Ad esempio, potresti avere i seguenti criteri per un ordine:

  * Soddisfa una quantità minima
  * È prima di una certa data
  * Include un certo tipo di articolo  

Per utilizzare un modello di prezzo di base, è sufficiente specificare un prezzo unitario quando imposti un articolo o una risorsa. Tale prezzo sarà sempre utilizzato sui documenti di vendita. Per i modelli più avanzati, ad esempio, quando desideri offrire prezzi speciali per una campagna di vendita, puoi specificare i criteri nella pagina **Prezzi di vendita**. Puoi offrire prezzi speciali basati su una combinazione delle seguenti informazioni:  

* Cliente
* Articolo
* Unità di misura
* Quantità minima
* Date che definiscono il periodo di validità dei prezzi.

Dopo aver impostato i prezzi speciali, [!INCLUDE[prod_short](includes/prod_short.md)] può calcolare il miglior prezzo sui documenti di vendita e acquisto e sulle righe di registrazione progetto e articolo. Per ulteriori informazioni vedi [Calcolo del miglior prezzo](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Per gli sconti puoi impostare due tipi:

| Tipo di sconto | Descrizione |
| --- | --- |
| **Sconto Riga Vendita** |Aggiungi un importo nelle righe di vendita con una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine. Il tipo è lo stesso dei prezzi di vendita. |
| **Sconto fattura** |Una percentuale di sconto che viene sottratta dal totale nei documenti di vendita se la somma di tutte le righe di un documento supera un determinato valore minimo. |

> [!TIP]  
> Se un articolo non dovrà mai essere venduto a un prezzo scontato, lasciare vuoti i campi relativi allo sconto nella pagina dell'articolo e non includere l'articolo in alcuna impostazione di sconto riga.

## Per impostare un prezzo di vendita per un cliente

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente. 

#### [Esperienza corrente](#tab/current-experience/)

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Scegliere il cliente, quindi l'azione **Prezzi**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà un prezzo di vendita speciale al cliente.

#### [Nuova esperienza](#tab/new-experience/)  

Per default, lo stato dei nuovi listini prezzi è **Bozza**. I listini prezzi in bozza non sono inclusi nel calcolo dei prezzi. Quando hai finito di aggiungere righe e desideri iniziare a usare i prezzi puoi modificare lo stato in **Attivo**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Scegliere il cliente, quindi l'azione **Listini prezzi di vendita**. 
3. Scegliere **Nuovo** per creare un nuovo listino prezzi di vendita.
4. Nelle Schede dettaglio **Generale** e **Imposta** compilare i campi appropriati. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Per aggiungere articoli all'elenco, effettua una delle seguenti operazioni:
   * Per aggiungere molti articoli, scegliere **Suggerisci righe** e quindi immettere i criteri di filtro per specificare i tipi di articolo da aggiungere. Facoltativamente, puoi immettere le impostazioni per gli articoli specifici del listino prezzi. Se necessario, puoi apportare modifiche alle impostazioni in un secondo momento.
   * Per copiare articoli da un altro listino prezzi, scegliere **Copia righe**, quindi scegliere il listino prezzi da copiare.
   * Per aggiungere articoli manualmente, nella griglia, nel campo **Tipo prodotto** selezionare il tipo di prodotto a cui si riferisce il listino prezzi. In base alla selezione, compilare i restanti campi in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Per iniziare a utilizzare il listino prezzi, nel campo **Stato** scegliere **Attivo**.  

---

## Utilizzo dei listini prezzi di vendita e di acquisto

> [!NOTE]
> L'utilizzo dei listini prezzi richiede che l'amministratore abbia abilitato la funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni vedi [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management) nel contenuto per amministratori.

La maggior parte della nuova esperienza sui prezzi di vendita è simile all'esperienza corrente, ma ci sono alcune differenze. Tali differenze sono descritte nelle sezioni riportate di seguito.

I campi **Collega a - Tipo** e **Collega a - Nr.** consentono di scegliere a cosa collegare il listino prezzi, ad esempio al cliente o al gruppo prezzi cliente. Utilizzando **Visualizza colonne per**, puoi mostrare o nascondere le colonne rilevanti per impostare prezzi e sconti oppure prezzi o sconti.

### Conversione dei prezzi esistenti quando si attiva l'aggiornamento della funzionalità dei prezzi

Quando abiliti l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** nella pagina **Gestione funzionalità** si apre la guida **Aggiornamento dati funzionalità**. Utilizza l'interruttore **Usa prezzi predefiniti** come segue:

* Se vuoi lavorare con tutti i prezzi su un'unica pagina, attivalo. I prezzi esistenti vengono convertiti in un listino prezzi predefinito per ciascuno dei seguenti documenti:

  * Vendite
  * Acquisti
  * Ricavi commesse
  * Acquisti commesse

  Puoi modificare tutti i prezzi per queste aree nella pagina **Foglio di lavoro prezzi**. I listini prezzi predefiniti sono impostati nelle pagine **Setup contabilità clienti**, **Setup contabilità fornitori** e **Setup progetti**.

> [!NOTE]
> Se i prezzi sono impostati solo su schede articolo o risorsa, i listini prezzi predefiniti non verranno compilati con tali prezzi durante l'aggiornamento dei dati. Tuttavia, puoi aprire uno qualsiasi dei listini prezzi predefiniti o la pagina **Foglio di lavoro prezzi** e utilizzare l'azione **Suggerisci righe** per aggiungere i prezzi impostati sulle schede articolo o risorsa.

* Per utilizzare i listini prezzi di vendita, disattivala. I prezzi esistenti vengono convertiti in un nuovo listino prezzi predefinito per ciascuna combinazione dei seguenti elementi:

  * Cliente
  * Gruppo di clienti o campagna
  * Date di inizio e fine
  * Valute

Se hai molte combinazioni, avrai molti listini prezzi.

Se hai già abilitato la Nuova esperienza prezzi, puoi creare listini prezzi predefiniti manualmente o specificare un listino prezzi esistente come predefinito. Per impostare un listino prezzi esistente come predefinito, attiva l'interruttore **Consenti aggiornamento impostazioni predefinite** per il listino prezzi. Quindi nelle pagine **Setup contabilità clienti**, **Setup contabilità fornitori** o **Setup progetti** imposta il listino prezzi come predefinito.

### Modifica dei listini prezzi attivi

Per consentire alle persone di modificare i prezzi sui listini prezzi attivi per articoli, risorse, clienti, fornitori o altre entità che utilizzano i prezzi, attiva l'interruttore **Consenti modifica prezzo attivo** nelle pagine **Setup contabilità clienti** e **Setup contabilità fornitori**.

Quando l'interruttore **Consenti modifica prezzo attivo** è disattivato, per aggiornare i prezzi in un listino prezzi è necessario modificare lo stato del listino prezzi in **Bozza**, apportare la modifica, quindi riattivare il listino.

La pagina **Panoramica dei prezzi** fornisce una panoramica di tutti i prezzi nei listini prezzi. Puoi impostare i filtri per limitare l'elenco dei prezzi che potresti voler modificare o aggiungere. Dopo aver modificato i prezzi, è necessario utilizzare l'azione **Verifica righe** per verificare i prezzi rispetto ad altre righe del listino prezzi. La verifica dei prezzi consente di evitare duplicati e ambiguità durante il calcolo dei prezzi.

> [!NOTE]
> Quando modifichi una riga in un listino prezzi attivo, lo stato della riga diventa **Bozza** e la riga non verrà considerata nel calcolo dei prezzi finché non utilizzi l'azione **Verifica righe**. Dopo aver verificato il prezzo, lo stato della riga diventa **Attivo** e verrà considerato nei calcoli del prezzo.

Per aggiungere nuovi prezzi, nella pagina **Panoramica dei prezzi** usa l'azione **Aggiungi nuove righe**. Si apre la pagina **Foglio di lavoro prezzi** e puoi aggiungere le righe di prezzo suggerendole in base a criteri, copiandole da altri listini o inserendole manualmente. Successivamente, puoi utilizzare l'azione **Implementare variazione prezzi** per confrontare i nuovi prezzi con altri listini per evitare duplicati e ambiguità per il calcolo dei prezzi.

#### Creare righe prezzo di vendita in base al prezzo unitario

1. Nella pagina **Prospetto prezzi** scegli l'azione **Suggerisci righe**.
2. Nella pagina **Righe prezzo - Crea nuovo** compila i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nel campo **Filtro prodotto** definisci i filtri per il **Tipo di prodotto** selezionato.
4. Scegli il campo **Impostazioni predefinite** per specificare le impostazioni come:
   * A quali entità sarà assegnato il listino prezzi.
   * Le date in cui il prezzo è valido.
   * Il codice valuta.
   * Il filtro tipo importo che definisce le colonne mostrate nelle righe del listino prezzi.
5. Selezionare **OK**. Nuove righe verranno aggiunte alla pagina **Foglio di lavoro prezzi** con le impostazioni selezionate e i prezzi unitari dalle schede articolo.
6. Modifica le righe create con i nuovi prezzi unitari o gli sconti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Creare righe prezzo di vendita in base ai listini prezzi esistenti

1. Nella pagina **Prospetto prezzi** scegli l'azione **Copia righe**.
2. Sulla pagina **Righe prezzo - Copia esistente** seleziona un listino esistente nel campo **Da listino prezzi**.
3. Nel campo **Filtro riga prezzo**, definisci i filtri per i prodotti del listino prezzi selezionato.
4. Scegli il campo **Impostazioni predefinite** per specificare le impostazioni come:
   * A quali entità sarà assegnato il listino prezzi.
   * Le date in cui il prezzo è valido.
   * Il codice valuta.
   * Il filtro tipo importo che definisce le colonne mostrate nelle righe del listino prezzi.
5. Compila gli altri campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Selezionare **OK**. Nuove righe verranno aggiunte alla pagina **Foglio di lavoro prezzi** con le impostazioni selezionate.
7. Modifica le righe create con i nuovi prezzi unitari o gli sconti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Per copiare prezzi di vendita

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente.

#### [Esperienza corrente](#tab/current-experience/)  

Se si desidera copiare prezzi di vendita, ad esempio i prezzi di vendita di un singolo cliente per poterli utilizzare per un gruppo prezzi cliente, eseguire il processo batch **Suggerisci prezzo vendita in prosp.** nella pagina **Prospetto Prezzi Vendita**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Prospetto prezzi vendita** e quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo vendita in prosp.** .  
3. Nella Scheda dettaglio **Prezzi vendita** immettere i prezzi di vendita originali che si desidera copiare nei campi **Tipo vendita** e **Codice vendita**.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.  
5. Per creare nuovi prezzi mediante il processo batch, selezionare la casella di controllo **Crea nuovi prezzi**.  
6. Seleziona il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per il tipo vendita selezionato.  

   > [!NOTE]  
   > Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella pagina **Prezzo vendita**, scegliere l'azione **Implementare variazione prezzi** nella pagina **Prospetto prezzi vendita**.

#### [Nuova esperienza](#tab/new-experience/)  

Puoi specificare le impostazioni che verranno utilizzate dal listino prezzi:

* Usa le impostazioni dall'intestazione nell'elenco che stai copiando.
* Usa le impostazioni dall'elenco che stai copiando. Per utilizzare le impostazioni del listino in cui stai copiando i prezzi, attiva l'opzione **Utilizzai valori predefiniti dalla destinazione**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Listini prezzi di vendita** e quindi scegli il collegamento correlato.
2. Scegliere il listino prezzi da copiare e quindi scegliere **Copia righe**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Non possono esistere due articoli con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva il listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  
  
---

## Per aggiornare in blocco i prezzi degli articoli

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente.

#### [Esperienza corrente](#tab/current-experience/)

Puoi compilare la pagina Prospetto prezzi vendita per aggiornare in blocco i prezzi degli articoli, come aumentare tutti i prezzi di una determinata percentuale usando il seguente processo:

* **Suggerisci prezzo vendita in prosp.** suggerisce le modifiche in uno dei due modi:

  * Applicando un fattore di rettifica ai prezzi di vendita esistenti.
  * Copiando gli accordi sui prezzi di vendita esistenti per altri clienti, gruppi di prezzi dei clienti o campagne di vendita.

* **Suggerisci prezzo articolo in prosp.** suggerisce le modifiche in uno dei due modi:

  * Applicando un fattore di rettifica ai prezzi unitari di vendita nelle schede articolo.
  * Suggerendo prezzi per nuove combinazioni di valute, unità di misura e così via.

  Questo processo batch non modifica i prezzi unitari sugli articoli.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prezzi vendita** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo articolo in prosp.** .  
3. Nella Scheda dettaglio **Articolo**, riempire il campo **Nr.** o **Categoria registrazione magazzino** o altri campi con i prezzi degli articoli originali che si desidera aggiornare.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.
5. Se vuoi che il processo batch rettifichi automaticamente i prezzi degli articoli suggeriti, immetti la rettifica nel campo **Fattore rettifica**. Ad esempio, immetti 1,15 in **Fattore Rettifica** per aumentare del 15% il prezzo dell'articolo.  
6. Per creare nuovi prezzi mediante il processo batch, attiva l'interruttore **Crea nuovi prezzi**.  
7. Scegli il pulsante **OK** per compilare le righe nella pagina **Foglio di lavoro prezzi di vendita** con i nuovi prezzi suggeriti.
8. Per implementare i suggerimenti, utilizza l'azione **Implementare variazione prezzi**. Il processo batch crea suggerimenti ma non li implementa. 

#### [Nuova esperienza](#tab/new-experience/)

Per aggiornare i prezzi per più articoli, è necessario creare un nuovo listino prezzi e quindi copiare le righe da un listino prezzi esistente. Quando si copiano le righe, è anche possibile utilizzare i filtri per specificare cosa copiare, nonché specificare un numero intero o decimale nel campo **Fattore rettifica** per aumentare o ridurre i prezzi. Il listino prezzi deve essere nello stato **Bozza**. Se necessario, è possibile quindi disattivare il vecchio listino prezzi.

> [!NOTE]
> Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  

---

## Calcolo del prezzo migliore

Dopo aver registrato i prezzi speciai e gli sconti di riga per vendite e acquisti, [!INCLUDE[prod_short](includes/prod_short.md)] calcola automaticamente il miglior prezzo sui documenti di vendita e acquisto e sulle righe di registrazione progetto e articolo.

Con il termine "miglior prezzo" si intende il prezzo più basso ammissibile che gode dello sconto riga più alto possibile praticabile in una specifica data. [!INCLUDE[prod_short](includes/prod_short.md)] calcola il miglior prezzo quando inserisce il prezzo unitario e la percentuale di sconto riga per gli articoli in nuove righe di documenti e di registrazione.

> [!NOTE]  
> Di seguito viene descritto come viene calcolato il prezzo migliore per le vendite. Per gli acquisti il calcolo è simile ma si basa sui parametri disponibili. Ad esempio, i gruppi di sconti articolo non sono supportati per l'acquisto.

1. [!INCLUDE[prod_short](includes/prod_short.md)] controlla la combinazione del cliente di fatturazione e dell'articolo e quindi calcola il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    * Il cliente usufruisce di uno speciale accordo relativo a prezzi o sconti o appartiene a un gruppo che ne usufruisce?
    * L'articolo o il gruppo sconto articolo specificato nella riga è incluso in uno di tali accordi prezzi o sconti?
    * La data è compresa tra la data di inizio e quella di fine dell'accordo relativo a prezzo/sconto? Per fatture e note di credito, questa è la data riportata nel campo **Data di registrazione** nell'intestazione del documento. Per tutti gli altri documenti, è la data nel campo **Data ordine** sulle intestazioni.
    * È stato specificato un codice unità di misura? In caso affermativo, in [!INCLUDE[prod_short](includes/prod_short.md)] verranno controllati i prezzi o gli sconti aventi lo stesso codice di unità di misura, altrimenti verranno verificati prezzi o gli sconti a cui non è associato alcun codice di unità di misura.

2. [!INCLUDE[prod_short](includes/prod_short.md)] controlla se eventuali accordi di prezzo/sconto si applicano alle informazioni sul documento o sulla riga del giornale di registrazione. Quindi inserisce il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    * C'è un requisito di quantità minima nell'accordo di prezzo/sconto che è soddisfatto?
    * C'è un requisito di valuta nell'accordo di prezzo/sconto che è soddisfatto? In caso affermativo, il prezzo più basso e lo sconto riga più alto per tale valuta vengono immessi, anche se la valuta locale fornirebbe un prezzo migliore. Se non esistono accordi prezzi o sconti riga per il codice di valuta specificato, in [!INCLUDE[prod_short](includes/prod_short.md)] verranno automaticamente selezionati il prezzo più basso e lo sconto riga più alto per la valuta locale.

Se non è possibile calcolare alcun prezzo speciale per l'articolo specificato nella riga, viene recuperato l'ultimo costo diretto o il prezzo unitario dalla scheda articolo immesso.

## Sconti fattura di vendita e addebiti assistenza

Quando usi gli sconti fattura, l'importo totale in fattura determina lo sconto applicato. Nella pagina **Sconti fattura clienti** è inoltre possibile aggiungere un addebito di assistenza a fatture che superano un certo importo.  

Prima di utilizzare gli sconti fattura con le vendite si devono specificare varie informazioni. È necessario decidere quanto segue:  

* A quali clienti verrà concesso questo tipo di sconto?  
* Quali percentuali di sconto verranno applicate?  

Se vuoi calcolare automaticamente gli sconti fattura, nella pagina **Setup contabilità clienti** attiva l'interruttore **Calcola sconto fatt.**.  

Per ogni cliente, puoi specificare se offrire sconti in fattura se i criteri della fattura sono soddisfatti. Ad esempio, quando l'importo della fattura è sufficientemente elevato. Gli sconti fattura possono essere in valuta locale per i clienti nazionali o in valuta estera per i clienti esteri.  

Per collegare le percentuali di sconto a importi di fatturazione specifici, utilizza la pagina **Sconti fattura clienti** di ogni cliente. È possibile immettere un numero qualsiasi di percentuali. A ogni cliente è possibile associare una propria pagina oppure è possibile collegare più clienti alla stessa pagina.  

Oltre a oppure invece di una percentuale di sconto, è possibile collegare l'importo di un addebito di assistenza a un importo della fattura specifico.  

> [!TIP]  
> Prima di immettere le informazioni, è opportuno preparare uno schema della struttura di sconto da utilizzare. La struttura consente di determinare più facilmente i clienti che possono essere collegati alla stessa pagina di sconto fattura. Minore è il numero delle pagine da impostare, più veloce risulta l'inserimento delle informazioni principali.

Per informazioni sugli sconti per le vendite, vedi [Impostare gli sconti per i clienti](/training/modules/customer-discounts-dynamics-365-business-central/index).

### Calcolo degli sconti fattura per le vendite

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## Per impostare uno sconto riga vendita per un cliente

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente.

#### [Esperienza corrente](#tab/current-experience/)  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Sconti riga**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà uno sconto riga vendita al cliente.

> [!NOTE]
> Quando si aprono le pagine **Prezzi vendita** e **Sconti riga vendita** di un cliente specifico, i campi **Filtro tipo vendita** e **Filtro codice vendita** sono impostati per il cliente e non possono essere modificati né rimossi.
>
> Per impostare i prezzi o gli sconti riga per tutti i clienti, un gruppo di prezzi dei clienti o una campagna, è necessario aprire le pagine da una scheda articolo. In alternativa, per i prezzi di vendita, utilizzare la pagina **Prospetto Prezzi Vendita**. Per ulteriori informazioni, vedi [Per aggiornare in blocco i prezzi degli articoli](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Nuova esperienza](#tab/new-experience/)  

1. Scegli l'icona ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Clienti** e quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Listini prezzi di vendita**.
3. Aprire il listino prezzi per il quale specificare lo sconto riga.
4. Creare una nuova riga o scegliere una riga esistente, quindi compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Nel campo **Definisce** scegliere **Prezzo e sconto** o solo **Sconto**. 
6. Nel campo **% sconto riga** specificare la percentuale di sconto.

    > [!TIP]
    > Se si modifica una riga esistente, è possibile filtrare le righe scegliendo l'opzione appropriata nel campo **Visualizza colonne per**.

    > [!NOTE]  
    > I codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni. Per impostare le condizioni di sconto fattura specifiche del cliente, impostare il campo **Codice sconto fattura** sul codice cliente del cliente, quindi procedere al passaggio successivo.

---

## Per impostare uno sconto fattura per un cliente

Dopo avere stabilito a quali clienti si devono applicare gli sconti fattura, è necessario immettere i codici di sconto fattura nelle pagine scheda cliente. Quindi imposta le condizioni per ogni codice.

1. Scegli l'icona ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Clienti** e quindi scegli il collegamento correlato.
2. Aprire la pagina relativa al cliente al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il cliente.

> [!NOTE]  
> I codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni.

Continua a impostare le nuove condizioni dello sconto fattura di vendita.

1. Nella pagina **Clienti** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura clienti**.
2. Nel campo **Codice valuta** immetti il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
3. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
4. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
5. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

## Vedere anche

[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Impostazione di gruppi di prezzi dei clienti](sales-how-to-set-up-customer-price-groups.md)  
[Impostazione delle categorie sconto clienti](sales-how-to-set-up-customer-discount-groups.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
